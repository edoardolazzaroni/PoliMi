
L’informatica è una scienza, ovvero una conoscenza  sistematica di tecniche e metodi per rappresentare ed elaborare l’informazione. È inoltre costituita da una collezione strutturata di 
dati (osservazioni, fatti, entità fisiche o concettuali) che rappresentano una parte del mondo reale.
	CALCOLATORE = strumento elettronico che elabora informazione, che esegue un algoritmo (o un insieme di algoritmi) ed utilizza elementi di memoria per immagazzinare le informazioni che sta elaborando![[Pasted image 20251029170852.png|467x268]]
		
# Algoritmi

- ALGORITMO = sequenza finita di passi non ambigui e comprensibili da un esecutore per permettere di risolvere un problema;
	- Flusso di CONTROLLO = descrizione a priori di tutte le possibili sequenze dei passi algoritmici; il flusso di controllo di un diagramma di flusso viene costruito mediante specifiche regole:
		- Un solo blocco di inizio
		- Almeno un blocco di terminazione (preferibilmente uno)
		- Non si può lasciare sconnessa alcuna freccia in ingresso o in uscita di un 
		- qualsiasi altro blocco
	 Il flusso di controllo di un algoritmo viene costruito in base a tre strutture di controllo dette: 
		- SEQUENZA
		 ![[Pasted image 20251029172250.png|262x346]]
		- SELEZIONE
		![[Pasted image 20251029172346.png|306x174]]
		- ITERAZIONE
			- Ciclo a condizione FINALE (il corpo del ciclo è eseguito almeno una volta):
			![[Pasted image 20251029172743.png|322x256]]
			- Ciclo a condizione INIZIALE (il corpo del ciclo è eseguito zero o più volte):
			![[Pasted image 20251029172813.png|328x177]]
		Teorema di Jacopini e Böhm: formulato nel 1966 dagli informatici italiani Corrado Böhm e Giuseppe Jacopini, afferma che qualsiasi algoritmo può essere espresso utilizzando unicamente le tre strutture di controllo fondamentali (sequenza, selezione ed iterazione);
	- Flusso di ESECUZIONE = sequenza di operazioni effettivamente seguita in esecuzione;
	- Elementi grafici:
	![[Pasted image 20251029171350.png|341x303]]

- VARIABILE = contenitore di valori, a cui è sempre associato un valore alla volta, non può essere vuota (al massimo non è inizializzata e quindi contiene un valore “a caso”), è collocata in una riga della memoria, è identificata tramite un nome simbolico. Le operazioni descritte nell’algoritmo possono essere eseguite di volta in volta sui diversi valori assegnati alle variabili (formulazione generale dell’algoritmo); possiamo eseguire due operazioni su una variabile:
	- Lettura: recuperiamo il valore contenuto
	- Scrittura: salviamo un nuovo valore

# Algebra di Boole

L’algebra di Boole (inventata da G. Boole, britannico, seconda metà ’800), o algebra della logica, è un’algebra astratta che opera su due soli valori di verità, falso e vero, mediante operatori logici.

- In un calcolatore VERO = 1, FALSO = 0.
- Una variabile logica può contenere il valore 0 o 1 e memorizza il risultato di una condizione.

È possibile esprimere condizioni più complesse mediante gli operatori logici:

- Operatori logici BINARI (con 2 operandi logici):
	- OR (SOMMA logica)
	- AND (PRODOTTO logico)

• Operatore logico UNARIO (con 1 operando):
	- Operatore NOT (NEGAZIONE o inversione)

![[image.png|547x194]]

# Rappresentazione binaria

- Usata dal calcolatore per tutte le informazioni; alfabeto: {0, 1}
	- BIT (“BInary digIT”): unità elementare di informazione
	- Facile da implementare: dispositivi che assumono due stati (acceso/spento), ovvero due valori di tensione: $Vdd$  e $Vgnd$
- Con *n* bit codifichiamo $2^n$ numeri nell'intervallo $[0; 2^n - 1]$
- Per convertire un numero naturale in binario si usa il metodo dei resti, dividendo il numero considerato per 2 fino ad arrivare allo 0/1: 

| dividendo | divisore | resto |
| :-------: | :------: | :---: |
|    19     |    2     |   1   |
|     9     |    2     |   1   |
|     4     |    2     |   0   |
|     2     |    2     |   0   |
|     1     |    2     |   1   |
|     0     |          |       |

- Formula per rappresentare il numero *N* in bit $=log2(N+1)$

## OPERAZIONI con numeri binari naturali

- ADDIZIONE:
		![[image-1.png|365x159]]

	- Nelle operazioni binarie si può verificare OVERFLOW: il risultato di un’operazione non può essere rappresentato sul numero di bit a disposizione, generando così un risultato errato

- SOTTRAZIONE:
		![[image-2.png|365x152]]

	- Il secondo operando deve essere minore del primo, e al posto dei riporti come nella somma si utilizzano i prestiti

## Numeri binari interi RELATIVI in MODULO E SEGNO:

Nel computer il segno di un numero deve essere rappresentato in qualche modo con cifre binarie, perciò si ricorre ai numeri relativi:
	Il primo bit a sinistra rappresenta il segno del numero (bit di segno), i bit rimanenti rappresentano il valore; si usa per convenzione 0 per il segno POSITIVO, 1 per il segno NEGATIVO.
		In questo modo con $n$ bit $(n\geq2)$ codifichiamo $2^n$ numeri nell'intervallo $(-2^(n-1), 2^(n-1))$ 
	Osservazioni:
		- Il bit di segno è applicato al numero rappresentato, ma non fa propriamente parte del numero in quanto tale, ovvero non ha significato numerico;
		- Distaccando il bit di segno, i bit rimanenti rappresentano il valore assoluto del numero;
	Formula per rappresentare in modulo e segno il numero *N* in bit $=log2(N+1)+1$
	Operazioni:
		- Somma di due numeri con STESSO SEGNO: si sommano i valori assoluti dei due numeri (sono due numeri naturali) e si aggiunge al risultato il segno dei due operandi;
		- Somma di due numeri con segno discorde: si effettua la sottrazione tra il valore assoluto più grande e quello più piccolo (sono due numeri naturali) e si aggiunge al risultato il segno dell’operando con valore assoluto maggiore;
		- Sottrazione: Si inverte il segno del secondo operando e si esegue la somma secondo le regole mostrate sopra

### COMPLEMENTO A DUE:

Il complemento a due è un sistema binario, ma il primo bit (quello a sinistra, il più significativo) ha peso negativo, mentre tutti gli altri bit hanno peso positivo; vi è ancora il bit di segno (il più significativo).
	Esempi:
			![[image-3.png|286x169]]

- Conversione da decimale a C2:
		- Se $Ddec\geq0$:
			1) Convertire $Ddec$ in binario naturale
			2) Aggiungere il bit 0 in testa alla sequenza di bit ottenuta
			*Esempio: $154 (dec) = 10011010 (bin) = 010011010 (C2)$
		- Se $Ddec<0$:
			1) Trascurare il segno e converti $Ddec$ in binario naturale
			2) Aggiungere il bit 0 in testa alla sequenza di bit ottenuta
			3) Calcolare l’opposto del numero così ottenuto, secondo la procedura di inversione in C2
			*Esempio: $-154 (dec) = 154 (dec) = 10011010 (bin) = 010011010 (bin) = 101100101 + 1 Þ 101100110C2$*


1. Trascurare il segno e converti Ddec in binario naturale

2. Aggiungere il bit 0 in testa alla sequenza di bit ottenuta

3. Calcolare l’opposto del numero così ottenuto, secondo la procedura 

di inversione in C2

§ Esempio: -154dec Þ 154dec Þ 10011010bin Þ

 Þ 010011010bin Þ 101100101 + 1 Þ 101100110C2
- 