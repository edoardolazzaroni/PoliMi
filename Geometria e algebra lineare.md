

# Capitolo I: Vettori nel piano e nello spazio


Il concetto di vettore, fondamentale sia in matematica che nelle applicazioni (fisiche, ecc.), può essere introdotto a vari livelli di astrazione. In questa sezione di occuperemo di vettori nel piano e nello spazio: in questo contesto, è possibile dare una definizione geometrica elementare di vettore; molte grandezze fisiche (velocità, accelerazione, forza,...) si rappresentano in questo modo. In seguito vedremo come la nozione di vettore si possa generalizzare in termini astratti, ottenendo un concetto più flessibile, che risulta molto utile per l'algebra, il calcolo infinitesimale e le loro applicazioni.

### **1.1 Operazioni fondamentali sui vettori**

- Un vettore nel piano o nello spazio è individuato assegnando:
	a) un numero reale non negativo che esprime la sua **lunghezza** o **modulo** o intensità;
	b) una **direzione**, individuata da una retta (rette *parallele* individuano la stessa direzione);
	c) un **verso**.

Geometricamente, possiamo pensare ai vettori come a segmenti orientati, con la precisazione che due segmenti orientati che possano ottenersi l'uno dall'altro per traslazione sono lo stesso vettore.
Se nello spazio è fissato un sistema di riferimento cartesiano di cui $O$ è l'origine, possiamo anche vedere i vettori come frecce uscenti da $O$.



*Vettori come frecce uscendi da $O$. $\overrightarrow{OA}$ e $\overrightarrow{PQ}$ rappresentano lo strsso vettore applicato in due punti diversi dello spazio*

La direzione ed il verso del vettore sono allora quelli indicati dalla freccia corrispondente mentre il suo modulo coincide con la lunghezza della freccia. Per indicare un vettore potremo usare una lettera in grassetto (come **v, w**,...) oppure il simbolo $\overrightarrow{OA}$ se $A$ è la punta della freccia. Si dice anche che $\overrightarrow{OA}$ è il vettore posizione del punto A.
Due punti fissati $P$ e $Q$, nell'ordine, individuano un vettore con direzione coincidente con quella della retta passante per $P$ e $Q$, con verso da $P$ a $Q$ e con modulo pari alla lunghezza del segmento $PQ$. Il vettore individuato dai due punti $P$ e $Q$ coincide col vettore rappresentato dalla freccia $\overrightarrow{OA}$ che si ottine traslando parallelamente il segmento $PQ$ fino a far coincidere $P$ con $O$ e $Q$ con $A$; per il vettore così rappresentato si può anche usare il simbolo $\overrightarrow{PQ}$.
Sottolineiamo però che $\overrightarrow{OA}$ e $\overrightarrow{PQ}$ sono due rappresentazioni diverse dello stesso vettore **v**, una volta applicato in $O$, un'altra applicato in $P$.

- Il modulo di un vettore $\mathbf{v}$ sarà indicato con $\left | \mathbf{v} \right |$.
- Il vettore di modulo $0$ si chiama **vettore nullo** e sarà indicato con $\mathbf{0}$.

Sui vettori si possono definire varie operazioni: cominciamo ad introdurre le due fondamentali, ovvero la <u>SOMMA di VETTORI</u> ed il <u>PRODOTTO di un VETTORE per uno SCALARE</u>;

- **Somma di vettori**. Dati due vettori $\mathbf{v}=\overrightarrow{OA}$ e $\mathbf{w}=\overrightarrow{OB}$, la loro somma è definita al seguente modo: si applica $\mathbf{w}$ in $A$, cioè si scrive $\mathbf{v}=\overrightarrow{AC}$ con $C$ opportuno; allora $\mathbf{v}+\mathbf{w}=\overrightarrow{OC}$. Ne segue che $\mathbf{v}+\mathbf{w}$ si può ottenere con la ben nota regola del parallelogramma: il vettore $\mathbf{v}+\mathbf{w}$ è la diagonale del parallelogramma costruito su $\mathbf{v}$ e $\mathbf{w}$, come in figura.
	Si noti che il segmento orientato associato a $\mathbf{v}+\mathbf{w}$ è contenuto nel piano dei segmenti orientati associati a $\mathbf{v}$ e $\mathbf{w}$.



**PROPRIETÀ**:
	a) <mark class="hltr-yellow">Associativa</mark>: $(\mathbf{u}+\mathbf{v})+\mathbf{w}=\mathbf{u}+(\mathbf{v}+\mathbf{w})$
	b) <mark class="hltr-yellow">Commutativa</mark>: $\mathbf{u}+\mathbf{v}=\mathbf{v}+\mathbf{u}$
	c) <mark class="hltr-yellow">Vettore nullo</mark> ($\mathbf{0}$): $\mathbf{v}+\mathbf{0}=\mathbf{v}$
	d) <mark class="hltr-yellow">Vettore opposto</mark> ($-\mathbf{v}$): $\mathbf{v}+(-\mathbf{v})=0$

La somma $\mathbf{v}+(-\mathbf{w})$ si scrive semplicemente $\mathbf{v}-\mathbf{w}$, definendo in tal modo la <u>differenza tra due vettori</u>.



Le proprietà appena enunciate possono essere dimostrate geometricamente, in base alla definizione di somma.
Per esempio, la prorietà commutativa dipende dal fatto che in un parallelogramma i lati opposti sono uguali e paralleli; da questo discende che $\mathbf{v}=\overrightarrow{OA}=\overrightarrow{BC}$, $\mathbf{w}=\overrightarrow{OB}=\overrightarrow{AC}$, perciò:
						$\mathbf{v}+\mathbf{w}=\overrightarrow{OA}+\overrightarrow{AC}=\overrightarrow{OC}$
						$\mathbf{w}+\mathbf{v}=\overrightarrow{OB}+\overrightarrow{BC}=\overrightarrow{OC}$

e quindi $\mathbf{v}+\mathbf{w}=\mathbf{w}+\mathbf{v}$.

Con un ragionamento geometrico analogo si può dimostrare la proprietà associativa. Le proprietà del vettore nullo e dell'opposto sono immediate.

- **Moltiplicazione di un vettore per uno scalare**. Se $\mathbf{v}$ è un vettore e $t$ è uno scalare (cioè un numero reale) il prodotto di $t$ per $\mathbf{v}$, indicato con $t\mathbf{v}$, è definito come il vettore che ha lunghezza $\left|t\right|\cdot\left|\mathbf{v}\right|$, ha la direzione di $\mathbf{v}$ e lo stesso verso se $t>0$, verso opposto se $t<0$.



**PROPRIETÀ**:
	a) $1\cdot\mathbf{v}=\mathbf{v}$
	b) $s(t\mathbf{v})=(st)\mathbf{v}$
	c) $t(\mathbf{v}+\mathbf{w})=t\mathbf{v}+t\mathbf{w}$
	d) $(s+t)\mathbf{v}=s\mathbf{v}+t\mathbf{v}$
	(con $s,t\in\mathbb{R}$)

Anche queste proprietà hanno una dimostrazione geometrica.
Per esempio, per provare la terza, si consideri la figura successiva: i triangoli $OAB$, $OCD$ sono simili per il Teorema di Talete, perchè $AB$ e $CD$ sono paralleli (rappresentando i vettori $\mathbf{w}$ e $t\mathbf{w}$). Ne segue che $OD:OB=OC:OA=t$. Ma $\overrightarrow{OD}=t\mathbf{v}+t\mathbf{w}$, $\overrightarrow{OB}=\mathbf{v}+\mathbf{w}$, perciò $t\mathbf{v}+t\mathbf{w}=t(\mathbf{v}+\mathbf{w})$.



- **VERSORI**: un vettore di modulo unitario si chiama versore. Dato un vettore $\mathbf{v}$ (non nullo), indichiamo con:
									$vers(\mathbf{v})=\frac{\mathbf{v}}{\left | \mathbf{v} \right |}$
	il versore ottenuto da $\mathbf{v}$ dividentolo per il suo modulo, ossia <u>normalizzandolo</u>.

È utile ora passare dal punto di vista della geometria elementare a quello della geometria analitica, ossia introdurre un sistema di riferimento cartesiano. Questo renderà possibili calcoli analitici coi vettori e costituirà il punto di partenza per le generalizzazioni successive.


### **1.2 Vettori nel piano**

Se introduciamo un sistema di riferimento cartesiano ortogonale nel piano, questo si può identificare con l'insieme $\mathbb{R}^2$ delle coppie ordinate di numeri reali. All'origine $O$ si può associare il vettore nullo $\mathbf{O}$; ad un punto $A(x,y)$ viene associato il vettore $\mathbf{v}=\overrightarrow{OA}$.
Viceversa, ad ogni vettore $\mathbf{v}$ è associata un'unica freccia che ha come primo estremo l'origine e come secondo un punto $A=(x,y)$. In questo modo è possibile identificare il punto di coordinate $A=(x,y)$ come il vettore posizione $\overrightarrow{OA}$. Potremo allora scrivere $v=(x,y)$ invece di $v=\overrightarrow{OA}$
e i numeri $x$ e $y$ si dicono <u>componenti scalari</u> di $\mathbf{v}$.
Si noti che $\mathbf{v}=$ lunghezza di $\overrightarrow{OA}=\sqrt{x^2+y^2}$ (Teorema di Pitagora).

Due punti $P=(a,b)$ e $Q=(c,d)$, nell'ordine, individuano il vettore di componenti scalari $x=c-a, y=d-b$, cioè: $\overrightarrow{PQ}=(c-a, d-b)$



Se consideriamo 


