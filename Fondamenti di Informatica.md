
L’informatica è una scienza, ovvero una conoscenza  sistematica di tecniche e metodi per rappresentare ed elaborare l’informazione. È inoltre costituita da una collezione strutturata di 
dati (osservazioni, fatti, entità fisiche o concettuali) che rappresentano una parte del mondo reale.
	CALCOLATORE = strumento elettronico che elabora informazione, che esegue un algoritmo (o un insieme di algoritmi) ed utilizza elementi di memoria per immagazzinare le informazioni che sta elaborando;![[Pasted image 20251029170852.png]]	
# Algoritmi

- ALGORITMO = sequenza finita di passi non ambigui e comprensibili da un esecutore per permettere di risolvere un problema;
	- Flusso di CONTROLLO = descrizione a priori di tutte le possibili sequenze dei passi algoritmici; il flusso di controllo di un diagramma di flusso viene costruito mediante specifiche regole:
		- Un solo blocco di inizio
		- Almeno un blocco di terminazione (preferibilmente uno)
		- Non si può lasciare sconnessa alcuna freccia in ingresso o in uscita di un 
		- qualsiasi altro blocco
	 Il flusso di controllo di un algoritmo viene costruito in base a tre strutture di controllo dette: 
		- SEQUENZA![[Pasted image 20251029172250.png]]
		- SELEZIONE![[Pasted image 20251029172346.png]]
		- ITERAZIONE
			- Ciclo a condizione FINALE (il corpo del ciclo è eseguito almeno una volta):![[Pasted image 20251029172743.png]]
			- Ciclo a condizione INIZIALE (il corpo del ciclo è eseguito zero o più volte):![[Pasted image 20251029172813.png]]
		Teorema di Jacopini e Böhm: formulato nel 1966 dagli informatici italiani Corrado Böhm e Giuseppe Jacopini, afferma che qualsiasi algoritmo può essere espresso utilizzando unicamente le tre strutture di controllo fondamentali (sequenza, selezione ed iterazione);
	- Flusso di ESECUZIONE = sequenza di operazioni effettivamente seguita in esecuzione;
	- Elementi grafici:![[Pasted image 20251029171350.png]]

- VARIABILE = contenitore di valori, a cui è sempre associato un valore alla volta, non può essere vuota (al massimo non è inizializzata e quindi contiene un valore “a caso”), è collocata in una riga della memoria, è identificata tramite un nome simbolico. Le operazioni descritte nell’algoritmo possono essere eseguite di volta in volta sui diversi valori assegnati alle variabili (formulazione generale dell’algoritmo); possiamo eseguire due operazioni su una variabile:
	- Lettura: recuperiamo il valore contenuto
	- Scrittura: salviamo un nuovo valore

# Conversioni binarie

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
- 