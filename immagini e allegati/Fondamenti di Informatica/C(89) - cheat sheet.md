

> [!note] Come leggere i frammenti
> Gli snippet sono illustrativi: in un programma reale ricorda che in C89 **le dichiarazioni vanno sempre a inizio blocco** e i commenti sono solo `/* ... */`.

## Indice

- [[#1. Regole e struttura del programma|1. Regole e struttura del programma]]
- [[#2. Preprocessore|2. Preprocessore]]
- [[#3. Tipi, costanti e variabili|3. Tipi, costanti e variabili]]
- [[#4. Operatori e conversioni|4. Operatori e conversioni]]
- [[#5. Costrutti di controllo|5. Costrutti di controllo]]
- [[#6. Array|6. Array]]
- [[#7. Stringhe|7. Stringhe]]
- [[#8. Puntatori|8. Puntatori]]
- [[#9. Gestione della memoria|9. Gestione della memoria]]
- [[#10. Funzioni|10. Funzioni]]
- [[#11. Struct, union, enum, typedef|11. Struct, union, enum, typedef]]
- [[#12. Liste concatenate|12. Liste concatenate (stack e queue)]]
- [[#13. Gestione dei file|13. Gestione dei file]]
- [[#14. Argomenti da linea di comando|14. Argomenti da linea di comando]]
- [[#15. Libreria standard|15. Libreria standard (15 header)]]
- [[#16. Programma integrato|16. Programma integrato]]
- [[#17. Limiti del C89 ed errori tipici|17. Limiti del C89, errori, checklist]]

---

## 1. Regole e struttura del programma

### 1.1 Le dieci regole d'oro

| #   | Regola                                                                              |
| --- | ----------------------------------------------------------------------------------- |
| 1   | Commenti **solo** `/* ... */`, non annidabili, niente `//`                          |
| 2   | In ogni blocco `{ }` le **dichiarazioni precedono tutte le istruzioni**             |
| 3   | `main` deve fare `return 0;` **esplicito** (non è implicito come in C99)            |
| 4   | Ogni istruzione finisce con `;` — i blocchi `{ }` no                                |
| 5   | Case sensitive: `Variabile` ≠ `variabile`                                           |
| 6   | Identificatori: `[A-Za-z_][A-Za-z0-9_]*` (31 char significativi interni, 6 esterni) |
| 7   | Niente `long long`, `bool`, VLA, `inline`, initializzatori designati                |
| 8   | Indici array da `0` a `n-1`, **nessun controllo** dei limiti                        |
| 9   | Le stringhe sono `char[]` terminati da `'\0'`                                       |
| 10  | Il passaggio dei parametri è **sempre per valore**                                  |

### 1.2 Esempio di programma minimo

```c
#include <stdio.h>              /* 1. direttive preprocessore */

#define MAX 100                 /* 2. macro / costanti simboliche */

typedef struct { int x, y; } Punto;   /* 3. tipi */

static int contatore = 0;       /* 4. variabili globali */

int area(int b, int h);         /* 5. prototipi */

int main(void){                 /* 6. punto di ingresso */

    int r;                      /* 7. dichiarazioni locali */
    r = area(3, 4);             /* 8. istruzioni */
    printf("area = %d\n", r);
    return 0;
}

int area(int b, int h){         /* 9. definizioni */

    return b * h;
}
```

### 1.3 Organizzazione multi-file

> [!tip] Caso d'uso
> Progetti modulari: l'header espone l'interfaccia, il `.c` nasconde l'implementazione con `static`.

```c
/* ---- geometria.h ---- */
#ifndef GEOMETRIA_H             /* include guard: obbligatorio di fatto */
#define GEOMETRIA_H

#define PI 3.14159265358979

typedef struct { double x, y; } Punto;

extern int chiamate;            /* DICHIARAZIONE (definita nel .c) */
double distanza(Punto a, Punto b);
void   stampa(Punto p);

#endif
```

```c
/* ---- geometria.c ---- */
#include <stdio.h>
#include <math.h>
#include "geometria.h"

int chiamate = 0;               /* DEFINIZIONE */

static double quad(double x)    /* static = privata al file */
{
    return x * x;
}

double distanza(Punto a, Punto b)
{
    chiamate++;
    return sqrt(quad(a.x - b.x) + quad(a.y - b.y));
}

void stampa(Punto p) { printf("(%g, %g)\n", p.x, p.y); }
```

```c
/* ---- main.c ---- */
#include <stdio.h>
#include "geometria.h"

int main(void)
{
    Punto a = {0.0, 0.0}, b = {3.0, 4.0};
    printf("d = %g (chiamate: %d)\n", distanza(a, b), chiamate);
    return 0;
}
```

```bash
gcc -std=c89 -pedantic main.c geometria.c -lm -o geo
```


---

## 2. Preprocessore

| Direttiva | Sintassi | Caso d'uso |
|---|---|---|
| `#include` | `<stdio.h>` / `"mio.h"` | sistema / file locale |
| `#define` | `#define N 10` | costante simbolica |
| macro funzione | `#define MAX(a,b) ((a)>(b)?(a):(b))` | pseudo-funzione inline |
| `#undef` | `#undef N` | rimuovere macro |
| `#if/#elif/#else/#endif` | `#if N > 10` | compilazione condizionale |
| `#ifdef` / `#ifndef` | `#ifdef DEBUG` | test esistenza macro |
| `defined()` | `#if defined(A) && !defined(B)` | condizioni composte |
| `#error` | `#error "serve C89"` | bloccare build errate |
| `#line` | `#line 1 "f.c"` | codice generato |
| `#pragma` | implementation-defined | opzioni del compiler |

```c
#define PI 3.14159
#define QUAD(x) ((x)*(x))          /* parentesi SEMPRE: QUAD(1+1) deve dare 4 */
#define STR(x) #x                  /* stringifica: STR(ciao) -> "ciao" */
#define CAT(a,b) a##b              /* incolla token: CAT(var,1) -> var1 */
#define NEL(a) (sizeof(a)/sizeof((a)[0]))   /* n. elementi di un array VERO */
#define SWAP(t,a,b) do { t tmp_=(a); (a)=(b); (b)=tmp_; } while (0)

#ifdef DEBUG
#  define LOG(msg) fprintf(stderr, "%s:%d: %s\n", __FILE__, __LINE__, (msg))
#else
#  define LOG(msg) ((void)0)       /* si annulla senza effetti collaterali */
#endif

#if !defined(__STDC__)
#  error "Compilatore non conforme ANSI C"
#endif
```

**Macro predefinite C89:** `__FILE__` `__LINE__` `__DATE__` `__TIME__` `__STDC__` (=1).

> [!warning] Trappole
> - `__func__` è C99, **non** C89.
> - Le macro sono **testuali**: `QUAD(i++)` incrementa due volte!
> - Macro multi-istruzione: sempre `do { ... } while (0)`.


---

## 3. Tipi, costanti e variabili

### 3.1 Tipi fondamentali

| Tipo | Min. garantito | Range tipico (32/64 bit) |
|---|---|---|
| `char` | 8 bit | −128..127 o 0..255 (implementation-defined) |
| `signed char` / `unsigned char` | 8 bit | −128..127 / 0..255 |
| `short` | 16 bit | −32768..32767 |
| `int` | 16 bit | −2147483648..2147483647 |
| `long` | 32 bit | ±2·10⁹ (64 bit su Linux/64) |
| `unsigned short/int/long` | idem | 0..2ⁿ−1, aritmetica modulare |
| `float` | 6 cifre | ~1e−38..1e38 |
| `double` | 10 cifre | ~1e−308..1e308 |
| `long double` | ≥ double | 80/128 bit |
| `enum` | compatibile con intero | |
| `void` | incompleto | solo `void *` e funzioni senza ritorno |

Modificatori: `signed` `unsigned` `short` `long` — Qualificatori: `const` `volatile`.

### 3.2 Costanti

```c
42        012        0x2A          /* dec, ottale (=10), esadecimale (=42) */
42U       42L        42UL          /* unsigned, long, unsigned long */
3.14      3.14f      3.14L         /* double, float, long double */
1e-3      .5         5.            /* notazione scientifica */
'a'       '\n'       '\0'          /* carattere: in C ha tipo int! */
"ciao"                             /* char[5] con '\0' finale */
enum { ROSSO, VERDE = 5, BLU };    /* 0, 5, 6 — NO virgola finale in C89 */
```

**Escape:** `\a \b \f \n \r \t \v \\ \' \" \? \0` · `\123` ottale · `\x1F` esadecimale.
Stringhe adiacenti si concatenano: `"ciao " "mondo"`.

### 3.3 Anatomia di una dichiarazione

```text
[classe-di-memorizzazione] [qualificatori] tipo dichiaratore [= init] ;
```

```c
int x = 3, y = 4;                /* più variabili, stessa base */
const double pi = 3.14159;       /* sola lettura */
volatile int flag_hw;            /* può cambiare fuori dal flusso (ISR, hardware) */
static int privato;              /* linkage interno (globale) o durata permanente (locale) */
extern int globale;              /* definita in altro file */
register int i;                  /* richiesta registro: non puoi fare &i */
typedef unsigned long ulong;     /* alias di tipo */
typedef int (*Confronto)(const void *, const void *);
```

| Classe | Durata | Visibilità | Linkage | Caso d'uso |
|---|---|---|---|---|
| `auto` (default locale) | blocco | blocco | — | normali locali |
| `register` | blocco | blocco | — | contatori critici |
| `static` locale | programma | blocco | — | contatore che "ricorda" tra chiamate |
| `static` globale | programma | file | interno | incapsulazione di modulo |
| globale / `extern` | programma | programma | esterno | dati condivisi (con parsimonia) |

```c
int progressivo(void)            /* caso d'uso: stato persistente */
{
    static int n = 0;            /* inizializzata UNA volta, vale 0 di default */
    return ++n;
}
```

### 3.4 Inizializzazione

```c
int a[5] = {1, 2, 3};            /* a[3]=a[4]=0 */
int z[10] = {0};                 /* tutto a zero */
int m[2][3] = {{1,2,3},{4,5,6}};
char s[] = "ciao";               /* dimensione 5 */
struct P { int x, y; } p = {1, 2};
union U { int i; double d; } u = {7};   /* solo il PRIMO membro */
static int g;                    /* 0 automaticamente (durata statica) */
int loc;                         /* INDETERMINATO: leggerlo = UB */
```

> [!warning] C89
> - Non esistono `{.x = 1}` né `{[2] = 5}` (C99).
> - `const int n = 10;` **non** rende `n` una costante usabile come dimensione di array: usa `#define` o `enum`.

**Costanti: quale usare?** `#define` (testuale, no tipo) · `enum` (interi, debug-friendly) · `const` (tipizzato, sola lettura).


---

## 4. Operatori e conversioni

### 4.1 Precedenza (1 = più alta) e associatività

| P. | Operatori | Ass. |
|---|---|---|
| 1 | `f()` `a[i]` `s.x` `p->x` `x++` `x--` | → |
| 2 | `++x` `--x` `+x` `-x` `!` `~` `*p` `&x` `sizeof` `(tipo)x` | ← |
| 3 | `*` `/` `%` | → |
| 4 | `+` `-` | → |
| 5 | `<<` `>>` | → |
| 6 | `<` `<=` `>` `>=` | → |
| 7 | `==` `!=` | → |
| 8 | `&` | → |
| 9 | `^` | → |
| 10 | `\|` | → |
| 11 | `&&` (short-circuit) | → |
| 12 | `\|\|` (short-circuit) | → |
| 13 | `?:` | ← |
| 14 | `=` `+=` `-=` `*=` `/=` `%=` `<<=` `>>=` `&=` `^=` `\|=` | ← |
| 15 | `,` | → |

### 4.2 Esempi per categoria

```c
/* aritmetici */    q = a / b;  r = a % b;      /* % SOLO interi */
/* relazionali */   if (a <= b) ...             /* producono int 0/1 */
/* logici */        if (p != NULL && p->v > 0)  /* && valuta p->v solo se p!=NULL */
/* bit a bit */     f |=  (1u << 3);            /* set bit 3   */
                    f &= ~(1u << 3);            /* clear bit 3 */
                    f ^=  (1u << 3);            /* toggle      */
                    if (f & (1u << 3)) ...      /* test        */
/* incremento */    a[i++] = 0;                 /* usa i, poi incrementa */
/* condizionale */  max = (a > b) ? a : b;
/* assegnamento */  tot += x;  n <<= 1;
/* virgola */       for (i = 0, j = n; i < j; i++, j--) ...
/* sizeof */        n = sizeof(int);  m = sizeof a / sizeof a[0];
```

### 4.3 Conversioni

```c
media = (double) somma / n;      /* cast: evita la divisione intera */
c = (char) (i & 0xFF);
```

- **Integer promotions:** `char`/`short` → `int` in ogni espressione.
- **Usual arithmetic conversions:** verso il tipo più ampio; a pari rango `unsigned` vince.
- **Default argument promotions** (funzioni senza prototipo e `...`): `char/short`→`int`, `float`→`double`. Per questo `printf("%f", x)` accetta anche un `float`.

> [!danger] Comportamento indefinito / insidie
> - `if (-1 < 1u)` è **falso** (conversione a unsigned).
> - C89: `/` e `%` con operandi negativi → arrotondamento e segno *implementation-defined*.
> - Sequence point: `i = i++;`, `a[i] = i++;`, `f(i++, i++)` sono **UB**.
> - Shift con conteggio negativo o ≥ ampiezza del tipo: UB.


---

## 5. Costrutti di controllo

```c
/* ---- selezione ---- */
if (n > 0)        { ... }
else if (n == 0)  { ... }
else              { ... }

switch (comando) {               /* solo espressioni intere/caratteri */
    case 'a':
    case 'A':  aggiungi(); break;   /* etichette costanti, fall-through */
    case 'q':  esci();     break;
    default:   errore();   break;
}

/* ---- iterazione ---- */
while (fgets(r, sizeof r, f) != NULL) { ... }   /* n. giri ignoto */

do {                                            /* almeno 1 giro: menu */
    printf("Scelta: ");
    n = leggi();
} while (n < 1 || n > 5);

for (i = 0; i < n; i++) { ... }                 /* n. giri noto */
for (i = 0, j = n - 1; i < j; i++, j--) { ... }
for (;;) { ... }                                /* infinito */

/* ---- salti ---- */
break;        /* esce dal ciclo/switch più interno */
continue;     /* salta al prossimo giro (nel for esegue comunque i++) */
goto errore;  /* solo dentro la stessa funzione */
return expr;  /* esce dalla funzione */

errore:
    pulisci();
    return EXIT_FAILURE;
```

> [!tip] Caso d'uso legittimo del `goto`
> Cleanup centralizzato delle risorse (unico idioma ampiamente accettato in C).

```c
int elabora(const char *file)
{
    FILE *f = NULL;
    char *buf = NULL;
    int esito = -1;

    f = fopen(file, "r");
    if (f == NULL) goto fine;
    buf = malloc(1024);
    if (buf == NULL) goto fine;
    /* ... lavoro ... */
    esito = 0;
fine:
    free(buf);                   /* free(NULL) è lecito */
    if (f != NULL) fclose(f);
    return esito;
}
```

> [!warning] C89: dichiarazioni solo a inizio blocco
> ```c
> {
>     int a = 1;
>     printf("%d\n", a);
>     /* int b = 2;  <-- ERRORE */
>     { int b = 2; printf("%d\n", b); }   /* OK: nuovo blocco */
> }
> /* for (int i = 0; ...)  <-- ERRORE: dichiara i prima */
> ```


---

## 6. Array

### 6.1 Sintassi

```c
int v[10];                        /* indici 0..9 */
double m[3][4];                   /* matrice, memorizzata per righe */
int t[2][3][4];                   /* 3D */
int a[] = {1, 2, 3};              /* dimensione dedotta = 3 */
int z[100] = {0};                 /* azzeramento */
char nome[32];                    /* buffer per stringa di max 31 char + '\0' */

v[0] = 5;  m[1][2] = 3.0;
n = sizeof v / sizeof v[0];       /* numero elementi (solo array veri!) */
```

### 6.2 Array e funzioni

```c
/* l'array DECADE a puntatore: la dimensione va passata a parte */
double media(const int v[], int n)     /* equivalente a: const int *v */
{
    double s = 0.0;
    int i;
    for (i = 0; i < n; i++) s += v[i];
    return n > 0 ? s / n : 0.0;
}

/* matrice: tutte le dimensioni tranne la prima vanno specificate */
void stampa_mat(int m[][4], int righe)
{
    int i, j;
    for (i = 0; i < righe; i++) {
        for (j = 0; j < 4; j++) printf("%4d", m[i][j]);
        putchar('\n');
    }
}
```

### 6.3 Casi d'uso classici

```c
/* ricerca lineare */
int cerca(const int v[], int n, int x)
{
    int i;
    for (i = 0; i < n; i++) if (v[i] == x) return i;
    return -1;
}

/* ricerca binaria (array ordinato) */
int bsearch_int(const int v[], int n, int x)
{
    int lo = 0, hi = n - 1, mid;
    while (lo <= hi) {
        mid = lo + (hi - lo) / 2;
        if (v[mid] == x) return mid;
        if (v[mid] < x) lo = mid + 1; else hi = mid - 1;
    }
    return -1;
}

/* inversione in place */
void inverti(int v[], int n)
{
    int i, t;
    for (i = 0; i < n / 2; i++) { t = v[i]; v[i] = v[n-1-i]; v[n-1-i] = t; }
}

/* istogramma / counting: array come tabella di frequenza */
int freq[26] = {0};
if (c >= 'a' && c <= 'z') freq[c - 'a']++;

/* lookup table al posto di switch */
static const char *giorni[] = {"lun","mar","mer","gio","ven","sab","dom"};
printf("%s\n", giorni[g]);
```

> [!warning] Limiti
> - **No VLA** in C89: `int v[n];` con `n` variabile è illegale → `malloc` ([[#9. Gestione della memoria|§9]]).
> - Array non assegnabili (`a = b;`) né confrontabili (`a == b` confronta indirizzi) → cicli / `memcpy` / `memcmp`.
> - `a[10]` su `int a[10]` è UB, non un errore diagnosticato.


---

## 7. Stringhe

### 7.1 Modello

```c
char s1[] = "ciao";     /* array COPIA, modificabile, sizeof = 5, strlen = 4 */
char *s2  = "ciao";     /* puntatore a LETTERALE: modificarlo è UB */
char buf[10];           /* spazio per 9 caratteri + '\0' */
/* 'a' != "a": il secondo è un array di 2 char */
```

### 7.2 Riferimento string.h

| Funzione | Prototipo | Note |
|---|---|---|
| `strlen` | `size_t strlen(const char *s)` | esclude `'\0'`, O(n) |
| `strcpy` | `char *strcpy(char *d, const char *s)` | **nessun** controllo dimensione |
| `strncpy` | `char *strncpy(char *d, const char *s, size_t n)` | **non** termina con `\0` se truncata! |
| `strcat` / `strncat` | `char *strcat(char *d, const char *s)` | `d` deve avere spazio |
| `strcmp` / `strncmp` | `int strcmp(const char *a, const char *b)` | <0, 0, >0 |
| `strchr` / `strrchr` | `char *strchr(const char *s, int c)` | prima / ultima occorrenza |
| `strstr` | `char *strstr(const char *h, const char *n)` | sottostringa |
| `strtok` | `char *strtok(char *s, const char *sep)` | **modifica `s`**, stato statico |
| `strspn`/`strcspn`/`strpbrk` | — | prefissi / insiemi di caratteri |
| `memcpy` | `void *memcpy(void *d, const void *s, size_t n)` | aree **non** sovrapposte |
| `memmove` | `void *memmove(void *d, const void *s, size_t n)` | anche sovrapposte |
| `memset` | `void *memset(void *d, int c, size_t n)` | riempie byte |
| `memcmp` / `memchr` | — | confronto / ricerca su byte |
| `strerror` | `char *strerror(int err)` | descrizione errore |
| `strcoll` / `strxfrm` | — | confronto secondo la locale |

### 7.3 Casi d'uso

```c
#include <string.h>
#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>
#include <errno.h>

/* --- copia sicura (idioma C89, senza snprintf che è C99) --- */
char dst[16];
strncpy(dst, src, sizeof dst - 1);
dst[sizeof dst - 1] = '\0';

/* --- concatenazione controllata --- */
char riga[64];
strcpy(riga, "nome=");
strncat(riga, nome, sizeof riga - strlen(riga) - 1);

/* --- costruzione con sprintf (buffer abbastanza grande!) --- */
char msg[128];
sprintf(msg, "%s:%d -> %g", file, linea, valore);

/* --- confronto (MAI usare == ) --- */
if (strcmp(cmd, "esci") == 0) ...
if (strncmp(cmd, "set", 3) == 0) ...          /* prefisso */

/* --- tokenizzare CSV --- */
char csv[] = "anna;28;roma";
char *tok = strtok(csv, ";");
while (tok != NULL) { printf("[%s]\n", tok); tok = strtok(NULL, ";"); }

/* --- togliere il newline di fgets --- */
riga[strcspn(riga, "\n")] = '\0';

/* --- trovare estensione --- */
char *punto = strrchr(nomefile, '.');
if (punto != NULL && strcmp(punto, ".txt") == 0) ...

/* --- stringa → numero con controllo errori --- */
char *fine;
long n;
errno = 0;
n = strtol(testo, &fine, 10);
if (fine == testo || *fine != '\0' || errno == ERANGE) { /* non valido */ }

/* --- numero → stringa --- */
char num[32];
sprintf(num, "%ld", n);

/* --- minuscole / pulizia --- */
for (p = s; *p != '\0'; p++) *p = (char)tolower((unsigned char)*p);
```

```c
/* --- duplicare una stringa: strdup NON è C89 --- */
char *duplica(const char *s)
{
    char *c = malloc(strlen(s) + 1);
    if (c != NULL) strcpy(c, s);
    return c;
}

/* --- versioni "fatte a mano" per capire i puntatori --- */
size_t mia_strlen(const char *s)
{
    const char *p = s;
    while (*p) p++;
    return (size_t)(p - s);
}

char *mia_strcpy(char *d, const char *s)
{
    char *r = d;
    while ((*d++ = *s++) != '\0') ;
    return r;
}
```

> [!warning] Trappole sulle stringhe
> `gets()` (insicuro, usa `fgets`) · `scanf("%s", s)` senza limite (usa `%31s`) · `strncpy` senza terminatore · `strtok` su letterali o annidato · `strlen` dentro il ciclo (O(n²)) · dimenticare `+1` per `'\0'`.


---

## 8. Puntatori

### 8.1 Sintassi fondamentale

```c
int x = 5;
int *p = &x;        /* & = indirizzo di */
*p = 7;             /* * = dereferenziazione: x ora vale 7 */
int **pp = &p;      /* puntatore a puntatore */
**pp = 9;

void *g = &x;       /* generico: conversione implicita da/in ogni tipo oggetto */
int *q = g;         /* in C non serve il cast */

int *nullo = NULL;  /* non punta a nulla: dereferenziarlo = crash/UB */
if (p != NULL) { ... }
```

### 8.2 const e puntatori (leggere da destra)

```c
int *p;                     /* puntatore a int: tutto modificabile */
const int *p;               /* puntatore a int COSTANTE: *p non modificabile */
int *const p = &x;          /* puntatore COSTANTE a int: p non riassegnabile */
const int *const p = &x;    /* nessuno dei due modificabile */
```

Caso d'uso: parametri in sola lettura → `void f(const char *s)`, `int somma(const int v[], int n)`.

### 8.3 Aritmetica

```c
#include <stddef.h>          /* ptrdiff_t */

int a[5] = {10,20,30,40,50};
int *p = a;                  /* a decade a &a[0] */
p++;                         /* avanza di sizeof(int) byte → a[1] */
*p += 5;                     /* a[1] = 25 */
ptrdiff_t d = &a[4] - p;     /* 3 (tipo con segno) */
/* a[i] == *(a+i) == *(i+a) == p[i] */

/* scandire con puntatore (idioma efficiente) */
int *fine = a + 5;
for (p = a; p < fine; p++) printf("%d ", *p);
```

Lecito: puntare **dentro** lo stesso array (o uno oltre la fine, senza dereferenziare). Confronti/differenze tra array diversi = UB.

### 8.4 Array vs puntatore

```c
char s[10];      /* sizeof = 10, &s tipo char(*)[10], non riassegnabile */
char *p = s;     /* sizeof = 4/8, &p tipo char**, riassegnabile */
/* parametro: void f(char s[10]) è ESATTAMENTE void f(char *s) */
int (*pa)[10] = &a;   /* puntatore a INTERO array: (*pa)[3] */
```

### 8.5 Casi d'uso

```c
/* 1. modificare l'argomento (out-parameter) */
void scambia(int *a, int *b) { int t = *a; *a = *b; *b = t; }
/* scambia(&x, &y); */

/* 2. restituire più valori */
int dividi(int a, int b, int *resto)
{
    if (b == 0) return 0;
    *resto = a % b;
    return a / b;
}

/* 3. restituire memoria allocata */
int *crea_vettore(int n) { return malloc((size_t)n * sizeof(int)); }

/* 4. modificare un puntatore del chiamante (doppio puntatore) */
void alloca(char **out, size_t n) { *out = malloc(n); }
/* char *s; alloca(&s, 100); */

/* 5. puntatori a funzione: callback e tabelle di dispatch */
int (*f)(int, int) = somma;
int r = f(2, 3);                    /* oppure (*f)(2,3) */

typedef int (*Op)(int, int);
Op tabella[4] = { add, sub, mul, dvd };
r = tabella[op](a, b);              /* sostituisce uno switch */

void applica(int v[], int n, int (*trasforma)(int))
{
    int i;
    for (i = 0; i < n; i++) v[i] = trasforma(v[i]);
}
```


---

## 9. Gestione della memoria

### 9.1 Le quattro funzioni (stdlib.h)

| Funzione | Prototipo | Comportamento |
|---|---|---|
| `malloc` | `void *malloc(size_t n)` | `n` byte **non** inizializzati; `NULL` se fallisce |
| `calloc` | `void *calloc(size_t nm, size_t sz)` | `nm*sz` byte **azzerati**; controlla overflow |
| `realloc` | `void *realloc(void *p, size_t n)` | ridimensiona, può **spostare** il blocco; `realloc(NULL,n)` = malloc |
| `free` | `void free(void *p)` | rilascia; `free(NULL)` è lecito e non fa nulla |

### 9.2 Pattern corretti

```c
/* --- array dinamico (sostituisce il VLA vietato in C89) --- */
int n = 1000;
int *v = malloc((size_t)n * sizeof *v);   /* sizeof *v: robusto ai cambi di tipo */
if (v == NULL) { perror("malloc"); exit(EXIT_FAILURE); }
/* ... v[i] ... */
free(v);
v = NULL;                                /* evita dangling pointer */

/* --- struct --- */
Nodo *p = malloc(sizeof *p);              /* NON sizeof(Nodo*) ! */

/* --- crescita con realloc (pattern sicuro) --- */
int *tmp = realloc(v, (size_t)nuovo * sizeof *v);
if (tmp == NULL) { free(v); return -1; }  /* v è ancora valido: non perderlo! */
v = tmp;
```

```c
/* --- matrice dinamica: blocco unico (veloce, 1 free) --- */
int *dati = malloc((size_t)righe * colonne * sizeof *dati);
#define EL(i,j) dati[(i)*colonne + (j)]
EL(2,3) = 7;
free(dati);

/* --- matrice dinamica: array di puntatori (righe di lunghezza diversa) --- */
int **m = malloc((size_t)righe * sizeof *m);
if (m == NULL) exit(EXIT_FAILURE);
for (i = 0; i < righe; i++) {
    m[i] = malloc((size_t)colonne * sizeof **m);
    if (m[i] == NULL) { /* libera le precedenti e esci */ }
}
for (i = 0; i < righe; i++) free(m[i]);
free(m);
```

```c
/* --- vettore dinamico che cresce (caso d'uso: lettura di n ignoto) --- */
typedef struct { int *d; size_t n, cap; } Vettore;

void v_init(Vettore *v) { v->d = NULL; v->n = v->cap = 0; }

int v_push(Vettore *v, int x)
{
    if (v->n == v->cap) {
        size_t nc = v->cap ? v->cap * 2 : 8;
        int *t = realloc(v->d, nc * sizeof *v->d);
        if (t == NULL) return 0;
        v->d = t; v->cap = nc;
    }
    v->d[v->n++] = x;
    return 1;
}

void v_free(Vettore *v) { free(v->d); v->d = NULL; v->n = v->cap = 0; }
```

### 9.3 Regole e errori

| Errore | Conseguenza / rimedio |
|---|---|
| non controllare `NULL` | crash su memoria esaurita |
| `sizeof(puntatore)` invece di `sizeof *p` | alloca 4/8 byte invece della struct |
| usare memoria dopo `free` | *use-after-free*, UB → azzera il puntatore |
| doppio `free` | corruzione heap |
| perdere l'ultimo puntatore | *memory leak* |
| `free` su puntatore non heap | UB |
| `return buf;` con `char buf[32]` locale | puntatore a stack morto → `malloc` o buffer del chiamante |
| `realloc` fallito assegnato a `p` | leak: usa una temporanea |
| dimenticare `+1` per il `'\0'` | overflow di 1 byte |

> [!tip] Verifica
> ```bash
> valgrind --leak-check=full ./prog
> ```
> **Stack vs heap:** locali = stack (automatici, limitati, veloci); `malloc` = heap (grandi, durata controllata, più lento).


---

## 10. Funzioni

### 10.1 Dichiarazione e definizione

```c
/* prototipo ANSI (sempre preferibile: abilita il controllo dei tipi) */
int    max(int a, int b);
void   f(void);                  /* NESSUN parametro */
void   g();                      /* parametri NON specificati: nessun controllo */
double media(const double v[], int n);
int    printf(const char *fmt, ...);
static int helper(int x);        /* privata al file */

int max(int a, int b) { return a > b ? a : b; }

/* stile K&R: legale ma obsoleto */
int max(a, b)
int a; int b;
{ return a > b ? a : b; }
```

> [!warning] C89
> Una funzione chiamata senza dichiarazione si assume implicitamente `int f()`: bug silenziosi. **Dichiara sempre.**

### 10.2 Parametri e ritorno

```c
void f(int x)         { x = 10; }        /* per valore: il chiamante non cambia */
void f2(int *x)       { *x = 10; }       /* effetto "per riferimento" */
void f3(int v[])      { v[0] = 10; }     /* array = puntatore: modifica reale */
void f4(struct P p)   { p.x = 1; }       /* struct per valore: COPIA */
void f5(struct P *p)  { p->x = 1; }      /* per indirizzo: modifica + efficiente */
struct P f6(void)     { struct P r = {1,2}; return r; }  /* ritorno per valore: OK */
int *f7(void)         { return malloc(10 * sizeof(int)); } /* heap: OK */
```

### 10.3 Ricorsione

```c
long fatt(int n) { return n <= 1 ? 1L : n * fatt(n - 1); }

int fib(int n) { return n < 2 ? n : fib(n-1) + fib(n-2); }   /* esponenziale! */

void hanoi(int n, char da, char a, char via)
{
    if (n == 0) return;
    hanoi(n - 1, da, via, a);
    printf("%c -> %c\n", da, a);
    hanoi(n - 1, via, a, da);
}

/* conteggio ricorsivo su lista */
int conta(Nodo *p) { return p == NULL ? 0 : 1 + conta(p->next); }
```

Ogni chiamata ha il proprio frame: attenzione a profondità (stack overflow) e ricalcoli.

### 10.4 Funzioni variadiche (stdarg.h)

```c
#include <stdarg.h>

int somma_n(int n, ...)              /* almeno 1 parametro nominale */
{
    va_list ap;
    int i, tot = 0;
    va_start(ap, n);
    for (i = 0; i < n; i++)
        tot += va_arg(ap, int);      /* MAI va_arg(ap, float/char): usa double/int */
    va_end(ap);
    return tot;
}

/* caso d'uso: wrapper di logging */
void logmsg(const char *fmt, ...)
{
    va_list ap;
    fprintf(stderr, "[LOG] ");
    va_start(ap, fmt);
    vfprintf(stderr, fmt, ap);       /* versioni v* per inoltrare */
    va_end(ap);
    fputc('\n', stderr);
}
```

### 10.5 main

```c
int main(void) { return 0; }
int main(int argc, char *argv[]) { /* ... */ return EXIT_SUCCESS; }
```

`return` da `main` ≡ `exit(codice)`. Codici: `0`/`EXIT_SUCCESS` = ok, `EXIT_FAILURE` = errore. Gli handler `atexit()` vengono eseguiti all'uscita normale (non con `abort`).


---

## 11. Struct, union, enum, typedef

```c
/* --- struct: record eterogeneo --- */
struct Punto { int x, y; };

typedef struct Studente {
    char  nome[32];
    int   voto;
    struct Studente *next;      /* autoriferimento: base delle liste */
} Studente;

Studente a = {"anna", 28, NULL};
Studente b = a;                 /* COPIA dei membri (i puntatori copiano
                                   solo l'indirizzo: shallow copy!) */
Studente *p = &a;
p->voto = 30;                   /* ≡ (*p).voto */
/* confronto: membro per membro, non esiste == tra struct */

/* --- struct annidate e array di struct --- */
struct Rett { struct Punto tl, br; };
struct Rett r = {{0,0},{3,4}};
r.br.x = 5;
Studente classe[30];
classe[0].voto = 18;
```

```c
/* --- union: memoria condivisa --- */
union Valore { int i; double d; char s[8]; };   /* sizeof = max dei membri */

struct Etichetta {                              /* tagged union: idioma C89 */
    enum { T_INT, T_DBL, T_STR } tipo;
    union Valore v;
};
struct Etichetta e;
e.tipo = T_INT; e.v.i = 42;
switch (e.tipo) { case T_INT: printf("%d\n", e.v.i); break; /* ... */ }

/* --- enum: costanti intere leggibili --- */
typedef enum { LUN, MAR, MER, GIO, VEN, SAB, DOM, N_GIORNI } Giorno;
Giorno g = MER;
for (g = LUN; g < N_GIORNI; g++) ...   /* N_GIORNI come sentinella */

/* --- bit-field: solo int/unsigned int/signed int in C89 --- */
struct Stato {
    unsigned int attivo   : 1;
    unsigned int errore   : 1;
    unsigned int livello  : 3;   /* 0..7 */
};
struct Stato s = {1, 0, 5};
if (s.attivo) ...

/* --- typedef: leggibilità e portabilità --- */
typedef unsigned long ulong;
typedef struct Nodo Nodo;
typedef int (*Cmp)(const void *, const void *);
typedef char Riga[128];
```

> [!note] Layout
> - `offsetof(Studente, voto)` (`<stddef.h>`) → offset in byte del membro.
> - **Padding:** `sizeof(struct)` ≥ somma dei membri; l'ordine dei campi cambia la dimensione. Non aspettarti portabilità byte-per-byte scrivendo struct su file binario.
> - `union`: inizializzabile solo il **primo** membro.


---

## 12. Liste concatenate

### 12.1 Lista semplicemente concatenata — libreria completa

```c
#include <stdio.h>
#include <stdlib.h>

typedef struct Nodo {
    int dato;
    struct Nodo *next;
} Nodo;

/* --- creazione --- */
static Nodo *nuovo(int x)
{
    Nodo *p = malloc(sizeof *p);
    if (p == NULL) { perror("malloc"); exit(EXIT_FAILURE); }
    p->dato = x;
    p->next = NULL;
    return p;
}

/* --- inserimento in testa: O(1) --- */
void push_front(Nodo **testa, int x)
{
    Nodo *p = nuovo(x);
    p->next = *testa;
    *testa = p;
}

/* --- inserimento in coda col doppio puntatore: O(n), senza casi speciali --- */
void push_back(Nodo **testa, int x)
{
    Nodo **pp = testa;
    while (*pp != NULL) pp = &(*pp)->next;
    *pp = nuovo(x);
}

/* --- inserimento ordinato --- */
void insert_ord(Nodo **testa, int x)
{
    Nodo **pp = testa;
    while (*pp != NULL && (*pp)->dato < x) pp = &(*pp)->next;
    { Nodo *p = nuovo(x); p->next = *pp; *pp = p; }
}

/* --- ricerca --- */
Nodo *cerca(Nodo *testa, int x)
{
    Nodo *p;
    for (p = testa; p != NULL; p = p->next) if (p->dato == x) return p;
    return NULL;
}

/* --- rimozione della prima occorrenza: 1 = rimossa --- */
int rimuovi(Nodo **testa, int x)
{
    Nodo **pp = testa;
    while (*pp != NULL && (*pp)->dato != x) pp = &(*pp)->next;
    if (*pp == NULL) return 0;
    {
        Nodo *morto = *pp;
        *pp = morto->next;      /* scavalca */
        free(morto);
        return 1;
    }
}

/* --- lunghezza e stampa --- */
size_t lunghezza(const Nodo *p)
{
    size_t n = 0;
    for (; p != NULL; p = p->next) n++;
    return n;
}

void stampa(const Nodo *p)
{
    for (; p != NULL; p = p->next) printf("%d -> ", p->dato);
    printf("NULL\n");
}

/* --- inversione in place: O(n) --- */
void inverti(Nodo **testa)
{
    Nodo *prec = NULL, *cur = *testa, *succ;
    while (cur != NULL) {
        succ = cur->next;
        cur->next = prec;
        prec = cur;
        cur = succ;
    }
    *testa = prec;
}

/* --- distruzione: salva next PRIMA di free --- */
void libera(Nodo **testa)
{
    Nodo *p = *testa;
    while (p != NULL) {
        Nodo *succ = p->next;
        free(p);
        p = succ;
    }
    *testa = NULL;
}

int main(void)
{
    Nodo *lista = NULL;
    push_back(&lista, 3);
    push_back(&lista, 1);
    push_front(&lista, 9);
    insert_ord(&lista, 2);
    stampa(lista);                 /* 9 -> 3 -> 1 -> 2 -> NULL */
    inverti(&lista);
    rimuovi(&lista, 3);
    stampa(lista);
    printf("n = %lu\n", (unsigned long)lunghezza(lista));
    libera(&lista);
    return 0;
}
```

> [!tip] Perché `Nodo **`?
> Per modificare la *testa* del chiamante (o il campo `next` del precedente) serve l'indirizzo del puntatore: elimina tutti i casi speciali "lista vuota / primo elemento".

### 12.2 Lista doppiamente concatenata

```c
typedef struct D { int v; struct D *prev, *next; } D;

/* inserimento di un nodo prima di pos (NULL = in coda) */
void d_insert(D **testa, D *pos, int x)
{
    D *n = malloc(sizeof *n);
    if (n == NULL) exit(EXIT_FAILURE);
    n->v = x;
    n->next = pos;
    n->prev = pos ? pos->prev : NULL;
    if (n->prev) n->prev->next = n; else *testa = n;
    if (pos) pos->prev = n;
}

void d_remove(D **testa, D *n)
{
    if (n->prev) n->prev->next = n->next; else *testa = n->next;
    if (n->next) n->next->prev = n->prev;
    free(n);
}
```

Caso d'uso: cache LRU, code bidirezionali, cancellazione O(1) noto il nodo.

### 12.3 Stack e queue con lista

```c
/* STACK (LIFO): push/pop in testa */
void push(Nodo **s, int x) { push_front(s, x); }

int pop(Nodo **s, int *out)
{
    Nodo *p = *s;
    if (p == NULL) return 0;
    *out = p->dato; *s = p->next; free(p);
    return 1;
}

/* QUEUE (FIFO): head + tail → enqueue/dequeue O(1) */
typedef struct { Nodo *h, *t; } Coda;

void enq(Coda *q, int x)
{
    Nodo *p = nuovo(x);
    if (q->t) q->t->next = p; else q->h = p;
    q->t = p;
}

int deq(Coda *q, int *out)
{
    Nodo *p = q->h;
    if (p == NULL) return 0;
    *out = p->dato;
    q->h = p->next;
    if (q->h == NULL) q->t = NULL;
    free(p);
    return 1;
}
```

| Struttura | Pro                          | Contro                           | Quando                      |
| --------- | ---------------------------- | -------------------------------- | --------------------------- |
| Array     | accesso O(1), cache-friendly | dimensione fissa, insert O(n)    | n noto, accessi indicizzati |
| Lista     | insert/delete O(1), cresce   | accesso O(n), overhead puntatori | n ignoto, molte modifiche   |


---

## 13. Gestione dei file

### 13.1 Apertura, chiusura e modi

```c
FILE *f = fopen("dati.txt", "r");
if (f == NULL) { perror("dati.txt"); return EXIT_FAILURE; }
/* ... */
if (fclose(f) != 0) perror("fclose");
```

| Modo | Effetto | File inesistente |
|---|---|---|
| `"r"` | lettura | errore |
| `"w"` | scrittura, **tronca** | creato |
| `"a"` | append (scritture sempre in fondo) | creato |
| `"r+"` | lettura + scrittura | errore |
| `"w+"` | lettura + scrittura, tronca | creato |
| `"a+"` | lettura + append | creato |
| `+ "b"` | binario (`"rb"`, `"wb+"`…) | indifferente su Unix, **essenziale** su Windows |

Stream già aperti: `stdin`, `stdout`, `stderr`.

### 13.2 Funzioni per categoria

| Categoria | Funzioni |
|---|---|
| testo formattato | `fprintf fscanf sprintf sscanf vfprintf vprintf vsprintf` |
| caratteri | `fgetc getc getchar fputc putc putchar ungetc` |
| righe/stringhe | `fgets fputs puts` (`gets` esiste ma è insicuro) |
| binario | `fread fwrite` |
| posizionamento | `fseek ftell rewind fgetpos fsetpos` |
| stato/errori | `feof ferror clearerr perror` |
| buffering | `fflush setvbuf setbuf` |
| filesystem | `remove rename tmpfile tmpnam` |

### 13.3 Casi d'uso

```c
/* --- leggere un file di testo riga per riga (pattern CORRETTO) --- */
char riga[256];
int n = 0;
while (fgets(riga, sizeof riga, f) != NULL) {   /* MAI while(!feof(f)) */
    riga[strcspn(riga, "\n")] = '\0';
    n++;
    printf("%4d: %s\n", n, riga);
}
if (ferror(f)) perror("lettura");

/* --- scrivere report --- */
fprintf(f, "%-20s %5d %8.2f\n", nome, voti, media);

/* --- leggere record "nome valore" --- */
char nome[32]; int v;
while (fscanf(f, "%31s %d", nome, &v) == 2) { /* usa nome, v */ }
```

```c
/* --- copia di file (binaria, a blocchi: veloce) --- */
int copia(const char *src, const char *dst)
{
    FILE *fi, *fo;
    char buf[4096];
    size_t n;
    int ok = 1;

    fi = fopen(src, "rb");
    if (fi == NULL) { perror(src); return 0; }
    fo = fopen(dst, "wb");
    if (fo == NULL) { perror(dst); fclose(fi); return 0; }

    while ((n = fread(buf, 1, sizeof buf, fi)) > 0)
        if (fwrite(buf, 1, n, fo) != n) { ok = 0; break; }
    if (ferror(fi)) ok = 0;

    fclose(fi);
    if (fclose(fo) != 0) ok = 0;
    return ok;
}
```

```c
/* --- I/O binario di struct (archivio random-access) --- */
typedef struct { int id; char nome[32]; double val; } Rec;

Rec r = {1, "anna", 3.5};
fwrite(&r, sizeof r, 1, fo);                  /* scrive 1 record */

Rec tab[100];
size_t letti = fread(tab, sizeof tab[0], 100, fi);   /* quanti record letti */

/* accesso diretto al record k-esimo */
fseek(fi, (long)k * (long)sizeof(Rec), SEEK_SET);
fread(&r, sizeof r, 1, fi);
/* SEEK_SET (inizio) / SEEK_CUR (corrente) / SEEK_END (fine) */

long pos = ftell(fi);        /* posizione corrente, -1L se errore */
rewind(fi);                  /* torna all'inizio e azzera gli errori */

/* dimensione del file (affidabile solo in binario) */
fseek(fi, 0L, SEEK_END);
long dim = ftell(fi);
rewind(fi);

/* fgetpos/fsetpos: posizioni "opache", portabili anche su file enormi */
fpos_t p;
fgetpos(fi, &p);
/* ... */
fsetpos(fi, &p);
```

```c
/* --- errori: distinguere EOF da errore --- */
if (feof(f))        printf("fine file\n");
else if (ferror(f)) perror("errore I/O");
clearerr(f);

/* --- file temporaneo e rinomina --- */
FILE *t = tmpfile();                 /* cancellato alla chiusura */
/* ... scrivi t ... */
rename("nuovo.dat", "archivio.dat");
remove("vecchio.dat");

/* --- buffering: log a righe --- */
setvbuf(logfile, NULL, _IOLBF, 0);   /* _IOFBF pieno, _IOLBF righe, _IONBF nessuno */
fflush(stdout);                      /* MAI fflush(stdin): UB */
```

> [!warning] Trappole sui file
> `while (!feof(f))` legge l'ultimo record due volte · `fopen` senza test `NULL` · `fclose` dimenticato (dati persi nel buffer) · modo testo su dati binari · `fscanf` che si blocca su input malformato (preferisci `fgets` + `sscanf`) · `fwrite` di struct con padding (non portabile).


---

## 14. Argomenti da linea di comando

### 14.1 Modello

```c
int main(int argc, char *argv[])
```

- `argc` ≥ 1: numero di argomenti **incluso** il nome del programma.
- `argv[0]` = nome del programma (può essere `""` se non disponibile).
- `argv[1..argc-1]` = argomenti, **tutti stringhe**.
- `argv[argc]` == `NULL` (garantito).
- Il terzo parametro `char *envp[]` **non** è C89: usa `getenv()`.
- `getopt()` è POSIX, **non** C89 → parsing manuale.

```text
$ ./prog -n -o out.txt dati1.txt dati2.txt
argc = 6
argv[0]="./prog" [1]="-n" [2]="-o" [3]="out.txt" [4]="dati1.txt" [5]="dati2.txt"
```

### 14.2 Parsing manuale — schema completo

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <errno.h>

static void usage(const char *prog)
{
    fprintf(stderr,
        "Uso: %s [-v] [-n N] [-o FILE] [--] [FILE ...]\n"
        "  -v        verbose\n"
        "  -n N      numero di righe (default 10)\n"
        "  -o FILE   output (default stdout)\n"
        "  --        fine delle opzioni\n", prog);
    exit(EXIT_FAILURE);
}

int main(int argc, char *argv[])
{
    int verbose = 0, i;
    long n = 10;
    const char *out = NULL;

    for (i = 1; i < argc; i++) {
        const char *a = argv[i];

        if (strcmp(a, "--") == 0) { i++; break; }        /* fine opzioni */
        if (a[0] != '-' || a[1] == '\0') break;          /* primo file (o "-") */

        if (strcmp(a, "-v") == 0) {
            verbose = 1;
        } else if (strcmp(a, "-n") == 0) {
            char *fine;
            if (++i >= argc) usage(argv[0]);             /* richiede valore */
            errno = 0;
            n = strtol(argv[i], &fine, 10);
            if (*fine != '\0' || errno != 0 || n <= 0) usage(argv[0]);
        } else if (strcmp(a, "-o") == 0) {
            if (++i >= argc) usage(argv[0]);
            out = argv[i];
        } else if (strcmp(a, "-h") == 0 || strcmp(a, "--help") == 0) {
            usage(argv[0]);
        } else {
            fprintf(stderr, "Opzione sconosciuta: %s\n", a);
            usage(argv[0]);
        }
    }

    /* da i in poi: argomenti posizionali (file); "-" = stdin per convenzione */
    if (i >= argc) {
        if (verbose) fprintf(stderr, "leggo da stdin\n");
        /* elabora(stdin); */
    } else {
        for (; i < argc; i++) {
            FILE *f;
            if (strcmp(argv[i], "-") == 0) f = stdin;
            else {
                f = fopen(argv[i], "r");
                if (f == NULL) { perror(argv[i]); return EXIT_FAILURE; }
            }
            if (verbose) fprintf(stderr, "leggo %s\n", argv[i]);
            /* elabora(f); */
            if (f != stdin) fclose(f);
        }
    }

    if (out != NULL) {
        FILE *fo = fopen(out, "w");
        if (fo == NULL) { perror(out); return EXIT_FAILURE; }
        fprintf(fo, "n=%ld\n", n);
        fclose(fo);
    } else {
        printf("n=%ld\n", n);
    }
    return EXIT_SUCCESS;
}
```

### 14.3 Varianti utili

```c
/* opzioni raggruppate: -abc */
for (p = a + 1; *p != '\0'; p++) {
    switch (*p) { case 'a': /*...*/ break; case 'b': /*...*/ break;
                  default: usage(argv[0]); }
}

/* opzione con valore attaccato: -n5 oppure -oFILE */
if (strncmp(a, "-n", 2) == 0) n = strtol(a + 2, &fine, 10);

/* variabile d'ambiente come default */
const char *home = getenv("HOME");
if (home == NULL) home = ".";
```

> [!tip] Convenzioni CLI
> Errori e usage su `stderr`, dati su `stdout` (per permettere le pipe) · exit code 0 / non-zero · `--` per nomi di file che iniziano con `-` · `-` come sinonimo di stdin.


---

## 15. Libreria standard

### 15.0 I 15 header del C89

| Header | Contenuto |
|---|---|
| `<stdio.h>` | I/O ([[#13. Gestione dei file|§13]]), `printf/scanf` |
| `<stdlib.h>` | memoria, conversioni, ordinamento, ambiente, exit |
| `<string.h>` | stringhe e memoria ([[#7. Stringhe|§7]]) |
| `<math.h>` | `sin cos tan asin acos atan atan2 sinh cosh tanh exp log log10 pow sqrt ceil floor fabs fmod frexp ldexp modf`, `HUGE_VAL` |
| `<ctype.h>` | `isalpha isdigit isalnum isspace isupper islower isprint ispunct iscntrl isgraph isxdigit toupper tolower` |
| `<time.h>` | `time difftime mktime strftime asctime ctime gmtime localtime clock`, `struct tm`, `CLOCKS_PER_SEC` |
| `<limits.h>` | `CHAR_BIT SCHAR_MIN/MAX UCHAR_MAX SHRT_* INT_* LONG_* UINT_MAX ULONG_MAX MB_LEN_MAX` |
| `<float.h>` | `FLT_RADIX FLT_MANT_DIG FLT_DIG FLT_EPSILON FLT_MIN FLT_MAX DBL_* LDBL_*` |
| `<stddef.h>` | `size_t ptrdiff_t wchar_t NULL offsetof` |
| `<stdarg.h>` | `va_list va_start va_arg va_end` |
| `<assert.h>` | `assert(expr)`, disattivabile con `NDEBUG` |
| `<errno.h>` | `errno EDOM ERANGE` |
| `<setjmp.h>` | `jmp_buf setjmp longjmp` |
| `<signal.h>` | `signal raise sig_atomic_t SIGINT SIGSEGV SIGTERM SIGABRT SIGFPE SIGILL SIG_DFL SIG_IGN SIG_ERR` |
| `<locale.h>` | `setlocale localeconv LC_ALL LC_CTYPE LC_NUMERIC LC_TIME LC_COLLATE LC_MONETARY` |

> [!danger] Non esistono in C89
> `<stdbool.h>` `<stdint.h>` `<inttypes.h>` `<complex.h>` `<tgmath.h>` `<fenv.h>` `<wchar.h>` `<wctype.h>` `<iso646.h>`

### 15.1 printf e scanf — formato

`%[flag][larghezza][.precisione][lunghezza]specificatore`

| Spec | Tipo atteso |
|---|---|
| `%d` `%i` | `int` |
| `%u` `%o` `%x` `%X` | `unsigned` (dec / ott / hex) |
| `%c` | `int` / char |
| `%s` | `char *` |
| `%f` | `double` (decimale) |
| `%e` `%E` | `double` (esponenziale) |
| `%g` `%G` | `double` (compatto) |
| `%p` | `void *` |
| `%n` | `int *` (caratteri scritti) |
| `%%` | letterale `%` |

Flag: `-` sinistra · `+` segno · ` ` spazio · `#` forma alternativa · `0` padding zero.
Lunghezza: `h` short · `l` long (in `scanf`: `%lf` double, `%ld` long) · `L` long double.

```c
printf("%-10s|%5d|%08.3f|%#x|%.4g\n", "anna", 42, 3.14159, 255, 0.0001234);
/* anna      |   42|0003.142|0xff|0.0001234 */

printf("%lu byte\n", (unsigned long)sizeof(Rec));   /* size_t: cast + %lu (no %zu!) */

int n; double d; char s[32];
if (scanf("%d %lf %31s", &n, &d, s) != 3) { /* input non valido */ }
/* scanf: %*d scarta, %[a-z] insieme, %[^,] fino a virgola, %5s larghezza max */
```

> [!warning] Formati
> `%lf` in `printf` non è C89 (è C99); `%zu`, `%lld`, `%hhd` non esistono. Per `size_t` usa il cast a `unsigned long` + `%lu`.

### 15.2 stdlib.h in azione

```c
#include <stdlib.h>
#include <errno.h>
#include <time.h>

/* conversioni */
int    i = atoi("42");                 /* nessun controllo errori */
long   l = atol("123456");
double d = atof("3.14");
char *fine;
long   n = strtol("0x1F", &fine, 16);  /* base 0 = auto (0x/0) */
unsigned long u = strtoul("4294967295", &fine, 10);
double x = strtod("1.5e3", &fine);
if (errno == ERANGE) perror("overflow");
```

```c
/* ordinamento e ricerca generici */
int cmp_int(const void *a, const void *b)
{
    int x = *(const int *)a, y = *(const int *)b;
    return (x > y) - (x < y);            /* evita overflow di x-y */
}

int v[5] = {5,1,4,2,3}, chiave = 4;
int *trov;
qsort(v, 5, sizeof v[0], cmp_int);
trov = bsearch(&chiave, v, 5, sizeof v[0], cmp_int);   /* array GIÀ ordinato */

/* casuali */
srand((unsigned)time(NULL));
r = rand() % 100;                        /* 0..99; RAND_MAX in stdlib.h */

/* interi */
q = abs(-5);  lq = labs(-5L);
div_t  a = div(7, 2);    /* a.quot=3, a.rem=1 */
ldiv_t b = ldiv(7L, 2L);

/* terminazione e ambiente */
void cleanup(void) { /* chiusure, salvataggi */ }
atexit(cleanup);
if (errore_grave) abort();               /* uscita anomala, no atexit */
const char *path = getenv("PATH");
int rc = system("ls");                   /* implementation-defined */
exit(EXIT_FAILURE);
```

### 15.3 math.h, ctype.h, time.h

```c
#include <math.h>
double ip  = sqrt(a*a + b*b);
double ang = atan2(y, x);                /* radianti, quadrante corretto */
double p   = pow(2.0, 10.0);
int su = (int)ceil(3.2), giu = (int)floor(3.8);
/* round(), trunc(), fmin(), hypot(), isnan() sono C99:
   usa floor(x+0.5), (x != x) per il test NaN, ecc. */
```

```c
#include <ctype.h>
int cifre = 0;
for (p = s; *p; p++)
    if (isdigit((unsigned char)*p)) cifre++;   /* cast: char negativi = UB */
if (isalpha(c)) putchar(toupper(c));
```

```c
#include <time.h>
time_t t = time(NULL);
struct tm *lt = localtime(&t);
char buf[64];
strftime(buf, sizeof buf, "%d/%m/%Y %H:%M:%S", lt);
printf("%s (%d-%02d-%02d)\n", buf, lt->tm_year + 1900, lt->tm_mon + 1, lt->tm_mday);
printf("oggi: %s", ctime(&t));

struct tm data = {0};
data.tm_year = 126; data.tm_mon = 10; data.tm_mday = 21; data.tm_hour = 12;
time_t quando = mktime(&data);           /* normalizza e converte */
printf("differenza: %.0f s\n", difftime(quando, t));

clock_t ini = clock();
/* ... lavoro ... */
printf("CPU: %.3f s\n", (double)(clock() - ini) / CLOCKS_PER_SEC);
```

### 15.4 Debug, errori, segnali, salti non locali, locale

```c
#include <assert.h>
/* #define NDEBUG  prima dell'include per disattivare */
assert(n > 0);                       /* se falso: messaggio + abort */
assert(p != NULL && "p nullo");
```

```c
#include <errno.h>
errno = 0;
y = sqrt(-1.0);
if (errno == EDOM) fprintf(stderr, "dominio: %s\n", strerror(errno));
perror("fopen");                     /* stampa "fopen: <motivo>" */
```

```c
#include <signal.h>
static volatile sig_atomic_t stop = 0;
static void handler(int sig) { stop = 1; }        /* poche cose lecite qui */

signal(SIGINT, handler);
while (!stop) { /* lavoro interrompibile con Ctrl-C */ }
raise(SIGTERM);
```

```c
#include <setjmp.h>
jmp_buf env;
void profondo(void) { longjmp(env, 1); }          /* "eccezione" in C */

int main(void)
{
    if (setjmp(env) == 0) { profondo(); }         /* ritorna 0 la prima volta */
    else { printf("recuperato\n"); }              /* ritorna il valore di longjmp */
    return 0;
}
```

```c
#include <locale.h>
setlocale(LC_ALL, "");               /* adotta la locale dell'ambiente */
struct lconv *lc = localeconv();
printf("separatore decimale: %s\n", lc->decimal_point);
```


---

## 16. Programma integrato

> [!example] Cosa combina
> Liste concatenate + file + argomenti CLI + memoria dinamica + parsing con `fgets`/`sscanf`.

```c
/* archivio.c — C89 puro
   Uso: ./archivio [-n] [-o FILE] [--] [FILE ...]
   Input: righe "nome voto"; '#' = commento. Senza FILE legge stdin.
   -n ordina per nome, altrimenti per voto decrescente.               */

#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define NOME_MAX 32
#define RIGA_MAX 128

typedef struct Nodo {
    char nome[NOME_MAX];
    int  voto;
    struct Nodo *next;
} Nodo;

static Nodo *lista = NULL;
static int   per_nome = 0;

static void usage(const char *prog)
{
    fprintf(stderr, "Uso: %s [-n] [-o FILE] [--] [FILE ...]\n", prog);
    exit(EXIT_FAILURE);
}

static Nodo *crea(const char *nome, int voto)
{
    Nodo *p = malloc(sizeof *p);
    if (p == NULL) { perror("malloc"); exit(EXIT_FAILURE); }
    strncpy(p->nome, nome, NOME_MAX - 1);
    p->nome[NOME_MAX - 1] = '\0';
    p->voto = voto;
    p->next = NULL;
    return p;
}

static int confronta(const Nodo *a, const Nodo *b)   /* <0: a precede b */
{
    if (per_nome) return strcmp(a->nome, b->nome);
    return b->voto - a->voto;
}

static void inserisci(Nodo *n)                       /* insertion sort O(n²) */
{
    Nodo **pp = &lista;
    while (*pp != NULL && confronta(*pp, n) <= 0) pp = &(*pp)->next;
    n->next = *pp;
    *pp = n;
}

static int leggi(FILE *f, const char *quale)
{
    char riga[RIGA_MAX], nome[NOME_MAX];
    int voto, n = 0, ln = 0;

    while (fgets(riga, sizeof riga, f) != NULL) {
        ln++;
        if (riga[0] == '#' || riga[0] == '\n') continue;
        if (sscanf(riga, "%31s %d", nome, &voto) == 2) {
            inserisci(crea(nome, voto));
            n++;
        } else {
            fprintf(stderr, "%s:%d: riga ignorata\n", quale, ln);
        }
    }
    if (ferror(f)) perror(quale);
    return n;
}

static void libera(void)
{
    Nodo *p = lista;
    while (p != NULL) { Nodo *s = p->next; free(p); p = s; }
    lista = NULL;
}

int main(int argc, char *argv[])
{
    const char *out = NULL;
    FILE *fo = stdout;
    int i, tot = 0;
    Nodo *p;

    for (i = 1; i < argc; i++) {                     /* opzioni */
        const char *a = argv[i];
        if (strcmp(a, "--") == 0) { i++; break; }
        if (a[0] != '-' || a[1] == '\0') break;
        if (strcmp(a, "-n") == 0)      per_nome = 1;
        else if (strcmp(a, "-o") == 0) { if (++i >= argc) usage(argv[0]); out = argv[i]; }
        else usage(argv[0]);
    }

    if (i >= argc) {                                 /* input */
        tot += leggi(stdin, "<stdin>");
    } else {
        for (; i < argc; i++) {
            FILE *f = fopen(argv[i], "r");
            if (f == NULL) { perror(argv[i]); libera(); return EXIT_FAILURE; }
            tot += leggi(f, argv[i]);
            fclose(f);
        }
    }

    if (out != NULL) {                               /* output */
        fo = fopen(out, "w");
        if (fo == NULL) { perror(out); libera(); return EXIT_FAILURE; }
    }
    for (p = lista; p != NULL; p = p->next)
        fprintf(fo, "%-20s %3d\n", p->nome, p->voto);
    if (fo != stdout && fclose(fo) != 0) { perror(out); libera(); return EXIT_FAILURE; }

    fprintf(stderr, "%d record\n", tot);
    libera();
    return EXIT_SUCCESS;
}
```

```bash
$ gcc -std=c89 -pedantic -Wall archivio.c -o archivio
$ printf 'anna 28\nbruno 30\ncarla 25\n' | ./archivio -o out.txt
3 record
$ ./archivio -n out.txt
anna                  28
bruno                 30
carla                 25
```


---

## 17. Limiti del C89 ed errori tipici

### 17.1 Cosa NON esiste in C89

| Vietato | Alternativa C89 |
|---|---|
| `// commento` | `/* commento */` |
| dichiarazioni dopo istruzioni, `for (int i…)` | inizio blocco / blocco annidato |
| `long long`, `%lld` | `long`, `%ld` |
| `bool/true/false`, `<stdbool.h>` | `int` + `enum { FALSE, TRUE }` |
| VLA `int a[n]` | `malloc` |
| `inline`, `restrict`, `_Generic`, `_Static_assert` | macro / niente |
| `{.x=1}`, `[2]=5`, `(int[]){1,2}` | inizializzatori posizionali |
| `<stdint.h>`, `int32_t` | `limits.h` + `typedef` manuali |
| `snprintf`, `round`, `trunc`, `hypot`, `isnan` | `sprintf` + buffer capiente, `floor(x+0.5)`, `x != x` |
| `strdup`, `getopt`, `strcasecmp` (POSIX) | implementazione manuale ([[#7. Stringhe|§7]], [[#14. Argomenti da linea di comando|§14]]) |
| `__func__`, virgola finale negli `enum` | stringa letterale / rimuovi virgola |
| `return` implicito 0 in `main` | `return 0;` |

### 17.2 Top 20 errori

1. `if (x = 5)` invece di `==`
2. `;` spurio dopo `if (...)` / `for (...)` / `while (...)`
3. `break` dimenticato nello `switch`
4. Divisione intera involontaria: `1/2 == 0`
5. Confronto di stringhe con `==` o di `double` con `==`
6. `scanf` senza `&` (tranne array/stringhe) o senza limite di larghezza
7. `printf` con formato non corrispondente al tipo
8. `strcpy`/`sprintf`/`gets` senza controllo della dimensione
9. `strncpy` senza terminatore `'\0'`
10. `while (!feof(f))` invece del test sul valore di ritorno
11. `fopen` senza test `NULL`; `fclose` dimenticato
12. `malloc` senza test; `sizeof(p)` invece di `sizeof *p`
13. `realloc` fallito assegnato allo stesso puntatore (leak)
14. use-after-free / doppio free / dangling pointer
15. `return` di un array locale
16. Indici fuori range (`a[n]`, `for (i=0; i<=n; i++)`)
17. `sizeof` su un parametro-array credendo sia la dimensione reale
18. Macro senza parentesi; effetti collaterali negli argomenti di macro
19. Confronto signed/unsigned (`if (-1 < 1u)` è falso)
20. UB da sequence point: `i = i++`, `f(i++, i++)`

### 17.3 Checklist di revisione

- [ ] Compila con `-std=c89 -pedantic -Wall -Wextra` **senza warning**
- [ ] Ogni `malloc`/`realloc` ha il test `NULL` e un `free` corrispondente
- [ ] Ogni `fopen` ha il test `NULL` e la `fclose`
- [ ] Ogni buffer ha dimensione nota e limiti rispettati (`+1` per `'\0'`)
- [ ] Ogni funzione ha il prototipo visibile prima dell'uso
- [ ] `main` ritorna un codice esplicito; errori su `stderr`
- [ ] Nessun commento `//`, nessuna dichiarazione dopo istruzioni
- [ ] `valgrind ./prog` pulito (nessun leak, nessun accesso invalido)