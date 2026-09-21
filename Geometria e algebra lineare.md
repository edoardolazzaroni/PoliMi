

# Capitolo I: Vettori nel piano e nello spazio


Il concetto di vettore, fondamentale sia in matematica che nelle applicazioni (fisiche, ecc.), può essere introdotto a vari livelli di astrazione. In questa sezione di occuperemo di vettori nel piano e nello spazio: in questo contesto, è possibile dare una definizione geometrica elementare di vettore; molte grandezze fisiche (velocità, accelerazione, forza,...) si rappresentano in questo modo. In seguito vedremo come la nozione di vettore si possa generalizzare in termini astratti, ottenendo un concetto più flessibile, che risulta molto utile per l'algebra, il calcolo infinitesimale e le loro applicazioni.

### 1.1 **Operazioni fondamentali sui vettori**

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



- **VERSORE**: un vettore di modulo unitario si chiama <u>versore</u>. Dato un vettore $\mathbf{v}$ (non nullo), indichiamo con:
									$vers(\mathbf{v})=\frac{\mathbf{v}}{\left | \mathbf{v} \right |}$
	il versore ottenuto da $\mathbf{v}$ dividentolo per il suo modulo, ossia <u>normalizzandolo</u>.

È utile ora passare dal punto di vista della geometria elementare a quello della geometria analitica, ossia introdurre un sistema di riferimento cartesiano. Questo renderà possibili calcoli analitici coi vettori e costituirà il punto di partenza per le generalizzazioni successive.


### 1.2 **Vettori nel piano**

Se introduciamo un sistema di riferimento cartesiano ortogonale nel piano, questo si può identificare con l'insieme $\mathbb{R}^2$ delle coppie ordinate di numeri reali. All'origine $O$ si può associare il vettore nullo $\mathbf{O}$; ad un punto $A(x,y)$ viene associato il vettore $\mathbf{v}=\overrightarrow{OA}$.
Viceversa, ad ogni vettore $\mathbf{v}$ è associata un'unica freccia che ha come primo estremo l'origine e come secondo un punto $A=(x,y)$. In questo modo è possibile identificare il punto di coordinate $A=(x,y)$ come il vettore posizione $\overrightarrow{OA}$. Potremo allora scrivere $v=(x,y)$ invece di $v=\overrightarrow{OA}$
e i numeri $x$ e $y$ si dicono <u>componenti scalari</u> di $\mathbf{v}$.
Si noti che $\mathbf{v}=$ lunghezza di $\overrightarrow{OA}=\sqrt{x^2+y^2}$ (Teorema di Pitagora).

Due punti $P=(a,b)$ e $Q=(c,d)$, nell'ordine, individuano il vettore di componenti scalari $x=c-a, y=d-b$, cioè: $\overrightarrow{PQ}=(c-a, d-b)$.



Se consideriamo due vettori $\mathbf{u}=(x_1, y_1)$ e $\mathbf{v}=(x_2, y_2)$ si verifica immediatamente che $u \pm v=(x_1 \pm x_2, y_1 \pm y_2)$, e che se $t \in \mathbb{R}\rightarrow t\mathbf{u}=(t x_1,t y_1)$.



Le formule precedenti sono fondamentali in quanto permettono di eseguire le operazioni sui vettori per via analitica, senza necessità di costruzioni geometriche.
I vettori $\mathbf{i}=(1,0)$ e $\mathbf{j}=(0,1)$ sono diretti come gli assi coordinati, hanno lunghezza $\left | \mathbf{i} \right |=1=\left | \mathbf{j} \right |$ (sono <u>versori</u>) e sono <u>ortogonali</u> tra loro.
Inoltre ogni altro vettore $\mathbf{v}=(x,y)$ si può esprimere nella forma $\mathbf{v}=x\mathbf{i}+y\mathbf{j}$; $\mathbf{i}$ e $\mathbf{j}$ si dicono **VERSORI FONDAMENTALI NEL PIANO**.


### 1.3 **Vettori nello spazio**

Se introduciamo un sistema di riferimento cartesiano ortogonale nello spazio tridimensionale, con origine nel punto $O$ di riferimento, questo si può identificare con l'insieme $\mathbb{R}^3$ delle terne ordinate $(x,y,z)$ di numeri reali.
Di solito si sceglie una terna di assi ortogonali con un'orientazione destrorsa (con ciò si intende che se indice e medio della mano destra puntano rispettivamente nel verso positivo degli assi $x$ e $y$, il pollice punta nel verso positivo dell'asse $z$).



La formula della distanza tra due punti $P=(a,b,c)$ e $Q = (a',b',c')$ si estende subito nel caso bidimensionale: $\overline{PQ}=\sqrt{(a-a')^2 +(b-b')^2 + (c-c')^2}$, diagonale del parallelepipedo indicato in figura.



Il vettore $\mathbf{v}=\overrightarrow{PQ}$ ha componenti scalari $x=(a-a'), y= (b-b'), z=(c-c')$ e coincide con il vettore $\overrightarrow{OA}$, <u>vettore posizione</u> del punto $A(x,y,z)$. Si può scrivere allora $\mathbf{v}=(x,y,z)$ invede ci $\mathbf{v}=\overrightarrow{OA}$.
La lunghezza di $\mathbf{v}$ coincide con la lunghezza di $\overrightarrow{PQ}$, ossia $|\mathbf{v}|=\sqrt{x^2+y^2+z^2}$

I vettori $\mathbf{i}=(1,0,0)$, $\mathbf{j}=(0,1,0)$, $\mathbf{k}=(0,0,1)$ sono <u>versori</u>, mutualmente ortogonali, diretti nel verso positivo dei tre assi, rispettivamente. Ogni altro vettore $\mathbf{v}=(x,y,z)$ si può scrivere nella forma $\mathbf{v}=x\mathbf{i}+y\mathbf{j}+z\mathbf{k}$.
$\mathbf{i}$, $\mathbf{j}$, $\mathbf{k}$ si dicono **VERSORI FONDAMENTALI NELLO SPAZIO**. Le operazioni di somma di vettori e prodotto per uno scalare si possono eseguire componente per componente, come nel caso piano:

					$(x_1,y_1,z_1)+(x_2+y_2+z_2)=(x_1+x_2,y_1+y_2,z_1+z_2);$
								$t(x_1,y_1,z_1)=(tx_1,ty_1,tz_1)$


### 1.4 **Combinazioni lineari di vettori. Vettori linearmente indipendenti**

Consideriamo $k$ vettori $\mathbf{v_1,...,v_k}$ (nel piano e nello spazio) e $k$ scalari $\alpha_1,...,\alpha_k$.
Il vettore $\mathbf{w}=\alpha_1 \mathbf{v_1}+ ... +\alpha_k \mathbf{v_k}$ si chiama **COMBINAZIONE LINEARE** dei vettori $\mathbf{v_1,...,v_k}$ con coefficienti $\alpha_1,...,\alpha_k$.

- #DEFINIZIONE(1). I vettori di $\mathbf{v_1,...,v_k}$ si dicono **LINEARMENTE DIPENDENTI** se almeno uno di essi si può esprimere come combinazione lineare degli altri; in caso contrario si dicono **LINEARMENTE INDIPENDENTI**.
	 
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


### 1.5 **Prodotto scalare e vettoriale**

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

### 2.1 **Equazione della retta**

Una retta nello spazio è individuata da:
	a) un punto e un vettore direzionale;
	b) due punti;
	c) intersezione di due piani non paralleli.


a) Cominciamo col primo caso. Consideriamo un punto $P_0(x_0,y_0,z_0)$ ed un vettore $\mathbf{v}=(a,b,c)$ non nullo; ci proponiamo di scrivere l'equazione della retta passante per $P_0$, parallela a $\mathbf{v}$.



Dalla figura si vede che un generico punto $P(x,y,z)$ appartentente alla retta si trova aggiungendo al vettore posizione $\mathbf{p}_0=\overrightarrow{OP_0}$ un opportuno multiplo $t\mathbf{v}$ di $\mathbf{v}$.
Abbiamo quindi per il vettore posizione $\mathbf{p}=\overrightarrow{OP}$ del generico punto sulla retta:

							$\mathbf{p}=\mathbf{p}_0+t\mathbf{v}, t\in\mathbb{R}$

che prende il nome di <u>equazione parametrica vettoriale della retta</u>;
$t$ è una "coordinata" sulla retta, corrispondente alla scelta di $P_0$ come origine.
Le <u>equazioni parametriche scalari</u> si ricavano scrivendo componente per componente:

							$\begin{cases} x=x_0+ta\\ y=y_0+tb \\ z=z_0+tc \end{cases}\quad t\in\mathbb{R}$

Il significato delle equazioni parametriche (sia la prima che la seconda) è il seguente: al variare del parametro $t$ in $\mathbb{R}$, il punto $(x,y,z)$ si muove sulla retta, descrivendo tale linea.

Se $a\ne0, b\ne0, c\ne0$, si può eliminare $t$ nelle equazioni scalari, ottenendo:	

$\frac{x-x_0}{a}=t,\frac{y-y_0}{b}=t, \frac{z-z_0}{c}=t$,ossia $\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}$

che sono le <u>equazioni cartesiane</u> della retta.
Se uno o due tra i parametri $a,b,c$ è nullo, si ottiene per esempio:

							$x=x_0 \quad \frac{y-y_0}{b}=\frac{z-z_0}{c}$

Nel caso in cui $a^2+b^2+c^2=1$, cioè nel caso in cui $\mathbf{v}$ è un *versore*, i numeri $a,b,c$ prendono il nome di <u>coseni direttori della retta</u>, in quanto rappresentano i coseni degli angoli che la retta forma con ciascuno degli assi coordinati.


b) Nel secondo caso si vuole scrivere l'equazione della retta passante per i punti $P_0=(x_0,y_0,z_0)$ e $P_1=(x_1,y_1,z_1)$; riconduciamo al primo caso scegliendo uno dei due, per esempio $P_0$ ed il vettore direzionale $\mathbf{v}=(x_1-x_0,y_1-y_0,z_1-z_0)$.
Le equazioni parametriche della retta risultano allora

							$\begin{cases} x=x_0+t(x_1-x_0)\\ y=y_0+t(y_1-y_0) \\ z=z_0+t(z_1-z_0) \end{cases}$


- **Condizioni di parallelismo ed ortogonalità tra rette**

Due rette sono **parallele** se i loro vettori direzionali sono paralleli (linearmente indipendenti). Precisamente, le due rette

$\begin{cases} x=x_0+ta\\ y=y_0+tb \\ z=z_0+tc \end{cases}\quad$ e $\quad\begin{cases} x=x_1+ta' \\ y=y_1+tb' \\ z=z_1+tc' \end{cases}$

sono parallele se $\exists\lambda\ne0$ t.c. $(a',b',c')=\lambda(a,b,c)$.
Le due rette sono **ortogonali** se lo sono i loro vettori direzionali, cioè se $(a',b',c')\cdot(a,b,c)=aa'+bb'+cc'\equiv0$.

Si noti che per essere ortogonali non è necessario che le due rette siano **incidenti** (cioè si intersechino in un punto).


c) Prima di vedere come si scrive l'equazione di una retta come intersezione di due piani, vediamo come si scrive l'equazione di un piano.


### 2.2 **Equazione del piano**

Un piano è individuato da:
	a) un punto ed un vettore ortogonale al piano stesso;
	b) tre punti;
	c) due rette incidenti.


a) Cominciamo col primo caso. Consideriamo un punto $P_0(x_0,y_0,z_0)$ ed un vettore $\mathbf{n}=(a,b,c)$ non nullo; ci proponiamo di determinare l'equazione del piano passante per $P_0 \perp \mathbf{n}$.



Dalla figura si vede che se $P=(x,y,z)$ è il generico punto del piano, allora il vettore $\overrightarrow{P_0P}$ è parallelo al piano e quindi $\perp \mathbf{n}$. Si ottiene allora l'equazione vettoriale:
								$\mathbf{n}\cdot\overrightarrow{P_0P}=0$

L'equazione cartesiana del piano si ottiene passando dai vettori alle coordinate, cioè:
					$a(x-x_0)+b(y-y_0)+c(z-z_0)=0$

ossia dove $\begin{cases} ax+by+cz=d \\ d=\mathbf{n}\cdot\mathbf{p}_0=ax_0+by_0+cz_0 \end{cases}$

Facciamo qualche osservazione:
- Se $a^2+b^2+c^2=1$, cioè $\mathbf{n}$ è un versore, allora $a,b,c$ sono i <u>coseni direttori</u> del piano;
- Se $d=0$, il piano passa per l'origine $O=(0,0,0)$;
- Se uno dei coefficienti $a,b,c$ è nullo, il piano è parallelo ad uno degli assi coordinati. Per esempio, se $c=0$ il piano è parallelo all'asse $z$, e quindi è perpendicolare al piano $(x,y)$;
	Si noti che l'equazione $ax+by=d$, che nel piano rappresenta una retta, nello spazio rappresenta un piano perpendicolare al piano $(x,y)$.
- Se due coefficienti sono nulli, allora il piano è parallelo ad uno dei piani coordinati. Per esempio, se $a=b=0$, il piano ha equazione $z=k$ ed è parallelo al piano $(x,y)$;
- Se $d\ne0$, si può dividere l'equazione cartesiana precedente per $d$, ottenendo così:
								$\frac{x}{\alpha}+\frac{y}{\beta}+\frac{z}{\gamma}=1$
	In tal caso $\alpha, \beta, \gamma$ rappresentano le intercette del piano con gli assi coordinati.


- **Condizioni di parallelismo ed ortogonalità tra piani**

Due piani sono **paralleli** se lo sono i lori vettori ortogonali. Precisamente, i piani

$ax+by+cz=d, \quad a'x+b'y+c'z=d'$

sono paralleli se $\exists \lambda \ne 0$ t.c. $(a',b',c')=\lambda(a,b,c)$
Sono **ortogonali** se lo sono i loro vettori normali: $(a',b',c')\cdot(a,b,c)=aa'+bb'+cc'\equiv0$.


Possiamo ora trattare il caso rimasto in sospeso nella discussione dei modi di scrivere l'equazione di una retta.
c) Siano $ax+by+cz=d$ e $a'x+b'y+c'z=d'$ le equazioni di due piani non paralleli.
Essi si intersecano lungo una retta rappresentata dal sistema:

$\begin{cases} ax+by+cz=d\\ a'x+b'y+c'z=d' \end{cases}$

Un vettore direzionale della retta deve essere ortogonale ad entrambi i vettori $\mathbf{n}=(a,b,c)$ e $\mathbf{n}'=(a',b',c')$; si può perciò scegliere come vettore direzionale della retta:
					$\mathbf{v}=\mathbf{n}\times\mathbf{n}'=(bc'-b'c,a'c-ac',ab'-a'b)$

In alternativa, si possono scrivere le equazioni parametriche della retta col seguente procedimento: si considera il sistema nelle tre incognite $(x,y,z)$, che definisce la retta; se in tale sistema si riescono ad esprimere due variabili in funzione della terza, si può assumere la terza variabile come parametro.


- **Distanza di un punto da piano**

Si voglia calcolare la distanza $\delta$ di un punto $P_1(x_1,y_1,z_1)$ dal piano passante per $P_0=(x_0,y_0,z_0)$ ed ortogonale al vettore $\mathbf{n}=(a,b,c)$. Dalla figura si vede che $\delta$ è la lunghezza del segmento $P_2P_1$ uguale alla lunghezza della proiezione di $P_0P_1$ lungo la direzione $\mathbf{n}$.



Se si introduce il versore $\mathbf{N}=\frac{1}{\sqrt{a^2+b^2+c^2}}(a,b,c)$, la lunghezza della proiezione è il modulo del prodotto scalare tra $\mathbf{N}$ ed il vettore $\overrightarrow{P_0P_1}$, cioè:

$\delta=|\mathbf{N}\cdot\overrightarrow{P_0P_1}|=\frac{|a(x_1-x_0)+b(y_1-y_0)+c(z_1-z_0)|}{\sqrt{a^2+b^2+c^2}}$

ossia, ricordando che abbiamo posto $d=ax_0+by_0+cz_0$:

							$\delta=\frac{|ax_1+by_1+cz_1-d|}{\sqrt{a^2+b^2+c^2}}$



# Capitolo III: Spazi vettoriali


Iniziamo ora lo studio dei primi elementi di algebra lineare: si tratta di una disciplina che viene utilizzata sia in altri rami della matematica (geometria, analisi, ...) che nelle discipline applicative vere e proprie. L'idea centrale è quella di *linearità*.
Introduciamo quindi la definizione di *spazio vettoriale* astratto, e definiremo le *trasformazioni lineari* tra spazi vettoriali; studieremo quindi il *calcolo matriciale*, strumento basilare per lo studio di queste trasformazioni. Infine applicheremo questi concetti allo studio dei *sistemi lineari* ed al problema della *diagonalizzazione* di una trasformazione.


### 3.1 **Vettori $n$-dimensionali: lo spazio $\mathbb{R}^n$, spazi vettoriali astratti**

Nei primi capitoli abbiamo visto come i vettori nel piano e nello spazio si possano identificare, previa la scelta di un sistema di riferimento cartesiano, con coppie o terne ordinate di numeri reali. Una volta fatta questa identificazione, è possibile eseguire le operazioni fondamentali sui vettori (somma o prodotto per uno scalare) operando direttamente su queste coppie/terne:

						$(v_1,v_2)+(u_1,u_2)=(v_1+u_1,v_2+u_2)$
								$\lambda(v_1,v_2)=(\lambda v_1,\lambda v_2)$

Questi fatti suggeriscono la possibilità di considerare le $n$-uple ordinate di numeri reali come vettori di uno spazio astratto a $n$ dimensioni.


#### 3.1.1 **Lo spazio $\mathbb{R}^n$**

Consideriamo dunque l'insieme $\mathbb{R}^n$ di tutte le $n$-uple ordinate di numeri reali: $\mathbb{R}^n=\left\{(x_1, x_2, \cdots,x_n):x_i\in\mathbb{R}\right\}$ (ricordiamo che il simbolo $\mathbb{R}^n$ è un'abbreviazione del prodotto cartesiano $\mathbb{R}\times\mathbb{R}\times\cdots\mathbb{R}$ $n$ volte).
Potremo indicare un elemento di $\mathbb{R}^n$ con $\mathbf{x},\mathbf{y},\cdots \ .$
Se, per esempio, $\mathbf{x}=(x_1,x_2,\cdots,x_n)$, diremo che $x_i$ sono le **componenti del vettore** $\mathbf{x}$.
È possibile definire in modo naturale la somma di due vettori e la moltiplicazione per uno scalare:

				$(x_1,x_2,\cdots,x_n)+(y_1,y_2,\cdots,y_n)=(x_1+y_1,x_2+y_2,\cdots,x_n+y_n)$
							$\lambda(x_1,x_2,\cdots,x_n)=(\lambda v_1,\lambda x_2,\cdots,\lambda x_n)$

Si noti il diverso punto di vista che stiamo adottando rispetto a prima: lì, dopo aver definito la somma di due vettori nel piano per via geometrica (regola del parallelogramma), si dimostrava che la somma si poteva calcolare, rappresentando i valori come coppie ordinate di numeri reali, sommando componente per componente. Qui invece, non essendo visualizzabili i vettori $n$-dimensionali (quando $n>3$), l'analoga formula della somma componente per componente è la definizione stessa di somma di due $n$-uple. Possiamo anche dire che i vettori $n$-dimensionali sono enti algebrici, che però condividono molte proprietà degli enti geometrici elementari studiati nel piano e nello spazio. Pertanto, nello studio di $\mathbb{R}^n$, la terminologia e le intuzioni geometriche legate allo spazio ordinario risultano spesso utili.

Le operazioni di somma di due vettori e di prodotto per uno scalare godono delle stesse proprietà formali che abbiamo evidenziato [[#1.1 **Operazioni fondamentali sui vettori**|precedentemente]].

L'insieme dei vettori del piano e dello spazio possono essere identificati, rispettivamente, con $\mathbb{R}^2$ e $\mathbb{R}^3$.


#### 3.1.2 **Spazi vettoriali astratti**

Generalizzando ancora, si può dare una definizione astratta di spazio vettoriale, che si rivela utile in matematica perchè consente di trattare unitariamente molte situazioni diverse.

- #DEFINIZIONE(2). Si dice **SPAZIO VETTORIALE** su un campo numerico $\mathbb{K}$ (che per noi sarà $\mathbb{R}$ o $\mathbb{C}$) un insieme $V$ di elementi per i quali sono definite:
	
	- un'operazione di <mark class="hltr-yellow">somma</mark> che associa ad ogni coppia di elementi di $V$ un altro ed unico elemento di $V$;
	- un'operazione di <mark class="hltr-yellow">prodotto</mark> che associa ad ogni coppia formata da un elemento di $V$ e da un numero appartenente a $\mathbb{K}$ un altro ed unico elemento di $V$;
	
	Le operazioni di somma e prodotto così definite devono possedere tutte le proprietà che abbiamo elencato per le operazioni sui vettori di $\mathbb{R}^n$.
	Gli elementi di $V$ si chiamano <u>vettori</u>, gli elementi di $\mathbb{K}$ si chiamano <u>scalari</u>.

Naturalmente, l'insieme dei vettori nel piano, nello spazio, lo spazio $\mathbb{R}^n$, sono esempi di spazi vettoriali sul campo $\mathbb{R}$. L'esempio più naturale di spazio vettoriale sul campo $\mathbb{C}$, invece, è lo spazio $\mathbb{C}^n$ delle $n$-uple ordinate di numeri complessi: due $n$-uple di numeri complessi si possono sommare tra loro componente per componente, così come una $n$-upla si può moltiplicare per un numero complesso.

- #DEFINIZIONE(3). Sia $V$ uno spazio vettoriale e $V_1$ un sottoinsieme di $V$. Se $V_1$, caratterizzato dalle stesse operazioni definite in $V$, risulta essere anch'esso uno spazio vettoriale, diremo che $V_1$ è un **SOTTOSPAZIO VETTORIALE** di $V$.

- <u>Criterio di riconoscimento dei sottospazi</u>. Per verificare che un sottoinsieme $V_1$ di $V$ è un sottospazio non è necessario verificare che le operazioni abbiano le proprietà richieste (associativa, ...): se queste proprietà valgono in tutto $V$, a maggior ragione varranno in $V_1$. Invece, occorre verificare che eseguendo tali operazioni su elementi di $V_1$ non si esce da $V_1$, ovvero che: $\forall \ \mathbf{v}_1,\mathbf{v}_2 \in V_1, \ \lambda \in \mathbb{R} \quad$ si ha che $\quad \mathbf{v}_1+\mathbf{v}_2\in V_1$ e $\lambda \mathbf{v}_1\in V_1$.


#### 3.1.3 **Indipendenza lineare, base e dimensione**

In uno spazio vettoriale qualunque si può definire la nozione di <u>combinazione lineare di vettori</u>, e quella di <u>indipendenza lineare</u> in modo del tutto analogo a quanto visto per i vettori nel piano o nello spazio.

- Si dice **combinazione lineare** di $n$ vettori $\mathbf{v}_1, \mathbf{v}_2,\cdots,\mathbf{v}_n$ ogni vettore del tipo:
						$\alpha_1\mathbf{v}_1+ \alpha_2\mathbf{v}_2,\cdots,\alpha_n\mathbf{v}_n \quad$ con $\alpha_i \in \mathbb{R}$

- Si dice che $n$ vettori $\mathbf{v}_1, \mathbf{v}_2,\cdots,\mathbf{v}_n$ sono linearmente dipendenti se esiste una loro combinazione lineare, a coefficienti non tutti nulli, che dà il vettore nullo; viceversa, si dice che sono indipendenti se l'identità:
							$\alpha_1\mathbf{v}_1+ \alpha_2\mathbf{v}_2,\cdots,\alpha_n\mathbf{v}_n =\mathbf{0}$

(implica $\alpha_i =0$ per $i=1,2,\cdots,n$).

- #DEFINIZIONE(4). Sia $V$ uno spazio vettoriale, e supponiamo che esistano $n$ vettori $\mathbf{e}_1, \mathbf{e}_2,\cdots,\mathbf{e}_n$ tali che:
	1. $\mathbf{e}_1, \mathbf{e}_2,\cdots,\mathbf{e}_n$ sono linearmente indipendenti;
	2. ogni altro vettore di $V$ può scriversi come combinazione lineare di questi, ossia: per ogni $\mathbf{v}\in\mathbf{V}$ esistono $n$ coefficienti reali $v_1,v_2,\cdots,v_n$ tali che
	
								$\mathbf{v}=\sum_{i=1}^n v_i\mathbf{e}_i$
	
	Allora si dice che $\mathbf{e}_1, \mathbf{e}_2,\cdots,\mathbf{e}_n$ costituiscono una **BASE** di $V$.
	Si dimostra che, se $V$ ha una base di $n$ vettori, ogni altra base di $V$ è costituita da $n$ vettori. Diremo allora che $V$ ha **dimensione** $n$.
	
	Può accadere però che non esista alcun $n$ per cui $V$ ha una base di $n$ vettori; in tal caso si dice che $V$ ha <u>dimensione infinita</u>. Quindi, o $V$ ha dimensione infinita, oppure la sua dimensione è un numero $n$ univocamente determinato.
	La scomposizione di un vettore $\mathbf{v}$ come combinazione lineare dei vettori di una base è unica; infatti se:
						$\mathbf{v}=\sum_{i=1}^n v_i\mathbf{e}_i \quad$ e $\quad \mathbf{v}=\sum_{i=1}^n w_i\mathbf{e}_i$
	
	si ha, sottraendo, $\mathbf{0}=\mathbf{v}=\sum_{i=1}^n (v_i-w_i)\mathbf{e}_i$ che implica, per l'indipendenza dei vettori $\mathbf{e}_i$, $v_i=w_i \quad \forall i=1,2,\cdots,n$.
	
I coefficienti $v_1,v_2,\cdots,v_n$ si chiamano **componenti scalari** di $\mathbf{v}$ rispetto alla base $\mathbf{e}_1, \mathbf{e}_2,\cdots,\mathbf{e}_n$. Se la base si ritiene fissata si può individuare il vettore $\mathbf{v}$ scrivendo:
						$\mathbf{v}=(v_1,v_2,\cdots,v_n) \quad$ o $\quad \mathbf{v}=\begin{pmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{pmatrix}$

Chiameremo il primo <u>vettore riga</u> ed il secondo <u>vettore colonna</u>.


#### 3.1.4 **Spazi di funzioni**

Una classe di spazi vettoriali particolarmente importanti nello studio dell'analisi matematica è quella degli <u>spazi di funzioni</u>: sia $I\subset\mathbb{R}$ un intervallo e indichiamo con $\mathcal{F}_I$ l'insieme di tutte le funzioni $f \ : \ I\rightarrow\mathbb{R}$.
Tra queste funzioni si possono definire un'operazione di somma ed una di prodotto per uno scalare, ponendo per $f,g \ : \ I\rightarrow\mathbb{R}$ e $\lambda \in \mathbb{R}$:
							$(f+g)(x)=f(x)+g(x)$
								$(\lambda f)(x)=\lambda f(x)$.

È immediato verificare che, munito di queste operazioni, $\mathcal{F}_I$ risulta essere uno spazio vettoriale su $\mathbb{R}$. Inoltre questo spazio ha dimensione infinita (tranne nel caso in cui l'intervallo $I$ sia ridotto ad un solo punto), in quanto non esiste un numero finito di funzioni $f_i \ : \ I\rightarrow\mathbb{R}, \ i=1,2,\cdots,n$ tali che ogni altra funzione non si possa esprimere come loro combinazione lineare.

Spesso è più interessante considerare, anzichè l'insieme di tutte le funzioni possibili, l'insieme delle funzioni con qualche proprietà importante (funzioni continue, integrabili, ...).
Ad esempio, indicheremo con $C(I)$ l'insieme di tutte le funzioni $f \ : \ I\rightarrow\mathbb{R}$ continue in $I$.
Poichè ogni combinazione lineare di funzioni continue è ancora una funzione continua, in base al [[#3.1.2 **Spazi vettoriali astratti**|criterio di riconoscimento di sottospazi vettoriali]] possiamo concludere che $C(I)$ è un sottospazio di $\mathcal{F}_I$, ed in particolare esso è a sua volta uno spazio vettoriale.
Un analogo ragionamento mostra che l'insieme di tutte le funzioni derivabili in $(a,b)$ e l'insieme di tutte le funzioni integrabili in $[a,b]$ risultano essere spazi vettoriali.



### 3.2 **Prodotto scalare in $\mathbb{R}^n$**

Torniamo ora ad occuparci specificamente dello spazio $\mathbb{R}^n$. Tra i vettori del piano e dello spazio, abbiamo visto che sono definite oltre alle [[#3.1.1 **Lo spazio $ mathbb{R} n$**|due operazioni caratteristiche di ogni spazio vettoriale]], altre due operazioni: il <u>prodotto scalare</u> e, per vettori dello spazio, anche il <u>prodotto vettoriale</u>.
Mentre il secondo è un'operazione tipica di $\mathbb{R}^3$, il prodotto scalare può essere definito in $\mathbb{R}^n$:

						$(x_1,x_2,\cdots,x_n)\cdot(y_1,y_2,\cdots,y_n)=\sum_{i=1}^n x_iy_i$

Questo prodotto scalare ha le [[#1.5 **Prodotto scalare e vettoriale**|stesse proprietà formali]] che aveva nel caso di $\mathbb{R}^2$ o $\mathbb{R}^3$.
Analogamente, si dirà che in $\mathbb{R}^n$:

- Due vettori $\mathbf{u}, \mathbf{v}$ sono <mark class="hltr-yellow">ortogonali</mark> se $\mathbf{u}\cdot\mathbf{v}=\mathbf{0}$;
- Due vettori $\mathbf{u}, \mathbf{v}$ sono <mark class="hltr-yellow">paralleli</mark> se $\mathbf{u}=\lambda\mathbf{v} \quad (\lambda \in \mathbb{R})$;
- Definiamo modulo o norma di un vettore $\mathbf{v}$ il numero $|\mathbf{v}|=\sqrt{\mathbf{v}\cdot\mathbf{v}}=(\sum_{i=1}^n {v^2}_i)^\frac{1}{2}$
	
	Un vettore di modulo unitario si dice versore. Dato un vettore $\mathbf{v}$ non nullo, si definisce
								$vers(\mathbf{v})=\frac{\mathbf{v}}{|\mathbf{v}|}$.

Accade spesso di voler sostituire un vettore $\mathbf{v}$ con il corrispondente $vers(\mathbf{v})$; questa operazione si dice **normalizzazione del vettore** $\mathbf{v}$ e $vers(\mathbf{v})$ prende il nome di vettore normalizzato.

- #TEOREMA(1). Il modulo di un vettore soddisfa le proprietà seguenti $\forall \mathbf{u}, \mathbf{v} \in \mathbb{R}^n, \lambda \in \mathbb{R}$:
	1. Positività: $|\mathbf{v}|\ge0$ e $|\mathbf{v}|=0 \leftrightarrow \mathbf{v}=0$
	2. Omogeneità: $|\lambda\mathbf{v}|=|\lambda||\mathbf{v}|$
	3. Disuguaglianza triangolare: $|\mathbf{u}+\mathbf{v}|\le|\mathbf{u}|+|\mathbf{v}|$
	4. Disuguaglianza di Cauchy-Schwarz: $|\mathbf{u}\cdot\mathbf{v}|\le|\mathbf{u}||\mathbf{v}|$
	
	*Dimostrazione*:
	
	*(1)* Le prime due proprietà sono immediate. Per provare la Disuguaglianza di Cauchy-Schwarz, consideriamo il vettore $\mathbf{u}+t\mathbf{v}$, con $t\in\mathbb{R}$ qualunque. Per le proprietà del prodotto scalare si ha: $0\le(\mathbf{u}+t\mathbf{v})\cdot(\mathbf{u}+t\mathbf{v})=\mathbf{u}\cdot\mathbf{u}+2t\mathbf{u}\cdot\mathbf{v}+t^2\mathbf{v}\cdot\mathbf{v}$.
	Ricordando che $\mathbf{u}\cdot\mathbf{u}$, $\mathbf{u}\cdot\mathbf{v}$, $\mathbf{v}\cdot\mathbf{v}$ sono tre costanti, mentre $t$ è generico, si può rileggere la precedente disuguaglianza dicendo che il trinomio di secondo grado in $t$ non è mai negativo.
	CIò è possibile solo se il suo discriminante non è positivo, ovvero $(\mathbf{u}\cdot\mathbf{v})^2-(\mathbf{u}\cdot\mathbf{u})(\mathbf{v}\cdot\mathbf{v})\le 0$, cioè: $|\mathbf{u}\cdot\mathbf{v}|\le\sqrt{(\mathbf{u}\cdot\mathbf{u})(\mathbf{v}\cdot\mathbf{v})}=|\mathbf{u}|\cdot|\mathbf{v}|$, come volevasi dimostrare.
	
	*(2)* La Disuguaglianza triangolare segue dalle relazioni: $|\mathbf{u}\cdot\mathbf{v}|^2=(\mathbf{u}+\mathbf{v})\cdot(\mathbf{u}+\mathbf{v})=\mathbf{u}\cdot\mathbf{u}+2(\mathbf{u}\cdot\mathbf{v})+\mathbf{v}\cdot\mathbf{v}\le|\mathbf{u}|^2+2|\mathbf{u}||\mathbf{v}|+|\mathbf{v}|^2=(|\mathbf{u}|+|\mathbf{v}|)^2$, come volevasi dimostrare.


La nozione di modulo consente di definire la **distanza tra due vettori**:

								$d(\mathbf{v},\mathbf{w})=|\mathbf{v}-\mathbf{w}|$

le cui proprietà sono le seguenti:
	a. Positività ed annullamento: $d(\mathbf{v},\mathbf{w})\ge 0$ e $d(\mathbf{v},\mathbf{w})=0$ sse $\mathbf{v}=\mathbf{w}$;
	b. Simmetria: $d(\mathbf{v},\mathbf{w})=d(\mathbf{w},\mathbf{v})$;
	c. Disuguaglianza triangolare: $d(\mathbf{v},\mathbf{w})\le d(\mathbf{v},\mathbf{u})+d(\mathbf{u},\mathbf{w})$;

Tali proprietà seguono immediatamente dalle proprietà del modulo.



### 3.3 **Spazi vettoriali con prodotto scalare**

Facciamo ora un altro salto di astrazione, e consideriamo la possibilità di introdurre, in certi spazi vettoriali diversi da $\mathbb{R}^n$, un'operazione che goda delle stesse proprietà formali del prodotto scalare.

- #DEFINIZIONE(5). Sia $V$ uno spazio vettoriale su $\mathbb{R}$, e supponiamo che sia definita un'operazione che ad ogni coppia di vettori $\mathbf{u},\mathbf{v}\in V$ associa uno scalare $\mathbf{u}\cdot\mathbf{v}$, in modo che siano soddisfatte le [[#3.2 **Prodotto scalare in $ mathbb{R} n$**|quattro proprietà del prodotto scalare]]. Diremo allora che l'operazione $\cdot$ è un **prodotto scalare**, o $\mathbf{u},\mathbf{v}\in V,$ in $V$, e che $V$ è uno spazio vettoriale con prodotto scalare.
	- Due vettori $\mathbf{u},\mathbf{v}\in V$ si diranno <u>ortogonali</u> se $\mathbf{u}\cdot\mathbf{v}=0$;
	- Si definisce <u>modulo</u> (o norma) del vettore $\mathbf{v}$ il numero $|\mathbf{v}|=\sqrt{\mathbf{v}\cdot\mathbf{v}}$;
	- Si deginisce la <u>distanza tra due vettori</u> come: $d(\mathbf{u},\mathbf{v})=|\mathbf{u}-\mathbf{v}|$.

Si noti che la definizione di modulo ha senso grazie alla quarta proprietà del prodotto scalare, che garantisce che il radicando non sia negativo.
Continua a valere il teorema precedente: in altre parole, dagli assiomi di prodotto scalare discendono le proprietà del modulo enunciate dal teorema stesso, analogamente dalle proprietà del modulo discendono le proprietà della distanza tra due vettori.


- **Complemento ortogonale**: se $V$ è uno spazio vettoriale con prodotto interno e $V_{1}$ è un sottospazio di $V$, definiamo ${V_{1}}^{\perp}=\left\{\mathbf{v}\in V:\mathbf{v}\cdot\mathbf{u}=0 \quad \forall\mathbf{u}\in V_{1} \right\}$ 