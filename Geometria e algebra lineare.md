

# Capitolo I: Vettori nel piano e nello spazio


Il concetto di vettore, fondamentale sia in matematica che nelle applicazioni (fisiche, ecc.), può essere introdotto a vari livelli di astrazione. In questa sezione di occuperemo di vettori nel piano e nello spazio: in questo contesto, è possibile dare una definizione geometrica elementare di vettore; molte grandezze fisiche (velocità, accelerazione, forza,...) si rappresentano in questo modo. In seguito vedremo come la nozione di vettore si possa generalizzare in termini astratti, ottenendo un concetto più flessibile, che risulta molto utile per l'algebra, il calcolo infinitesimale e le loro applicazioni.

### **1.1 Operazioni fondamentali sui vettori**

- Un vettore nel piano o nello spazio è individuato assegnando:
	a) un numero reale non negativo che esprime la sua **lunghezza** o **modulo** o intensità;
	b) una **direzione**, individuata da una retta (rette *parallele* individuano la stessa direzione);
	c) un **verso**.

Geometricamente, possiamo pensare ai vettori come a segmenti orientati, con la precisazione che due segmenti orientati che possano ottenersi l'uno dall'altro per traslazione sono lo stesso vettore.
Se nello spazio è fissato un sistema di riferimento cartesiano di cui $O$ è l'origine, possiamo anche vedere i vettori come frecce uscenti da $O$.

![[Screenshot 2026-09-16 alle 15.03.01.png]]
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

Due punti $P=(a,b)$ e $Q=(c,d)$, nell'ordine, individuano il vettore di componenti scalari $x=c-a, y=d-b$, cioè: $\overrightarrow{PQ}=(c-a, d-b)$.



Se consideriamo due vettori $\mathbf{u}=(x_1, y_1)$ e $\mathbf{v}=(x_2, y_2)$ si verifica immediatamente che $u \pm v=(x_1 \pm x_2, y_1 \pm y_2)$, e che se $t \in \mathbb{R}\rightarrow t\mathbf{u}=(t x_1,t y_1)$.



Le formule precedenti sono fondamentali in quanto permettono di eseguire le operazioni sui vettori per via analitica, senza necessità di costruzioni geometriche.
I vettori $\mathbf{i}=(1,0)$ e $\mathbf{j}=(0,1)$ sono diretti come gli assi coordinati, hanno lunghezza $\left | \mathbf{i} \right |=1=\left | \mathbf{j} \right |$ (sono <u>versori</u>) e sono <u>ortogonali</u> tra loro.
Inoltre ogni altro vettore $\mathbf{v}=(x,y)$ si può esprimere nella forma $\mathbf{v}=x\mathbf{i}+y\mathbf{j}$; $\mathbf{i}$ e $\mathbf{j}$ si dicono **VERSORI FONDAMENTALI NEL PIANO**.


### **1.3 Vettori nello spazio**

Se introduciamo un sistema di riferimento cartesiano ortogonale nello spazio tridimensionale, con origine nel punto $O$ di riferimento, questo si può identificare con l'insieme $\mathbb{R}^3$ delle terne ordinate $(x,y,z)$ di numeri reali.
Di solito si sceglie una terna di assi ortogonali con un'orientazione destrorsa (con ciò si intende che se indice e medio della mano destra puntano rispettivamente nel verso positivo degli assi $x$ e $y$, il pollice punta nel verso positivo dell'asse $z$).



La formula della distanza tra due punti $P=(a,b,c)$ e $Q = (a',b',c')$ si estende subito nel caso bidimensionale: $\overline{PQ}=\sqrt{(a-a')^2 +(b-b')^2 + (c-c')^2}$, diagonale del parallelepipedo indicato in figura.



Il vettore $\mathbf{v}=\overrightarrow{PQ}$ ha componenti scalari $x=(a-a'), y= (b-b'), z=(c-c')$ e coincide con il vettore $\overrightarrow{OA}$, <u>vettore posizione</u> del punto $A(x,y,z)$. Si può scrivere allora $\mathbf{v}=(x,y,z)$ invede ci $\mathbf{v}=\overrightarrow{OA}$.
La lunghezza di $\mathbf{v}$ coincide con la lunghezza di $\overrightarrow{PQ}$, ossia $|\mathbf{v}|=\sqrt{x^2+y^2+z^2}$

I vettori $\mathbf{i}=(1,0,0)$, $\mathbf{j}=(0,1,0)$, $\mathbf{k}=(0,0,1)$ sono <u>versori</u>, mutualmente ortogonali, diretti nel verso positivo dei tre assi, rispettivamente. Ogni altro vettore $\mathbf{v}=(x,y,z)$ si può scrivere nella forma $\mathbf{v}=x\mathbf{i}+y\mathbf{j}+z\mathbf{k}$.
$\mathbf{i}$, $\mathbf{j}$, $\mathbf{k}$ si dicono **VERSORI FONDAMENTALI NELLO SPAZIO**. Le operazioni di somma di vettori e prodotto per uno scalare si possono eseguire componente per componente, come nel caso piano:

					$(x_1,y_1,z_1)+(x_2+y_2+z_2)=(x_1+x_2,y_1+y_2,z_1+z_2);$
								$t(x_1,y_1,z_1)=(tx_1,ty_1,tz_1)$


### **1.4 Combinazioni lineari di vettori. Vettori linearmente indipendenti**

Consideriamo $k$ vettori $\mathbf{v_1,...,v_k}$ (nel piano e nello spazio) e $k$ scalari $\alpha_1,...,\alpha_k$.
Il vettore $\mathbf{w}=\alpha_1 \mathbf{v_1}+ ... +\alpha_k \mathbf{v_k}$ si chiama **COMBINAZIONE LINEARE** dei vettori $\mathbf{v_1,...,v_k}$ con coefficienti $\alpha_1,...,\alpha_k$.

- **Definizione (1).** I vettori di $\mathbf{v_1,...,v_k}$ si dicono <u>LINEARMENTE INDIPENDENTI</u> se almeno uno di essi si può esprimere come combinazione lineare degli altri; in caso contrario si dicono **LINEARMENTE INDIPENDENTI**.
	 
	- Equivalentemente, $\mathbf{v_1,...,v_k}$ sono <mark class="hltr-yellow">indipendenti</mark> se $\alpha_1 \mathbf{v_1}+ ... +\alpha_k \mathbf{v_k}=\mathbf{0}$ implica $\alpha_1,...,\alpha_k=0$.
	
	- Nel caso particolare di due vettori $\mathbf{v_1,v_2}$ essi sono linearmente <mark class="hltr-yellow">dipendenti</mark> se, per qualche scalare $\alpha$, si ha $\mathbf{v_1}=\alpha \mathbf{v_2}$
		cioè, se uno è multiplo dell'altro. Geometricamente, ciò significa che sono paralleli o sulla stessa retta.

Nel caso di tre vettori $\mathbf{v_1,v_2,v_3}$, di cui per esempio $\mathbf{v_2}$ e $\mathbf{v_3}$ indipendenti, dire che $\mathbf{v_1}$ è combinazione lineare di $\mathbf{v_2}$ e $\mathbf{v_3}$ significa geometricamente che $\mathbf{v_1}$ giace nel piano individuato da $\mathbf{v_2}$ e $\mathbf{v_3}$ (quando i tre vettori hanno origine nel medesimo punto). Infatti, in tal caso $\mathbf{v_1}$ è la diagonale del parallelogramma che ha per lati due multipli di $\mathbf{v_2}$, $\mathbf{v_3}$, quindi giace nel piano individuato da $\mathbf{v_2}$, $\mathbf{v_3}$.



*Per esempio*, nel piano, i vettori $\mathbf{i}=(1,0)$ e $\mathbf{j}=(0,1)$ sono linearmente indipendenti, come pure, nello spazio, i vettori $\mathbf{i}=\begin{Bmatrix}1 \\ 0 \\ 0\end{Bmatrix}, \mathbf{j}=\begin{Bmatrix}0 \\ 1 \\ 0\end{Bmatrix}, \mathbf{k}=\begin{Bmatrix}0 \\ 0 \\ 1\end{Bmatrix}$ (*riguardare formula versori fondamentali nello spazio*).
In realtà, data una qualunque terna di vettori nello spazio linearmente indipendenti, $\mathbf{v_1,v_2,v_3}$, ed un quarto vettore $\mathbf{v}$, si può sempre scrivere $\mathbf{v}=\alpha_1 \mathbf{v_1}+\alpha_2 \mathbf{v_2}+\alpha_3 \mathbf{v_3}$, con opportuni scalari $\alpha_1,\alpha_2,\alpha_3$.

Analogamente, data una qualunque coppia di vettori nel piano linearmente indipendenti, $\mathbf{v_1,v_2}$, ogni altro vettore $\mathbf{v}$ può scriversi come combinazione lineare dei primi: $\mathbf{v}=\alpha_1 \mathbf{v_1}+\alpha_2 \mathbf{v_2}$, con opportuni scalari $\alpha_1,\alpha_2$.

Dimostriamo, per esempio, quest'ultima affermazione. Siano $\mathbf{v_1}=\overrightarrow{OA}$, $\mathbf{v_2}=\overrightarrow{OB}$, $\mathbf{v}=\overrightarrow{OC}$.
Tracciando da $C$ le rette parallele ad $OA$ e $OB$, risultano individuati su tali rette due vettori, rispettivamente paralleli a $\mathbf{v_1,v_2}$, la cui somma dà $\mathbf{v}$ (per la regola del parallelogramma). Ma essendo paralleli a $\mathbf{v_1,v_2}$, tali vettori sono del tipo $\alpha_1 \mathbf{v_1},\alpha_2 \mathbf{v_2}$, per opportuni $\alpha_1,\alpha_2$.
Dunque, abbiamo provato che si ha $\mathbf{v}=\alpha_1 \mathbf{v_1}+\alpha_2 \mathbf{v_2}$.

Da queste considerazioni segue che **nello spazio non vi possono essere più di tre vettori linearmente indipendenti, nel piano non più di due**.


### **1.5 Prodotto scalare e vettoriale**

- **PRODOTTO SCALARE**. Dati due vettori $\mathbf{v}$ e $\mathbf{w}$ nel piano o nello spazio, il loro <u>prodotto scalare o interno</u>, denotato con $\mathbf{v}\cdot\mathbf{w}$ o con $\langle \mathbf{v},\mathbf{w} \rangle$, è assegnato, per definizione, dalla formula seguente:
								$\mathbf{v}\cdot\mathbf{w}=|\mathbf{v}|\cdot|\mathbf{w}|\cdot\cos\alpha$ 

dove $\alpha$ è l'angolo che essi formano $(0\le \alpha \le \pi)$.
*Si noti che il prodotto di due vettori è un numero reale (non un vettore).*

**PROPRIETÀ**:
	a) <mark class="hltr-yellow">Commutativa</mark>: $\mathbf{v}\cdot\mathbf{w}=\mathbf{w}\cdot\mathbf{v}$
	b) <mark class="hltr-yellow">Distributiva</mark>: $\mathbf{u}\cdot(\mathbf{v}+\mathbf{w})=\mathbf{u}\cdot\mathbf{v}+\mathbf{u}\cdot\mathbf{w}$
	c) Inoltre, $\forall t\in\mathbb{R}$, si ha $(t\mathbf{v})\cdot\mathbf{w}=t(\mathbf{v}\cdot\mathbf{w})$
	d) Si noti poi che $\mathbf{v}\cdot\mathbf{v}=|\mathbf{v}|^2$
	e) Infine, $\mathbf{v}$ è **perpendicolare** a $\mathbf{w}$ se e solo se $\mathbf{v}\cdot\mathbf{w}=0$.

*Tutte queste proprietà seguono dalla definizione di prodotto scalare.*

- **PROIEZIONI**. La proiezione di un vettore $\mathbf{v}$ su una retta $r$, orientata, si chiama **componente vettoriale** di $\mathbf{v}$ rispetto all'asse $r$ ed è data dal vettore $(\mathbf{v}\cdot\mathbf{r})\mathbf{r}$, dove $\mathbf{r}$ è il <u>VERSORE</u> lungo la retta.

Infatti, $\mathbf{v}\cdot\mathbf{r}=|\mathbf{v}|\cdot|\mathbf{r}|\cdot\cos\alpha=|\mathbf{v}|\cdot\cos\alpha$ e quindi $|\mathbf{v}\cdot\mathbf{r}|$ dà la lunghezza del vettore proiezione; il segno di $\mathbf{v}\cdot\mathbf{r}$ $(>0$ se $\alpha<\frac{\pi}{2}$, $<0$ se $\alpha >\frac{\pi}{2})$ determina il verso.
Nel piano, i versori $\mathbf{i}$ e $\mathbf{j}$ sono ortogonali e quindi $\mathbf{i}\cdot\mathbf{j}=0$.
In termini di componenti, dati due vettori nel piano $\mathbf{v}=x_1 \mathbf{i}+x_2 \mathbf{j}$, $\mathbf{w}=y_1 \mathbf{i}+y_2 \mathbf{j}$ si ha, usando le proprietà del prodotto scalare:
		$\mathbf{v}\cdot\mathbf{w}=x_1 \mathbf{i}+x_2 \mathbf{j}\cdot(y_1 \mathbf{i}+y_2 \mathbf{j})=x_1y_1 \mathbf{i}+x_1y_2 \mathbf{j}+x_2y_1 \mathbf{i}+x_2y_2 \mathbf{j}\cdot\mathbf{j}=x_1y_1+x_2y_2$ 

da cui l'importante **formula del prodotto scalare nel piano**: $\mathbf{v}\cdot\mathbf{w}=x_1y_1+x_2y_2$

Analogamente, nello spazio si hanno i vettori $\mathbf{v}=x_1 \mathbf{i}+x_2 \mathbf{j}+x_3 \mathbf{k}$ e $\mathbf{w}=y_1 \mathbf{i}+y_2 \mathbf{j}+y_3 \mathbf{k}$, perciò avremo come **formula del prodotto scalare nello spazio**: $\mathbf{v}\cdot\mathbf{w}=x_1y_1+x_2y_2+x_3y_3$ 

Le ultime due formule trovate risultano molto comode per il calcolo effettivo del prodotto di dui vettori di cui si conoscono le componenti, in quanto non richiedono il calcolo specifico dell'angolo formato dai vettori.

- **PRODOTTO VETTORIALE NELLO SPAZIO**. Dati due vettori $\mathbf{v}$ e $\mathbf{w}$, il loro <u>prodotto vettoriale</u>, denotato con $\mathbf{v}\times\mathbf{w}$, è il vettore caratterizzato dalle seguenti proprietà:
		1. La lunghezza di $\mathbf{v}\times\mathbf{w}$ è data da $|\mathbf{v}\times\mathbf{w}|=|\mathbf{v}|\cdot|\mathbf{w}|\cdot\sin\alpha$, 
			dove $\alpha$ è l'angolo che essi formano $(0\le \alpha \le \pi)$;
		2. $\mathbf{v}\times\mathbf{w}$ è perpendicolare al piano di $\mathbf{v}$ e $\mathbf{w}$;
		3. $\mathbf{v}$, $\mathbf{w}$ e $\mathbf{v}\times\mathbf{w}$, nell'ordine, formano una terna destrorsa di vettori.

**PROPRIETÀ**:
	a) <mark class="hltr-yellow">Anticommutativa</mark>: $\mathbf{v}\times\mathbf{w}=-\mathbf{w}\times\mathbf{v}$
	b) <mark class="hltr-yellow">Distributiva</mark>: $\mathbf{u}\times(\mathbf{v}+\mathbf{w})=\mathbf{u}\times\mathbf{v}+\mathbf{u}\times\mathbf{w}$
	c) Inoltre, $\forall t\in\mathbb{R}$, si ha $(t\mathbf{v})\times\mathbf{w}=t(\mathbf{v}\times\mathbf{w})$
	d) Si noti poi che $\mathbf{v}\times\mathbf{v}=0$ (essendo $\alpha=0$)
	e) Infine, $\mathbf{v}$ è **parallelo** a $\mathbf{w}$ se e solo se $\mathbf{v}\times\mathbf{w}=0$.



- **PRODOTTO MISTO NELLO SPAZIO**. Se $\mathbf{u}$, $\mathbf{v}$ e $\mathbf{w}$ sono tre vettori nello spazio, il loro <u>prodotto misto</u> è definito dal numero reale $\mathbf{u}\cdot(\mathbf{v}\times\mathbf{w})$
		La parentesi è in realtà superflua, in quanto $(\mathbf{u}\cdot\mathbf{v})\times\mathbf{w}$ non ha senso. Si può perciò scrivere semplicemente $\mathbf{u}\cdot\mathbf{v}\times\mathbf{w}$.
		Si dimostra in seguito che il prodotto misto non varia permutando ciclicamente i tre vettori $\mathbf{u}$, $\mathbf{v}$ e $\mathbf{w}$: $\mathbf{u}\cdot\mathbf{v}\times\mathbf{w}=\mathbf{w}\cdot\mathbf{u}\times\mathbf{v}=\mathbf{v}\cdot\mathbf{w}\times\mathbf{u}$

Geometricamente, il valore assoluto del prodotto misto rappresenta il volume del parallelepipedo costruito sui vettori $\mathbf{u}$, $\mathbf{v}$ e $\mathbf{w}$, infatti si ha $volume = altezza \cdot area \ di  \ base$.
L'area di base è $|\mathbf{v}\times\mathbf{w}|$, mentre l'altezza $h$ è uguale alla lunghezza della componente di $\mathbf{u}$ nella direzione di $\mathbf{v}\times\mathbf{w}$, perpendicolare alla base. Se l'angolo $\theta$ tra $\mathbf{u}$ e $\mathbf{v}\times\mathbf{w}$ è acuto ($<\frac{\pi}{2}$), si ha $h=|\mathbf{u}|\cos\theta$, mentre se $\theta$ è ottuso ($>\frac{\pi}{2}$) si ha $h=-|\mathbf{u}|\cos\theta$.
Dunque, $volume = |\mathbf{u}\cdot\mathbf{v}\times\mathbf{w}|=|\mathbf{v}\times\mathbf{w}|\cdot|\mathbf{u}|\cos\theta$.

Se il prodotto misto è nullo allora $\mathbf{u}$ è perpendicolare a $\mathbf{v}\times\mathbf{w}$ e pertanto giace nel piano individuato da $\mathbf{v}$ e $\mathbf{w}$. In conclusione:
					$\mathbf{u}\cdot\mathbf{v}\times\mathbf{w}=0$ se e solo se $\mathbf{u}, \mathbf{v}, \mathbf{w}$ sono <u>complanari</u>

ossia se e solo se $\mathbf{u}, \mathbf{v}, \mathbf{w}$ sono <u>linearmente dipendenti</u>.


Questo fatto ci fornisce un metodo analitico per verificare se tre vettori (nello spazio) siano indipendenti oppure no, mediante un calcolo puramente meccanico. Infatti, siano:
				$\mathbf{u}=(u_1,u_2,u_3), \mathbf{v}=(x_1,x_2,x_3), \mathbf{w}=(y_1,y_2,y_3)$
sfruttando le formule precedenti del prodotto scalare e vettoriale, abbiamo:
			$\mathbf{u}\cdot\mathbf{v}\times\mathbf{w}=u_1(x_1y_3-x_3y_2)+u_2(x_3y_1-x_1y_3)+u_3(x_1y_2-x_2y_1)$
			
e dunque i tre vettori <u>sono indipendenti se e solo se quest'ultima espressione è diversa da 0</u>.



# Capitolo II: Geometria lineare nello spazio


Mediante il calcolo vettoriale introdotto nei paragrafi precedenti è facile scrivere, in un dato sistema di riferimento, vari tipi di equazioni per rette e piani.

- **Equazione della retta**

	Una retta nello spazio è individuata da:
		a) un punto e un vettore direzionale;
		b) due punti;
		c) intersezione di due piani non paralleli.
	Cominciamo col primo caso. Consideriamo un punto $P_0(x_0,y_0,z_0)$ ed un vettore $\mathbf{v}=(a,b,c)$ non nullo; ci proponiamo di scrivere l'equazione della retta passante per $P_0$, parallela a $\mathbf{v}$.



	Dalla figura si vede che un generico punto $P(x,y,z)$ appartentente alla retta si trova aggiungendo al vettore posizione $\mathbf{p}_0=\overrightarrow{OP_0}$ un opportuno multiplo $t\mathbf{v}$ di $\mathbf{v}$.
	Abbiamo quindi per il vettore posizione $\mathbf{p}=\overrightarrow{OP}$ del generico punto sulla retta:
							$\mathbf{p}=\mathbf{p}_0+t\mathbf{v}, t\in\mathbb{R}$
	che prende il nome di <u>equazione parametrica vettoriale della retta</u>;
	$t$ è una "coordinata" sulla retta, corrispondente alla scelta di $P_0$ come origine.
	Le <u>equazioni parametriche scalari</u> si ricavano scrivendo componente per componente:
							$\begin{cases} x=x_0+ta\\ y=y_0+tb \\ z=z_0+tc \end{cases}\quad t\in\mathbb{R}$ 

	Il significato delle equazioni parametriche (sia la prima che la seconda) è il seguente: al variare del parametro $t$ in $\mathbb{R}$, il punto $(x,y,z)$ si muove sulla retta, descrivendo tale linea.

	Se $a\ne0, b\ne0, c\ne0$, si può eliminare $t$ nelle equazioni scalari, ottenendo:
	$\frac{x-x_0$