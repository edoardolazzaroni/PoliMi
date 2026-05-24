

# Parte I: Informatica Teorica


## **Linguaggi Formali**


### **1.1 Alfabeti e Stringhe**

Di seguito sono riportate alcune definizioni importanti riguardanti i linguaggi formali:

- Un ==alfabeto== (o vocabolario) $V$ è un insieme finito di oggetti elementari detti simboli (o caratteri);
- Una ==stringa== $x$ appartenente ad un alfabeto $V$ è una sequenza finita e ordinata di caratteri appartenenti a tale alfabeto. Data una stringa $x$, la notazione $|x|$ indica la lunghezza di tale stringa, ovvero il numero di caratteri di cui è composta (la cardinalità del suo dominio $V$). Per convenzione la stringa vuota, che non contiene nessun carattere, è indicata con la lettera $ε$. La stringa vuota $ε$ ha lunghezza zero.

Per poter confrontare due stringhe e necessario verificare che:
- $|x| = |y|$
- $x_i = y_i‎  ,‎ ∀i= 0,1,2,...,|x|$

La **concatenazione** (o prodotto) $x.y$ di due stringhe x e y è una stringa composta da tutti i caratteri di x seguiti da tutti i caratteri di y. Inoltre, la concatenazione $x.ε$ produce come risultato la stringa x.
Data una stringa s, una stringa x è **sottostringa** (o fattore) di s se esistono due stringhe y e z, tali che $s = yxz$. Inoltre:
- se $y = ε$, x è detta prefisso
- se $z = ε$, x è detta suffisso
- se $z = y = ε$, $x= s$

Data una stringa x, l’espressione $x^i$ indica la concatenazione della stringa x con s e stessa per $i−1$ volte, ovvero $x^0 = ε$ e $x^{i+1} = x.x^i$  .


### **1.2 Operatori di Kleene**

Per poter proseguire con il trattato, è prima necessario introdurre alcuni concetti matematici fondamentali. Si danno quindi le seguenti definizioni:

- Un ==semigruppo==  è una coppia $<S,◦>$, dove:
	- S è un insieme chiuso rispetto a $◦$ per cui, se si prendono due qualsiasi elementi A e B di tale insieme, l’operazione $A◦B$ produce come risultato un elemento appartenente ad S;
	- $◦$ è un’operazione associativa su S.

Nel contesto dei linguaggi, l’operatore $◦$ rappresenta la concatenazione di stringhe.

- Un ==monoide== è un semigruppo in cui è definito un elemento unitario $u∈S$, tale che $∀x,∃u (x◦u= x)$.

Nel contesto dei linguaggi, l’elemento unitario $u$ rappresenta la stringa vuota $ε$: infatti, la concatenazione di una generica stringa $x$ con la stringa vuota $ε$ produce come risultato nuovamente la stringa originaria $x$.

- Un ==gruppo== è un monoide in cui è definito un elemento inverso $x−1$ unico per ogni elemento x dell’insieme S, tale che $∀x(x◦x−1 = u)$.

Si possono quindi definire gli **Operatori di Kleene**:

- Sia $< S,◦ >$ un semigruppo. Per ogni $X ⊆ S, S+$ indica il sottoinsieme di S generato da X, ovvero l’insieme di tutti gli elementi $s∈S$ tale per cui $s= x_1 ◦x_2 ◦...◦x_n$ per qualche $n≥1$, con $x_i ∈X$ (stringhe non vuote).

Nel contesto dei linguaggi, l’operatore $+$ di Kleene rappresenta l’insieme infinito di stringhe non vuote, che si possono generare a partire dall’insieme $S$ di simboli, a cui si applica tale operatore.

- Se $<S,◦,u>$ è un monoide, allora $X∗= X^+ ∪{u‎}$ è un monoide (più precisamente un sottomonoide) di S ed è detto monoide libero generato da X; esso è detto **Stella di Kleene**.

Nel contesto dei linguaggi, la stella di Kleene rappresenta l’insieme infinito di stringhe, inclusa la stringa vuota $ε$, che si possono generare a partire dall’insieme $S$ di simboli, a cui si applica tale operatore. Quindi: $X^∗ = X^+ ∪{ε}$.
Ad esempio, dato l’insieme di simboli $S= \left \{a,b,c\right \}$, $S^+ = \left \{a,b,c,aa,ab,ac,ba,bb,bc,ca,cb,cc,aaa...\right \}$ e $S^∗ = \left \{ε,a,b,c,aa,ab,ac,ba,bb,bc,ca,cb,cc,aaa...\right \}$.


### **1.3 Linguaggi**

Data la definizione della stella di Kleene, si può ora dare la definizione di linguaggio:

- Un ==linguaggio== L su un alfabeto V è un sottoinsieme di $V^∗$.

Dato un insieme di simboli, si possono generare infiniti linguaggi.

Poichè i linguaggi sono un insieme di stringhe, valgono tutte le **operazioni insiemistiche** come:
	- Unione ($L_1 ∪L_2$): l’insieme di tutte le stringhe che appartengono o ad $L_1$ o ad $L_2$ o ad entrambi i linguaggi;
	- Intersezione ($L_1 ∩L_2$): l’insieme di tutte le stringhe che appartengono sia ad $L_1$ che ad $L_2$;
	- Differenza ($L_1/L_2$): l’insieme di tutte le stringhe che appartengono ad L1 ma non ad L2;
	- Complementare ($L^C = A^∗/L$): l’insieme di tutte le stringhe che non appartengono al linguaggio $L$;
	- Concatenazione ($L_1.L_2$): l’insieme di tutte le stringhe che si ottengono concatenando ad ogni stringa di $L_1$ ogni stringa di $L_2$; formalmente $L_1.L_2 =\left \{xy: x∈L_1, y∈L_2\right \}$;
	- Potenza $n$-esima ($L^n$): l’insieme di tutte le stringhe che si ottengono concatenando $L$ con se' stesso $n$ volte, utilizzando le regole della concatenazione precedentemente definite;
	- Chiusura di Kleene: $\left ( L^∗= \bigcup_{n=0}^{∞} L^{n}, L^+ = \bigcup_{n=1}^{∞} L^{n}\right )$.

Le operazioni su di un determinato linguaggio crea nuove classi di linguaggi con caratteristiche proprie, talvolta interessanti. Un linguaggio diventa di interesse nel momento in cui le stringhe di cui è composto possono essere utilizzate per veicolare informazioni, problemi, soluzioni o per rappresentare programmi, documenti, elementi multimediali o, nel caso più rilevante, per rappresentare computazioni.




## **Automi Deterministici**


In questo capitolo verrà introdotto il concetto di automa e se ne analizzeranno le varie classi esistenti, differenziandole in base alla loro espressività nella rappresentazione di linguaggi via via sempre più complessi. Si inizierà con lo studio degli automi determinstici per passare gradualmente a quelli non deterministici, analzzandone le differenze e le caratteristiche più importanti. Di seguito sono date le definizioni di automa, accettatore e trasduttore:

- Gli ==automi== sono sistemi dinamici discreti e tempo invarianti. Lo stato di un automa viene modificato a fronte di un simbolo di ingresso. Ogni automa presenta uno stato iniziale, da cui ha inizio la sua esecuzione, e uno o più stati finali in cui la sua esecuzione ha termine.
- Gli ==accettatori== sono automi che indicano se una determinata sequenza di simboli appartiene ad un linguaggio.
- I ==trasduttori== sono automi che mappano una determinata sequenza di simboli appartenenti ad un linguaggio in una sequenza di simboli appartenenti ad un linguaggio differente. Un trasduttore lavora quindi su due nastri infiniti: il primo nastro in ingresso di sola lettura, il secondo nastro in uscita di sola scrittura.

Un automa è rappresentato graficamente come un inisieme di circonferenze denominate (che rappresentano gli stati dell’automa), ognuna delle quali è connessa ad altri stati tramite frecce. Su tali frecce è segnata la condizione da soddisfare per intraprendere quel passaggio di stato e come viene modificato lo stato durante il passaggio. Lo stato iniziale si riconosce per via di una freccia entrante nel nodo, mentre gli stati finali sono rappresentati da circonferenze con bordo doppio.

*Esempio di rappresentazione di un automa a stati finiti:*

![[Screenshot 2026-05-23 alle 16.07.21.png|363]]

*Esempio di rappresentazione di una macchina di Turing:*

![[Screenshot 2026-05-23 alle 21.02.24.png|574]]


### **2.1 Automi a Stati Finiti**

Gli FSA (Finite State Automaton) sono automi che presentano un numero finito di stati. Formalmente:

- Un ==FSA== è una tupla di 5 elementi $<Q,A,δ,q_0,F >$, dove:
	- $Q$ è un insieme finito di stati;
	- $A:=$ {$a_0,a_1,a_2,...,a_n$} è l’alfabeto di ingresso;
	- $δ: Q×A→Q$: è la funzione di transizione (eventualmente parziale);
	- $q_0 ∈Q$ è lo stato iniziale;
	- $F ⊆Q$ è un insieme di stati finali.

Quando l’automa riceve in ingresso un simbolo del proprio alfabeto, cambia lo stato in cui si trova. Il passaggio da uno stato a quello successivo avviene attraverso la funzione di transizione $δ$; tale funzione indica, a partire da un determinato stato, in quale stato si troverà l’automa dopo la ricezione di un simbolo in ingresso.
**Attenzione!** La funzione di transizione δ non sempre è totale: ciò significa che in alcuni automi non tutte le transizioni da uno stato a quello successivo sono definite. Gli automi che presentano una funzione di transizione completa sono detti completi.
Data la funzione di transizione $δ$ è possibile definire una sequenza di mosse $δ^∗$, che opera su una stringa anzichè su un unico simbolo in ingresso. Formalmente:

- La chiusura **riflessiva** e **transitiva** della funzione di trasferimento, indicata con $δ^∗: Q×A^∗→Q$ è definita in maniera induttiva come segue:
		$δ^∗(q,ε)=q$;
		$δ^∗(q,yi) = δ(δ^∗(q,y),i)$
	$∀x: x∈L⇔δ^∗(q_0,x) ∈F$.

In altri termini, se l’automa ricesse in ingresso la stringa vuota $ε$, allora rimarrebbe nello stato $q$ in cui si trova, mentre nel caso in cui ricevesse una sequenza di caratteri $yi$ lo stato che l’automa raggiungerebbe sarebbe quello che raggiungerebbe con ingresso $i$, a partire dallo stato che raggiungerebbe da $q$ con la stringa $y$.
Tramite questa definizione, si può affermare che una generica stringa $x$ appartiene al linguaggio $L$ se e solo se l’automa si trova in uno stato finale a fronte della lettura della stringa in ingresso: in tal caso si dice che l’automa accetta o riconosce la stringa di ingresso. Per questo motivo, gli FSA sono detti essere **accettatori**, in quanto verificano se una determinata stringa appartiene o meno ad un dato linguaggio.

#### **2.1.1 Trasduttore a Stati Finiti**

Gli FST (Finate State Trasducer) sono trasduttori che presentano un numero finito di stati . Formalmente:

- Un ==FST== è una tupla di 7 elementi $<Q,I,δ,q_0,F,O,η>$, dove:
	- $Q$ è un insieme finito di stati;
	- $I$ è l’alfabeto di ingresso;
	- $δ: Q×I →Q$ è la funzione di transizione (eventualmente parziale);
	- $q_0 ∈Q$ è lo stato iniziale;
	- $F ⊆Q$ è un insieme di stati finali;
	- $O$ è l’alfabeto di uscita;
	- $η: Q×I →O^∗$ è la funzione di uscita (eventualmente parziale).

#### **2.1. AUTOMI A STATI FINITI**

Quando l’automa riceve in ingresso un simbolo, modifica il proprio stato e mostra in uscita una sequenza di uno o più simboli. Il passaggio da uno stato a quello successivo avviene attraverso la funzione di transizione $δ$, mentre l’operazione di uscita avviene tramite la funzione di uscita $η$.

**Attenzione!** La funzione di uscita $η$ non sempre è totale: ciò significa che in alcuni automi è possibile che non ci sia nessuna associazione fra un simbolo del linguaggio in ingresso e un simbolo del linguaggio di uscita.

Data la funzione di uscita $η$, è possibile definire una sequenza di uscita $η^∗$, che opera su una stringa anzichè su un unico simbolo in ingresso. Formalmente:

- La chiusura riflessiva e transitiva della funzione di uscita, indicata con $η^∗: Q×I^∗→ O^∗$, è definita in maniera induttiva come segue:
		$η^∗(q,ε) = ε$;
		$η^∗(q,yi) = η^∗(q,y).η(δ^∗(q,y),i)$
	$∀x: τ(x) = η^∗(q_0,x) ⇔ δ^∗(q_0,x) ∈F$ in cui tau rappresenta la funzione di traduzione.

In altri termini, se l’automa ricevesse in ingresso la stringa vuota $ε$, allora rimarrebbe nello stato $q$ in cui si trova e non scriverebbe nessun simbolo sul nastro di uscita, mentre, nel caso in cui ricevesse in ingresso una sequenza di caratteri $yi$, allora l’automa produrebbe in uscita quello che produrrebbe da $q$ leggendo $y$ seguito da ciò che produrrebbe dallo stato che raggiungerebbe da $q$ leggendo $y$, avendo $i$ come ingresso. Quindi la funzione $η^∗$ ha il compito di concatenare il simbolo (o la stringa) che si ottiene a fronte della prima transizione con i simboli (o le stringhe) che si ottengono nei successivi passaggi di stato.
Tramite questa definizione, si può affermare che la traduzione di una stringa in ingresso $x$ è accettata se e solo se l’automa si trova in uno stato finale a fronte della lettura di $x$.


#### **2.1.2 Operazioni sugli Automi a Stati Finiti**

Gli Automi a Stati Finiti sono chiusi rispetto alle sequenti operazioni:

- INTERSEZIONE. Formalmente, dati:
	– $A^1 =<Q^1,I,δ^1,q_0^1 ,F^1>$
	– $A^2 =<Q^2,I,δ^2,q_0^2 ,F^2>$
	allora $< A^1,A^2 >= < Q^1 ×Q^2,I,δ,< q_0^1 ,q_0^2 >,F^1 ×F^2 >$ e si può dimostrare che il linguaggio $L(<A^1,A^2>) = L(A^1) ∩L(A^2)$.

- UNIONE. Formalmente, dati:
	– $A^1 =<Q^1,I,δ^1,q_0^1 ,F^1 >$
	– $A^2 =<Q^2,I,δ^2,q_0^2 ,F^2>$
	allora $< A^1,A^2 >= < Q^1 ×Q^2,I,δ,< q_0^1 ,q_0^2 >,F^1 ×Q^2 ∪Q^1 ×F^2$ con $δ(< q^1,q^2 >,i) =<δ^1(q^1,i),δ^2(q^2,i) >$.

- COMPLEMENTAZIONE. L’idea alla base del ragionamento è che $F^C = Q−F$, quindi per poter complementare un automa a stati finiti è necessario rendere finali gli stati che non lo sono e viceversa. Bisogna però prestare attenzione al caso in cui la funzione di transizione dell’automa sia parziale: in tal caso, è necessario innanzitutto completare l’automa, definendo tutte le transizioni precedentemente non definite, e solo in seguito procedere con lo stesso algoritmo.


#### **2.1.3 Pumping Lemma**

Gli automi appena analizzati sono molto semplici e hanno delle evidenti limitazioni, che li rendono inefficaci nella risoluzione di alcuni problemi. Dallo studio di questi automi si possono ricavare alcuni teoremi dimostrabili, utili per mettere in luce tali limitazioni:

- **Primo Teorema**: dato un automa a stati finiti $A=< Q,I,δ,q_0,F >$, dove $Q$ ha cardinalità $n$, il linguaggio riconosciuto da $A$ non è vuoto se e solo se $A$ accetta una stringa $x$ con $— x —  ¡n$. 

- **Secondo Teorema**: dato un automa a stati finiti $A=< Q,I,δ,q_0,F >$, dove $Q$ ha cardinalità $n$, il linguaggio riconosciuto da $A$ è infinito se e solo se $A$ accetta una stringa $x$ con $n≤ |x| <2n$.

I teoremi sono basati sul fatto che un determinato FSA può presentare cicli nella sua rappresentazione grafica. Nel caso in cui l’automa non presenta alcun ciclo nella sua rappresentazione grafica, il linguaggio è **sicuramente finito**, in quanto la stringa in ingresso può far passare l’automa una sola volta in ciascuno dei suoi stati: di conseguenza, la stringa può essere lunga al più come il numero di stati dell’automa meno uno.

Si enuncia quindi il seguente teorema noto con il nome di Pumping Lemma:

- ==Teorema del Pumping Lemma==: sia $A$ un automa a stati finiti. Se $x∈L$ e $|x| ≤ |Q|$, allora esistono uno stato $q∈Q$ e una stringa $w∈I^+$ tali che:
	- $x= ywz$
	- $δ^∗(q,w) = q$

Perciò vale che $∀n≥0, ywnz∈L$.

Il Pumping Lemma fornisce una condizione necessaria, ma non sufficiente sulla struttura dei linguaggi che vengono riconosciuti da un FSA. In altri termini, il teorema afferma che se una stringa $x$ è lunga almeno quanto il numero degli stati interni di un determinato automa che accetta tale stringa, allora $x$ passa necessariamente per una sequenza di mosse contenti un ciclo. Inoltre, tutte le stringhe che si ottengono da $x$ ripetendo la sua sottostringa che attraversa il ciclo, sono sequenze riconosciute e accettate dall’automa. Allo stesso modo, sono accettate anche tutte le stringhe che si ottengono da $x$ cancellando qualsiasi sua sottostringa che attraversi tale ciclo.

Ora supponiamo di progettare un automa $A$ che riconosce tutte e sole le stringhe del linguaggio $L= \left \{a^nb^n : n < 0\right \}$. Inizialmente si assume che $A$ sia in grado di riconoscere un tale linguaggio. Si considera innanzitutto il caso in cui $x= a^mb^m : m> |Q|$. Sappiamo, grazie al Pumping Lemma, che ci sarà un ciclo interno all’automa e può esistere nei tre casi sottolineati:
	1)$...aaaaaabbbbbb...$ : se così fosse si potrebbe rimovere dalla stringa la sottostringa che passa all’interno del ciclo e l’automa riconoscerebbe comunque come accettabile tale stringa, ma ciò non è vero in quanto il numero di $a$ presenti dopo la rimozione di tale sottostringa sarebbe minore del numero delle $b$ e dunque la stringa non sarebbe riconosciuta dall’automa;
	2)$...aaaaaabbbbbb...$ : si applica lo stesso ragionamento del punto precedente;
	3)$...aaaaaabbbbbb...$ : se così fosse si potrebbe ripercorrere quel determinato ciclo anche due volte, ma così facendo si otterrebbe la stringa $...aaaaaaaabbaabbbbbbbb...$ che, secondo il lemma dovrebbe essere riconoscibile dall’automa, ma così non è.

Si nota quindi che non esiste nessun automa a stati finiti che riesca a interpretare un tale linguaggio, in quanto ha una struttura che richiede di contare e ricordare il numero di simboli letti. Per poter contare un numero $n$ arbitrariamente grande si renderebbe necessaria una memoria infinita, che abbia, quindi, un numero infinito di stati.



### **2.2 Automi a Pila**

I PDA (Push Down Automaton) sono automi che presentano un numero finito di stati e una memoria organizzata su una struttura a pila. Tale memoria ha lo stesso comportamento dell’omonima struttura dati: i nuovi simboli vengono inseriti in cima allo stack ed estratti dalla cima dello stack, secondo la politica *LIFO* (Last In First Out). Per indicare che non ci sono più simboli in memoria, si utilizza il simbolo speciale $Z_0$, detto di fondo pila.

Questi particolari tipi di automi hanno la possibilità di utilizzare il simbolo in cima alla pila per decidere quale transizione effettuare e la possibilità di manipolare la pila, rimuovendone il simbolo alla cima, oppure aggiungendo un nuovo simbolo. Formalmente:

- Un ==PDA== è una tupla di 7 elementi $<Q,I,δ,Γ,q_0,Z_0,F >$, dove:
	- $Q$ è un insieme finito di stati;
	- $I$ è l’alfabeto di ingresso;
	- $Γ$ è l’alfabeto della pila, tale per cui $Γ ∩I= ∅$;
	- $δ: Q×(I∪{ε}) ×Γ →Q×Γ^∗$ è la funzione di transizione (eventualmente parziale);
	- $q_0$ è lo stato iniziale;
	- $Z_0$ è il simbolo di fondo pila, ovvero l’unico simbolo che appare inizialmente nella pila;
	- $F ⊆Q$ è un insieme di stati finali.

Dalla definizione, si può osservare che l’automa è in grado di decidere il passo successivo anche senza la lettura di alcun simbolo dal nastro di ingresso, ma solo a fronte della lettura di un simbolo sulla cima dello stack. Tali mosse prendono il nome di **ε-mosse** o mosse spontanee. Ovviamente, per uno stesso stato, non è possibile definire sia una transizione spontanea che una non spontanea, in quanto l’automa in questione sarebbe non deterministico e non sarebbe possibile definirne il comportamento a priori.
Una mossa spontanea non altera la posizione della testina di lettura sul nastro di ingresso, proprio per il fatto che, in tal caso, l’automa ignora deliberatamente il nastro in questione.
Per gli automi a pila, si può introdurre il concetto di configurazione, ossia una generalizzazione della nozione di stato, definita come segue:

- Una **configurazione** $c$ è una tupla di 3 elementi $<q,x,γ >$, dove:
	- $q∈Q$ è lo stato corrente del dispositivo di controllo;
	- $x∈I^∗$ è la porzione non ancora letta della stringa d’ingresso;
	- $γ ∈Γ^∗$ è la stringa composta da tutti i simboli contenuti all’interno della pila.

Una configurazione può essere quindi vista come una fotografia dello stato dell’automa in un determinato istante di tempo.
Le transizioni tra configurazioni, indicate con il simbolo $⊢,$ dipendono naturalmente dalla funzione di transizione $δ$ e si distinguono in due categorie:

1. Se $δ(q,i,A) =<q′,α>$ è una mossa definita, si ha che $c=<q,x,γ >⊢ c′ =<q′,x′,γ′>$, dove:
	- $γ= Aβ$, la pila contiene il simbolo $A$, utilizzato per eseguire la mossa, seguito dalla stringa $β$ composta da tutti i restanti simboli della pila;
	- $x = iy$, la stringa in ingresso è composta da un simbolo $i$, utilizzato per eseguire la mossa, seguito dalla stringa $y$ composta da tutti i restanti simboli non ancora letti;
	- $γ′ = αβ$, dopo la transizione, la pila contiene la stringa $α$ appena inserita, seguita dalla stringa $β$ composta da tutti i restanti simboli della pila;
	- $x′ = y$, dopo la transizione, la stringa in ingresso è composta da tutti i simboli non ancora letti; in altre parole, la testina di lettura si sposta a destra di una posizione.

2. Se $δ(q,ε,A) =<q′,α>$ è una mossa definita, si ha che $c=<q,x,γ >⊢ c′ =<q′,x′,γ′>$, dove:
	- $γ= Aβ$, la pila contiene il simbolo $A$, utilizzato per eseguire la mossa, seguito dalla stringa $β$ composta da tutti i restanti simboli della pila;
	- $γ′ = αβ$, dopo la transizione, la pila contiene la stringa $α$ appena inserita, seguita dalla stringa $β$ composta da tutti i restanti simboli della pila;
	- $x′ = x$, dopo la transizione, la stringa in ingresso è la medesima; in altre parole, la testina di lettura non si sposta.

Se $δ(q,ε,A) \ne ⊥$, ovvero se la funzione di transizione è definita, allora $∀i ∈ I,δ(q,i,A) = ⊥$: se questa proprietà non fosse soddisfatta, entrambe le transizioni sarebbero consentinte e, come detto precedentemente, l’automa non avrebbe un comportamento deterministico.

Data la funzione di transizione tra configurazioni $⊢$, si può definire la chiusura transitiva e riflessiva $⊢^∗$ che opera su un insieme di configurazioni anzichè su un’unica configurazione. Un automa a pila accetta una determinata stringa $x$ se c’è un cammino coerente che va dallo stato iniziale ad uno stato finale al termine della lettura della stringa d’ingresso. Formalmente:

$∀x∈I^∗,x∈L ⇐⇒ c_0 =<q_0,x,Z_0 >⊢^∗ c_F =<q∈F,ε,γ >$

Sappiamo quindi che il linguaggio $a^nb^n$ non può essere riconosciuto da alcun FSA per il Pumping
Lemma. Inoltre, ogni linguaggio riconosciuto da un FSA è riconoscibile anche da un PDA. Si può affermare, quindi, che gli automi a pila sono più espressivi e di **maggiore potenza** rispetto agli automi a stati finiti, i quali possono essere visti come un sottoinsieme dei PDA.
A differenza degli FSA, i PDA potrebbero anche non terminare la propria esecuzione dopo un numero finito di mosse, in quanto possono presentare cicli di ε-mosse. Tali cicli non aggiungono potere espressivo ai PDA: questo significa che gli automi a pila ciclici riconoscono lo stesso insieme di linguaggi degli automi aciclici. Per questo motivo, si preferisce eliminare tale categoria di automi, utilizzando tranisizioni tra configurazioni del tipo $< q,x,α >⊢_d^∗< q′,x,β >$, in cui il simbolo $⊢_d^∗$ indica che per $< q,x,α >⊢^∗<q′,x,β >$ con $β= Zβ′, δ(q′,ε,Z) = ⊥$, ovvero transizioni che hanno necessariamente bisogno di un simbolo in ingresso per proseguire la propria esecuzione. Formalmente:

- Un PDA si definisce **aciclico** se e solo se: $∀x∈I^∗∃q,γ :<q_0,x,Z_0 >⊢_d^∗<q,ε,γ >$.

Un tale automa legge sempre per intero la stringa in ingresso prima di terminare la propria esecuzione ed accettare tale stringa, non potendo finire in un ciclo di ε-mosse. Un automa a pila cicliclo può sempre essere trasformato in un automa a pila aciclico equivalente.


#### **2.2.1 Trasduttori a Pila**

I PDT (Push Down Trasducer) sono trasduttori che presentano un numero finiti di stati e una memoria organizzata su una struttura a pila. Formalmente:

- Un ==PDT== è una tupla di 9 elementi $<Q,I,δ,Γ,q_0,Z_0,F,O,η>$, dove:
	- $Q$ è un insieme finito di stati;
	- $I$ è l’alfabeto di ingresso;
	- $Γ$ è l’alfabeto della pila, tale per cui $Γ ∩I= ∅$;
	- $δ: Q×(I∪{ε}) ×Γ →Q×Γ^∗$ è la funzione di transizione (eventualmente parziale);
	- $q_0$ è lo stato iniziale;
	- $Z_0$ è il simbolo di fondo pila, ovvero l’unico simbolo che appare inizialmente nella pila;
	- $F ⊆Q$ è un insieme di stati finali.
	- $O$ è l’alfabeto di uscita;
	- $η: Q×(I∪{ε}) ×Γ →O^∗$ è la funzione di uscita (eventualmente parziale).

- Una configurazione $c$ di un PDT è una tupla di 4 elementi $<q,x,γ,z>$, dove:
	- $q∈Q$ è lo stato corrente del dispositivo di controllo;
	- $x∈I^∗$ è la porzione non ancora letta della stringa d'ingresso;
	- $γ ∈Γ^∗$ è la stringa composta da tutti i simboli contenuti all’interno della pila;
	- $z∈O^∗$ è la stringa presente sul nastro di uscita.

Le relazioni di transizione $c=<q,x,γ,z>⊢c′=<q′,x′,γ′,z′>$ possono essere di due categorie:

1. Se $δ(q,i,A) =<q′,α>$ è una mossa definita, si ha che $η(q,i,A) = w$, dove:
	- $γ= Aβ$, la pila contiene il simbolo $A$, utilizzato per eseguire la mossa, seguito dalla stringa $β$ composta da tutti i restanti simboli della pila;
	- $x = iy$, la stringa in ingresso è composta da un simbolo $i$, utilizzato per eseguire la mossa, seguito dalla stringa $y$ composta da tutti i restanti simboli non ancora letti;
	- $γ′ = αβ$, dopo la transizione, la pila contiene la stringa $α$ appena inserita, seguita dalla stringa $β$ composta da tutti i restanti simboli delle pila;
	- $x′ = y$, dopo la tranisizone, la stringa in ingresso è composta da tutti i simboli non ancora letti; in altre parole, la testina di lettura si sposta a destra di una posizione;
	- $z′ = zw$, dopo la transizione, alla stringa sul nastro di uscita viene concatenato il simbolo $w$ prodotto dalla funzione di traduzione.

2. Se $δ(q,ε,A) =<q′,α>$ è una mossa definita, si ha che $η(q,ε,A) = w$, dove:
	- $γ= Aβ$, la pila contiene il simbolo $A$, utilizzato per eseguire la mossa, seguito dalla stringa $β$ composta da tutti i restanti simboli della pila;
	- $γ′ = αβ$, dopo la transizione, la pila contiene la stringa $α$ appena inserita, seguita dalla stringa $β$ composta da tutti i restanti simboli della pila;
	- $x′ = x$, dopo la transizione, la stringa in ingresso è la medesima; in altre parole, la testina di lettura non si sposta;
	- $z′ = zw$, dopo la transizione, alla stringa sul nastro di uscita viene concatenato il simbolo $w$ prodotto dalla funzione di traduzione.

La **condizione di accettazione** della traduzione è quindi la seguente:

$∀x∈I^∗: x∈L∧z= η(x) ⇐⇒ c_0 =<q_0,x,Z_0,ε>⊢^∗c_F =<q∈F,ε,γ,z>$.


#### **2.2.2 Operazioni sugli Automi a Pila**

Gli Automi a Pila sono chiusi solamente rispetto all’operazione di complementazione. Ogni PDA può essere complementato seguendo le operazioni qui elencate:

1. Eliminazione dei cicli;
2. Aggiunta di stati di errore;
3. Eliminazione delle mosse spontanee che collegano stati non finali a stati finali;
4. Scambio di stati finali e non finali.

I PDA non sono aperti rispetto ad alcun’altra operazione, quindi un automa a pila non riesce a riconoscere i linguaggi generati dall’intersezione o l’unione di più linguaggi. Inoltre, gli automi a pila presentano ulteriori limitazioni dovute al fatto che lo stack di memoria sia di tipo distruttivo: per poter leggere le informazioni contenute in memoria è prima necessario eliminare tutte le altre informazioni che si trova al di sopra di essa. Quindi, linguaggi del tipo $L= \left \{a^nb^nc^n |n≥1\right \}$ non possono essere riconosciuti da normali PDA perchè una volta terminata la lettura delle $b$ e quindi una volta eliminati tutti i simboli sulla pila per controllare che il numero di $b$ sia uguale al numero di $a$, non rimane più alcuna informazione per poter verificare che il numero di $c$ sia uguale al numero delle altre lettere.



### **2.3 Macchine di Turing**

Le MT (Turing Machine) sono automi che presentano un numero finito di stati e che operano su un insieme di nastri infiniti a destra: un nastro di ingresso, un nastro di uscita e uno o più nastri di memoria. Ogni nastro è composto da celle inizializzate dal simbolo di blank (tramite cui si indica che la cella è vuota) che può essere sovrascritto con un qualsiasi simbolo dell’alfabeto in ingresso. Il dispositivo di controllo può muovere le testine di lettura dei nastri in maniera indipendente l’una dall’altra, spostandole a destra (R) o a sinistra (L) di una cella, oppure lasciandole ferme (S) nella posizione in cui si trovano. L’unica eccezione è costituita dal nastro di uscita che può essere spostato solamente a destra. In alternativa, l’automa può anche non effettuare alcuna operazione, fermandosi definitivamente. Formalmente:

- Una ==MT== a $k$ nastri è una tupla di 9 elementi $<Q,I,Γ,O,δ,η,q_0,Z_0,F >$, dove:
	- $Q$ è un insieme finito di stati;
	- $I$ è l’alfabeto di ingresso;
	- $Γ$ è l’alfabeto di memoria;
	- $O$ è l'alfabeto di uscita;
	- $δ:(Q−F)×I×Γ^k →Q×Γ^k×\left \{R,L,S\right \}^{k+1}$ è la funzione di transizione (eventualmente parziale);
	- $η: (Q−F) ×I×Γ^k →O×\left \{R,S\right \}$ è la funzione di uscita (eventualmente parziale), definita dove è definita la funzione di transizione $δ$;
	- $q_0∈Q$ è lo stato iniziale;
	- $Z_0∈Γ$ è il simbolo iniziale dell’alfabeto di memoria;
	- $F ⊆Q$ è un insieme di stati finali.

Si noti che la funzione di transizione $δ$ è definita in modo tale che non ci siano transizioni uscenti da uno stato finale.

- Una **configurazione** $c$ di una MT a $k$ nastri è una tupla di $k+3$ elementi $<q, x↑iy, α_1 ↑A_1β_1,...,α_k↑A_kβ_k, u↑o>$, dove:
	- $q∈Q$ è lo stato attuale in cui si trova l’automa;
	- $x↑iy$ è la posizione in cui si trova la testina di lettura del nastro di ingresso, con $x,y∈I^∗$e $i∈I$;
	- $α_1 ↑A_1β_1$ è la posizione in cui si trova la testina di lettura del primo nastro di memoria, con $α_1,β_1 ∈Γ^∗$ e $A_1 ∈Γ$;
	- $α_k ↑A_kβ_k$ è la posizione in cui si trova la testina di lettura del $k$-esimo nastro di memoria, con $α_k,β_k ∈Γ^∗$ e $A_k ∈Γ$;
	- $u↑o$ è la posizione in cui si trova la testina di lettura del nastro di uscita, con $u∈O^∗$ e $o∈O$;
	- $↑\notin I∪Γ ∪O$, rappresenta la posizione della testina di lettura di un determinato nastro; la testina di lettura punta la cella in cui è contenuto il carattere immediatamente alla destra del simbolo $↑$.

La configurazione iniziale $c_0$ di una MT a $k$ nastri è una tupla di $k+3$ elementi: $<q_0,↑iy,↑Z_0,...,↑Z_0,↑ (blank)>$. Quindi: $x= ε,A_1,...,A_k = Z_0,α_1,...,α_k = ε,β_1,...β_k = ε,u= ε$ e $o= (blank)$.

Ora, data la definizione di configurazione, è necessario anche formalizzare il significato di transizione $⊢$ tra due date configurazioni $c$ e $c′$ (detta anche mossa o passo computazionale):

- Siano: $c =< q,x ↑iy,α_1 ↑A_1β_1,...,α_k ↑A_kβ_k,u ↑o >$, con $x = xi,y= jy,α_1 = α_1A_1,...,α_k = α_kA_k$ e $β_1 = β_1B_1,...,β_k = β_kB_k, c′ =<q′,x′↑i′y′,α′_1 ↑A′_1β′_1,...,α′_k↑A′_kβ′_k,u′↑o′>$, $δ(q,i,A_1,...,A_k) =< p,C_1,...,C_k,N,N_1,...N_k >$, con $p ∈Q,N,N_1,...,N_k ∈\left \{R,L,S\right \}$e $C_1,...,C_k ∈Γ$, e $η(q,i,A_1,...,A_k) =<v,M >$, con $v∈O$ e $M ∈\left \{R,S\right \}$. Allora $c⊢c′$ se e solo se:
	1. Vale che $p= q′$;
	2. Vale anche una delle seguenti condizioni:
		(a) $x=x’, i=i’, y=y’$ ed $N=S$;
		(b) $x’=xi, i’=j, y’=y$ ed $N=R$;
		(c) $x’=x, i’=i, y’=iy$ ed $N=L$;
	3. Vale anche una delle seguenti condizioni, per $1 ≤r≤k$:
		(a) $α′_r= α_r,A′_r= C_r,β′_r=β_r$, ed $N_r = S$;
		(b) $α′_r= α_rC_r,A′_r= B_r,β′_r=β_r$, ed $N_r = R$; se $β_r = ε$, allora $A′_r=(blank)$ e $β′_r= ε$;
		(c) $α′_r= α_r,A′_r= A_r,β′_r = C_rβ_r$ ed $N_r = L$;
	4. Vale anche una delle seguenti condizioni:
		(a) $u’=u, o’=v$ ed $M=S$;
		(b) $u’=uv, o=(blank)$ ed $M=R$.

Se nei casi *2c* e *3c*, $x= ε$ oppure $α= ε$, allora non esiste una configurazione $c’$ tale che $c⊢c′$ e la macchina di Turing termina la propria esecuzione. Lo stesso comportamento si ottiene nel caso in cui le funzioni $δ$ ed $η$ non sono definite in $<1,i,A_1,...,A_k >$. In tali casi, $c$ viene anche definita configurazione di arresto.

In altre parole, se $δ(q,i,A_1,...,A_k) =<p,C_1,...,C_k,N,N_1,...,N_k>$, la condizione *1* vincola lo stato di $x′$ ad essere quello di arrivo della transizione. Le condizioni di tipo *2* definiscono l’evoluzione del nastro di ingresso al passaggio da $c$ a $c′$: se la testina rimane ferma (condizione *2a*), le tre parti in cui la testina divide il nastro saranno identiche in $c$ e $c′$; se la testina si muove a destra (condizione *2b*), la parte a sinistra della testina conterrà anche il simbolo corrente di $c$, il simbolo corrente di $c′$ sarà il primo simbolo della parte destra in $c$ e la rimanente parte destra di $c$ sarà la parte destra di $c′$; infine, se la testina si muove a sinistra (condizione *2c*), la parte a sinistra della testina in $c′$ conterrà tutti i simboli della parte sinistra in $c$, tranne l’ultimo che diventerà il simbolo corrente di $c′$ e la parte destra di $c′$ sarà composto dal simbolo corrente in $c$ seguito dalla sua parte destra. Analogamente le condizioni di tipo *3* specificano l’evoluzione dei nastri di memoria e le condizioni *4* quella del nastro di uscita.

Si introduce di seguito il teorema tramite cui si afferma la supremazia delle macchine di Turing nella computazione e nella traduzione.

- La classe di linguaggi riconosciuti dalle Macchine di turing include strettamente la classe dei linguaggi riconosciuti dagli Automi a Pila. Inoltre, le macchine di Turing sono trasduttori più **potenti** rispetto ai trasduttori a pila, per cui tutte le traduzioni effettuate da un PDT possono essere effettuate anche da una MT trasduttrice, ma non viceversa.

==Le macchine di Turing sono il formalismo più potente di cui siamo a disposizione==.


#### **2.3.1 Macchine di Turing come Accettatori**

Quando le macchine di Turing vengono impiegate per il riconoscimento di un determinato linguaggio o per definire nuovi linguaggi, il nastro di uscita viene completamente ignorato. Dunque, una MT utilizzata come accettatore è una tupla di 7 elementi, ottenuta eliminando gli elementi $O$ (l’alfabeto di uscita) ed $η$ (la funzione di uscita). Di conseguenza si omette anche la rappresentazione del nastro di uscita.

- Sia $M$ una MT a $k$ nastri. Una stringa $x∈I^∗$ è accettata da $M$ se e solo se:
		$c_0 =<q_0,↑x,↑Z_0,...,↑Z_0 >⊢^∗c_F <q∈F,x′↑iy, α_1 ↑A_1β_1,...,α_k↑A_kβ_k >$.

In altre parole, il linguaggio riconosciuto da una MT $M$ è composto da tutte e sole le stringhe che permettono di andare dallo stato iniziale ad uno stato finale. Inoltre, non è richiesto che al termine della computazione la testina si trovi al termine della stringa in ingresso: la MT $M$ può raggiungere uno stato finale anche senza aver completamente letto la stringa in ingresso.

Se $x / ∈ L$, $M$ può anche non raggiungere mai una configurazione di arresto e continuare la sua esecuzione per un tempo indefinito.


#### **2.3.2 Macchine di Turing come Trasduttori**

Quando le macchine di Turing vengono impiegate per la traduzione di linguaggi, ovvero per mappare stringhe di $I^∗$ in stringhe di $O^∗$, il nastro di uscita non viene più ignorato come nel caso degli accettatori.
Dunque, una MT utilizzata come trasduttore è una tupla di 9 elementi, esattamente come presentata nella definizione generale di MT:

- Sia $M$ una MT a $k$ nastri, definisce una traduzione $τ(x) = y$, con $τ_M : I^∗→O^∗$, se e solo se:
$c_0 =<q_0,↑x,↑Z_0,...,↑Z_0,↑ >⊢∗c_F =<q∈F,x′↑iy, α_1 ↑A_1β_1,...,α_k↑A_kβ_k, y↑(blank)>$.

In altre parole, una stringa $x$ viene tradotta in una stringa $y$ da una MT $M$ se esiste un cammino che parte da una configurazione iniziale con $x$ sul nastro di ingresso e termina in una configurazione finale con $y$ sul nastro di uscita.


#### **2.3.3 Altri Modelli di Macchine di Turing**

Il modello originario di automa, pensato da Alan Turing (padre fondatore dell’odierna informatica), era una macchina, simile a quelle analizzate nelle sezioni precedenti, con l’unica differenza che presentava un solo nastro infinito (sia a destra che a sinistra), utilizzato come ingresso, uscita e memoria. Formalmente:

- Una ==MT a nastro singolo== è una tupla di 5 elementi $<Q,A,δ,q_0,F >$, dove:
	- $Q$ è un insieme finito di stati;
	- $A$ è un alfabeto finito caratteristico del nastro;
	- $q_0 ∈Q$ è lo stato iniziale;
	- $F ⊆Q$ è l’insieme di stati finali;
	- $δ: (Q−F) ×A→Q×A×\left \{R,L,S\right \}$ è la funzione di transizione (eventualmente parziale).

Si noti che, le macchine di Turing ad 1 nastro sono un modello di automa differente rispetto ad una macchina di Turing a singolo nastro: nel primo caso, la TM presenta ben tre nastri (uno di ingresso, uno di uscita e uno di memoria), mentre nel secondo caso, la MT presenta un unico nastro.

- Le MT multinastro e le MT a nastro singolo sono formalismi equivalenti, ossia accettano la stessa classe di linguaggi e realizzano la stessa classe di traduzioni.

Ognuno dei modelli di macchine di Turing precedentemente analizzati possono essere dotati di nastri multidimensionali: il modello che se ne ricava è la MT con nastro multimensionale. Un nastro $k$-dimensionale è realizzato in modo che ogni cella sia identificata univocamente da una tupla di $k$ interi positivi. Anche questo modello di macchina di Turing è equivalente agli altri analizzati, in quanto si può stabilire una corrispondenza biiettiva fra $\mathbb{N} −\left \{0\right \}$ e $(\mathbb{N} −\left \{0\right \})^k$, che indicano rispettivamente l’insieme delle posizioni della testina per i nastri lineari e l’insieme delle posizioni della testina per i nastri multidimensionali. Un esempio importante è l’enumerazione delle celle del nastro bidimensionale, che si ottiene tramite la formula:

						$d(x,y) = x+ \frac{(x+ y)(x+ y−1)}{2}$

ottenuta con il metodo della diagonalizzazione.




## **Automi non Deterministici**


Tutti modelli analizzati fino ad ora sono deterministici, nel senso che una volta fissato lo stato iniziale e l’ingresso, il comportamento di tale automa è univocamente determinato. In altri termini, per ogni stato e per ogni ingresso è sempre possibile determinare a priori lo stato in cui l’automa termina la propria esecuzione.
Ci sono però casi in cui questo non è possibile, in quanto non si ha una conoscenza sufficientemente accurata del comportamento dell’automa per poter prevedere l’esatta evoluzione del modello. In tal caso si dice che l’automa è non deterministico.


### **3.1 Automi a Stati Finiti non deterministici**

Gli ==NFSA== (Nondeterministic Finite State Automaton) sono automi a stati finiti che presentano un numero finito di stati. Tali automi sono definiti come i corrispettivi automi deterministici, con l’unica differenza che presentano una funzione di transizione definita nel seguente modo:

								$δ: Q×I →℘(Q)$
	(in cui $℘(Q)$ rappresenta l'insieme delle parti di $Q$, i cui elementi sono insiemi di stati)

Di conseguenza, la chiusura riflessiva e transitiva di tale funzione, si definisce induttivamente nel seguente modo:

								$δ^∗(q,ε) = \left \{q\right \}, ∀q$
							$δ∗(q,xi) =\bigcup_{q′∈δ^∗(q,x)}^{ } δ(q′,i)$

Nel caso di accettatori, $x∈I^∗$ è accettata da un NFSA $<Q,I,δ,q_0,F >$ se e solo se $δ^∗(q_0,x)∩F= ∅$.
In altre parole, un NFSA può presentare diverse sequenze di transizioni per ogni dato stato e per ogni data sequenza di ingresso, quindi la chiusura riflessive e transitiva della funzione $δ$ non rappresenta più un singolo cammino coerente con la stringa di ingresso, ma un insieme di cammini possibili. Questo porta anche alla necessità di dover modificare la condizione di accettazione di una determinata stringa in ingresso: intuitivamente, infatti, tale nastro è accettato dall’automa se e solo se almeno una delle possibili sequenze di transizioni conduce a uno stato finale.

Gli automi non deterministici a stati finiti hanno la stessa potenza di calcolo dei corrispettivi automi deterministici, ma sono spesso più convenienti da utilizzare. Da qui il seguente teorema:

- **Teorema**: per ogni NFSA $A$, può essere costruito un FSA $A_D$ deterministico che accetti lo stesso linguaggio.

Infatti, dato un NFSA, si può costruire un FSA equivalente che ha come stati gli insiemi formati da stati dell’NFSA. La funzione di transizione è costruita in modo che se un insieme di stati è raggiungibile a partire da uno stato dell’NFSA, allora tale relazione deve essere presente anche nell’FSA sfruttando la costruzione degli stati come insiemi di stati dell’NFSA.


### **3.2 Automi a Pila non deterministici**

Un ==NPDA== (Nondeterministic Push Down Automaton) è un automa che presenta un numero finito di stati e una memoria organizzata su una struttura a pila. Tali automi sono definiti come i corrispettivi automi deterministici, con l’unica differenza che presentano una funzione di transizione definita nel seguente modo:

						$δ: Q×(I∪\left\{ε\right\}) ×Γ →℘_F(Q×Γ^∗)$

La relazione di transizione fra configurazioni su $Q×I^∗×Γ^∗$ è definita da $< q,x,γ >⊢< q′,x′,γ′>$ se e solo se vale una delle seguenti condizioni:

1. $x= ay,x′ = y,γ= Aβ,γ′ = αβ,<q′,α>∈δ(q,a,A)$;
2. $x= x′,γ= Aβ,γ′= αβ,<q′,α>∈δ(q,ε,A)$.

Inoltre, la stringa $x∈I^∗$ è accettata dall’automa se e solo se:

						$<q0,x,Z0 >⊢^∗<q∈F,ε,γ ∈Γ^∗>.$


Si noti che i PDA sono automi intrinsecamente non deterministici: infatti, nella prima definizione di automa a pila si era dovuto aggiungere il vincolo che, se per una determinata condizione era definita una ε-mossa, allora non era definita nessun’altra transizione che partisse da quello stato. Nella definizione appena data, invece, questo vincolo viene rimosso.


### **3.3 Macchine di Turing non deterministiche**

Una ==NTM== (Nondeterministic Turing Machine) è un automa che presenta un numero finito di stati e che opera su un insieme di nastri infiniti a destra. Tali automi sono definiti come i corrispettivi automi deterministici, con l’unica differenza che presentano una funzione di transizione e di accettazione definita nel seguente modo:

				$<δ,η>: (Q−F) ×I×Γ^k →℘(Q×Γ^k ×\left\{R,L,S\right\}^{k+1} ×\left\{R,S\right\})$

mentre per una NTM a nastro singolo, la funzione di transizione è definita nel seguente modo:

						$δ: (Q−F) ×A→℘(Q×A×\left\{R,L,S\right\})$


- **Teorema**: le macchine di Turing non deterministiche non sono più potenti delle corrispettive macchine di Turing deterministiche se utilizzate come riconoscitori di linguaggi.

Data una qualsiasi NTM $M$, è sempre possibile costruire una MT deterministica $M’$ che riconosce lo stesso linguaggio di M. Se si considera una computazione di M su una stringa in ingresso, questa è ben definita da un albero di configurazioni, in cui è inserita ogni configurazione raggiungibile dallo stato iniziale. Una stringa viene accettata solo se esiste almeno un cammino all’interno della struttura ad albero che si conclude in una configurazione finale. $M’$ potrà simulare il comportamento della MT $M$, ricostruendo in maniera sequenziale tutte le possibili computazioni di $M$. Si noti però che quando una stringa non viene accettata, la macchina di Turing $M$ potrebbe entrare in un ciclo infinito, senza mai terminare la propria esecuzione: per questo motivo, l’albero delle computazioni potrebbe presentare rami infiniti. La MT $M’$, che simula $M$, deve quindi evitare di visitare l’albero delle computazioni ’in profondità’ (ovvero tramite un algoritmo di depth first search), ossia seguendo un percorso fino al suo termine, prima di passare ad un ramo successivo, in quanto alcuni rami sono, appunto, infiniti. Conviene quindi visitare l’albero delle computazioni ’in ampiezza’ (ovvero tramite un algoritmo di breadth first search), ossia seguendo tutti i nodi dei rami sullo stesso livello. In questo modo, se esiste un cammino dell’albero di $M$ che porti all’accettazione della stringa, M’ riuscirà a trovarlo in un tempo finito, terminando la propria esecuzione. Altrimenti, se tutti i cammini di $M$ terminano in stati non finali, $M’$ terminerà la propria esecuzione senza aver trovato nessun nodo di accettazione e rifiuterà la stringa in ingresso.




## **Grammatiche**


Come visto in precedenza, spesso gli automi vengono utilizzati come modelli per il riconoscimento di linguaggi. Gli automi sono quindi uno strumento formale per la descrizione e la definizione di un determinato linguaggio, costituito dall’insieme delle stringhe accettate dall’automa stesso. Un altro formalismo utilizzato per la definizione di linguaggio sono le cosiddette ==grammatiche formali==, che definiscono un linguaggio fornendo il procedimento mediante cui si ottengono le stringhe appartenenti al linguaggio stesso.


### **4.1 Introduzione**

Una grammatica formale è un insieme di regole per costruire stringhe appartenenti ad un determinato linguaggio, attraverso il meccanismo di riscrittura, che consiste in un insieme di tecniche che determinano come sostituire le parti di una formula con parti più semplificate. In generale, un meccanismo di riscrittura consiste in un insieme di regole linguistiche, di cui una descrive l’oggetto principale come una sequenza di componenti. Ogni componente si può raffinare da elementi via via sempre più dettagliati, fino ad ottenere una sequenza di componenti elementari.

Una grammatica non è altro che un meccanismo linguistico, composto dall’oggetto principale, detto anche simbolo iniziale, da un insieme di componenti, a loro volta da sostituire durante il processo di derivazione, detti anche simboli non terminali, un insieme di elementi di base, detti anche simboli elementari, e da un insieme di regole di raffinamento o sostituzioni, chiamate produzioni.

- Una ==grammatica== $G$ è una tupla di 4 elementi $G=<V_T,V_N,P,S >$, dove:
	- $V_T$ è un insieme di simboli terminali (solitamente indicati con lettere minuscole), detto anche **alfabeto terminale**;
	- $V_N$ è un insieme di simboli non terminali (solitamente indicati con lettere maiuscole), tali che $V_T ∩V_N = ∅$, detto anche **alfabeto non terminale**; $V$ indica $V_T ∪V_N$;
	- $P$ è un insieme finito di $V_N^+ ×V^∗$, detto anche **insieme delle produzioni** di G. Un elemento $p=<α,β >∈P$ si indica con $α→β$, in cui $α$ è la parte sinistra di $p$, mentre $β$ è la parte destra di $p$;
	- $S$ è un elemento particolare di $V_N$, detto **assioma** o simbolo iniziale.

Quindi, un elemento che deve essere ancora raffinato è un simbolo non terminale, un elemento di base è un simbolo terminale, le componenti di un oggetto possono essere sia simboli terminali che non terminali, mentre una produzione corrisponde ad una regola di raffinamento.

- Data una grammatica $G$, si definisce su $V^∗$ la relazione binaria di derivazione immediata, indicata con il simbolo $⇒$ da $α$ a $β$. Tale relazione sussiste se e solo se $α= α_1γα_2,β= α_1δα_2$, con $α_1,α_2,δ∈V^∗,γ ∈V_N^+,γ →δ∈P$.

Data la definizione di derivazione immediata, si può anche definire la chiusura riflessiva e transitiva, indicata con il simbolo $⇒^∗$, che opera su una serie di stringhe (di simboli elementari o non elementari), anzichè che su una sola stringa.
Date le precedenti definizioni, si può ora definire il linguaggio generato da una grammatica, tramite la seguente definizione:

- Data una grammatica $G$, il linguaggio $L(G)$ generato da $G$ è definito come:

							$L(G) = \left\{x|S ⇒^∗x,x∈V_T^∗\right\}$

Quindi il linguaggio generato da una grammatica è costituito da tutte e sole le stringhe di simboli terminali, derivati a partire dall’assioma $S$, applicando un numero qualsiasi di sostituzioni.


### **4.2 Classificazione**

Una volta definite cosa siano le grammatiche, è possibile classificarle in base alle loro proprietà e in base alla forma ammessa per le produzioni. Tale classificazione viene anche detta ==Gerarchia di Chomsky==, tramite cui si dividono le grammatiche in quattro categorie:

- Tipo 0 (NON RISTRETTE): sono grammatiche definite come nella definizione generale, ovvero grammatiche che non possiedono nessuna restrizione nel tipo di produzione;
- Tipo 1 (CONTESTUALI): sono grammatiche a cui si introduce il vincolo per cui le produzioni possono essere solo nella forma $αAβ →αγβ$, dove $α,β,γ ∈V$ e $A ∈V_N$, con $γ ̸= ε$; inoltre, la derivazione $S →ε$ è consentita solo se $S$ non appare a destra in nessuna regola di derivazione;
- Tipo 2 (NON CONTESTUALI): sono grammatiche a cui si introduce il vincolo per cui ad ogni produzione $α→β ∈P$ si verifica che $|α| = 1$ (quindi $α∈V_N$) e $β ∈V^∗$;
- Tipo 3 (REGOLARI): sono grammatiche a cui si introduce il vincolo per cui ad ogni produzione $α →β ∈P$ si verifica che $|α | = 1$ (quindi $α ∈V_N$) e che $β$ sia in una sola delle seguenti forme: $aB, Ba, a$ oppure $ε$, con $a ∈V_T$ e $B ∈V_N$; inoltre, la derivazione $S →ε$ è consentita solo se $S$ non appare a destra in nessuna regola di derivazione.


*Gerarchia di Chomsky*:

![[Algoritmi e Principi dell'Informatica-1779628545932.webp|524]]


### **4.3 Grammatiche e Automi**

Studiando le grammatiche e i linguaggi da esse generate, si può osservare una certa corrispondenza con gli automi analizzati nei capitoli precedenti. Si introducono qui alcuni teoremi che mettono in luce la correlazione esistente fra automi e grammatiche:

- **Teorema**: dato un FSA $A$, è possibile costruire una grammatica regolare (di tipo 3) $G$ ad esso equivalente, ossia in grado di riconoscere lo stesso linguaggio riconosciuto da $A$, e viceversa. Dunque, le grammatiche regolari e gli automi a stati finiti sono modelli differenti per descrivere la stessa classe di linguaggi.

Dato un FSA $A=< I,δ,q_0,F >$, si può costruire una grammatica $G=< V_N,V_T,P,S >$ regolare, tale che:
	- $V_N = Q$;
	- $V_T = I$;
	- $S= q_0$;
	- $∀B →bC ⇐⇒ C ∈δ(B,b)$;
	- $∀B →ε,B ∈F$.

Data una grammatica $G=< V_N,V_T,P,S >$ regolare, si può costruire un FSA $A=< I,δ,q_0,F >$, tale che:
	- $Q= V_N ∪\left\{q_F\right\}$;
	- $I= V_T$;
	- $q_0 = S$;
	- $F= \left\{q_F\right\}$;
	- $∀A→bC,C ∈δ(A,B)$;
	- $∀A→b,q_F ∈δ(A,b)$.

In generale, l’automa a stati finiti $A$, ottenuto a partire dalla grammatica regolare $G$, è non deterministico.

- **Teorema**: dato un NPDA $A$ è possibile costruire una grammatica $G$ non contestuale (di tipo 2) ad esso equivalente, ossia in grado di riconoscere lo stesso linguaggio riconosciuto da $A$, e viceversa; dunque, le grammatiche non contestuali e gli automi a pila non deterministici sono modelli differenti per descrivere la stessa classe di linguaggi.

- **Teorema**: data una MT $M$ utilizzata come accettatore di linguaggi è possibile costruire una grammatica generale $G$ (di tipo 0) ad essa equivalente, ossia in grado di riconoscere lo stesso linguaggio riconosciuto da $M$, e viceversa. Dunque, le grammatiche non ristrette e le macchine di Turing sono modelli differenti per descrivere la stessa classe di linguaggi.


### **4.4 Espressioni Regolari**

Un’espressione regolare è un’espressione utilizzabile per denotare un linguaggio attraverso la struttura delle stringhe che lo compongono.

- Dato un alfabeto di simboli terminali denotato con $V_T$, si definiscono su di esso le espressioni regolari e i corrispondenti linguaggi denotati:
	- $∅$ è un’espressione regolare che denota il linguaggio vuoto;
	- $∀a∈V_T,a$ è un’espressione regolare che denota il linguaggio formato solo dal simbolo $a$;
	- Se $R_1$ ed $R_2$ sono espressioni regolari, anche la loro unione, indicata con $R_1 + R_2$ o $R_1 | R_2$, è un’espressione regolare;
	- Se $R_1$ ed $R_2$ sono espressioni regolari, anche la loro concatenazione, indicata con $R_1·R_2$, è un’espressione regolare;

Se R `e un’espressione regolare, anche la stella di Kleene di R, indicata con R∗, `e un’espressione

regolare.24 CAPITOLO 4. GRAMMATICHE

Nessun’altra stringa `e un’espressione regolare.

Gli operatori |,·

,

∗ definiti per le espressioni regolari, hanno un implicito ordine di applicazione, se

non indicato diversamente dall’uso delle parentesi. In particolare, * ha la precedenza rispetto a·, che ha

a sua volta la precedenza su |.

Inoltre, vale anche il seguente teorema:

Teorema 4.4.1. La classe dei linguaggi denotati dalle espressioni regolari coincide con la classe dei

linguaggi regolari.

4.5 Pattern

Definizione 4.5.1. Un sistema di pattern `e una tripla <A,V,p>, dove:

A `e un alfabeto;

V `e un insieme di variabili tale che A∩V= ∅;

p `e una stringa su A∪V detta pattern.

Il linguaggio generato dal sistema di pattern consiste in tutte le stringhe su Aottenute da psostituendo

ogni variabile in p con una stringa su A.

Ad esempio, il pattern <0,1,v1,v2,v1v10v2 > rappresenta il linguaggio composto dalle stringhe che

iniziano con 0 (nel caso in cui v1 = ε) oppure che iniziano con una qualunque stringa sull’alfabeto A(in

questo caso binario) ripetuta due volte, seguita da uno 0 e terminano con una qualunque altra stringa

dell’alfabeto A (inclusa ε).

Le espressioni regolari seguono la stessa idea dei sistemi di pattern, ma hanno un potere espressivo

differente: nello specifico `e possibile esprimere certi linguaggi con i pattern, ma non con le espressioni

regolare, e viceversa, `e possibile esprimere alcuni linguaggi con le espressioni regolari, ma non con i

pattern. Per tale motivo, i due modelli si dicono essere non confrontabili

4.6 Riepilogo

Tabella 4.1: Relazione fra grammatiche, linguaggi e automi

Gerarchia Grammatiche Linguaggi Automa minimo

tipo 0 Generali Ricorsivamente enumerabili TM

tipo 1 Dipendenti dal contesto Dipendenti dal contesto LBA*

tipo 2 Non contestuali Non contestuali NPDA

tipo 3 Regolari Regolari FSA

* Gli LBA (Linear Bounded Automata) sono un particolare tipo di macchina di Turing non determi-

nistica in cui la lunghezza del nastro `e funzione lineare della dimensione della stringa in ingresso. Tali

automi non sono stati trattati in questo documento.Capitolo 5

Computabilit`a

In questa sezione si cercher`a di rispondere alla domanda: quali problemi possono essere affrontati e risolti

mediante gli automi analizzati? Si ricordi che automi e grammatiche, pur essendo modelli matematici,

si possono considerare dispositivi meccanici per la risoluzione di problemi e che esistono formalismi che

hanno un potere espressivo maggiore di altri, ossia sono in grado di riconoscere una classe di linguaggi

che altri formalismi non riescono a riconoscere. Inoltre, si ricordi che, nessun formalismo `e pi`u potente

delle macchine di Turing, sia dal punto di vista del riconoscimento che della traduzione di linguaggi e,

per tanto, sono detti formalismi massimi.

5.1 Formalizzazione dei Problemi

Molti problemi possono essere opportunamente descritti come il riconoscimento di un determinato lin-

guaggio o coma la sua traduzione in un altro linguaggio. Ogni problema matematico `e descrivibile

mediante una di queste forme, alla sola condizione che il dominio di tale problema sia un insieme nume-

rabile, in maniera tale che i suoi elementi si possono porre in corrispondenza biunivoca con gli elementi

di N o, se si preferisce, di V∗, in cui V rappresenta un alfabeto. Dunque, il problema di origine si pu`o

riformulare come il problema di calcolo di una funzione f : N →N. Quanto detto `e in perfetto accordo

con tutti i formalismi matematici esaminati fino ad ora: questi, infatti, sono discreti e hanno un dominio

matematico numerabile.

Il riconoscimento di linguaggi e la loro traduzione sono due formulazioni differenti di un problema, che

sono facilmente riducibili l’uno all’altro. Infatti, dato il problema di stabilire se una determinata stringa

x appartenga al linguaggio L, tale problema pu`o anche essere impostato come la traduzione τL(x), per

cui τL(x) = 1 se x∈L, τL(x) = 0 altrimenti. Viceversa, data la traduzione τ : V∗

1 →V∗

2 , si pu`o definire

il linguaggio seguente:

Lτ = {z |z = x$y, x ∈V∗

1 , y= τ(x) ∈V∗

2 , $ / ∈(V1 ∪V2)}Ovvero il linguaggio formato da una

stringa e la sua traduzione, separati dal simbolo $. Un dispositivo che riconosce il linguaggio Lτ pu`o

essere utilizzato come trasduttore che calcola τ: per ogni x, infatti, `e possibile enumerare tutte le y∈V∗

2

e verificare se x$y ∈Lτ oppure no. Prima o poi, se la funzione τ(x) ̸= ⊥, verr`a trovata una stringa per

cui la macchina risponder`a positivamente.

5.2 Tesi di Church

Le macchine di Turing, come visto in precedenza, sono il formalismo pi`u potente che si ha a disposizione

per il calcolo computazionale: ogni programma eseguibile da un calcolatore moderno pu`o essere eseguito

anche da una macchina di Turing. Dunque, le macchine di Turing hanno la stessa espressivit`a dei

linguaggi di programmazione ad alto livello, detti anche Turing completi.

Pi`u formalmente, data una TM M, `e possibile costruire un programma, scritto in un determinato

linguaggio di programmazione (come C, Java ecc...), che simuli il ocmportamento di M, purch`e il calco-

latore disponga di una quantit`a di memoria sufficiente durante l’esecuzione. Inoltre, dato un programma

scritto in un determinato linguaggio di programmazione, `e possibile coistruire una TM M che calcoli la

stessa funzione calcolata dal programma.

Tesi 5.2.1 (Tesi di Church - Prima Parte). Non esiste alcun formalismo, per modellare una determinata

computazione meccanica, che sia pi`u potente delle TM e dei formalismi ad essi equivalenti.

25`

26 CAPITOLO 5. COMPUTABILIT

A

La tesi di Church non `e un teorema perch`e per sua natura non `e dimostrabile, in quanto andrebbe

verificato ogni qual volta si introducesse un nuovo formalismo computazionale.

In base a questo risultato si pu`o affermare che, se si riesce a dimostrare che un determinato problema

`e risolvibile da una TM, allora `e sicuramente possibile risolverlo mediante un modello matematico di

calcolo, che abbia la stessa potenza delle macchine di Turing. Viceversa, se si dimostra che un problema

non pu`o essere risolto da una TM, allora `e verificato che tale problema `e irrisolvibile da qualunque

modello matematico.

Si introduce ora il concetto di algoritmo, centrale nell’informatica. Per algoritmo si intende la pro-

cedura di risoluzione di un problema mediante un dispositivo automatico di calcolo. Gli algoritmi si

possono anche intendere come un metodo astratto di descrizione dei programmi eseguibili, ovvero una

sequenza di comandi che, una volta eseguiti, portano alla risoluzione del problema.

Ogni algoritmo ha le seguneti propriet`a:

1. Un algoritmo deve contenere una sequenza finita di istruzioni;

2. Ogni istruzione deve essere immediatamente eseguibile da qualche procedimento meccanico di cal-

colo, ossia deve esistere un processore che sia in grado di comprendere univocamente le istruzioni

e di eseguirle producendo risultati precisi ed inequivocabili;

3. Il processore `e dotato di celle di memoria in cui possono essere immagazzinati i riultati intermedi;

4. La computazione `e discreta, ossia l’informazione `e codificata in forma digitale e la computazione

procede attraverso passi discreti;

5. Gli algorimi vengono eseguiti deterministicamente;

6. Non esiste un limite finito sui dati di ingresso e di uscita: ogni calcolatore pu`o ricevere in ingresso

o emettere in uscita stringhe di lunghezza arbitraria;

7. Non esiste un limite alla quantit`a di memoria richiesta per effettuare i calcoli;

8. Non esiste un limite al numero di passi discreti richiesti per effettuare un calcolo ed `e dunque

possibile avere computazioni infinite.

La tesi di Church non si ferma solo nell’affermazione che nessun formalismo sia pi`u espresivo delle

TM, ma afferma anche che nessun algoritmo `e in grado di risolvere un problema che non `e risolvibile da

una TM. Formalmente:

Tesi 5.2.2 (Tesi di Church - Seconda Parte). Ogni algoritmo per la soluzione automatica di un problema

pu`o essere codificato in termini di una TM (o di un formalismo a potenza equivalente).

Teorema 5.2.1. Ogni funzione (o problema), per cui esiste una TM che la calcoli (o risolva), si dice

computabile o calcolabile (o risolvibile). Un problema risolvibile la cui risposta sia booleana ed esistente

per ogni valore del dominio di definizione (ossia `e formalizzato da una funzione calcolabile e totale) si

dice decidibile.

Grazie alla seconda parte della tesi di Church si pu`o affermare che `e possibile studiare i limiti

del calcolo automatico indipendentemente dalla formalizzazione del problema e del particolare modello

computazionale.

5.3 Enumerazione delle TM

Le macchine di Turing possono essere viste come dei calcolatori astratti, specializzati nella risoluzione di

un solo problema e non porgrammabili. Ci si pone quindi la domanda: ’le TM sono in grado di simulare

i calcolatori programmabili e di risolvere i problemi da N a N?’

Per poter risondere a tale domanda, si noti innanzitutto che dato un qualsiasi insieme S, questo pu`o

essere enumerato algoritmicamente se `e possibile stabilire una biiezione fra l’insieme S e l’insieme dei

numeri naturali N, calcolabile attraverso un algoritmo o da una TM. Alla stessa maniera `e possibile

enumerare algoritmicamente l’insieme delle TM tramite una biiezione E : {TM}↔N. Tale biiezione

`e implementabile da un algoritmo che riceve in ingresso un numero n e ritorna la n-esima macchina

di Turing. Un’enumerazione calcolabile da una TM viene chiamata G¨odelizzazione, mentre il numero

naturale biiettivamente associato da tale enumerazione ad una TM `e detto numero di G¨odel della TM.5.4. MACCHINE DI TURING UNIVERSALI 27

Inoltre, `e noto che una TM M pu`o risolvere una funzione fM : D→R, con D ed R opportunamente

codificati nell’alfabeto di M, dunque si indicher`a con fy la funziuone calcolata dalla y-esima macchina

di Turing, indicata con My = E(y).

5.4 Macchine di Turing Universali

Le UTM (Universal Turing Machines) sono TM in grado di modellare dispositivi generali di risoluzione

dei problemi, in cui il problema da risolvere non viene codificato nella struttura del dispositivo (come

avviene per le TM), ma gli viene fornito come input, assieme ai dati con cui operare (esattamente

come gli oderni calcolatori). Le UTM sono quindi MT che calcolano la funzione g(y,x) = fy(x), in

cui y rappresenta la funzione fy, calcolata dalla TM My, ed x rappresenta l’ingresso su cui My opera;

calcolano, dunque, il valore della funzione fy applicata ad x.

Come si pu`o osservare, la UTM cos`ı definita non sembra appartenere all’insieme delle macchine di

Turing, in quanto la funzione g(y,x) `e opera da N ×N ad N, anzich`e da N ad N come tutte le altre TM.

`

E per`o possibile, come gi`a dimostrato in precedenza, definire una biiezione calcolabile algoritmicamente,

tramite la funzione:

d(x,y) = x+ (x+ y)(x+ y−1)

2

che mette in corrispondenza l’insieme N ×N, composto dalle coppie di numeri naturali, all’insieme N,

composto da numeri naturali.

Graficamente, `e come visitare le coppie di punti nel piano in un ordine prefissato, dove la posizione

di un punto nella visita rappresenta il numero naturale associato alla coppia che identifica le coordinate

del punto.

Figura 5.1: Grafico di biiezione

Si osservi che la funzione g(y,x) `e computabile da una macchina di Turing, ossia ∃i∈N : fi = g, ed

`e possibile calcolarla tramite i seguenti passaggi:

1. Si sceglie un alfabeto finito A per codificare i numeri naturali ed ogni altra informazione richiesta

per la computazione;

2. Si traduce la rappresentazione di n in un’opportuna rappresentazione della coppia <x,y > corri-

spondente ad n. La rappresentazione decimale di n pu`o essere tradotta nelle due rappresentazioni

decimali di x ed y, separate dal simbolo $;

3. Si traduce y in un’opportuna codifica della TM y-esima My nella enumerazione di G¨odel;

4. Si simula la computazione di My su x.

Teorema 5.4.1. Per ogni x ed ogni y, esiste e si pu`o costruire una macchina di Turing universale in

grado di calcolare g(y,x) = fy(x)

Tramite questo teorema si pu`o affermare che `e possibile creare una macchina di Turing che simuli il

comportamento degli odierni calcolatori ”general purpose”.`

28 CAPITOLO 5. COMPUTABILIT

A

5.5 Problemi Algoritmicamente Irrisolvibili

Come si `e visto in precedenza, tutte le funzioni computabili fy : N →N si possono enumerare: questo

significa che la cardinalit`a dell’insieme delle funzioni computabili `e pari ad ℵ0, ovvero alla cardinalit`a dei

numeri naturali N. L’insieme delle funzioni {f : N →N}contiene la classe delle funzioni {f : N →{0,1},

in quanto {0,1}⊆N. Quindi, poich`e |{f : N →N}| ≥ |{f : N →{0,1}}|= ℘(N) = 2ℵ0 , si pu`o

dedurre che la cardinalit`a della classe delle funzioni da N ad N `e strettamente maggiore della cardinalit`a

della classe delle funzioni computabili: dunque, gran parte delle funzioni di N non pu`o essere calcolata.

Ora, quando si vuole definire una funzione si usa un linguaggio che la esprima, ovvero un sottoinsieme

del monoide libero su di un determinato alfabeto finito: dunque, il linguaggio `e un insieme numerabile.

Si ricava quindi che la classe delle funzioni denotabili `e a sua volta numerabile.

Quando si scrive un programma, ci sono diverse propriet`a che si vorebbero garantire. Una di queste `e

la terminazione del programma, ovvero la garanzia che, dato un qualsiasi ingresso conforme al programma

stesso, esso termini la propria computazione e non vada, dunque, in un ciclo infinito. Nella realt`a, per`o,

non `e possibile garantire a priori la terminazione del programma per un generico valore in ingresso,

n`e decidere atgtraverso un algoritmo se ci`o possa avvenire in corrispondenza di uno specifico valore

in ingresso. Pi`u in generale, il problema della terminazione del calcolo automatico `e in generale non

decidibile, nonostante tale problema sia definibile. Si `e quindi constatato che esistono problemi definibili,

ma che non possono essere risolti algoritmicamente: dunque, l’insieme dei problemi definibili contiene

strettamente l’insieme dei problemi risolvibili, nonostante entrambi siano numerabili e con la stessa

cardinalit`a.

fy risolvibili

f definibili

f : N →N (problemi totali)

Figura 5.2: Gerarchia dei problemi

Teorema 5.5.1 (Halting Problem). Nessuna TM pu`o calcolare la funzione g : N ×N →{0,1}definita

nel seguente modo:

g(x,y) = if fy(x) = ⊥then1 else0

La dimostrazione di tale teorema si ottiene tramite la tecnica della diagonale, detta anche metodo

di Cantor: l’obiettivo `e quello di mostrare che un’enumerazione di oggetti di cardinalit`a almeno 2, non

`e completa, ossia che un oggetto che si vorrebbe trovare all’interno di tale enumerazione in realt`a non `e

presente. L’enumerazione di una successione pu`o essere rappresentata come una tabella con un numero

infinito di righe. L’elemento che non compare in tale tabella viene individuato per assurdo considerando

inizialmente la diagonale d (dunque di `e l’elemento che si trova all’i-esima riga e all’i-esima colonna) e

poi componendo una diagonale d′tale che, per ogni i, d′

i sia diverso da di.

Teorema 5.5.2. Nessuna TM `e in grado di calcolare la funzione totale k definita nel seguente modo:

k(x) = if fx(x) ̸= ⊥then1 else0

Questo problema rappresenta un caso speciale della funzione g(y,x) in quanto k(x) = g(x,x), dunque

la calcolabilit`a della funzione k `e direttamente correlata alla calcolabilit`a della funzione g. Si noti

che, in generale, se un problema `e irrisolvibile, pu`o accadere che un suo caso particolare sia risolvibile,

mentre una sua generalizzazione `e necessariamente irrisolvibile. Al contrario, se un problema `e risolvibile,5.6. PROBLEMI DI DECISIONE 29

pu`o accadere che una sua generalizzazione diventi irrisolvibile, mentre un suo caso particolare rimane

sicuramente risolvibile.

Un altro teorema certamente importante `e il seguente:

Teorema 5.5.3. Nessuna TM `e in grado di calcolare la funzione k definita nel seguente modo:

k(y) = if fy(x) ̸= ⊥then1 else0

Da un punto di vista pratico questo problema `e interessante perch`e qualifica tutti i possibili dati in

ingresso. Afferma, infatti, l’irrisolvibilit`a del problema di decidere se un certo programma termini la pro-

pria esecuzione per qualsiasi dato in ingresso o se, al contrario, per qualche dato il programma andrebbe

in loop.Nel caso precedente, invece, si era interessati al problema di sapere se un certo programma con

certi dati avrebbe terminato o meno la propria esecuzione.

In definitiva, si `e constatato che esistono problemi non risolvibili algoritmicamente. Ci`o non esclude

comunque la possibilit`a di trovare una soluzione per tali problemi, in quanto non tutti i problemi sono

risolvibili tramite un procedimento algoritmico.

5.6 Problemi di Decisione

Un problema di decisione `e una domanda che ha come uniche risposte si o no (0, 1). Questo pu`o anche

essere espresso come un problema di appartenenza di un determinato elemento ad un certo insieme.

Pi`u in generale si noti che una qualsiasi propriet`a di un determinato elemento di un insieme pu`o essere

formalizzata come un suo sottoinsieme (ad esempio, la propriet`a di terminazione del calcolo per ogni

valore dei dati in ingresso individua un sottoinsieme dell’insieme di tutti i programmi).

In questa sezione si prendono in particolare considerazione i sottoinsiemi di N, indicati convenzional-

mente con S ⊆N. Quindi, formalmente, dato un determinato elemento x∈N e un insieme S, si cerca

di capire se x appartenga ad S.

Definizione 5.6.1. La funzione caratteristica cS : N →{0,1}di un insieme S `e definita come segue:

cS(x) = if x∈S then1 else0

La risolvibilit`a del problema di appartenenza ad un insieme (detta anche ricorsivit`a dell’insieme)

dipende dalla computabilit`a della funzione caratteristica cS, come definito di seguito:

Definizione 5.6.2. Un insieme S `e ricorsivo (o decidibile) se e solo se la sua funzione caratteristica `e

computabile.

Si noti, inoltre, che per ogni insieme S, la sua funzione caratteristica cS `e totale: infatti, dato un

qualsiasi elemento x∈N, questo necessariamente apparteniene o non appartiene all’insieme.

Definizione 5.6.3. Un insieme S `e ricorsivamente enumerabile (o semidecidibile) se e solo se `e l’insieme

vuoto oppure `e l’immagine di una funzione totale e computabile gs, ovvero:

S= Igs

= {x|∃y,y∈N ∧x= gs(y)}

Gli insiemi decidibili devono il loro nome al fatto che il problema di appartenenza pu`o essere risolto

tramite un algoritmo meccanico e che, quindi, una TM che implementi la loro funzione caratteristica

fornisce necessariamente una risposta al quesito se x∈S,∀x∈N. Inoltre, per ogni insieme ricorsivamente

numerabile S `e possibile costruire una sequenza x0 = gS(0),x1 = gS(1),x2 = gS(2),... tale per cui, se

x ∈S, allora esiste i tale che x = gS(i). In questo caso, esaminando la sequenza di elementi {xi}

si riuscir`a a trovare l’elemento x, concludendo che questo appartiene all’insieme S. Perci`o, se per un

¯

qualsiasi

i risultasse che x / ∈{gS(i) |0 ≤i≤¯

i}non si potrebbe concludere n`e che x∈S, n`e che x / ∈S:

per questo motivo, l’insieme S viene anche detto semidecidibile.

Teorema 5.6.1. Se S `e ricorsivo, `e anche ricorsivamente enumerabile.

S `e ricorsivo se e solo se sia S che¯

S= N−S sono ricorsivamente enumerabili.`

30 CAPITOLO 5. COMPUTABILIT

A

Quindi, riepilogando, si dice che un insieme S `e:

Ricorsivo (o Decidibile), se e solo se la sua funzione caratteristica cS `e computabile;

Ricorsivamente enumerabile (o Semidecidibile), se e solo se:

– S `e l’insieme vuoto;

– S `e l’immagine di una funzione gS totale e computabile (detta generatrice);

quindi, S= IgS

= {gS(0),gs(1),gS(2),...}

Si consideri ora il seguente teorema:

Teorema 5.6.2. Per ogni insieme S, se i∈S implica che fi sia totale e se per ogni funzione f totale e

computabile, esiste i∈S |f= fi, allora S non `e ricorsivamente enumerabile.

Informalmente, questo teorema stabilisce che tutte le funzioni totali computabili non sono ricorsi-

vamente enumerabili (mentre le funzioni parziali computabili lo sono). Dunque, tale teorema afferma

implicitamente che non esiste nessun formalismo ricorsivamente enumerabile in grado di definire tutte

e sole le funzioni totali e computabili: infatti, gli FSA sono in grado di definire le funzioni totali, ma

non tutte, le TM definiscono tutte le funzioni computabili, ma anche quelle non totali, e un linguaggio

di programmazione (come il C) `e in grado di definire tutti gli algoritmi, ma anche anche quelli che non

terminano mai.

Si cerca quindi di comprendere se sia possibile eliminare le funzioni non totali: per far ci`o, si prenda

in considerazione una generica funzione parziale, ad esempio, arricchendo N con il valore {⊥}o con

qualsiasi altro simbolo che indichi che la funzione non `e definita per certi valori. Tale trasformazione

da funzione parziale a totale, per`o, non pu`o essere applicata perch`e nel passaggio `e possibile perdere la

computabilit`a della funzione. Questo risultato `e enunciato nel seguente teorema:

Teorema 5.6.3. Non esiste una funzione totale e computabile h che sia un’estensione della seguente

funzione: g(x) = if fx(x) ̸= ⊥thenfx(x) + 1 else⊥

Tale teorema, afferma quindi che non `e possibile estendere una funzione parziale ad una totale, in

quanto si potrebbe perdere la sua computabilit`a.

Vale anche il seguente risultato:

Teorema 5.6.4. Un insieme S `e ricorsivamente enumerabile se e solo se S= Dh, in cui h `e una funzione

parziale e computabile (S= {x|h(x) ̸= ⊥}), oppure se e solo se S= Ig, in cui g `e una funzione parziale

e computabile (S= {x|x= g(y),y∈N}).

Quindi, dato l’insieme K= {x|f(x) ̸= ⊥}questo `e semidecidibile perch`e K= Dh, con h(x) = fx(x),

ma `e anche indecidibile in quanto la funzione caratteristica dell’insieme K, definita come cK(x) =

if fx(x) ̸= ⊥then 1 else 0, non `e computabile. Si `e appena dimostrato che esistono insiemi che sono

semidecidibili, ma allo stesso tempo indecidibili.

insiemi ricorsivi

insiemi RE*

℘(N)

Figura 5.3: Gerarchia degli insiemi

*Con RE si indicano gli insiemi Ricorsivamente Enumerabili.

Si noti che tutte le inclusioni sono strette.5.7. TEOREMI DI KLEENE E RICE 31

5.7 Teoremi di Kleene e Rice

Teorema 5.7.1 (Teorema di Kleene del punto fisso). Sia t una qualunque funzione totale e computabile.

Allora `e sempre possibile trovare un intero p, tale per cui:

fp = ft(p)

La funzione fp `e detta punto fisso di t, perch`e t trasforma fp in fp stessa.

Teorema 5.7.2 (Teorema di Rice). Sia F un insieme generico di funzioni computabili. L’insieme

S= {x |fx ∈F}degli indici delle TM che calcolano le funzioni di F, `e ricorsivo se e solo se F= ∅

oppure F `e l’insieme di tutte le funzioni computabili.

Il teorema di Rice ha un forte impatto pratico negativo, in quanto afferma che. in tutti i casi non

banali, S non `e decidibile. Non `e quindi possibile stabilire algoritmicamente se un dato algoritmo sia in

grado di risolvere un determinato problema, n`e se due programmi siano equivalenti (ossia se calcolino

la stessa funzione). Il grande impatto pratico del teorema di Rice deriva dal fatto che il concetto di

sottoinsieme F di funzioni computabili `e un’espressione formale del concetto generale di propriet`a di

problemi risolvibili: una propriet`a degli elementi di un insieme `e un sottoinsieme dell’insieme dato e una

funzione computabile `e una formalizzazione del concetto di problema risolvibile; quindi, il teorema di

Rice efferma che non `e possibile stabilire se un determinato algoritmo risolve un problema pur risolvibile

che godia di una qualsiasi propriet`a non banale.`

32 CAPITOLO 5. COMPUTABILIT

ACapitolo 6

Logica

I linguaggi possono essere rappresentati in modi differenti, tramite modelli e astrazioni via via pi`u potenti,

tra cui:

Insiemi;

Pattern;

Espressioni Regolari;

Modelli Operazionali (come gli Automi);

Modelli Generativi (come le Grammatiche);

Modelli Dichiarativi (come la Logica).

I concetti di logica introdotti di seguito sono utilizzati per definire in maniera differente i linguaggi.

6.1 Logica Proposizionale

Il calcolo proposizionale, detto anche logica proposizionale, `e un modello dichiarativo formale della logica

matematica che si basa sul concetto di proposizione, ovvero frasi che possono assumere solamente il valore

vero o il valore falso. In generale, ogni linguaggio consiste di una sintassi e di una semantica: la sintassi

`e l’insieme delle regole attraverso cui `e possibile costruire le frasi di cui il linguaggio `e composto, mentre

la semantica spiega il significato delle varie frasi del linguaggio.

Sintassi In modo formale:

Definizione 6.1.1. La logica proprosizionale `e composta da un linguaggio L, il cui alfabeto `e costituito

dai seguenti elementi:

1. Un insieme numerabile (finito o non) di proposizioni (simboli di relazione nullaria), che possono

essere simboli, stringhe o frasi;

2. Un insieme di connettivi logici:¬(NOT), ∧(AND), ∨(OR), ⇒(Implicazione) e ⇔(Coimplicazione);

3. Un insieme di simboli di punteggiatura: ( e )

I simboli che compongono l’alfabeto sono privi di significato: assegnarne il significato `e compito della

semantica.

Una proposizione si dice essere atomica quando non pu`o essere scomposta in parti pi`u piccole. Nel

caso contrario, la proposizione `e composta da due o pi`u proposizioni pi`u piccole legate fra loro trami-

te i connettivi logici appena introdotti. Le parentesi sono utilizzare per modificare la precedenza dei

connettivi, che di base avrebbero il seguente ordine logico:¬,∧,∨,⇒,⇔.

La sintassi del linguaggio definisce le sequenze ammissibili di simboli sull’alfabeto, le cosiddette for-

mule ben formate (fbf). L’insieme di queste formule ben definite su L`e il pi`u piccolo insieme tale che

ogni proposizione `e una formula e, se F e Gsono formule, allora anche¬F, F∧G, F∨G, F ⇒GF ⇔G

3334 CAPITOLO 6. LOGICA

Tabella 6.1: Tabella della verit`a dei connettivi logici

F G¬F F ∧G F ∨G F ⇒G F ⇔G

T T T F F T F F F T F F T F T F T T T

T F F

T T F

F T T

sono formule. In logica proposizionale si ha che se A`e una proposizione, allora Ae ¬Asono letterali, in

cui A `e letterale positivo, mentre¬A `e detto letterale negativo. Infine, si dice letterale complementare

¯

la proposizione

L definito come¬A se L= A, oppure A se L= ¬A.

Una volta introdotte le formule ben formate, `e possibile definire le sottoformule, ovvero una parte

di una fbf che `e a sua volta una fbf. L’insieme Stfm(F) delle sottoformule di F `e definito come il pi`u

piccolo insieme di formule tale che:

F ∈Stfm(F);

Se¬G∈Stfm(F), allora G∈Stfm(F);

se G∧H,G∨H,G⇒H,G⇔H ∈Stfm(F), allora H,G∈Stfm(F).

Semantica La semantica, invece, ha lo scopo di assegnare un significato alle formule appena definite,

tramite una funzione I, detta interpretazione, che mappa ogni proposizione ad un valore di verit`a (vero o

falso): formalmente, I : {fbf}→{0,1}. Tale funzione, quindi, non fa altro che assegnare il valore di vero

(1) o falso (0) alle lettere proposizionali costanti 1 e valuta il valore di verit`a di¬F,F ∧G,F ∨G,F ⇒

G,F ⇔G sulla base dei valori di verit`a delle proposizioni F e G.

Da qui, si introduce il simbolo ⊨, che si utilizza per associare formule ed interpretazioni. Dunque, la

scrittura I ⊨ F, che si legge I rende vera F, vale nei seguenti casi:

I ⊨ A se e solo se I(A) = T, con A proposizione;

I ⊨¬F se e solo se I ⊭ F;

I ⊨ F ∧G se e solo se I ⊨ F e I ⊨ G;

I ⊨ F ∨G se e solo se I ⊨ F o I ⊨ G;

I ⊨ F ⇒G se e solo se I ⊭ G o I ⊨ G;

I ⊨ F ⇔G se e solo se I ⊨ F ⇒G e I ⊨ G→F.

Dal concetto di interpretazione, si possono definire le seguenti propriet`a della semantica delle formule

proposizionali:

Se I ⊨ F, allora si dice che I `e un modello di F;

F si dice valida (o si dice essere una tautologia) se e solo se per ogni interpretazione I vale che

I ⊨ F;

F `e soddisfacibile se e solo se esiste un’interpretazione I tale che I ⊨ F;

F `e falsificabile se e solo se esiste un’interpretazione I tale che I ⊭ F;

F `e insoddisfacibile se e solo se per ogni interpretazione I vale che I ⊭ F;

F `e contingente se e solo se `e sia soddisfacibile che falsificabile;

Ogni formula del tipo F ∧¬F `e una contraddizione, indicata con ⊥;

Ogni formula del tipo F ∨¬F `e detta principio del terzo escluso, indicata con ⊤

1Le lettere proposizionali costanti sono T (o V ) per rappresentare una proposizione vera, oppure ⊥ (o F ) per

rappresentare una proposizione falsa6.1. LOGICA PROPOSIZIONALE 35

Un insieme di formule Fcomporta logicamente una formula G o, equivalentemente, una formula G`e

una conseguenza logica di un insieme di formule F, se ogni modello di F`e anche un modello di G e si

scrive con F⊨ G. Dopo aver stabilito una corrispondenza semantica fra due formule logiche, `e possibile

anche stabilire una relazione di equivalenza fra due formule logiche, relazione che vale solamente se la

corrispondenza fra le due formule `e biunivoca, ovvero se vale sia F ⊨ Gche G⊨ F: una tale relazione si

rappresenta con la scrittura F ≡G.

Esistono innumerevoli equivalenze notevoli:

F ∧F ≡F

F ∨F ≡F

F ∧G≡G∧F

F ∨G≡G∨F

F ∧(G∧H) ≡(F ∧G) ∧H

F ∨(G∨H) ≡(F ∨G) ∨H

(F ∧G) ∨F ≡F

(F ∨G) ∧F ≡F

F ∧(G∨H) ≡(F ∧G) ∨(F ∧H)

F ∨(G∧H) ≡(F ∨G) ∧(F ∨H)

¬¬F ≡F

¬(F ∧G) ≡¬F ∧¬G

¬(F ∨G) ≡¬F ∧¬G

F ⇔G≡(F ⇒G) ∧(G⇒F)

F ⇒G≡¬F ∨G

F ⇒G≡¬G⇒¬F

In logica prposizionale `e anche possibile sostituire una sottoformula G di una formula ben formata F

con una formula H: la formula risultate viene indicata con la scrittura F[G\H]. Tale sostituzione, per`o,

pu`o avvenire solamente se G≡H.

In base a questi concetti si pu`o notare che non tutti i connettivi logici sono strettamente necessa-

ri, in quanto possono essere sostituiti con altri. A questo proposito, un insieme di connettivi `e detto

funzionalmente completo se e solo se qualunque formula proposizionale pu`o essere trasformata in una

formula semanticamente equivalente che contiene solamente i connettivi dell’insieme dato. Sfruttando

tali insiemi, detti minimali, e le equivalenze semantiche, `e possibile definire delle forme normali, che in-

troducono degli schemi sintattici per scrivere formule, che hanno completa generalit`a semantica, ovvero

permettono di formalizzare il significato di qualsiasi formula che si possa scrivere con la completa gene-

ralit`a sintattica della logica proposizionale. In altre parole, per ogni formula ben formata esistono una

o pi`u formule logicamente equivalenti ad essa scritte in una forma normale, utili per la maniplazione di

tali formule. Esistono tre principali forme normali per la logica proposizionale, chiamate forma negativa,

forma congiuntiva e forma disgiuntiva. Una formula `e in forma normale negativa se e solo se `e composta

solamente da letterali, congiunzioni e disgiunzioni; una formula `e in forma normale congiuntiva (detta

anche CNF) se e solo se ha la forma C1 ∧C2 ∧...∧Cn, dove Ci `e una disgiunzione di letterali; una formula

`e in forma normale disgiuntiva (detta anche DFN) se e solo se ha la forma D1 ∨D2 ∨...∨Dn, dove Di `e

una congiunzione di letterali.

A questo punto `e possibile completare la definizione della logica proposizionale attraverso i concetti

di assioma e regole di inferenza, che costituiscono un sistema formale assiomatico-deduttivo (in inglese

calculus). Questi elementi definiscono una relazione di derivabilit`a (relazione gi`a analizzata nel contesto

delle grammatiche), detta anche dimostrabilit`a, tra un insieme di formule Fe una formula G. Dunque,

i sistemi formali della logica hanno un compito molto simile a quello assolto dalle grammatiche, ovvero

producono meccanicamente una formula risultante a partire da un insieme iniziale di formule, applicando

assiomi e regole di inferenza. Si scrive, quindi, F⊢G se G pu`o essere ottenuto da F. Idealmente, la

relazione di derivabilit`a dovrebbe essere corretta (cio`e se F⊢Gallora F⊨ G) e completa (cio`e se F⊨ G

allora F ⊢G). Se una formula F pu`o essere derivata in una teoria Fusando solamente assiomi e regole

di inferenza di un sistema, allora si dice che F `e un teorema.36 CAPITOLO 6. LOGICA

6.2 Logica del Primo Ordine

La logica proposizionale appena analizzata ha molte applicazioni, ma il suo potere espressivo `e ristretto.

Per questo motivo, nel 1979 `e stata sviluppata la logica del primo ordine, che permette dal punto di vista

ontologico di considerare non solo fatti (come avveniva nella logica proposizionale), ma anche propriet`a,

relazioni e funzioni.

Sintassi In modo formale:

Definizione 6.2.1. La logica del primo ordine `e composta da un linguaggio L, il cui alfabeto `e costituito

dai seguenti elementi:

1. Un insieme numerabile infinito di variabili;

2. Un insieme di simboli di funzione;

3. Un insieme di simboli di predicati (o relazioni);

4. Un insieme di connettivi logici:¬(NOT), ∧(AND), ∨(OR), ⇒(Implicazione) e ⇔(Coimplicazione);

5. Un insieme di quantificatori: ∃(Esiste) e ∀(Per ogni);

6. Un insieme di simboli di punteggiatura: ( , ) e le virgole.

Ogni simbolo di funzione e relazione ha una ariet`a fissata, che indica il numero di argomenti associati

a quella determinata funzione. Le funzioni nullarie sono dette costanti, mentre i predicati costanti

sono detti proposizioni. I simboli dell’alfabeto sono privi di significato: assegnarne uno `e compito della

semantica.

Per poter scrivere formule nella logica del primo ordine c’`e la necessit`a di denotare tutti gli oggetti

di cui il linguaggio Lpu`o parlare, detti termini. Tale denotazione avviene induttivamente come segue:

ogni variabile `e un termine della formula;

se f `e un simbolo di funzione n-aria e t1,t2,...,tn sono termini, allora f(t1,t2,...,tn) `e un termine.

Gli oggetti appena denotati attraverso i termini, si possono utilizzare all’interno delle formule della

logica del primo ordine, definite anch’esse in maniera induttiva. L’insieme delle formule della logica del

primo ordine `e definito come il pi`u piccolo insieme tale che:

Se p`e un simbolo di relazione n-aria e t1,t2,...,tn sono termini, allora p(t1,t2,...,tn) `e una formula

detta atomica o semplicemente atomo;

Se F e G sono formule e X `e una variabile, allora¬F,F ∨G,F ∧G,F ⇒G,F ⇔G,∃XF,∀XF

sono formule.

Nella scrittura di formule appartenenti alla logica del primo ordine, c’`e un’osservazione da fare:

quando si utilizza il quantificatore ∀il connettivo principale utilizzato `e ⇒, mentre nel caso si utilizzi

il quantificatore ∃allora il connettivo principale `e ∧. Inoltre, se QX(F) rappresenta una formula in

cui Q `e un quantificatre, allora F si dice ambito di Q e che Q `e applicato ad F. Un’occorrenza di una

variabile in una formula `e legata se e solo se la sua occorrenza `e entro l’ambito di un quantificatore che

impiega quella variabile, altrimenti `e libera. Una formula `e chiusa se e solo se non contiene occorrenze

libere di variabili. Le formule chiuse sono quelle per le quali, data un’interpretazione I, si pu`o calcolare

la veridicit`a.

Semantica Come per il caso della logica proposizionale, anche la logica del primo ordine ha una

semantica basata sul concetto di interpretazione: un’interpretazione I di un alfabeto A `e un dominio

non vuoto D (indicato anche con |I|) e una funzione che che associa ogni costante c ∈A a un oggetto

cI ∈D, ogni simbolo n-ario di funzione f ∈A a una funzione fI : Dn →D e ogni simbolo n-ario di

predicato p∈Aa una relazione pI ⊆D×D×...×Dnvolte. Prima di poter assegnare un significato alle

fromule, va definito il significato di ogni termine, indicato con ϕI(t) con til termine a cui dare singificato

nell’interpretazione I.6.2. LOGICA DEL PRIMO ORDINE 37

ϕ`e induttivamente definito nel seguente modo:

1. cI se t`e una costante c;

2. ϕ(X) se t`e una variabile X;

3. fI(ϕI(t1),...,ϕI(tn)) se t`e nella forma f(t1,...,tn).

Ora, sia ϕ una valutazione, X una variabile, I un’interpretazione e cI ∈|I|, allora ϕ[X →cI] `e una

valutazione identica a ϕ, eccetto per il fatto che mappa X in cI. Il significato di una formula, quindi,

`e un valore di verit`a che `e definito induttivamente. Dunque la scrittura I ⊨ϕ F, che si legge F `e vero

rispetto all’interpretazione I e al significato ϕ, vale nei seguenti casi:

I ⊨ϕ p(t1,...,tn) se e solo se <ϕI(t1),...,ϕI(tn) >∈pI;

I ⊨ϕ ¬F se e solo se I ⊭ϕ F;

I ⊨ϕ (F ∧G) se e solo se I ⊨ϕ F e I ⊨ϕ G;

I ⊨ϕ (F ∨G) se e solo se I ⊨ϕ F o I ⊨ϕ G;

I ⊨ϕ (F ⇒G) se e solo se I ⊭ϕ F o I ⊨ϕ G

I ⊨ϕ (F ⇔G) se e solo se I ⊨ϕ (F ⇒G) e I ⊨ϕ (G⇒F);

I ⊨ϕ ∀X(F) se e solo se I ⊨ϕ[X→cI ] F per ogni cI ∈|I|;

I ⊨ϕ ∃X(F) se e solo se I ⊨ϕ[X→cI ] F per qualche cI ∈|I|

Se F `e una formula chiusa, il suo significato dipende solamente dall’interpretazione I, che viene detta

modello per F (I ⊨ F) se e solo se per ogni valutazione ϕ si ha che I ⊨ϕ F. Inoltre, se F`e un insieme

di formule, un’interpretazione `e modello di Fse e solo se tale interpretazione `e modello per ogni F ∈F.

La relazione di conseguenza logica ⊨ tra insiemi di formule e formule pu`o essere estesa anche per la

logica del primo ordine, cos`ı come anche i concetti di validit`a, soddisfacibilit`a, falsificabilit`a, contingenza

e insoddisfacibilit`a, analizzati nello studio della logica proposizionale.

Come nel caso della logica proposizionale, esistono innumerevoli equivalenze notevoli:

∀X(F) ≡¬(∃X(¬F))

∃X(F) ≡¬(∀X(¬F))

∀X(F) ∧(∀X)G≡∀X(F ∧G)

∃X(F) ∨(∃X)G≡∃X(F ∨G)

(∀X)(∀Y)F ≡(∀Y)(∀X)F

(∃X)(∃Y)F ≡(∃Y)(∃X)F

(∀X(F)) ∧G≡∀X(F ∧G)∗

(∀X(F)) ∨G≡∀X(F ∨G)∗

(∃X(F)) ∧G≡∃X(F ∧G)∗

(∃X(F)) ∨G≡∃X(F ∨G)∗

Le equivalenze segnate con * sono valide solo se X non `e libera in G.38 CAPITOLO 6. LOGICA

6.3 Logica Monadica del Primo Ordine

In questa sezione si analizza un frammento della logica monadica del primo ordine, che permette di

descrivere certe stringhe su un determinato alfabeto I. La logica monadica, come suggerisce il nome, si

occupa solamente dei predicati monadici, ovvero di tutti quei predicati che hanno ariet`a pari ad uno.

Sintassi Una generica formula F appartenente alla logica monadica del primo ordine ha una sintassi

molto semplice, articolata nei seguenti casi:

a(x) con a∈I, ovvero un predicato unario per ogni simbolo dell’alfabeto I;

x<y, che costituisce l’unica eccezzione della logica monadica in quanto non `e un operatore unario,

ma binario;

¬F, operatore NOT;

F ∧F, operatore AND;

∀x(F), quantifcatore di una formula rispetto ad una variabile;

Il dominio delle variabili `e N.

Si pu`o osservare come, rispetto alla logica proposizionale e del primo ordine, la logica monadica non

fa uso della maggior parte degli operatori logici, del quantificatore esistenziale, della maggior parte degli

operatori matematici, di oggetti o funzioni. Tutti i costrutti non utilizzati da tale logica possono essere

drivati dagli operatori che sono stati presentati.

Le formule scritte in questa logica possono confrontare dei numeri rappresentati dalle variabili, che

rappresentano posizioni all’interno delle stringhe scritte sull’alfabeto di riferimento. Quindi con l’alfabeto

Idi riferimento posso scrivere delle stringhe mediante i predicati unari e, con la logica monadica `e possibile

calcolare la posizione, rappresentata dalle variabili, di determinati caratteri all’interno di tali stringhe

per poterli confrontare con altre posizioni.

Con gli operatori logici, matematici e i quantificatori utilizzati nella logica monadica del primo ordine,

come gi`a detto in precedenza, `e possibile derivare tutti gli altri operatori. Nello specifico:

F1 ∨F2 ≡¬(¬F1¬F2)

F1 ⇒F2 ≡¬F1 ∨F2

∃x(F) ≡¬∀x(¬F)

x= y≡¬(x<y) ∧¬(y<x)

x≤y≡¬(y<x)

In realt`a si possono anche introdurre alcune abbraviazioni di comodo. Le pi`u utilizzate sono:

x= 0 ≡∀y(¬(y<x))

successor(x,y) ≡x<y∧∃z(x<z∧z<y)

y= x+ 1 ≡successor(x,y)

y= x+ k(k>1) ≡∃z1,...,zk−1(y= zk−1 + 1 ∧...∧z1 = x+ 1)

y= x−1 ≡successor(y,x)

last(x) ≡¬∃y(y>x)

Le altre costanti (1, 2, 3, ...) possono essere ricavate tramite l’utilizzo del predicato successor (di

ariet`a due) applicata alla costante 0 tante volte quanto il numero che si vuole ottenere.

Una volta introdotti tutti questi concetti della logica monadica del primo ordine, si pu`o ora analizzare

l’interpretazione di queste formule logiche rispetto a stringhe di un determinato alfabeto di riferimento.

Dato un alfabeto I, una stringa w∈I+ ed un simbolo a∈I, a(x) `e vero se e solo se l’x-esimo simbolo

di w `e a, considerando un’indicizzazione che parte da 0.6.4. LOGICA MONADICA DEL SECONDO ORDINE 39

Semantica La semantica, nella logica monadica del primo ordine, assegna un valore di verit`a o falsit`a

alle formule, tramite una funzione di assegnamento v1 : V1 →[0,...,|w|−1], in cui w∈I+ `e una stringa

composta a partire dall’alfabeto I, mentre V1 `e l’insieme delle variabili. Tale funzione si comporta nel

seguente modo:

w,v1 ⊨ a(x) se e solo se w= uav e |u|= v1(x);

w,v1 ⊨ x<y se e solo se v1(x) <v1(y);

w,v1 ⊨¬F se e solo se w,v1 ⊭ F;

w,v1 ⊨ F1 ∧F2 se e solo se w,v1 ⊨ F1 e w,v1 ⊨ F2;

w,v1 ⊨ ∀x(F) se e solo se w,v′

1 ⊨ F ∀v′

1 con v′

1(y) = v1(y), y̸= x.

Propriet`a La logica monadica del primo ordine ha delle importanti propriet`a che consentono di identi-

ficare quali linguaggi `e possibile rappresentare con tale logica. Nello specifico, tutti i linguaggi esprimibili

mediante questa logica sono chiusti rispetto all’unione, all’intersezione e al complemento, Inoltre, si pu`o

dimostrare che non `e possibile esprimere il linguaggio Lp composto da tutte e sole le stringhe di lunghezza

pari con I= {a}: quindi, si pu`o osservare come la logica monadica del primo ordine `e strettamente meno

espressiva rispetto agli automi a stati finiti, il che significa che data una formula di tale logica, si pu`o

sempre costruire un FSA equivalente, ma non il contrario. Infine, i linguaggi definiti da questa logica

non sono chiusi rispetto alla stella di Kleene, ed `e per questo motivo che tali linguaggi sono anche detti

star-free, definibili tramite l’unione, l’intersezione, il complemento e la concatenazione di linguaggi finiti.

6.4 Logica Monadica del Secondo Ordine

Per riuscire ad ottenere lo stesso potere espressivo degli FSA `e necessario permettere alla logica del primo

ordine di quantificare sui predicati monadici, ovvero di poter quantificare anche su insiemi di posizioni.

Si ammettono quindi formule del tipo ∃X(F) oppure ∃X(x), in cui X `e detta essere una variabile del

secondo ordine, il cui dominio non `e pi`u l’insieme dei numeri naturali N, ma l’insieme dei predicati

monadici. Per convenzione si utilizzano le lettere maiuscole per indicare le variabili del secondo ordine e

lettere minuscole per le variabili del primo ordine.

Semantica L’assegnamento delle variabili del secondo ordine, che fanno parte dell’insiemeV2, avviene

attraverso la funzione v2 : V2 →℘([0,...,|w|−1]) tale che:

w,v1,v2 ⊨ X(x) se e solo se v1(x) ∈v2(X);

w,v1,v2 ⊨ ∃X(F) se e solo se w,v1,v′

2 ⊨ F per qualche v′

2(Y) = v2(Y), Y ̸= X

Tramite questa logica, si possono scrivere formule che risolvono il problema della rappresentazione

del linguaggio Lp, composto da tutte e sole le stringhe di lunghezza pari con I= {a}, che si pu`o indicare

nel seguente modo: ∃D(∀x(¬D(0) ∧(¬D(x) ⇔D(x+ 1)) ∧a(x) ∧(last(x) ⇒D(x)))), in cui D `e una

variabile del secondo ordine che indica le posizioni dispari.

Si pu`o dimostrare che, data una qualsiasi formula F appartenente alla logica monadica del secondo

ordine, `e possibile costruire un automa a stati finiti che accetta lo stesso linguaggio L definito da F

e, viceversa, dato un qualsiasi automa a stati finiti, `e possibile enunciare una formula che riconosce lo

stesso linguaggio. Di conseguenza, si pu`o affermare che la classe dei linguaggi definibili dalle formule

della logica monadica del secondo ordine coincide con i linguaggi regolari.40 CAPITOLO 6. LOGICA

Figura 6.1: Gerarchia dei linguaggi

6.5 Logica per la descrizione di Propriet`a

Quando si programma una funzione `e importante definire con precisione quale sia il suo funzionamen-

to, senza necessariamente descrivere come funzioni. A tal proposito si `e soliti scrivere le cosiddette

prcondizioni e postcondizioni:

Precondizione: indica le condizioni che devono valere prima che la funzione venga invocata;

Postcondizione: indica le condizioni che devono valere al termine dell’esecuzione del programma.

Dunque, il programma P deve essere tale per cui se la precondizione Pre vale prima dell’esecuzione

di tale programma, allora la post condizione Postdeve valere dopo l’esecuzione. Tali condizioni possono

essere espresse in linguaggi diversi, ma il pi`u comune `e la logica del primo ordine.Parte II

Algoritmi e Strutture Dati

41Capitolo 7

Complessit`a del Calcolo

Nei capitoli precedenti si `e dimostrato come esistano alcuni problemi che, pur essendo ben definiti,

non sono risolvibili algoritmicamente, per cui non esiste una TM in grado di risolvere quel determinato

problema. Un’altra difficolt`a da tenere in considerazione quando si manipolano i problemi,risiede nel

tempo di esecuzione, ovvero il tempo impiegato dal programma per fornire una soluzione: se non `e

possibile ottenere una soluzione in un tempo ragionevole, ovviamente, il problema diventa intrattabile,

nonostante sia teoricamente risolvibile.

Il concetto di intrattabilit`a `e strettamente correlato al concetto di complessit`a del calcolo: pi`u il

problema `e complesso e meno questo diventa trattabile. Informalmente, la complessit`a indica una misura

del prezzo da pagare per risolvere il problema. Le risorse che si utilizzano per la risoluzione di un problema

sono principalmente due: lo spazio, ovvero la memoria necessaria all’algoritmo, e il tempo richiesto per

produrre la soluzione. Si parler`a quindi di complessit`a spaziale e di complessit`a temporale.

Inoltre, la soluzione proposta per un dato problema occupa le risorse in due modi: esiste infatti

una componente costante, che non dipende quindi dai dati di ingresso, e una componente che invece

`e funzione della dimensione dei dati di ingresso (di pi`u complessa analisi, ma anche pi`u attinente alla

realt`a).

Si osservi inoltre che le due risorse, quella temporale e quella spaziale, seppur sembrino indipenden-

ti l’una dall’altra, sono in realt`a correlate: alla riduzione di utilizzo di una risorsa aumenta l’altra e

viceversa.

7.1 Analisi di complessit`a

La complessit`a del calcolo dipende dalla dimensione e, spesso, anche dai particolari valori assunti dai

dati in ingresso. Per questo motivo, si rende necessario effettuare un’analisi del caso pessimo, del caso

medio e del caso ottimo, in funzione della dimensione dei dati in ingresso. Pi`u formalmente, tali casi

rappresentano rispettivamente la scelta di ingressi per cui viene eseguito il massimo numero di istruzioni

nel programma, il comportamento del programma in relazione alla possibile distribuzione dei dati e la

scelta di input per cui viene eseguito il minor numero di istruzioni.

In generale, il caso ottimo non `e di particolare interesse e il caso medio richiede la conoscenza della

distribuzione dei dati in ingresso (non sempre nota). Il caso pessimo, invece, `e particolarmente interes-

sante in quanto fornisce i peggiori risultati ottenibili dall’algoritmo in termini di consumo di spazio o

tempo; si garantisce quindi che tutte le soluzioni proposte dall’algoritmo abbiano un dispendio di risorse

minore rispetto al caso pessimo, indipendentemente dalla tipologia degli ingressi. Dunque, se il caso

pessimo `e ritenuto accettabile, allora anche tutti gli altri casi lo sono.

Inoltre, a differenza di quanto analizzato per la risolvibilit`a dei problemi, la complessit`a non `e collegata

solo al problema che si vuole affrontare, ma dipende anche dell’algoritmo che si utilizza per risolverlo.

Nel capitolo sugli automi, `e stato pi`u volte affermato che le Macchine di Turing sono il formalismo

pi`u potente che si ha a disposizione per la risoluzione di prblemi, dunque, risulta ragionevole definire la

complessit`a temporale e spaziale impiegando un tale modello.

Definizione 7.1.1. Sia M una TM deterministica a k nastri e sia x ∈I∗. Sia c0 ⊢c1 ⊢.... ⊢cr una

computazione, ovvero una sequenza di transizioni di M tale che c0 =<q0,↑x,↑Z0, ...,↑Z0 > e

ci =<qi, xi↑yi, αi1 ↑βi1, ..., αik↑βik >, in cui cr `e una configurazione di arresto, se esiste. Allora, la

43`

44 CAPITOLO 7. COMPLESSIT

A DEL CALCOLO

funzione che rappresenta la complessit`a temporale TM di M `e definita nel seguente modo:

TM = if lacomputazioneterminathenrelse∞.

Informalmente, quindi, la complessit`a temporale viene definita come una funzione che fornisce il

numero esatto di passi richiesti da una TM per raggiungere la propria configurazione di arresto, se esiste,

a partire dalla configurazione iniziale, per una qualsiasi stringa in ingresso. analogamente, si pu`o definire

la complessit`a spaziale come una funzione che fornisce il numero massimo di celle del nastro utilizzate.

Definizione 7.1.2. Siano M, x, c0,...,cr definiti come nella definizione 7.1.1. La funzione che rappre-

senta la complessit`a spaziale SM di M `e definita nel seguente modo:

SM =

k

j=1

maxi∈{0,1,...,r}(|αij|)

Inoltre, vale che:

∀x,

SM

k ≤TM(x)

Si noti, inoltre, che la definizione di SM(x) prende in considerazione solamente i nastri di memoria e

ignora sia il nastro di ingresso che il nastro di uscita per il calcolo della complessit`a.

Secondo le definizioni 7.1.1 e 7.1.2, sia TM che SM sono funzioni definite su I∗, ma nella pratica la

complessit`a di una soluzione dipende sia dal contenuto dell’ingresso che dalla sua dimensione: a partire

da questa osservazione, si erano introdotti i concetti di complessit`a nel caso pessimo, medio e ottimo,

che si possono ridefinire nel seguente modo, alla luce delle definizioni appena date:

Definizione 7.1.3. Il caso pessimo, ottimo e medio sono cos`ı definiti:

Caso pessimo: TM(n) = max|x|=nTM(x);

Caso ottimo: TM(n) = min|x|=nTM(x);

Caso medio: TM(n) = |x|=nTM(x)

|I|n

Una volta analizzata la complessit`a temporale tramite il formalismo delle macchine di Turing, si

sposta l’attenzione sugli altri formalismi analizzati nel capitolo riguardante gli automi, in particolare

sugli automi a stati finiti, sugli automi a pila e sulle macchine di turine a singolo nastro.

Dato un automa a stati finiti A, si definisce la complessit`a temporale TA come l’intero i tale che

δi(q0,x) = q per qualche q, se esiste, ovvero il numero di transizioni effettuate per per processare la

stringa in ingresso x a partire dallo stato iniziale. Se δ∗(q0,x) `e indefinita, si pone TA = |x|, ovvero

pari alla lunghezza della stringa in ingresso. TA, evidentemente, indica il numero di mosse compiute

da A durante il riconoscimento della stringa x. Dunque, per ogni automa a stati finiti la complessit`a

temporale TA cresce in maniera lineare con il crescere della lunghezza della stringa. Al contrario, la sua

complessit`a spaziale SA non varia mai, in quanto gli FSA sono composti da un numero finito di stati

definiti a priori, indipendentemente dalla lunghezza della stringa letta.

Dato un automa a pila A, si pu`o analizzare sia la complessit`a temporale in funzione della stringa in

ingresso (TA(x)), sia in funzione della lunghezza della stringa (TA(n)). Come per gli automi a stati finiti,

quando si calcola la complessit`a temporale in funzione della stringa in ingresso, si contano il numero di

passi che portano da una configurazione iniziale ad una configurazione finale. Quando invece si vuole

utilizzare come parametro la lunghezza della stringa, la complessit`a temporale `e calcolata come il massimo

di tutte le complessit`a temporali in funzione delle stringhe in ingresso della lunghezza considerata. La

complessit`a spaziale SA, invece, viene associata al numero di celle di memoria della pila che vengono

occupate dall’automa per portare a termine la computazione.

La complessit`a temporale e spaziale per le macchine di Turing a nastro singolo sono definite esat-

tamente come per le TM a k-nastri. Data una macchina di Turing M a singolo nastro, la complessit`a

spaziale SM(x), che corrisponde al massimo numero di celle del nastro di memoria occupate da M du-

rante la computazione a fronte della stringa in ingresso x, non pu`o mai essere minore di |x|, in quanto

l’unico nastro presente in M `e sia di ingresso, che di memoria, che di uscita. Ci`o significa che l’unico7.2. COMPORTAMENTO ASINTOTICO 45

nastro presente, di cui si deve analizzare l’occupazione, `e precaricato con la stringa di ingresso x. Per

quanto riguarda la complessit`a spaziale, le TM a singolo nastro sono meno efficienti delle TM multinastro

e, in alcuni casi, di altri formalismi analizzati.

In generale, le macchine di Turing multinastro sono il formalismo pi`u potente ed efficiente per la

computazione di problemi.

7.2 Comportamento asintotico

Nella maggior parte dei casi si analizza la complessit`a spaziale o temporale di un determinato algoritmo

per valori molto grandi dell’ingresso x, ovvero per x che tende ad infinito. In questi casi si analizza il

comportamento asintotico dell’algoritmo, che fornisce un’approssimazione abbastanza precisa sul dispen-

dio di risorse. La notazione dell’ordine di grandezza di una funzione, nota sotto il nome di notazione

theta-grande (Θ), sottolinea i fattori dominanti che influeanzano la creascita della sua complessit`a in

funzione della dimensione dell’ingresso. Oltre alla notazione theta-grande, esistono anche le notazioni

o-grande (O) e omega-grande (Ω), le cui definizioni sono riportate di seguito:

Definizione 7.2.1 (Notazione O). Siano g : N →R+ ed f : N →R+ due funzioni. La funzione g `e

in O(f) se e solo se esistono due numeri positivi c ed n0 tali che per ogni n ≥n0, g(n) ≤cf(n). Ci`o

significa che O(f) = {g(n) : N →R+ |∃c,n0 >0 ∧∀n≥n0,g(n) ≤cf(n)}

Inoltre, vale che:

f(n)

lim

n→∞

g(n) = 0 ⇒f(n) ∈O(g(n))

Definizione 7.2.2 (notazione Ω). Siano g : N →R+ ed f : N →R+ due funzioni. La funzione g `e

in Ω(f) se e solo se esistono due numeri positivi c ed n0 tali che per ogni n ≥n0, cf(n) ≤g(n). Ci`o

significa che Ω(f) = {g(n) : N →R+ |∃c,n0 >0 ∧∀n≥n0,cf(n) ≤g(n)}.

Inoltre, vale che:

f(n)

lim

n→∞

= ∞⇒f(n) ∈Ω(g(n))

g(n)

La notazione o-grande rappresenta quindi un limite superiore per la funzione data, mentre la no-

tazione theta-grande rappresenta un limite inferiore. Nello specifico `e di interesse pratico prendere in

considerazione il minimo limite superiore e il massimo limite inferiore.

Definizione 7.2.3 (notazione Θ). Siano g : N →R+ ed f : N →R+ due funzioni. La funzione g `e in

Θ(f) se e solo se esistono tre numeri positivi c1,c2 ed n0 tali che per ogni n ≥n0, c1f(n) ≤g(n) ≤

c2f(n). Ci`o significa che Θ(f) = {g: N →R+ |∃c1,c2,n0 >0 ∧n≥n0,c1f(n) ≤g(n) ≤c2f(n)}

Inoltre, vale che:

f(n)

lim

n→∞

= c>0 ⇒f(n) ∈Θ(g(n))

g(n)

Dalla definizione 7.2.3, si pu`o dedurre che la funzione f ∈Θ(g) se e solo se f ∈O(g) e f ∈Ω(g).

Inoltre, Le notazioni indicate precedentemente godono delle seguenti propriet`a:

Transitivit`a:

– se f(n) ∈Θ(g(n)) e g(n) ∈Θ(h(n), allora f(n) ∈Θ(h(n));

– se f(n) ∈O(g(n)) e g(n) ∈O(h(n), allora f(n) ∈O(h(n));

– se f(n) ∈Ω(g(n)) e g(n) ∈Ω(h(n), allora f(n) ∈Ω(h(n));

Riflessivit`a:

– f(n) ∈Θ(f(n));

– f(n) ∈O(f(n));

– f(n) ∈Ω(f(n));

Simmetria: f(n) ∈Θ(g(n)) ⇐⇒ g(n) ∈Θ(f(n));

Simmetria trasposta: f(n) ∈O(g(n)) ⇐⇒ g(n) ∈Ω(f(n)).

Inoltre, la relazione Θ `e una relazione di equivalenza.`

46 CAPITOLO 7. COMPLESSIT

A DEL CALCOLO

7.3 Accelerazione Lineare

Si `e precedentemente affermato che la complessit`a della soluzione di un determinato problema pu`o essere

migliorata mediante opportune modifiche all’algoritmo risolutivo. A tal proposito si enunciano i seguenti

teoremi che pongono alcuni limiti al miglioramento degli algoritmi:

Teorema 7.3.1. Dato L un linguaggio accettato da una TM M multinastro (deterministica o meno) di

complessit`a spaziale SM(n), allora, per ogni costante c∈R+, L `e accettato anche da un’opportuna TM

M’ tale che SM′(n) <c·SM(n).

Teorema 7.3.2. Dato L un linguaggio accettato da una TM M multinastro (deterministica o meno) di

complessit`a spaziale SM(n), allora L `e accettato anche da un’opportuna TM M’ multinastro con k = 1

con la medesima complessit`a spaziale, concatenando i contenuti dei k nastri di M.

Teorema 7.3.3. Dato L un linguaggio accettato da una TM M multinastro (deterministica o meno) di

complessit`a spaziale SM(n), allora, per ogni costante c∈R+, L `e accettato anche da un’opportuna TM

M’ multinastro con k= 1 tale che SM′(n) <c·SM(n).

In generale, per la complessit`a temporale non si hanno risultati simili, ma `e possibile formulare alcuni

teoremi:

Teorema 7.3.4. Dato L un linguaggio accettato da una TM M multinastro (deterministica o meno) di

complessit`a temporale TM(n), allora, per ogni costante c∈R+, L `e accettato anche da un’opportuna TM

M’ con k+1 nastri tale che TM′(n) = max{n+ 1,c·TM(n)}.

I teoremi qui introdotti valgono anche per le moderne macchine di Von Neumann, in quanto possiamo

avere speedup lineari arbitrariamente grandi (ovviamente, entro i limiti fisici della termodinamica),

aumentando il parallelismo, ma miglioramenti pi`u che lineari si possono ottenere solamente modificando

l’algoritmo impiegato.

7.4 Macchina RAM

La macchina RAM (o Random Access Memory) `e un modello classico ispirata all`aarchitettura di Von

Neumann. Tale macchina `e costituita da un nastro in ingresso, un nastro in uscita, un programma

rappresentato da un numero finito di istruzioni, un contatore che indica l’istruzione corrente da eseguire

e una memoria ad accesso diretto.

Sia i nastri che la memoria sono composti da un numero illimitato di celle, ma al contrario dei nastri

di ingresso e uscita che si possono accedere in maniera sequenziale, la memoria `e indirizzata e si pu`o

accedere a una sua cella attraverso un numero intero i>0 che indica l’indirizzo di tale cella di memoria.

La cella 0 della memoria `e un registro speciale, detto accumulatore, che si utilizza per contenere il valore7.4. MACCHINA RAM 47

ISTRUZIONE Tabella 7.1: istruzioni macchina RAM

SEMANTICA

LOAD= x LOAD x LOAD* x STORE x STORE* x ADD= x ADD x ADD* x SUB= x SUB x SUB* x MULT= x MULT x MULT* x DIV= x DIV x DIV* x READ x READ* x WRITE= x WRITE x WRITE* x JUMP label JGZ label JLZ label JZ label HALT M[0] ←x

M[0] ←M[x]

M[0] ←M[M[x]]

M[x] ←M[0]

M[M[x]] ←M[0]

M[0] ←M[0] + x

M[0] ←M[0]+ M[x]

M[0] ←M[0] + M[M[x]]

M[0] ←M[0] - x

M[0] ←M[0] - M[x]

M[0] ←M[0] - M[M[x]]

M[0] ←M[0] * x

M[0] ←M[0] * M[x]

M[0] ←M[0] * M[M[0]]

M[0] ←M[0] \x

M[0] ←M[0] \M[x]

M[0] ←M[0] \M[M[x]]

M[x] ←input

M[M[x]] ←input

stampa x

stampa M[x]

stampa M[M[x]]

PC ←label

PC ←label if M[0] > 0

PC ←label if M[0] < 0

PC ←label if M[0] = 0

terminazione

di uno dei due operandi delle operazioni aritmetiche binarie che la macchina pu`o effettuare. Un generico

porgramma eseguibile dalla macchina RAM `e composto da istruzioni riportate nella tabella di seguito:

Una volta introdotte tutte le istruzioni eseguibili dalla macchina RAM, `e possibile ora studiarne la

complessit`a temporale, come fatto per le TM a k-nastri. A differenza delle TM, nelle macchine RAM

l’esecuzione delle diverse operazioni dipende dagli operandi necessari per eseguire tale operazione. Di-

venta quindi necessario analizzare tutte le istruzioni e definire il tempo richiesto per ciascuna di esse e

la quantit`a di memoria allocata. Queste quantit`a possono essere calcolate secondo due criteri, ovvero

tramite il criterio del costo costante e tramite il criterio del costo logaritmico. Il primo si basa sull’as-

sunzione che l’esecuzione di ciascuna istruzione richieda un’unit`a di tempo e che ciascuna allocazione in

memoria richieda un’unit`a di spazio (stessa assunzione fatta per le TM).

Si `e appena affermato per`o che nella macchina RAM le istruzioni hanno diversa natura e manipolano

dati di diversa dimensione: risulta, dunque, evidente che tale criterio `e poco affine alla realt`a. Per

tener conto della differente velocit`a di esecuzione e della differente quantit`a di memoria allocata da

ciascuna istruzione, si introduce il secondo criterio (del costo logaritmico), basato sulla supposizione che

il tempo richiesto per eseguire un’istruzione sia proporzionale alla lunghezza degli operandi dell’istruzione

considerata. Poich`e gli operandi sono rappresentati in memoria in codice binario, un generico operando

di valore v `e rappresentato da ⌊log2(|v|+ 1)⌋.

Dunque, `e possibile definire la funzione l(i) = if i̸= 0 then⌊log2(|v|+1)⌋else1 tramite cui calcolare

la complessit`a temporale logaritmica di ciascuna istruzione precedentemente analizzata nella tabella 7.4.

Alla stessa maniera, `e possibile calcolare i costi relativi allo spazio, introducendo la variabile m definita

come l’indirizzo pi`u alto della cella di memoria a cui si fa accesso durante l’esecuzione del programma, e

la variabile Mi che rappresenta il valore assoluto pi`u grande immagazzianto in M[i] durante l’esecuzione.

La complessit`a spaziale logaritmica si definisce quindi con la seguente formula:

m

l(Mi)

i=0

Di seguito sono riportati i costi logaritmici delle istruzioni RAM:`

48 CAPITOLO 7. COMPLESSIT

A DEL CALCOLO

Tabella 7.2: costi logaritmici delle istruzioni macchina RAM

ISTRUZIONE COSTO LOGARITMICO

LOAD= x LOAD x LOAD* x STORE x STORE* x ADD= x ADD x ADD* x READ x READ* x WRITE= x WRITE x WRITE* x JUMP label 1

JGZ label JLZ label JZ label HALT 1

l(x)

l(x) + l(M[x])

l(x) + l(M[x]) + l(M[M[x]])

l(M[0]) + l(x)

l(M[0]) + l(x) + l(M[x])

l(M[0]) + l(x)

l(M[0]) + l(x) + l(M[x])

l(M[0]) + l(x) + l(M[x]) + l(M[M[x]])

SUB, MULT, DIV definite come ADD.

l(input) + l(x)

l(input) + l(x) + l(M[x])

l(x)

l(x) + l(M[x])

l(x) + l(M[x]) + l(M[M[x]])

l(M[0])

l(M[0])

l(M[0])

Dunque, il criterio del costo costante si pu`o applicare solo in situazioni in cui si prevede che ogni valore

che comparir`a durante l’esecuzione del programma occupi esattamente una cella di memoria, altrimenti

si deve necessariamente applicare il criterio del costo logaritmico, che porta ad un calcolo pi`u preciso

della complessit`a.

7.5 Correlazione temporale fra TM e RAM

Una volta analizzato il comportamento della macchina RAM, `e possibile studiarne la correlazione con le

TM. Nello specifico, `e possibile simulare una TM deterministica a knastri attraverso una macchina RAM,

nel seguente modo: innanzitutto, si considera la memoria della RAM come suddivisa in blocchi, tutti di

dimensione k, ad eccezione del blocco 0, che ha dimensione k+1, in quanto memorizza lo stato della TM

e le posizioni delle k testine. I successivi blocchi vengono impiegati per contenere i valori contenuti nelle

successive posizioni di ciascuno dei k nastri di memoria della TM. Dunque, il valore rappresentato nella

i-esima cella del j-esimo nastro della TM `e contenuto nella locazione c+ k·j+ iin cui c`e una costante

opportuna della memoria della macchina RAM. Inoltre, per accedere al valore presente sotto la testina

di lettura di un determinato nastro `e prima necessario eseguire un accesso diretto al blocco 0, per poter

trovare la posizione del nastro stesso. Poi, per eseguire la funzione di transizione δ(q,i,s1,...,sk) e la

funzione di uscita η(q,i,s1,...,sk), si richiedono un numero prefissato di accessi in memoria per ottenere

q,i,s1,...,sn, necessari per l’esecuzione di tali funzioni.

Tutto ci`o conduce al seguente teorema:

Teorema 7.5.1. Una TM multinastro con complessit`a temporale TM pu`o essere simulata da una mac-

china RAM con complessit`a temporale TR = Θ(TM), secondo il criterio di costo uniforme, oppure

TR = Θ(TM·log(TM)), secondo il criterio di costo logaritmico.

Ovviamente `e possibile anche simulare una macchina RAM tramite una macchina di Turing, ma tale

costruzione `e molto pi`u complessa e richiede un’analisi approfondita. Si enuncia quindi solo il seguente

teorema:

Teorema 7.5.2. Sia L il linguaggio riconosciuto da una macchina RAM di complessit`a temporale TR

secondo il criterio del costo logaritmico. Se il programma RAM non utilizza le istruzioni MULT e DIV,

allora L pu`o essere riconosciuto da un’opportuna TM multinastro, in un tempo TM = Θ(T2

R).

Si pu`o quindi osservare come il legame tra TM e TR sia di tipo polinomiale, implicazione molto

importante perch`e suggerisce quale sia la classe di problemi trattabili nella pratica.Capitolo 8

Algoritmi

In questo capitolo si analizzano a fondo i principali algoritmi di ordinamento e i relativi tempi di esecu-

zione. Nello specifico, si utilizzer`a come modello di riferimento la macchina RAM con un criterio di costo

costante, come analizzato nei capitoli precedenti. Prima di proseguire nella trattazione `e necessario dare

una definizione generale di algoritmo:

Definizione 8.0.1. Un algoritmo `e una procedura di calcolo ben definita che prende un certo valore, o un

insieme di valori, in input e genera un valore, o un insieme di valori, in output. Dunque, un algoritmo

`e una serie di passi computazionali che trasformano l’input in output.

Un algoritmo pu`o anche essere visto come uno strumento per la risoluzione di un problema compu-

tazionale ben definito: sotto questo sguardo, un algoritmo si definisce corretto se, per ogni istanza di

input, termina con l’output corretto. Se un algoritmo `e corretto, allora risolve quel determinato problema

computazionale. Esistono molti modi per poter specificare un determinato algoritmo: si pu`o utilizzare

la lingua italiana o inglese, ma anche un linguaggio di programmazione come C, C++, JAVA e Pascal,

o ancora tramite uno pseudocodice.

8.1 Pseudocodifica

La pseudocodifica pu`o avvenire in molti modi, ma nel seguito si utilizzerano le convenzioni qui riportate:

L’indentazione serve ad indicare la struttura a blocchi dello pesudocodice, in modo da comprendere

quali istruzioni appartengono, per esempio, ad un ciclo for, a un ciclo while o ad un if-else statement.

Non sono utilizzate le parentesi graffe o parole chiave come begin ed end in quanto appesantiscono

la sintassi;

I costrutti iterativi while, for, repeat-until e il costrutto condizionale if-else hanno interpreta-

zioni simili a quelle dei comuni linguaggi di programmazione. Il contatore del ciclo mantiene il suo

valore dopo la fine del ciclo, quindi il valore che ha provocato la terminazione del ciclo stesso. Inol-

tre, si utilizza la parola chiave to quando il ciclo for incrementa il valore del suo contatore ad ogni

iterazione, mentre si utilizza la parola chiave down to nel caso la variabile venga decrementata;

Le assegnazioni di un valore ad una certa variabile avviene con il simbolo :=, differente dall’opera-

tore=, che invece indica l’eguaglianza di due valori all’interno di un costrutto if;

Per identificare un elemento appartenente ad un array, si utilizza la notazione con le parentesi

quadre, al cui interno si indica l’indice dell’elemento a cui si vuole accedere: array[i]; Per indicare

un intervallo di valori all’interno dell’array si utilizza la seguente sintassi: array[i..j], con cui si

indica la sottomatrice composta dagli elementi compresi fra i e j;

I dati utilizzati sono tipicamente organizzati in oggetti, formati da attributi, a cui si accede tramite

la notazione punto: oggetto.prop. Le variabili che rappresentano un determinato oggetto sono

trattate come puntatori a tale oggetto. Un puntatore che non fa riferimento ad alcun oggetto `e

inizializzato con il valore NIL;

I parametri vengono passati ad una procedura per valore: la procedura chiamata riceve una sua

copia dei parametri e, quindi, se a una di queste variabili `e assegnato un nuovo valore, la modifica

4950 CAPITOLO 8. ALGORITMI

non `e visibile dalla procedura chiamante. Nel caso venga passato come argomento un oggetto,

viene copiato il puntatore a tale oggetto e quindi le modifiche sono visibili anche dalla procedura

chiamante;

L’istruzione return restituisce immediatamente il controllo al punto in cui la procedura chiamante

ha effettuato la chiamata. Le istruzioni return possono anche ritornare un valore al chiamante;

Gli operatori booleani and e or sono cortocircuitati. Ci`o significa che nella valutazione dell’espres-

sione x and y, si valuta prima se il valore di x sia falso, in quanto, se lo fosse, l’intera espressione

sarebbe falsa e non avrebbe quindi alcun senso valutare il valore della variabile y. Al contrario,

nella valutazione dell’espressione x or y, si verifica innanzitutto se il valore di x sia vero, in quan-

to, se lo fosse, l’intera espressione sarebbe vera e non avrebbe quindi alcun senso valutare il valore

della variabile y.

Tramite queste regole `e possibile definire un generico algoritmo.

8.2 Insertion Sort

Una classe di algoritmi molto studiati `e quella riguardante l’ordinamento di un vettore, che consiste nella

disposizione dei suoi elementi in ordine crescente.

Il primo algoritmo analizzato `e l’insertion sort, che prende in input una sequenza di n numeri

[a1,a2,...,an] e restituisce in output una permutazione [a′

1,a′

2,...,a′

n] tale che a′

1 ≤a′

2 ≤...≤a′

n. Questo

algoritmo ordina sul posto 1 gli elementi assumendo che la sequenza da ordinare sia inizialmente partizio-

nata in una sottosequenza gi`a ordinata, all’inizio composta da un unico elemento (il primo dell’array), e

una sottosequenza ancora da ordinare. Ad ogni iterazione viene rimosso un elemento dalla sottosequenza

non ordinata e inserita nella posizione corretta all’interno della sottosequenza gi`a ordinata.

In pseudocodice:

1 i n s e r t i o n S o r t ( A ) :

2 f o r j := 2 to A . length :

3 key := A [ j ]

4 i := j - 1

5 w h i l e i > 0 and A [ i ] > key :

6 A [ i + 1] := A [ i ]

7 i := i - 1

8 A [ i + 1] = key

All’inizio di ogni iterazione del ciclo for, il cui indice `e j, la sottosequenza di elementi A[1..j-1]

`e la parte ordinata dell’array, mentre la sottosequenza A[j+1..n] `e costituita da elementi ancora da

ordinare.

Si analizza ora il tempo di esecuzione della procedura insertion sort: per ogni j = 2,3,...,nin cui

n = A.length, si indica con tj il numero di volte che il test del ciclo while nella riga 5 viene eseguito

per quel determinato valore di j.

Codice Costo Numero di volte

for j:= 2 to A.length c1 n

key := A[j] c2 n−1

i := j - 1 c3 n−1

while i > 0 and A[i] > key c4

n

j=2 tj

A[i + 1] := A[i] c5

n

j=2 (tj−1)

i := i - 1 c6

n

j=2 (tj−1)

A[i + 1] := key c7 n−1

Ad ogni riga di codice viene associato un costo ci che va moltiplicato per il numero di volte che tale

riga viene eseguita. Il tempo totale di esecuzione si calcola, dunque, sommando i vari contributi di tempo

di ogni riga, ottenendo cos`ı l’espressione di T(n):

1L’algoritmo risistema gli elementi della sequenza all’interno dell’array avendo, in ogni istante, al pi`u un numero finito

di elementi memorizzati all’esterno dell’array: ci`o permette di risparmiare memoria nel calcolatore.8.3. MERGE SORT 51

T(n) = c1n+ c2(n−1) + c3(n−1) + c4

n

j=2

tj + c5

n

(tj−1) + c6

j=2

n

(tj−1) + c7(n−1)

j=2

Ovviamente, il caso migliore si verifica quando l’array in input `e gi`a ordinato. In questo caso,

tj = 1 ∀j = 2,3...,n e l’espressione di T(n) assume la forma:

T(n) = (c1 + c2 + c3 + c4 + c7)n−(c2 + c3 + c4 + c7)

che `e funzione lineare di n. Dunque, T(n) = Θ(n).

Al contrario, il caso pessimo si verifica quando l’array in input `e ordinato, ma in ordine decrescente.

In questo caso tj= j ∀j = 2,3...,n e l’espressione di T(n) assume la forma:

T(n) = 1

2(c4 + c5 + c6)n2 + (c1 + c2 + c3)n+

che `e funzione quadratica di n. Dunque, T(n) = Θ(n2).

1

2(c4−c5−c6 + c8)n−(c2 + c3 + c4 + c7)

8.3 Merge Sort

L’algoritmo appena analizzato utilizza un approccio di tipo incrementale: dopo aver ordinato il sottoarray

A[1..j-1] inserisce l’elemento A[j] nella posizione corretta, ottenendo il sottoarray ordinato A[1..j].

Nel seguito, invece, si analizza un secondo approccio, pi`u efficiente del primo, soprattutto per array

di molti elementi: Divide et Impera. Questo criterio si basa sulla suddivisione ricorsiva del problema

in sottoproblemi pi`u piccoli, simili a quello originario, ma di dimensione ridotta, per poi risolvere i

sottoproblemi di dimensione minima e fondere i risultati ottenuti, per costruire una soluzione generale

del problema originario.

Il paradigma Divide et Impera, si basa in realt`a su tre passaggi:

1. Divide: il problema viene suddiviso in un certo numero di sottoproblemi, che sono istanze pi`u

piccole del problema originario, fino ad ottenere sottoproblemi minimi, non pi`u divisibili;

2. Impera: i sottoproblemi di dimensione minima vengono risolti in maniera ricorsiva; se i problemi

hanno dimensione sufficientemente piccola vengono risolti direttamente;

3. Combina: le soluzioni dei sottoproblemi vengono combinate per generare la soluzione del problema

generale.

Un tipico algoritmo che segue questo metodo di risoluzione `e il merge sort, che suddivide l’array

originario a met`a e ordina ricorsivamente i due sottoarray ottenuti, chiamando s`e stesso fino ad ottenere

sequenze di dimensione uno, di per s`e gi`a ordinate. A questo punto, le sottosequenze vengono fuse in

modo da ottenere un array ordinato.

Quest’ultimo passaggio viene effettuato tramite una procedura ausiliaria merge(A,p,q,r), dove A`e

un array, e p,q,r sono tre indici dell’array tali che p≤q<r. La porcedura assume che le sottosequenze

A[p..q] e A[q+1..r] siano ordinate e, quindi, le fonde per formare un unico sottoarray ordinato che

sostituisce il sottoarray corrente A[p..r]. La procedura merge(A,p,q,r) impiega un tempo Θ(n) con

n = r−p+ 1 il numero di elementi da fondere. Ad ogni iterazione, la procedura merge confronta gli

elementi pi`u piccoli dei due sottoarray, inserendoli nel sottoarray ”successivo” fino a quando uno dei

due sottoarray `e vuoto: a quel punto, i restanti elementi del sottoarray rimanente vengono copiati per

completare l’array ”successivo”. Da un punto di vista computazionale, ogni iterazione della procedura

impiega un tempo costante, in quanto deve semplicemente confrontare i due elementi dei due sottoarray.

Poich`e tale procedura viene effettuata per un massimo di n volte, la funsione impiega un tempo Θ(n).

In pseudocodice:

1 merge (A , p , q , r ) :

2 n1 := q - p + 1

3 n2 := r - q

4 L := [1 .. n1 + 1]

5 R := [1 .. n2 + 1]52 CAPITOLO 8. ALGORITMI

10 11 12 13 14 15 16 17 18 19 20 6 f o r i := 1 to n1 :

7 L [ i ] := A [ p + i - 1]

8 f o r j := 1 to n2 :

9 R [ j ] := A [ q + j ]

L [n1 + 1] := ∞

L [n2 + 1] := ∞

i := 1

j := 1

f o r k := p to r :

i f L [ i ] <= R [ j ]:

A [ k ] := L [ i ]

i := i + 1

e l s e :

A [ k ] := R [ j ]

j := j + 1

In altri termini, le righe 2 e 3 inizializzano i valori di n1 ed n2, che rappresentano la lunghezza dei due

sottoarray A[p..q] e A[q+1..r]. Nelle due righe successive vengono creati i due sottoarray ausiliari L

(per Left) ed R (per Right), che contano n+ 1 elementi (per motivi che verranno chiariti a breve). Le

righe dalla 6 alla 9, inizializzano gli array appena creati con i valori contenuti rispettivamente nella prima

e nella seconda met`a dell’array A. Le righe 10 e 11 inizializzano l’ultimo (n+ 1 -esimo) elemento dei due

sottoarray L ed R, con un valore sentinella. Impostando tale valore ad ∞, si `e certi che non possa essere

il valore pi`u piccolo fra i due confrontati: in questo modo, una volta arrivati alla fine di uno dei due

sottoarray, gli elementi dell’altro vengono ricopiati nell’array ”successivo” in quanto necessariamente pi`u

piccoli di ∞. Le ultime righe (dalla 12 alla 20) implementano la logica del confronto e dell’insermento

dell’elemento correntemente pi`u piccolo nell’array A.

Una volta analizzata la procedura merge, si pu`o introdurre l’algoritmo di ordinamento mergeSort.

In pseudocodice:

1 mergeSort (A , p , r ) :

2 i f p < r :

3 q = ⌊ ( p + r ) / 2 ⌋

4 mergeSort (A , p , q )

5 mergeSort (A , q +1 , r )

6 merge (A , p , q , r )

L’algoritmo calcola, in riga 2, un indice q, che serve a suddividere l’array A in due sottoarray che

contengono rispettivamente ⌈n/2⌉elementi ed ⌊n/2⌋elementi, su cui richiama ricorsivamente s`e stessa.

Una volta suddiviso l’array A in sottoarray di dimensione minima, viene chiamata la procedura merge,

precedentemente analizzata.

Come si pu`o facilmente osservare, la procedura mergeSort `e definita in maniera ricorsiva, quindi

l’analisi delle prestazioni temporali diventa leggermente pi`u complessa: infatti, si deve necessariamente

far uso di un’equazione di ricorrenza, che esprime il tempo di esecuzione totale di un problema di

dimensione n, in funzione del tempo di esecuzione per input pi`u piccoli. Se la dimensione del problema

diventa sufficientemente piccola, per esempio n≤c per qualche costante c, la soluzione del problema `e

diretta e richiede un tempo di esecuzione costante, indicata con Θ(1). Si suppone, inoltre, che il problema

originario venga suddiviso in a sottoproblemi, tutti di dimensione 1/b volte la dimensione del problema

originario. Dunque, `e necessario un tempo T(n/b) per risolvere un sottoproblema di dimensione n/b e

un tempo aT(n/b) per risolverli tutti. Infine, se si impiega un tempo D(n) per suddividere il problema

in a sottoproblemi e un tempo C(n) per fonderne le soluzioni, si ottiene la ricorrenza:

T(n) = Θ(1) if n≤c

aT(n/b) + D(n) + C(n) else

Per trovare ora il tempo di esecuzione T(n) nel caso peggiore si pu`o ragionare come segue. Nel caso in

cui i sottoarray abbiano cardinalit`a uno, la soluzione `e diretta, quindi viene impiegato un tempo costante

per risolvere il problema, mentre se i sottoarray hanno n>1 elementi, si suddivide il tempo di esecuzione

impostando D(n) = Θ(1), in quanto si impiega un tempo costante per calcolare il centro di un array,8.4. RISOLUZIONE RICORRENZE 53

C(n) = Θ(n), in quanto si `e gi`a precedentemente dimostrato che la procedura merge impieghi un tempo

lineare per la fusione delle soluzioni, e infine si pone a= b= 2, in quanto si suddivide ricorsivamente il

problema in due sottoproblemi di uguale dimensione 2. Con questo ragionamento, la ricorrenza assume

l’espressione:

T(n) = Θ(1) if n= 1

2T(n/2) + Θ(n) + Θ(1) if n>1

Si pu`o facilmente dimostrare (analiticamente oppure tramite il teorema dell’espreto, di cui si discuter`a

successivamente) che tale equazione ha soluzione T(n) = Θ(nlog2 n), che rappresenta il tempo di esecu-

zione dell’algoritmo mergeSort nel caso pessimo. Si pu`o osservare come tale algoritmo sia decisamente

migliore rispetto all’insertionSort, il cui tempo di esecuzione nel caso passimo `e Θ(n2).

Un modo per comprendere meglio come mai la complessit`a temporale del mergeSort sia proprio

Θ(nlog2 n), si riscrive la ricorrenza nel seguente modo:

T(n) = c if n= 1

2T(n/2) + cn+ c if n>1

in cui la costante c rappresenta sia il tempo richiesto per risolvere i problemi di dimensione 1, sia il

tempo per elemento dell’array dei passi divide e combina. Si pu`o costruire un albero di ricorsione, in cui

ogni ramo rappresenti una met`a dell’array precedente e ogni foglia sia un array di dimensione unitaria.

Il primo livello (in alto) ha un costo totale di cn, il secondo livello ha un costo totale di cn/2+cn/2 = cn

e cos`ı via fino all’ultimo livello, con costo totale di n+ n+...+ n (c volte), quindi di cn. In generale, il

livello iha 2i nodi, ciascuno dei quali ha un costo di c(n/2i), quindi, il numero totale di livelli dell’albero

di ricorsione `e log2 n+ 1, con n la dimensione dell’input. Dunque, per calcolare il costo totale, basta

sommare i costi di tutti i livelli, ottenendo cn(log2 n+ 1) = cn(log2 n) + cn, ovvero Θ(nlog2 n).

8.4 Risoluzione Ricorrenze

Come gi`a detto in precedenza, quando i problemi sono abbastanza grandi da essere risolti ricorsivamente,

si ha il cosiddetto caso ricorsivo, tramite cui si divide il problema in problemi pi`u piccoli di uguale natura.

Una volta che i sottoproblemi diventano sufficientemente piccoli da non richiedere pi`u il passo ricorsivo,

si `e raggiunto il cosiddetto caso base, da cui inizia la soluzione del problema.

Questo modello di risoluzione del problema viene anche detto Divide et Impera e richiede l’utilizzo

di equazioni di ricorrenza, tramite cui si caratterizzano i tempi di esecuzione degli algoritmi in termini

dei loro valori con input pi`u piccoli. Per risolvere tali equazioni, ovvero per trovare i limiti asintotici Θ

oppure O, esistono tre metodi:

1. Metodo di Sostituzione: si fa un’ipotesi di soluzione e si utilizza l’induzione matematica per

dimostrare che l’ipotesi sia corretta;

2. Metodo dell’Albero di ricorsione: si converte la ricorrenza in una struttura ad albero, i cui nodi

rappresentano i costi ai vari livelli della ricorsione;

3. Metodo dell’Esperto (Master theorem): fornisce i limiti per ricorrenze nella forma

T(n) = aT(n/b) + f(n) con a≥1,b>1 e f(n) data. Una ricorrenza in questa forma caratterizza

un algoritmo divide et impera che crea a sottoproblemi di dimensione 1/b, i cui passi divide e

combina richiedono un tempo f(n).

A volte, le ricorrenze non saranno delle uguaglianze, ma delle disuguaglianze nella forma T(n) ≤...,

che stabilisce un limite superiore su T(n) (quindi si utilizza la notazione Oanzich`e Θ), oppure nella forma

T(n) ≥..., che stabilisce invece un limite inferiore su T(n) (quindi si utilizza la notazione Ω anzich`e Θ).

Inoltre, ci sono casi in cui si trascurano dei dettagli tecnici di poca importanza, come le condizioni al

contorno: infatti, poich`e il tempo di esecuzione di un algoritmo con un input di dimensione costante

`e costante, le ricorrenze che ne derivano hanno T(n) = Θ(1), per valori sufficientemente piccoli di n.

Questa decisione risiede nel fatto che, sebbene le condizioni al contorno cambiano la soluzione esatta

2In realt`a, sarebbe pi`u accurato scrivere T (⌊n/2⌋)+T (⌈n/2⌉) in quanto non sempre la dimensione dell’array A `e potenza

di 2 e, dunque, divisibile ricorsivamente in due met`a. In questo caso `e pi`u agevole, anche nei calcoli, ipotizzare che

i sottoarray da suddividere abbiano un numero pari di elementi. Tale approssimazione, comunque, non influisce sulla

complessit`a finale del calcolo.54 CAPITOLO 8. ALGORITMI

della ricorrenza, tuttavia la soluzione non cambia per pi`u di un fattore costante e quindi asintoticamente

rimane immutata.

8.4.1 Metodo di Sostituzione

Uno dei metodi per la risoluzione delle occorrenze e, quindi, per il calcolo del tempo di esecuzione degli

algoritmi, `e il metodo della sostituzione, che richiede due passaggi:

1. Ipotizzare la forma della soluzione;

2. Utilizzare l’induzione matematica per dimostrare che la soluzione ipotizzata sia corretta.

Questo metodo pu`o essere applicato solamente se si ha un’idea della forma generale della soluzione e si

vuole calcolare il limite superiore o inferiore della ricorrenza che si analizza.

ESEMPIO: Si determini il limite superiore della ricorrenza T(n) = 2T(⌊n/2⌋) + n.

Si suppone che la soluzione sia O(nlog2 n). Il metodo di sostituzione consiste nel dimostrare che

T(n) ≤cnlog2 n per un generico c>0. Si verifica, innanzitutto, che questo limite sia valido anche per

⌊n/2⌋, ovvero che T(⌊n/2⌋) ≤c⌊n/2⌋log2(⌊n/2⌋). Facendo le opportune sostituzioni si ha:

T(n) ≤ 2(c⌊n/2⌋log2(⌊n/2⌋)) + n

≤ cnlog2(n/2) + n

= cnlog2 n−cnlog2 2 + n

= cnlog2 n−cn+ n

≤ cnlog2 n

L’ultimo passaggio `e vero solo per c≥1. A questo punto, l’induzione matematica richiede di dimostrare

che la soluzione vale per le condizioni al contorno. Si suppone, per esempio, che l’unica condizione al

contorno sia T(1) = 1: si deve dimostrare che `e possibile scegliere una costante csufficientemente grande

in modo che il limite T(n) ≤cnlog2 n sia valido anche per le condizioni al contorno. Quindi per n= 1

(condizione al contorno), il limite T(n) ≤cnlog2 n diventa T(1) ≤clog2 1 = 0, che per`o `e in contrasto

con T(1) = 1: il caso base della dimostrazione induttiva non `e valido!

Questo ostacolo nella dimostrazione pu`o essere facilmente superato sfruttando la notazione asinto-

tica, che richiede di provare che T(n) ≤cnlog2 n sia valida solamente dopo un certo n0 in poi, scelto

arbitrariamente: l’idea `e quella di escludere la condizione al contorno dalla dimostrazione induttiva. Si

osservi che, per n≥3, la ricorrenza non dipende direttamente da T(1), quindi si pu`o sostituire con T(2)

e T(3), impiegati come casi base della dimostrazione induttiva. Inoltre, ponendo n0 = 2, se T(1) = 1

allora T(2) = 4 e T(3) = 5. Basta quindi determinare una costante c tale per cui T(2) = 4 ≤2clog2(2)

e T(3) = 5 ≤3clog2(3): le precedenti condizioni sono soddisfatte solo per c≥2.

Non esiste un metodo unico e generale per indovinare la soluzione corretta di una ricorrenza, ma

`e possibile formulare delle buone ipotesi tramite il metodo dell’albero di ricorsione. Inoltre, se una

ricorrenza `e simile gi`a risolta in precedenza, allora `e possibile che anche la soluzione sia analoga. Un

altro metodo per formulare un’ipotesi di soluzione consiste nel dimostrare dei limiti superiori e inferiori

molto generali e larghi, per poi ridurre gradualmente il grado di incertezza, aumentando il limite inferiore

e diminuendo il limite superiore.

Ci sono poi casi in cui la soluzione ipotizzata sembra essere corretta, ma i calcoli matematici non

soddisfano il passo induttivo: solitamente, il problema risiede nel fatto che l’ipotesi induttiva non `e

abbastanza forte per dimostrare il limite esatto. In un caso del genere, spesso `e necessario semplicemente

correggere l’ipotesi sottraendo un termine di ordine inferiore per fare in modo che i calcoli soddisfino i

requisiti.

ESEMPIO: Si calcoli la ricorrenza T(n) = T(⌊n/2⌋) + T(⌈n/2⌉) + 1 supponendo che la soluzione sia

T(n) = O(n). Si deve quindi dimostrare che T(n) ≤cn per qualche c arbitraria. Sostituendo l’ipotesi

all’interno della ricorrenza si ottiene:

T(n) ≤ c⌊n/2⌋+ c⌈n/2⌉+ 1

= cn+ 1

che non implica che T(n) ≤cn per qualunque valore di c. Sembrerebbe quindi che l’ipotesi fatta sia

sbagliata, ma al contrario si pu`o dimostrare che `e corretta, formulando un’ipotesi induttiva pi`u forte. Per8.4. RISOLUZIONE RICORRENZE 55

affrontare tale problema, si sottrae un termine di ordine inferiore dalla precedente ipotesi, ad esempio,

un termine costante d≥0, ottenendo come nuova ipotesi T(n) ≤cn−d, che sostituita alla ricorrenza:

T(n) ≤ (c⌊n/2⌋−d) + (c⌈n/2⌉−d) + 1

= cn−2d+ 1

≤ cn−d

che diventa valida per ogni d≥1. Come prima, la costante c deve essere scelta arbitrariamente grande

affinch`e siano soddisfatte le condizioni al contorno.

Infine, ci sono casi in cui tramite una piccola manipolazione algebrica `e possibile rendere una ricor-

renza ignota simile ad una pi`u familiare.

ESEMPIO: Si calcoli la ricorrenza T(n) = 2T(⌊√n⌋) + log2(n). Tale ricorrenza sembra molto com-

plessa da risolvere, ma `e possibile semplificarla ponendo m= log2n, ottenendo cos`ı

T(2m) = 2T(2m/2) + m. Chiamando S(m) la ricorrenza appena ottenuta, `e possibile scrivere S(m) =

2S(m/2) + m, simile alla precedente ricorrenza analizzata T(n) = 2T(⌊n/2⌋) + n; in effetti, la soluzione

della ricorrenza S(m) `e la stessa ottenuta in precedenza. Dunque, la soluzione `e S(m) = mlog2 m e,

ripristinando i termini con la sostituzione m= log2n, si ottiene che T(n) = O(log2n·log2(log2n)).

8.4.2 Metodo dell’Albero di Ricorsione

Dato che spesso `e complesso fomulare un’ipotesi di soluzione per una data ricorrenza, `e possibile utiliz-

zare il metodo dell’albero di ricorsione, in cui ogni nodo rappresenta il costo di un singolo sottoproblema.

Sommando i costi dei nodi di ogni livello, si ottengono i costi relativi a quel livello e, sommando tali

costi, si ottiene il costo generale della ricorrenza, che rappresenta l’ipotesi da verificare con il metodo

della sostituzione. Utilizzando questo metodo, si tollera un certo livello di approssimazione, in quan-

to `e interessante analizzare solamente il comportamento asintotico della ricorrenza: si possono quindi

eliminare gli operatori ’ceil’ e ’floor’ e fare delle ipotesi blande per semplificare i calcoli.

ESEMPIO: Si calcoli la ricorrenza T(n) = 3T(⌊n/4⌋) + Θ(n2). Come detto, si pu`o approssimare la

ricorrenza eliminando l’operatore floor, ottenendo T(n) = 3T(n/4) + cn2, per una data costante c>0.

Per comodit`a, si suppone anche che nsia una potenza di 4, in modo tale che ogni livello dell’albero abbia

dimensione intera. Si ottiene cos`ı il seguente albero delle ricorrenze:

Figura 8.1: Albero della ricorrenza T(n) = 3T(n/4) + cn2

La parte (a) della figura mostra T(n), che viene espanso nella parte (b) in un albero equivalente

che rappresenta la ricorrenza. Il termine cn2 nella radice di quest’albero rappresenta il costo al livello56 CAPITOLO 8. ALGORITMI

16

pi`u alto della ricorsione, mentre i tre sottoalberi rappresentano i costi richiesti dai tre sottoproblemi di

dimensione n/4. La parte (c) mostra l’espansione dei nodi di costo T(n/4) dalla parte (b), in cui ogni

nodo figlio ha costo c(n/4)2. Tale processo viene ripetuto pi`u e pi`u volte fino ad ottenere i casi base,

rappresentati nella parte (d) con T(1).

La dimensione dei sottoproblemi per i nodi alla profondit`a i `e di n/4i, quindi la dimensione del

sottoproblema diventa 1 (dimensione delle foglie) quando (n/4)i = 1, ovvero quando i= log4(n): dunque,

l’albero della ricorrenza ha esattamente log4n+1 livelli. Ora, per determinare il costo di ogni livello, basti

pensare che ogni nodo dell’albero genera tre sottonodi e che, dunque, il numero di nodi alla profondit`a i

`e 3i. Moltiplicando il risultato appena ottenuto con il costo di un singolo nodo, si ottiene che ogni livello

ha un costo di 3ic(n/4i)2 = (3/16)icn2. L’ultimo livello dell’albero conta nlog4 3 nodi, ognuno di costo

T(1), per un costo totale di nlog4 3T(1), ovvero Θ(nlog4 3).

A questo punto, si sommano i contributi di ogni livello, ottenendo:

T(n) = cn2 +

=

log4 n−1

i=0

3

16

cn2 +

i

3

16

i

3

16

2

cn2 +...+

cn2 + Θ(nlog4 3)

∗

<

∞

i=0

3

16

cn2 + Θ(nlog4 3)

1

=

1−(3/16)cn2 + Θ(nlog4 3)

=

cn2 + Θ(nlog4 3)

13

= O(n2).

3

16

log4 n−1

cn2 + Θ(nlog4 3)

Il passaggio segnato con * rappresenta una piccola approssimazione: la log4 n−1

i=0

3

16

i

cn2 ammette

come limite superiore∞

i=0

3

16

i

cn2, che rappresenta una serie geometrica decrescente infinita. In questo

modo `e possibile proseguire con agilit`a i calcoli, ottenendo come ipotesi T(n) = O(n2), che dovr`a essere

verificata con il metodo della sostituzione.

8.4.3 Metodo dell’Esperto

Il metodo dell’esperto `e impiegato per la risoluzione di ricorrenze del tipo T(n) = aT(n/b) + f(n),

con a ≥1,b > 1 costanti ed f(n) una funzione asintoticamante positiva. Una ricorrenza di questo

tipo rappresenta il tempo di esecuzione di un algoritmo che divide il problema di dimensione n in a

sottoproblemi di dimensione n/b, mentre la funzione f(n) rappresenta il costo di divisione del problema

e di combinazione delle soluzioni. Il metodo dell’esperto dipende dal seguente teorema:

Teorema 8.4.1 (Master Theorem). Date le costanti a ≥1, b > 1 e la funzione f(n), se la ricorsione

T(n) si presenta nella forma T(n) = aT(n/b) + f(n), allora pu`o essere limitata asintoticamente nei

seguenti modi:

1. Se f(n) = O(nlogb a−ε) per qualche ε>0, allora T(n) = Θ(nlogb a);

2. Se f(n) = Θ(nlogb a), allora T(n) = Θ(nlogb alog2(n));

3. Se f(n) = Ω(nlogb a+ε) per qualche ε > 0 e se af(n/b) ≤cf(n) per qualche c < 1 e per ogni n

sufficientemente grande, allora T(n) = Θ(f(n)).

Si osservi che in ciascuno dei tre casi, si confronta la funzione f(n) con la funzione nlogb a: in-

tuitivamente, la soluzione della ricorrenza `e determinata dalla funzione polinomialmente 3 pi`u gran-

de. Se la funzione nlogb a `e pi`u grande polinomialmente, come nel caso uno, allora sar`a soluzione

della ricorrenza, altrimenti la soluzione sar`a f(n), come enunciato nel caso tre, in cui si deve anche

verificare la condizione di regolarit`a della funzione. Nel caso due, in cui le due funzioni sono asin-

toticamente uguali, si moltiplicano entrambi i membri per un fattore logaritmico e la soluzione sar`a

T(n) = Θ(nlogb alog2(n)) = Θ(f(n)log2(n)).

3Una funzione `e polinomialmente pi`u grande rispetto ad un’altra funzione se la prima `e asintoticamente pi`u grande della

seconda di un fattore nε per qualche ε > 0.8.5. HEAP SORT 57

I tre casi, sfortunatamente, non coprono tutte le funzioni f(n) possibili, in quanto ci sar`a un intervallo

fra i casi 1 e 2, in cui la funzione f(n) `e minore di nlogb a, ma non polinomialmente, mentre ci sar`a anche

un intervallo fra i casi 2 e 3, in cui la funzione f(n) `e maggiore di nlogb a, ma non polinomialmente. In

questi casi, il teorema dell’esperto non pu`o essere applicato.

Per utilizzare il teorema enunciato, bisogna semplicemente determinare in quali dei tre casi rientra

la funzione f(n) e confrontarla con la funzione nlogb a

.

ESEMPIO: Si determini la soluzione della ricorrenza T(n) = 9T(n/3) + n. In questo caso, si ha che

a= 9,b= 3 ed f(n) = n e quindi nlogb a = nlog3 (9) = Θ(n2). Dato che f(n) = O(nlog3 (9)−ε), con ε= 1

(in quanto f(n) = n), si pu`o applicare il caso 1 del teorema dell’esperto e concludere immediatamente

che la soluzione della ricorrenza `e T(n) = Θ(n2), in quanto n2 `e polinomialmente pi`u grande di n.

ESEMPIO: Si determini la soluzione della ricorrenza T(n) = 2T(n/2)+nlog2 n. In questo caso, si ha

che a= 2,b= 2 ed f(n) = nlog2 n e quindi nlogb a = nlog2 (2) = n. Si potrebbe erroneamente pensare di

essere nel terzo caso del teorema dell’esperto, ma le due funzioni non sono polinomialmente comparabili

quindi non si pu`o applicare il teorema. La ricorrenza, dunque, deve necessariamente essere risolta con

l’utilizzo dei metodi precedentemente analizzati.

8.5 Heap Sort

Analizzando l’algoritmo Merge Sort si `e constatato che `e efficiente dal punto di vista temporale, ma non

dal punto di vista spaziale, in quanto occupa una grande quantit`a di memoria. A questo proposito, si

analizza ora l’algoritmo Heap Sort, che effettua un ordinamento sul posto degli elementi utilizzando

una struttura dati detta Heap (’mucchio’), per la gestione delle informazioni.

Un Heap (binario) `e una struttura dati ad albero binario quasi completo 4, in cui ogni nodo rappre-

senta un elemento dell’array da ordinare. Nello specifico, A[1] `e la radice dell’albero, e per ogni elemento

A[i], A[2i] e A[2i+1] rappresentano i figli del nodo, mentre A[⌊n/2⌋] rappresenta il nodo padre. Si

possono quindi definire le seguenti procedure:

1 parent ( i ) :

2 return ⌊i/2⌋

1 left ( i ) :

2 return 2i

1 right ( i ) :

2 return 2i+ 1

Oltre all’attributo A.length, che ne ritorna la lunghezza, l’array A possiede in questo caso anche

l’attributo A.heapSize, che indica il numero degli elementi dell’heap che sono registrati nell’array A. In

altre parole, anche se l’array contiene n elementi, con n=A.length, soltanto gli elementi in A[1..A.

heapSize], con 0 ≤A.heapSize ≤A.length, sono elementi validi dell’heap.

Esistono, inoltre, due tipologie di heap binari: max-heap e min-heap. Il primo, pi`u importante, `e

costruito in modo tale che ogni nodo rispetti la condizione per cui A[parent(i)] ≥ A[i]; dunque, il

valore di un nodo `e al massimo il valore del nodo padre e, di conseguenza, l’elemento pi`u grande di un

max-heap `e memorizzato alla sua radice. Il secondo, meno utilizzato, `e costruito in modo tale che ogni

nodo rispetti la condizione per cui A[parent(i)] ≤ A[i].

Per implementare l’algoritmo heapsort si fa utilizzo del max-heap; per poterne mantenere le propriet`a

si utilizza la procedura di supporto maxHeapify, un algoritmo che prende in input un array A e un suo

indice i, e restituisce l’array ordinato in modo tale da rappresentare il max-heap. Quando tale procedura

viene invocata, essa assume che gli alberi binari di radici left(i) e right(i) siano dei max-heap, ma

assume anche che A[i] possa essere pi`u piccolo dei suoi figli, violando la propriet`a fondamentale. La

procedura, quindi, ha il compito di far ’scendere’ il valore A[i] in modo tale che il sottoalbero con radice

di indice i diventi un max-heap.

4Un albero binario quasi completo `e una struttura dati ad albero in cui ogni livello `e completo, eccetto per al pi`u l’ultimo

livello, che potrebbe essere completo solo fino ad un certo punto da sinistra58 CAPITOLO 8. ALGORITMI

In pseudocodice:

1 ma xH ea pi fy (A , i ) :

2 l := left ( i )

3 r := right ( i )

4 i f l <= A . heapSize and A [ l ] > A [ i ]:

5 max := l

6 e l s e :

7 max := i

8 i f r <= A . heapSize and A [ r ] > A [ max ]:

9 max := r

10 i f max != i :

11 swap A [ i ] with A [ max ]

12 ma xH ea pi fy (A , max )

A ogni passo viene determinato il pi`u grande degli elementi A[i], A[left(i)] e A[right(i)] e il

suo indice viene memorizzato nella variabile max. Se A[i] `e l’elemento pi`u grande, allora il sottoalbero

`e gi`a un max-heap e la procedura termina la propria esecuzione, altrimenti uno dei due figli contiene

l’elemento pi`u grande e A[i] viene scambiato con A[max] (swap with); in questo modo, il nodo di

indice i e i suoi figli soddisfano la propriet`a di max-heap. Il nodo con indice massimo, per`o, presenta il

valore originale di A[i] e, quindi, il sottoalbero di radice max potrebbe violare la propriet`a fondamentale:

quindi, la procedura viene chiamata ricorsivamente sul sottoalbero, fino a raggiungere le foglie.

Questa procedura viene eseguita in un tempo O(h), con hl’altezza dell’albero. Essendo l’albero quasi

completo, h= O(logn), quindi T(n) = O(logn).

Ora, tramite la procedura maxHeapify `e possibile convertire un array A[1..n] (con n=A.length)

in un max-heap. Prima di procedere, `e importante osservare come tutti gli elementi A[⌊n/2⌋+ 1 .. n]

siano foglie dell’albero e, quindi, ciascuno di essi `e un heap di un solo elemento, che si pu`o utilizzare

come punto di partenza per la costruzione dell’heap. Si introduce, dunque, la procedura buildMaxHeap,

che attraversa i nodi restanti dell’albero ed esegue la procedura maxHeapify in ciascuno di essi.

In pseudocodice:

1 b u i l d M a x h e a p ( A ) :

2 A . heapSize := A . length

3 f o r i := ⌊A . length / 2 ⌋ down to 1:

4 ma xH ea pi fy (A , i )

Si pu`o dimostrare che tale procedura impiega un tempo di esecuzione T(n) = O(n).

A questo punto, `e possibile scrivere l’algoritmo heapSort. In pseudocodice:

1 heapSort ( A ) :

2 b u i l d M a x h e a p ( A )

3 f o r i := A . length down to 2:

4 swap A [1] with A [ i ]

5 A . heapSize := A . heapSize - 1

6 ma xH ea pi fy (A , 1)

Questo algoritmo si basa sul fatto che, una volta riordinato l’array in maniera che rappresenti un

max-heap, l’elemento pi`u grande dell’array si trova in A[1]: questo elemento pu`o quindi essere inserito

nella posizione finale corretta scambiandolo con A[n]. Se ora si toglie il nodo n dall’heap, diminuendo

A.heapSize, si nota che i figli della radice restano max-heap, ma la nuova radice potrebbe violare la

propriet`a del max-heap. Questo problema pu`o essere rimosso chiamando la procedura maxHeapify(

A, 1), che lascia un max-heap in A[1..n-1]. Questa operazione viene ripetuta fino ad un heap di

dimensione 2, gi`a ordinato per definizione.

Come detto in precedenza, la procedura buildMaxHeap impiega un tempo di esecuzione lineare (O(n)),

mentre le n−1 chiamate alla procedura maxHeapify impiegano ciascuna un tempo O(logn). Pertanto

il tempo di esecuzione dell’heapSort impiega un tempo di esecuzione T(n) = O(nlogn).8.6. QUICK SORT 59

8.6 Quick Sort

Quick sort `e un algoritmo di ordinamento divide et impera, il cui tempo di esecuzione nel caso peggiore

`e O(n2). Nonostante un tempo di esecuzione molto lento nel caso peggiore, quick sort `e uno degli

algoritmi pi`u utilizzati perch`e ha un tempo medio atteso Θ(nlog) e i fattori costanti nascosti dalla

notazione asintotica sono pressoch`e nulli. Inoltre, `e un algoritmo di ordinamento sul posto, che lo rende

utilizzabile anche in calcolatori con memoria limitata.

L’idea generale di questo algoritmo si basa sui tre tipici passi del metodo divide et impera, per un

sottoarray A[p..r]:

1. Divide: partiziona l’array A[p..r] in due sottoarray A[p..q-1] e A[q+1..r] (eventualmente vuoti)

tali che ogni elemento di A[p..q-1] sia minore o uguale di A[q] che, a sua volta, `e minore o uguale

di ogni elemento di A[q+1..r].

2. Impera: ordina i due sottoarray A[p..q-1] e A[q+1..r] chiamando ricorsivamente s`e stesso.

3. Combina: nessuna operazione di ricombinazione necessaria in quanto l’array A[p..r] `e gi`a ordi-

nato.

La procedura quickSort `e implementata tramite il seguente pseudocodice:

1 quickSort (A , p , r ) :

2 i f p < r :

3 q = partition (A , p , r )

4 quickSort (A , p , q -1)

5 quicksort (A , q +1 , p )

Per pter ordinare un intero array A, la chiamata iniziale a tale algoritmo `e quickSort(A, 1, A.

length). Si noti che all’interno di tale algoritmo viene chiamata la sottoprocedura partition, definita

come segue in pseudocodifica:

1 partition (A , p , r ) :

2 x := A [ r ]

3 i := p - 1

4 f o r j := p to r - 1:

5 i f A [ j ] <= x :

6 i := i + 1

7 swap A [ i ] with A [ j ]

8 swap A [ i + 1] with A [ r ]

9 return i + 1

Questo algoritmo riarrangia il sottoarray A[p..r] sul posto selezionando un elemento x = A[r] come

pivot, intorno a cui partizionare l’array. All’inizio di ogni iterazione del ciclo for di riga 4, per qualsiasi

indice k si individuano quattro regioni:

1. Se p≤k≤i, allora A[k] ≤ x;

2. Se i+ 1 ≤k≤j−1, allora A[k] ≥ x;

3. Se k= r, allora A[k]=x;

4. Gli indici k tali che j ≤k≤r−1 non hanno una particolare relazione con il pivot x.

Le ultime due righe della procdeura, inveceinseriscono il pivot al suo posto nel mezzo dell’array,

scambiandolo con l’elemento pi`u a sinistra, che `e maggiore di x, e restituisce un nuovo indice di pivot. Il

tempo di esecuzione dell’algoritmo partition con input il sottoarray A[p..r] `e Θ(n), con n= r−p+1.

Il tempo di esecuzione dell’algoritmo quickSort dipende solamente da come viene partizionato l’array

(in maniera bilanciata o meno) che, a sua volta, dipende da quali elementi vengono utilizzati per il

partizionamento. Se il partizionamento `e bilanciato, l’algoritmo ha un tempo di esecuzione Θ(nlogn),

mentre nel caso peggiore, quando il partizionamento `e sbilanciato, l’algoritmo converge ad una solzuione

in un tempo Θ(n2).

Il comportamento nel caso peggiore si verifica quando la subroutine partition produce un sotto-

problema con n−1 elementi e uno vuoto. Per calcolare il tempo di esecuzione, si suppone che questo60 CAPITOLO 8. ALGORITMI

sbilanciamento si verifichi per ogni chiamata ricorsiva. Il partizionamento costa un tempo di esecuzione

Θ(n) e, dato che uno dei due array `e vuoto e l`aaltro conta n−1 elementi, si ha un tempo totale:

T(n) = T(n−1) + T(0) + Θ(n) = T(n−1) + Θ(1) + Θ(n)

Intuitivamente, e si sommano i costi ad ogni livello della ricorsione si ottiene una serie aritmetica, il cui

valore `e Θ(n2). Questa situazione si verifica quando l’array di partenza `e gi`a completamente ordinato.

Il comportamento nel caso ottimo si verifica quando la subroutine partition produce due sotto-

problemi di dimensione non maggiore di n/2: in questo caso il tempo di esecuzione dell’algoritmo `e

molto pi`u rapido e avviene in un tempo totale T(n) ≤2T(n/2) + Θ(n), che per il secondo caso del

teorema dell’esperto, ha soluzione T(n) = Θ(nlogn). Si noti, inoltre, che nel caso in cui la partizione

non fosse perfettamente bilanciata, l’algoritmo riuscirebbe comunque a riordinare l’array in un tempo

T(n) = Θ(nlogn): questo dimostra che il quickSort `e un algoritmo molto pi`u vicino al caso ottimo che

al caso pessimo, caso che si verifica in una sola istanza del problema (quando, appunto, `e ordinato).

Il comportamento nel caso medio si verifica quando la subroutine partition produce una combina-

zione di partizioni ’buone’ e ’cattive’. Si suppone, per semplicit`a, che le partizioni buone e cattive si

alternino all’interno dell’albero di ricorsione e che quelle buone siano tutte nel caso migliore, mentre le

quelle cattive siano nel caso pessimo. Si ipotizzi che nella radice dell’albero il costo di ripartizione `e ne i

sottoarray prodotti hanno dimensione n−1 e 0 (caso pessimo), mentre nel livello successivo il prtiziona-

mento del sottoarray n−1 produca due array di dimensione (n−1)/2 e (n−1)/2−1 (caso migliore). Il

costo di una divisione cattiva, seguito da una divisione buona `e comunque Θ(n), ovvero lo stesso costo di

una divisione buona: intuitivamente, quindi, la coppia divisione buona/cattiva impiega lo stesso tempo

totale di esecuzione Θ(nlogn), con l’unica differenza che cambiano le costanti moltiplicative, eclissante

nella notazione asintotica.

8.7 Counting Sort

Gli algoritmi analizzati fino ad ora, seppur differenti fra loro, condividono un’importante propriet`a:

l’ordinamento che effettuano `e basato soltanto su confronti fra gli elementi di input. Questi algoritmi

sono detti di ordinamento per confronti e, dati due elementi ai e aj, eseguono uno dei test ai <aj,ai ≤

aj,ai = aj,ai ≥aj o ai >aj per determinare il loro ordine relativo.

Gli algoritmi di ordinamento per confronti possono essere visti in termini di alberi di decisione,

ovvero alberi binari completi che rappresentano i confronti fra gli elementi effettuati da un determinato

algoritmo di ordinamento. Ora, l’esecuzione di un algoritmo di ordinamento corrisponde ad indicare su

tale albero un cammino semplice che collega la radice dell’albero con una foglia (nello specifico, una delle

foglie che rappresentano le permutazioni ordinate dell’array di ingresso). Ogni nodo interno di tale albero

rappresenta un confronto: il sottoalbero sinistro corrisponde a confronti del tipo ai ≤aj, mentre quello

destro corrisponde a confronti del tipo ai > aj. Si noti che sulle foglie sono presenti tutte le possibili

permutazioni della sequenza di input: dunque un albero di decisione pu`o presentare pi`u di n! foglie, in

quanto alcune permutazioni potrebbero comparire pi`u volte, ma meno di 2h (con h, l’altezza dell’albero).

La lunghezza del cammino semplice pi`u lungo dalla radice di un albero di decisione ad una delle sue

foglie rappresenta il numero di confronti che un determinato algoritmo di ordinamento deve svolgere nel

caso peggiore: questo numero `e equivalente all’altezza dell’albero stesso. Si introduce quindi il seguente

teorema, che determina un limite inferiore sul tempo di esecuzione degli algoritmi di ordinamento per

confronti:

Teorema 8.7.1. Qualsiasi algoritmo di ordinamento per confronti richiede Ω(nlogn) confronti nel caso

peggiore.

da cui deriva anche:

Teorema 8.7.2. Ogni albero di decisione di un algoritmo di ordinamento di n elementi ha altezza

Ω(nlogn).

Una volta determinato il limite inferiore del tempo di esecuzione degli algoritmi di ordinamento, si

introduce qui l’algoritmo counting sort, che riordina un array di dimensione nin un tempo lineare Θ(n).

Tale algoritmo suppone che ciascuno degli elementi di input sia un numero intero compreso nell’intervallo8.7. COUNTING SORT 61

da 0 a k∈N e determina per ciascun di essi il numero di elementi minori; utilizza poi questa informazione

per inserire l’elemento corrente direttamente nella giusta posizione nell’array di output. Ad esempio, se

l’elemento x`e pi`u grande di 5 altri elementi, allora verr`a inserito nella posizione 6 dell’array di output.

Nel codice di counting sort, si suppone che l’input sia un array A[1..n], con n=A.length. Occorrono

altri due array: l’array B[1..n], che contiene l’output ordinato, e l’array C[0..k] fornisce la memoria

temporanea di lavoro. In pseudocodice:

1 c o u n t i n g S o r t (A , B , k ) :

2 C := [0 .. k ]

3 f o r i := 0 to k :

4 C [ i ] := 0

5 f o r j := 1 to A . length :

6 C [ A [ j ]] := C [ A [ ji ]] + 1

7 f o r i := 1 to k :

8 C [ i ] := C [ i ] C [ i - 1]

9 f o r j := A . length down to 1

10 B [ C [ A [ j ]]] := A [ j ]

11 C [ A [ j ]] := C [ A [ j ]] - 1

Dopo che il ciclo for in riga 3 inizializza a zero tutti gli elementi dell’array C, ogni elemento dell’input

viene esaminato con il secondo ciclo for (in riga 5): se il valore di un elemento `e i, viene incrementato

il valore di C[i]. Dunque, dopo la riga 6, l’array C contiene il numero di elementi uguagli ad i, per ogni

i = 0,1,...,k. Le righe 7 e 8 determinano, per ogni i = 0,1,...,k, quanti elementi di input sono minori

o uguali a i. Infine, il ciclo for di riga 9 inserisce l’elemento corrente nella posizione corretta all’interno

dell’array di output B.

Il primo ciclo for impiega un tempo di esecuzione Θ(k), il secondo un tempo Θ(n), il terzo un tempo

Θ(k) e, infine, il ciclo for di riga 9 impiega un tempo di esecuzione lineare Θ(n). Dunque, il tempo di

esecuzione totale dell’algoritmo countingSort `e T(n) = Θ(n+ k). Di solito, questa procedura viene

utilizzata quando h= Θ(n), facendo si che il tempo totale di esecuzione sia un Θ(n).

L’algoritmo appena analizzato batte il limite inferiore di tempo Ω(nlogn) per gli algoritmi di or-

dinamento per confronti perch`e non confronta nessun elemento dell’input, ma utilizza il valore di ogni

elemento come indice di un array C di appoggio.62 CAPITOLO 8. ALGORITMICapitolo 9

Strutture Dati

Gli insiemi manipolati dagli algoritmi, a differenza di quelli matematici, possono essere modificati in-

serendo o rimuovendo elementi. Questi insiemi sono detti dinamici e giocano un ruolo importante in

informatica, perch`e modellano le strutture utilizzate per memorizzare in modo ordinato i dati.

In una tipica implementazione di un insieme dinamico, ogni elemento `e rappresentato da un oggetto, i

cui attributi possono essere esaminati e manipolati a piacimento dagli algoritmi. In molte strutture dati,

l’oggetto dispone di una chiave identificativa (spesso univoca, ma non necessariamente) e ovviamente

di dati satelliti che si vogliono memorizzare ordinatamente in memoria. Oltre a questi due attributi,

l’oggetto pu`o anche contenere altri dati specifici per una determinata struttura dati, in modo da rendere

pi`u semplice e veloce la loro manipolazione.

Le tipiche operazioni che si possono svolgere sulle strutture dati sono suddivise in due categorie:

le query (interrogazioni), che hanno il solo scopo di estrapolare informazioni dall’insieme dinamico, e le

operazioni di modifica, che hanno il compito di modificare l’insieme. Di seguito sono elencate le istruzioni

pi`u comuni:

search(S, k): `e un’operazione di query che, dato un insieme S e un valore chiave k, restituisce

NIL se tale elemento non appartiene all’insieme.

insert(S, x): `e un’operazione di modifica che inserisce all’interno dell’insieme S l’elemento

puntato da x.

delete(S, x): `e un’operazione di modifica che, dato un puntatore x ad un elemento dell’insieme

S, rimuove x da S.

minimum(S): `e un’operazione di query che ritorna l’elemento dell’insieme S con la chiave pi`u

piccola.

maximum(S): `e un’operazione di query che ritorna l’elemento dell’insieme Scon la chiave pi`u grande.

successor(S, x): `e un’operazione di query che, dato un elemento x la cui chiave appartiene ad

un insieme totalmente ordinato S, restituisce un puntatore all’elemento successivo pi`u grande di S

oppure NIL se x`e il pi`u grande degli elementi.

predecessor(S, x): `e un’operazione di query che, dato un elemento xla cui chiave appartiene ad

un insieme totalmente ordinato S, restituisce un puntatore all’elemento precedente pi`u piccolo di

S oppure NIL se x`e il pi`u piccolo degli elementi.

9.1 Stack

Gli stack sono insiemi dinamici dove l’elemento da rimuovere tramite l’operazione delete `e predeter-

minato. In questa struttura dati, l’elemento cancellato `e quello inserito per ultimo, secondo la politica

LIFO (Last In, First Out). Nello specifico, le operazioni di insert e delete prendono rispettivamente

il nome di push e pop 1: la prima inserisce in cima alla pila l’elemento passato come argomento, mentre

la seconda operazione elimina l’unico elemento accessibile dalla pila, ovvero la cima.

1Questa operazione non prende nessun argomento, in quanto l’elemento da eliminare `e predeterminato

6364 CAPITOLO 9. STRUTTURE DATI

Questa struttura dati pu`o essere implementata tramite un array con un massimo di nelementi S[1..

n], che presenta lo specifico atrtibuto S.top, ovvero l’indice tramite cui accedere all’ultimo elemento

inserito. L’array `e dunque composto dagli elementi S[1..S.top], dove S[1] rappresenta l’elemento in

fondo alla pila, mentre S[S.top] rappresenta l’elemento in cima. Ovviamente, se S.top = 0, si dice

che la pila `e vuota, in quanto non contiene nessun elemento. In questo caso, se si tenta di estrarre

un elemento dallo stack, si ottiene un errore di underflow dello stack, mentre se si cerca di inserire un

elemento sulla pila piena (che conta quindi di n elementi), si ottiene un errore di overflow dello stack.

Le operazioni dello stack possono essere implementate molto semplicemente in pseudocodifica come

segue:

1 push (S , x ) :

2 i f S . top = S . length :

3 error " overflow "

4 e l s e :

5 S . top := S . top + 1

6 S [ S . top ] := x

1 pop ( S ) :

2 i f iS . top = 0:

3 error " underflow "

4 e l s e :

5 S . top := S . top - 1

6 return S [ S . top + 1]

Si noti come, in questo caso, l’operazione di pop ritorna l’elemento appena eliminato dallo stack.

Entrambe le procedure vengono eseguite in tempo costante Θ(1).

9.2 Queue

Le code sono insiemi dinamici dove l’elemento da rimuovere tramite l’operazione delete `e predeter-

minato. In questa struttura dati, l’elemento cancellato `e quello inserito per primo, secondo la politica

FIFO (First In First Out). Nello specifico, la coda presenta un inizio detto head e una fine detta tail,

e le operazioni di insert e delete prendono rispettivamente il nome di enqueue e dequeue 2: la prima

inserisce in fondo alla fila l’elemento passato come argomento, mentre la seconda operazione elimina il

primo elemento della fila.

Questa struttura dati pu`o essere implementata tramite un array di nelementi Q[1..n], che contiene

un massimo di n−1 elementi, per ragioni che verranno chiarite in seguito. L’attributo Q.head punta

all’inizio della coda, mentre l’attributo Q.tail punta alla posizione in cui l’ultimo elemento che dovr`a

essere inserito prender`a posto (ovvero alla posiziove vuota successiva all’ultimo elemento della coda).

Gli elementi della coda, quindi, occupano le posizioni Q.head, Q.head + 1, ..., Q.tail - 1. Alla fine

dell’array la posizione 1 della queue segue immediatamete la posizione n secondo un ordine circolare.

Se Q.head = Q.tail allora la coda `e vuota. All’inizio le posizioni Q.head e Q.tail combaciano e sono

entrambe inizializzate al valore 1.

Come per gli stack, se la coda `e vuota, il tentativo di rimuovere un elemento provoca un errore di

underflow, mentre se Q.head = Q.tail + 1 la coda `e piena e il tentativo di inserire un nuovo elemento

provoca un errore di overflow.

Le operazioni della queue possono essere implementate molto semplicemente in pseudocodifica come

segue:

1 enqueue (Q , x ) :

2 Q [ Q . tail ] := x

3 i f Q . tail = Q . length :

4 Q . tail := 1

5 e l s e :

6 Q . tail := Q . tail + 1

2Anche in questo caso, questa operazione non prende nessun argomento, in quanto l’elemento da eliminare `e

predeterminato9.3. LINKED LIST 65

1 dequeue (Q , x ) :

2 x := Q [ Q . head ]

3 i f Q . head = Q . length :

4 Q . head := 1

5 e l s e :

6 Q . head := Q . head + 1

7 return x

Entrambe le procedure vengono eseguite in un tempo costante Θ(1).

9.3 Linked List

Una lista concatenata `e una struttura dati i cui oggetti sono disposti in ordine lineare, determinato

da un puntatore in ogni oggetto. Una lista doppiamente concatenata `e una lista in cui ogni oggetto

presenta, oltre ad una chiave key, anche un puntatore all’elemento successivo next e un puntatore a

quello precedente prev. Se x.prev = NIL, allora l’elemento x `e il primo elemento della lista e si dice

essere la testa (o head) della lista. Se, invece, x.next = NIL, allora x`e l’ultimo elemento della lista e si

dice essere la coda (o tail) della lista. Intuitivamente, l’attributo L.head punta alla testa della lista, che

sar`a vuota se L.head = NIL.

Questa struttura dati pu`o presentare varie forme: pu`o essere doppiamente concatenata o singolar-

mente concatenata, oppure pu`o essere circolare o non. Una lista si dice singolarmente concatenata se i

suoi oggetti non sono dotati di puntatore all’elemento precedente, mentre si dicono circolari se l’ultimo

elemento possiede un puntatore alla testa della lista, che a sua volta possiede un puntatore alla coda se

la lista `e circolare. Una lista concatenata pu`o anche essere ordinata o non: si dice ordinata quando la

disposizione lineare degli elementi corrisponde con la disposizione crescente delle chiavi degli elementi e,

in tal caso, la testa della lista conterr`a l’elemento minimo, mentre la coda l’elemento massimo.

Nel seguito si fa riferimento a liste non ordinate doppiamente concatenate per lo sviluppo degli

algoritmi che le manipolano.

Ricerca La prima procedura che sia analizza `e listSearch(L, k), che trova il primo elemento con la

chiave k nella lista L, restituendo un puntatore a tale oggetto. Se nessun oggetto con chiave k`e presente

nella lista, allora viene restituito il valore NIL. In pseudocodifica:

1 li st Se ar ch (L , k ) :

2 x := L . head

3 w h i l e x != NIL and x . key != key :

4 x := x . next

5 return x

Si noti quindi che l’algoritmo listSearch cerca l’elemento di chiave k tramite una ricerca lineare

sulla list L di n elementi. Dunque, l’algoritmo impiega un tempo Θ(n) nel caso peggiore, in quanto

potrebbe essere necessario scorrere l’intera lista.

Inserimento La seconda procedura analizzata `e listInsert(L, x) che inserisce l’elemento x di

attributo key (gi`a inizializzato) in testa alla lista. In pseudocodifica:

1 li st In se rt (L , x ) :

2 x . next := L . head

3 i f L . head != NIL :

4 L . head . prev := x

5 L . head := x

6 x . prev := NIL

Questa procedura impiega un tempo costante Θ(1) per la sua esecuzione.

Rimozione L’ultima procedura analizzata per le linked list `e listDelete(L, x), che rimuove l’e-

lemento x dalla lista L. Per poter eliminare tale elemento `e prima necessario chiamare la funzione

listSearch per ottenere il puntatore all’elemento desiderato. In pseudocodifica:66 CAPITOLO 9. STRUTTURE DATI

1 li st De le te (L , x ) :

2 i f x . prev != NIL :

3 x . prev . next := x . next

4 e l s e :

5 L . head := x . next

6 i f x . next != NIL :

7 x . next . prev := x . prev

Anche questa procedura impiega un tempo di esecuzione Θ(1).

9.4 Hash Table

9.4.1 Indirizzamento diretto

Prima di procedere con l’introduzione alle tavole di hash, `e prima necessario introdurre il concetto di

indirizzamento diretto, una tecnica molto efficiente nel caso in cui l’insieme da cui vengono acquisite le

chiavi, detto insieme universo U= {0,1,2...,m−1}, `e un insieme ragionevolmente piccolo. Si suppone,

inoltre, che due elementi distinti non possano avere chiavi coincidenti. Per rappresentare un tale insieme

dinamico si utilizza un array, oppure una tavola ad indirizzamento diretto, indicata con T[0..m−1], dove

ogni cella k di tale tabella punta all’elemento dell’insieme di chiave k. Se la k-esima cella non contiene

nessun elemento, viene inizializzata con il valore NIL.

Le operazioni di dizionario sono semplici da implementare in pseudocodifica e impiegano tutte un

tempo costante O(1) (nel caso peggiore):

1 d i r e c t A d d r e s s S e a r c h (T , 2 return T [ k ]

k ) :

1 d i r e c t A d d r e s s I n s e r t (T , 2 T [ x . key ] := x

x ) :

1 d i r e c t A d d r e s s D e l e t e (T , 2 T [ x . key ] := NIL

x ) :

In alcune implementazioni `e possibile memorizzare l’elemento di chiave k direttamente all’interno

della tabella, anzich`e in un oggetto esterno, risparmiando spazio in memoria.

9.4.2 Introduzione alle Tavole di Hash

La difficolt`a nell’implementazione di una tale struttura dati `e evidente: l’insieme universo U, nella

maggior parte dei casi, `e troppo grande per essere memorizzato in una tavola T di dimensione |U|.

Inoltre, l’insieme K delle chiavi effettivamente memorizzate `e molto pi`u piccolo dell’inisieme U delle

chiavi disponibili e, dunque, la maggior parte dello spazio allocato per la tavola T non verrebbe mai

utilizzato. A questo proposito si introduce una nuova struttura dati, detta tavola di hash, che utilizza

una memoria proporzionale al numero delle chiavi effettivamente memorizzate nel dizionario, riducendo

lo spreco di memoria.

Quando l’insieme K delle chiavi memorizzate in un dizionario `e molto pi`u piccolo dell’universo U di

tutte le chiavi possibili, utilizzando una tavola di hash si pu`o ridurre lo spazio richiesto fino a Θ(|K|),

rdiucendo per`o l’efficienza temporale a O(1) nel caso medio (anzich`e pessimo). Nella tabella di hash,

l’elemento di chiave k non viene memorizzato direttamente nella cella k, ma viene utilizzata una cosid-

detta funzione di hash h(k) che calcola l’indice k della cella. La funzione di hash h(k) associa ad ogni

chiave dell’universo U una specifica chiave della tavola di hash T[0..m−1]. Formalmente:

h(k) : U →{0,1,...,m−1}, m<<|U|

Si dice che h(k) `e il valore hash della chiave k.9.4. HASH TABLE 67

9.4.3 Hashing Concatenato

Il problema principale con la tecnica di indirizzamento appena analizzata `e che, riducendo l’intervallo

degli indici da |U|ad m << |U|, `e molto probabile che due chiavi vengano mappate nella stessa cella:

in tal caso si dice che avviene una collisione. Per evitare un evento simile `e possibile, in prima analisi,

implementare una funzione di hash totalmente deterministica il pi`u randomica possibile, in modo da

minimizzare le collisioni. Si dimostra per`o che un evento di collisione `e impossibile da evitare in quanto

|U|>m e quindi, dopo l’m-esima chiamata alla funzione di hash, avver`a sicuramente una collisione.

Si rende necessario, dunque, implementare un meccanismo che gestisca tali eventi. Nello specifico, la

tecnica pi`u utilizzata `e il concatenamento (o chaining), tramite cui, tutti gli elementi associati ad una

stessa cella k sono posti in una lista concatenata. La cella k, in questo caso, punta al nodo di testa della

lista che contiene gli elementi mappati in tale cella, oppure ha valore NIL, nel caso in cui la cella non

contenga nessun elemento.

Le operazioni di dizionario su una tavola di hash T sono facili da implementare in pseudocodifica nel

caso di gestione delle collisioni tramite concatenamento:

1 c h a i n e d H a s h I n s e r t (T , x ) :

2 li st In se rt ( T [ h ( x . key ) ] , x )

1 c h a i n e d H a s h S e a r c h (T , x ) :

2 li st Se ar ch ( T [ h ( x . key ) ] , x )

1 c h a i n e d H a s h D e l e t e (T , x ) :

2 li st De le te ( T [ h ( x . key ) ])

In cui le procedure listInsert, listSearch e listDelete, sono le stesse analizzate nella sezione

delle liste concatenate e hanno il compito, rispettivamente, di inserire in testa alla lista un nodo, cercare

un nodo nella lista ed eliminare un nodo dalla lista.

Si passa ora all’analisi del tempo di esecuzione di tali procedure: nel caso peggiore, l’inserimento in

lista di un nodo `e O(1), la ricerca avviene in tempo proporzionale alla lunghezza della lista, quindi O(n),

mentre l’eliminazione di un nodo dalla lista avviene, sempre nel caso peggiore, in tempo O(1) se la lista

`e doppiamente concatenata.

Si noti che la funzione chainedHashDelete prende come input un elemento x, non la sua chiave k,

quindi non occorre cercare prima l’elemento x. Se la tavola di hash supporta la cancellazione, allora

le sue liste dovrebbero essere doppiamente concatenate in modo che la cancellazione di un elemento sia

pi`u rapida. Se le liste fossero singolarmente concatenate, per cancellare l’elemento x, si dovrebbe prima

trovare x nella lista T[h(x.key)] in modo da poter aggiornare l’attributo next dell’elemento precedente

in lista, assegnandogli il valore NIL.

9.4.4 Analisi della Funzione di Hash

Data una tavola di hash T, che conta mcelle in cui sono memorizzati nelementi, si definisce il fattore di

carico αdella tavola T come il rapporto n/m, ossia il numero medio di elementi memorizzati in una lista.

Il caso peggiore nell’hashing si verifica quando tutte le n chiavi sono associate alla stessa cella, creando

una lista di lunghezza n. Il tempo di esecuzione della ricerca diventa quindi Θ(n) a cui si aggiunge il

tempo di esecuzione della funzione di hashing. Ovviamente, un caso del genere `e molto improbabile nel

caso in cui la funzione di hash sia ben progettata. Per il momento si suppone che ogni elemento ha

uguale probabilit`a di essere mappato in una qualsiasi delle m celle, indipendentemente dalle celle in cui

sono stati mappati gli altri elementi. Tale ipotesi viene definita hashing uniforme semplice. Per ogni

j = 0,1,...,m−1, si indica con nj la lunghezza della lista T[j], ottenendo quindi il numero di elementi

totali memorizzati in tabella `e n= n0 +n1 +...+nm−1. Il valore atteso di ogni nj sar`a E[nj] = α= n/m,

quindi il tempo medio per la ricerca di un elemento di chiave k non presente nella lista (caso pessimo)

`e Θ(1 + α), che si dimostra essere anche il tempo di ricerca dello stesso elemento, questa volta presente

tabella. Nella pratica, se il numero di celle nella tavola di hash `e almeno proporzionale al numero di

elementi della tavola, si ottiene che n= O(m) e quindi α= n/m= O(m)/m= O(1). Pertanto, la ricerca

di un elemento della tavola richiede un tempo costante.Ogni operazione di dizionario pu`o essere svolta,

in media, in un tempo O(1).68 CAPITOLO 9. STRUTTURE DATI

9.4.5 Funzione di Hash

Per progettare una buona tabella di hash `e necessario implementare una funzione di hash che sia alta-

mente efficiente. A questo proposito si introducono tre possibili schemi di implementazione: hashing per

divisione (uristico), hashing per moltiplicazione (euristico) e hashing universale (aleatorio, non analizzato

in questa sezione). In generale, una buona funzione di hashing deve soddisfare approssimativamente la

condizione di hashing uniforme semplice: ogni chiave deve avere la stessa probabilit`a di essere mappata

in una qualsiasi cella della tabella. Di solito non `e possibile verificare questa condizione, in quanto non

`e nota la distribuzione delle probabilit`a secondo cui vengono estratte le chiavi. Quindi, nella pratica,

spesso si utilizzano delle tecniche euristiche per la realizzazione di tali funzioni.

La maggior parte delle funzioni di hashing suppone che l’universo delle chiavi sia l’insieme dei numeri

naturali N e quindi, se nella struttura dati progettata, la chiave non `e un numero naturale ma, ad

esempio, una stringa, `e necessario studiare un metodo di conversione: nei calcolatori questo metodo `e

tipicamente gi`a implementato, in quanto ogni informazione analogica viene convertita in una stringa

binaria di bit (appartenente ad N). Nello studio dei tre metodi di hashing si suppone che le chiavi siano

numeri naturali.

Metodo della Divisione Quando si applica il metodo della divisione per creare una funzione di hash,

una chiave kviene associata a una delle mcelle prendeno il resto della divisione fra ked m. Formalmente,

la funzione di hash `e cos`ı definita:

h(k) = kmodm

Il vantaggio principale di questo metodo `e che si pu`o implementare molto rapidamente e richiede un

tempo di esecuzione costante.

Quando si utilizza il metodo della divisione, si cerca di evitare alcuni valori di m. Nello specifico si

evitano le potenze di 2, in quanto se m = 2p, allora h(k) rappresenta proprio i p bit meno significativi

di k: infatti, sarebbe pi`u corretto far dipendere la funzione di hash da tutti i bit della chiave. Inoltre,

si evita di scegliere m+ 2p−1 quando k `e una stringa di caratteri interpretata in base 2p, in quanto

la permutazione dei caratteri di k non cambia il suo valore di hash. Una buona scelta di m, invece,

potrebbe essere un numero primo non troppo vicino a una potenza esatta di 2.

Metodo della Moltiplicazione Il metodo della moltiplicazione per la creazione di funzioni di hash

consiste in due passi. Nel primo passaggio si moltiplica la chiave kper una costante A, tale che 0 <A<1,

per poi estrarre la parte frazionaria del numero appena ottenuto. Nel secondo passaggio si moltiplica

questo valore per m e si prende la parte intera inferiore del risultato. Formalmente, la funzione di hash

`e cos`ı definita:

h(k) = ⌊m(k·Amod1)⌋

dove k·Amod1 rappresenta la parte frazionaria di kA, ovvero kA−⌊kA⌋.

Il vantaggio principale di questo metodo `e che il valore di m non `e critico. Tipicamente si sceglie

un valore di m tale per cui sia una potenza di 2, in modo da rendere pi`u semplice implementare tale

funzione in un calcolatore reale. Si upponga, infatti, che la dimensione di una parola nel calcolatore

sia w bit e che il numero k sia contenuto in una sola parola. Si scelga poi un valore di A che sia una

frazione nella forma s/2w, con s intero nell’intervallo 0 < s < 2w. A questo punto, si moltiplica k per

s= A·2w: il risultato sar`a un numero di 2wbit r12w+ r0, in cui r1 rappresenta la parte pi`u significativa

del prodotto ed r0 la parte meno significativa. Il valore hash desiderato di p bit `e formato dai p bit pi`u

significativi di r0. Sebbene queste operazioni funzionino con qualsiasi valore della costante A, la scelta

spesso adoperata `e A≈(√5−1)/2 ≈0.6180339887...

9.4.6 Indirizzamento Aperto

Un altro metodo per evitare le collisioni `e tramite l’indirizzamento aperto, in cui tutti gli elementi sono

memorizzati nella tavola hash, ovvero ogni cella contiene un elemento dell’insieme dinamico o la costante

NIL se non contiene nessun elemento. Quando si cerca un elemento, si esamina sistematicamente la tabella

fino a quando non si trova l’elemento desiderato, oppure finch`e non ci sono pi`u elementi da controllare

(l’elemento non `e nell’array). Nell’indirizzamento aperto, a differenza degli altri metodi, la tavola hash

pu`o riempirsi fino a quando non pu`o pi`u fisicamente contenere altri elementi. Una conseguenza di questo

design `e che il fattore di carico αnon supera mai il valore 1. Il vantaggio di questo metodo sta nel fatto

che elimina completamente l’utilizzo dei puntatori, in quanto calcola la sequenza delle celle da esaminare,

e libera quindi una notevole quantit`a di memoria, utilizzata per incrementare la capacit`a della tabella,

riducendo il rischio di collisioni.9.4. HASH TABLE 69

Inserimento Per effettuare un insierimento mediante il metodo dell’indirizzamento aperto, si esamina

in successione le posizioni della tavola hash fino a che non si trova una cella libera in cui inserire la

chiave. L’efficienza di questo metodo consiste nel calcolare una nuova sequenza di accesso alla tabella

in base alla chiave dell’oggetto da inserire, anzich`e seguire sempre lo stesso cammino di accessi, che

impiegherebbe un tempo di esecuzione Θ(n). Per determinare quali celle esaminare durante la fase di

ispezione, si estende la funzione di hash in modo da includere l’ordine di ispezione (a partire da 0), come

secondo input. Formalmente, la funzione di hash modificata `e definita come segue:

h(k,i) : U ×{0,1,...,m−1}→{0,1,...,m−1}

Si richiede, inoltre, che per ogni chiave k la sequenza di ispezione <h(k,0),h(k,1),...,h(k,m−1) > sia

una permutazione della sequenza <0,1,...,m−1 >, in modo tale che ogni cella della tavola possa essere

considerata come possibile cella in cui inserire una nuova chiave. In pseudocodifica:

1 ha sh In se rt (T , k ) :

2 i := 0

3 repeat

4 j := h (k , i )

5 i f T [ j ] = NIL or T [ j ] = DELETED :

6 T [ j ] := k

7 return j

8 e l s e :

9 i := i + 1

10 u n t i l i = m

11 error " hash table overflow "

Questa procedura prende in input una tavola di hash T e una chiave k da inserire in tabella, e

ritorna l’indice della cella in cui `e stato inserito l’elemento, oppure error di overflow se non `e presente

nessuna cella libera. Si noti nella condizione in riga 5, che viene verificato se la cella T[k] contiene il

valore DELETED: questo valore speciale verr`a ripreso e analizzato pi`u avanti assieme alla procedura di

eliminazione delle chiavi dalla tabella.

Ricerca Per la ricerca di una determinata chiave kesamina la stessa sequenza di celle che ha esaminato

l’algoritmo di inserimento quando ha inserito l’elemento di chiave k. Dunque, la procedura di ricerca

potrebbe terminare la propria esecuzione senza successo quando trova una cella vuota, in quanto la chiave

ksarebbe stata inserita in quella posizione (si presuppone che le chiavi non possano essere eliminate dalla

tavola). In pseudocodifica:

1 ha sh Se ar ch (T , k ) :

2 i := 0

3 repeat

4 j := h (k , i )

5 i f T [ j ] = k :

6 return j

7 i := i + 1

8 u n t i l T [ j ] = NIL or i = m

9 return NIL

Questa procedura, come la precedente, prende in input una tavola di hash T e una chiave k da

ricercare in tabella, e ritorna l’indice della cella in cui `e stato trovato l’elemento, oppure NIL se non `e

presente nessuna cella che contiene l’elemento oppure se nella sequenza di ricerca si trova una cella libera

(per le ragioni precedentemente analizzate).

Rimozione La procedura di cancellazione di una chiave dalla tavola di hash ad indirizzamento aperto

`e un’operazione molto complessa, in quanto non `e possibile semplicemente cancellare il contenuto della

cella i, assegnandone il valore NIL, in quanto sarebbe impossibile ricercare qualsiasi elemento in tabella

per come `e stata definita la procedura di ricerca. Dunque, si rende necessario marcare la cella il cui

`

contenuto `e stato eliminato con il valore speciale DELETED, anzich`e NIL.

E per questo motivo che in

riga 5 della procedura di inserimento viene anche verificato se la cella ispezionata contanga il valore

DELETED. Si noti inoltre che, utilizzando questa nuova notazione, il tempo di esecuzione della procedura70 CAPITOLO 9. STRUTTURE DATI

di ricerca non dipende pi`u dal fattore di carico α. Per questo motivo, nella pratica si preferisce spesso

utilizzare il metodo della concatenazione quando `e necessario che la tabella di hash supporti l’operazione

di cancellazione delle chiavi.

9.4.7 Hashing Uniforme

Nell’analisi delle tabelle hash con indirizzamento aperto si ipotizza hashing uniforme: si suppone, infatti,

che ogni chiave abbia la stessa probabilit`a di avere come sequenza di ispezione una delle m! permutazioni

di <0,1,...,m−1 >. L’hashing uniforme estende il concetto di hashing uniforme semplice, impiegato pi`u

volte precedentemente, al caso in cui la funzione di hash produce, non un singolo numero, ma un’intera

sequenza di ispezione. Nella pratica non `e possibile ottenere una funzione di hash uniforme, ma si

utilizzano delle approssimazioni accettabili. Si esaminano nel seguito tre tecniche utilizzate per calcolare

le sequenze di ispezione richieste nell’indirizzamento aperto: ispezione lineare, ispezione quadratica e

doppio hashing. Tali tecniche grantiscono che la sequenza < h(k,0),h(k,1),...,h(k,m−1) > sia una

permutazione di < 0,1,...,m−1 > per ogni chiave k, ma nessuna di loro pu`o garantire l’ipotesi di

hashing uniforme, in quanto nessuna di esse `e in grado di generare pi`u di m2 sequenze di ispezioni

differenti (invece delle m! sequenze richieste).

Ispezione Lineare Data una funzione di hash ordinaria h′: U →{0,1,...,m−1}, detta funzione di

hash ausiliaria, il metodo di ispezione lineare utilizza la funzione di hash

h(k,i) = (h′(k) + i) modm

per i = 0,1,...,m−1. Data la chiave k, la prima cella esaminata `e T[h′(k)], che `e la cella data dalla

funzione di hash ausiliaria, la seconda cella `e T[h′(k) + 1] e cos`ı via fino alla cella T[m−1]. Poi,

l’ispezione riprende dalle celle T[0],T[1],...,T[h′(k)−1]. Poich`e la prima cella ispezionata determina

l’intera sequenza di ispezioni, ci sono soltanto m sequenze di ispezione distinte. Questa tecnica `e facile

da implementare ma presenta un problema noto come addensamento primario: si formano lunghe file

di celle occupate che aumentano il tempo medio di ricerca. Tale fenomeno si presenta perch`e una cella

vuota preceduta da i celle piene ha probabilit`a (i+ 1)/m di essere la prossima ad essere occupata e le

lunghe file di celle occupate tendono, dunque, a diventare sempre pi`u lunghe.

Ispezione Quadratica Data la funzione di hash ausiliaria h′ : U →{0,1,...,m−1}, il metodo di

ispezione qudratica utilizza la funzione di hash

h(k,i) = (h′(k) + c1i+ c2i2) modm

per i = 0,1,...,m−1, con c1,c2 ̸= 0 costanti ausiliarie. Data la chiave k, la prima cella esaminata `e

T[h′(k)], mentre le successive posizioni esaminate sono distanti dalle precedenti di quantit`a che dipendono

in modo quadratico dal numero d’ordine di ispezione i. Questa tecnica funziona meglio della precedente,

ma i valori c1,c2 ed m non possono essere scelti in maniera arbitraria, ma devono essere tali per cui

si possa percorrere l’intera tabella. Inolte, se due chiavi hanno la stessa posizione iniziale di ispezione,

allora le due sequenze di ispezione saranno identiche portando al cosiddetto addensamento secondario.

Doppio Hashing Date la funzioni di hash ausiliarie h1 ed h2, il metodo di ispezione lineare utilizza

la funzione di hash

h(k,1) = (h1(k) + ih2(k)) modm

per i= 0,1,...,m−1. Il doppio hashing `e il metodo migliore disponibile per l’indirizzamento aperto, in

quanto le permutazioni prodotte hanno molte caratteristiche comuni con le permutazioni casuali. Data

la chiave k, la prima cella esaminata `e T[h1(k)], mentre le successive posizioni sono distanziate dalle

precedenti di quantit`a h2(k) mod m. Differentemente dai precedenti, il metodo del doppio hashing

produce sequenze che dipendono in due modi dalla chiave k, in quanto possono variare sia la posizione

iniziale della sequenza di ispezione, sia la distanza fra due posizioni successive.

Inoltre, il valore h2(k) deve essere relativamente primo con la dimensione mdella tavola hash perch`e

venga ispezionata l’intera tabella. Un modo pratico per garantire tale condizione `e scegliere m potenza

di due e definire h2 in modo che produca sempre un numero dispari. Un altro modo `e scegliere mprimo

e definire h2 in modo che generi sempre un numero intero positivo minore di m. In questo contesto,

il doppio hashing `e migliore delle precedenti tecniche in quanto utilizza Θ(m2) sequenze di ispezione,

anzich`e Θ(m), perch`e ogni possibile coppia di h1,h2 produce una distinta sequenza di ispezione.9.5. ALBERI BINARI 71

9.5 Alberi Binari

Un albero binario di ricerca `e una struttura dati ad albero3 che supporta molte operazioni degli insiemi

dinamici, come search. delete, insert, minimum, maximum, successor e predecessor. Tali alberi

sono rappresentati da strutture concatenate in cui ogni nodo `e un oggetto, che oltre ad avere una chiave

e i dati satellite, contengono anche gli attributi left, right e parent, che puntano rispettivamente al

figlio sinistro, al figlio destro e al padre. Se manca un figlio o un padre, i corrispondenti attributi sono

inizializzati a NIL. Il nodo radice, detto anche root, `e l’unico nodo nell’albero il cui attributo padre `e

inizializzato con NIL.

Le chiavi dell’albero binario di ricerca sono memorizzate in maniera da rispettare sempre la propriet`a

fondamentale per cui se x`e un nodo in un albero binario di ricerca ed y`e il nodo nel sottoalbero sinistro

di x, allora y.key ≤x.key, mentre se y `e un nodo nel sottoalbero destro di x, allora y.key ≥x.key.

Tale propriet`a permette di elencare ordinatamente tutte le chiavi di un albero binario di ricerca con

un semplice algoritmo ricorsivo di attraversamento simmetrico di un albero, tramite cui la chiave della

radice di un sottoalbero viene stampata nel mezzo tra la stampa dei valori nel sottoalbero sinistro e la

stampa dei valori nel sottoalbero destro. In pseudocodice:

1 i n o r d e r T r e e W a l k ( x ) :

2 i f x != NIL :

3 i n o r d e r T r e e W a l k ( x . left )

4 p r i n t x . key

5 i n o r d e r T r e e W a l k ( x . right )

Per attraversare un albero binario di ricerca costituito da n nodi, `e necessario un tempo Θ(n), in

quanto, dopo la chiamata iniziale, la procedura viene chiamata ricorsivamente esattamente due volte per

ogni nodo dell’albero.

Ricerca Un’altra tipica operazione svolta su un albero binario di ricerca `e quella di cercare una chiave

memorizzata nell’albero: oltre all’operazione search, gli alberi binari supportano anche query come

minimum, maximum, successor e predecessor.

Dato un puntatore alla radice dell’albero e una chiave k da cercare, la procedura treeSearch resti-

tuisce il puntatore al nodo di chiave k, se esiste, oppure NIL, se la chiave non `e presente nell’albero. In

pseudocodifica:

1 tr ee Se ar ch (x , k ) :

2 i f x = NIL or k = x . key :

3 return x

4 i f k < x . key :

5 return tr ee Se ar ch ( x . left , 6 e l s e :

7 return tr ee Se ar ch ( x . right , k )

k )

Questo algoritmo inizia la sua ricerca dalla radice dell’albero e ad ogni iterazione confronta il valore

k passato come argomento con x.key. Se le due chiavi sono uguali la ricerca termina e viene restituito

il puntatore al nodo, mentre se la chiave `e minore della chiave corrente analizzata, per la propriet`a

fondamentale degli alberi binari, si chiama ricorsivamente la procedura sul sottoalbero sinistro, altrimenti

sul sottoalbero destro. Il tempo di esecuzione di tale algoritmo `e O(h), dove h rappresenta l’altezza

dell’albero.

Minimo e Massimo Un elemento con chiave minima in un albero binario di ricerca pu`o sempre essere

trovato seguendo, a partire dalla radice, i puntatori left, fino a quando non viene incontrato un valore

NIL, sempre per la propriet`a fondamentale degli alberi binari di ricerca. In pseudocodifica:

1 t r e e M i n i m u m ( x ) :

2 w h i l e x . left != NIL :

3 x := x . left

4 return x

3consultare appendice A per approfondire la definizione di struttura dati ad albero.72 CAPITOLO 9. STRUTTURE DATI

La procedura per trovare l’elemento massimo, invece, `e simmetrica alla procedura appena analizzata.

In pseudocodifica:

1 t r e e M a x i m u m ( x ) :

2 w h i l e x . right != NIL :

3 x := x . right

4 return x

Entrambe queste procedure vengono eseguite in un tempo O(h), in un albero di altezza h.

Successore e Predecessore Dato un nodo in un albero binario di ricerca, spesso `e necessario trovare

il suo successore, nell’ordine stabilito da un attraversamento simmetrico. Il successore di un nodo x`e il

nodo con la pi`u piccola chiave maggiore di x.key. La struttura di un albero binario consente di trovare

tale nodo senza il bisogno di confrontare le chiavi. In pseudocodifica:

1 t r e e S u c c e s s o r ( x ) :

2 i f x . right != NIL :

3 return t r e e M i n i m u m ( x . right )

4 y := x . parent

5 w h i l e y != NIL and x = y . right :

6 x := y

7 y := y . parent

8 return y

Se il sottoalbero destro del nodo x non `e vuoto, allora il successore di x `e proprio il nodo pi`u a

sinistra nel sottoalbero destro, che viene trovato chiamando la procedura precedentemente analizzata

treeMinimum. Altrimenti, se il sottoalbero destro del nodo x`e vuoto e x ha un successore y, allora y `e

l’antenato pi`u prossimo di xil cui figlio sinistro `e anche antenato di x. Per trovare il nodo y, `e necessario

risalire l’albero partendo da x, fino a quando non si trova un nodo che `e figlio sinistro di suo padre.

Questa operazione `e svolta in un tempo O(h), con h l’altezza dell’albero.

La procedura per trovare il successore `e simmetrica alla procedura appena anlizzata e viene svolta

nello stesso tempo.

Inserimento Per inserire un nuovo valore v all’interno dell’albero binario di ricerca T, si utilizza la

seguente procedura, che riceve in input un nodo z, tale per cui z.key= v:

1 tr ee In se rt (T , z ) :

2 y := NIL

3 x := T . root

4 w h i l e x != NIL :

5 y := x

6 i f z . key < x . key :

7 x := x . left

8 e l s e :

9 x := z . right

10 z . parent := y

11 i f y = NIL :

12 T . root = z

13 e l s e i f z . key < y . key :

14 y . left := z

15 e l s e :

16 y . right := z

La procedura appena vista inizia dalla radice dell’albero e il puntatore xtraccia un cammino semplice

in discesa cercando un NIL da sostituire con l’elemento di input z. La procedura mantiene anche un

puntatore ydetto inseguitore che punta sempre al padre di x. Le righe 4-9 del ciclo while spostano questi

due puntatori verso il basso, andando a sinistra o a destra a seconda dell’esito del confronto fra z.key e

x.key, finch`e a x non viene assegnato il valore NIL. A questo punto si rende necessario il puntatore y

perch`e, quando si arriva a trovare il valore NIL da sostituire con il nodo z, la ricerca `e andata un passo9.5. ALBERI BINARI 73

oltre il nodo che deve essere modificato. Le righe successive inseriscono il nodo passato come argomento

all’interno dell’albero binario di ricerca. In generale, questo algoritmo viene eseguito in un tempo O(h),

in un albero di altezza h.

Cancellazione suddivide in tre casi:

La procedura per la cancellazione di un nodo z da un albero binario di ricerca si

1. se il nodo z non ha figli, si modifica il nodo z.parent in modo che non punti pi`u a z, ma a NIL;

2. Se il nodo z ha un solo figlio, si eleva il figlio di tale nodo in modo che occupi la posizione di z

nell’albero, modificando il padre di z affinch`e punti al figlio di z;

3. Se il nodo zha due figli, si trova prima di tutto il successore ydi z, che deve necessariamente trovarsi

nel sottoalbero destro di z, per poi fare in modo che yassuma la posizione di znell’albero. La parte

restante del sottoalbero destro originale diventa il nuovo sottoalbero destro di y e il sottoalbero

sinistro di z diventa il nuovo sottoalbero sinistro di y.

Per poter spostare i sottoalberi all’interno dell’albero binario di ricerca si deve prima definire una

procedura che sostituisca il sottoalbero figlio di suo padre con un altro sottoalbero. Questa procedura

sosituisce il sottoalbero con radice nel nodo u con il sottoalbero con radice nel nodo v, in modo che il

padre del nodo u diventa il padre del nodo v. In pseudocodifica:

1 tr an sp la nt (T , u , v ) :

2 i f u . parent = NIL :

3 T . root := v

4 e l s e i f u = u . parent . left :

5 u . parent . left := v

6 e l s e :

7 u . parent . right := v

8 i f v != NIL :

9 v . parent := u . parent

Una volta introdotto questo algoritmo, `e possibile ora analizzare la procedura di eliminazione:

1 tr ee De le te (T , z ) :

2 i f z . left = NIL :

3 tr an sp la nt (T , z , 4 e l s e i f z . right = NIL :

5 tr an sp la nt (T , z , z . right )

z . left )

6 e l s e :

7 y := t r e e M i n i m u m ( z . right )

8 i f y . parent != z :

9 tr an sp la nt (T , y , y . right )

10 y . right := z . right

11 y . right . parent := y

12 tr an sp la nt (T , z , y )

13 y . left := z . left

14 y . left . parent := y

Questa procedura gestisce i tre casi analizzati precedentemente. Le righe 2-3 gestiscono il caso in cui

il nodo z non ha figlio sinistro, le righe 4-5 gestiscono il caso in cui il nodo z ha un figlio sinistro, ma non

un figlio destro, mentre le restanti righe gestiscono il caso in cui il nodo ha sia figlio destro che sinistro.

Nello specifico, la riga 7 trova il nodo y, successore di z: poich`e z ha un sottoalbero destro non vuoto, il

suo successore deve essere il nodo di quel sottoalbero con la chiave pi`u piccola (per questo motivo viene

invocata la procedura treeMinimum). Come gi`a detto, y non ha figlio sinistro, quindi bisogna staccare

y dalla sua posizione corrente e metterlo al posto di z. Se y `e figlio destro di z, le ultime tre righe

sostituiscono z con y, per poi sostituire il figlio sinistro di y con il figlio sinistro di z. Se y non `e figlio

sinistro di z, le righe 9-11 sostituiscono y con il figlio destro di y e cambiano il figlio destro di z nel figlio

destro di y. Tale procedura richiede un tempo di esecuzione nell’ordine di O(h), in un albero binario di

ricerca alto h.74 CAPITOLO 9. STRUTTURE DATI

9.6 Alberi Red Black

Gli alberi rosso nero sono strutture dati ad albero di ricerca binaria con un bit aggiuntivo di memoria per

ogni nodo, che rappresenta il colore di tale nodo. Questa struttura dati, garantisce che nessun cammino

semplice dalla radice dell’albero fino ad una sua qualsiasi foglia si pi`u lungo del doppio di qualsiasi

altro cammino: si dice, quindi, che l’albero `e approssimativamente bilanciato. Ogni nodo dell’albero

contiene ora gli attributi key, left, right, parent e color. Se un nodo non contiene riferimenti a

figli o al nodo padre, il corrispondente attributo viene inizializzato con il valore NIL. In questo caso,

i puntatori a NIL vengono trattati come puntatori a nodi (vuoti) esterni dell’albero, mentre i nodi che

contengono informazioni sono trattati come nodi interni all’albero: dunque, tutte le foglie dell’albero

sono nodi che non contengono nessuna informazione. In realt`a, per semplificare le condizioni al contorno

nello pseudocodice, si `e soliti utilizzare un unico nodo sentinella inizializzato a NIL, in modo che per ogni

albero T, le sue foglie puntano al nodo T.nil di color nero.

I nodi dell’albero rosso nero vengono colorati tramite le seguenti regole:

1. Ogni nodo `e rosso o nero;

2. La radice `e nera;

3. Ogni foglia (vuota - NIL) `e nera;

4. Se un nodo `e rosso, allora entrambi i suoi figli sono neri;

5. Per ogni nodo, tutti i cammini semplici, che vanno dal nodo alle sue foglie discendenti, contengono

lo stesso numero di nodi neri.

Si definisce a questo proposito, altezza nera di un nodo x, indicato con bh(x), il numero di nodi neri

lungo un cammino semplice che inizia dal nodo x(non incluso). Per la propriet`a degli alberi rosso nero,

il concetto di altezza nera `e ben definito in quanto tutti i cammini semplici che scendono dal nodo hanno

lo stesso numero di nodi neri. In generale:

Teorema 9.6.1. L’altezza massima di un albero rosso nero con n nodi `e 2 log2(n+ 1).

La conseguenza immediata di questo teorema `e che le operazioni sugli insiemi dinamici possono tutte

essere implementate in un tempo O(log2 n) negli alberi rosso neri, perch`e possono essere eseguite nel

tempo O(h) in un albero binario di ricerca di altezza he qualsiasi albero rosso nero di nnodi `e un albero

binario di ricerca di altezza O(log2 n).

Rotazione Le operazioni di treeInsert e treeDelete sugli alberi rosso nero, potrebbero violare le

propriet`a della struttura, proprio perch`e modificano l’albero. Si rende quindi necessario ricalcolare i

colori di qualche nodo dell’albero e anche la struttura dei puntatori, dopo la chiamata a una delle due

procedure. La struttura dei puntatori viene modificata tramite una rotazione, ovvero un’operazione

locale che preserva le propriet`a degli alberi binari di ricerca. Quando si esegue una rotazione sinistra in

un nodo x, supponendo che il nodo y= x.right sia diverso da NIL, si fa ”perno” sul collegamento tra x

e y: il nodo ydiventa la nuova radice del sottoalbero, con x come figlio sinistro di y e il figlio sinistro di

y come figlio destro di x. In pseudocodifica:

1 le ft Ro ta te (T , x ) :

2 y := x . right

3 x . right := y . left

4 i f y . left != T . nil :

5 y . left . parent := x

6 y . parent := x . parent

7 i f x . parent = T . nil :

8 T . root := y

9 e l s e i f x = x . parent . left :

10 x . parent . left := y

11 e l s e :

12 x . parent . right := y

13 y . left := x

14 x . parent := y9.6. ALBERI RED BLACK 75

Il codice per la procedura rightRotate `e simmetrico a quello appena analizzato. Entrambe le

procedure vengono eseguite nel tempo O(1).

Inserimento L’inserimento di un nodo in un albero rosso nero viene eseguito tramite una versione

leggermente modificata della procedura di inserimento analizzata per gli alberi binari di ricerca. Inoltre,

per poter preservare le condizioni degli alberi rosso neri, `e necessario utilizzare una seconda procedura

che ricolora i nodi dell’albero in seguito alla chiamata della procedura di inserimento. In pseudocodifica:

1 RBInsert (T , z ) :

2 y := T . nil

3 x := T . root

4 w h i l e x != T . nil :

5 y := x

6 i f z . key < x . key :

7 x := x . left

8 e l s e :

9 x := x . right

10 z . parent := y

11 i f y = T . nil :

12 T . root := z

13 e l s e i f z . key < y . key :

14 y . left := z

15 e l s e :

16 y . right := z

17 z . left := T . nil

18 z . right := T . nil

19 z . color = RED

20 RBFixup (T , z )

Dunque, tramite questa procedura, il nodo z viene inserito nella posizione corretta all’interno dell’al-

bero rosso nero, inizializzando gli attributi left eright a NIL (per rispettare la struttura dell’albero)

e il suo colore a rosso. Dato che l’inserimento di questo nodo potrebbe aver causato la violazione del-

le propriet`a fondamentali degli alberi rosso neri, viene chiamata la procedura di ripristino RBFixup,

implementata con la seguente pseudocodifica:

1 R B I n s e r t F i x u p (T , z ) :

2 w h i l e z . parent . color = RED :

3 i f z . parent = z . parent . parent . left :

4 y := z . parent . parent . right

5 i f y . color = RED :

6 z . parent . color := BLACK 7 y . color := BLACK // caso 1

8 z . parent . parent . color := RED 9 z := z . parent . parent // caso 1

// caso 1

// caso 1

10 e l s e :

11 i f z = z . parent . right :

12 z := z . parent // caso 2

13 le ft Ro ta te (T , z ) 14 z . parent . color := BLACK 15 z . parent . parent . color := RED 16 r i g h t R o t a t e (T , z . parent . parent ) // caso 2

// caso 3

// caso 3

// caso 3

17 e l s e :

18 come righe 4 -16 con " left " e " right " scambiati

19 T . root . color := BLACK

Una volta chiamata la funzione di inserimento, sicuramente la propriet`a 1 (ogni nodo `e rosso o nero)

e la propriet`a 3 (ogni foglia `e nera) sono rispettate in quanto i figli del nodo rosso appena inserito

sono T.nil. Anche la propriet`a 5 (per ogni nodo, tutti i cammini semplici che vanno dal nodo alle sue

foglie discendenti contengono lo stesso numero di nodi neri) `e rispettata proprio perch`e il nodo inserito76 CAPITOLO 9. STRUTTURE DATI

nell’albero `e di color rosso. Le uniche due propriet`a che potrebbero non essere rispettate sono la 2 (la

radice `e nera) e la 4 (se un nodo `e rosso, allora entrambi i suoi figli sono neri). Entrambe le possibili

violazioni sono dovute al fatto che il nodo inserito viene colorato di rosso: infatti, se l’albero `e vuoto, il

nodo viene inserito alla radice violando la propriet`a 2, mentre se il padre del nodo inserito `e rosso, viene

violata la propriet`a 4.

Dunque, nel caso ci fossero violazioni delle propriet`a degli alberi rosso nero, ce ne sarebbe solo una

e riguarderebbe le due propriet`a di cui si `e appena discusso. Esistono 3 casi possibili, segnati anche

all’interno dello pseudocodice nei commenti, per la ricolorazione dei nodi:

Caso 1 Lo zio y di z `e rosso: il caso 1 (righe 6-9) viene eseguito quando z.parent e y sono entrambi rossi.

Poich`e z.parent.parent`e nero, `e possibile colorare di nero z.parent e y risolvendo il problema per

cui z e z.parent sono entrambi rossi. Si ricolora poi di rosso z.parent.parent per conservare la

propriet`a 5 e si ripete il ciclo while con z.parent.parent come nuovo nodo z.

Caso 2 Lo zio y di z `e nero e z `e figlio destro: nel caso 2 (righe 12-13), lo zio di z `e di colore nero e il

nodo z `e figlio destro. In questo caso `e necessaria una semplice rotazione a sinistra per riportarsi

immediatamente al caso 3. Una rotazione del genere non influisce n`e sull’altezza dell’albero n`e

sulla propriet`a 5.

Caso 3 Lo zio y di z `e nero e z `e figlio sinistro: nel caso 3 (righe 14-16), lo zio di z `e sempre nero, ma

il nodo z `e figlio sinistro anzich`e destro. In questo caso si applicano alcune modifiche sui colori e

alcune rotazioni aggiuntive a destra per poter preservare le propriet`a degli alberi rosso nero.

Rimozione La procedura di rimozione di un determinato nodo dall’albero rosso nero si basa sulla

subroutine transplant, che deve essere opportunamente modificata in modo da adattarsi alla struttura

degli alberi rosso nero. In pseudocodifica:

1 R B T r a n s p l a n t (T , u , v ) :

2 i f u . parent = T . nil :

3 T . root := v

4 e l s e i f u = u . parent . left :

5 u . parent . left := v

6 e l s e :

7 u . parent . right := v

8 v . parent := u . parent

Una volta introdotta questa procedura, `e possibile analizzare l’algoritmo di rimozione, simile a quella

analizzata per gli alberi di ricerca binaria, con l’unica differenza che si tiene traccia del nodo y, che

potrebbe violare le propriet`a degli alberi rosso nero. Per evitare tali violazioni, si utilizza una seconda

procedura di supporto che ha il compito di ricalcolare i colori dell’albero, in modo da rispettare le sue

propriet`a. In pseudocodifica:

1 RBDelete (T , z ) :

2 y := z

3 y O r i g i n a l C o l o r := y . color

4 i f z . left = T . nil :

5 x := z . right

6 R B T r a n s p l a n t (T , z , z . right )

7 e l s e i f z . right = T . nil

8 x := z . left

9 R B T r a n s p l a n t (T , z , z . left )

10 e l s e :

11 y := t r e e M i n i m u m ( z . right )

12 y O r i g i n a l C o l o r := y . color

13 x := y . right

14 i f y . parent = z :

15 x . parent := y

16 e l s e :

17 18 R B T r a n s p l a n t (T , y . right := z . right

y , y . right )9.7. GRAFI 77

19 20 21 22 23 24 25 i f y . right . parent := y

R B T r a n s p l a n t (T , z , y )

y . left := z . left

y . left . parent := y

y . color := z . color

y O r i g i n a l C o l o r = BLACK :

R B D e l e t e F i x u p (T , x )

1 R B D e l e t e F i x u p (T , x ) :

2 w h i l e x != T . root and x . color = BLACK :

3 i f x = x . parent . left :

4 w := x . parent . right

5 i f w . color = RED :

6 w . color := BLACK // caso 1

7 x . parent . color := RED 8 le ft Ro ta te (T , x . parent ) 9 w := x . parent . right // caso 1

// caso 1

// caso 1

10 i f w . left . color = BLACK and w . roght . colr = BLACK :

11 w . color := RED // caso 2

12 x := x . parent // caso 2

13 e l s e :

14 i f w . right . color = BLACK :

15 w . left . color = BLACK 16 w . color = RED // caso 3

17 r i g h t R o t a t e (T , w ) 18 w := x . parent . right 19 w . color := x . parent . color 20 x . parent . color := BLACK 21 w . right . color := BLACK 22 le ft Ro ta te (T , x . parent ) // caso 3

// caso 3

// caso 3

// caso 4

// caso 4

// caso 4

// caso 4

23 x := T . root // caso 4

24 e l s e :

25 come righe 4 -23 con " left " e " right " scambiati

26 x . color := BLACK

9.7 Grafi

Un grafo G `e una coppia (V,E), in cui V `e l’insieme finito dei vertici del grafo, mentre E `e l’insieme

degli archi di G. Un arco `e una relazione binaria su V che collega due vertici detti adiacenti: se un arco e

connette due vertici ue v, allora pu`o essere rappresentato come la coppia (u,v) dei vertici che connette.

Da questo si ottiene che l’insieme E ⊆V2 e quindi che 0 ≤|E|≤|V|2

.

Esistono due tipologie di grafi, ovvero i grafi orientati e non orientati. Un grafo si dice non orientato

quando la coppia (u,v) `e la stessa di (v,u) e non c’`e quindi la nozione di direzione da un nodo all’altro.

D’altra parte, in un grafo orientato, la coppia (u,v) `e differente dall’arco (v,u), in quanto si tiene conto

della direzione di attraversamento.

9.7.1 Rappresentazione

Esistono due metodi principali per la rappresentazione dei grafi: la prima consiste in una collezione di

liste di adiacenza, mentre la seconda in una matrice di adiacenza. Entrambi i metodi possono essere

applicati sia ai grafi orientati che non orientati.

Rappresentazione con liste di adiacenza Tale rappresentazione di un grafo G = (E,V) consiste

in un array Adj di |V|liste concatenate, una per ogni vertice V. Per ogni u ∈V, la lista di adicenza

Adj[u] include tutti i vertici adiacenti a u in G. Poich`e le liste di adiacenza rappresentano gli archi di

un grafo, nello pseudocodice si tratta l’array Adj come un attributo del grafo G.78 CAPITOLO 9. STRUTTURE DATI

Inoltre, Se G`e un grafo orientato, la somma delle lunghezze di tutte le liste di adiacenza `e esattamente

|E|, perch`e un arco nella forma (u,v) `e rappresentato inserendo v in G.Adj[u]. Al contrario, se G `e un

grafo non orientato, la somma delle lunghezze di tutte le liste di adiacenza `e 2|E|, perch`e se (u,v)

rappresenta un arco non orientato, allora u appare nella lista di adiacenza di v e viceversa. Per i grafi

orientati e non, la rappresentazione con liste di adiacenza ha la propriet`a di occupare una quantit`a di

memoria Θ(V + E).

Lo svantaggio principale di questo metodo di rappresentazione risiede nel fatto che il metodo di ricerca

`e abbastanza inefficiente: infatti, per poter determinare se un determinato arco (u,v) `e presente nel grafo,

`e necessario cercare v nella lista di adiacenza G.Adj[u], operazione che richiede un tempo lineare.

Rappresentazione con matrice di adiacenza Tale rappresentazione di un grafo G= (E,V) consiste

in una matrice A= (aij) di dimensione |V|×|V|tale per cui:

ai,j=

1 if (i,j) ∈E

0 else

Per poter procedere con tale rappresentazione, `e prima necessario che i vertici siano numerati in

maniera arbitraria da 1 a |V|. Si noti che, la matrice di adiacenza Aper un grafo non orientato `e uguale

alla sua trasposta AT, per la propriet`a principale dei grafi non orientati, per cui (u,v) = (v,u).

Lo svantaggio maggiore nell’impiego di una matrice di adiacenza `e l’utilizzo intensivo di memoria,

nell’ordine di Θ(|V|2). Nonostante questo, per grafi di dimensione relativamente piccole, si preferisce

utilizzare questo metodo a quello precedente, per la sua semplicit`a di utilizzo. In generale conviene

utilizzare il metodo delle liste di adiacenza quando |E|̸= Θ(|V|2), cio`e quando il grafo `e sparso (ovvero

quando il numero di nodi connessi non `e molto grande), mentre se il grafo `e completo (ovvero quando

ogni nodo `e connesso con i restanti), conviene utilizzare una matrice di adiacenza.

9.7.2 Visita in Ampiezza

La visita in ampiezza (o breadth-first search) `e l’algoritmo pi`u semplice di ricerca nei grafi. Dato un

grafo G`e un vertice distinto s, detto sorgente, la visita in ampiezza ispeziona sistematicamente gli archi

di G per scoprire tutti i vertici che sono raggiungibili da s, calcolando la distanza da s a ciascun vertice

raggiungibile. L’algoritmo `e cos`ı chiamato perch`e espande la frontiera fra i vertici scoperti e quelli ancora

da scoprire in maniera uniforme lungo l’ampiezza della frontiera: l’algoritmo, infatti, scopre tutti i vertici

che si trovano a distanza k da s, prima di scoprire tutti i ivertici che si trovano a distanza k+ 1.

Per tenere traccia del lavoro, la visita colora i vertici di bianco, grigio oppure nero. Inizialmente,

tutti i vertici sono di colore bianco e possono diventare grigi e poi neri. Un vertice viene scoperto quando

viene incontrato per la prima volta durante la visita, cessando di essere bianco. Tutti i vertici adiacenti

ai vertici neri sono di colore grigio, il che significa che sono stati scoperti dall’algoritmo. I vertici grigi,

invece, potrebbero presentare alcuni vertici adiacenti bianchi, che rappresentano la frontiera da scoprire:

tali vertici sono tenuti in memoria in una coda (gestita dalla politica FIFO) e, ad ogni iterazione, si

elimina dalla coda un elemento u, visitando i vertici a lui adiacenti che sono ancora bianchi. Si noti che,

se u.dist`e la distanza del vertice u da s, allora la distanza dei nodi bianchi adiacenti ad u`e u.dist+ 1.

In pseudocodifica:

1 b r e a d t h F i r s t S e a r c h (G , s ) :

2 f o r each u in G . V - { s }:

3 u . color := WHITE

4 u . dist := ∞

5 s . color := GRAY

6 s . dist := 0

7 Q := ∅

8 enqueue (Q , s )

9 w h i l e Q != ∅:

10 u := dequeue ( Q )

11 f o r each v in u . Adj :

12 i f v . color = WHITE :

13 v . color := GRAY

14 v . dist := u . dist + 1

15 enqueue (q , v )

16 u . color := BLACK9.7. GRAFI 79

Informalmente, le righe 2-4 inizializzano ogni vertice, colorandolo di bianco, eccetto il vertice s che

in riga 5 viene colorato di grigio, in quanto `e il vertice sorgente gi`a visitato ad inizio ricerca, e a cui

viene assegnata la distanza 0. Le righe 7 e 8 inizializzano la coda Q inserendo il solo vertice s. Il ciclo

while di riga 10-16 viene reiterato fin tanto che ci sono ancora vertici grigi, la cui frontiera protrebbe

ancora presentare vertici di colore bianco. La riga 10 determina il vertice grigio u che si trova in testa

alla coda, rimuovendolo dalla coda stessa (dequeue), in modo da poter accedere ai suoi vertici adiacenti.

Il ciclo for, di righe 11-15, esamina ciascun vertice v della lista di adiacenza di u: se questo vertice `e

bianco, allora non `e ancora stato scoperto e, quindi, l’algoritmo lo colora di grigio e lo inserisce nella

coda dopo avergli assegnato il valore di distanza u.dist+ 1. Dopo aver esaminato ogni vertice nella lista

di adiacenza di u, tale vertice viene colorato di nero in riga 16.

Dato un grafo G= (V,E), il tempo di esecuzione dell’algoritmo BFS `e O(|E|+ |V|).

9.7.3 Visita in Profondit`a

La visita in profondit`a (o depth-first search) `e un algoritmo che adotta una strategia differente rispetto

al precedente: consiste, infatti, nel visitare il grafo sempre pi`u in profondit`a se possibile. Nella visita in

profondit`a, gli archi vengono ispezionati a partire dall’ultimo vertice v scoperto, che ha ancora archi non

ispezionati nella sua lista di adiacenza. Questo processo continua fino a quando non sono stati scoperti

tutti i vertici che sono raggiungibili dal vertice vda cui inizia la ricerca. Se rimane ancora qualche vertice

da ispezionare, allora se ne sceglie uno nuovo come sorgente e si reitera il processo.

Dunque, si pu`o affermare che se l’algoritmo BFS si basa sulla strategia di visitare i vertici secondo

una politica LIFO, l’algoritmo DFS si basa su una politica di tipo FIFO: una volta inserito un nodo in

cima alla pila, si visitano tutti i vertici adiacenti relativi a quel nodo, prima di procedere alla visita dei

vertici adiacenti del successivo.

Come per il precedente algoritmo, anche in questo caso i vertici vengono colorati durante la loro

visita, per indicarne lo stato. Inizialmente tutti i vertici sono colorati di bianco e nel momento in cui un

determinato vertice viene visitato per la prima volta, questo viene colorato di grigio. Infine, un vertice

`e colorato di nero nel momento in vui sono ispezionati tutti i suoi vertici adiacenti. Oltre alla lista

di adiacenza e al colore, i vertici all’interno di un grafo visitato in profondit`a, contengono anche due

informazioni temporali: la prima, memorizzata in v.d, registra il momento in cui il vertice viene scoperto

e colorato di grigio, mentre le seconda, memorizzata in v.f, registra il momento in cui la visita completa

l’ispezione della lista di adiacenza di v e viene colorato di nero. Quindi, un vertice v `e bianco prima del

tempo v.d, grigio fra il tempo v.d e v.f, nero successivamente. Queste informazioni aggiuntive servono

per agevolare la scrittura di procedure e sono utilizzate anche da parte di algoritmi pi`u avanzati.

Si introduce di seguito la procedura in pseudocodifica che realizza la strategia di visita in profondit`a:

1 d e p t h F i r s t S e a r c h ( G ) :

2 f o r each u in G . V :

3 u . color := WHITE

4 time := 0

5 f o r each u in G . V :

6 i f u . color = WHITE :

7 DFSVisit (G , u )

La procedura imposta, in righe 2-3, il colore di tutti i vertici di bianco, per poi inizializzare una

variabile globale time,tramite cui si memorizzano le informazioni temporali precedentemente discusse.

Le righe successive servono ad ispezionare in profondit`a tutti i vertici che hanno colore bianco, tramite

la procedura di supporto DFSVisit, introdotta di seguito.

1 DFSVisit (G , u ) :

2 time := time + 1

3 u . d := time

4 u . color := GREY

5 f o r each v in G . Adj [ u ]:

6 i f v . color = WHITE :

7 DFSVisit (G , v )

8 u . color := BLACK

9 time := time + 1

10 u . f := time80 CAPITOLO 9. STRUTTURE DATI

In ogni chiamata della procedura DFSVisit, il vertice upassato come argomento `e inizialmente bianco,

quindi gli si assegna subito il colore grigio dopo aver assegnato al vertice il tempo di scoperta (u.d) il

tempo incrementato di una unit`a (righe 2-4). Subito dopo, il ciclo for di righe 5-7 esplora tutti i vertici

v di colore bianco adiacenti ad ue chiama ricorsivamente la procedura in modo da visitare il vertice v e

i vertici a lui adiacenti, sempre se di colore bianco. Dopo aver terminato la visita in profondit`a di tutti

i vertici a partire dal vertice sorgente u, il colore di tale vertice viene cambiato in nero e si assegna al

tempo di fine esplorazione u.f il valore temporale, dopo averlo nuovamente incrementato di una unit`a

(righe 8-10).

Anche in questo caso, come per il procedimento precedente, il tempo medio di esecuzione dell’algo-

ritmo di ispezione in profondit`a `e Θ(|V|+ |E|).

9.7.4 Ordinamento Topologico

La visita in profondit`a pu`o essere utilizzata per eseguire l’ordinamento topologico di un determinato

grafo orientato aciclico (detto anche DAG - Directed Acyclic Graph). Un ordinamento topologico di un

dag G = (V,E) `e un ordinamento lineare di tutti i suoi vertici, tale che se G contiene un arco (u,v),

allora u appare prima di v nell’ordinamento. Un ordinamento topologico di un grafo pu`o essere visto

come un ordinamento dei suoi vertici lungo una linea orizzontale ion modo che tutti gli archi orientati

siano diretti da sinistra verso destra: intuitivamente, questo tipo di ordinamento, serve a rappresentare

la precedenza di determinati eventi.

In pseudocodifica:

1 t o p o l o g i c a l S o r t ( G ) :

2 L := ∅

3 f o r each u in G . V :

4 u . color := WHITE

5 f o r each u in G . V :

6 i f u . color = WHITE :

7 t o p o l o g i c a l S o r t V i s i t (L , 8 return L

u )

1 t o p o l o g i c a l S o r t V i s i t (L , u ) :

2 u . color := GRAY

3 f o r each v in G . Adj [ u ]

4 i f v . color = WHITE :

5 t o p o l o g i c a l S o r t V i s i t (L , 6 x . key := u

7 li st In se rt (L , x )

8 u . color := BLACK

v )

L’idea di questo algoritmo `e quella di visitare il dag con l’algoritmo di vista DFS e, quando un vertice

viene colorato di nero, lo si inserisce in testa alla lista Lche rappresenta tutti i nodi ordinati. Una volta

completata la visita di ogni vertice, la lista ottenuta rappresenta l’ordinamento topologico del grafo.

Anche in questo caso, l’algoritmo impiega un tempo di esecuzione medio Θ(|V|+ |E|).