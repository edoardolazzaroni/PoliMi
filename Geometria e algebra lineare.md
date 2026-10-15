
[Diario GAL 2024 con tutte le registrazioni ed i file note](https://polimi365-my.sharepoint.com/:x:/g/personal/10141626_polimi_it/IQD8jfWD1XOTQbJlFql3S9VRAVt_9KKDRvasFv4U1gpcGpE?e=J4XlXE)


# **Capitolo I: Vettori nel piano e nello spazio**


Il concetto di vettore, fondamentale sia in matematica che nelle applicazioni (fisiche, ecc.), può essere introdotto a vari livelli di astrazione. In questa sezione di occuperemo di vettori nel piano e nello spazio: in questo contesto, è possibile dare una definizione geometrica elementare di vettore; molte grandezze fisiche (velocità, accelerazione, forza,...) si rappresentano in questo modo. In seguito vedremo come la nozione di vettore si possa generalizzare in termini astratti, ottenendo un concetto più flessibile, che risulta molto utile per l'algebra, il calcolo infinitesimale e le loro applicazioni.

### 1.1 **Operazioni fondamentali sui vettori**

- Un vettore nel piano o nello spazio è individuato assegnando:
	a) un numero reale non negativo che esprime la sua **lunghezza** o **modulo** o intensità;
	b) una **direzione**, individuata da una retta (rette *parallele* individuano la stessa direzione);
	c) un **verso**.

Geometricamente, possiamo pensare ai vettori come a segmenti orientati, con la precisazione che due segmenti orientati che possano ottenersi l'uno dall'altro per traslazione sono lo stesso vettore.
Se nello spazio è fissato un sistema di riferimento cartesiano di cui $O$ è l'origine, possiamo anche vedere i vettori come frecce uscenti da $O$.

![[Screenshot 2026-09-16 alle 15.03.01.png|565]]
###### #Figura(1) *Vettori come frecce uscendi da $O$. $\overrightarrow{OA}$ e $\overrightarrow{PQ}$ rappresentano lo stesso vettore applicato in due punti diversi dello spazio.*


La direzione ed il verso del vettore sono allora quelli indicati dalla freccia corrispondente mentre il suo modulo coincide con la lunghezza della freccia. Per indicare un vettore potremo usare una lettera in grassetto (come **v, w**,...) oppure il simbolo $\overrightarrow{OA}$ se $A$ è la punta della freccia. Si dice anche che $\overrightarrow{OA}$ è il vettore posizione del punto A.
Due punti fissati $P$ e $Q$, nell'ordine, individuano un vettore con direzione coincidente con quella della retta passante per $P$ e $Q$, con verso da $P$ a $Q$ e con modulo pari alla lunghezza del segmento $PQ$. Il vettore individuato dai due punti $P$ e $Q$ coincide col vettore rappresentato dalla freccia $\overrightarrow{OA}$ che si ottine traslando parallelamente il segmento $PQ$ fino a far coincidere $P$ con $O$ e $Q$ con $A$; per il vettore così rappresentato si può anche usare il simbolo $\overrightarrow{PQ}$.
Sottolineiamo però che $\overrightarrow{OA}$ e $\overrightarrow{PQ}$ sono due rappresentazioni diverse dello stesso vettore **v**, una volta applicato in $O$, un'altra applicato in $P$.

- Il modulo di un vettore $\mathbf{v}$ sarà indicato con $\left | \mathbf{v} \right |$.
- Il vettore di modulo $0$ si chiama **vettore nullo** e sarà indicato con $\mathbf{0}$.

Sui vettori si possono definire varie operazioni: cominciamo ad introdurre le due fondamentali, ovvero la <u>SOMMA di VETTORI</u> ed il <u>PRODOTTO di un VETTORE per uno SCALARE</u>;

- **Somma di vettori**. Dati due vettori $\mathbf{v}=\overrightarrow{OA}$ e $\mathbf{w}=\overrightarrow{OB}$, la loro somma è definita al seguente modo: si applica $\mathbf{w}$ in $A$, cioè si scrive $\mathbf{v}=\overrightarrow{AC}$ con $C$ opportuno; allora $\mathbf{v}+\mathbf{w}=\overrightarrow{OC}$. Ne segue che $\mathbf{v}+\mathbf{w}$ si può ottenere con la ben nota regola del parallelogramma: il vettore $\mathbf{v}+\mathbf{w}$ è la diagonale del parallelogramma costruito su $\mathbf{v}$ e $\mathbf{w}$, come in figura.
	Si noti che il segmento orientato associato a $\mathbf{v}+\mathbf{w}$ è contenuto nel piano dei segmenti orientati associati a $\mathbf{v}$ e $\mathbf{w}$.

![[Geometria e Algebra Lineare-1790433438119.webp|518]]
###### #Figura(2) *Somma di due vettori.*


**PROPRIETÀ**:
	a) <mark class="hltr-yellow">Associativa</mark>: $(\mathbf{u}+\mathbf{v})+\mathbf{w}=\mathbf{u}+(\mathbf{v}+\mathbf{w})$
	b) <mark class="hltr-yellow">Commutativa</mark>: $\mathbf{u}+\mathbf{v}=\mathbf{v}+\mathbf{u}$
	c) <mark class="hltr-yellow">Vettore nullo</mark> ($\mathbf{0}$): $\mathbf{v}+\mathbf{0}=\mathbf{v}$
	d) <mark class="hltr-yellow">Vettore opposto</mark> ($-\mathbf{v}$): $\mathbf{v}+(-\mathbf{v})=0$

La somma $\mathbf{v}+(-\mathbf{w})$ si scrive semplicemente $\mathbf{v}-\mathbf{w}$, definendo in tal modo la <u>differenza tra due vettori</u>.

![[Geometria e Algebra Lineare-1790433651481.webp|372]]
###### #Figura(3) *Differenza tra vettori.*


Le proprietà appena enunciate possono essere dimostrate geometricamente, in base alla definizione di somma.
Per esempio, la prorietà commutativa dipende dal fatto che in un parallelogramma i lati opposti sono uguali e paralleli; da questo discende che $\mathbf{v}=\overrightarrow{OA}=\overrightarrow{BC}$, $\mathbf{w}=\overrightarrow{OB}=\overrightarrow{AC}$, perciò:
						$\mathbf{v}+\mathbf{w}=\overrightarrow{OA}+\overrightarrow{AC}=\overrightarrow{OC}$
						$\mathbf{w}+\mathbf{v}=\overrightarrow{OB}+\overrightarrow{BC}=\overrightarrow{OC}$

e quindi $\mathbf{v}+\mathbf{w}=\mathbf{w}+\mathbf{v}$.

Con un ragionamento geometrico analogo si può dimostrare la proprietà associativa. Le proprietà del vettore nullo e dell'opposto sono immediate.

- **Moltiplicazione di un vettore per uno scalare**. Se $\mathbf{v}$ è un vettore e $t$ è uno scalare (cioè un numero reale) il prodotto di $t$ per $\mathbf{v}$, indicato con $t\mathbf{v}$, è definito come il vettore che ha lunghezza $\left|t\right|\cdot\left|\mathbf{v}\right|$, ha la direzione di $\mathbf{v}$ e lo stesso verso se $t>0$, verso opposto se $t<0$.

![[Geometria e Algebra Lineare-1790433882898.webp|561]]
###### #Figura(4) *Moltiplicazione di $\mathbf{v}$ per $3$ e $-2$.*


**PROPRIETÀ**:
	a) $1\cdot\mathbf{v}=\mathbf{v}$
	b) $s(t\mathbf{v})=(st)\mathbf{v}$
	c) $t(\mathbf{v}+\mathbf{w})=t\mathbf{v}+t\mathbf{w}$
	d) $(s+t)\mathbf{v}=s\mathbf{v}+t\mathbf{v}$
	(con $s,t\in\mathbb{R}$)

Anche queste proprietà hanno una dimostrazione geometrica.
Per esempio, per provare la terza, si consideri la figura successiva: i triangoli $OAB$, $OCD$ sono simili per il Teorema di Talete, perchè $AB$ e $CD$ sono paralleli (rappresentando i vettori $\mathbf{w}$ e $t\mathbf{w}$). Ne segue che $OD:OB=OC:OA=t$. Ma $\overrightarrow{OD}=t\mathbf{v}+t\mathbf{w}$, $\overrightarrow{OB}=\mathbf{v}+\mathbf{w}$, perciò $t\mathbf{v}+t\mathbf{w}=t(\mathbf{v}+\mathbf{w})$.
![[Geometria e Algebra Lineare-1790434023090.webp|388]]
###### #Figura(5) *La proprietà $t(\mathbf{v}+\mathbf{w})=t\mathbf{v}+t\mathbf{w}$.*


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

![[Geometria e Algebra Lineare-1790434118867.webp|576]]
###### #Figura(6) *Le frecce $\overrightarrow{PO}$ e $\overrightarrow{OA}$ rappresentano lo stesso vettore, le cui componenti scalari sono $x=c-a,\ y=d-b$.*

Se consideriamo due vettori $\mathbf{u}=(x_1, y_1)$ e $\mathbf{v}=(x_2, y_2)$ si verifica immediatamente che $u \pm v=(x_1 \pm x_2, y_1 \pm y_2)$, e che se $t \in \mathbb{R}\rightarrow t\mathbf{u}=(t x_1,t y_1)$.

![[Geometria e Algebra Lineare-1790434380380.webp]]
###### #Figura(7) *Somma e prodotto per uno scalare, componente per componente.*


Le formule precedenti sono fondamentali in quanto permettono di eseguire le operazioni sui vettori per via analitica, senza necessità di costruzioni geometriche.
I vettori $\mathbf{i}=(1,0)$ e $\mathbf{j}=(0,1)$ sono diretti come gli assi coordinati, hanno lunghezza $\left | \mathbf{i} \right |=1=\left | \mathbf{j} \right |$ (sono <u>versori</u>) e sono <u>ortogonali</u> tra loro.
Inoltre ogni altro vettore $\mathbf{v}=(x,y)$ si può esprimere nella forma $\mathbf{v}=x\mathbf{i}+y\mathbf{j}$; $\mathbf{i}$ e $\mathbf{j}$ si dicono **VERSORI FONDAMENTALI NEL PIANO**.


### 1.3 **Vettori nello spazio**

Se introduciamo un sistema di riferimento cartesiano ortogonale nello spazio tridimensionale, con origine nel punto $O$ di riferimento, questo si può identificare con l'insieme $\mathbb{R}^3$ delle terne ordinate $(x,y,z)$ di numeri reali.
Di solito si sceglie una terna di assi ortogonali con un'orientazione destrorsa (con ciò si intende che se indice e medio della mano destra puntano rispettivamente nel verso positivo degli assi $x$ e $y$, il pollice punta nel verso positivo dell'asse $z$).

![[Geometria e Algebra Lineare-1790434560467.webp|493]]
###### #Figura(8) *Sistema di riferimento destrorso in $\mathbb{R}^3$.*


La formula della distanza tra due punti $P=(a,b,c)$ e $Q = (a',b',c')$ si estende subito nel caso bidimensionale: $\overline{PQ}=\sqrt{(a-a')^2 +(b-b')^2 + (c-c')^2}$, diagonale del parallelepipedo indicato in figura.

![[Geometria e Algebra Lineare-1790434670224.webp]]
###### #Figura(9) *Distanza tra due punti nello spazio.*


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
	
	![[Geometria e Algebra Lineare-1790434781428.webp|515]]
	###### #Figura(10) *(a) Vettori linearmente dipendenti; (b) vettori indipendenti.*


Nel caso di tre vettori $\mathbf{v_1,v_2,v_3}$, di cui per esempio $\mathbf{v_2}$ e $\mathbf{v_3}$ indipendenti, dire che $\mathbf{v_1}$ è combinazione lineare di $\mathbf{v_2}$ e $\mathbf{v_3}$ significa geometricamente che $\mathbf{v_1}$ giace nel piano individuato da $\mathbf{v_2}$ e $\mathbf{v_3}$ (quando i tre vettori hanno origine nel medesimo punto). Infatti, in tal caso $\mathbf{v_1}$ è la diagonale del parallelogramma che ha per lati due multipli di $\mathbf{v_2}$, $\mathbf{v_3}$, quindi giace nel piano individuato da $\mathbf{v_2}$, $\mathbf{v_3}$.

![[Geometria e Algebra Lineare-1790434899291.webp|508]]
###### #Figura(11) *Vettori linearmente dipendenti.*


*Per esempio*, nel piano, i vettori $\mathbf{i}=(1,0)$ e $\mathbf{j}=(0,1)$ sono linearmente indipendenti, come pure, nello spazio, i vettori $\mathbf{i}=\begin{Bmatrix}1 \\ 0 \\ 0\end{Bmatrix}, \mathbf{j}=\begin{Bmatrix}0 \\ 1 \\ 0\end{Bmatrix}, \mathbf{k}=\begin{Bmatrix}0 \\ 0 \\ 1\end{Bmatrix}$ (*riguardare formula versori fondamentali nello spazio*).
In realtà, data una qualunque terna di vettori nello spazio linearmente indipendenti, $\mathbf{v_1,v_2,v_3}$, ed un quarto vettore $\mathbf{v}$, si può sempre scrivere $\mathbf{v}=\alpha_1 \mathbf{v_1}+\alpha_2 \mathbf{v_2}+\alpha_3 \mathbf{v_3}$, con opportuni scalari $\alpha_1,\alpha_2,\alpha_3$.

Analogamente, data una qualunque coppia di vettori nel piano linearmente indipendenti, $\mathbf{v_1,v_2}$, ogni altro vettore $\mathbf{v}$ può scriversi come combinazione lineare dei primi: $\mathbf{v}=\alpha_1 \mathbf{v_1}+\alpha_2 \mathbf{v_2}$, con opportuni scalari $\alpha_1,\alpha_2$.

Dimostriamo, per esempio, quest'ultima affermazione. Siano $\mathbf{v_1}=\overrightarrow{OA}$, $\mathbf{v_2}=\overrightarrow{OB}$, $\mathbf{v}=\overrightarrow{OC}$.
Tracciando da $C$ le rette parallele ad $OA$ e $OB$, risultano individuati su tali rette due vettori, rispettivamente paralleli a $\mathbf{v_1,v_2}$, la cui somma dà $\mathbf{v}$ (per la regola del parallelogramma). Ma essendo paralleli a $\mathbf{v_1,v_2}$, tali vettori sono del tipo $\alpha_1 \mathbf{v_1},\alpha_2 \mathbf{v_2}$, per opportuni $\alpha_1,\alpha_2$.
Dunque, abbiamo provato che si ha $\mathbf{v}=\alpha_1 \mathbf{v_1}+\alpha_2 \mathbf{v_2}$.

![[Geometria e Algebra Lineare-1790435017349.webp|235]]
###### #Figura(12)

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

![[Geometria e Algebra Lineare-1790435142121.webp|551]]
###### #Figura(13) *Proiezione di $\mathbf{v}$ sulla retta $r$.*


Infatti, $\mathbf{v}\cdot\mathbf{r}=|\mathbf{v}|\cdot|\mathbf{r}|\cdot\cos\alpha=|\mathbf{v}|\cdot\cos\alpha$ e quindi $|\mathbf{v}\cdot\mathbf{r}|$ dà la lunghezza del vettore proiezione; il segno di $\mathbf{v}\cdot\mathbf{r}$ $(>0$ se $\alpha<\frac{\pi}{2}$, $<0$ se $\alpha >\frac{\pi}{2})$ determina il verso.
Nel piano, i versori $\mathbf{i}$ e $\mathbf{j}$ sono ortogonali e quindi $\mathbf{i}\cdot\mathbf{j}=0$.
In termini di componenti, dati due vettori nel piano $\mathbf{v}=x_1 \mathbf{i}+x_2 \mathbf{j}$, $\mathbf{w}=y_1 \mathbf{i}+y_2 \mathbf{j}$ si ha, usando le proprietà del prodotto scalare:
		$\mathbf{v}\cdot\mathbf{w}=x_1 \mathbf{i}+x_2 \mathbf{j}\cdot(y_1 \mathbf{i}+y_2 \mathbf{j})=x_1y_1 \mathbf{i}+x_1y_2 \mathbf{j}+x_2y_1 \mathbf{i}+x_2y_2 \mathbf{j}\cdot\mathbf{j}=x_1y_1+x_2y_2$ 

da cui l'importante **formula del prodotto scalare nel piano**: $\mathbf{v}\cdot\mathbf{w}=x_1y_1+x_2y_2$

Analogamente, nello spazio si hanno i vettori $\mathbf{v}=x_1 \mathbf{i}+x_2 \mathbf{j}+x_3 \mathbf{k}$ e $\mathbf{w}=y_1 \mathbf{i}+y_2 \mathbf{j}+y_3 \mathbf{k}$, perciò avremo come **formula del prodotto scalare nello spazio**: $\mathbf{v}\cdot\mathbf{w}=x_1y_1+x_2y_2+x_3y_3$ 

Le ultime due formule trovate risultano molto comode per il calcolo effettivo del prodotto di dui vettori di cui si conoscono le componenti, in quanto non richiedono il calcolo specifico dell'angolo formato dai vettori.


*Esempio*: Lavoro di una forza
Il lavoro compiuto da una forza costante $\mathbf{F}$ che sposta il suo punto di applicazione lungo un segmento da $A$ a $B$ è definito come il prodotto della lunghezza del segmento $AB$ per la lunghezza della componente (vettoriale) di $\mathbf{F}$ lungo la retta $AB$. In altri termini, introdotto il vettore spostamento $\mathbf{s}=\overrightarrow{AB}$, il lavoro $L$ è dato dalla formula: $L=\mathbf{F}\cdot\mathbf{s}=|\mathbf{F}|\cdot|\mathbf{s}|\cdot\cos\alpha$
dove $\alpha$ è l'angolo tra la direzione di $\mathbf{F}$ e quella della retta $AB$.
Si noti che il lavoro è nullo se $\mathbf{F}$ è ortogonale alla retta $AB$.


- **PRODOTTO VETTORIALE NELLO SPAZIO**. Dati due vettori $\mathbf{v}$ e $\mathbf{w}$, il loro <u>prodotto vettoriale</u>, denotato con $\mathbf{v}\times\mathbf{w}$, è il vettore caratterizzato dalle seguenti proprietà:
		1. La lunghezza di $\mathbf{v}\times\mathbf{w}$ è data da $|\mathbf{v}\times\mathbf{w}|=|\mathbf{v}|\cdot|\mathbf{w}|\cdot\sin\alpha$, 
			dove $\alpha$ è l'angolo che essi formano $(0\le \alpha \le \pi)$;
		2. $\mathbf{v}\times\mathbf{w}$ è perpendicolare al piano di $\mathbf{v}$ e $\mathbf{w}$;
		3. $\mathbf{v}$, $\mathbf{w}$ e $\mathbf{v}\times\mathbf{w}$, nell'ordine, formano una terna destrorsa di vettori.

![[Geometria e Algebra Lineare-1790435297190.webp|386]]
###### #Figura(14) *Prodotto vettoriale.*

**PROPRIETÀ**:
	a) <mark class="hltr-yellow">Anticommutativa</mark>: $\mathbf{v}\times\mathbf{w}=-\mathbf{w}\times\mathbf{v}$
	b) <mark class="hltr-yellow">Distributiva</mark>: $\mathbf{u}\times(\mathbf{v}+\mathbf{w})=\mathbf{u}\times\mathbf{v}+\mathbf{u}\times\mathbf{w}$
	c) Inoltre, $\forall t\in\mathbb{R}$, si ha $(t\mathbf{v})\times\mathbf{w}=t(\mathbf{v}\times\mathbf{w})$
	d) Si noti poi che $\mathbf{v}\times\mathbf{v}=0$ (essendo $\alpha=0$)
	e) Infine, $\mathbf{v}$ è **parallelo** a $\mathbf{w}$ se e solo se $\mathbf{v}\times\mathbf{w}=0$.

![[Geometria e Algebra Lineare-1790435384222.webp|406]]
###### #Figura(15) *L'area del parallelogramma costruito su $\mathbf{v}$ e $\mathbf{w}$ è $|\mathbf{v}|\cdot|\mathbf{w}|\cdot\sin\alpha=|\mathbf{v}\times\mathbf{w}|$.*



*Esempio* (1): I vettori della base canonica per $\mathbb{R}^3$, $\mathbf{i},\mathbf{j},\mathbf{k}$ formano una terna ortogonale destrorsa e pertanto si ha:

$\mathbf{i}\times\mathbf{i}=0\quad\mathbf{j}\times\mathbf{j}=0\quad\mathbf{k}\times\mathbf{k}=0\quad\mathbf{i}\times\mathbf{j}=\mathbf{k}\quad\mathbf{j}\times\mathbf{k}=\mathbf{i}\quad\mathbf{k}\times\mathbf{i}=\mathbf{j}$

Quest'ultime e le proprietà del prodotto vettoriale permettono di scrivere il prodotto vettoriale di due vettori:

$\mathbf{v}=x_{1}\mathbf{i}+x_{2}\mathbf{j}+x_{3}\mathbf{k}\quad$ e $\quad\mathbf{w}=y_{1}\mathbf{i}+y_{2}\mathbf{j}+y_{3}\mathbf{k}$

in termini delle loro componenti. Infatti si ha:

$\begin{align}\mathbf{v}\times\mathbf{w}&=(x_{1}\mathbf{i}+x_{2}\mathbf{j}+x_{3}\mathbf{k})\times(y_{1}\mathbf{i}+y_{2}\mathbf{j}+y_{3}\mathbf{k})=\\&=x_{1}y_{1}\mathbf{i}\times\mathbf{i} + x_{1}y_{2}\mathbf{i}\times\mathbf{j}+x_{1}y_{3}\mathbf{i}\times\mathbf{k}+\\&+ x_{2}y_{1}\mathbf{j}\times\mathbf{i}+x_{2}y_{2}\mathbf{j}\times\mathbf{j}+x_{2}y_{3}\mathbf{j}\times\mathbf{k}+\\&+ x_{3}y_{1}\mathbf{k}\times\mathbf{i}+x_{3}y_{2}\mathbf{k}\times\mathbf{j}+x_{3}y_{3}\mathbf{k}\times\mathbf{k}=\\&=(x_{2}y_{3}-x_{3}y_{2})\mathbf{i}+(x_{3}y_{1}-x_{1}y_{3})\mathbf{j}+(x_{1}y_{2}-x_{2}y_{1})\mathbf{k}\end{align}$

da cui l'<mark class="hltr-yellow">importante formula</mark>: $\mathbf{v}\times\mathbf{w}=(x_{2}y_{3}-x_{3}y_{2})\mathbf{i}+(x_{3}y_{1}-x_{1}y_{3})\mathbf{j}+(x_{1}y_{2}-x_{2}y_{1})\mathbf{k}$

Nel [[#4.3 **Determinante**|paragrafo 4.3]] vedremo come questa formula si possa riscrivere in modo più sintetico usando la nozione di determinante di una matrice.


*Esempio* (2): Momento di una forza rispetto ad un punto
Sia $\mathbf{F}$ una forza con punto di applicazione $A$. Il momento di $\mathbf{F}$ rispetto ad un punto $O\ne A$ è definito dal vettore:
$\mathbf{M}=\mathbf{r}\times\mathbf{F}\quad$ dove $\mathbf{r}=\overrightarrow{OA}$.


- **PRODOTTO MISTO NELLO SPAZIO**. Se $\mathbf{u}$, $\mathbf{v}$ e $\mathbf{w}$ sono tre vettori nello spazio, il loro <u>prodotto misto</u> è definito dal numero reale $\mathbf{u}\cdot(\mathbf{v}\times\mathbf{w})$
		La parentesi è in realtà superflua, in quanto $(\mathbf{u}\cdot\mathbf{v})\times\mathbf{w}$ non ha senso. Si può perciò scrivere semplicemente $\mathbf{u}\cdot\mathbf{v}\times\mathbf{w}$.
		Si dimostra in seguito che il prodotto misto non varia permutando ciclicamente i tre vettori $\mathbf{u}$, $\mathbf{v}$ e $\mathbf{w}$: $\mathbf{u}\cdot\mathbf{v}\times\mathbf{w}=\mathbf{w}\cdot\mathbf{u}\times\mathbf{v}=\mathbf{v}\cdot\mathbf{w}\times\mathbf{u}$

Geometricamente, il valore assoluto del prodotto misto rappresenta il volume del parallelepipedo costruito sui vettori $\mathbf{u}$, $\mathbf{v}$ e $\mathbf{w}$,

![[Geometria e Algebra Lineare-1790435527270.webp|338]]
###### #Figura(16) *$\quad|\mathbf{u}\cdot(\mathbf{v}\times\mathbf{w})|=$ volume del parallelepipedo*


infatti si ha $volume = altezza \cdot area \ di  \ base$.
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


*Esempio*: Verificare se i vettori $(1,2,3),(0,2,2),(2,1,2)$ sono indipendenti oppure no.
Calcoliamo:

$(0,2,2)\cdot(1,2,3)\times(2,1,2)=2(3\cdot 2-1\cdot 2)+2(1\cdot 1-2\cdot 2)=2\cdot 4+2\cdot(-3)=2\ne 0$

I vettori sono perciò indipendenti.




# **Capitolo II: Geometria lineare nello spazio**


Mediante il calcolo vettoriale introdotto nei paragrafi precedenti è facile scrivere, in un dato sistema di riferimento, vari tipi di equazioni per rette e piani.

### 2.1 **Equazione della retta**

Una retta nello spazio è individuata da:
	a) un punto e un vettore direzionale;
	b) due punti;
	c) intersezione di due piani non paralleli.


a) Cominciamo col primo caso. Consideriamo un punto $P_0(x_0,y_0,z_0)$ ed un vettore $\mathbf{v}=(a,b,c)$ non nullo; ci proponiamo di scrivere l'equazione della retta passante per $P_0$, parallela a $\mathbf{v}$.

![[Geometria e Algebra Lineare-1791120505287.webp|512]]
###### #Figura(17)


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

![[Geometria e Algebra Lineare-1791120647041.webp|553]]
###### #Figura(18)


- **Condizioni di parallelismo ed ortogonalità tra rette**

Due rette sono **parallele** se i loro vettori direzionali sono paralleli (linearmente indipendenti). Precisamente, le due rette

$\begin{cases} x=x_0+ta\\ y=y_0+tb \\ z=z_0+tc \end{cases}\quad$ e $\quad\begin{cases} x=x_1+ta' \\ y=y_1+tb' \\ z=z_1+tc' \end{cases}$

sono parallele se $\exists\lambda\ne0$ t.c. $(a',b',c')=\lambda(a,b,c)$.
Le due rette sono **ortogonali** se lo sono i loro vettori direzionali, cioè se $(a',b',c')\cdot(a,b,c)=aa'+bb'+cc'\equiv0$.

Si noti che per essere ortogonali non è necessario che le due rette siano **incidenti** (cioè si intersechino in un punto).


*Esempio*: Si voglia calcolare l'equazione della retta passante per i due punti $P_{0}=(3,-1,1),P_{1}=(4,2,-3)$. Come vettore direzionale si può prendere $\mathbf{v}=\overrightarrow{P_{0}P_{1}}=(1,3,-4)$.

L'equazione parametrica vettoriale è dunque: $(x,y,z)=(3,-1,1)+t(1,3,-4)\quad t\in\mathbb{R}$

Le equazioni scalari sono: ${\begin{cases}x=3+t \\  y=-1+3t \\  z=1-4t\end{cases}}\quad t\in\mathbb{R}$

Infine, quelle cartesiane sono: $\frac{x-3}{1}=\frac{y+1}{3}=\frac{z-1}{-4}$

Questa retta è parallela alla retta ${\begin{cases}x=2+4t \\  y=1+12t \\  z=-16t\end{cases}}\quad$, in quanto $(4,12,-16)=4(1,3,-4)$, e ortogonale alla retta ${\begin{cases}x=2-2t \\  y=2t \\  z=5+t\end{cases}}\quad$, in quanto $(-2,2,1)\cdot(1,3,-4)=-2+6-4=0$.



c) Prima di vedere come si scrive l'equazione di una retta come intersezione di due piani, vediamo come si scrive l'equazione di un piano.


### 2.2 **Equazione del piano**

Un piano è individuato da:
	a) un punto ed un vettore ortogonale al piano stesso;
	b) tre punti;
	c) due rette incidenti.


a) Cominciamo col primo caso. Consideriamo un punto $P_0(x_0,y_0,z_0)$ ed un vettore $\mathbf{n}=(a,b,c)$ non nullo; ci proponiamo di determinare l'equazione del piano passante per $P_0 \perp \mathbf{n}$.

![[Geometria e Algebra Lineare-1791120747253.webp|414]]
###### #Figura(19)


Dalla figura si vede che se $P=(x,y,z)$ è il generico punto del piano, allora il vettore $\overrightarrow{P_0P}$ è parallelo al piano e quindi $\perp \mathbf{n}$. Si ottiene allora l'equazione vettoriale:
								$\mathbf{n}\cdot\overrightarrow{P_0P}=0$

L'equazione cartesiana del piano si ottiene passando dai vettori alle coordinate, cioè:
					$a(x-x_0)+b(y-y_0)+c(z-z_0)=0$

ossia dove $\begin{cases} ax+by+cz=d \\ d=\mathbf{n}\cdot\mathbf{p}_0=ax_0+by_0+cz_0 \end{cases}$

Facciamo qualche **osservazione**:
- Se $a^2+b^2+c^2=1$, cioè $\mathbf{n}$ è un versore, allora $a,b,c$ sono i <u>coseni direttori</u> del piano;
- Se $d=0$, il piano passa per l'origine $O=(0,0,0)$;
- Se uno dei coefficienti $a,b,c$ è nullo, il piano è parallelo ad uno degli assi coordinati. Per esempio, se $c=0$ il piano è parallelo all'asse $z$, e quindi è perpendicolare al piano $(x,y)$;
	Si noti che l'equazione $ax+by=d$, che nel piano rappresenta una retta, nello spazio rappresenta un piano perpendicolare al piano $(x,y)$.
- Se due coefficienti sono nulli, allora il piano è parallelo ad uno dei piani coordinati. Per esempio, se $a=b=0$, il piano ha equazione $z=k$ ed è parallelo al piano $(x,y)$;
- Se $d\ne0$, si può dividere l'equazione cartesiana precedente per $d$, ottenendo così:
								$\frac{x}{\alpha}+\frac{y}{\beta}+\frac{z}{\gamma}=1$
	In tal caso $\alpha, \beta, \gamma$ rappresentano le intercette del piano con gli assi coordinati.

![[Geometria e Algebra Lineare-1791120841013.webp|510]]
###### #Figura(20)


*Esempio* (1): Si voglia scrivere l'equazione del piano passante per il punto $(1,2,-1)$ e normale al vettore $\mathbf{v}=(2,3,0)$.

L'equazione è $(x-1,y-2,z+3)\cdot(2,3,0)=0$
cioè $2(x-1)+3(y-2)=0\rightarrow 2x+3y-8=0$

Nel caso (b) si vuole scrivere l'equazione del piano passante per i punti $P_{0}=(x_{0},y_{0},z_{0}), P_{1}=(x_{1},y_{1},z_{1}), P_{2}=(x_{2},y_{2},z_{2})$

Per ricondurci al caso (a) individuiamo un vettore ortogonale al piano.
I vettori $\mathbf{v}=\overrightarrow{P_{0}P_{1}}=(x_{1}-x_{0},y_{1}-y_{0},z_{1}-z_{0})$ e $\mathbf{w}=\overrightarrow{P_{0}P_{2}}=(x_{2}-x_{0},y_{2}-y_{0},z_{2}-z_{0})$ sono paralleli al piano e perciò il loro prodotto vettoriale sarà ortogonale al piano stesso. Poniamo:

$\mathbf{n}=\mathbf{v}\times\mathbf{w}$

Scegliendo poi, per esempio, $P_{0}$, l'equazione del piano è: $\mathbf{n}\cdot\overrightarrow{P_{0}P}=0$



*Esempio* (2): Si voglia calcolare l'equazione del piano passante per i tre punti $A=(1,0,-1),B=(2,1,0),C=(0,1,-2)$.

Per usare la formula $\mathbf{n}\cdot\overrightarrow{P_0P}=0$ occorre individuare un vettore normale al piano. Poichè i vettori $\mathbf{v}=\overrightarrow{AB}=(1,1,1),\mathbf{w}=\overrightarrow{AC}=(-1,1,-1)$ sono paralleli al piano, il loro prodotto vettoriale sarà ortogonale al piano stesso. Scegliamo però:

$\mathbf{n}=\mathbf{v}\times\mathbf{w}=-2\mathbf{i}+2\mathbf{k}$

Abbiamo quindi, scegliendo $P_{0}=A$: $-2(x-1)+2(z-1)=0$, ossia $-x+z+2=0$

Nel caso (c), per scrivere l'equazione del piano contente le due rette $\mathbf{p}=\mathbf{p}_{0}+t\mathbf{v},\mathbf{p}=\mathbf{p}_{0}+t\mathbf{w}$, incidenti in $P_{0}$ ma distinte ($\mathbf{v},\mathbf{w}$ indipendenti), è sufficiente applicare il ragionamento del caso (b), ottenendo l'equazione:

$(\mathbf{p}-\mathbf{p}_{0})\cdot(\mathbf{v}\times\mathbf{w})=0$



*Esempio* (3): Stabilire se le seguenti rette $P=(4,-2,2)+t(1,-1,0)$ e $P=(1,1,2)+t(2,1,3)$ sono complanari o sghembe e, nel primo caso, scrivere l'equazione del piano che le contiene.

I vettori $(1,-1,0),(2,1,3)$ evidentemente non sono paralleli, perciò le rette sono complanari se e solo se sono incidenti. Stabiliamo se lo sono cercando se esistono valori dei parametri $t,u$ per cui si abbia:

$(4,-2,2)+t(1,-1,0)=(1,1,2)+u(2,1,3)\rightarrow{\begin{cases}t-2u=-3 \\  -t-u=3 \\  3u=0\end{cases}}$

che dà $u=0,t=-3$. Per questi valori dei parametri le rette si incontrano in $P_{0}=(1,1,2)$, dunque le rette sono incidenti e le loro equazioni si possono riscrivere, evidenziando il punto comune $P_{0}$, nella forma:

$P=(1,1,2)+t(1,-1,0)$ e $P=(1,1,2)+t(2,1,3)$

A questo punto la determinazione del piano che le contiene si può fare come illustrato al punto (c):

$(x-1,y-1,z-2)\cdot((1,-1,0)\times(2,1,3))=0\rightarrow-3(x-1)-3(y-1)+3(z-2)=0$

e quindi: $z-x-y=0$.



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


*Esempio*: Scriviamo le equazioni parametriche della retta intersezione dei piani: ${\begin{cases}x+y+z=1 \\  x-2y-z=2\end{cases}}$

Ricaviamo: ${\begin{cases}x+y=1-z \\  x-2y=2+z\end{cases}}\rightarrow{\begin{cases}y=\frac{-1-2z}{3} \\  x=\frac{4-z}{3}\end{cases}}$

da cui, ponendo $z=t$ otteniamo le equazioni parametriche della retta: ${\begin{cases}x=\frac{4}{3}-\frac{1}{3}t \\  y=-\frac{1}{3}-\frac{2}{3}t \\  z=t\end{cases}}$



- **Distanza di un punto da piano**

Si voglia calcolare la distanza $\delta$ di un punto $P_1(x_1,y_1,z_1)$ dal piano passante per $P_0=(x_0,y_0,z_0)$ ed ortogonale al vettore $\mathbf{n}=(a,b,c)$. Dalla figura si vede che $\delta$ è la lunghezza del segmento $P_2P_1$ uguale alla lunghezza della proiezione di $P_0P_1$ lungo la direzione $\mathbf{n}$.



Se si introduce il versore $\mathbf{N}=\frac{1}{\sqrt{a^2+b^2+c^2}}(a,b,c)$, la lunghezza della proiezione è il modulo del prodotto scalare tra $\mathbf{N}$ ed il vettore $\overrightarrow{P_0P_1}$, cioè:

$\delta=|\mathbf{N}\cdot\overrightarrow{P_0P_1}|=\frac{|a(x_1-x_0)+b(y_1-y_0)+c(z_1-z_0)|}{\sqrt{a^2+b^2+c^2}}$

ossia, ricordando che abbiamo posto $d=ax_0+by_0+cz_0$:

							$\delta=\frac{|ax_1+by_1+cz_1-d|}{\sqrt{a^2+b^2+c^2}}$




# **Capitolo III: Spazi vettoriali**


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



*Esempio* (1): In $\mathbb{R}^2$ la coppia $\mathbf{i},\mathbf{j}$ costituisce una base, detta canonica. Analogamente, la terna $\mathbf{i},\mathbf{j},\mathbf{k}$ è la base canonica di $\mathbb{R}^{3}$. Più in generale, in $\mathbb{R}^n$ consideriamo la $n$-upla di vettori:




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


- **Complemento ortogonale**: se $V$ è uno spazio vettoriale con prodotto interno e $V_{1}$ è un sottospazio di $V$, definiamo

						${V_{1}}^{\perp}=\left\{\mathbf{v}\in V:\mathbf{v}\cdot\mathbf{u}=0 \quad \forall\mathbf{u}\in V_{1} \right\}$
	
	In altre parole, ${V_{1}}^{\perp}$ è <mark class="hltr-yellow">l'insieme dei vettori che sono ortogonali</mark> a tutti i vettori di $V_{1}$.
	Si verifica facilmente che tale insieme è un sottospazio di $V$, che prende il nome di <u>complemento ortogonale</u> di $V_{1}$.
	Più in generale, <u>due sottospazi</u> $U$ e $W$ di $V$ si dicono ortogonali se ogni vettore di $U$ è ortogonale ad ogni vettore di $W$:
							$\mathbf{u}\cdot\mathbf{w}=0 \quad \forall \mathbf{u}\in U, \mathbf{w}\in W$


#### 3.3.1 **Basi ortonormali**

Consideriamo uno spazio vettoriale di dimensione finita, dotato di prodotto scalare.
Fissata una base $\mathbf{e}_1, \mathbf{e}_2,\cdots,\mathbf{e}_n$ calcoliamo il prodotto scalare di due vettori

$\mathbf{u}=\sum_{i=1}^n u_i\mathbf{e}_i$ e $\mathbf{v}=\sum_{j=1}^n v_j\mathbf{e}_j$

Applicando le proprietà del prodotto scalare si ha: 

$\mathbf{u}\cdot\mathbf{v}=(\sum_{i=1}^n u_i\mathbf{e}_i)\cdot(\sum_{j=1}^n v_j\mathbf{e}_j)=\sum_{i,j=1}^n u_{i}v_j\mathbf{e}_i\mathbf{e}_j$

È sufficiente quindi conoscere gli $n^2$ prodotti scalare $\mathbf{e}_i\cdot\mathbf{e}_j$ per poter calcolare il prodotto scalare di due vettori qualsiasi. Il calcolo risulta particolarmente comodo quando gli $n$ vettori della base risultano **ortonormali**, ossia:

1) Sono a due a due ortogonali: $\mathbf{e}_i\cdot\mathbf{e}_j=0$ per $i\ne j$;
2) Ogni vettore ha modulo unitario: $|\mathbf{e}_i|^2=\mathbf{e}_i\cdot\mathbf{e}_j=1$ per $i=1,\cdots,n$;

Una tale base si dice **base ortonormale**, e gioca un ruolo fondamentale nello studio degli spazi con prodotto scalare. In tal caso infatti si ottiene:

$\mathbf{u}\cdot\mathbf{v}=(\sum_{i=1}^n u_i\mathbf{e}_i)\cdot(\sum_{j=1}^n v_j\mathbf{e}_j)=\sum_{i=1}^n u_{i}v_i$

ovvero: il prodotto scalare di ottiene dalle componenti dei due vettori con la stessa formula che vale nel caso del prodotto scalare euclideo in $\mathbb{R}^n$. In particolare, per $\mathbf{u}=\mathbf{v}$ si ha:

							$|\mathbf{u}|^2=\mathbf{u}\cdot\mathbf{u}=\sum_{i=1}^n {u_{i}}^2$

ovvero anche il modulo di un vettore si calcola mediante le sue componenti con la stessa formula che vale nel caso euclideo.
L'ultima proprietà si può esprimere anche nel seguente modo: se $\mathbf{v}_1, \mathbf{v}_2,\cdots,\mathbf{v}_n$ sono vettori a due a due ortogonali (di modulo qualsiasi), si ha:

$|\sum_{i=1}^n v_i|^2=\sum_{i=1}^n |v_i|^2$

che è una sorta di Teorema di Pitagora in forma astratta.
Per esempio, in $\mathbb{R}^n$ la base canonica è anche una base ortonormale rispetto al prodotto scalare euclideo.

Si può dimostrare che <mark class="hltr-yellow">uno spazio vettoriale di dimensione finita e dotato di prodotto scalare ha sempre una base ortonormale</mark>:

- #TEOREMA(2). **Procedimento di ortonormalizzazione di Gram-Schmidt**
	
	Sia $V$ uno spazio vettoriale di dimensione finita $n$, dotato di prodotto interno. Allora:
	
	1. $V$ ha una base ortonormale;
	2. In particolare, se $V_{1}$ è un sottospazio di $V$ di dimensione $m<n$, si può costruire una base ortonormale di $V$ del tipo $\mathbf{u}_1, \mathbf{u}_2,\cdots,\mathbf{u}_n$ dove i primi $m$ vettori $\mathbf{u}_1, \mathbf{u}_2,\cdots,\mathbf{u}_m$ sono una base ortonormale di $V_{1}$ e gli ultimi $n-m$ vettori $\mathbf{u}_{m+1}, \mathbf{u}_2,\cdots,\mathbf{u}_n$ sono una base ortonormale di ${V_{1}}^{\perp}$.
	
	Invece di presentare la dimostrazione astratta, illustriamo con un *esempio numerico* il procedimento di ortonormalizzazione.
	Consideriamo in $\mathbb{R}^3$ i due vettori indipendenti $\mathbf{v}_{1}=(1,0,-1)$ e $\mathbf{v}_{2}=(0,1,-1)$;
	detto $V$ il sottospazio vettoriale di $\mathbb{R}^3$ generato da $\mathbf{v}_{1},\mathbf{v}_{2}$ (che come si verifica non è altro che il piano passante per l'origine di equazione $x+y+z=0$), proponiamoci di costruire una base ortonormale di $V$, ossia di ortonormalizzare la base $\mathbf{v}_{1},\mathbf{v}_{2}$. I passi sono i seguenti:
	
	1) Normalizziamo $\mathbf{v}_{1}$, definendo: $\mathbf{u}_{1}=\frac{\mathbf{v}_{1}}{|\mathbf{v}_{1}|}=\left( \frac{1}{\sqrt{2}},0,-\frac{1}{\sqrt{2}} \right)$;
	
	2) Calcoliamo la componente di $\mathbf{v}_{2}$ nella direzione di $\mathbf{u}_{1}$, data da:
						$(\mathbf{v}_{2}\cdot\mathbf{u}_{1})\mathbf{u}_{1}=\frac{1}{\sqrt{2}}\left( \frac{1}{\sqrt{2}},0,-\frac{1}{\sqrt{2}} \right)=\left( \frac{1}{2},0,-\frac{1}{2} \right)$
	
	3) Sottraiamo a $\mathbf{v}_{2}$ la sua componente nella direzione di $\mathbf{u}_{1}$, ottenendo così un vettore ortogonale a $\mathbf{u}_{1}$ e che insieme ad esso genera $V$:
					$\mathbf{v}_{2}-(\mathbf{v}_{2}\cdot\mathbf{u}_{1})\mathbf{u}_{1}=(0,1,-1)-\left( \frac{1}{2},0,-\frac{1}{2} \right)=\left( -\frac{1}{2},1,-\frac{1}{2} \right)$
	
	4) Normalizziamo quest'ultimo vettore, definendo:
					$\mathbf{u}_{2}=\frac{\left( \frac{1}{2},1,-\frac{1}{2} \right)}{\sqrt{\frac{1}{4}+1+\frac{1}{4}}}=\sqrt{\frac{2}{3}}\left( -\frac{1}{2},1,-\frac{1}{2} \right)=\left( -\frac{1}{\sqrt{6}},\sqrt{\frac{2}{3}},-\frac{1}{\sqrt{6}} \right)$
		
		Il lettore verifichi che $\mathbf{u}_{1},\mathbf{u}_{2}$ costituiscono effettivamente una base ortonormale di $V$.
		Se ora volessimo costruire una base ortonormale di $\mathbb{R}^3$ che abbia come primi elementi $\mathbf{u}_{1},\mathbf{u}_{2}$, dovremmo iterare il procedimento come segue:
	
	1) Scegliamo un vettore di $\mathbb{R}^3$ indipendente da $\mathbf{u}_{1},\mathbf{u}_{2}$, per esempio $\mathbf{v}_{3}=(0,0,1)$;
	
	2) Sottraiamo a $\mathbf{v}_{3}$ la sua proiezione su $V$, ossia calcoliamo:
	$\mathbf{v}_{3}'=\mathbf{v}_{3}-{(\mathbf{v}_{3}\cdot\mathbf{u}_{1})\mathbf{u}_{1}+(\mathbf{v}_{3}\cdot\mathbf{u}_{2})\mathbf{u}_{2}}=(0,0,1)-\left\{ -\frac{1}{\sqrt{2}}\left( \frac{1}{\sqrt{2}},0,-\frac{1}{\sqrt{2}}\right)-\frac{1}{\sqrt{6}}(-\frac{1}{\sqrt{6}},\sqrt{\frac{2}{3}},-\frac{1}{\sqrt{6}}) \right\}=\left( \frac{1}{3},\frac{1}{3},\frac{1}{3} \right)$
	3) Normalizziamo $\mathbf{v}_{3}'$, ottenendo:
							$\mathbf{u}_{3}=\frac{\left( \frac{1}{3},\frac{1}{3},\frac{1}{3} \right)}{\sqrt{\frac{1}{3}}}=\left( \frac{1}{\sqrt{3}},\frac{1}{\sqrt{3}},\frac{1}{\sqrt{3}} \right)$
	
	Il lettore verifichi che $\mathbf{u}_{3}$ è ortogonale a $\mathbf{u}_{1},\mathbf{u}_{2}$ ed ha modulo unitario, perciò $\mathbf{u}_{1},\mathbf{u}_{2},\mathbf{u}_{3}$ sono una base ortonormale di $\mathbb{R}^3$, i cui primi due elementi sono una base ortonormale di $V$.
	
	Più in generale, l'*algoritmo iterativo* di ortonormalizzazione di un sistema $\mathbf{v}_{1},\mathbf{v}_{2},\cdots,\mathbf{v}_{n}$ di vettori linearmente indipendenti è il seguente:
	
		$\mathbf{u}_{1}=vers(\mathbf{v}_{1})$
		$\mathbf{u}_{k}=vers(\mathbf{v}_{k}-\sum_{j=1}^{k-1} (\mathbf{u}_{j}\cdot\mathbf{v}_{k})\mathbf{u}_{j}) \quad$ per $k=2,3,\cdots,n$.
	
	Lo studente è invitato a dimostrare che i vettori $\mathbf{u}_{1},\mathbf{u}_{2},\cdots,\mathbf{u}_{n}$ così costruiti sono effettivamente ortonormali. Si noti che il sistema di vettori ortonormali $\mathbf{u}_{1},\mathbf{u}_{2},\cdots,\mathbf{u}_{n}$ non dipende solo dal sistema di vettori $\mathbf{v}_{1},\mathbf{v}_{2},\cdots,\mathbf{v}_{n}$ di partenza, ma anche dall'ordine in cui li consideriamo.


- #TEOREMA(3). **Proiezione ed elemento di minima distanza**
	
	Sia $V$ uno spazio dotato di prodotto scalare, $V_{1}$ un sottospazio di $V$ di dimensione finita e $\mathbf{v}$ un elemento di $V$ che non appartiene a $V_{1}$; allora esistono e sono univocamente determinati due vettori $\mathbf{u},\mathbf{w}$ tali che:
							$\mathbf{v}=\mathbf{u}+\mathbf{w} \quad$, con $\mathbf{u}\in V_{1}$ e $\mathbf{w}\in {V_{1}}^\perp$
	Il vettore $\mathbf{u}$ si dirà proiezione ortogonale di $\mathbf{v}$ su $V_{1}$ e, tra i vettori di $V_{1}$, è quello di minima distanza da $\mathbf{v}$.
	
	Si noti che in questo enunciato lo spazio ambiente $V$ può anche avere dimensione infinita, mentre $V_{1}$ per ipotesi ha dimensione finita.
	
	*Dimostrazione*:
	
	Poichè $V_{1}$ è uno spazio vettoriale di dimensione finita con prodotto interno, per il [[#teorema|teorema]] esiste una base ortonormale $\mathbf{e}_{1},\mathbf{e}_{2},\cdots,\mathbf{e}_{n}$ di $V_{1}$. Utilizzando questa base definiamo il vettore
	
								$\mathbf{u}=|^2=\sum_{i=1}^n (\mathbf{v}\cdot\mathbf{e}_{i})e_{i}$
		
	che rappresenta la proiezione di $\mathbf{v}$ su $V_{1}$. Poniamo anche $\mathbf{w}=\mathbf{v}-\mathbf{u}$.
	Dalle definizioni segue subito che $\mathbf{u}\in V_{1}$ e $\mathbf{v}=\mathbf{u}+\mathbf{w}$; proviamo che $\mathbf{w}\in {V_{1}}^\perp$.
	È sufficiente dimostrare l'ortogonalità di $\mathbf{w}$ a ciascun elemento $\mathbf{e}_{j}$ della base di $V_{1}$, in quanto l'ortogonalità a qualunque vettore di $V_{1}$ seguirà per linearità. Si ha:
	
		$\mathbf{w}\cdot\mathbf{e}_{j}=(\mathbf{v}-\mathbf{u})\cdot\mathbf{e}_{j}=\mathbf{v}\cdot\mathbf{e}_{j}-(\sum_{i=1}^n (\mathbf{v}\cdot\mathbf{e}_{i})\mathbf{e}_{i})\cdot\mathbf{e}_{j}=\mathbf{v}\cdot\mathbf{e}_{j}-\sum_{i=1}^n (\mathbf{v}\cdot\mathbf{e}_{i})(\mathbf{e}_{i}\cdot\mathbf{e}_{j})$
		
	essendo $\mathbf{e}_{i}\cdot\mathbf{e}_{j}=0$ per $i\ne j$ e $\mathbf{e}_{i}\cdot\mathbf{e}_{i}=1, \quad =\mathbf{v}\cdot\mathbf{e}_{j}-(\mathbf{v}\cdot\mathbf{e}_{j})=0$,
	
	dunque $\mathbf{w}\in {V_{1}}^\perp$. Per mostrare che $\mathbf{u}$ è l'elemento di $V_{1}$ di minima distanza da $\mathbf{v}$, sia $\mathbf{u}_{1}$ un altro generico elemento di $V_{1}$. Essendo:
	
								$\mathbf{v}-\mathbf{u}_{1}=\mathbf{w}+(\mathbf{u}-\mathbf{u}_{1})$
	
	con $(\mathbf{u}-\mathbf{u}_{1})\in V_{1}$ e $\mathbf{w}\in V_{1}^\perp$, per il Teorema di Pitagora si ha:
	
				$|\mathbf{v}-\mathbf{u}_{1}|^2=|\mathbf{w}+(\mathbf{u}-\mathbf{u}_{1})|^2=|\mathbf{w}|^2+|\mathbf{u}-\mathbf{u}_{1}|^2\ge|\mathbf{w}|^2=|\mathbf{v}-\mathbf{u}|^2$
	
	quindi la distanza di $\mathbf{v}$ da $\mathbf{u}$ è minore della distanza da $\mathbf{v}$ da qualunque altro elemento di $\mathbf{u}_{1}$ di $V_{1}$ (come volevasi dimostrare).


#### 3.3.2 **Somma diretta di sottospazi ortogonali**

Sia $V$ uno spazio vettoriale qualsiasi. Dati due sottospazi $U$ e $W$ qualunque, se ne possono formare altri due particolarmente significativi:

- $V \cap W$, ovvero l'**intersezione**;
- $V+W=\left\{\mathbf{v}+\mathbf{w}:\mathbf{v}\in V, \mathbf{w}\in W\right\}$, che coincide con il sottospazio generato da $V\cup W$.

Vale il seguente risultato: 

- #PROPOSIZIONE(1). Dati due sottospazi $U$ e $W$ di $V$, vale la **formula**:

					$dim(U+W)=dim U+ dim W - dim (U\cap W)$

Supponiamo ora che $V$ sia uno spazio vettoriale dotato di prodotto scalare. Se i sottospazi $U$ e $W$ sono ortogonali, si ha evidentemente $U\cap W=\left\{\mathbf{0}\right\}$, per cui:

						$dim(U+W)=dim U + dim W$

Naturalmente non è detto che risulti $U+W=V$. Quando questo accade, la circostanza merita una definizione ed una notazione speciale:

- #DEFINIZIONE(6). Si dice che $V$ è **somma diretta** dei sottospazi ortogonali $U$ e $W$ e si scrive:

								$V=U\oplus W$
	
	Se ogni vettore $\mathbf{v}\in V$ si può scrivere univocamente nella forma $\mathbf{v}=\mathbf{u}+\mathbf{w}$, con $\mathbf{u}\in U,\mathbf{w}\in W$.

- #PROPOSIZIONE(2). Se $V=U\oplus W$, i due sottospazi $U,W$ sono uno il complemento ortogonale dell'altro.
	
	*Dimostrazione*:
	
	Facciamo vedere che, se $V=U\oplus W$, allora $W=U^\perp$.
	Ovviamente si ha $W\subseteq U^\perp$, perchè $W$ è ortogonale a $U$. Viceversa, sia $\mathbf{v}\in U^\perp$ e, in base alla definizione precedente, scriviamolo nella forma $\mathbf{v}=\mathbf{u}+\mathbf{w}$.
	Facendo prodotto scalare con $\mathbf{u}$ si ottiene $\mathbf{v}\cdot\mathbf{u}=\mathbf{u}\cdot\mathbf{u}+\mathbf{w}\cdot\mathbf{u}$.
	
	Ma $\mathbf{v}\cdot\mathbf{u}=0$ essendo $\mathbf{v}$ ortogonale a $U$ e $\mathbf{w}\cdot\mathbf{u}=0$ perchè $W$ e $U$ sono ortogonali.
	Si deduce che $\mathbf{u}\cdot\mathbf{u}=|\mathbf{u}|^2=0$ che implica $\mathbf{u}=\mathbf{0}$; ma allora $\mathbf{v}=\mathbf{w}\in W$ e perciò $U^\perp\subseteq W$.
	
	Nella definizione precedente $\mathbf{u}$ è la proiezione di $\mathbf{v}$ su $U$, mentre $\mathbf{w}$ è la proiezione di $\mathbf{v}$ su $W$ e vale il Teorema di Pitagora: $|\mathbf{v}|^2=|\mathbf{u}|^2+|\mathbf{w}|^2$.


#### 3.3.3 **Il concetto di linearità**

Nel secondo capitolo abbiamo introdotto il concetto generale di funzione tra due insiemi, come legge che associa univocamente ad un dato "ingresso" una certa "uscita".
Ci occupiamo ora del caso in cui gli insiemi in questione siano due spazi vettoriali $V_{1},V_{2}$; una funzione $f$ di dominio $V_{1}$ e codominio $V_{2}$, $\ f:\ V_{1}\rightarrow V_{2}$ sarà dunque una legge che ad ogni vettore di $V_{1}$ associa uno ed un sol vettore di $V_{2}$.
Tra queste funzioni, particolare importanza hanno quelle che godono di una speciale proprietà, detta <u>linearità</u>:

- #DEFINIZIONE(7). Siano $V_{1},V_{2}$ due spazi vettoriali su un campo $\mathbb{K}$ (ovvero $\mathbb{R}$ o $\mathbb{C}$), e sia $f:\ V_{1}\rightarrow V_{2}$. Si dirà che $f$ è una **funzione lineare** se, $\forall \ \alpha \in\mathbb{K}, \ \forall\ \mathbf{v}_{1},\mathbf{v}_{2}\in V_{1}$, si ha:
	
	1. <mark class="hltr-yellow">Additività</mark>: $f(\mathbf{v}_{1}+\mathbf{v}_{2})=f(\mathbf{v}_{1})+f(\mathbf{v}_{2})$
	2. <mark class="hltr-yellow">Omogeneità</mark>: $f(\alpha\mathbf{v}_{1})=\alpha f({\mathbf{v}_{1}})$
	
	Tali proprietà si possono riassumere nell'unica formula:
	
	$f(\alpha_{1}\mathbf{v}_{1}+\alpha_{2}\mathbf{v}_{2})=\alpha_{1}f(\mathbf{v}_{1})+\alpha_{2}f(\mathbf{v}_{2})$, $\quad \forall \ \alpha_{1},\alpha_{2}\in\mathbb{K},\quad \mathbf{v}_{1},\mathbf{v}_{2}\in V_{1}$
	
	Sinonimi spesso usati di funzione lineare sono **applicazione lineare**, trasformazione lineare.

Il concetto di linearità è fondamentale in matematica e nelle applicazioni. Vedremo nel prossimo capitolo che il <u>calcolo matriciale</u> permette di descrivere completamente le applicazioni lineari tra spazi vettoriali di dimensione finita.

Segnaliamo anche un tipo di funzione tra spazi vettoriali che è in stretta relazione con le applicazioni lineare: si dice **trasformazione affine** (o lineare affine), tra due spazi vettoriali $V_{1},V_{2}$, una trasformazione del tipo$f:\ V_{1}\rightarrow V_{2}$, che abbia la forma $f(\mathbf{v})=l(\mathbf{v})+\mathbf{b}$,
dove $l:\ V_{1}\rightarrow V_{2}$ è lineare e $\mathbf{b}\in V_{2}$ è un elemento fissato.
	*Ad esempio*, 
	$f:\ \mathbb{R}\rightarrow\mathbb{R}$, $f(x)=ax+b$
	con $a,b\in\mathbb{R}$ fissati non è lineare ma affine.




# **Capitolo IV: Matrici e trasformazioni lineari**


### 4.1 **L'algebra delle matrici**

Si può dire informalmente che una <u>matrice</u> è una tabella a doppia entrata; ne sono *esempi* la tavola pitagorica, l'orario ferroviario, le tabelle delle distanze chilometriche, *ecc*.
Possiamo dare la seguente definizione:

- #DEFINIZIONE(8). Si dice **matrice** di tipo $(m,n)$ su un insieme numerico $\mathcal{A}$, un insieme di $m\cdot n$ numeri appartenenti ad $\mathcal{A}$, disposti in una tabella di $m$ <u>righe</u> ed $n$ <u>colonne</u>.

La generica matrice $\mathbf{A}$ di tipo $(m,n)$ si può scrivere nella forma:

$\mathbf{A}=\begin{pmatrix}a_{11}&a_{12}&\cdots&a_{1n}\\ \vdots&\vdots&\ &\vdots \\ a_{m1}&a_{m2}& \cdots &a_{mn}\end{pmatrix}$

Si noti il significato del doppio indice: $a_{ij}$ si legge "elemento di posto $i,j$".
Il primo dei due indici rappresenta il numero della riga, il secondo quello della colonna, motivo per cui essi costituiscono una sorta di coordinate dell'elemento nella matrice.
Scriveremo sinteticamente $\mathbf{A}=(a_{ij})$, $\mathbf{B}=(b_{ij})$ indicando a parte il tipo di matrice o il campo di variabilità degli indici: $i=1,\cdots,m;j=1,\cdots,n$.

- Se $m=n$, la matrice si dice **quadrata** (di ordine $m$).

- Due matrici dello steso tipo $(m,n)$ si dicono **uguali** se sono uguali i rispettivi elementi, ovvero se $\mathbf{A}=(a_{ij}),\mathbf{B}=(b_{ij})$ allora $\mathbf{A}=\mathbf{B} \iff a_{ij}=b_{ij}$.

- Due matrici dello stesso tipo si possono **sommare** ottenendo una matrice ancora dello stesso tipo; se: $\mathbf{A}=(a_{ik}),\mathbf{B}=(b_{ik}), \mathbf{C}=(c_{ik})$, con $i=1,\cdots,m;k=1,\cdots,n$ si definisce $\mathbf{A}+\mathbf{B}=\mathbf{C} \iff a_{ik}+b_{ik}=c_{ik}$
	
	*Per esempio*,
	
	$\begin{pmatrix}7 & 11 &17 \\ 21 & -5 & -9 \end{pmatrix}+\begin{pmatrix}4&-10&3\\7&81&32\end{pmatrix}=\begin{pmatrix}11&1&20\\28&76&23\end{pmatrix}$

- Con le matrici si possono effettuare altre operazioni, ad esempio si piuò **moltiplicare** una matrice per un numero: se $t$ è un numero e $\mathbf{A}=(a_{ik})$, allora $t\mathbf{A}=(ta_{ik})$
	
	*Per esempio*,
	
	$3\cdot\begin{pmatrix}1&3&1\\0&-1&5\\0&0&3\end{pmatrix}=\begin{pmatrix}3&9&3\\0&-3&15\\0&0&9\end{pmatrix}$


Si verifica facilmente che l'insieme $\mathbf{M}(m,n)$ di tute le matrici su $\mathbb{R}$ di tipo $(m,n)$ è uno spazio vettoriale. In particolare, l'elemento $\mathbf{0}$ è la matrice che ha tutti gli elementi nulli, e la matrice **opposta** di $\mathbf{A}$, detta $-\mathbf{A}$, è la matrice che ha per elementi gli opposti degli elementi di $\mathbf{A}$.
La dimensione dello spazio vettoriale è $n\cdot m$ e la <u>base canonica</u> è costituita dalle matrici $n\times m$ aventi tutti gli elementi nulli, tranne uno uguale ad 1.
In particolare,

- $\mathbf{M}(1,n)$ si identifica con $\mathbb{R}^n$, pensato come spazio di vettori riga;
- $\mathbf{M}(n,1)$ si identifica con $\mathbb{R}^n$, pensato come spazio di vettori colonna.

I vettori di $\mathbb{R}^n$ sono quindi particolari matrici.

Le righe di una matrice $\mathbf{A}$ di tipo $(m,n)$ possono essere viste come vettori riga di $\mathbb{R}^n$, cioè $\mathbf{a}_{i}=(a_{i1},a_{i2},\cdots,a_{in})\quad i=1,2,\cdots,m$
e viceversa le colonne possono essere viste come vettori colonna di $\mathbb{R}^m$, cioè $a^j=\begin{pmatrix}a_{1j}\\a_{2j}\\ \vdots \\a_{mj}\end{pmatrix}$
quindi la matrice $\mathbf{A}$ si può scrivere nei modi seguenti: $\mathbf{A}=\begin{pmatrix}\mathbf{a}_{1}\\ \mathbf{a}_{2}\\ \vdots \\ \mathbf{a}_{m}\end{pmatrix}=(\mathbf{a}^1|\mathbf{a}^2|\cdots|\mathbf{a}^n)$

Possiamo anche definire un prodotto tra matrici, che però non è valido per ogni coppia di quest'ultime come si vede nella seguente definizione:

- #DEFINIZIONE(9). **Prodotto di matrici**
	
	Date due matrici $\mathbf{A}=(a_{ik})$ e $\mathbf{B}=(b_{ks})$ di tipo $(m,n)$ e $(n,p)$, indicheremo con $\mathbf{A}\cdot\mathbf{B}$, o più semplicemente con $\mathbf{A}\mathbf{B}$, la matrice $\mathbf{C}$ di tipo $(m,p)$ il cui elemento $c_{ij}$ è il prodotto scalare della $i$-esima riga di $\mathbf{A}$ e della $j$-esima colonna di $\mathbf{B}$ (le quali sono entrambe vettori $n$-dimensonali). In simboli:
				$c_{ij}=\mathbf{a}_{i}\cdot\mathbf{b}^j=\sum_{k=1}^n a_{ik}b_{kj},\quad$ dove $i=1,2,\cdots,m$ e $j=1,2,\cdots,p$
	
	*Per esempio*,
	
	$\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}\cdot\begin{pmatrix}1&3\\-7&8\\0&1\end{pmatrix}=\begin{pmatrix}-13&22\\-31&58\end{pmatrix}$
	
	infatti:
	$c_{11}=1\cdot\ 1+2\cdot(-7)+3\cdot 0=-13$
	$c_{12}=1\cdot\ 3+2\cdot 8+3\cdot 1=22$
	$c_{21}=4\cdot\ 1+5\cdot(-7)+6\cdot 0=-31$
	$c_{22}=4\cdot\ 3+5\cdot 8+6\cdot 1=58$
	
	Due matrici $\mathbf{A}$ e $\mathbf{B}$ tali che il numero delle colonne della prima coincide col numero di righe della seconda si dicono conformabili. Di conseguenza i<mark class="hltr-yellow">l prodotto di matrici si può effettuare solo tra matrici conformabili</mark>; si chiama anche <u>prodotto righe per colonne</u> per il medesimo motivo.
	
	- Se $\mathbf{A}$ è una matrice $(m,n)$ e $\mathbf{B}$ è una matrice $(n,p)$, con $m\ne p$, è definito il prodotto $\mathbf{A}\mathbf{B}$ ma non il prodotto $\mathbf{B}\mathbf{A}$, per cui in generale <u>il prodotto non è commutativo</u>.
		
		Se però $\mathbf{A}$ e $\mathbf{B}$ sono <u>quadrate</u> dello stesso ordine, entrambi i prodotti $\mathbf{A}\mathbf{B}$ e $\mathbf{B}\mathbf{A}$ sono ben definiti, ma non sono in generale uguali: $\mathbf{A}\mathbf{B}\ne\mathbf{B}\mathbf{A}$.
		Si è quindi costretti a specificare se la moltiplicazione avviene a destra $(\mathbf{A}\mathbf{B})$ o viceversa a sinistra $(\mathbf{B}\mathbf{A})$.
	
	- Il prodotto righe per colonne è però <mark class="hltr-yellow">associativo</mark>; più precisamente, date tre matrici $\mathbf{A}$ di tipo $(m,n)$, $\mathbf{B}$ di tipo $(n,p)$ e $\mathbf{C}$ di tipo $(p,r)$ i due prodotti $\mathbf{A}(\mathbf{B}\mathbf{C})$ e $(\mathbf{A}\mathbf{B})\mathbf{C}$ sono ben definiti ed uguali.
		
		In particolare, se $\mathbf{A}$ è una matrice quadrata ha senso definire $\mathbf{A}^n=\mathbf{A}\cdot\mathbf{A}\cdot\cdots\cdot\mathbf{A}$.
	
	- Per le matrici vale anche la proprietà <mark class="hltr-yellow">distributiva</mark>: $\mathbf{A}(\mathbf{B}+\mathbf{C})=\mathbf{A}\mathbf{B}+\mathbf{A}\mathbf{C}$
		
		quando ciò ha senso, ovvero se $\mathbf{A}$ è di tipo $(n,m)$ e $\mathbf{B},\mathbf{C}$ sono di tipo $(m,r)$.
		Analogamente $(\mathbf{B}+\mathbf{C})\mathbf{A}=\mathbf{B}\mathbf{A}+\mathbf{C}\mathbf{A}$, se $\mathbf{B},\mathbf{C}$ sono di tipo $(n,m)$ e $\mathbf{A}$ è di tipo $(m,r)$.


- È importante sottolineare che tra le matrici quadrate di ordine $n$ ne esiste una, che indichiamo con $\mathbf{I}_{n}$, tale che per ogni altra matrice $\mathbf{A}$ dello stesso ordine si ha: $\mathbf{A}\mathbf{I}_{n}=\mathbf{I}_{n}\mathbf{A}$
	
	Tale matrice si chiama **matrice identità** ed ha la forma: $\mathbf{I}_{n}=\begin{pmatrix}1&0&0&\cdots& 0\\0&1&0&\cdots&0\\ \vdots&\vdots&\vdots&\ddots &\vdots\\ 0&0&0&\cdots&1\end{pmatrix}$


- Si chiama **matrice trasposta** di una matrice $\mathbf{A}$ di tipo $(m,n)$ e la si indica con il simbolo $\mathbf{A}^\top$, la matrice di tipo $(n,m)$ che si ottiene da $\mathbf{A}$ scambiando le righe con le colonne.
	
	*Per esempio*,
	
	$\mathbf{A}=\begin{pmatrix}7&10&3\\-5&4&2\end{pmatrix},\quad \mathbf{A}^\top=\begin{pmatrix}7&-5\\10&4\\3&2\end{pmatrix}$
	
	In simboli, se $\mathbf{A}=(a_{ij})$, $\mathbf{A}^\top$ avrà $a_{ji}$ come elemento di posto $ij$. Si osservi la seguente <mark class="hltr-yellow">proprietà</mark>: $(\mathbf{A}\mathbf{B})^\top=\mathbf{B}^\top\mathbf{A}^\top\quad$ (se $\mathbf{A}$ è di tipo $(n,m)$ e $\mathbf{B}$ di tipo $(m,r)$).
	
	Se $\mathbf{A}=\mathbf{A}^\top$ (e quindi $m=n$), tale matrice si dice essere **simmetrica**.
	Cioò significa che per ogni coppia di indici $i,j$ risulta $a_{ij}=a_{ji}$, ovvero la matrice è una tabella <u>simmetrica rispetto alla diagonale principale</u>.
		*Esempio*: $\begin{pmatrix}1&2&-1\\2&0&3\\-1&3&4\end{pmatrix}$ è una matrice simmetrica.



Una matrice quadrata del tipo $U=\begin{pmatrix}d_{1}&*&*&*&*\\0&d_{2}&*&*&*\\0&0&d_{3}&*&*\\ \vdots&\vdots&\vdots&\ddots&\vdots\\ 0&0&0&\cdots&d_{n}\end{pmatrix}$

dove gli asterischi indicano elementi qualsiasi, si chiama **triangolare alta**; analogamente, si dice **triangolare bassa** se tutti gli elemeneti sopra la diagonale principale sono nulli.
Una matrice quadrata si dice **diagonale** se sono nulli tutti i suoi elementi fuori dalla diagonale principale.

È facile controllare che: il prodotto di matrici quadrate dello stesso ordine triangolari alte/basse è ancora triangolare alta/bassa. Evidentemente, se $\mathbf{A}$ è triangolare e simmetrica allora deve essere diagonale; se $\mathbf{A}$ è triangolare sia alta che bassa allora è diagonale.



### 4.2 **Rappresentazione matriciale delle trasformazioni lineari**

Una matrice $\mathbf{A}$, quadrata di ordine $n$, trasforma un vettore di $\mathbb{R}^n$ in un altro vettore di $\mathbb{R}^n$ mediante il prodotto righe per colonne (se pensiamo sempre i vettori come colonne): $\mathbf{x}\in\mathbb{R}^n$ è trasformato nel vettore $\mathbf{A}\mathbf{x}\in\mathbb{R}^n$
Analogamente, una matrice $\mathbf{A}$ di tipo $(m,n)$ trasforma un vettore $\mathbf{x}\in\mathbb{R}^n$ nel vettore $\mathbf{A}\mathbf{x}\in\mathbb{R}^m$
Inoltre, in questa trasformazione

						$L:\mathbb{R}^n\rightarrow\mathbb{R}^m \quad \quad L:\mathbf{x}\mapsto\mathbf{A}\mathbf{x}$

è lineare. Si verifica subito infatti, dalla definizione di prodotto righe per colonne, che $\forall \ \mathbf{x},\mathbf{y}\in\mathbb{R}^n,\lambda\in\mathbb{R}$,

							$\mathbf{A}(\mathbf{x}+\mathbf{y})=\mathbf{A}\mathbf{x}+\mathbf{A}\mathbf{y}$
								$\mathbf{A}(\lambda\mathbf{x})=\lambda\mathbf{A}\mathbf{x}$

Infine, considerazioni analoghe valgono se al campo reale sostituiamo il campo complesso $\mathbb{C}$: una matrice di tipo $(m,n)$ a elementi complessi realizza una trasformazione lineare di $\mathbb{C}^n$ in $\mathbb{C}^m$.

Il prossimo importante teorema afferma, in sostanza, che tutte le trasformazioni lineari da $\mathbb{R}^n$ a $\mathbb{R}^m$ (o da $\mathbb{C}^n$ a $\mathbb{C}^m$) sono di questo tipo; anzi, tutte le trasformazioni lineari tra due spazi vettoriali qualsiasi, di dimensione finita, si possono rappresentare a questo modo:

- #TEOREMA(4). **Teorema di Rappresentazione**
	
	Siano $V_n,V_{m}$ due spazi vettoriali sul campo $\mathbb{K}$ di dimensione $n,m$ rispettivamente, e sia $\mathcal{L}:V_{n}\rightarrow V_{m}$ una trasformazione lineare.
	Fissate due basi $\mathbf{u}_{1},\mathbf{u}_{2},\cdots,\mathbf{u}_{n}$ e $\mathbf{v}_{1},\mathbf{v}_{2},\cdots,\mathbf{v}_{m}$ in $V_{n}$ e $V_{m}$, rispettivamente, esiste un'**unica matrice** $\mathbf{A}$ di tipo $(m,n)$ a elementi in $\mathbb{K}$ che rappresenta $\mathcal{L}$ nel senso che, se $\mathbf{x}=x_{1}\mathbf{u}_{1}+x_{2}\mathbf{u}_{2}+\cdots+x_{n}\mathbf{u}_{n}$ e $\mathcal{L}(\mathbf{x})=y_{1}\mathbf{v}_{1}+\cdots+y_{m}\mathbf{v}_{m}$, allora:
	
								$\begin{pmatrix}y_{1}\\y_{2}\\ \vdots \\y_{m}\end{pmatrix}=\mathbf{A}\begin{pmatrix}x_{1}\\x_{2}\\ \vdots \\x_{n}\end{pmatrix}$
	
	Si noti che, qualunque sia lo spazio vettoriale $V_{n}$ e fissata una base nel medesimo spazio, ogni vettore è individuato dalla $n$-upla delle sue componenti rispetto a questa base, cioè da un elemento di $\mathbb{K}^n$. Il teorema afferma quindi l'esistenza di una matrice che rappresenta la trasformazione lineare, nel senso che, fissata una base nello spazio di partenza ed una nello spazio di arrivo, il vettore delle componenti di $\mathcal{L}(x)$ si ottiene moltiplicando la matrice per il vettore delle componenti di $\mathbf{x}$.
	Nel seguito parleremo di matrici a elementi reali e di trasformazioni lineari di $\mathbb{R}^n$ in $\mathbb{R}^m$, che perrò varrà pari pari sostituendo $\mathbb{C}$ ad $\mathbb{R}$.
	
	*Dimostrazione*:
	
	Essendo $\mathcal{L}(\mathbf{u}_{1})\in V_{m}$, si può scrivere $\mathcal{L}(\mathbf{u}_{1})=a_{11}\mathbf{v}_{1}+\cdots+a_{m1}\mathbf{v}_{m}$
	Analogamente abbiamo $\mathcal{L}(\mathbf{u}_{2})=a_{12}\mathbf{v}_{1}+\cdots+a_{m_{2}}\mathbf{v}_{m}\quad\cdots\quad\mathcal{L}(\mathbf{u}_{n})=a_{1n}\mathbf{v}_{1}+\cdots+a_{mn}\mathbf{v}_{m}$
	
	per opportuni coefficenti $a_{ij}\in\mathbb{R}$. Poniamo ora $\mathbf{A}=(a_{ij})\quad i=1,2,\cdots,m \quad j=1,2,\cdots,n$
	e sia $\mathbf{x}=x_{1}\mathbf{u}_{1}+x_{2}\mathbf{u}_{2}+\cdots+x_{n}\mathbf{u}_{n}$.
	
	Si ha, per la linearità di $\mathcal{L}$ e le equazioni precedenti:
	$\mathcal{L}(x)=\mathcal{L}\left( \sum_{j=1}^n x_{j}\mathbf{u}_{j}\right)=\sum_{j=1}^n x_{j}\mathcal{L}(\mathbf{u}_{j})=\sum_{j=1}^n x_{j}\sum_{i=1}^m a_{ij}\mathbf{v}_{i}=\sum_{j=1}^n\sum_{i=1}^m a_{ij}x_{j}\mathbf{v}_{i}=\sum_{i=1}^m\left( \sum_{j=1}^n a_{ij}x_{j} \right)\mathbf{v}_{i}$
	Si vede quindi che le componenti scalari di $\mathcal{L}(x)$ rispetto alla base $\mathbf{v}_{1},\mathbf{v}_{2},\cdots,\mathbf{v}_{m}$ sono date dalla formula:
							$y_{i}=\sum_{j=1}^n a_{ij}x_{j} \quad\quad i=1,2,\cdots,m$
	
	che, raggruppate in forma matriciale, danno: $\begin{pmatrix}y_{1}\\y_{2}\\ \vdots \\ y_{m}\end{pmatrix}=\mathbf{A}\begin{pmatrix} x_{1}\\x_{2}\\ \vdots \\ x_{n}\end{pmatrix}$
	
	La matrice $\mathbf{A}$ rappresenta dunque $\mathcal{L}$ nel senso precisato nell'enunciato del teorema.
	Tale matrice è unica, come conseguenza del fatto che ogni vettore $\mathcal{L}(\mathbf{u}_{i}),i=1,2,\cdots,n$ si può esprimere in un unico modo come combinazione lineare dei vettori $\mathbf{v}_{1},\mathbf{v}_{2},\cdots,\mathbf{v}_{m}$.
	
	**Osservazioni**:
	
	1. Il teorema di rappresentazione chiarisce il motivo per cui il prodotto di matrici è stato definito proprio in quel modo ("righe per colonne"). Infatti, è quello il tipo di prodotto adatto a rappresentare le trasformazioni lineari;
	2. Quest'ultima osservazione è anche alla base dell'utilità del calcolo matriciale in fisica.


- Siano ora $L_{1}:\mathbb{R}^n\rightarrow \mathbb{R}^m$ e $L_{2}:\mathbb{R}^m\rightarrow \mathbb{R}^s$ due trasformazioni lineari, rappresentate rispettivamente da una matrice $\mathbf{A}$ di tipo $(m,n)$ e da una matrice $\mathbf{B}$ di tipo $(s,m)$, ottenute fissando una volta per tutte una base in $\mathbb{R}^n, \mathbb{R}^m, \mathbb{R}^s$ (è necessario che la base considerata in $\mathbb{R}^m$ sia la stessa per $L_{1}$ e $L_{2}$). Consideriamo la trasformazione composta,
	
	$L_{2}\circ L_{1}:\mathbb{R}^n\rightarrow\mathbb{R}^s$
	$(L_{2}\circ L_{1}):\mathbf{x}\mapsto L_{2}(L_{1}\mathbf{x})$
	
	È immediato verificare che $L_{2}\circ L_{1}$ è anch'essa una trasformazione lineare; per il Teorema di Rappresentazione, esisterà una matrice $\mathbf{C}$, di tipo $(s,n)$, che rappresenta tale trasformazione rispetto alle stesse basi. Essa è così definita:
	
	$\mathbf{C}=\mathbf{B}\mathbf{A}$
	
	ossia la matrice rappresentativa di $L_{2}\circ L_{1}$ è il prodotto righe per colonne delle matrici $\mathbf{B},\mathbf{A}$ che rappresentano $L_{2}\circ L_{1}$, rispettivamente. Si verifica immediatamente scrivendo il vettore $\mathbf{x}$ come $n$-upla rispetto alla base fissata:
	
	$L_{2}(L_{1}\mathbf{x})=\mathbf{B}\cdot(\mathbf{Ax})=(\mathbf{BA})\mathbf{x}\quad$, ossia $\mathbf{BA}$ rappresenta $L_{2}\circ L_{1}$.


- Notiamo infine che una **trasformazione affine** tra due spazi vettoriali ([[#### 3.3.3 **Il concetto di linearità**|vedi paragrafo 3.3.3]]), cioò del tipo:
	
	$f:V_{n}\rightarrow V_{m}$
	$f(\mathbf{v})=l(\mathbf{v})+\mathbf{u}$
	
	con $l:V_{n}\rightarrow V_{m}$ lineare e $\mathbf{u}\in V_{m}$ vettore fissato, si rappresenterà rispetto alle basi fissate in $V_{n},V_{m}$ nella forma matriciale:
	
	$L(\mathbf{x})=\mathbf{Ax}+\mathbf{b}$
	
	dove $\mathbf{A}$ è un'opportuna matrice $(m,n)$ e $\mathbf{b}\in\mathbb{R}^m$ il vettore che rappresenta $\mathbf{u}$ rispetto alla base scelta in $V_{m}$.



### 4.3 **Determinante**

Uno dei concetti centrali associati ad una <u>matrice quadrata</u> è quello di **determinante**, la cui definizione generale tuttavia non è elementare.
D'altra parte, noi siamo interessato soprattutto al calcolo dei determinanti perciò, adottanto un atteggiamento "ricorsivo", definiremo esplicitamente il determinante per matrici di ordine $n=1$ e $n=2$, indicando poi come si ottenga il determinante di una matrice di ordine $n$.

- Per $n=1$, cioè per una matrice costituita da un solo elemento $a_{11}$, il determinante è per definizione l'elemento stesso.

- Per $n=2$, ovvero una matrice quadrata di ordine 2, del tipo: $\mathbf{M}=\begin{pmatrix}a_{11}&a_{12}\\a_{21}&a_{22}\end{pmatrix}$ il determinante, indicato con $\det\mathbf{M}$ oppure con $|\mathbf{M}|$ è assegnato dalla formula:

							$\det\mathbf{M}=a_{11}\cdot a_{22}-a_{12}\cdot a_{21}$
	
	*Ad esempio*, data:
	
					$\mathbf{M}=\begin{pmatrix}1&-3\\2&-4\end{pmatrix}\quad\rightarrow\quad \det\mathbf{M}=1\cdot(-4)-2\cdot(-3)=2$

- Sia data ora la matrice quadrata di ordine $n$: $\quad\mathbf{A}=\begin{pmatrix}a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\ \vdots \\a_{n1}&a_{n2}&\cdots&a_{nn}\end{pmatrix}$
	
	Conviene introdurre alcune definizioni:
	
	a) Si chiama <u>minore complementare</u> di un elemento $a_{ij}$ e lo si indica con $M_{ij}$, il determinante della matrice ottenuta cancellando la riga $i$ e la colonna $j$ dalla matrice $\mathbf{A}$;
	
	b) Si chiama <u>complemento algebrico</u> di un elemento $a_{ij}$ il numero $A_{ij}=(-1)^{i+j}M_{ij}$
		Notiamo che:
		$(-1)^{i+j}=1\quad$ se $\quad i+j$ è pari
		$(-1)^{i+j}=-1\quad$ se $\quad i+j$ è dispari
		Per esempio, sia $\mathbf{A}=\begin{pmatrix}8&2&-1\\4&3&-5\\-6&0&4\end{pmatrix}$; consideriamo l'elemento $a_{13}=-1$. Si ha:
		$M_{13}=\det\begin{pmatrix}4&3\\-6&0\end{pmatrix}=18$, $A_{13}=(-1)^{1+3}M_{13}=18$
	
	c) Si chiama determinante della matrice quadrata $\mathbf{A}$ la somma dei prodotti degli elementi di una qualunque linea (riga o colonna) per i loro complementi algebrici. In formule, $\forall k,1\le k\le n$, si ha fissando la riga $k$:
		
						$\det\mathbf{A}=a_{k1}A_{k1}+a_{k2}A_{k2}+\cdots a_{kn}A_{kn}$
		
	oppure, fissando la colonna $k$:
						
						$\det\mathbf{A}=a_{1k}A_{1k}+a_{2k}A_{2k}+\cdots a_{nk}A_{nk}$


Segue quindi il prossimo Teorema:

- #TEOREMA(5). **Teorema di Laplace**
	
	Il risultato che si ottiene calcolando il determinante di una matrice come nell'ultima definizione (c) <u>non dipende dalla particolare riga o colonna scelta</u>.
	
	*Per esempio*,
	
	calcoliamo il determinante della matrice $\mathbf{A}$ (*ultimo esempio*):
	
	$\det\mathbf{A}=-6\cdot\begin{vmatrix}2&-1\\3&-5\end{vmatrix}-0\cdot\begin{vmatrix}8&-1\\4&-5\end{vmatrix}+4\cdot\begin{vmatrix}8&2\\4&3\end{vmatrix}=58$
	
	Se avessimo scelto un'altra colonna/riga il risultato non sarebbe cambiato.


Si voglia ora calcolare il determinante della seguente matrice:

$\mathbf{A}=\begin{pmatrix}1&2&3&4\\0&2&5&1\\2&0&3&0\\0&-1&-2&1\end{pmatrix}$

Applicando il teorema, considerando la prima colonna, si ha:

$\begin{align}\det\mathbf{A}&=1\cdot\begin{vmatrix}2&5&1\\0&3&0\\-1&-2&1\end{vmatrix}-0\cdot\begin{vmatrix}2&3&4\\0&3&0\\-1&-2&1\end{vmatrix}+2\cdot\begin{vmatrix}2&3&4\\2&5&1\\-1&-2&1\end{vmatrix}-0\cdot\begin{vmatrix}2&3&4\\2&5&1\\0&3&0\end{vmatrix}=\\ &= 2\cdot\begin{vmatrix}3&0\\-2&1\end{vmatrix}-1\cdot\begin{vmatrix}5&1\\3&0\end{vmatrix}+2\cdot\left\{2\begin{vmatrix}5&1\\-2&1\end{vmatrix}-2\cdot\begin{vmatrix}3&4\\-2&1\end{vmatrix}-1\cdot\begin{vmatrix}3&4\\5&1\end{vmatrix}\right\}=\\ &= 6+3+2\left\{14-22+17\right\}=27\end{align}$


- #TEOREMA(6). **Proprietà elementari del determinante**
	
	Sia $\mathbf{A}$ una matrice $(n,n)$.
	
	a. Se $\mathbf{A}$ ha una riga o una colonna di soli zeri, $\det\mathbf{A}=0$;
	b. Scambiando due righe o due colonne, il determinante cambia di segno;
	c. Se $\mathbf{A}$ ha due righe o due colonne uguali, $\det\mathbf{A}=0$;
	d. Il determinante è una funzione lineare di ciascuna sua riga/colonna, ossia:
		d1:$\quad\det\begin{pmatrix}a_{1}+b_{1}\\ a_{2}\\ \cdots \\a_{n}\end{pmatrix}=\det\begin{pmatrix}a_{1}\\ a_{2}\\ \cdots \\a_{n}\end{pmatrix}+\det\begin{pmatrix}b_{1}\\ a_{2}\\ \cdots \\a_{n}\end{pmatrix}$
		d2: $\det\begin{pmatrix}\lambda a_{1}\\ a_{2}\\ \cdots \\a_{n}\end{pmatrix}=\lambda\det\begin{pmatrix}a_{1}\\ a_{2}\\ \cdots \\a_{n}\end{pmatrix}$
		(gli $a_{i}$ sono i vettori riga che costituiscono la matrice);
	
	e. Se ad una riga/colonna si aggiunge una qualunque combinazione lineare delle altre righe/colonne, il determinante non cambia;
	f. Se le righe/colonne di $\mathbf{A}$ sono vettori linearmente indipendenti, $\det\mathbf{A}=0$;
	g. $\det(\lambda\mathbf{A})=\lambda^n\det\mathbf{A}$;
	h. Se $\mathbf{A}$ è triangolare (in particolare, se è diagonale) $\det\mathbf{A}=a_{11}\cdot a_{22}\cdot\cdots\cdots a_{nn}$.
	
	*Dimostrazione sul libro*


Un'altra importante proprietà del determinante è la seguente:

- #TEOREMA(7). **Teorema di Binet**
	
	Se $\mathbf{A}$ e $\mathbf{B}$ sono matrici quadrate dello stesso ordine, $\det\mathbf{AB}=\det\mathbf{A}\cdot\det\mathbf{B}$


- **Regola di Sarrus** per i determinanti del terzo ordine:
	
	calcoliamo il determinante della matrice $\mathbf{M}=\begin{pmatrix}a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}\end{pmatrix}$ mediante il Teorema di Laplace, sviluppando secondo gli elementi della prima riga. Si ha:
	$\det\mathbf{M}=a_{11}\begin{vmatrix}a_{22}&a_{23}\\a_{32}&a_{33}\end{vmatrix}-a_{12}\begin{vmatrix}a_{21}&a_{23}\\a_{31}&a_{33}\end{vmatrix}+a_{13}\begin{vmatrix}a_{21}&a_{22}\\a_{31}&a_{32}\end{vmatrix}=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{13}a_{22}a_{31}+a_{11}a_{23}a_{32}-a_{12}a_{21}a_{33}$
	Questa somma può essere ottenuta col seguente procedimento, noto come Regola di Sarrus:


#### 4.3.1 **Prodotto vettoriale misto. Significato geometrico del determinante**

Il prodotto vettoriale dei due vettori di $\mathbb{R}^3$: $\mathbf{v}=(x_{1},x_{2},x_{3})$ e $\mathbf{w}=(y_{1},y_{2},y_{3})$ si può riscrivere nel modo seguente:

$\mathbf{v}\times\mathbf{w}=\begin{vmatrix}x_{2}&x_{3}\\ y_{2}&y_{3}\end{vmatrix}\mathbf{i}-\begin{vmatrix}x_{1}&x_{3}\\ y_{1}&y_{3}\end{vmatrix}\mathbf{j}+\begin{vmatrix}x_{1}&x_{2}\\ y_{1}&y_{2}\end{vmatrix}\mathbf{k}$

Se $x_{3}=y_{3}=0$, si riduce a: $\mathbf{v}\times\mathbf{w}=\begin{vmatrix}x_{1}&x_{2}\\ y_{1}&y_{2}\end{vmatrix}\mathbf{k}$

e quindi $|\mathbf{v}\times\mathbf{w}|=|\det\begin{pmatrix}x_{1}&x_{2}\\ y_{1}&y_{2}\end{pmatrix}|$

Ricordando il [[### 1.5 **Prodotto scalare e vettoriale**|significato del modulo di prodotto vettoriale]] si ricava che il modulo del determinante $\begin{vmatrix}x_{1}&x_{2}\\ y_{1}&y_{2}\end{vmatrix}$ coincide con l'area del parallelogramma costruito sui vettori piani $(x_{1},x_{2}),(y_{1},y_{2})$.
Poichè l'area del parallelogramma è nulla se e solo se i due vettori che lo generano sono paralleli, si ha anche che il determinante $2\times 2$ è <u>nullo</u> se e solo se le sue righe/colonne sono due vettori paralleli, cioè <mark class="hltr-yellow">linearmente dipendenti</mark>.

Se ora $\mathbf{u}=(z_{1},z_{2},z_{3})$ è un terzo vettore, ricaviamo la seguente formula per il prodotto misto $\mathbf{u}\cdot\mathbf{v}\times\mathbf{w}$:

$\mathbf{u}\cdot\mathbf{v}\times\mathbf{w}=z_{1}\begin{vmatrix}x_{2}&x_{3}\\ y_{2}&y_{3}\end{vmatrix}-z_{2}\begin{vmatrix}x_{1}&x_{3}\\ y_{1}&y_{3}\end{vmatrix}+z_{3}\begin{vmatrix}x_{1}&x_{2}\\ y_{1}&y_{2}\end{vmatrix}=\begin{vmatrix}z_{1}&z_{2}&z_{3}\\ x_{1}&x_{2}&x_{3}\\y_{1}&y_{2}&y_{3}\end{vmatrix}$

Ricordando il [[### 1.5 **Prodotto scalare e vettoriale**|significato geometrico del prodotto misto]] si ricava che il modulo del determinante rappresenta il volume del parallelepipedo costruito sui vettori $\mathbf{u},\mathbf{v}$ e $\mathbf{w}$.
Poichè a sua volta il volume del parallelepipedo è nullo se e solo se i tre vettori sono complanari, si ha anche che il determinante $3\times 3$ è <u>nullo</u> se e solo se le sue righe/colonne sono tre vettori complanari, cioè <mark class="hltr-yellow">linearmente dipendenti</mark>.

Otteniamo quindi nel caso particolare $n=2,3$ un comodo criterio di dipendenza o indipendenza lineare, mediante il calcolo del determinante.

- L'ultima formula permette anche di dimostrare facilmente la <mark class="hltr-yellow">proprietà di invarianza ciclica</mark> del prodotto misto: $\mathbf{u}\cdot\mathbf{v}\times\mathbf{w}=\mathbf{w}\cdot\mathbf{u}\times\mathbf{v}=\mathbf{v}\cdot\mathbf{w}\times\mathbf{u}$
	
	Infatti, ricordando che il segno del determinante cambia scambiando due righe della matrice, si ha per esempio: $\begin{vmatrix}\mathbf{u}\\ \mathbf{v}\\ \mathbf{w}\end{vmatrix}=-\begin{vmatrix}\mathbf{v}\\ \mathbf{u}\\ \mathbf{w}\end{vmatrix}=\begin{vmatrix}\mathbf{w}\\ \mathbf{u}\\ \mathbf{v}\end{vmatrix}$
	che dimostra la prima uguaglianza (analogamente si prova l'altra).



### 4.4 **Caratteristica di una matrice**

Abbiamo visto che, se le righe/colonne di $\mathbf{A}$ sono vettori linearmente dipendenti, allora $\det\mathbf{A}=0$ (Teorema 6). Inoltre, abbiamo dimostrato che se $n=2,3$ vale anche il viceversa (per via del significato geometrico del determinante): esso si annulla se e solo se le righe della matrice sono linearmente dipendenti.
Questo risultato è valido in realtà per $n$ qualsiasi, e può essere anzi ulteriormente generalizzato allo studio di un qualsiasi numero $r$ di vettori di $\mathbb{R}^n$ (con $r\le n$):

- #TEOREMA(8). Siano $\mathbf{a}_{1},\mathbf{a}_{2},\cdots,\mathbf{a}_{r}$ $r$ vettori riga di $\mathbb{R}^n \ (r<n)$, e sia $\mathbf{A}$ la matrice $(r,n)$ che ha per righe questi vettori. Allora i vettori $\mathbf{a}_{1},\mathbf{a}_{2},\cdots,\mathbf{a}_{r}$ sono linearmente dipendenti se e solo se ogni matrice $(r,r)$ estratta da $\mathbf{A}$ ha determinante nullo; sono indipendenti se e solo se esiste almeno una matrice $(r,r)$ estratta da $\mathbf{A}$ con determinante diverso da $0$. Inoltre: $n$ vettori di $\mathbb{R}^n$ sono linearmente dipendenti/indipendenti se e solo se la matrice $(n,n)$ che si ottinee accostandoli ha determinante uguale a $0$/diverso da $0$.
	
	Ricordiamo che $r$ vettori di $\mathbb{R}^n$ con $r>n$ sono sempre linearmente dipendenti.

Introduciamo ora il concetto di **rango** o **caratteristica** di una matrice:

- #DEFINIZIONE(10). **Caratteristica di una matrice**
	
	Dati una matrice $\mathbf{A}$ di $m$ righe e $n$ colonne (con $m$ non necessariamente uguale ad $n$) ed un intero $k\le min(m,n)$, si dice **minore** di ordine $k$ estratto dalla matrice $\mathbf{A}$ il determinante di una qualsiasi matrice di ordine $k$ ottenuta con gli elementi comuni a $k$ righe e $k$ colonne di $\mathbf{A}$. Si definisce **caratteristica** o **rango** di $\mathbf{A}$ l'intero $r\ge 0$ tale che: esiste un minore estratto da $\mathbf{A}$ di ordine $r\ne 0$ ed ogni minore estratto da $\mathbf{A}$ di ordine $r+1$ è nullo.
	Segue immediatamente che:
	
	<mark class="hltr-yellow">Il rango di una matrice rappresenta il numero massimo di righe/colonne linearmente indipendenti</mark>.

Per la determinazione del rango risulta utile la seguente proprozione:

- #PROPOSIZIONE(3). **Proposizione di Kronecker**
	
	Condizione necessaria e sufficiente affinchè una matrice abbia rango $k$ è che esista un minore di ordine $k\ne 0$ e siano nulli tutti i minori di ordine $k+1$ ottenuti da quello orlandolo con una qualunque altra riga o colonna.


*Esempio*:
Applichiamo il metodo indicato nella Proposizione di Kronecker alla matrice $\mathbf{A}=\begin{pmatrix}1&2&3&4\\2&0&3&5\\2&4&6&8\end{pmatrix}$

Consideriamo una matrice estratta da $\mathbf{A}$ di ordine $1$ con $\det \ne 0$, ovvero $\mathbf{A}^*=(1)$

"Orliamo" tale matrice in tutti i modi possibili, finchè si ottenga una matrice del secondo ordine con $\det \ne 0$: $\mathbf{A}^{* *}=\begin{pmatrix}1&2\\2&0\end{pmatrix}\quad \det\mathbf{A}^{* *}=-4$
Ripetendo il ragionamento, "orlando" cioè in tutti i modi possibili la $\mathbf{A}^{* *}$:

$\mathbf{A}_{1}^{* *}=\begin{pmatrix}1&2&3\\2&0&3\\2&4&6\end{pmatrix}\quad\mathbf{A}_{2}^{* *}=\begin{pmatrix}1&2&4\\2&0&5\\2&4&8\end{pmatrix}$

si ottengono due matrici i cui determinanti sono nulli. Il rango è dunque $2$ in accordo al Teorema precedente.

Per la determinazione del rango di $\mathbf{A}$ seguendo la definizione avremmo dovuto calcolare quattro determinanti del terzo ordine, mentre col metodo della Proposizione di Kronecker i determinanti $3\times 3$ da calcolare si sono ridotti a due.
Ovviamente i vantaggi risultano evidenti quanto più grandi sono le dimensioni della matrice.



### 4.5 **Matrice inversa**

Se $a$ è un numero non nullo, esiste un unico $a^{-1}=\frac{1}{a}$ (il reciproco di $a$) tale che:

							$a\cdot a^{-1}=a^{-1}\cdot a=1$

Se $\mathbf{A}$ è una matrice quadrata $(n,n)$, chiameremo **matrice inversa** di $\mathbf{A}$ la matrice (<u>se esiste</u>) $\mathbf{A}^{-1}$ tale che:

							$\mathbf{A}\cdot\mathbf{A}^{-1}=\mathbf{A}^{-1}\cdot\mathbf{A}=\mathbf{I}_{n}$

dove $\mathbf{I}_{n}$ è la [[### 4.1 **L'algebra delle matrici**|matrice identità]].

La condizione che garantisce l'esistenza della matrice inversa, analoga alla condizione $a\ne 0$ per l'esistenza del reciproco di un numero, è che sia $\det\mathbf{A}\ne 0$.
Il seguente Teorema precisa questa affermazione, e indica un modo per calcolare $\mathbf{A}^{-1}$:

- #TEOREMA(9). Condizione necessaria è sufficiente affinchè esista la matrice inversa $\mathbf{A}^{-1}$ è che $\mathbf{A}$ sia non singolare, cioà che $\det\mathbf{A}\ne 0$. In tal caso vale la formula:
	
	$\mathbf{A}^{-1}=\frac{1}{\det\mathbf{A}}=\cdot\begin{pmatrix}A_{11}&A_{12}&\cdots&A_{1n}\\A_{21}&A_{22}&\cdots&A_{2n}\\ \vdots & \vdots &  & \vdots\\A_{n1}&A_{n2}&\cdots&A_{nn}\end{pmatrix}^\top$
	
	dove $\top$ indica "trasposta" e gli $A_{ij}$ sono i <u>complementi algebrici</u> degli elementi $a_{ij}$ della matrice $\mathbf{A}$. Infine, $\det{\mathbf{A}^{-1}}=\frac{1}{\det\mathbf{A}}$.
	
	*Dimostrazione sul libro*


In base a questo teorema, una matrice non singolare ($\det\ne 0$) viene anche detta **invertibile**.
Vale anche la seguente:

- #PROPOSIZIONE(4). **Prodotto di matrici invertibili**
	
	Se $\mathbf{A},\mathbf{B}$ sono due matrici quadrate non singolari, anche il prodotto $\mathbf{AB}$ è non singolare, e vale: $(\mathbf{AB})^{-1}=\mathbf{B}^{-1}\cdot\mathbf{A}^{-1}$
	
	*Dimostrazione*:
	Per il Teorema di Binet, se $\det\mathbf{A}\ne 0$ e $\det\mathbf{B}\ne 0$ si ha: $\det(\mathbf{AB})=\det\mathbf{A}\cdot\det\mathbf{B}\ne 0$
	Quindi $\mathbf{AB}$ è non singolare. Notiamo che $(\mathbf{B}^{-1}\cdot\mathbf{A}^{-1})\cdot(\mathbf{AB})=\mathbf{B}^{-1}(\mathbf{A}^{-1}\mathbf{A})\mathbf{B}=\mathbf{B}^{-1}\mathbf{I}\mathbf{B}=\mathbf{B}^{-1}\mathbf{B}=\mathbf{I}$
	Analogamente si verifica che $(\mathbf{AB})\cdot(\mathbf{B}^{-1}\mathbf{A}^{-1})=\mathbf{I}$, dunque effettivamente $\mathbf{B}^{-1}\cdot\mathbf{A}^{-1}$ è la matrice inversa di $\mathbf{AB}$.




# **Capitolo V: Sistemi lineari**


### 5.1 **Generalità. Metodo di Cramer**

Applichiamo i concetti introdotti nel [[#Capitolo IV Matrici e trasformazioni lineari|capitolo IV]] allo studio dei sistemi lineari.
Per **sistema lineare** si intende un sistema di equazioni algebriche di primo grado, il cui numero e numero di incognite possono variare.

*Ad esempio*, $\begin{cases}7x-2y+z=8\\0,1x-3y+4z=\sqrt{2}\\ x+y+z=0\end{cases}\quad$ (3 equazioni, 3 incognite)

Generalmente si scrivono al primo membro dell'equazione le incognite, moltiplicate per i loro coefficienti; al secondo membro i termini noti: se questi sono tutti nulli il sistema si dice **omogeneo**.

In questo paragrafo ci occuperemo di sistemi nei quali il numero delle equazioni uguaglia quello delle incognite. Per questi sistemi i coefficienti delle incognite si possono ordinare in una matrice quadrata.

*Dall'esempio precedente* avremo quindi: $\begin{pmatrix}7&-2&1\\0,1&-3&4\\1&1&1\end{pmatrix}$

Le righe rappresentano i coefficienti delle incognite nella $1^a,2^a$ e $3^a$ equazione, mentre le colonne rappresentano i coefficienti di $x,y$ e $z$.

Dato un sistema di $n$ equazioni in $n$ incognite (detto anche "sistema $n\times n$"), il nostro scopo è quello di determinare le eventuali <u>soluzioni</u>.
Per soluzione si intende una $n$-upla di numeri che, sostituiti ordinatamente alle incognite, soddisfino simultaneamente tutte le equazioni del sistema.

*Per esempio*, la coppia di numeri $x=1,y=-2$ è soluzione del sistema $\begin{cases}2x-3y=8\\x+7y=-13\end{cases}$

Una domanda naturale a questo punto è la seguente: un sistema lineare ha sempre soluzioni? Ed eventualmente, quante?


#### 5.1.1 **Tecniche elementari di soluzione**

Ricordiamo che due sistemi si dicono <u>equivalenti</u> se hanno le stesse soluzioni. Le operazioni che permettono di passare da un sistema ad un altro equivalente al primo sono le seguenti:

1. Sostituire ad un'equazione un'altra ad essa equivalente (ossia ottenuta dalla prima sommando membro a membro la stessa quantità, o moltiplicando ambo i membri per una stessa quantità non nulla);
2. Sommare o sottrarre membro a membro due equazioni del sistema e sostituire una delle due con quella così ottenuta.

L'applicazione congiunta (e ripetuta) delle due operazioni precedenti permette altre tipiche operazioni, come quella di ricavare una variabile in funzione delle altre da un'equazione e sostituirla in tutte le altre equazioni.

*Esempio*: si vuole risolvere il sistema $3\times 3$: $\quad{\begin{cases}x+y-z=0\\y+z=2\\3x+z=-1\end{cases}}$
Dalla seconda ricaviamo la $z$ e la sostituiamo nelle altre due: $\quad{\begin{cases}z=2-y\\ x+y-(2-y)=0\\3x+(2-y)=-1\end{cases}}$
Le ultime due equazioni sono ora un sistema nelle due incognite $(x,y)$: $\quad{\begin{cases} x+2y=0\\3x-y=-3\end{cases}}$
Sommando alla prima equazione il doppio della seconda si ha: $\quad{\begin{cases} 7x=-4\\x+2y=2\end{cases}}$

Dalla prima si ricava $x=-\frac{4}{7}$, che sostituità nella seconda dà $y=\frac{9}{7}$; ricordando infine la prima equazione del secondo sistema $(z=2-y)$, otteniamo $z=\frac{5}{7}$. Il sistema è quindi determinato, e la soluzione è il vettore $(x,y,z)=\left( -\frac{4}{7},\frac{9}{7},\frac{5}{7} \right)$.

Nelle applicazioni dell'algebra lineare si ha a che fare con sistemi di molte equazioni ed incognite, per i quali non è pensabile la soluzione manuale; si capisce così l'importanza di avere a disposizione una teoria che permetta di rispondere a domande riguardo l'esistenza e l'unicità delle soluzioni, in particolare che permetta di stabilire la solubilità di un dato sistema a priori.


#### 5.1.2 **Sistemi di $n$ equazioni in $n$ incognite, non omogenei**

Consideriamo un sistema generale di $n$ equazioni in $n$ incognite: 

${\begin{cases}a_{11}x_{1}+a_{12}x_{2}+\cdots+a_{1n}x_{n}=b_{1}\\a_{21}x_{2}+a_{22}x_{2}+\cdots+a_{2n}x_{n}=b_{2}\\ \vdots \\a_{n1}x_{1}+a_{n2}x_{2}+\cdots+a_{nn}x_{n}=b_{n}\end{cases}}$

La matrice $\mathbf{A}$ dei coefficienti è: $\quad\mathbf{A}={\begin{pmatrix}a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\ \vdots \\a_{n1}&a_{n2}&\cdots&a_{nn}\end{pmatrix}}$

Introducendo i vettori colonna $\mathbf{x}={\begin{pmatrix}x_{1}\\x_{2}\\ \vdots \\ x_{n}\end{pmatrix}}$ (delle incognite) e $\mathbf{b}={\begin{pmatrix}b_{1}\\b_{2}\\ \vdots \\ b_{n}\end{pmatrix}}$ (termini noti),

il sistema precedente si può porre nella forma matriciale $\mathbf{A}\mathbf{x}=\mathbf{b}$

Per risolvere il sistema ricorriamo all'analogia con l'equazione scalare $ax=b$: se $a\ne 0$, l'unica soluzione è $x=\frac{b}{a}$; l'analogo della condizione $a\ne 0$ è ora $\det\mathbf{A}\ne 0$.
Infatti, per il Teorema sulla matrice inversa, se $\det\mathbf{A}\ne 0 \rightarrow\exists\mathbf{A}^{-1}$; moltiplicandolo a sinistra per $\mathbf{A}^{-1}$ entrambi i membri si trova: $\mathbf{A}^{-1}(\mathbf{A}\mathbf{x})=\mathbf{A}^{-1}\cdot\mathbf{b}$
ed utilizzando la proprietà associativa per il prodotto tra matrici si ricava: $(\mathbf{A}\cdot\mathbf{A}^{-1})\mathbf{x}=\mathbf{A}^{-1}\mathbf{b}$
ed infine, poichè $\mathbf{A}^{-1}\cdot\mathbf{A}=\mathbf{I}_{n}$ e $\mathbf{I}_{n}\cdot\mathbf{x}=\mathbf{x}$, si ottiene la formula per il vettore soluzione del problema:
								$\mathbf{x}=\mathbf{A}^{-1}\cdot\mathbf{b}$

Si osserva che, sviluppando i calcoli, le componenti $x_{i}\ (i=1,2,\cdots,n)$ di $\mathbf{x}$ si ottengono:

								$x_{i}=\frac{|\mathbf{B}_{i}|}{|\mathbf{A}|}$

dove a numeratore compare il determinante della matrice $\mathbf{B}_{i}$ che si ottiene dalla matrice $\mathbf{A}$ sostituendo, alla colonna $i$-esima, la colonna dei termini noti $\mathbf{b}$:

$\mathbf{B}_{i}={\begin{pmatrix}a_{11}&a_{12}&\cdots&b_{1}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&b_{2}&\cdots&a_{2n}\\ \vdots & \vdots & & \vdots & &\vdots\\a_{n1}&a_{n2}&\cdots&b_{n}&\cdots&a_{nn}\end{pmatrix}}$

Infatti, ricordando [[#4.5 **Matrice inversa**|l'espressione della matrice inversa]], si ha:

$x_{i}=(\mathbf{A}^{-1}b)_{i}=\frac{1}{\det\mathbf{A}}\sum_{j=1}^n A_{ji}b_{j}=\frac{1}{\det\mathbf{A}}\cdot\det\mathbf{B}_{i}$

come si vede calcolando il determinante di $\mathbf{B}_{i}$ rispetto alla $i$-esima colonna.
Abbiamo così dimostrato un importante risultato:

- #TEOREMA(10). **Teorema di Cramer**
	
	Consideriamo il sistema di $n$ equazioni in $n$ incognite $\mathbf{A}\mathbf{x}=\mathbf{b}$
	(con $\mathbf{A}$ matrice $(n,n)$, $b\in\mathbb{R}^n$ assegnato e $\mathbf{x}\in\mathbb{R}^n$ incognito). Se $\det\mathbf{A}\ne 0$, il sistema è determinato, ossia ha una ed una sola soluzione.


*Esempio*:

Consideriamo il sistema ${\begin{cases}2x+y+3z=12\\4y-z=7\\5x+8z=24\end{cases}}\quad\rightarrow\quad\mathbf{A}={\begin{pmatrix}2&1&3\\0&4&-1\\5&0&8\end{pmatrix}}$

Poichè $|\mathbf{A}|=-1$, il sistema ammette soluzione unica; dall'espressione $x_{i}=\frac{|\mathbf{B}_{i}|}{|\mathbf{A}|}$ abbiamo:

$x=-{\begin{vmatrix}12&1&3\\-7&4&-1\\34&0&8\end{vmatrix}}=2$

$y=-{\begin{vmatrix}2&12&3\\0&-7&-1\\5&34&8\end{vmatrix}}=-1$

$z=-{\begin{vmatrix}2&1&12\\0&4&-7\\5&0&34\end{vmatrix}}=3$


#### 5.1.3 **Sistemi omogenei di $n$ equazioni in $n$ incognite**

Interpretiamo ora il Teorema di Cramer per i sistemi omogenei $\mathbf{A}\mathbf{x}=\mathbf{b}$
In questo caso, se $\det\mathbf{A}\ne 0$, l'unica soluzione è $\mathbf{x}=\mathbf{0}$ (infatti $\mathbf{A}^-1\cdot\mathbf{0}=\mathbf{0}$).
Viceversa, supponiamo che sia $\det\mathbf{A}=0$. Ciò significa, per il [[#4.4 **Caratteristica di una matrice**|Teorema (8)]], che le colonne di $\mathbf{A}$ $(\mathbf{a}_1,\mathbf{a}_{2},\cdots,\mathbf{a}_{n})$ sono vettori linearmente dipendenti, ossia esistono numeri $x_{1},x_{2},\cdots,x_{n}$, non tutti nulli, tali che: $x_{1}\mathbf{a}_1+x_{2}\mathbf{a}_{2}+\cdots+x_{n}\mathbf{a}_{n}=0$.

Dunque, detto $\mathbf{x}$ il vettore $(x_{1},x_{2},\cdots,x_{n})$, si ha:

$\mathbf{A}\mathbf{x}=(\mathbf{a}_{1}|\mathbf{a}_{2}|\cdots|\mathbf{a}_{n}){\begin{pmatrix}x_{1}\\x_{2}\\ \vdots \\x_{n}\end{pmatrix}}=x_{1}\mathbf{a}_1+x_{2}\mathbf{a}_{2}+\cdots+x_{n}\mathbf{a}_{n}=0$

ossia: il sistema $\mathbf{A}\mathbf{x}=\mathbf{0}$ in questo caso ammette almeno una soluzione $\mathbf{x}$ non banale ($\mathbf{x}\ne\mathbf{0}$).
Si noti che se $\mathbf{A}\mathbf{x}=\mathbf{0}$, si ha anche, $\forall\lambda\in\mathbb{R}$, $\mathbf{A}(\lambda\mathbf{x})=\lambda\mathbf{A}\mathbf{x}=\mathbf{0}$
perciò in questo caso le soluzioni del sistema omogeneo sono infinite. Riassumendo, abbiamo dimostrato il seguente Teorema:

- #TEOREMA(11). Il sistema omogeneo di $n$ equazioni in $n$ incognite $\mathbf{A}\mathbf{x}=\mathbf{0}$ ha solo la soluzione banale $(\mathbf{x}=\mathbf{0})$ se e solo se $\det\mathbf{A}\ne 0$; ha almeno una soluzione non banale (ed i questo caso infinite) se e solo se $\det\mathbf{A}= 0$.

Cosa succede invece al sistema non omogeneo se $\det\mathbf{A}= 0$? A questo risponderemo successivamente col Teorema di Rouchè-Capelli. Possiamo fin d'ora fare però la seguente **osservazione**:
	Supponiamo che $\mathbf{x}_{0}$ sia una soluzione del sistema omogeneo, ossia $\mathbf{A}\mathbf{x}_{0}=0$, e $\mathbf{x}_{1}$ sia una soluzione del sistema non omogeneo, $\mathbf{A}\mathbf{x}_{1}=\mathbf{b}$.
	Allora anche $\mathbf{x}_{0}+\mathbf{x}_{1}$ è soluzione del sistema non omogeneo, infatti:
	
	$\mathbf{A}(\mathbf{x}_{0}+\mathbf{x}_{1})=\mathbf{A}\mathbf{x}_{1}+\mathbf{A}\mathbf{x}_{0}=\mathbf{b}+\mathbf{0}=\mathbf{b}$
	Se $\det\mathbf{A}= 0$, sappiamo che il sistema omogeneo ha sempre infinite soluzioni. Ne concludiamo che:
	Se $\det\mathbf{A}= 0$ e il sistema non omogeneo $\mathbf{A}\mathbf{x}=\mathbf{b}$ ha una soluzione, allora ne ha infinite.
	In altre parole, quando $\det\mathbf{A}= 0$, per il sistema non omogeneo viene necessariamente a cadere o l'esistenza o l'unicità della soluzione: <u>il sistema è impossibile o indeterminato</u>.
	Vedremo in seguito come si può prevedere se accade l'una o l'altra cosa.



### 5.2 **Immagine e nucleo di una trasformazione lineare da $\mathbb{R}^n$ a $\mathbb{R}^m$**

Per affrontare lo studio dei sistemi lineari di $n$ equazioni in $m$ incognite è utile prima studiare qualche altra proprietà delle trasformazioni lineari.

- #DEFINIZIONE(11). **Immagine**
	
	Se $\mathcal{L}$ è lineare da $\mathbb{R}^n$ a $\mathbb{R}^m$, si chiama **immagine** ([[#### 3.3.3 **Il concetto di linearità**|caso particolare della definizione data nel capitolo 3.3]]) di $\mathcal{L}$ l'insieme dei vettori di $\mathbb{R}^m$ che sono i trasformati di qualche vettore di $\mathbb{R}^n$. Tale insieme si indica con:
										$\mathrm{Im}(\mathcal{L})$
	
	Se $\mathbf{y}\in \mathrm{Im}({\mathcal{L}})$ deve essere $\mathbf{y}={\mathcal{L}}(\mathbf{x})$ per qualche $\mathbf{x}\in\mathbb{R}^n$.


Le proprietà principali sono espresse dal seguente Teorema:

- #TEOREMA(12).
	
	1) L'insieme $\mathrm{Im}(\mathcal{L})$ è un sottospazio vettoriale di $\mathbb{R}^m$;
	2) Fissate le basi in $\mathbb{R}^n$ e $\mathbb{R}^m$, sia $\mathbf{A}$ una matrice di tipo $(m,n)$ che rappresenta $\mathcal{L}$. Allora:
		
									$\dim \ \mathrm{Im}{\mathcal{L}}=rk(\mathbf{A})$
		
		(dove $rk$ indica il rango della matrice).
	
	*Dimostrazione sul libro*.

Da questo teorema segue immediatamente che <mark class="hltr-yellow">le matrici che rappresentano (rispetto a basi diverse) la stessa trasformazione lineare hanno lo stesso rango</mark>.


- #DEFINIZIONE(12). **Nucleo**
	
	Il nucleo di un'applicazione lineare $\mathcal{L}$ si indica con il simbolo $Ker (\mathcal{L})$ ed è l'insieme dei vettori di $\mathbb{R}^n$ che hanno come immagine il vettore nullo di $\mathbb{R}^m$. In simboli:
	
						$Ker(\mathcal{L})=\left\{\mathbf{x}\in\mathbb{R}^n \ | \ \mathcal{L}(\mathbf{x})=\mathbf{0} \in \mathbb{R}^m\right\}$
	
	Anche $Ker (\mathcal{L})$ è uno spazio vettoriale.


Vale l'importante formula che lega le dimensioni di immagine e nucleo per una generica trasformazione lineare $\mathcal{L}$:

- #TEOREMA(13). Se $\mathcal{L}:\mathbb{R}^n\rightarrow\mathbb{R}^m$ è una trasformazione lineare, allora:
	
							$\dim Ker(\mathcal{L})+\dim \mathrm{Im}(\mathcal{L})=n$
	
	*Dimostrazione sul libro*.


*Esempio*: Sia $\mathcal{L}$ la trasformazione lineare da $\mathbb{R}^3$ in $\mathbb{R}^3$ che, rispetto alle basi canoniche, è rappresentata dalla matrice $\mathbf{A}={\begin{pmatrix}1&-1&0\\-2&3&1\\-1&2&1\end{pmatrix}}$

Il rango di $\mathbf{A}$ è $rk=2$, essendo la terza colonna (o riga) somma delle altre due e 

${\begin{vmatrix}1&-1\\-2&3\end{vmatrix}}=1\ne 0$.

Dunque $\dim \mathrm{Im}(\mathcal{L})=2$ e $\dim Ker(\mathcal{L})=n-rk=2-1=1$.

Per determinare $\mathrm{Im}(\mathcal{L})$ calcoliamo:

$\mathbf{A}{\begin{pmatrix}x_{1}\\x_{2}\\ x_{3}\end{pmatrix}}={\begin{pmatrix}1&-1&0\\-2&3&1\\-1&2&1\end{pmatrix}}{\begin{pmatrix}x_{1}\\x_{2}\\ x_{3}\end{pmatrix}}={\begin{pmatrix}x_{1}-x_{2}\\-2x_{1}+3x_{2}+x_{3}\\-x_{1}+2x_{2}+x_{3}\end{pmatrix}}={\begin{pmatrix}y_{1}\\ y_{2}\\ y_{3}\end{pmatrix}}$

Poichè $y_{3}=y_{2}+y_{1}$, $\mathrm{Im}(\mathcal{L})$ coincide col piano di equazione $y_{1}+y_{2}-y_{3}=0$

Detto altrimenti, il generico elemento di $\mathrm{Im}(\mathcal{L})$ è del tipo: ${\begin{pmatrix}y_{1}\\ y_{2}\\ y_{1}+y_{2}\end{pmatrix}}$ ossia $y_{1}{\begin{pmatrix}1\\0\\1\end{pmatrix}}+y_{2}{\begin{pmatrix}0\\1\\1\end{pmatrix}}$
pertanto una base di $\mathrm{Im}(\mathcal{L})$ è costituita dai due vettori ${\begin{pmatrix}1\\0\\1\end{pmatrix}}$ e ${\begin{pmatrix}0\\1\\1\end{pmatrix}}$.

Per determinare il nucleo ($Ker (\mathcal{L})$), occorre risolvere il sistema omogeneo:

${\begin{cases}x_{1}-x_{2}=0\\-2x_{1}+3x_{2}+x_{3}=0\end{cases}}$

dal quale abbiamo omesso la terza equazione, in quanto dipendente dalle prime due. Si trova subito $x_{2}=x_{1}$ e $x_{3}=-x_{1}$, per cui il generico vettore del nucleo è della forma $\lambda{\begin{pmatrix}1\\1\\-1\end{pmatrix}}$, $\lambda\in\mathbb{R}$.


#### 5.2.1 **Trasformazioni iniettive e suriettive**

- #DEFINIZIONE(13). Se $\mathrm{Im}(\mathcal{L})=\mathbb{R}^m$, si dice che $\mathcal{L}$ è **suriettiva**.
	
	Ciò significa che l'equazione $\mathcal{L}(\mathbf{x})=\mathbf{b}$ ha <u>almeno una soluzione</u> $\mathbf{x}$, indipendentemente da $\mathbf{b}$.


- #DEFINIZIONE(14). Se $Ker(\mathcal{L})=\left\{\mathbf{0}\right\}$, si dice che $\mathcal{L}$ è **iniettiva**.
	
	Ciò significa che l'equazione $\mathcal{L}(\mathbf{x})=\mathbf{0}$ ha <u>solo la soluzione nulla</u>.
	Per la linearità di $\mathcal{L}$, questo è equivalente ad affermare che l'equazione $\mathcal{L}(\mathbf{x})=\mathbf{b}$ ha al più (massimo) una soluzione $\mathbf{x}$, indipendentemente da $\mathbf{b}$ (infatti se $\mathbf{x}_{1},\mathbf{x}_{2}$ sono due soluzioni di $\mathcal{L}(\mathbf{x})=\mathbf{b}$, per linearità $\mathcal{L}(\mathbf{\mathbf{x}_{1}-\mathbf{x}_{2}})=\mathbf{b}-\mathbf{b}=\mathbf{0}$, dunque $\mathbf{x}_{1}=\mathbf{x}_{2}$).


- #DEFINIZIONE(15). Se $\mathcal{L}$ è sia iniettiva che suriettiva, si dice che $\mathcal{L}$ è **biiettiva**; la corrispondenza stabilita da $\mathcal{L}$ è **biunivoca**.
	
	In tal caso l'equazione $\mathcal{L}(\mathbf{x})=\mathbf{b}$ ha una ed una sola soluzione $\mathbf{x}$, indipendentemente da $\mathbf{b}$.
	Interessante è se $n=m$: in tal caso il Teorema (13) implica che
	
					$\dim Ker(\mathcal{L})=0\iff\dim \mathrm{Im}(\mathcal{L})=n$
	
	e perciò, per trasformazioni lineari $\mathcal{L}$ da $\mathbb{R}^n$ a $\mathbb{R}^n$, iniettività equivaale a suriettività (e quindi biunivocità).

Detto altrimenti:

- #PROPOSIZIONE(5). Se $\mathcal{L}$ è una trasformazione lineare da $\mathbb{R}^n$ a $\mathbb{R}^n$, per l'equazione $\mathcal{L}(\mathbf{x})=\mathbf{b}$ si può affermare che c'è esistenza di soluzione $(\forall \ \mathbf{b})$ se e solo se c'è unicità di soluzione.


Sempre dal Teorema (13), infine, si legge che se $n\ne m$ la trasformazione lineare $\mathcal{L}$ non può essere biunivoca.



### 5.3 **Sistemi generali. Teorema di Rouchè-Capelli**


Consideriamo ora il sistema ${\begin{cases}a_{11}x_{1}+a_{12}x_{2}+\cdots+a_{1n}x_{n}=b_{1}\\a_{21}x_{1}+a_{22}x_{2}+\cdots+a_{2n}x_{n}=b_{2}\\ \vdots \\a_{m1}x_{1}+a_{m2}x_{2}+\cdots+a_{mn}x_{n}=b_{n}\end{cases}}$

costituito da $m$ equazioni in $n$ incognite ($m,n$ qualsiasi).
Sia $\mathbf{A}$ la matrice $(m,n)$ dei coefficienti del sistema. Pensando di fissare in $\mathbb{R}^n$ e $\mathbb{R}^m$ le rispettive basi canoniche, sia $L:\mathbb{R}^n\rightarrow\mathbb{R}^m$ la trasformazione lineare rappresentata da $\mathbf{A}$. Il sistema lineare può dunque riscriversi nella forma $L(\mathbf{x})=\mathbf{b}$ o anche $\mathbf{A}\mathbf{x}=\mathbf{b}$, con $\mathbf{x}\in\mathbb{R}^n,\mathbf{b}\in\mathbb{R}^m$. Risolvere il sistema significa trovare quali vettori $\mathbf{x}\in\mathbb{R}^n$ hanno come immagine attraverso $L$ il vettore $\mathbf{b}\in\mathbb{R}^m$. Vale in proposito il seguente risultato:

- #TEOREMA(14). **Teorema di Rouchè-Capelli**
	
	Sia $\mathbf{A}$ la matrice dei coefficienti del sistema appena considerato e $\mathbf{B}=(\mathbf{A}|\mathbf{b})$ la matrice completa, ottenuta orlando la matrice $\mathbf{A}$ con la colonna dei termini noti.
	Allora il sistema ha soluzioni se e solo se la matrice $\mathbf{A}$ e la matrice $\mathbf{B}$ hanno **rango uguale**.
	
	*Dimostrazione*:
	
	Per quanto premesso all'enunciato del teorema, il sistema è risolubile se e solo se $\mathbf{b}\in \mathrm{Im}(L)$. Indicando con $(\mathbf{a}_1,\mathbf{a}_{2},\cdots,\mathbf{a}_{n})$ le colonne di $\mathbf{A}$ e con $\mathbf{e}_{j}$ i vettori della base canonica di $\mathbb{R}^n$, si ha $\mathbf{A}\mathbf{e}_{j}=\mathbf{a}_{j}$
	cioè le colonne della matrice $\mathbf{A}$ sono i trasformati dei vettori della base canonica in $\mathbb{R}^n$.
	Di conseguenza, ogni elemento di $\mathrm{Im}(L)$ è combinazione lineare delle colonne di $\mathbf{A}$, perchè ogni vettore $\mathbf{x}=\sum x_{j}\mathbf{e}_{j}\in\mathbb{R}^n$ si ha:
	
	$\mathbf{A}\mathbf{x}=\sum x_{j}\mathbf{A}\mathbf{e}_{j}=\sum x_{j}\mathbf{a}_{j}$
	
	Dunque il sistema è solubile se e solo se $\mathbf{b}$ è combinazione lineare delle colonne di $\mathbf{A}$, ossia, ricordando che $\dim \mathrm{Im}(L)=rk(\mathbf{A})$, se e solo se $rk(\mathbf{A}|\mathbf{b})=rk(\mathbf{A})$
	
	Osserviamo che, se il sistema omogeneo $(\mathbf{b}=\mathbf{0})$, la condizione $rk(\mathbf{A})=rk(\mathbf{B})$ è sempre soddisfatta. In questo caso l'insieme delle soluzioni del sistema è lo spazio $Ker(L)$. Sempre per il Teorema (13) avremo che $\dim Ker(L)+\dim \mathrm{Im}(L)=n$
	
	Inoltre $\dim \mathrm{Im}(L)=rk(\mathbf{A})$; perciò $\dim Ker (L)=n-rk(\mathbf{A})$


Abbiamo così dimostrato il seguente:

- #TEOREMA(15). Le soluzioni del sistema omogeneo formano uno spazio vettoriale di dimensione $n-r$$\quad(r=rk(\mathbf{A}))$. Si dice anche che il sistema ha $\infty^{n-r}$ soluzioni, per indicare che le soluzioni sono **infinite** e dipendono da $n-r$ parametri arbitrari.


Supponiamo ora che il sistema non omogeneo sia <u>risolubile</u>, ovvero supponiamo sia soddisfatta l'ipotesi del Teorema di Rouchè-Capelli, e chiediamoci: quante sono le sue soluzioni?

- #TEOREMA(16). Se il sistema precedentemente considerato ammette una soluzione $\mathbf{x}_{1}$, le soluzioni del sistema sono tutte e sole le $n$-uple del tipo $\mathbf{x}_{1}+\mathbf{x}_{0}$
	
	al variare di $\mathbf{x}_{0}$ in $Ker(L)$. (ossia al variare di $\mathbf{x}_{0}$ tra le soluzioni del sistema omogeneo).
	Pertanto il sistema non omogeneo ha $\infty^{n-r}$ soluzioni, dove $(r=rk(\mathbf{A}))$.
	
	*Dimostrazione*:
	
	Se $L(\mathbf{x}_{1})=\mathbf{b}$ e $\mathbf{x}_{0}\in Ker(L)$, $\quad L(\mathbf{x}_{1}+\mathbf{x}_{0})=L(\mathbf{x}_{1})+L(\mathbf{x}_{0})=\mathbf{b}+\mathbf{0}=\mathbf{b}$,
	
	perciò ogni $n$-upla del tipo $\mathbf{x}_{1}+\mathbf{x}_{0}$ è soluzione del sistema.
	Viceversa, sia $\mathbf{x}_{2}$ una soluzione del sistema, e definiamo $\mathbf{x}_{0}=\mathbf{x}_{2}-\mathbf{x}_{1}$. Risulta:
	$L(\mathbf{x}_{0})=L(\mathbf{x}_{2}-\mathbf{x}_{1})=L(\mathbf{x}_{2})-L(\mathbf{x}_{1})=\mathbf{b}-\mathbf{b}=0$,
	
	perciò $\mathbf{x}_{0}\in Ker(L)$. Dunque $\mathbf{x}_{2}=\mathbf{x}_{1}+\mathbf{x}_{0}$ con $\mathbf{x}_{0}\in Ker(L)$, ossia ogni soluzione del sistema si può scrivere a questo modo. Poichè $\mathbf{x}_{0}$ dipende da $n-r$ parametri arbitrari e $\mathbf{x}_{1}$ è fissato, anche la generica soluzione del sistema non omogeneo dipende da $n-r$.


Abbiamo fin qui chiarito le condizioni che permettono di decidere se il sistema è risolubile o no, e in caso affermativo abbiamo "contato" le soluzioni.
Illustriamo ora il metodo con cui si possono effettivamente determinare.

Supponendo verificata l'ipotesi $rk(\mathbf{A}|\mathbf{b})=rk(\mathbf{A})=r$ si può eseguire questo **schema risolutivo**
	1) Si isola un minore di ordine $r$ estratto dalla matrice $\mathbf{A}$, non singolare;
	2) Del sistema si considerano solo le $r$ equazioni corrispondenti alle $r$ righe del minore; le alte $m-r$ equazioni vengono eliminate: infatti, queste sono automaticamente soddisfatte quando lo sono le prime $r$;
	3) Al primo membro si mantengono le $r$ incognite i cui coefficienti costituiscono le $r$ colonne del minore; i termini contenenti le altre $n-r$ incognite si trasportano al secondo membro;
	4) Si ottiene un sistema di $r$ equazioni ed $r$ incognite, al quale si può applicare il metodo di Cramer (o qualunque altro);
	5) Le soluzioni trovate dipendono dalle $n-r$ incognite portare al secondo membro, che possono assumere valori arbitrari.


- Si noti che l'unico caso in cui il sistema è determinato è quando $r=n$ ($n=$ numero di incognite che compaiono nel sistema, $r=rk(\mathbf{A})$ ed uguaglia il numero di incognite che si riescono a ricavare).
- Se $r<n$, se il sistema è risolubile è sempre indeterminato, con $\infty^{n-r}$ soluzioni.

Notiamo anche che nella teoria esposta in questo paragrafo rientra il particolare caso dei sistemi non omogenei di $n$ equazioni in $n$ incognite, con determinante nullo, caso che era stato lasciato sospeso [[#5.1.3 **Sistemi omogenei di $n$ equazioni in $n$ incognite**|nel paragrafo 5.1.3]].

I risultati di questo paragrafo riguardanti le soluzioni dei sistemi lineari si possono riformulare in termini di relazioni tra particolari sottospazi associati alle righe o colonne della matrice del sistema. Possiamo associare ad una matrice $\mathbf{A}$ di ordine $m\times n$ i seguenti sottospazi:

- Lo spazio generato dalle colonne di $\mathbf{A}$, indicato con $R(\mathbf{A})$, sottospazio di $\mathbb{R}^m$;
- $Ker(\mathbf{A})$, sottospazio di $\mathbb{R}^n$;
- Lo spazio generato dalle righe di $\mathbf{A}$, ossia $R(\mathbf{A})^\top$, sottospazio di $\mathbb{R}^n$;
- $Ker(\mathbf{A})^\top$, sottospazio di $\mathbb{R}^m$.

Sappiamo che $\dim R(\mathbf{A})=\dim R(\mathbf{A}^\top)=r$
e che $\dim Ker(\mathbf{A})=n-r, \dim Ker (\mathbf{A}^\top)=m-r$

Il seguente teorema permette di rileggere in termini di relazioni tra tali sottospazi la teoria finora svolta:

- #TEOREMA(17). Si ha:
	
	1. $R(\mathbf{A})=[Ker(\mathbf{A}^\top)]^\perp$ ovvero: $\quad R(\mathbf{A})\oplus Ker(\mathbf{A}^\top)=\mathbb{R}^m$
	2. $R(\mathbf{A}^\top)=[Ker(\mathbf{A})]^\perp$ ovvero: $\quad R(\mathbf{A}^\top)\oplus Ker(\mathbf{A})=\mathbb{R}^n$
	
	*Dimostrazione*:
	
	Siano $\mathbf{b}\in R(\mathbf{A})$ e $\mathbf{y}\in Ker(\mathbf{A}^\top)$. Allora $\mathbf{b}=\mathbf{A}\mathbf{x}$, per qualche $\mathbf{x}\in \mathbb{R}^n$. Si ha:
	
	$\mathbf{y}^\top\mathbf{b}=\mathbf{y}^\top(\mathbf{A}\mathbf{x})=(\mathbf{A}^\top\mathbf{y})^\top\mathbf{x}=\mathbf{0}^\top\mathbf{x}=0$
	
	Pertanto $R(\mathbf{A})$ e $Ker(\mathbf{A}^\top)$ sono ortogonali. Per mostrare che $R(\mathbf{A})\oplus Ker(\mathbf{A}^\top)=\mathbb{R}^m$ basta far vedere che qualunque vettore ortogonale a $R(\mathbf{A})$ appartiene a $Ker(\mathbf{A}^\top)$.
	Sia dunque $\mathbf{y}\in R(\mathbf{A})^\top$. Allora qualunque sia $\mathbf{x}\in\mathbb{R}^n$,
	
	$(\mathbf{A}^\top\mathbf{t})^\top\mathbf{x}=\mathbf{y}^\top(\mathbf{A}\mathbf{x})=\mathbf{0}^\top\mathbf{x}=0$
	
	che implica $\mathbf{A}^\top\mathbf{y}=\mathbf{0}$ e cioè $\mathbf{y}\in Ker(\mathbf{A}^\top)$.
	Il secondo punto del teorema si dimostra in modo analogo scambiando $\mathbf{A}$ con $\mathbf{A}^\top$.


Interpretiamo il Teorema in termini di soluzione del sistema $\mathbf{A}\mathbf{x}=\mathbf{b}$.
Il primo punto equivale ad affermare che il sistema è risolubile se e solo se $\mathbf{b}$ è ortogonale al nucleo di $\mathbf{A}^\top$ (versione del Teorema di Rouchè-Capelli).
Il secondo punto equivale ad affermare che ogni soluzione si ottiene aggiungendo ad una soluzione particolare un elemento del nucleo di $\mathbf{A}$.
Una conseguenza di queste affermazioni è:

- #TEOREMA(17), #COROLLARIO(1). La matrice $\mathbf{A}$ (come trasformazione lineare) realizza una corrispondenza biunivoca tra $R(\mathbf{A}^\top)$ e $R(\mathbf{A})$, ossia tra lo spazio delle sue righe e quello delle sue colonne.
	
	In altri termini, il corollario afferma che, per ogni elemento $\mathbf{b}$ nello spazio delle colonne di $\mathbf{A}$ esiste un'unica soluzione $\mathbf{x}$ appartenente allo spazio delle righe di $\mathbf{A}$ del sistema $\mathbf{A}\mathbf{x}=\mathbf{b}$.
	È poi facile convincersi, dal secondo punto del Teorema, che tale soluzione è quella di minimo modulo tra tutte le possibili soluzioni del sistema.


*Esempio*:
Consideriamo il sistema di quattro equazioni in tre incognite: ${\begin{cases}x+2y+3z=1\\x-2y-z=0\\2x+8y+10z=3\\2x+2z=1\end{cases}}$
Si ha: $\mathbf{A}={\begin{pmatrix}1&2&3\\1&-2&-1\\2&8&10\\2&0&2\end{pmatrix}},\quad\mathbf{B}={\begin{pmatrix}1&2&3&1\\1&-2&-1&0\\2&8&10&3\\2&0&2&1\end{pmatrix}}$

In entrambe le matrici la terza riga si ottiene moltiplicando la prima per $3$ e sottraendo la seconda, mentre la quarta riga è la somma delle prime due. Quindi $rk(\mathbf{A})\le 2,rk(\mathbf{B})\le 2$.

Essendo $\det{\begin{pmatrix}1&2\\1&-2\end{pmatrix}}=-4\ne 0$, $rk(\mathbf{A})=rk(\mathbf{B})=2$. In base al Teorema di Rouchè-Capelli il sistema è quindi risolubile. Per determinare le soluzioni usiamo la procedura indicata sopra:

1. Isoliamo il minore $\begin{vmatrix}1&2\\1&-2\end{vmatrix}$ corrispondente alle prime due righe e due colonne di $\mathbf{A}$;
2. Eliminiamo la terza e la quarta equazione del sistema;
3. Portiamo a secondo membro i termini contenenti $z$;
4. Si ottiene il sistema di due equazioni in due incognite: ${\begin{cases}x+2y=1-3z\\x-2y=z\end{cases}}$

Sottraendo la seconda equazione dalla prima si ottiene: ${\begin{cases}x+2y=1-3z\\4y=1-4z\end{cases}}$
da cui $y=\frac{1-4z}{4},x=1-3z-2\left( \frac{1-4z}{4} \right)=\frac{1}{2}-z$.

In conclusione le soluzioni sono assegnate dalla formula $x=\frac{1}{2}-z$ e $y=\frac{1-4z}{4}$ 
(con $z$ arbitrario).
Detto altrimenti, le soluzioni sono tutti i vettori del tipo $\left( \frac{1}{2}-z,\frac{1-4z}{4},z \right)$
(con $z\in\mathbb{R}$ arbitrario).
Le soluzioni sono $\infty^1$, ovvero dipendono da un parametro arbitrario: $z$.



### 5.4 **Metodo di eliminazione di Gauss**

Presentiamo ora un metodo per risolvere i sistemi lineari, che è alternativo rispetto a quello basato sul Teorema di Cramer incontrato in precedenza e si presta meglio ad essere tradotto in un effettivo algoritmo risolutivo.

Cominciamo con un sistema di $n$ equazioni in $n$ incognite: $\mathbf{A}\mathbf{x}=\mathbf{b}$
L'idea molto semplice è quella di procedere con una serie di operazioni elementari sulle equazioni del sistema, ossia sulle righe della matrice completa, in modo da ottenere ogni volta un sistema equivalente (cioè con le stesse soluzioni) cercando di ridursi alla fine ad un sistema $\mathbf{A}^*\mathbf{x}=\mathbf{b}^*$ del tipo <u>triangolare</u> seguente:

${\begin{cases}d_{1}x_{1}+a_{12}^*x_{2}+a_{13}^*x_{3}+\cdots+a_{1n}^*x_{n}=b_{1}^*\\d_{2}x_{2}+a_{23}^*x_{3}+\cdots+a_{2n}^*x_{n}=b_{2}^*\\ \vdots \\d_{n-1}x_{n-1}+a_{n-1,n}^*x_{n}=b_{n-1}^*\\d_{n}x_{n}=b_{n}^*\end{cases}}$

i coefficienti sulla diagonale principale $d_{1},d_{2},\cdots,d_{n}$ alla fine del processo prendono il nome di **elementi pivotali** o **pivot**. Si noti che $\det\mathbf {A}^*=d_{1}d_{2}\cdots d_{n}$.

Se i pivoti sono tutti diversi da zero, il sistema ha una ed una sola soluzione, facilmente calcolabile con un procedimento di sostituzione "all'indietro": dall'ultima equazione si ricava $x_{n}=b_{n}^*d_{n}^{-1}$; sostituendo nella penultima trovo: $x_{n-1}=(-a_{n-1,n}^*b_{n}^*+b_{n-1}*)d_{n-1}$
e così via fino a determinare $x_{1}$.

Se qualche pivot è nullo la matrice $\mathbf{A}^*$ è singolare (e quindi anche $\mathbf{A}$).
Abbiamo già visto che in tal caso il sistema può non essere risolubile oppure ammettere infinite soluzioni. Esamineremo più avanti come si sviluppa il metodo in questi casi ritrovando i risultati teorici delle sezioni precedenti.


Illustriamo il metodo di eliminazione mediante un *esempio*:

Sia da risolvere il sistema: ${\begin{cases}2x+y+z=1\\4x+y=-2\\-2x+2y+z=-5\end{cases}}$

Si comincia col determinare un sistema equivalente (stesse soluzioni) eliminando l'incognita $x$ nella seconda e nella terza equazione, mediante le seguenti operazioni:

1) Si sottrae dalla seconda eq. la prima moltiplicata per $2$;
2) Si somma alla terza eq. la prima, ottenendo così il sistema: ${\begin{cases}2x+y+z=1\\-y-2z=-4\\3y+2z=-4\end{cases}}$
	evidentemente il primo pivot è $d_{1}=2$;
3) Si ignora la prima equazione e si elimina l'incognita $y$ dalla terza equazione, ottenendo così: 
	
	${\begin{cases}2x+y+z=1\\-y-2z=-4\\-4z=-16\end{cases}}$
	
	gli altri pivot sono $d_{2}=-1,d_{3}=-4$.
	
	La soluzione è ora immediata: $z=4,y=-4,x=\frac{1}{2}$.


Si capisce facilmente come il metodo sia generalizzabile ad un sistema di $n$ equazioni in $n$ incognite, dove possiamo sempre supporre $d_{1}=a_{11}\ne 0$. Il primo passo consiste nell'aggiungere alle altre equazioni opportuni multipli della prima, in modo da azzerare tutti i coefficienti sotto il primo pivot $d_{1}$. Nel secondo si ignora la prima equazione e si aggiungono alle altre opportuni multipli della seconda, in modo da azzerare tutti i coefficienti sotto il secondo pivot $d_{2}$.
Se ad ogni passo si produce un pivot non nullo, l'azzeramento dei coefficienti sotto ogni pivot è sempre possibile e si procede così fino alla forma triangolare alta finale. Una sostituzione all'indietro fornisce immediatamente la soluzione.

Vediamo ora come in generale si traduce l'idea precedente in un algoritmo.


#### 5.4.1 **Sistemi $n\times n$. Il caso dei pivot tutti diversi da zero. Fattorizzazione LU di una matrice quadrata**

Introduciamo anzitutto qualche notazione matriciale che ci servirà a rappresentare le operazioni elementari che trasformano il sistema in uno ad esso equivalente.

- **Matrici di permutazione**: prendiamo la matrice identità di ordine $n$ e scambiamo le due righe $j$ e $k$: indichiamo la nuova matrice con $\mathbf{P}_{jk}$. Sia ora $\mathbf{A}$ una matrice di ordine $n\times n$: allora la matrice $\mathbf{P}_{jk}\mathbf{A}$ si ottiene da $\mathbf{A}$ scambiando le righe $j$ e $k$.
	
	*Esempio*:
	
	$\mathbf{A}={\begin{pmatrix}3&1&5\\4&1&0\\-2&2&1\end{pmatrix}}, \mathbf{P}_{jk}=\begin{pmatrix}0&0&1\\0&1&0\\1&0&0\end{pmatrix}\rightarrow\mathbf{P}_{13}\mathbf{A}=\begin{pmatrix}0&0&1\\0&1&0\\1&0&0\end{pmatrix}{\begin{pmatrix}3&1&5\\4&1&0\\-2&2&1\end{pmatrix}}={\begin{pmatrix}-2&2&1\\4&1&0\\3&1&5\end{pmatrix}}$
	
	La prima e la terza riga sono scambiate. Se postmoltiplichiamo per $\mathbf{P}_{jk}$, cioè calcoliamo $\mathbf{A}\mathbf{P}_{jk}$, sono le colonne di $\mathbf{A}$ che vengono scambiate:
	
	$\mathbf{A}\mathbf{P}_{jk}={\begin{pmatrix}3&1&5\\4&1&0\\-2&2&1\end{pmatrix}}\begin{pmatrix}0&0&1\\0&1&0\\1&0&0\end{pmatrix}={\begin{pmatrix}5&1&3\\0&1&4\\1&2&-2\end{pmatrix}}$


- **Matrici elementari**: introduciamo ora delle matrici che servono invece a rappresentare l'operazione di sommare o sottrarre ad un'equazione un multiplo di un'altra equazione. Indichiamo con $\mathbf{E}_{ij}(q)$ la matrice costruita sostituendo nella matrice identità lo zero in posizione $ij,i>j$, con il numero $q$. Pre/post moltiplicando una matrice $\mathbf{A}$ per $\mathbf{E}_{ij}(q)$ si aggiunge alla riga/colonna $i$ il multiplo $q$ della riga $j$.
	
	*Esempio*:
	
	$\mathbf{E}_{31}(-2)\mathbf{A}={\begin{pmatrix}1&0&0\\0&1&0\\-2&0&1\end{pmatrix}}{\begin{pmatrix}2&-1&1\\4&1&0\\1&-3&5\end{pmatrix}}={\begin{pmatrix}2&-1&1\\4&1&0\\-3&-1&3\end{pmatrix}}$
	
	e si vede che la terza riga della matrice prodotto è ottenuta sommando alla terza riga di $\mathbf{A}$ la prima riga moltiplicata per $-2$.
	Queste matrici si chiamano <u>matrici elementari</u>, sono triangolari basse e hanno $1$ sulla diagonale principale.


Rileggiamo ora il [[#5.4 **Metodo di eliminazione di Gauss**|metodo di eliminazione]] in termini matriciali. Usiamo ancora il sistema:

${\begin{pmatrix}2&-1&1\\4&1&0\\1&-3&5\end{pmatrix}}{\begin{pmatrix}x\\y \\  z\end{pmatrix}}={\begin{pmatrix}1 \\  -2 \\  -5\end{pmatrix}}$

La prima operazione (si sottrae dalla seconda eq. la prima moltiplicata per $2$) può essere realizzata mediante premoltiplicazione della matrice dei coefficienti e del vettore dei termini noti per la matrice elementare:

$\mathbf{E}_{21}(-2)={\begin{pmatrix}1&0&0 \\  -2&1&0 \\  0&0&1\end{pmatrix}}$

Analogamente, la seconda e terza operazione (si somma alla terza eq. la prima, si ignora la prima equazione e si elimina l'incognita $y$ dalla terza equazione) si realizzano premoltiplicando rispettivamente per le matrici:

$\mathbf{E}_{31}(1)={\begin{pmatrix}1&0&0 \\  0&1&0 \\  1&0&1\end{pmatrix}}$ e $\mathbf{E}_{32}(3)={\begin{pmatrix}1&0&0 \\  0&1&0 \\  0&3&1\end{pmatrix}}$, ottenendo così:

$\mathbf{E}_{32}(3)\mathbf{E}_{31}(1)\mathbf{E}_{21}(-2)={\begin{pmatrix}1&0&0 \\  -2&1&0 \\  -5&3&1\end{pmatrix}}$

che è triangolare bassa. Poniamo poi: $\mathbf{U}=\mathbf{E}_{32}(3)\mathbf{E}_{31}(1)\mathbf{E}_{21}(-2)\mathbf{A}={\begin{pmatrix}2&1&1 \\  0&-1&-2 \\  0&0&-4\end{pmatrix}}$

che è triangolare alta ed ha sulla diagonale principale i pivot. Abbiamo dunque $\mathbf{A}=\mathbf{L}\mathbf{U}$
dove $\mathbf{L}=\mathbf{E}_{21}(-2)^{-1}\mathbf{E}_{31}(1)^{-1}\mathbf{E}_{32}(3)^{-1}$.

Si può controllare facilmente che le inverse $\mathbf{E}_{ij}(q)$ si ottengono semplicemente sostituendo $-q$ a $q$, cioè:

$\mathbf{E}_{ij}(q)^{-1}=\mathbf{E}_{ij}(-q)$

Perciò: $\mathbf{L}={\begin{pmatrix}1&0&0 \\  2&1&0 \\  0&0&1\end{pmatrix}}{\begin{pmatrix}1&0&0 \\  0&1&0 \\  -1&0&1\end{pmatrix}}{\begin{pmatrix}1&0&0 \\  0&1&0 \\  0&-3&1\end{pmatrix}}={\begin{pmatrix}1&0&0 \\  2&1&0 \\  -1&-3&1\end{pmatrix}}$

che è triangolare bassa, ha gli elementi della diagonale principale tutti uguali a $1$, gli altri elementi $q_{ij}$ sono gli opposti degli elementi $i,j$ che compaiono nelle matrici $\mathbf{E}_{ij}(q)$ utilizzate per costuire $\mathbf{L}$.
Possiamo quindi scrivere: $\mathbf{A}=\mathbf{L}\mathbf{U}:{\begin{pmatrix}2&1&1\\4&1&0\\-2&2&1\end{pmatrix}}={\begin{pmatrix}1&0&0 \\  2&1&0 \\  -1&-3&1\end{pmatrix}}{\begin{pmatrix}2&1&1 \\  0&-1&-2 \\  0&0&-4\end{pmatrix}}$

La matrice $\mathbf{A}$ è stata quindi fattorizzata nel prodotto di due matrici triangolari. Le due matrici $\mathbf{L}$ ed $\mathbf{U}$ sono univocamente determinate. Infatti se $\mathbf{A}=\mathbf{L}\mathbf{U}=\mathbf{L}'\mathbf{U}'$, con $\mathbf{L}'$ ed $\mathbf{U}'$ rispettivamente triangolare bassa ed alta, si ha anche: $(\mathbf{L}')^{-1}\mathbf{L}=\mathbf{U}'\mathbf{U}^{-1}$.

Ora $(\mathbf{L}')^{-1}$ ed $(\mathbf{L}')^{-1}\mathbf{L}$ sono triangolari basse mentre $\mathbf{U}^{-1}$ ed $\mathbf{U}'\mathbf{U}^{-1}$ sono triangolari alte, con elementi uguali ad $1$ sulla diagonale principale. Ne segue che entrambi i membri sono matrici diagonali. Ma allora deve essere:

$(\mathbf{L}')^{-1}\mathbf{L}=\mathbf{U}'\mathbf{U}^{-1}=\mathbf{I}\rightarrow \mathbf{L}=\mathbf{L}', \mathbf{U}=\mathbf{U}'$.


Riassumiamo generalizzando ad una matrice quadrata di ordine $n$:

- #PROPOSIZIONE(6). Se nel processo di eliminazione di Gauss tutti i pivot sono $\ne 0$, la matrice $\mathbf{A}$ ammette la fattorizzazione $\mathbf{A}=\mathbf{L}\mathbf{U}$
	
	dove $\mathbf{L},\mathbf{U}$ sono univocamente determinate dalle seguenti proprietà:
	
	a) $\mathbf{L}$ è triangolare bassa con elementi sulla diagonale principale tutti uguali ad $1$; gli altri elementi non nulli sono i $q_{ij}$ descritti in precedenza;
	
	b) $\mathbf{U}$ è la matrice che si ottiene al termine del processo di eliminazione, è triangolare alta e gli elementi sulla diagonale principale sono i pivot.

Di conseguenza:

- #PROPOSIZIONE(6), #COROLLARIO(2). Nelle ipotesi della Proposizione precedente il sistema (di $n$ equazioni in $n$ incognite) $\mathbf{A}\mathbf{x}=\mathbf{b}$ è equivalente al sistema triangolare alto $\mathbf{U}\mathbf{x}=\mathbf{L}^{-1}\mathbf{b}$ ed ha <u>esattamente una soluzione</u>.
	
	Infatti, essendo $\mathbf{U}\mathbf{x}=\mathbf{L}^{-1}\mathbf{b}$ triangolare e con elementi $1$ sulla diagonale, può essere univocamente risolto per sostituzione all'indietro, un'equazione dopo l'altra.


#### 5.4.2 **Sistemi $n\times n$. Pivot non tutti diversi da zero**

Esaminiamo ora il caso in cui, durante il processo di eliminazione, i primi $k-1$ pivot siano non nulli, mentre $d_{k}=0$. Controlliamo gli elementi della colonna $k$-esima, sotto $d_{k}$.
Vi sono due possibilità:
	a. Tutti questi elementi sono nulli;
	b. Ne esiste uno non nullo, diciamo l'elemento $a_{lk}$.

Nel primo caso (a) la difficoltà è più seria: la matrice $\mathbf{A}$ è <u>singolare</u>. Le incognite rimaste nelle ultime $n-k+1$ equazioni sono meno di $n-k+1$ e quindi o il sistema ha infinite soluzioni oppure non ne ha alcuna. Completeremo l'analisi di questo caso considerando direttamente sistemi generali di $m$ equazioni in $n$ incognite.

Nel secondo caso (b) la difficoltà si supera facilmente scambiando le righe $k$ e $l$ ed il procedimento di eliminazione può continuare. Se proseguendo non ci si trova mai nel primo caso (a), l'eliminazione si può portare a termine.
Per quanto riguarda la fattorizzazione, lo scambio di due righe $k$ e $l$ si effettua premoltiplicando per la matrice di permutazione $\mathbf{P}_{kl}$ ottenuta dalla matrice identità scambiando quelle due righe. Nella fattorizzazione intervengono allora le matrici di permutazione $\mathbf{P}_{kl}^{-1}=\mathbf{P}_{lk}$ che non mantengono la forma triangolare delle $\mathbf{E}_{ij}(q)$. Il prodotto di tali matrici non è triangolare bassa. La fattorizzazione può tuttavia essere quasi del tutto recuperata utilizzando la seguente osservazione.
Esaminiamo la lista di scambi tra righe necessari per portare a termine l'eliminazione ed eseguiamole prima di incominciarla. In altri termini, rimpiazziamo la matrice originale $\mathbf{A}$ con una matrice $\mathbf{PA}$, dove $\mathbf{P}$ realizza tutte le permutazioni richieste di righe.
$\mathbf{P}$ è il prodotto di matrici $\mathbf{P}_{kl}$ e contiene esattamente un $1$ in ogni riga. La matrice $\mathbf{PA}$ ammette la fattorizzazione $\mathbf{LU}$ con pivot tutti diversi da zero.

- #PROPOSIZIONE(7). Se $\mathbf{A}$ è <u>non singolare</u> esiste una matrice di permutazione $\mathbf{P}$ tale che la matrice $\mathbf{PA}$ ammette la fattorizzazione $\mathbf{PA}=\mathbf{LU}$ (con tutti i pivot diversi da zero).

- #PROPOSIZIONE(7), #COROLLARIO(3). Nelle ipotesi della Proposizione precedente il sistema (di $n$ equazioni in $n$ incognite) $\mathbf{A}\mathbf{x}=\mathbf{b}$ è equivalente al sistema triangolare alto $\mathbf{U}\mathbf{x}=\mathbf{L}^{-1}\mathbf{P}\mathbf{b}$ ed ha <u>esattamente una soluzione</u>.


#### 5.4.3 **Sistemi lineari di $m$ equazioni in $n$ incognite. Fattorizzazione di una matrice rettangolare**

Esaminiamo ora il caso di un sistema generale di $m$ equazioni in $n$ incognite $\mathbf{A}\mathbf{x}=\mathbf{b}$, con $m\ne n$.
Il metodo di eliminazione di Gauss si può applicare anche in questo caso.
Quando però tutto viene riletto in termini di fattorizzazione della matrice $\mathbf{A}$, si presenta qualche differenza.

Ci serviamo di un *esempio* di $4$ eq. in $5$ incognite, ma lavorando direttamrnte sulla matrice dei coefficienti del sistema, che supponiamo sia:

$\mathbf{A}={\begin{pmatrix}1&3&3&2&0 \\  2&6&9&1&-6 \\  -1&-3&3&0&-2 \\  -1&-3&1&-6&-8\end{pmatrix}}$

Il primo pivot è $a_{11}=1\ne 0$, per cui le consuete operazioni elementari permettono di produrre zeri nella prima colonna sotto quel pivot; si ottiene:

${\begin{pmatrix}1&3&3&2&0 \\  0&0&3&-3&-6 \\  0&0&6&2&-2 \\  0&0&4&-4&-8\end{pmatrix}}$

Il secondo pivot è $0$, gli elementi sottostanti sono nulli e lo scambio di righe non può produrre un pivot $\ne 0$.
Per procedere oltre con l'eliminazione si va al primo elemento non nullo in seconda riga, nelle colonne successive; nell'esempio è $3$ in terza colonna. Annulliamo gli elementi sotto il $3$ con le operazioni: $3^a \ riga-(2\times 2^a \ riga)$ e $4^a \ riga-\left( \frac{4}{3}\times 2^a \ riga \right)$.

Si ottiene così la matrice: $\mathbf{U}={\begin{pmatrix}1&3&3&2&0 \\  0&0&3&-3&-6 \\  0&0&0&8&10 \\  0&0&0&0&0\end{pmatrix}}$

Si considera ora la terza colonna dove si riconosce che il nuovo pivot è $8$.
Essendoci solo zeri nell'ultima riga, il processo di eliminazione è finito. La forma finale di $\mathbf{U}$ è triangolare alta (in questo caso detta anche <u>trapezoidale alta</u>) con pivot uguali a $1$ (prima riga), $3$ (seconda riga) e $8$ (terza riga) non nulli.


Come prima, a partire da $\mathbf{U}$ possiamo ricostruire la matrice $\mathbf{A}$ premoltiplicando $\mathbf{U}$ per le inverse delle matrici elementari $\mathbf{E}_{ij}(q)$. Il prodotto $\mathbf{L}$ di queste ultime è una matrice quadrata e triangolare bassa di ordine $m$, il numero di righe di $\mathbf{A}$.
Essendo $\mathbf{L}$ invertibile, $\mathbf{A}=\mathbf{L}\mathbf{U}$ ha lo stesso rango di $\mathbf{U}$.
Nel caso siano necessari scambi di righe nulla cambia rispetto al caso di una matrice quadrata, con l'introduzione della matrice di permutazione $\mathbf{P}$.

Riassumiamo le conclusioni:

- #PROPOSIZIONE(8). Sia $\mathbf{A}$ una matrice $m\times n$. Esistono una matrice di permutazione $\mathbf{P}$, una matrice quadrata $\mathbf{L}$ di ordine $m$, triangolare bassa, ed una matrice $\mathbf{U}$ di ordine $m\times n$, trapezoidale alta, tali che $\mathbf{PA}=\mathbf{LU}$
	Inoltre, $rk(\mathbf{U})=rk(\mathbf{A})$.

Il sistema $\mathbf{A}\mathbf{x}=\mathbf{b}$ è equivalente al sistema trapezoidale $\mathbf{U}\mathbf{x}=\mathbf{L}^{-1}\mathbf{P}\mathbf{b}$.


Una volta arrivati a tale forma trapezoidale ($\mathbf{U}\mathbf{x}=\mathbf{L}^{-1}\mathbf{P}\mathbf{b}$) è immediato trarre conclusioni sulla risolubilità o meno del sistema.
Tornando all'esempio, poichè vi sono tre pivot non nulli, $rk(\mathbf{A})=3$.

Una prima conclusione è che il sistema omogeneo finale: ${\begin{cases}x_{1}+3x_{2}+3x_{3}+2x_{4}=0 \\  3x_{3}-3x_{4}-6x_{5}=0 \\  8x_{4}+10x_{5}=0 \\  0=0\end{cases}}$
equivale al sistema triangolare: ${\begin{cases}x_{1}+3x_{3}+2x_{4}=-3x_{2} \\  3x_{3}-3x_{4}=6x_{5} \\  8x_{4}=-10x_{5}\end{cases}}$

ottenuto lasciando a primo membro le variabili corrispondendi ai pivot non nulli.
Si vede che esistono $\infty^2$ soluzioni, essendo $x_{2},x_{5}$ variabili libere.
La risolubilità del sistema non omogeneo si legge dalle righe di zeri.

Per *esempio*, se $\mathbf{b}={\begin{pmatrix}2 \\  0 \\  -1 \\  2\end{pmatrix}}$, il sistema trapezoidale finale è: ${\begin{cases}x_{1}+3x_{2}+3x_{3}+2x_{4}=2 \\  3x_{3}-3x_{4}-6x_{5}=-4 \\  8x_{4}+10x_{5}=9 \\  0=\frac{28}{3}\end{cases}}$

che evidentemente non ha soluzione. Ciò riflette il fatto che il vettore $\mathbf{L}^{-1}\mathbf{P}$ non appartiene allo spazio generato dalle colonne di $\mathbf{U}$ ([[#5.3 **Sistemi generali. Teorema di Rouchè-Capelli**|Teorema di Rouchè-Capelli)]]).




# **Capitolo VI: Autovettori ed autovalori. Diagonalizzazione**


### 6.1 **Matrici diagonalizzabili**

Consideriamo una trasformazione $\mathcal{L}$ da $\mathbb{R}^n$ a $\mathbb{R}^n$. La rappresentazione di $\mathcal{L}$ per mezzo di una matrice $\mathbf{A}$ (in questo caso quadrata di ordine $n$) dipende dalla scelta della base in $\mathbb{R}^n$.
È chiaro che se si potesse scegliere una base rispetto alla quale $\mathcal{L}$ fose rappresentata da una matrice di forma speciale, per esempio **diagonale**, si avrebbe un grande vantaggio, almeno sul piano dell'esecuzione dei calcoli.

Supponiamo, *per esempio*, che una trasformazione $\mathcal{L}:\mathbb{R}^2\rightarrow\mathbb{R}^3$, rispetto ad una opportuna base, si possa rappresentare mediante la matrice diagonale:

$\mathbf{A}={\begin{pmatrix}c_{1}&0&0 \\  0&c_{2}&0 \\  0&0&c_{3}\end{pmatrix}}$

ciò significa che la trasformazione $\mathbf{y}=\mathcal{L}(\mathbf{x})$ rispetto a questa base si scrive così:

${\begin{cases}y_{1}=c_{1}x_{1} \\  y_{2}=c_{2}x_{2} \\  y_{3}=c_{3}x_{3}\end{cases}}$

Si tratta di un'espressione particolarmente semplice, in cui ogni variabile $y_{i}$ dipende solo dalla variabile $x_{i}$, anzichè da tutte e tre ("separazione di variabili").
Geometricamente significa che abbiamo scelto un opportuno sistema di riferimento in $\mathbb{R}^3$ (non necessariamente ortogonale), rispetto al quale la trasformazione agisce come una dilatazione di un certo coefficiente $c_{i}$ su ciascun asse.
Rispetto a questa base i calcoli risultano più semplici, e le proprietà della trasformazione appaiono in modo più trasparente. Diremo in questo caso che **la trasformazione ha forma diagonale**.

Cominceremo ad esaminare come cambia la rappresentazione di $\mathcal{L}$ cambiando la base in $\mathbb{R}^n$.
Supponiamo che $\mathbb{R}^n$ sia riferito alla base canonica $\mathbf{e}^1,\mathbf{e}^{2},\cdots,\mathbf{e}^{n}$. Scegliamo ora $n$ vettori linearmente indipendenti $\mathbf{\tilde{e}}^1,\mathbf{\tilde{e}}^{2},\cdots,\mathbf{\tilde{e}}^{n}$ ed assumiamoli come nuova base.
La matrice $\mathbf{S}=(\mathbf{\tilde{e}}^1|\mathbf{\tilde{e}}^{2}|\cdots|\mathbf{\tilde{e}}^{n})$ ottenuta accostando i vettori (colonna) $\mathbf{\tilde{e}}^1,\mathbf{\tilde{e}}^{2},\cdots,\mathbf{\tilde{e}}^{n}$ rappresenta, nella base canonica, la trasformazione che fa passare da una base all'altra. Infatti, come si verifica subito: $\mathbf{S}\mathbf{e}^i=\mathbf{\tilde{e}}^i\quad (i=1,2,\cdots,n)$

Poichè i vettori $\mathbf{\tilde{e}}^i$ sono indipendenti, $\det\mathbf{S}\ne 0$, quindi $\mathbf{S}$ è invertibile, e possiamo anche scrivere:

								$\mathbf{e}^i=\mathbf{S}^{-1}\mathbf{\tilde{e}}^i$

Se quindi un vettore di $\mathbb{R}^n$ ha, rispetto alla base canonica, le coordinate $\mathbf{x}=(x_{1},x_{2},\cdots,x_{n})$, nella 
nuova base avrà coordinate $\mathbf{\tilde{x}}=(\tilde{x}_{1},\tilde{x}_{2},\cdots,\tilde{x}_{n})$ date da:

								$\mathbf{\tilde{x}}=\mathbf{S}^{-1}\mathbf{x}$

Infatti, se la matrice $\mathbf{S}=(s_{ij})$ ha per colonne le rappresentazioni dei vettori $\mathbf{\tilde{e}}^i$ nella base di $\mathbf{e}_{i}$, significa che $s_{ij}=(\mathbf{\tilde{e}}_{j})_{i}$, quindi da:

								$\mathbf{x}=\sum_{j=1}^n \tilde{x}_{j}\mathbf{\tilde{e}}_{j}$

ricaviamo: $x_{i}=\sum_{j=1}^n \tilde{x}_{j}(\mathbf{\tilde{e}}_{j})_{i}=\sum_{j=1}^n \tilde{x}_{j}s_{ij}$, ossia $\mathbf{x}=\mathbf{S}\mathbf{\tilde{x}}$.

Allora, se $\mathbf{y}=\mathbf{A}\mathbf{x}$ nella base canonica, risulta: $\mathbf{\tilde{y}}=\mathbf{S}^{-1}\mathbf{y}=\mathbf{S}^{-1}\mathbf{A}\mathbf{x}=\mathbf{S}^{-1}\mathbf{A}\mathbf{S}\mathbf{\tilde{x}}$
e perciò la trasformazione $\mathcal{L}$ nella nuova base è rappresentata dalla matrice:

								$\mathbf{\tilde{A}}=\mathbf{S}^{-1}\mathbf{A}\mathbf{S}$

Si dice che due matrici $\mathbf{A},\mathbf{\tilde{A}}$ legate da quest'ultima relazione (con $\mathbf{S}$ ovviamente matrice invertibile) sono **SIMILI**, o **EQUIVALENTI**.

Si noti che dal [[#4.3 **Determinante**|Teorema di Binet]] segue che <u>due matrici simili hanno lo stesso determinante</u>. Infatti, se $\mathbf{\tilde{A}}=\mathbf{S}^{-1}\mathbf{A}\mathbf{S}$ si ha: $|\mathbf{\tilde{A}}|=|\mathbf{S}^{-1}\mathbf{A}\mathbf{S}|=|\mathbf{S}^{-1}|\mathbf{A}||\mathbf{S}|=\frac{1}{|\mathbf{S}|}|\mathbf{A}||\mathbf{S}|=|\mathbf{A}|$.

È utile evidenziare anche un'altra proprietà legata a questa:

- #PROPOSIZIONE(9). **Due matrici simili hanno la stessa caratteristica**.
	
	*Dimostrazione* su libro.


Diamo ora una definizione generale:

- #DEFINIZIONE(16). Diremo che una matrice quadrata $\mathbf{A}$ a elementi in $\mathbb{K}$ (dove $\mathbb{K}=\mathbb{R} \ o \ \mathbb{C}$) è **diagonalizzabile** (su $\mathbb{K}$) se esistono due matrici $\mathbf{\Lambda}$ e $\mathbf{S}$ (a elementi in $\mathbb{K}$), $\mathbf{\Lambda}$ diagonale e $\mathbf{S}$ non singolare, tali che: $\quad \mathbf{A}=\mathbf{S}\mathbf{\Lambda}\mathbf{S}^{-1}$.
	La matrice $\mathbf{S}$ si dice <u>matrice di passaggio</u>.

In questo caso esiste una base di $\mathbb{K}^n$ in cui la trasformazione che rispetto alla base canonica si rappresentava con la matrice $\mathbf{A}$, si rappresenta invece con una matrice diagonale.
Nella nuova base, quindi, la trasformazione è più semplice da studiare, quanto ha forma diagonale.

Il problema che ci poniamo è quindi: data una matrice, decidere se essa è diagonalizzabile, e in caso affermativo determinare la matrice diagonale e la matrice di passaggio. Questo problema è legato ad un altro, che ora introdurremo, quello della ricerca di **autovalori** e **autovettori** della matrice.
Notiamo esplicitamente quanto segue: poichè i numeri reali sono particolari numeri complessi, una matrice $(n,n)$ a elementi reali può vedersi sia come trasformazione lineare di $\mathbb{R}^n$ in sè che come trasformazione lineare di $\mathbb{C}^n$ in sè; in entrambi i casi ci si può chiedere se la matrice $\mathbf{A}$ è diagonalizzabile.
Ora può accadere, come vedremo, che $\mathbf{A}$ sia diagonalizzabile su $\mathbb{C}$ ma non su $\mathbb{R}$. Per una matrice a elementi reali, dunque, le due nozioni di diagonalizzabilità vanno distinte.



### 6.2 **Autovalori ed autovettori di una matrice**

Chiediamoci se esistono vettori (non nulli) di $\mathbb{K}^n$ che vengono trasformati da $\mathbf{A}$ in vettori paralleli.
Se $\mathbf{v}\in\mathbb{K}^n$ è un tale vettore, dovrà risultare $\mathbf{A}\mathbf{v}=\lambda\mathbf{v}$ per qualche $\lambda \in\mathbb{K}^n$.
In altre parole, ci stiamo chiedendo se esistono particolari vettori sui quali la trasformazione agisce come se fosse di tipo diagonale. In tal caso, preso un qualsiasi vettore $t\mathbf{v}$ parallelo a $\mathbf{v} \ (t\in\mathbb{K})$ si avrà anche, per linearità: $\mathbf{A}(t\mathbf{v})=t\mathbf{A}\mathbf{v}=(t\lambda)\mathbf{v}$ e quindi, in questo caso, possiamo affermare che la direzione di $\mathbb{K}^n$ individuata dal vettore $\mathbf{v}$ è trasformata in se stessa.

Scrivendo $\mathbf{I}_{n}\mathbf{v}$ al posto di $\mathbf{v}$ possiamo riscrivere l'ultima equazione nella forma: $(\mathbf{A}-\lambda\mathbf{I}_{n})\mathbf{v}=\mathbf{0}$.
In questa equazione il vettore $\mathbf{v}$ (come lo scalare $\lambda$) è incognito: le componenti del vettore soddisfano perciò un sistema lineare omogeneo $n\times n$. Sappiamo che, perchè esistano vettori $\mathbf{v}$ (non nulli) che risolvono tale equazione, dovrà essere:

								$D(\lambda)=|\mathbf{A}-\lambda\mathbf{I}_{n}|=0$

*Per esempio*, 
per $n=2$, se $\mathbf{A}={\begin{pmatrix}a_{11}&a_{12}\\a_{21}&a_{22}\end{pmatrix}} \quad \rightarrow \quad {\begin{vmatrix}a_{11}-\lambda &a_{12} \\  a_{21}&a_{22}-\lambda \end{vmatrix}}=\lambda^2-(a_{11}+a_{22})\lambda+a_{11}a_{22}-a_{12}a_{21}=0$

L'ultima equazione è un'equazione algebrica in $\lambda$, di grado $n$, detta **equazione caratteristica della matrice** $\mathbf{A}$; il polinomio $D(\lambda)$ è detto **polinomio caratteristico della matrice** $\mathbf{A}$.
Questo polinomio dipende solo dalla trasformazione lineare, e non dal riferimento in cui questa è descritta; in altri termini, non varia se si sostituisce alla matrice $\mathbf{A}$ un'altra matrice ad essa equivalente. Infatti si può scrivere: $\mathbf{S}^{-1}\mathbf{A}\mathbf{S}-\lambda\mathbf{I}=\mathbf{S}^{-1}(\mathbf{A}-\lambda)\mathbf{S}$
e quindi, usando le proprietà del determinante:

					$|\mathbf{S}^{-1}\mathbf{A}\mathbf{S}-\lambda\mathbf{I}|=|\mathbf{S}^{-1}(\mathbf{A}-\lambda)\mathbf{S}|=\frac{1}{|\mathbf{S}|}\mathbf{A}-\lambda\mathbf{I}|\mathbf{S}|=\mathbf{D}(\lambda)$

È utile fissare il risultato appena ottenuto:

- #PROPOSIZIONE(10). Due matrici $n\times n$ simili hanno lo stesso polinomio caratteristico.


Una prima conseguenza di questa proprietà è la seguente. Si può osservare facilmente che nella scrittura esplicita del polinomio $\det({\mathbf{A}-\lambda\mathbf{I}})$, il termine contenente la potenza $\lambda^{n-1}$ è $(-\lambda)^{n-1}(a_{11}+a_{22}+\cdots+a_{nn})$.

La somma degli elementi sulla diagonale principale di una matrice quadrata è detta **traccia** della matrice:

$Tr(\mathbf{A})=a_{11}+a_{22}+\cdots+a_{nn}$

<mark class="hltr-yellow">Possiamo quindi affermare che due matrici simili hanno la stessa traccia, oltre che lo stesso determinante e la stessa caratteristica</mark>.

- #DEFINIZIONE(17). **Autovalori e autovettori**
	
	Chiameremo **autovalore** della matrice $\mathbf{A}$ (o della trasformazione che la matrice $\mathbf{A}$ rappresenta) qualsiasi numero $\lambda\in\mathbb{C}$ soddisfi l'equazione caratteristica; chiameremo **autovettore** (corrispondente all'autovalore $\lambda$) ogni vettore $\mathbf{v}\ne 0 \ (\mathbf{v}\in\mathbb{K}^n)$ che risolva l'equazione $\mathbf{A}\mathbf{v}=\lambda\mathbf{v}$.


Alcune **osservazioni** sono opportune.

Si noti innanzitutto che, poichè matrici simili hanno lo stesso polinomio caratteristico, avranno pure gli strssi autovalori: dunque essi dipendono solo dalla trasformazione lineare, e non dall particolare matrice rappresentativa (o base scelta).
Nella definizione di autovalore, anche se la matrice $\mathbf{A}$ è reale e la pensiamo come rappresentativa di una trasformazione di $\mathbb{R}^n$ in $\mathbb{R}^n$ , gli autovalori possono essere complessi.
In altre parole, i problemi della diagonalizzazione e della ricerca di autovalori e autovettori hanno la loro impostazione naturale nel campo complesso.

Notiamo che, mentre un autovettore corrisponde sempre ad un unico autovalore (perchè l'identità $\mathbf{A}\mathbf{v}=\lambda\mathbf{v}$ determina univocamente $\lambda$), ad un autovalore corrispondono sempre infiniti autovettori, in quanto se $\mathbf{A}\mathbf{v}=\lambda\mathbf{v}$, è anche $\mathbf{A}(c\mathbf{v})=\lambda(c\mathbf{v})$, come già osservato, e quindi tutti i vettori $c\mathbf{v}$ paralleli a $\mathbf{v}$ sono pure autovettori relativi a $\lambda$.
Se la matrice $\mathbf{A}$ è reale, il polinomio caratteristico è a coefficienti reali per cui gli autovalori sono reali oppure a coppie complessi coniugati. Gli autovettori possono essere scelti in modo che agli autovalori reali corrispondano autovettori reali e ad autovalori complessi coniugati corrispondano autovettori complessi coniugati.


*Esempio*: Trovare autovalori e autovettori della matrice $\mathbf{A}={\begin{pmatrix}0&1&1 \\  1&1&0 \\  1&0&1\end{pmatrix}}$

Calcoliamo: $\det(\mathbf{A}-\lambda\mathbf{I}_{3})={\begin{vmatrix}-\lambda&1&1 \\  1&1-\lambda&0 \\  1&0&1-\lambda\end{vmatrix}}= (\det 3^a riga)=(\lambda-1)+(a-\lambda)(-\lambda+\lambda^2-1)=(1-\lambda)(\lambda^2-\lambda-2)=(1-\lambda)(\lambda+1)(\lambda-2)$
Gli autovalori (valori di $\lambda$ che annullano il determinante di $\mathbf{A}-\lambda\mathbf{I}_{3}$) sono: $\lambda_{1}=1\quad\lambda_{2}=-1\quad\lambda_{3}=2$

Gli autovettori corrispondenti si trovano risolvendo il sistema omogeneo $(\mathbf{A}-\lambda\mathbf{I}_{3})\mathbf{x}=0$.

Se $\lambda=1$ tale sistema diventa:

${\begin{cases}-x+y+z=0 \\  x=0 \\  x=0\end{cases}}\quad$ ossia $\quad{\begin{cases}y+z=0 \\  x=0\end{cases}}$

e perciò abbiamo $\infty^1$ soluzioni date da ${\begin{cases}x=0 \\  y=-c \\  z=c\end{cases}}\quad$ (con $c$ parametro arbitrario).
Queste soluzioni rappresentano $\infty^1$ vettori, tutti paralleli tra di loro. Uno qualsiasi di essi si otterrà dando a $c$ un particolare valore, per esempio $c=1$. Il vettore ${\begin{pmatrix}0 \\  -1 \\  1\end{pmatrix}}$ è perciò un autovettore della matrice $\mathbf{A}$ corrispondente all'autovalore $1$.

Se $\lambda=-1$ il sistema diventa:

${\begin{cases}x+y+z=0 \\  x+2y=0 \\  x+2z=0\end{cases}}\quad$ cioè $\quad{\begin{cases}y=-\frac{x}{2} \\ z=-\frac{x}{2} \end{cases}}$

quindi le soluzioni sono del tipo ${\begin{cases}x=c \\  y=-\frac{c}{2} \\  z=-\frac{c}{2}\end{cases}}\quad$ e si hanno ancora $\infty^1$ autovettori paralleli tra loro; uno di essi è (per $c=2$): ${\begin{pmatrix}2 \\  -1 \\  -1\end{pmatrix}}$.

Se $\lambda=2$ il sistema diventa:

${\begin{cases}-2x+y+z=0 \\  x-y=0 \\  x-z=0\end{cases}}\quad$ ossia $\quad{\begin{cases}y=x \\ z=x \end{cases}}$

quindi le soluzioni sono del tipo ${\begin{cases}x=c \\  y=c \\  z=c\end{cases}}\quad$ e si hanno ancora $\infty^1$ autovettori paralleli tra loro; uno di essi è (per $c=1$): ${\begin{pmatrix}1 \\  1 \\  1\end{pmatrix}}$.


*Esempio*: Trovare autovalori e autovettori della matrice $\mathbf{A}={\begin{pmatrix}0&1 \\  -1&0\end{pmatrix}}$

Si ha: $\det(\mathbf{A}-\lambda\mathbf{I}_{2})={\begin{vmatrix}-\lambda&1 \\  -1&-\lambda\end{vmatrix}}=\lambda^2+1=0\longrightarrow\lambda=\pm i\quad$ (autovalori complessi coniugati)

Questo spinge a vedere $\mathbf{A}$ come trasformazione lineare di $\mathbb{C}^2$ in sè. Gli autovettori corrispondenti a $\lambda=i$ si trovano risolvendo il sistema:

$(\mathbf{A}-i\mathbf{I}_{2})\mathbf{x}=0\quad$ cioè $\quad{\begin{cases}-ix+y=0 \\  -x-iy=0\end{cases}}\quad$ ossia $\quad y=ix$

Si hanno dunque gli $\infty^1$ autovettori del tipo ${\begin{pmatrix}c \\  ic\end{pmatrix}}$, al variare di $c\in\mathbb{C}$;
in particolare, uno di essi è ${\begin{pmatrix}1 \\  i\end{pmatrix}}$.

Con calcoli analoghi si vede che gli autovettori relativi a $\lambda=-i$ sono del tipo ${\begin{pmatrix}c \\  -ic\end{pmatrix}}$, al variare di $c\in\mathbb{C}$;
in particolare, uno di essi è ${\begin{pmatrix}1 \\  -i\end{pmatrix}}$. In questo caso non esistono vettori $\mathbf{v}\in\mathbb{R}^2$ tali che $\mathbf{A}\mathbf{v}=\lambda\mathbf{v}$.



### 6.3 **Condizioni di diagonalizzabilità**

La relazione tra il problema della diagonalizzabilità di una matrice e quello della ricerca dei suoi autovalori e autovettori è espressa dal seguente:

- #TEOREMA(18). La matrice $\mathbf{A}$ è diagonalizzabile su $\mathbb{K}$ se e solo se $\mathbb{K}^n$ possiede una base di autovettori di $\mathbf{A}$. In tal caso, detti $\mathbf{h}_{1},\mathbf{h}_{2},\cdots,\mathbf{h}_{n}$ gli autovettori di tale base, e $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$ gli autovalori corrispondenti ($\lambda_{i}\in\mathbb{K}$, non necessariamente distinti), risulta:
	
								$\mathbf{A}=\mathbf{S}\mathbf{\Lambda}\mathbf{S}^{-1}$
	
	dove $\mathbf{\Lambda}=diag(\lambda_{1},\lambda_{2},\cdots,\lambda_{n})$ e $\mathbf{S}=(\mathbf{h}_{1}|\mathbf{h}_{2}|\cdots|\mathbf{h}_{n})$.
	
	*Dimostrazione*:
	
	Supponiamo che $\mathbf{A}$ sia diagonalizzabile su $\mathbb{K}$, ossia valga $\mathbf{A}=\mathbf{S}\mathbf{\Lambda}\mathbf{S}^{-1}$, con $\mathbf{S},\mathbf{\Lambda}$ matrici a elementi in $\mathbb{K}$, $\mathbf{S}$ non singolare e $\mathbf{\Lambda}$ diagonale. Perciò $\mathbf{A}\mathbf{S}=\mathbf{S}\mathbf{\Lambda}$.
	Chiamando $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$ gli elementi della diagonale di $\mathbf{\Lambda}$ e $\mathbf{h}_{1},\mathbf{h}_{2},\cdots,\mathbf{h}_{n}$ le colonne di $\mathbf{S}$m l'equazione $\mathbf{A}\mathbf{S}=\mathbf{S}\mathbf{\Lambda}$ si riscrive $\mathbf{A}\mathbf{h}_{i}=\lambda_{i}\mathbf{h}_{i} \ (i=1,2,\cdots,n)$. Questo prova che gli $\mathbf{h}_{i}$ sono autovettori e i $\lambda_{i}$ sono gli autovalori corrispondenti; poichè $\mathbf{S}$ è non singolare, i vettori $\mathbf{h}_{i}$ sono indipendenti, e quindi sono effettivamete una base di $\mathbb{K}^n$ di autovettori.
	Viceversa, supponiamo ora che esista una base di $\mathbb{K}^n$ di autovettori di $\mathbf{A}$, $\mathbf{h}_{1},\mathbf{h}_{2},\cdots,\mathbf{h}_{n}$, e siano $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$ gli autovalori corrispondenti. Definendo le matrici $\mathbf{\Lambda}=diag(\lambda_{1},\lambda_{2},\cdots,\lambda_{n})$ e $\mathbf{S}=(\mathbf{h}_{1}|\mathbf{h}_{2}|\cdots|\mathbf{h}_{n})$, le relazioni $\mathbf{A}\mathbf{h}_{i}=\lambda_{i}\mathbf{h}_{i} \ (i=1,2,\cdots,n)$ si riscrivono $\mathbf{A}\mathbf{S}=\mathbf{S}\mathbf{\Lambda}$, cioè $\mathbf{A}=\mathbf{S}\mathbf{\Lambda}\mathbf{S}^{-1}$ (l'invertibilità di $\mathbf{S}$ segue dall'ipotesi di indipendenza dei vettori $\mathbf{h}$), perciò $\mathbf{A}$ è diagonalizzabile.
	
	Si noti in particolare che una condizione necessaria (ma non sufficiente) affinchè una matrice reale sia diagonalizzabile su $\mathbb{R}$ è che i suoi autovalori siano reali.


*Esempio*: Studiamo la diagonalizzabilità o meno della matrice $\mathbf{A}={\begin{pmatrix}1&1 \\  0&2\end{pmatrix}}$
Per quanto visto, i passi da seguire sono i seguenti:

1) Determiniamo gli autovalori risolvendo l'equazione caratteristica:
	
	${\begin{vmatrix}1-\lambda &1 \\  0 & 2-\lambda\end{vmatrix}}=(1-\lambda)(2-\lambda)=0 \ \rightarrow \ \lambda=1,\lambda=2$

2) Determiniamo gli autovettori relativi agli autovalori trovati. Ciò significa risolvere, per ciascun autovalore, il sistema omogeneo:
	
	${\begin{pmatrix}1-\lambda &1 \\  0&2-\lambda \end{pmatrix}}{\begin{pmatrix}x \\  y\end{pmatrix}}=0$
	
	Per $\lambda=1$: $\quad{\begin{cases}y=0 \\  y=0\end{cases}}\quad$ perciò gli autovettori sono $(x,0)$; uno di essi è $(1,0)$.
	Per $\lambda=2$: $\quad{\begin{cases}-x+y=0 \\  0=0\end{cases}}\quad$ perciò gli autovalori sono $(x,x)$; uno di essi è $(1,1)$.

3) Osserviamo ora che i due autovettori $(1,0),(1,1)$ sono indipendenti, perciò formano una base di $\mathbb{R}^2$. Pertanto $\mathbf{A}$ è diagonalizzabile, con:
	
	$\mathbf{\Lambda}={\begin{pmatrix}1&0 \\  0&2\end{pmatrix}},\quad\mathbf{S}={\begin{pmatrix}1&1 \\  0&1\end{pmatrix}}$
	
	calcolando anche $\mathbf{S}^{-1}={\begin{pmatrix}1&-1 \\  0&1\end{pmatrix}}$ si può scrivere la relazione $\mathbf{A}=\mathbf{S}\mathbf{\Lambda}\mathbf{S}^{-1}$:
	
	${\begin{pmatrix}1&1 \\  0&2\end{pmatrix}}={\begin{pmatrix}1&1 \\  0&1\end{pmatrix}}{\begin{pmatrix}1&0 \\  0&2\end{pmatrix}}{\begin{pmatrix}1&-1 \\  0&1\end{pmatrix}}$

Abbiamo così diagonalizzato la matrice $\mathbf{A}$.


L'ipotesi del Teorema precedente non è sempre di verifica agevole, specialmente se le dimensioni della matrice non sono piccole. Vediamo quindi di comprendere più in dettaglio quali sono le situazioni in cui una matrice è o non è diagonalizzabile. Diamo anzitutto qualche definizione:

- #DEFINIZIONE(18). **Molteplicità algebrica**
	
	Si dice che un autovalore $\lambda_{0}$ ha **molteplicità algebrica** $m$ se $\lambda_{0}$ è una radice del polinomio caratteristico $D(\lambda)$ di molteplicità $m$, cioè se $D(\lambda)$ è divisibile per $(\lambda-\lambda_{0})^m$ ma non per $(\lambda-\lambda_{0})^{m+1}$.
	
	Siano $\lambda_{1},\lambda_{2},\cdots,\lambda_{k} \ (k\le n)$ gli autovalori distinti di $\mathbf{A}$ (reali o complessi), di molteplicità $m_{1},m_{2},\cdots,m_{k}$, rispettivamente. Per il Teorema Fondamentale dell'Algebra, $\sum_{i=1}^k m_{i}=n$.
	L'insieme degli autovettori corrispondenti all'autovalore $\lambda_{j}$ non è altro che il nucleo della trasformazione $\mathbf{A}-\lambda_{j}\mathbf{I}$. Più precisamente, poichè per definizione gli autovettori devono essere non nulli, diciamo che l'insieme degli autovettori corrispondenti all'autovalore $\lambda_{j}$, con l'aggiunta del vettore $\mathbf{0}$, coincide con il nucleo della trasformazione $\mathbf{A}-\lambda_{j}\mathbf{I}$.

- #DEFINIZIONE(19). **Autospazio, molteplicità geometrica**
	
	Lo spazio vettoriale $Ker(\mathbf{A}-\lambda_{j}\mathbf{I})$ viene detto **autospazio** associato all'autovalore $\lambda_{j}$ e la sua dimensione $d_{j}$ è detta **molteplicità geometrica** dell'autovalore $\lambda_{j}$.


Valgono inoltre i seguenti fatti:

- #TEOREMA(19).
	
	a) Autovettori relativi ad autovalori distinti sono linearmente indipendenti;
	b) La molteplicità geometrica di un autovalore non supera la sua molteplicità algebrica: $d_{j}\le m_{j}$.


- #DEFINIZIONE(20). Un autovalore $\lambda_{j}$ si dice **regolare** se $d_{j}= m_{j}$.

Se un autovalore è **semplice**, cioè ha molteplicità algebrica $1$, anche $d_{j}$ dovrà essere uguale a $1$, perciò <mark class="hltr-yellow">un autovalore semplice è sempre regolare</mark>. La distinzione tra autovalori regolari o meno ha quindi senso per gli autovalori di molteplicità algebrica $>1$.
Arriviamo così al seguente:

- #TEOREMA(20). La matrice $\mathbf{A}$ a elementi in $\mathbb{K}$ è diagonalizzabile su $\mathbb{K}$ se e solo se i suoi autovalori sono tutti regolari. (Se $\mathbb{K}=\mathbb{R}$: "se e solo se i suoi autovalori sono tutti reali e regolari").
	
	*Dimostrazione*:
	
	Infatti, se la matrice è diagonalizzabile, $\mathbb{K}^n$ ha una base di autovettori di $\mathbf{A}$. Ora, se $\lambda_{1},\lambda_{2},\cdots,\lambda_{k}$ sono gli autovalori distinti di $\mathbf{A}$ (se $\mathbb{K}=\mathbb{R}$ reali perchè $\mathbf{A}$ è diagonalizzabile), ciascun autospazio fornisce $d_{j}$ autovettori indipendenti tra loro (per definizione di molteplicità geometrica), e indipendenti da quelli degli altri autospazi (per il Teorema precedente, punto (a)). Il numero totale di autovettori indipendenti è quindi:
	
									$\sum_{j=1}^k d_{j}$
	
	D'altro canto $d_{j}<m_{j}$ e $\sum_{j=1}^k m_{j}=n$; perciò l'unica possibilità per avere $n$ autovettori reali e indipendenti è che sia $d_{j}=m_{j} \quad \forall j$, quindi gli autovalori sono regolari.
	Viceversa, supponiamo ora che gli autovalori $\lambda_{1},\lambda_{2},\cdots,\lambda_{k}$ siano tutti regolari, quindi ogni autospazio fornisce $m_{j}$ autovettori indipendenti tra loro (e indipendenti da quelli degli altri autospazi). In conclusione, il numero totale di autovettori indipendenti è $\sum_{j=1}^k m_{j}=n$, dunque $\mathbb{K}^n$ ha una base di autovettori di $\mathbf{A}$.

Dal Teorema precedente segue in particolare che se una matrice reale ha tutti gli autovalori reali e semplici, è diagonalizzabile su $\mathbb{R}$; se ha tutti gli autovalori semplici (ma non tutti reali) è diagonalizzabile su $\mathbb{C}$. Infatti gli autovalori semplici sono automaticamente regolari.


*Esempio* (1): Sia $\mathbf{A}={\begin{pmatrix}0&1 \\  -1&0\end{pmatrix}}$ e chiediamoci se la matrice è diagonalizzabile.
	L'equazione caratteristica è: $\lambda^2+1=0,\lambda=\pm i$quindi non esistono autovalori reali. Pertanto $\mathbf{A}$ non è diagonalizzabile su $\mathbb{R}$. D'altro canto gli autovalori, in $\mathbb{C}$, sono semplici, quindi la matrice è diagonalizzabile su $\mathbb{C}$.

*Esempio* (2): Sia $\mathbf{A}={\begin{pmatrix}1&1 \\  0&1\end{pmatrix}}$
	Equazione caratteristica: $(\lambda-1)^2=0\rightarrow\lambda=1$ autovalore doppio.
	Cercando gli autovettori si trova ${\begin{pmatrix}x \\  0\end{pmatrix}}$ pertanto l'autospazio relativo a $\lambda=1$ ha $\dim=1$, l'autovalore non è regolare, e la matrice non è diagonalizzabile.

*Esempio* (3): Sia $\mathbf{A}={\begin{pmatrix}2&0&3 \\  0&2&1 \\  0&0&1\end{pmatrix}}$
	Equazione caratteristica: $(2-\lambda)^2(1-\lambda)=0$, perciò $\lambda=1$ autovalore semplice (quindi regolare), $\lambda=2$ autovalore doppio. L'autospazio relativo a $\lambda=2$ si determina risolvendo il sistema:
	
	${\begin{pmatrix}0&0&3 \\  0&0&1 \\  0&0&-1\end{pmatrix}}{\begin{pmatrix}x \\  y \\  z\end{pmatrix}}=0$
	che dà $z=0$; perciò l'autospazio consiste dei vettori $(x,y,0)$, e ha quindi $\dim=2$.
	$\lambda=2$ è regolare, e la matrice è diagonalizzabile.
	Per diagonalizzarla effettivamente, occorre calcolare anche un autovettore relativo a $\lambda=1$. Si trova, per esempio, $(-3,0,1)$. Quindi si può porre $\mathbf{A}=\mathbf{S}\mathbf{\Lambda}\mathbf{S}^{-1}$ con:
	
	$\mathbf{\Lambda}=\begin{pmatrix}1&0&0\\0&2&0\\0&0&2\end{pmatrix},\quad\mathbf{S}=\begin{pmatrix}-3&1&0\\0&0&1\\1&0&0\end{pmatrix},\quad\mathbf{S}^{-1}=\begin{pmatrix}0&0&1\\1&0&3\\0&1&0\end{pmatrix}$
	Si noti che le ultime due colonne della matrice $\mathbf{S}$ sono una base dell'autospazio relativo all'autovalore $\lambda=2$.


- **Osservazione**: Nel caso di autovalori non regolari non è possibile trovare una matrice equivalente a quella data, che sia diagonale. È tuttavia possibile ridurre la matrice ad una forma "canonica" più semplice, detta **forma di Jordan**.


#### 6.3.1 **Matrici reali simmetriche. Matrici ortogonali**

Una classe particolare di matrici reali che, come vedremo, risultano <mark class="hltr-yellow">sempre diagonalizzabili</mark>, è quella delle **matrici simmetriche**. Per discutere questo risultato dobbiamo prima introdurre un'altra classe di matrici che giocano un ruolo importante, quello delle **matrici ortogonali**.

- #DEFINIZIONE(21). Una matrice $\mathbf{A}$ reale di tipo $(n,n)$ si dice **ortogonale** se:
	
							$\mathbf{A}\cdot\mathbf{A}^\top=\mathbf{A}^\top\cdot\mathbf{A}=\mathbf{I}$
	
	ossia se $\mathbf{A}$ è una matrice non singolare la cui inversa coincide con la trasposta.

[[#4.1 **L'algebra delle matrici**|Ricordiamo]] che la trasposta $\mathbf{A}^\top$ di una matrice $\mathbf{A}$ è quella che si ottiene scambiando le righe con le colonne. Perciò se $\mathbf{A}=(a_{ij})$, $\mathbf{A}^\top=(a_{ji})$.
Inoltre, se $\mathbf{A},\mathbf{B}$ sono due matrici $(n,n)$, vale la proprietà $(\mathbf{A}\mathbf{B})^\top=\mathbf{B}^\top\mathbf{A}^\top$.


- #TEOREMA (21). **Proprietà delle matrici ortogonali**
	
	a. $\mathbf{A}$ è una matrice ortogonale di tipo $(n,n)$ se e solo se le sue righe sono una base ortonormale di $\mathbb{R}^n$; lo stesso vale per le colonne.
	b. Il determinante di una matrice ortogonale vale $1$ o $-1$.
	c. Il prodotto di due matrici ortogonali è ortogonale.
	d. La trasformazione lineare rappresentata da una matrice ortogonale conserva il modulo dei vettori: $|\mathbf{A}\mathbf{x}|=|\mathbf{x}|\quad\mathbf{x}\in\mathbb{R}^n$, e conserva il loro prodotto scalare: $\mathbf{A}\mathbf{x}\cdot\mathbf{A}\mathbf{y}=\mathbf{x}\cdot\mathbf{y}$.
	
	*Dimostrazioni*:
	
	a. Poniamo $\mathbf{A}={\begin{pmatrix}\mathbf{a}_{1} \\  \mathbf{a}_{2} \\  \cdots \\  \mathbf{a}_{n}\end{pmatrix}}$; la relazione $\mathbf{A}\cdot\mathbf{A}^\top=\mathbf{I}_{n}$ dà, ragionando sugli elementi:
	
	$\sum_{k=1}^n a_{ik}a_{jk}={\begin{cases}1 & \mbox{se }i=j\\  0& \mbox{se }i\ne j\end{cases}}\quad$ ossia $\quad\mathbf{a}_{i}\cdot\mathbf{a}_{j}={\begin{cases}1 & \mbox{se }i=j\\  0& \mbox{se }i\ne j\end{cases}}$
	
	il che significa che i vettori riga di $\mathbf{A}$ sono ortonormali (e quindi sono una base, essendo in numero $n$).
	Analogamente, ponendo $\mathbf{A}=(\mathbf{a}_{1}'|\mathbf{a}_{2}'|\cdots|a_{n}')$ la relazione $\mathbf{A}^\top\cdot\mathbf{A}=\mathbf{I}_{n}$ dà:
	
	$\mathbf{a}_{i}'\cdot\mathbf{a}_{j}'=\sum_{k=1}^n a_{ki}a_{kj}={\begin{cases}1 & \mbox{se }i=j\\  0& \mbox{se }i\ne j\end{cases}}\quad$
	
	e quindi anche le colonne di $\mathbf{A}$ sono ortonormali.
	Ripercorrendo i passaggi all'inverso si vede che se, viceversa, le righe (rispettivamente, le colonne) di $\mathbf{A}$ sono una base ortonormale di $\mathbb{R}^n$, allora $\mathbf{A}\cdot\mathbf{A}^\top=\mathbf{I}_{n}$ (rispettivamente, $\mathbf{A}^\top\cdot\mathbf{A}=\mathbf{I}_{n}$).
	
	
	b. Dalla relazione $\mathbf{A}^\top\cdot\mathbf{A}=\mathbf{I}_{n}$, per il [[#4.3 **Determinante**|Teorema di Binet]] si ha $\det(\mathbf{A}^\top)\cdot\det(\mathbf{A})=1$.
	Ricordando che $\det(\mathbf{A}^\top)=\det(\mathbf{A})\iff\det^2(\mathbf{A})=1,\det(\mathbf{A})=\pm 1$.
	
	
	c. Siano $\mathbf{A},\mathbf{B}$ ortogonali. Allora:
		
			$(\mathbf{A}\mathbf{B})\cdot(\mathbf{A}\mathbf{B})^\top=(\mathbf{A}\mathbf{B})\cdot(\mathbf{B}^\top\mathbf{A}^\top)=\mathbf{A}(\mathbf{B}\mathbf{B}^\top)\mathbf{A}^\top=\mathbf{A}\mathbf{I}_{n}\mathbf{A}^\top=\mathbf{A}\mathbf{A}^\top=\mathbf{I}_{n}$
	
	Analogamente si prova che $(\mathbf{A}\mathbf{B})^\top\cdot(\mathbf{A}\mathbf{B})=\mathbf{I}_{n}$, perciò $\mathbf{A}\mathbf{B}$ è ortogonale.
	
	
	d. Con le notazioni del prodotto righe per colonne, il prodotto scalare $\mathbf{x}\cdot\mathbf{y}$ è $\mathbf{x}^\top\mathbf{y}$, quello dei trasformati è $\quad(\mathbf{A}\mathbf{x})^\top\cdot(\mathbf{A}\mathbf{y})=\mathbf{x}^\top\mathbf{A}^\top\mathbf{A}\mathbf{y}=\mathbf{x}^\top\mathbf{I}_{n}\mathbf{y}=\mathbf{x}^\top\mathbf{y}$
	quindi il prodotto scalare si conserva; in particolare allora si conserva il modulo dei vettori:
		
						$|\mathbf{A}\mathbf{x}|^2=(\mathbf{A}\mathbf{x})^\top(\mathbf{A}\mathbf{x})=\mathbf{x}^\top\mathbf{x}=|\mathbf{x}|^2$


Se $n=2,3$ la conservazione del prodotto scalare ha il significato geometrico di conservazione degli angoli e delle lunghezze. Geometricamente, le trasformazioni lineari che conservano gli angoli e lunghezze sono le rotazioni rispetto all'origine, eventualmente accompagnate da una riflessione (rispetto ad una retta, nel piano; rispetto a un piano, nello spazio), ad eccezione delle traslazioni in quanto non sono trasformazioni lineari.
Precisamente, si osserva che le trasformazioni lineari che rappresentano una rotazione rispetto all'origine senza alcuna riflessione sono rappresentate da matrici ortogonali aventi $\det=1$; queste matrici si chiamano ortogonali speciali, o comunemente **matrici di rotazione**.
Invece, le trasformazioni lineari che rappresentano una rotazione rispetto all'origine accompagnata da una riflessione sono rappresentate da matrici ortogonali aventi $\det=-1$.

Si noti che in base al punto (a) del Teorema precedente, scambiando tra loto due colonne/righe di una matrice ortogonale $n\times n$ si ottiene una matrice ancora ortogonale, che però avrà determinante di segno opposto. In particolare, data una matrice ortogonale con $\det=-1$, è sufficiente scambiare tra loro due righe/colonne per ottenere una matrice di rotazione.
Quest'ultimo fatto ci sarà utile nelle applicazioni geometriche della diagonalizzazione, che vedremo nel prossimo capitolo.

Possiamo ora enunciare l'importante:

- #TEOREMA(22). Sia $\mathbf{A}$ una matrice reale e simmetrica. Allora $\mathbf{A}$ è diagonalizzabile, con una matrice di passaggio ortogonale, ossia:
		
								$\mathbf{A}=\mathbf{M}\mathbf{\Delta}\mathbf{M}^\top$
	
	con $\mathbf{\Delta}$ diagonale e $\mathbf{M}$ ortogonale. In particolare, ciò significa che $\mathbb{R}^n$ possiede una base ortonormale di autovettori di $\mathbf{A}$.


Ricordiamo esplicitamente come si costruiscono le matrici $\mathbf{M}$ e $\mathbf{\Delta}$:

1. Si calcolano gli autovalori di $\mathbf{A}$, $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$ e $n$ autovettori corrispondenti; questi risultano a due a due ortogonali;
2. Si normalizzano gli $n$ autovettori, ottenendo $\mathbf{h}_{1},\cdots,\mathbf{h}_{n}$ vettori colonna ortonormali;
3. Si ha allora $\mathbf{M}=(\mathbf{h}_{1}|\mathbf{h}_{2}|\cdots|\mathbf{h}_{n})$ e $\mathbf{\Delta}=diag(\lambda_{1},\lambda_{2},\cdots,\lambda_{n})$.
4. Nel caso risultasse $\det\mathbf{M}=-1$, per ottenere una matrice $\mathbf{M}$ di rotazione è sufficiente scambiare tra loro (ad esempio) i primi due autovettori e i primi due autovalori, ossia porre: $\mathbf{M}=(\mathbf{h}_{2}|\mathbf{h}_{1}|\cdots|\mathbf{h}_{n})$ e $\mathbf{\Delta}=diag(\lambda_{2},\lambda_{1},\cdots,\lambda_{n})$.


*Esempio* (1): Dimostriamo il Teorema per $n=2$. La generica matrice di tipo $(2,2)$ è: $\mathbf{A}={\begin{pmatrix}a&b \\  c&d\end{pmatrix}}$
	I suoi autovalori sono dati da ${\begin{vmatrix}a-\lambda &b \\  b&c-\lambda\end{vmatrix}}=\lambda^2-(a+c)\lambda+ac-b^2=0$
	
	$\lambda=\frac{(a+c)\pm\sqrt{(a+c)^2-4(ac-b^2)}}{2}=\frac{(a+c)\pm\sqrt{(a-c)^2}+4b^2}{2}$
	Come si vede, il discriminante è sempre $\ge0$, il che implica autovalori reali. In particolare, il discriminante si annulla se e solo se $a=c$ e $b=0$
	ossia se e solo se $\mathbf{A}$ è già una matrice diagonale. Altrimenti si hanno $2$ autovalori reali e distinti, quindi semplici, quindi regolari, e perciò la matrice è diagonalizzabile.
	Mostriamo che è possibile diagonalizzarla con una matrice ortogonale.
	Siano $\lambda_1,\lambda_2$ i due autovalori, e $\mathbf{v}_1,\mathbf{v}_2$ due autovettori corrispondenti, rispettivamente. Mostriamo che $\mathbf{v}_1$ e $\mathbf{v}_2$ sono ortogonali. Infatti:
	$\mathbf{v}_1\cdot(\mathbf{A}\mathbf{v}_2)=\lambda_2\mathbf{v}_1\cdot\mathbf{v}_2$ e $\mathbf{v}_2\cdot(\mathbf{A}\mathbf{v}_1)=\lambda_1\mathbf{v}_1\cdot\mathbf{v}_2$
	D'altro canto la simmetria della matrice $\mathbf{A}$ implica che $\mathbf{v}_1\cdot(\mathbf{A}\mathbf{v}_2)=\mathbf{v}_2\cdot(\mathbf{A}\mathbf{v}_1)$, infatti:
	$\mathbf{v}_1\cdot(\mathbf{A}\mathbf{v}_2)=\sum_{i=1}^2 v_1^i \sum_{j=1}^2 a_{ji}v_2^j=\sum_{j=1}^2 v_2^j \sum_{i=1}^2 a_{ji}v_1^i=\mathbf{v}_2\cdot(\mathbf{A}\mathbf{v}_1)$
	Ne segue che $\lambda_1\mathbf{v}_1\cdot\mathbf{v}_2=\lambda_2\mathbf{v}_1\cdot\mathbf{v}_2$, ed essendo $\lambda_1\ne\lambda_2$ dev'essere $\mathbf{v}_1\cdot\mathbf{v}_2=0$.
	Basta ora normalizzare i due autovettori per averne due ortonormali; la matrice che ha questi come colonne è quindi una matrice ortogonale, che diagonalizza $\mathbf{A}$.


*Esempio* (2): Diagonalizziamo la matrice $\mathbf{A}={\begin{pmatrix}1&1 \\  1&1\end{pmatrix}}$
	Gli autovalori sono dati da $\lambda^2-2\lambda=0$, cioè $\lambda=0,\lambda=2$.
	Gli autovettori relativi a $\lambda=0$ sono dati da $x+y=0$, cioè sono del tipo $(x,-x)$, per esempio $(1,-1)$.
	Gli autovettori relativi a $\lambda=2$ sono dati da $-x+y=0$, per esempio $(1,1)$.
	Possiamo quindi scrivere: $\mathbf{A}={\begin{pmatrix}1&1 \\  -1&1\end{pmatrix}}{\begin{pmatrix}0&0 \\  0&2\end{pmatrix}}{\begin{pmatrix}1&1 \\  -1&1\end{pmatrix}}^{-1}$
	Si noti che i due autovettori scelti sono ortogonali ma non sono normalizzati, quindi la matrice $\mathbf{S}$ qui utilizzata non è ortogonale.
	Normalizzando gli autovettori, otteniamo una matrice di passaggio ortogonale:
	$\mathbf{S}={\begin{pmatrix}\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}} \\  -\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\end{pmatrix}}$
	che in questo caso rappresenta una rotazione di $-\frac{\pi}{4}$ nel piano.
	La sua inversa è la matrice trasposta, perciò possiamo scrivere:
	$\mathbf{A}={\begin{pmatrix}\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}} \\  -\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\end{pmatrix}}{\begin{pmatrix}0&0 \\  0&2\end{pmatrix}}{\begin{pmatrix}\frac{1}{\sqrt{2}}&-\frac{1}{\sqrt{2}} \\  \frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\end{pmatrix}}$


#### 6.3.2 **Rotazioni dello spazio**

Abbiamo visto che una matrice ortogonale $(2,2)$ o $(3,3)$ rappresenta geometricamente una rotazione nel piano o nello spazio, eventualmente accompagnata da una riflessione.
Soffermiamoci ora sul caso tridimensionale; dal punto di vista geometrico una rotazione nello spazio (senza riflessione) è determinata da un asse di rotazione, e da un angolo di rotazione attorno a tale asse. Possiamo individuare una rotazione con un vettore $\alpha\mathbf{n}$, dove $\mathbf{n}$ è un versore che individua l'asse di rotazione e $\alpha$ l'angolo di rotazione antioraria rispetto all'asse orientato come $\mathbf{n}$. Quindi una rotazione è individuata da $3$ parametri indipendenti.
Dal punto di vista algebrico una rotazione è individuata da una matrice $(3,3)$ ortogonale. [[#6.3.1 **Matrici reali simmetriche. Matrici ortogonali**|Le condizioni di ortogonalità]] implicano $6$ relazioni indipendenti tra i $9$ coefficienti della matrice, e quindi i parametri indipendenti che individuano la matrice sono $3$.
Chiediamoci come si legge, dalla matrice, l'informazione geometrica su quale sia l'asse e l'angolo di rotazione. A questo risponde il prossimo:

- #TEOREMA (23). **Teorema di Eulero**
	
	Una matrice $\mathbf{M}$ ortogonale $(3,3)$ avente $\det=1$ ha sempre un autovalore uguale ad $1$ con un autovettore reale, e due autovalori complessi coniugati di modulo unitario, $e^{i\alpha},e^{-i\alpha}$, per qualche $\alpha$.
	Il versore $\mathbf{n}$ dell'autovettore reale indica l'asse di rotazione, mentre il numero $\alpha$ indica l'angolo. l'angolo $\alpha$ si può anche calcolare direttamente dalla relazione:
		
							$Tr \mathbf{M}=1+2\cos\alpha$
	
	dove $Tr\mathbf{M}$ (traccia di $\mathbf{M}$) indica la somma degli elementi di $\mathbf{M}$ posti sulla diagonale principale.


*Esempio*: Le rotazioni di angolo $\alpha$ attorno agli assi $x,y,z$ sono date rispettivamente dalle matrici:

$\mathbf{R}_{x}(\alpha)={\begin{pmatrix}1&0&0 \\  0&\cos\alpha&\sin\alpha \\  0&-\sin\alpha&\cos\alpha\end{pmatrix}}\quad\mathbf{R}_{y}(\alpha)={\begin{pmatrix}\cos\alpha&0&\sin\alpha \\  0&1&0 \\  -\sin\alpha&0&\cos\alpha\end{pmatrix}}\quad\mathbf{R}_{z}(\alpha)={\begin{pmatrix}\cos\alpha&\sin\alpha&0 \\  -\sin\alpha&\cos\alpha&0 \\  0&0&1\end{pmatrix}}$




# **Capitolo VII: Coniche**


Nei capitoli precedenti abbiamo introdotto alcuni concetti e strumenti fondamentali dell'algebra lineare e abbiamo sviluppato i primi elementi della geometria analitica dello spazio limitandoci alla geometria degli enti lineari (rette e piani). Naturalmente, molti degli aspetti più interessanti e utili della geometria riguardano gli oggetti geometrici curvi: linee del piano e superfici nello spazio.
Dal punto di vista algebrico, i più semplici oggetti geometrici curvi che è naturale considerare sono quelli descritti da equazioni algebriche di secondo grado in due variabili (che rappresenteranno particolari curve nel piano) o in tre variabili (che rappresenteranno superfici nello spazio): queste curve e superfici prendono il nome di **coniche** e **quadriche**, rispettivamente.
Come vedremo, nello studio delle proprietà di questi oggetti, l'algebra lineare studiata in precedenza risulta essere uno strumento molto potente.

Le coniche sono, dopo la circonferenza, le prime curve piane che storicamente sono state studiate: nella matematica greca erano studiate coi metodi della geometria euclidea, del piano e dello spazio. Noi discuteremo brevemente le coniche dal punto di vista della geometria elementare, per poi concentrarci sul punto di vista della geometria analitica.


### 7.1 **Le coniche dal punto di vista elementare e le loro equazioni canoniche**


#### 7.1.1 **Le coniche come sezioni di un cono**

Un primo modo per definire le coniche utilizza il punto di vista della geometria elementare dello spazio. Consideriamo anzitutto un **cono a due falde**, ovvero la superficie, nello spazio, così definita: si considera una retta $a$, detta asse del cono (che pensiamo verticale), e un punto $V$ su $a$, detto vertice del cono; su un piano orizzontale e non passante per $V$ si considera una circonferenza avente il centro su $a$; il cono a due falde è la superficie formata da tutte le rette (dette generatrici del cono) che passano per $V$ e per un punto qualsiasi della circonferenza.



Si dice **sezione conica** (o semplicemente **conica**) qualsiasi curva si ottenga intersecando un cono a due falde con un piano qualsiasi dello spazio, non passante per il vertice $V$.
Precisamente:

- Se il piano è meno inclinato delle generatrici (rispetto all'orizzontale), allora interseca una sola delle due falde del cono, e taglia su di esse una curva (limitata) detta **ellisse**. Se il piano è orizzontale, l'ellisse è una **circonferenza**.
- Se il piano è parallelo ad una generatrice, interseca una sola delle due falde del cono, e taglia su di esse una curva (illimitata) detta **parabola**.
- Se il piano è più inclinato delle generatrici, interseca entrambe le falde del cono, e taglia su di esse una curva, illimitata e spezzata in due rami, detta **iperbole**.



#### 7.1.2 **Le coniche come luoghi geometrici piani e le loro equazioni canoniche**

Senza fare uso di costruzioni tridimensionali, le coniche possono anche essere definite direttamente come opportuni luoghi geometrici, nel piano, nei modi seguenti.

- #DEFINIZIONE(22). **Ellisse**
	
	Siano $F_{1},F_{2}$ due punti nel piano, eventualmente coincidenti, e $d$ un numero reale maggiore della distanza $\overline{F_{1}F_{2}}$. Si chiama **ellisse** di **fuochi** $F_{1},F_{2}$ l'insieme dei punti $P$ del piano tali che $\overline{PF_{1}}+\overline{PF_{2}}=d$, ossia tali che la somma delle loro distanze dai $2$ fuochi è costante.



Se in particolare $F_{1}\equiv F_{2}$, l'ellisse è la circonferenza di diametro $d$ e centro $F_{1}$.
Scegliamo un sistema di riferimento cartesiano in cui sia $F_{1}\equiv(c,0);F_{2}\equiv(-c,0)$, per un certo $c>0$. Se $P\equiv(x,y)$, imponendo la relazione $\overline{PF_{1}}+\overline{PF_{2}}=d$ (con $2c<d$) si ottiene un'equazione del tipo:
	
								$\frac{x^2}{a^2}+\frac{y^2}{b^2}=1\quad$

con $a,b>0$ e $a>b$, detta <u>equazione canonica dell'ellisse</u>.
I numeri $a,b$ sono detti **semiassi** dell'ellisse e sono legati ai fuochi dalla relazione $c=\sqrt{b^2-a^2}$, mentre $d=2a$.
Una curva avente tale equazione ma con $b>a$ rappresenta invece un'ellisse avente i fuochi sull'asse $y$:

$F_{1}\equiv(0,c);F_{2}\equiv(0;-c),\quad$ con $c=\sqrt{b^2-a^2},d=2b$

I fuochi dell'ellisse stanno quindi sempre sull'asse maggiore. I punti $(\pm a,0),(0,\pm b)$ si dicono **vertici** dell'ellisse. Se $a=b$ l'ellisse è la <u>circonferenza</u> di centro $0$ (origine) e raggio $R=a=b$.



- #DEFINIZIONE(23). **Parabola**
	
	Sia $F$ un punto del piano e $r$ una retta non passante per $F$. Si dice **parabola** di **fuoco** $F$ e direttrice $r$ il luogo dei punti equidistanti da $F$ e $r$.
	In altre parole: per ogni punto $P$ della parabola, detta $H$ la sua proiezione su $r$, risulta $\overline{PH}=\overline{PF}$.



Se scegliamo un riferimento in cui il fuoco della parabola è $F\equiv(a,0)$ e la direttrice è la retta: $x=-a$, uguagliando le distanze di $P(x,y)$ dal fuoco e dalla direttrice si ottiene l'equazione:
	
								$y^2=4ax$

detta <u>equazione canonica della parabola</u>.
L'equazione:
	
								$x^2=4ay$

rappresenta invece la parabola di fuoco $F\equiv(0,a)$ e direttrice la retta: $y=-a$.



- #DEFINIZIONE(24). **Iperbole**
	
	Siano $F_{1},F_{2}$ due punti nel piano e $d$ un numero reale positivo minore della distanza $\overline{F_{1}F_{2}}$. Si chiama **iperbole** di **fuochi** $F_{1},F_{2}$ il luogo dei punti $P$ del piano tali che $|\overline{PF_{1}}-\overline{PF_{2}}|=d$, ossia tali che il modulo della differenza delle loro distanze dai due fuochi sia costante.
	La relazione precedente equivale a $\overline{PF_{1}}-\overline{PF_{2}}=\pm d$; ciascuna delle due equazioni (con il segno $+$ o $-$) individua uno dei due **rami dell'iperbole**.



Se scegliamo un riferimento in cui i fuochi sono i punti $F_{1}\equiv(c,0);F_{2}\equiv(-c,0)$ per un certo $c>0$ imponendo la relazione $|\overline{PF_{1}}-\overline{PF_{2}}|=d$ (con $2c>d$) si ottiene un'equazione del tipo:
	
								$\frac{x^2}{a^2}-\frac{y^2}{b^2}=1$

detta <u>equazione canonica dell'iperbole</u>, dove i coefficienti $a,b$ sono legati ai fuochi dalla relazione $c=\sqrt{a^2+b^2}$.
I punti $(\pm a,0)$ sono detti **vertici** dell'iperbole, le rette $y=\pm\frac{b}{a}x$ sono dette **asintoti** dell'iperbole.
L'analoga equazione:
	
								$\frac{x^2}{a^2}-\frac{y^2}{b^2}=-1$

con $a,b>0$ rappresenta un'iperbole avente fuochi sull'asse $y$, $F_{1}\equiv(0,c),F_{2}\equiv(0,-c)$, vertici $(0,\pm b)$ e gli stessi asintoti.
Se in particolare $a=b$, l'iperbole si dice **equilatera**: in questo gli asintoti sono le rette $y=\pm x$, ortogonali tra loro.


Concludiamo questa prima panoramica sulle coniche ricordando che si può dimostrare che una curva è un'ellisse/parabola/iperbole rispetto alla prima definizione (ossia come opportuna sezione di un cono) se e solo se lo è rispetto alla seconda definizione (ossia come luogo geometrico definito mediante opportune distanze).
<mark class="hltr-yellow">Le due definizioni date sono dunque equivalenti</mark>.






### 7.2 **L'equazione generale delle coniche. Riduzione a forma canonica**

La forma canonica delle coniche è quella che l'equazione di una curva di questo tipo assume in un sistema di riferimento opportuno, ossia scelto appositamente affinchè l'equazione della conica sia la più semplice possibile.
Chiediamoci ora: se cambiamo sistema di riferimento, come cambia l'equazione? Prima di rispondere alla domanda è opportuno aprire una parentesi da cui apparirà meglio l'interesse della domanda stessa.


#### 7.2.1 **Movimenti rigidi, trasformazioni di coordinate, proprietà geometriche**

Cominciamo a ricordare che, nel piano, il più generale <mark class="hltr-yellow">movimento rigido</mark> (cioè che non altera le mutue distanze tra i punti) consiste in una <u>rototraslazione</u> (eventualmente combinata con una riflessione rispetto a una retta):
eseguire una rototraslazione di assi equivale quindi a cambiare il sistema di riferimento (cartesiano ortogonale), senza cambiare unità di misura sugli assi (ed eventualmente cambiando l'orientamento di uno dei due assi, se abbiamo eseguito una riflessione). A sua volta, [[#4.1 **L'algebra delle matrici**|sappiamo]] che una rotazione di angolo $\alpha$ rispetto all'origine è espressa dalle equazioni:

${\begin{cases}x=x'\cos\alpha-y'\sin\alpha \\  y=x'\sin\alpha+y'\cos\alpha\end{cases}}$

o anche, in forma compatta matriciale, dalla moltiplicazione per una [[#6.3.2 **Rotazioni dello spazio**|matrice di rotazione]]:

${\begin{pmatrix}x \\  y\end{pmatrix}}=\mathbf{R}{\begin{pmatrix}x' \\  y'\end{pmatrix}}$

con $\mathbf{R}$ matrice $(2,2)$ non singolare tale che $\mathbf{R}\mathbf{R}^\top=\mathbf{R}^\top\mathbf{R}=\mathbf{I}$ (ossia $\mathbf{R}$ è ortogonale) e $\det\mathbf{R}=1$.
Una rotazione eventualmente combinata con una riflessione rispetto a una retta è espressa da una matrice ortogonale qualsiasi (cioè avente $\det=\pm 1$); chiameremo **trasformazione ortogonale** una trasformazione di questo tipo.

Una <u>traslazione</u>, secondo un vettore $(u,v)^\top$, è espressa dalle equazioni: ${\begin{cases}x=x'+u \\  y=x'+v\end{cases}}$

Due trasformazioni ortogonali, nel piano, commutano tra loro e la loro composizione è un'altra trasformazione ortogonale; analogamente, due traslazioni commutano tra loro e la loro composizione è un'altra traslazione. Invece una traslazione e una trasformazione ortogonale non commutano tra loro.
*Ad esempio*, ruotare di un angolo $\alpha$ e poi traslare di un vettore $[u,v]^\top$ si esprime mediante le equazioni:

${\begin{cases}x=x'\cos\alpha-y'\sin\alpha +u \\  y=x'\sin\alpha+y'\cos\alpha +v\end{cases}}$

mentre traslare di un vettore $[u,v]^\top$ e poi ruotare di un angolo $\alpha$ si esprime mediante le equazioni:

${\begin{cases}x=(x'+u)\cos\alpha-(y'+v)\sin\alpha \\  y=(x'+u)\sin\alpha+(y'+v)\cos\alpha\end{cases}}\quad$, che comunque si possono riscrivere nella forma:

${\begin{cases}x=x'\cos\alpha-y'\sin\alpha +u' \\  y=x'\sin\alpha+y'\cos\alpha +v'\end{cases}}\quad$ con $\quad{\begin{cases}u'=u\cos\alpha-v\sin\alpha \\  v'=u\sin\alpha+v\cos\alpha\end{cases}}$

Dalla discussione precedente discende la prossima:

- #PROPOSIZIONE(11). Componendo, in qualsiasi ordine, un numero finito di traslazioni e rotazioni rispetto all'origine, nel piano, si ottiene sempre una trasformazione di equazioni ${\begin{cases}x=x'\cos\alpha-y'\sin\alpha +u \\  y=x'\sin\alpha+y'\cos\alpha +v\end{cases}}$, per qualche $\alpha,u,v\in\mathbb{R}$, detta appunto **rototraslazione**.
	
	In forma compatta matriciale, e ammettendo anche riflessioni rispetto ad una retta per l'origine, questa assume la forma:
	
							${\begin{pmatrix}x \\  y\end{pmatrix}}=\mathbf{R}{\begin{pmatrix}x' \\  y'\end{pmatrix}}+{\begin{pmatrix}u \\  v\end{pmatrix}}$
	
	con $\mathbf{R}$ matrice ortogonale $(2,2)$ e $[u,v]^\top\in\mathbb{R}^2$ assegnato.


Se una curva è rappresentata, rispetto ad un certo sistema di riferimento cartesiano ortogonale, da una certa equazione $f(x,y)=0$, cambiando riferimento sarà rappresentata da una nuova equazione $g(x',y')=0$, che si ottiene dalla precedente eseguendo sulle variabili $(x,y)$ un'opportuna trasformazione (vedi Proposizione precedente). La curva geometricamente rimane quindi la stessa.

È naturale chiedersi se nell'equazione sia rimasta traccia di quest'ultimo fatto: in altre parole, c'è qualche <u>proprietà algebrica</u> dell'equazione $f(x,y)=0$ che non cambia se eseguiamo una trasformazione di variabili?
Diremo che queste eventuali proprietà dell'equazione esprimono una <u>proprietà geometrica</u> della curva, per sottolineare il fatto che dipendono dalla curva e non dal particolare sistema di riferimento scelto per descriverla.

Anche l'operazione di moltiplicare ambo i membri dell'equazione per una costante $\lambda\ne 0$ porta formalmente ad un'equazione diversa, $\lambda f(x,y)=0$, eppure non cambia ovviamente il luogo geometrico descritto. Affinchè una proprietà algebrica dell'equazione esprima una proprietà geometrica della curva occorre quindi che la proprietà si conservi anche moltiplicando ambo i membri dell'equazione per una costante.

Si può dimostrare ad esempio la seguente:

- #PROPOSIZIONE(12). Se $f(x,y)=0$ è un'equazione algebrica di grado $n$ in $x,y$ (ossia $f$ è un polinomio di grado $n$), eseguendo sulle variabili $(x,y)$ una rototraslazione si ottiene un'equazione $g(x',y')=0$ che è ancora algebrica di grado $n$ in $x',y'$.

In altre parole: il grado $n$ di $f(x,y)$ esprime una proprietà geometrica della curva da essa rappresentata. Si anche che il grado $n$ è un'**invariante** (cioè una quantità che non cambia eseguendo una rototraslazione sulle variabili).

Ha senso parlare quindi ad esempio di "curve del secondo/terzo/$\cdots$ ordine", e non solo di equazioni, per indicare curve piane la cui equazione è espressa da un'equazione algebrica di grado $2,3,\cdots$. Infatti, se questo è vero in un particolare sistema di riferimento, allora sarà vero in <mark class="hltr-yellow">ogni</mark> sistema di riferimento cartesiano.
Dimostreremo questa Proposizione nel caso particolare $n=2$.


#### 7.2.2 **Le coniche come curve algebriche del second'ordine**

Consideriamo ora l'equazione canonica di un'ellisse, un'iperbole o una parabola e chiediamoci come cambia eseguendo una rototraslazione: in generale otterremo un'equazione dei secondo grado in $x,y$ completa di tutti i termini, ossia del tipo:

						$ax^2+bxy+cy^2+dx+ey+f=0$

Questo significa che, in un sistema di riferimento generico (ossia non scelto con criteri particolari) l'equazione di una conica assume quest'ultima forma, ovvero di una <u>curva del second'ordine</u>.
La discussione precedente suggerisce allora la seguente:

- #DEFINIZIONE(25). **Coniche come curve del second'ordine**
	
	Si dice conica di una qualunque piana del second'ordine, ossia espressa da un'equazione del tipo $ax^2+bxy+cy^2+dx+ey+f=0$ in cui i coefficienti $a,b,c$ non siano tutti nulli (altrimenti la curva sarebbe del prim'ordine, cioè una retta).

Per ora sappiamo che le coniche che già conosciamo si rappresentano in qualsiasi sistema di riferimento come curve del second'ordine, quindi sono coniche anche nel senso di quest'ultima definizione.
Non è chiaro se valga il viceversa: qualsiasi curva del second'ordine è un'ellisse, iperbole o parabola nel senso elementare del termine?
I prossimi esempi mostrano che non è così, e quindi l'ultima definizione data appare più ampia delle definizioni del [[#7.2 **L'equazione generale delle coniche. Riduzione a forma canonica**|paragrafo precedente]]:


*Esempio*. Consideriamo le seguenti equazioni, tutte di tipo:
	a) $x^2-y^2=0$
	b) $x^2=0$
	c) $x^2+y^2=0$
	d) $x^2+y^2+1=0$

L'equazione (a) è equivalente a $(x+y)(x-y)=0$, perciò rappresenta le due rette $y=x,y=-x$;
la (b) rappresenta una sola retta: $x=0$;
la (c) individua un solo punto, l'origine $O$;
la (d) infine non è mai verificata, perciò individua l'insieme vuoto $\left\{0\right\}$.


Inoltre, per quanto ne sappiamo fin qui, potrebbe restare il dubbio che esistano curve del second'ordine che hanno come immagine geometrica una curva effettiva ma di un tipo diverso dalle ellissi/parabole/iperboli che già conosciamo.

Data un'equazione di tipo $ax^2+bxy+cy^2+dx+ey+f=0$, occorrono dei criteri per decidere anzitutto se essa rappresenti effettivamente una curva nel senso intuitivo del termine (si dirà: una **conica reale non degenere**), e in secondo luogo di che tipo di curva si tratti.
I problemi sono quindi: riconoscere il tipo di curva a partire dall'equazione, e saperla ridurre a forma canonica, cioè trovare un sistema di riferimento in cui abbia un'equazione semplice, che ci permetta di tracciarla.

Entrambi i problemi si affrontano utilizzando il calcolo matriciale. Cominciamo col chiederci come si trasforma l'equazione $ax^2+bxy+cy^2+dx+ey+f=0$ sotto l'azione di una rototraslazione e che cosa eventualmente resta invariato.
È quindi più comodo riscrivere l'equazione nella forma:

					$a_{11}x^2+2a_{12}xy+a_{22}y^2+a_{13}x+a_{23}y+a_{33}=0$

Introducendo la matrice $(3,3)$ simmetrica:

							$\mathbf{A}={\begin{pmatrix}a_{11}&a_{12}&a_{13} \\  a_{12}&a_{22}&a_{23} \\  a_{13}&a_{23}&a_{33}\end{pmatrix}}$

l'equazione si riscrive nella forma matriciale seguente:

$(x,y,1)\mathbf{A}(x,y,1)^\top=0\quad$ o anche $\quad\mathbf{x}\mathbf{A}\mathbf{x}^\top=0\quad$ (avendo posto $\mathbf{x}=(x,y,1)$)

Poniamo anche $\mathbf{B}={\begin{pmatrix}a_{11}&a_{12} \\  a_{12}&a_{22}\end{pmatrix}}$.

Le matrici $\mathbf{A},\mathbf{B}$ si dicono rispettivamente **matrice dei coefficienti della conica** e **matrice dei termini di secondo grado della conica**.

Supponiamo ora di eseguire una rototraslazione di assi, di tipo ${\begin{cases}x=x'\cos\alpha-y'\sin\alpha +u \\  y=x'\sin\alpha+y'\cos\alpha +v\end{cases}}$;
la nuova equazione, nelle variabili $(x',y')$ può essere riscritta nella forma $a_{11}x^2+2a_{12}xy+a_{22}y^2+a_{13}x+a_{23}y+a_{33}=0$, con nuovi coefficienti $a_{ij}'$ che raccogliamo in una nuova matrice $\mathbf{A}'$.
Si dimostra che, anche se $\mathbf{A}'$ in generale può avere tutti gli elementi diversi dai corrispondenti elementi di $\mathbf{A}$, alcune quantità calcolate su questa matrice rimangono invariate (si dicono perciò **invarianti**):

- #TEOREMA(24). **Invarianti di una conica**
	
	A seguito di una rototraslazione di assi, la conica avente matrice dei coefficienti $\mathbf{A}$ e matrice dei termini di secondo grado $\mathbf{B}$ si trasforma in un'altra conica e le seguenti quantità rimangono invariate:
	
	$I_{3}=\det\mathbf{A}$ (<mark class="hltr-yellow">invariante cubico</mark>);
	$I_{3}=\det\mathbf{B}$ (<mark class="hltr-yellow">invariante quadratico</mark>);
	$I_{1}=Tr\mathbf{B}$ (<mark class="hltr-yellow">invariante lineare</mark>, Traccia = somma degli elementi sulla diagonale principale)
	
	In particolare, l'annullarsi o meno di un invariante $I_{1},I_{2}$ o $I_{3}$ esprime una proprietà geometrica della curva.


- **Osservazione** (1):
	
	Notiamo che se moltiplichiamo ambo i membri dell'equazione $a_{11}x^2+2a_{12}xy+a_{22}y^2+a_{13}x+a_{23}y+a_{33}=0$ della conica per una costante $\lambda\ne 0$, tutti i coefficienti $a_{ij}$ risultano moltiplicati per $\lambda$ e quindi le quantità $I_{1},I_{2},I_{3}$ si trasformano rispettivamente in $\lambda I_{1},\lambda^2 I_{2},\lambda^3 I_{3}$, da cui i nomi dei vari invarianti.
	Da questo fatto segue che anche il segno dell'invariante $I_{2}$ (ma non quello di $I_{1},I_{3}$) esprime una proprietà geometrica della curva.

- **Osservazione** (2): **Matrici a blocchi**
	
	A volte è comodo rappresentare una matrice dalla struttura complessa in termini di blocchi più piccoli. Ad esempio, se:
	
	$\mathbf{A}={\begin{pmatrix}a&b \\  c&d\end{pmatrix}}$,
	
	la scrittura $\mathbf{B}={\begin{pmatrix}\mathbf{A}&\mathbf{0}^\top \\  \mathbf{0}&1\end{pmatrix}}$ indica la matrice $(3,3)$ definita da $\mathbf{B}={\begin{pmatrix}a&b&0 \\  c&d&0 \\  0&0&1\end{pmatrix}}$.
	
	La dimensione dei vettori nulli indicati coi simboli $\mathbf{0},\mathbf{0}^\top$ nell'espressione di $\mathbf{B}$ si deduce in questo caso dal fatto che nell'angolo in basso a destra c'è un elemento singolo (il numero $1$) e in quello in alto a sinistra c'è una matrice $(2,2)$.
	Dovendo eseguire il prodotto di due "matrici a blocchi" espresse in termini di blocchi di dimensioni opportune, si può operare come se i blocchi fossero numeri. Ad esempio:
	
						${\begin{pmatrix}\mathbf{A}&\mathbf{0}^\top \\  \mathbf{0}&a\end{pmatrix}}{\begin{pmatrix}\mathbf{A}'&\mathbf{0}^\top \\  \mathbf{0}&a'\end{pmatrix}}={\begin{pmatrix}\mathbf{AA'}&\mathbf{0}^\top \\  \mathbf{0}&aa'\end{pmatrix}}$
	
	come si può verificare riscrivendo il calcolo senza far uso della notazione a blocchi.
	Useremo talvolta questo genere di scrittura abbreviata.


*Dimostrazione* ( #TEOREMA(24)) sul libro.


A titolo di *esempio*, calcoliamo gli invarianti $I_{2},I_{3}$ per l'ellisse, la parabola e l'iperbole in forma canonica:

- **Ellisse**:

	$\frac{x^2}{a^2}+\frac{y^2}{b^2}=1;\quad\mathbf{A}={\begin{pmatrix}\frac{1}{a^2}&0&0 \\  0&\frac{1}{b^2}&0 \\  0&0&-1\end{pmatrix}}\rightarrow I_{3}=\det\mathbf{A}=-\frac{1}{a^2b^2};I_{2}=\det\mathbf{B}=\frac{1}{a^2b^2}$.

- **Parabola**:

	$y=ax^2;\quad\mathbf{A}={\begin{pmatrix}a&0&0 \\  0&0&-1 \\  0&-1&0\end{pmatrix}}\rightarrow I_{3}=\det\mathbf{A}=-a;I_{2}=\det\mathbf{B}=0$.

- **Iperbole**:
	
	$\frac{x^2}{a^2}-\frac{y^2}{b^2}=\pm 1;\quad\mathbf{A}={\begin{pmatrix}\frac{1}{a^2}&0&0 \\  0&-\frac{1}{b^2}&0 \\  0&0&\mp 1\end{pmatrix}}\rightarrow I_{3}=\det\mathbf{A}=\pm\frac{1}{a^2b^2};I_{2}=\det\mathbf{B}=-\frac{1}{a^2b^2}$.

Notiamo che in tutti e tre i casi risulta $I_{3}\ne 0$, inoltre si ha: $I_{2}{\begin{cases}>0& \mbox{per l'ellisse} \\  =0 & \mbox{per la parabola} \\  <0& \mbox{per l'iperbole}\end{cases}}$.

D'altro canto sappiamo che una rototraslazione e una moltiplicazione dell'equazione per una costante non nulla non alterano il segno di $I_{2}$, quindi se una curva è un'ellisse/parabola/iperbole ([[#7.1 **Le coniche dal punto di vista elementare e le loro equazioni canoniche**|nel senso della geometria elementare]]), in qualunque sistema di riferimento la sua equazione ci darà $I_{2}$ rispettivamente positivo, nullo o negativo.
<u>Il calcolo algebrico di tale quantità permette quindi immediatamente di riconoscere la conica</u>.

Quest'argomentazione lascia però in ombra un punto delicato: presuppone infatti a priori che la curva sia una di queste tre. Ciò che ci aspetta ora è quest'ultima parte dell'indagine: a partire da una qualsiasi equazione algebrica di secondo grado, riconoscere se e quando questa rappresenta effettivamente una conica nel senso elementare del termine.

- #DEFINIZIONE(26). Si dice che una conica è **degenere**, o **riducibile**, quando la sua equazione si può riscrivere nella forma:
					
						$(ax+by+c)(a'x+b'y+c')=0$
	
	per certi $a,b,c,a',b',c'\in\mathbb{R}$ o $\mathbb{C}$.


Vale il seguente teorema che ci limitiamo ad enunciare:

- #TEOREMA(25). Una conica è **degenere** se e solo se si annulla il suo invariante $I_{3}$, cioè il determinante della matrice dei coefficienti. In questo caso il luogo geometrico descritto nel piano dall'equazione può essere una coppia di rette, oppure una retta, oppure un punto.


Ci concentriamo ora sulle coniche non degeneri, per le quali vogliamo ottenere una caratterizzazione completa in base ai loro invarianti.

- #TEOREMA(26). **Riconoscimento di una conica non degenere**
	
	Consideriamo una conica non degenere, cioè con $I_{3}\ne 0$. Allora:	
	- Se $I_{2}>0$ esiste una rototraslazione che la riduce alla forma canonica di un'ellisse:
	
		$\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ (reale) oppure $\frac{x^2}{a^2}+\frac{y^2}{b^2}=-1$ (immaginaria);
		
	- Se $I_{2}<0$ esiste una rototraslazione che la riduce alla forma canonica di un'iperbole:
		
		$\frac{x^2}{a^2}-\frac{y^2}{b^2}=1\quad$ oppure $\quad\frac{x^2}{a^2}-\frac{y^2}{b^2}=-1$;
		
	- Se $I_{2}=0$ esiste una rototraslazione che la riduce alla forma canonica di una parabola:
	
		$y=ax^2\quad$ oppure $\quad x=by^2$.


Notiamo che l'enunciato del Teorema insegna a riconoscere una conica non degenere per mezzo dei suoi invarianti. La dimostrazione del Teorema mostrerà come questo sia possibile costruendo effettivamente una rototraslazione che riduca la conica a forma canonica, permettendo così di riconoscerne il tipo, ma anche di tracciare effettivamente la curva.

Il Teorema mostra anche che le coniche non degeneri coincidono effettivamente con le coniche nel senso della geometria elementare, con un'<u>unica eccezione</u>:
l'ellisse immaginaria, curva priva di punti reali, che tuttavia in base alla definizione algebrica di conica come curva del second'ordine risulta una conica non degenere.


*Dimostrazione* ( #TEOREMA(26)):

Per prima cosa cerchiamo una traslazione che ottenga come risultato di annullare i termini di primo grado (ovvero i coefficienti $a_{13},a_{23}$). Questo equivale a cercare $u,v$, per cui si abbia:

${\begin{cases}a_{13}+a_{11}u+a_{12}v=0 \\  a_{23}+a_{12}u+a_{22}v=0\end{cases}}$

Questo è un sistema lineare di due equazioni nelle due incognite $u,v$, risolubile purchè sia:

$\det{\begin{pmatrix}a_{11}&a_{12} \\  a_{12}&a_{22}\end{pmatrix}}\ne 0$, ossia $I_{2}\ne 0$.

Cominciamo a trattare questo caso: se $I_{2}\ne 0$ esiste una traslazione che porta la conica alla forma:

$a_{11}x^2+2a_{12}xy+a_{22}y^2+a_{33}=0$

(per semplicità continuiamo a chiamare i coefficienti $a_{ij}$ anzichè $a_{ij}'$).
Si osservi che questa conica ha l'origine come centro di simmetria, ossia: se il punto $(x,y)$ soddisfa l'equazione, anche $(-x,-y)$ (il suo simmetrico rispetto all'origine) la soddisfa.
Le coniche con $I_{2}\ne 0$ si dicono perciò **coniche a centro**.

Ora cerchiamo una rotazione che abbia come effetto di annullare il coefficiente $a_{12}$.
Qualsiasi rotazione trasformerà la conica in un'altra che ha ancora i termini $a_{13},a_{23}$ mancanti, e la matrice $\mathbf{B}$ si trasformerà secondo la legge $\mathbf{B}'=\mathbf{R}^\top\mathbf{B}\mathbf{R}$.

Noi desideriamo che $\mathbf{B}'$ risulti una matrice diagonale; poichè $\mathbf{B}$ è reale simmetrica, sappiamo che è sempre possibile diagonalizzarla mediante una matrice di rotazione, quindi: esiste una rotazione $\mathbf{R}$ che trasforma la conica in una di equazione (indicando i nuovi coefficienti ancora con i simboli $a_{ij}$ senza apici):

$a_{11}x^2+a_{22}y^2+a_{33}=0$, ossia $\mathbf{A}=diag(a_{11},_{22},a_{33})$.

(Nel seguito ci servirà saper calcolare esplicitamente la matrice di rotazione $\mathbf{R}$; a questo scopo è utile [[#6.3 **Condizioni di diagonalizzabilità**|ricordare]] che le sue colonne sono gli autovettori normalizzati relativi agli autovettori di $\mathbf{B}$)

Poichè siamo nell'ipotesi di conica non degenere, $I_{3}\ne 0$ perciò i tre coefficienti $a_{11},a_{22},a_{33}\ne 0$.
Distinguiamo ora i vari casi possibili in base al segno dei tre coefficienti rimasti: possiamo sempre supporre $a_{11}>0$ (eventualmente cambiando tutti i segni nell'equazione), perciò i casi sono:

1. $a_{aa}>0,a_{33}<0$. Dividendo per $a_{33}$ si può riscrivere l'equazione nella forma:

	$\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ (ellisse reale in forma canonica).

2. $a_{22}>0,a_{33}>0$. Dividendo per $a_{33}$ si può riscrivere l'equazione nella forma:

	$\frac{x^2}{a^2}+\frac{y^2}{b^2}=-1$ (ellisse immaginaria; si osservi che $I_{2}>0$ sia per reale che immaginaria).

3. $a_{22}<0,a_{33}<0$. Dividendo per $a_{33}$ si può riscrivere l'equazione nella forma:

	$\frac{x^2}{a^2}-\frac{y^2}{b^2}=1$ (iperbole in forma canonica).

4. $a_{22}<0,a_{33}>0$. Dividendo per $a_{33}$ si può riscrivere l'equazione nella forma:

	$\frac{x^2}{a^2}-\frac{y^2}{b^2}=-1$ (iperbole in forma canonica; si osservi che $I_{2}<0$ per entrambe).

Consideriamo ora il caso lasciato in sospeso, in cui $I_{2}=0$: si dice che **la conica non è a centro**.

Cerchiamo direttamente una rotazione che annulli il coefficiente $a_{12}$: esiste sempre una rotazione $\mathbf{R}$ che trasforma la matrice $\mathbf{A}$ in modo che $\mathbf{B}$ risulti diagonalizzata. Dopo la rotazione la conica ha quindi una nuova matrice:

$\mathbf{B}={\begin{pmatrix}a_{11}&0 \\  0&a_{22}\end{pmatrix}}$

Ricordiamo però che siamo nelle ipotesi $I_{2}\ne 0$, perciò si ha $a_{11}a_{22}=0$, quindi si annulla anche uno di questi coefficienti. Supponiamo ad esempio che sia $a_{11}=0$ (l'altro caso è analogo).
La nuova equazione è quindi:

$a_{22}y^2+2a_{13}x+2a_{23}y+a_{33}=0,\quad\mathbf{A}={\begin{pmatrix}0&0&a_{13} \\  0&a_{22}&a_{23} \\  a_{13}&a_{23}&a_{33}\end{pmatrix}}$

con $a_{22}\ne 0$ altrimenti la curva non sarebbe del second'ordine e $a_{13}\ne 0$, altrimenti si avrebbe $I_{3}=0$, ossia la conica sarebbe degenere. Cerchiamo una traslazione che annulli gli altri due coefficienti, $a_{23},a_{33}$. Con la tecnica di completamento del quadrato possiamo eliminare il coefficiente della $y$:

$a_{22}y^2+2a_{23}y=a_{22}\left( y^2+2\frac{a_{23}}{a_{22}}y \right)=a_{22}\left( y^2+2\frac{a_{23}}{a_{22}}y+\left( \frac{a_{23}}{a_{22}} \right)^2 \right)-\frac{a_{23}^2}{a_{22}}=a_{22}\left( y+\frac{a_{23}}{a_{22}} \right)^2-\frac{a_{23}^2}{a_{22}}$

perciò ponendo $y'=y+\frac{a_{23}}{a_{22}}$ l'equazione diventa: $a_{22}y'^2+2a_{13}x+a_{33}-\frac{a_{23}^2}{a_{22}}=0$.

Ora dalle identità: $2a_{13}x+a_{33}-\frac{a_{23}^2}{a_{22}}=2a_{13}\left( x+\frac{a_{22}a_{33}-a_{23}^2}{2a_{13}a_{22}} \right)$

leggiamo che ponendo $x'=x+\frac{a_{22}a_{33}-a_{23}^2}{2a_{13}a_{22}}$ l'equazione diventa:

$a_{22}y'^2+2a_{13}x'=0$
$x'=-\frac{a_{22}}{2a_{13}}y'^2$

che è una parabola in forma canonica.

Si osservi che abbiamo considerato tutti i casi possibili nell'ipotesi $I_{3}\ne 0$ e abbiamo riscontrato che la conica è effettivamente un'iperbole se $I_{2}<0$, un'ellisse reale o immaginaria se $I_{2}>0$, una parabola se $I_{2}=0$. Il Teorema è quindi dimostrato.


*Esempio*. Riconoscere le seguenti coniche e ridurle a forma canonica:

(a) $x^2+2y^2-4x+3y+1=0$
(b) $x^2-4y^2+x-1=0$
(c) $2xy+x+1=0$

a) $I_{3}\ne 0,I_{2}>0$ perciò è una conica non degenere e precisamente un'ellisse.
Non è immediatamente evidente se si tratti di un'ellisse reale o immaginaria, ma con la tecnica di completamento dei quadrati, scriviamo:

$x^2-4x=(x-2)^2-4$
$2y^2+3y=2\left( y+\frac{3}{4} \right)^2-\frac{9}{8}$

e quindi l'equazione diventa:

$(x-2)^2-4+2\left( y+\frac{3}{4} \right)^2-\frac{9}{8}+1=0\rightarrow\frac{(x-2)^2}{\frac{33}{8}}+\frac{\left( y+\frac{3}{4} \right)^2}{\frac{33}{16}}=1$

Perciò si tratta dell'ellisse reale di centro $\left( 2,-\frac{3}{4} \right)$ e semiassi $\sqrt{\frac{33}{8}},\frac{\sqrt{33}}{4}$.


b) $I_{3}\ne 0,I_{2}<0$ perciò è una conica non degenere e precisamente un'iperbole. Riscrivendo:

$x^2+x-1=\left( x+\frac{1}{2} \right)^2-\frac{1}{4}-1$

l'equazione prende la forma:

$\left( x+\frac{1}{2} \right)^2-4y^2=\frac{5}{4}\rightarrow\frac{\left( x+\frac{1}{2} \right)^2}{\left( \frac{\sqrt{5}}{2} \right)^2}-\frac{y^2}{\left( \frac{\sqrt{5}}{4} \right)^2}=1$

da cui leggiamo che è un'iperbole di centro $\left( -\frac{1}{2},0 \right)$, asintoti $y=\pm\frac{\left( \frac{\sqrt{5}}{4} \right)}{\left( \frac{\sqrt{5}}{2} \right)}\left( x+\frac{1}{2} \right)$, cioè $y=\pm\left( \frac{1}{2}x+\frac{1}{4} \right)$.


c) Si ha $I_{3}\ne 0,I_{2}<0$ perciò si tratta di un'iperbole non degenere. Posto $\mathbf{B}={\begin{pmatrix}0&1 \\  1&0\end{pmatrix}}$
cerchiamo anzitutto autovalori e autovettori di $\mathbf{B}$. Un facile calcolo dà: $\lambda_{1}=1,\lambda_{2}=-1$
con autovettori relativi (ad esempio): $\mathbf{v}_{1}=(1,1);\mathbf{v}_{2}=(1,-1)$.

Si noti che $\mathbf{v}_{1},\mathbf{v}_{2}$ sono ortogonali, ma non hanno modulo unitario. Normalizzandoli cioè calcolando:

$\mathbf{v}_{1}'=\left( \frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}} \right);\mathbf{v}_{2}=\left( \frac{1}{\sqrt{2}},-\frac{1}{\sqrt{2}} \right)$

otteniamo la matrice di rotazione richiesta: $\mathbf{R}={\begin{pmatrix}\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}} \\  \frac{1}{\sqrt{2}}&-\frac{1}{\sqrt{2}}\end{pmatrix}}\quad$ (rotazione di $\frac{\pi}{4}$).
Eseguendo dunque la rotazione:

${\begin{cases}x=\frac{1}{\sqrt{2}}x'+\frac{1}{\sqrt{2}}y' \\  y=\frac{1}{\sqrt{2}}x'-\frac{1}{\sqrt{2}}y'\end{cases}}$

l'equazione della conica diventa: $x'^2-y'^2+\frac{1}{\sqrt{2}}x'+\frac{1}{\sqrt{2}}y'+1=0$

Il completamento dei quadrati ci suggerisce ora la traslazione corretta da eseguire:

$\left( x'-\frac{1}{2\sqrt{2}} \right)^2-\frac{1}{8}-\left( y'+\frac{1}{2\sqrt{2}} \right)^2+\frac{1}{8}+1=0$

Ponendo quindi:

${\begin{cases}x''=x'-\frac{1}{2\sqrt{2}} \\  y''=y'+\frac{1}{2\sqrt{2}}\end{cases}}$

l'equazione dell'iperbole si può riscrivere nella forma canonica:

$x''^2-y''^2=-1$.


Nel Teorema precedente abbiamo considerato solo coniche non degeneri. Per analogia a quanto stabilito in tale Teorema possiamo ora dare la seguente:

- #DEFINIZIONE(27). Consideriamo una conica degenere. Diremo ancora che la conica è una:
	
	${\begin{cases}\mbox{ellisse (degenere)} \\  \mbox{parabola (degenere)} \\  \mbox{iperbole (degenere)}\end{cases}}$ se ${\begin{cases}>0 \\  =0 \\  <0\end{cases}}$.


Si può dimostrare la seguente:

- #PROPOSIZIONE(13). **Tipi di coniche degeneri**
	
	Le coniche degeneri possono essere solo dei seguenti tipi:
	
	- un'ellisse degenere è costituita da un solo punto reale (ad *es.* $x^2+y^2=0$);
	- una parabola degenere è costituita da una sola retta (reale) o da due rette parallele (reali) o dall'insieme vuoto (ad *es.* rispettivamente, $(y+1)^2=0,y(y+1)=0,y^2+1=0$);
	- un'iperbole degenere è costituita da due rette (reali) distinte o incidenti (ad *es.* $x^2-y^2=0$).


Per analogia con le coniche spezzate in due rette reali, nel caso dell'ellisse degenere (un punto) si dice anche che la conica si spezza in due rette complesse coniugate che si intersecano in un punto reale (ad *es.* $y=\pm ix$, che si interseca nell'origine $O$) e nel caso della parabola che degenera all'insieme vuoto si dice anche che la conica si spezza in due rette parallele immaginarie (ad *es.* $y=\pm i$, che non hanno alcun punto reale).
I prossimi esempi illustrano alcune di queste situazioni:


*Esempio* (1). Consideriamo la conica $x^2-2y^2+xy-x+y=0$.

La matrice dei coefficienti è: $\mathbf{A}={\begin{pmatrix}1&\frac{1}{2}&-\frac{1}{2} \\  \frac{1}{2}&-2&\frac{1}{2} \\  -\frac{1}{2}&\frac{1}{2}&0\end{pmatrix}}$

e il calcolo mostra che $I_{3}=\det\mathbf{A}=0$ e $I_{2}=\det\mathbf{B}<0$. Si tratta quindi di un'iperbole degenere che si spezza in due rette distinte. Per scomporre effettivamente il primo membro possiamo procedere così: risolviamo l'equazione come equazione di secondo grado in $x$, al modo seguente (ovviamente sarebbe lo stesso in $y$):

$x^2-x(1-y)+(y-2y^2)=0$
$x=\frac{(1-y)\pm\sqrt{(1-y)^2-4(y-2y^2)}}{2}=\frac{(1-y)\pm\sqrt{9y^2-6y+1}}{2}=\frac{(1-y)\pm(3y-1)}{2}$

da cui otteniamo le due rette $x=y;x=1-2y$
ossia l'equazione di partenza si può riscrivere così:

$(x-y)(x+2y-1)=0$.

La conica degenere in questo caso si spezza in due rette reali e distinte. Il fatto che nella risoluzione dell'equazione di secondo grado il radicando risulti un quadrato perfetto (e quindi $x$ si esprime come funzione lineare di $y$) dipende proprio dall'ipotesi $I_{3}=0$.



### 7.3 **Coniche ed eccentricità**

È possibile dare un'ulteriore caratterizzazione di ellisse, parabola e iperbole come opportuni luoghi geometrici, che rispetto alle definizioni in termini di fuochi o direttrice nel [[#7.1 **Le coniche dal punto di vista elementare e le loro equazioni canoniche**|primo paragrafo]] ha il pregio di trattare i tre tipi di coniche in modo più uniforme:

- #TEOREMA(27). **Caratterizzazione delle coniche mediante l'eccentricità**
	
	Consideriamo, nel piano, un punto detto <u>fuoco</u>, ed una retta non passante per il fuoco, detta <u>direttrice</u>. Il luogo dei punti $P$ per cui il rapporto tra la distanza di $P$ dal fuoco e la distanza di $P$ dalla direttrice è costante è una conica; questa costante si dice **eccentricità** ($e$) della conica. Precisamente la conica risulta essere:
	
	${\begin{cases}\mbox{iperbole}&\mbox{se}&e>1 \\  \mbox{parabola}&\mbox{se}&e=1 \\  \mbox{ellisse}&\mbox{se}&0<e<1\end{cases}}$


Segnaliamo che questa caratterizzazione delle coniche mediante l'eccentricità presenta un'<u>eccezione</u>: la circonferenza non può essere ottenuta con questo procedimento, in quanto in un certo senso rappresenta il caso limite di conica con eccentricità nulla.
Questo Teorema è alla base della rappresentazione delle coniche come curve in forma polare.

*Dimostrazione* ( #TEOREMA(27)):

Scegliamo un riferimento cartesiano in cui detto $F$ il fuoco e $d$ la direttrice risulti per qualche $a>0$: ${\begin{cases}F(a,0) \\ d:x=-a \end{cases}}$

La definizione richiede che, detto $P(x,y)$ il generico punto della conica, il rapporto tra la distanza di $P$ da $F$ e la distanza di $P$ da $d$ sia uguale ad una costante $e>0$, detta eccentricità della conica. Questa condizione si traduce nell'equazione:

$\frac{\sqrt{(x-a)^2+y^2}}{|x+a|}=e$

da cui ricaviamo successivamente:

$\sqrt{(x-a)^2+y^2}=e|x+a|$
$(x-a)^2+y^2=e^2(x+a)^2$

e, sviluppando e semplificando:

$x^2(1-e^2)+y^2-2ax(1+e^2)+a^2(1-e^2)=0$

che è la conica avente matrice dei coefficienti: $\mathbf{A}={\begin{pmatrix}1-e^2&0&-a(1+e^2) \\  0&1&0 \\  -a(1+e^2)&0&a^2(1-e^2)\end{pmatrix}}$

da cui calcoliamo: ${\begin{cases}I_{3}=-4a^2e^2 \\  I_{2}=1-e^2\end{cases}}$

La conica ottenuta è quindi non degenere per $a>0,e>0$, e risulta un'iperbole per $e>1$, un'ellisse per $0<e<1$, una parabola per $e=1$.

Notiamo ancora che nel caso $0<e<1$ l'ellisse non è mai una circonferenza. Per diventare una circonferenza dovrebbe infatti essere $e=0$, il che però corrisponde ad una conica degenere.




# **Capitolo VIII: Quadriche**


Se facciamo ruotare una parabola attorno al suo asse, oppure un'ellisse o un'iperbole attorno ai suoi due assi di simmetria, otteniamo superfici dall'aspetto abbastanza semplice che, prendendo il nome della conica generatrice, si dicono **paraboloide**, **ellissoide** o **iperboloide** di rotazione: questi sono gli esempi più semplici di **superfici quadriche** (ma non le uniche).

Per dare una definizione generale di superficie quadrica e poter studiare queste superfici è naturale utilizzare fin da subito il linguaggio della geometria analitica e del calcolo matriciale.
Diamo quindi la seguente:

- #DEFINIZIONE(28). **Quadriche come superfici del second'ordine**
	
	Si dice superficie quadrica (o semplicemente quadrica) il luogo dei punti dello spazio le cui coordinate $(x,y,z)$ soddisfano un'equazione algebrica di secondo grado in $x,y,z$ del tipo:
	
		$a_{11}x^2+a_{22}y^2+a_{33}z^2+2a_{12}xy+2a_{13}xz+2a_{23}yz+2a_{14}x+2a_{24}y+2a_{34}z+a_{44}=0$
	
	ovvero, in forma matriciale: $(x,y,z,1)\mathbf{A}(x,y,z,1)^\top=0$
	
	dove: $\mathbf{A}={\begin{pmatrix}a_{11}&a_{12}&a_{13}&a_{14} \\  a_{12}&a_{22}&a_{23}&a_{24} \\  a_{13}&a_{23}&a_{33}&a_{34} \\  a_{14}&a_{24}&a_{34}&a_{44}\end{pmatrix}}$
	
	è la matrice rela simmetrica $4\times 4$ di coefficienti $a_{ij}$. Supponiamo inoltre che la matrice dei termini di secondo grado:
	
	$\mathbf{B}={\begin{pmatrix}a_{11}&a_{12}&a_{13} \\  a_{12}&a_{22}&a_{23} \\    a_{13}&a_{23}&a_{33}\end{pmatrix}}$
	
	non sia la matrice nulla (altrimenti non si tratterebbe di una superficie del second'ordine, ma del primo ovvero un piano).


Anche se la definizione data è puramente algebrica, ci interessa studiare queste superfici dal punto di vista geometrico. Come per le coniche, le proprietà geometriche sono quelle che non dipendono dal particolare sistema di riferimento scelto, ossia sono <u>invarianti per rototraslazioni</u>.
Dopo aver richiamato qualche proprietà delle rototraslazioni nello spazio tridimensionale e aver individuato alcuni invarianti delle quadriche, cercheremo una rototraslazione che porti una quadrica ad assumere un'equazione la più semplice possibile.
Individueremo così facendo le equazioni in forma canonica dei vari tipi di quadriche, arrivando ad una classificazione delle quadriche stesse ed al riconoscimento del loro aspetto geometrico.



### 8.1 **Rototraslazioni nello spazio e invarianti di una quadrica**

Abbiamo visto nel  [[#6.3 **Condizioni di diagonalizzabilità**|capitolo 6.3]] che, nello spazio tridimensionale, una rotazione rispetto all'origine, eventualmente accompagnata da una riflessione rispetto ad un piano passante per l'origine, si può rappresentare mediante una matrice $\mathbf{R}$, $(3,3)$ ed ortogonale:

								${\begin{pmatrix}z \\  y \\  z\end{pmatrix}}=\mathbf{R}\begin{pmatrix}x' \\  y' \\  z'\end{pmatrix}$

A differenza di quanto accade nel piano, <u>il prodotto di due trasformazioni ortogonali nello spazio non è commutativo</u>. Ad ogni modo la composizione di due trasformazioni ortogonali è ancora una trasformazione ortogonale.
Una traslazione è rappresentata da:

							$\begin{pmatrix}x \\  y \\  z\end{pmatrix}=\mathbf{R}\begin{pmatrix}x' \\  y' \\  z'\end{pmatrix}+\begin{pmatrix}u \\  v \\  w\end{pmatrix}$

La composizione di un numero finito di traslazioni e di trasformazioni ortogonali, in qualunque ordine, assume sempre la medesima forma per qualche matrice ortogonale $\mathbf{R}$ e qualche vettore $(u,v,w)^\top\in\mathbb{R}^3$; l'ultima espressione rappresenta quindi la generica rototraslazione (con eventuale riflessione) nello spazio. Sotto l'azione di una rototraslazione qualsiasi, l'equazione di una generica quadrica si trasformerà ancora in un'equazione del second'ordine.

Vediamo più da vicino come cambia l'equazione di una quadrica sotto l'azione di una trasformazione ortogonale oppure di una traslazione. Il calcolo, in forma matriciale, è analogo a quello già fatto per le coniche.
Se $\mathbf{R}$ è una matrice ortogonale $(3,3)$, ponendo $\mathbf{x}=(x,y,z,1),\mathbf{x}'=(x',y',z',1)$, possiamo riscrivere (utilizzando la scrittura delle matrici a blocchi e ponendo $(0,0,0)=\mathbf{0}$):

$\mathbf{x}^\top=\begin{pmatrix}\mathbf{R}&\mathbf{0}^\top \\  \mathbf{0}&1\end{pmatrix}\mathbf{x}'^\top$, quindi $\mathbf{x}=\mathbf{x}'\begin{pmatrix}\mathbf{R}^\top&\mathbf{0}^\top \\ \mathbf{0}&1\end{pmatrix}$

che sostituite nell'equazione matriciale della quadrica $\mathbf{x}\mathbf{A}\mathbf{x}^\top=0$ danno:

$\mathbf{x}'\begin{pmatrix}\mathbf{R}^\top&\mathbf{0}^\top \\  \mathbf{0}&1\end{pmatrix}\mathbf{A}\begin{pmatrix}\mathbf{R}&\mathbf{0}^\top \\  \mathbf{0}&1\end{pmatrix}\mathbf{x}'^\top=0$

da cui leggiamo che la matrice $\mathbf{A}$ si trasforma nella matrice:

$\mathbf{A}'=\begin{pmatrix}\mathbf{R}^\top&\mathbf{0}^\top \\  \mathbf{0}&1\end{pmatrix}\mathbf{A}\begin{pmatrix}\mathbf{R}&\mathbf{0}^\top \\  \mathbf{0}&1\end{pmatrix}=\mathcal{R}^\top\mathbf{A}\mathcal{R}$

e in particolare $\mathbf{B}$ si trasforma in $\mathbf{B}'=\mathbf{R}^\top\mathbf{B}\mathbf{R}$.


Analogamente a quanto abbiamo visto per le coniche, l'azione di una rototraslazione $\mathbf{R}$ su una quadrica trasforma quindi la matrice $\mathbf{B}$ dei coefficienti dei termini di $2^o$ grado della quadrica in una matrice simile $\mathbf{B}'$. In particolare, $\mathbf{B}$ e $\mathbf{B}'$ hanno lo stesso determinante.
Inoltre, scegliendo opportunamente la matrice $\mathbf{R}$ ortogonale nell'ultima espressione, $\mathbf{B}$ può essere diagonalizzata, ossia portata alla forma: $\mathbf{B}'=diag(a_{11}',a_{22}',a_{33}')$.

Questo fatto sarà <u>utile nella riduzione a forma canonica della quadrica</u>.
Notiamo anche che la matrice $\mathcal{R}$ è ancora ortogonale, perciò anche $\mathbf{A}$ e $\mathbf{A}'$ sono matrici simili e in particolare hanno lo stesso determinante.

Eseguendo invece una traslazione, l'equazione della quadrica si trasforma in:

$\mathbf{x}'\mathbf{A}'\mathbf{x}'^\top=0$

dove la matrice $\mathbf{A}'$ ha gli stessi coefficienti di $\mathbf{A}$ nella parte di secondo grado $(\mathbf{B}'=\mathbf{B})$, mentre gli altri coefficienti cambiano secondo la legge:

${\begin{cases}a_{14}'=a_{11}u+a_{12}v+a_{13}w+a_{14} \\  a_{24}'=a_{12}u+a_{22}v+a_{23}w+a_{24} \\  a_{34}'=a_{13}u+a_{23}v+a_{33}w+a_{34} \\  a_{44}'=a_{11}u^2+a_{22}v^2+a_{33}w^2+2a_{12}uv+2a_{13}uw+2a_{23}uw+2a_{14}+2a_{24}+2a_{34}+a_{44}\end{cases}}$

Anche queste relazioni ci saranno <u>utili nella riduzione a forma canonica delle quadriche</u>.
Possiamo ora enunciare il seguente:

- #TEOREMA(28). **Invarianti di una quadrica**
	
	Con le notazioni introdotte nella #DEFINIZIONE(28), le seguenti quantità risultano invarianti sotto l'effetto di una rototraslazione:
	
	$\mathcal{I}_{1}=Tr\mathbf{B}=a_{11}+a_{22}+a_{33}$
	$\mathcal{I}_{2}=\det \begin{pmatrix}a_{11}&a_{12} \\  a_{12}&a_{22}\end{pmatrix}+\det \begin{pmatrix}a_{11}&a_{13} \\  a_{13}&a_{33}\end{pmatrix}+\det \begin{pmatrix}a_{22}&a_{23} \\  a_{23}&a_{33}\end{pmatrix}$
	$\mathcal{I}_{3}=\det\mathbf{B}$
	$\mathcal{I}_{4}=\det\mathbf{A}$
	
	Sono inoltre invarianti la caratteristica della matrice $\mathbf{A}$ e gli autovalori di $\mathbf{B}$.
	
	*Dimostrazione*:
	Ricordiamo che le matrici $\mathbf{A},\mathbf{B}$ di una conica si trasformano per effetto di una rototraslazione in matrici $\mathbf{A}',\mathbf{B}'$ simili rispettivamente ad $\mathbf{A},\mathbf{B}$ e che, per quanto visto nel [[#6.1 **Matrici diagonalizzabili**|capitolo 6.1]], matrici simili hanno lo stesso determinante, la stessa caratteristica e lo stesso polinomio caratteristico, quindi gli stessi autovalori. Ciò implica immediatamente che $\mathcal{I}_{4},\mathcal{I}_{3}$, la caratteristica di $\mathbf{A}$ e gli autovalori di $\mathbf{B}$ siano invarianti. Inoltre, scrivendo esplicitamente il polinomio caratteristico di $\mathbf{B}$ si ottiene:
	
						$\det(\mathbf{B}-\lambda\mathbf{I})=-\lambda^3+\lambda^2\mathcal{I}_{1}-\lambda\mathcal{I}_{2}+\mathcal{I}_{3}$
	
	da cui leggiamo l'invarianza di $\mathcal{I}_{1}$ e $\mathcal{I}_{2}$.


Osserviamo anche che, moltiplicando l'equazione della quadrica per un coefficiente $\lambda>0$, gli invarianti $\mathcal{I}_{1},\mathcal{I}_{2},\mathcal{I}_{3},\mathcal{I}_{4}$ risultano moltiplicati rispettivamente per $\lambda, \lambda^2, \lambda^3,\lambda^4$, mentre gli autovalori di $\mathbf{B}$ sono moltiplicati per $\lambda$.
Tenendo conto anche di quest'osservazione possiamo enunciate la seguente Proposizione, che raccoglie i fatti che operativamente utilizzeremo nella classificazione delle quadriche:

- #PROPOSIZIONE(14). I seguenti fatti esprimono una proprietà geometrica della superficie quadrica:

	- l'annullarsi o meno di ciascuno degli invarianti (in particolare utilizzeremo $\mathcal{I}_{3},\mathcal{I}_{4}$);
	- il segno degli invarianti $\mathcal{I}_{2}$ e $\mathcal{I}_{4}$ (utilizzeremo solo il segno di $\mathcal{I}_{4}$);
	- il numero di autovalori di $\mathbf{B}$ che si annullano e il fatto che gli autovalori non nulli siano concordi tra loro oppure no;
	- la caratteristica di $\mathbf{A}$.


Diamo anche la seguente:

- #DEFINIZIONE(29). Si dice che una quadrica è **degenere** se $\mathcal{I}_{4}=0$.


Vedremo un po' alla volta che forma possono assumere le quadriche degeneri.



### 8.2 **Riduzione a forma canonica delle quadriche: quadriche a centro**

Consideriamo ora una generica quadrica: ci proponiamo di determinare una rototraslazione che ne trasformi l'equazione in una forma abbastanza semplice da permetterci di riconoscere le proprietà importanti della superficie. Così facendo arriveremo ad una <u>classificazione delle quadriche</u>.

Chiediamoci anzitutto se esiste una **traslazione** che abbia come effetto quello di annullare i coefficienti dei termini di primo grado, cioè $a_{14},a_{24},a_{34}$; dal sistema trovato nel paragrafo precedente sappiamo che questo equivale a cercare $u,v,w$ che soddisfano il sistema:

						$\begin{cases}a_{11}u+a_{12}v+a_{13}w+a_{14}=0 \\  a_{12}u+a_{22}v+a_{23}w+a_{24}=0 \\  a_{13}u+a_{23}v+a_{33}w+a_{34}=0\end{cases}$

che è un sistema lineare di tre eq. in 3 incognite, avente per matrice dei coefficienti $\mathbf{B}$.
La traslazione cercata quindi esiste certamente se $\mathcal{I}_{3}\ne 0$; mettiamoci in tale ipotesi.
Dopo la traslazione quindi l'equazione della quadrica sarà (chiamando un'altra volta per semplicità i coefficienti con i simboli $a_{ij}$ anziché $a_{ij}'$):

				$a_{11}x^2+a_{22}y^2+a_{33}z^2+2a_{12}xy+2a_{13}xz+2a_{23}yz+a_{44}=0$

Si osserva che questa superficie è <u>simmetrica rispetto all'origine</u>: se la terna $x,y,z$ soddisfa l'equazione, anche $-x,-y-z$ la soddisfa; questo si può esprimere dicendo che l'origine $O$ è centro di simmetria per la quadrica, o anche che la superficie è una **quadrica a centro**.
Abbiamo quindi stabilito la seguente:

- #PROPOSIZIONE(15). Se $\mathcal{I}_{3}\ne 0$, la quadrica è a centro; un'opportuna traslazione la riconduce alla forma:
				
			$a_{11}x^2+a_{22}y^2+a_{33}z^2+2a_{12}xy+2a_{13}xz+2a_{23}yz+a_{44}=0$
				
	simmetrica rispetto ad $O$.


Esaminiamo ora l'effetto di una **rotazione** su una quadrica a centro, per la quale cioè risulta:

$\mathbf{A}=\begin{pmatrix}\mathbf{B}&\mathbf{0}^\top \\  \mathbf{0}&a_{44}\end{pmatrix}$, avendo posto $\mathbf{0}=(0,0,0)$. La matrice $\mathbf{A}$ si trasforma in:

				$\mathbf{A}'=\begin{pmatrix}\mathbf{R}^\top&\mathbf{0}^\top \\  \mathbf{0}&1\end{pmatrix}\begin{pmatrix}\mathbf{B}&\mathbf{0}^\top \\  \mathbf{0}&a_{44}\end{pmatrix}\begin{pmatrix}\mathbf{R}&\mathbf{0}^\top \\  \mathbf{0}&1\end{pmatrix}=\begin{pmatrix}\mathbf{R}^\top\mathbf{B}\mathbf{R}&\mathbf{0}^\top \\  \mathbf{0}&a_{44}\end{pmatrix}$

ossia la quadrica rimane a centro, e la matrice $\mathbf{B}$ si trasforma secondo la legge $\mathbf{B}'=\mathbf{R}^\top \mathbf{B}\mathbf{R}$.
Con una scelta opportuna della rotazione possiamo quindi diagonalizzare la matrice $\mathbf{B}$, ossia ridurre l'equazione della quadrica alla forma:

						$a_{11}x^2+a_{22}y^2+a_{33}z^2+a_{44}=0$

con $\mathcal{I}_{3}=a_{11}a_{22}a_{33}\ne 0$ per ipotesi. Si noti che in questo caso risulta $\mathcal{I}_{4}=a_{44}\mathcal{I}_{3}$.
Pertanto $\mathcal{I}_{4}=0$, ossia la quadrica è degenere, se e solo se $a_{44}=0$.
Discutiamo subito questa situazione, ossia consideriamo una <u>quadrica a centro, degenere</u>:

						$a_{11}x^2+a_{22}y^2+a_{33}z^2=0$

L'unica distinzione di rilievo, per quanto riguarda la forma della superficie descritta da questa equazione, sta nei segni dei tre coefficienti $a_{11},a_{22},a_{33}$ (tutti $\ne 0$ per l'ipotesi $\mathcal{I}_{3}\ne 0$).
Se i tre coefficienti non hanno tutti lo stesso segno, ad esempio $a_{11}$ e $a_{22}$ hanno lo stesso segno e $a_{33}$ ha segno diverso (gli altri casi si ottengono semplicemente cambiando nomi alle variabili), l'equazione si può riscrivere nella forma:

						$a^2x^2+b^2y^2=c^2z^2\quad(a,b,c>0)$

essa rappresenta un cono a due falde che ha vertice in $O$ e per generatrice ad esempio l'ellisse di equazione $ax^2+b^2y^2=c^2$ nel piano $z=1$.

Infatti, preso un punto $(x_{0},y_{0},1)$ su tale curva, ossia tale che $a^2x_{0}^2+b^2y_{0}^2=c^2$, la retta passante per $O$ e $(x_{0},y_{0},1)$ ha equazioni parametriche:

							$\begin{cases}x=tx_{0} \\  y=ty_{0} &\mbox{t}\in\mathbb{R} & \\  z=t\end{cases}$

e giace interamente sulla quadrica, in quanto:

			$a^2x^2+b^2y^2=a^2(tx_{0})^2+b^2(ty_{0})^2=t^2(a^2x_{0}^2+b^2y_{0}^2)=t^2c^2=c^2z^2$

Pertanto la superficie coincide con l'unione delle rette passanti per l'origine e i punti dell'ellisse $(ax^2+b^2y^2=c^2)$, ossia è un <u>cono avente tale ellisse come generatrice</u>.

Se invece i tre coefficienti $a_{11},a_{22},a_{33}$ hanno tutti lo stesso segno, l'equazione si può riscrivere nella forma:

							$a^2x^2+b^2y^2+c^2z^2=0\quad(a,b,c>0)$


ed è evidentemente soddisfatta solo da $O=(0,0,0)$. In questo caso quindi la quadrica degenere <u>si riduce a un punto</u>. Per analogia col caso precedente (cono a due falde) si parla anche di <u>cono immaginario</u>.

Occupiamoci ora delle quadriche a centro non degeneri, ossia del tipo $a_{11}x^2+a_{22}y^2+a_{33}z^2+a_{44}=0$ con tutti i coefficienti $\ne 0$, che quindi dividendo per $a_{44}$ si possono riscrivere come:

								$\alpha x^2+\beta y^2+\gamma z^2=1$

Le uniche differenze importanti dipendono dai segni dei coefficienti $\alpha,\beta,\gamma$: ciò che conta è semplicemente quanti di essi sono positivi (quali in dettaglio è solo una questione di nomi dati alle variabili). Le possibilità sono quindi quattro, a seconda che il numero di coefficienti positivi sia $3,2,1,0$. In corrispondenza di questi casi si ottengono rispettivamente le seguenti equazioni canoniche:

$\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=1$ (<mark class="hltr-yellow">ellissoide reale</mark>)
$\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}=1$ (<mark class="hltr-yellow">iperboloide a una falda</mark>)
$\frac{x^2}{a^2}-\frac{y^2}{b^2}-\frac{z^2}{c^2}=1$ (<mark class="hltr-yellow">iperboloide a due falde</mark>)
$\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=-1$ (<mark class="hltr-yellow">ellissoide immaginario</mark>)

per opportuni $a,b,c>0$.
Descriviamo ora brevemente tali superfici:

- **Ellissoide reale**: il modo più semplice di capire la forma di questa superficie è pensare che si può ottenere da una superficie sferica eseguendo una dilatazione di fattore diverso su ogni asse: $x=ax',y=by',z=cz'$, che dà all'ellissoide la forma di una "sfera allungata".
	I numeri $a,b,c$ sono i <u>semiassi</u> dell'ellissoide, che ha per <u>vertici</u> i punti $(\pm a,0,0),(0,\pm b,0),(0,0,\pm c)$. Se due dei tre semiassi sono uguali tra loro l'ellissoide è di rotazione: *ad esempio*, per $a=b$, la superficie taglia i piani $z=z_{0}$ (quando $|z_{0}|<c$) lungo le circonferenze:
						
								$x^2+y^2=a^2\left( 1-\frac{z_{0}^2}{c^2} \right)$
	
	pertanto la superficie si può vedere ottenuta facendo ruotare attorno all'asse $z$ l'ellisse (nel piano $xz$) $\frac{x^2}{a^2}+\frac{z^2}{c^2}=1$. Se tutti e tre i semiassi sono uguali, la superficie è una sfera di raggio $r$.


- **Iperboloide a una falda**: si osserva che la superficie taglia qualsiasi piano $z=z_{0}$ lungo l'ellisse:
								$\frac{x^2}{a^2}+\frac{y^2}{b^2}=1+\frac{z_{0}^2}{c^2}$
	
	I semiassi delle sezioni ellittiche crescono al crescere di $|z_{0}|$. La superficie è illimitata e connessa (cioè "formata da un pezzo solo", motivo per cui si dice a una falda).
	In particolare, per $a=b$ l'ellisse è una circonferenza e la quadrica è di rotazione, ottenuta facendo ruotare attorno all'asse $z$ l'iperbole $\frac{x^2}{a^2}-\frac{z^2}{c^2}=1$ nel piano $xz$ (da cui il nome iperboloide). Sezionando invece la superficie con un piano contenente l'asse $z$, ossia del tipo $\alpha x+\beta y=0$, si ottiene un'iperbole, come si verifica facilmente.
	Un particolarità di questa superficie è di <u>contenere due famiglie di rette</u>. Infatti, riscrivendo l'equazione nella forma:
	
								$\frac{x^2}{a^2}-\frac{z^2}{c^2}=1-\frac{y^2}{b^2}$
	
	si osserva che le due famiglie di rette:
	
	$\begin{cases}\frac{x}{a}+\frac{z}{c}=h\left( 1+\frac{y}{b} \right) \\  \frac{x}{a}-\frac{z}{c}\left( \frac{1}{h}\left( 1-\frac{y}{b} \right) \right)\end{cases}\quad$ e $\quad \begin{cases} \frac{x}{a}+\frac{z}{c}=h\left( 1-\frac{y}{b} \right) \\  \frac{x}{a}-\frac{z}{c}=\frac{1}{h}\left( 1+\frac{y}{b} \right) \end{cases}$

	(al variare di $h\in\mathbb{R}$), sono contenute nella superficie stessa, come si verifica moltiplicando membro a membro le due equazioni di ciascun sistema. Per questa ragione si dice che l'iperboloide a una falde è una **superficie rigata**. Precisamente:


- #PROPOSIZIONE(16). Le due famiglie di rette che giacciono sull'iperboloide a una falda hanno le seguenti proprietà:

	a) per ogni punto della superficie passano esattamente una retta della prima famiglia e una della seconda;
	b) due rette qualsiasi della stessa famiglia sono sghembe;
	c) ogni retta della prima famiglia interseca ogni retta della seconda famiglia.


- **Iperboloide a due falde**: riscrivendo l'equazione nella forma:
	
								$\frac{x^2}{a^2}-1=\frac{y^2}{b^2}+\frac{z^2}{c^2}$
	
	si osserva che la superficie è contenuta nelle regioni in cui $\frac{x^2}{a^2}-1\ge 0$, ossia nelle due regioni separate $x\ge a$ e $x\le-a$. Perciò la superficie consiste in <u>due falde distinte</u>.
	Più precisamente, la superficie è contenuta nella regione:
	
								$\frac{y^2}{b^2}+\frac{z^2}{c^2}<\frac{x^2}{a^2}$
	
	(come segue dal fatto che $\frac{x^2}{a^2}-1<\frac{x^2}{a^2}$), che rappresenta una delle due regioni in cui il cono a due falde:
	
								$\frac{y^2}{b^2}+\frac{z^2}{c^2}=\frac{x^2}{a^2}$
	
	divide lo spazio (precisamente, la regione contente l'asse del cono).
	Questo cono si dice <u>cono asintotico</u>, perchè la superficie si avvicina indefinitamente ad esso così come un'iperbole si avvicina ai suoi asintoti. Tagliando la superficie con un piano $x=x_{0}$ (per $|x_{0}|>a$) si trova l'ellisse:
	
								$\frac{y^2}{b^2}+\frac{z^2}{c^2}=\frac{x_{0}^2}{a^2}-1$
	
	In particolare se $b=c$ quest'ellisse è una circonferenza e la quadrica è di rotazione, ottenuta facendo ruotare attorno all'asse $x$ l'iperbole:
	
									$\frac{x^2}{a^2}-\frac{y^2}{b^2}=1$
	
	(nel piano $xy$). Tagliano invece la superficie con un piano contenente l'asse $x$, cioè del tipo $\alpha y+\beta z=0$, si ottiene sempre un'iperbole, i cui asintoti giacciono sul cono asintotico, come si verifica facilmente. A differenza dell'iperboloide a una falda, <u>l'iperboloide a due falde non è una superficie rigata</u>.


- **Ellissoide immaginario**: si vede subito che l'equazione:
	
								$\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=-1$
	
	non è soddisfatta da alcuna terna $(x,y,z)$ di numeri reali, quindi nello spazio $\mathbb{R}^3$ rappresenta l'insieme vuoto. Per analogia con l'ellissoide reale, la superficie è detta appunto ellissoide immaginario.



### 8.3 **Riduzione a forma canonica delle quadriche: quadriche non a centro**

Consideriamo ora le quadriche non a centro, ossia quelle per cui risulta $\mathcal{I}_{3}=0$.
In tal caso, non sempre esiste una traslazione che elimini i termini di primo grado; possiamo in compenso diagonalizzare subito la matrice $\mathbf{B}$, ossia effettuare un'opportuna rotazione di assi che elimini i termini $a_{12},a_{23},a_{13}$.
Dopo questa **rotazione** l'equazione della quadrica non a centro risulta quindi del tipo:

				$a_{11}x^2+a_{22}y^2+a_{33}z^2+2a_{14}x+2a_{24}y+2a_{34}z+a_{44}=0$

inoltre, $\mathcal{I}_{3}=a_{11}a_{22}a_{33}=0$, quindi almeno uno dei coefficienti $a_{11},a_{22},a_{33}$ si annulla.
*Ad esempio*, supponiamo $a_{33}=0$; la matrice dei coefficienti è quindi:

$\mathbf{A}=\begin{pmatrix}a_{11} & 0 & 0 & a_{14} \\  0 & a_{22} & 0 & a_{24} \\  0 & 0 & 0 & a_{34} \\  a_{14} & a_{24} & a_{34} & a_{44}\end{pmatrix}$

Notiamo che $\mathcal{I}_{4}=-a_{11}a_{22}a_{34}^2$.

Studiamo prima il caso della <u>quadrica non a centro e non degenere</u>; quindi $\mathcal{I}_{4}\ne 0$ e i coefficienti $a_{11},a_{22},a_{34}$ sono effettivamente diversi da $0$.

Cerchiamo una **traslazione** che annulli i coefficienti $a_{14},a_{24}$. Dal [[#8.1 **Rototraslazioni nello spazio e invarianti di una quadrica**|sistema]]:

${\begin{cases}a_{14}'=a_{11}u+a_{12}v+a_{13}w+a_{14} \\  a_{24}'=a_{12}u+a_{22}v+a_{23}w+a_{24} \\  a_{34}'=a_{13}u+a_{23}v+a_{33}w+a_{34} \\  a_{44}'=a_{11}u^2+a_{22}v^2+a_{33}w^2+2a_{12}uv+2a_{13}uw+2a_{23}uw+2a_{14}+2a_{24}+2a_{34}+a_{44}\end{cases}}$

leggiamo che questo significa risolvere il sistema in $u,v$ (in altre parole, la traslazione non agisce sulla terza variabile):

$\begin{cases}a_{11}u+a_{14}=0 \\  a_{22}v+a_{24}=0\end{cases}$

il che è immediato perchè stiamo supponendo $a_{11},a_{22}\ne 0$. Arriviamo quindi alla quadrica di equazione:

						$a_{11}x^2+a_{22}y^2+2a_{34}z+a_{44}=0$

Infine la traslazione $z=z'+w$ elimina il termine noto $a_{44}$ scegliendo $w=-\frac{a_{44}}{2a_{34}}$.
Le generica quadrica non a centro non degenere ha quindi equazione:

						$a_{11}x^2+a_{22}y^2+2a_{34}z+=0$

Le superfici sostanzialmente diverse si ottengono al variare dei segni dei tre coefficienti, secondo i seguenti due soli casi:

a) $a_{11},a_{22}$ <u>concordi</u>. L'equazione canonica è: $\frac{x^2}{a^2}+\frac{y^2}{b^2}=2pz$
	per opportuni $a,b,p>0$ (se $p<0$ la superficie si ottiene dalla precedente semplicemente ribaltando l'asse $z$);

b) $a_{11},a_{22}$ <u>discordi</u>. L'equazione canonica è $\frac{x^2}{a^2}-\frac{y^2}{b^2}=2pz$
	per opportuni $a,b,p>0$.

Studiamo quindi queste due superfici, che sono rispettivamente:

- **Paraboloide ellittico**: la superficie è contenuta nel semispazio $z>0$, e taglia ogni piano $z=z_{0}$ (con $z_{0}>0$) lungo l'ellisse:
	
								$\frac{x^2}{a^2}+\frac{y^2}{b^2}=2pz_{0}$
	
	Se $a=b$ quest'ellisse è una circonferenza e la quadrica è di rotazione, ottenuta facendo ruotare attorno all'asse $z$ la parabola $\frac{x^a}{a^2}=2pz$ (nel piano $xz$).
	Tagliando invece la superficie con un piano contenente l'asse $z$, cioè del tipo $\alpha x+\beta y=0$ si trova sempre una parabola avente per asse l'asse $z$ e per vertice $O$; si dice pertanto che l'origine è il vertice del paraboloide e l'asse $z$ il suo asse.


- **Paraboloide iperbolico** (detto anche **sella**): tagliando la superficie con un qualsiasi piano $z=z_{0}$ ($z_{0}\ne 0$) si trova un'iperbole:
	
								$\frac{x^2}{a^2}-\frac{y^2}{b^2}=2pz_{0}$
	
	- per $z_{0}>0$ è del tipo: $\frac{x^2}{A^2}-\frac{y^2}{B^2}=1$
	- per $z_{0}<0$ è del tipo: $\frac{x^2}{A^2}-\frac{y^2}{B^2}=1$
	
	Il piano $z=0$ taglia la superficie lungo le due rette $y=\pm \frac{b}{a}x$, ed è illimitata e connessa.
	Se $a=b$ l'iperbole è equilatera; in ogni caso la quadrica <u>non è una superficie di rotazione</u>.
	Tagliando la superficie con un piano contenente l'asse $z$, cioè del tipo $\alpha x+\beta y=0$, si ottiene sempre una parabola, che però a seconda della direzione del piano di sezione è concava verso l'alto o verso il basso.
	Come l'iperboloide a una falda anche il paraboloide iperbolico è una **superficie rigata**, in quanto contiene le due famiglie di rette:
	
	$\begin{cases} \frac{x}{a}+\frac{y}{b}=2hpz \\  \frac{x}{a}-\frac{y}{b}=\frac{1}{h} \end{cases}\quad$ e $\quad\begin{cases} \frac{x}{a}+\frac{y}{b}=-2hpz \\  \frac{x}{a}-\frac{y}{b}=-\frac{1}{h} \end{cases}$
	
	(al variare di $h\in \mathbb{R}$), come si verifica moltiplicando membro a membro le due equazioni di ciascun sistema.
	Precisamente, valgono ancore le proprietà espresse nella #PROPOSIZIONE(16).


Dobbiamo ancora considerare le <u>quadriche non a centro e degeneri</u>, ossia quelle aventi matrice dei coefficienti $\mathbf{A}=\begin{pmatrix}a_{11} & 0 & 0 & a_{14} \\  0 & a_{22} & 0 & a_{24} \\  0 & 0 & 0 & a_{34} \\  a_{14} & a_{24} & a_{34} & a_{44}\end{pmatrix}$ ma $\mathcal{I}_{4}=-a_{11}a_{22}a_{34}^2=0$.

Senza stare a illustrare in dettaglio i vari passi della riduzione a forma canonica, limitiamoci a descrivere in questo caso le situazioni essenzialmente distinte che si possono presentare.
La superficie può essere un **cilindro** o una **quadrica spezzata**.
Per cilindro (in senso lato) si intende una superficie formata da tutte le rette parallele a un certo asse fissato e passanti ciascuna per un punto di una curva fissata, che definisce la <u>sezione</u> del cilindro:

| Cilindri (con asse parallelo all'asse $z$) |                                                   |
| ------------------------------------------ | ------------------------------------------------- |
| $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$        | **cilindro ellittico** (cioè a sezione ellittica) |
| $\frac{x^2}{a^2}-\frac{y^2}{b^2}=1$        | **cilindro iperbolico**                           |
| $x^2=2py$                                  | **cilindro parabolico**                           |
| $\frac{x^2}{a^2}+\frac{y^2}{b^2}=-1$       | **cilindro immaginario** ($\emptyset$)            |


Le quadriche non a centro e spezzate sono invece le seguenti:

| Quadriche spezzate                  |                                                                                                 |
| ----------------------------------- | ----------------------------------------------------------------------------------------------- |
| $\frac{x^2}{a^2}-\frac{y^2}{b^2}=0$ | due piani (reali, $y=\pm \frac{b}{a}x$), incidenti su una retta (asse $z$)                      |
| $\frac{x^2}{a^2}+\frac{y^2}{b^2}=0$ | due piani complessi coniugati ($y=\pm i \frac{b}{a}x$), incidenti su una retta reale (asse $z$) |
| $x^2-a^2=0$                         | due piani paralleli reali ($x=\pm a$)                                                           |
| $x^2+a^2=0$                         | due piani immaginari ($x=\pm ia$) $\to \emptyset$                                               |
| $x^2=0$                             | un piano ($x=0$)                                                                                |

Si osservi che anche le quadriche spezzate, a rigore, soddisfano la definizione che abbiamo dato di cilindro (consistono tutte di rette parallele ad una asse); solitamente si riserva il nome di cilindro alle superfici che non si spezzano in piani.



### 8.4 **Riconoscimento di una quadrica mediante gli invarianti**

Nel paragrafo precedente abbiamo passato in rassegna tutti i casi possibili, ottenendo quindi una classificazione completa delle quadriche. È utile a questo punto riepilogare i casi ottenuti, calcolando in ciascuno di essi gli invarianti della quadrica, al fine di poter poi procedere in senso inverso, ossia: data l'equazione di una quadrica qualsiasi, dal calcolo degli invarianti risalire immediatamente al tipo di quadrica.
Il prossimi schema riassume gli elementi utili al riconoscimento delle quadriche in base agli invarianti.

La prima distizione da fare è:

A) $\mathcal{I}_{4}\ne 0 \implies$ **quadrica non degenere**;
B) $\mathcal{I}_{4}= 0 \implies$ **quadrica degenere**.


(A) **Riconoscimento delle quadriche non degeneri ($\mathcal{I}_{4}\ne 0$)**:

- $\mathcal{I}_{3}\ne 0 \implies$ quadrica non degenere **a centro**
	
	Esistono quattro tipi, che si riconoscono in base al segno dell'invariante $\mathcal{I}_{4}$ e alle relazioni tra i segni degli autovalori di $\mathbf{B}$ (si ricordi che se $\mathbf{B}$ è diagonale, come accade quanto l'equazione della quadrica è in forma canonica, i suoi autovalori sono semplicemente gli elementi sulla diagonale):

|                                     | $\mathcal{I}_{4}<0$         | $\mathcal{I}_{4}>0$         |
| ----------------------------------- | --------------------------- | --------------------------- |
| Autovalori di $\mathbf{B}$ concordi | **ellissoide reale**        | **ellissoide immaginario**  |
| Autovalori di $\mathbf{B}$ discordi | **iperboloide a due falde** | **iperboloide a una falda** |

- $\mathcal{I}_{3}= 0 \implies$ quadrica non degenere **non a centro**
	
	Esistono due tipi:

| $\mathcal{I}_{4}<0$   | $\mathcal{I}_{4}>0$    |
| --------------------- | ---------------------- |
| **paraboloide ellittico** | **paraboloide iperbolico** |


(B) **Riconoscimento delle quadriche degeneri ($\mathcal{I}_{4}= 0$)**:

- $\mathcal{I}_{3}\ne 0 \implies$ cono, precisamente:

|                                     |                                       |
| ----------------------------------- | ------------------------------------- |
| Autovalori di $\mathbf{B}$ concordi | **cono immaginario** (un punto reale) |
| Autovalori di $\mathbf{B}$ discordi | **cono reale** (a sezione ellittica)  |

- $\mathcal{I}_{3}= 0 \implies$ cilindro o una quadrica spezzata, precisamente:

|                    | Gli autovalori di $\mathbf{B}$ sono:           |                         |                                                    |
| ------------------ | ---------------------------------------------- | ----------------------- | -------------------------------------------------- |
|                    | uno nullo, due concordi                        | uno nullo, due discordi | due nulli                                          |
| $car \mathbf{A}=3$ | cilindro ellittico o immaginario ($\emptyset$) | cilindro iperbolico     | cilindro parabolico                                |
| $car \mathbf{A}=2$ | 2 piani immaginari incidenti (una retta reale) | 2 piani reali incidenti | 2 piani paralleli/2 piani immaginari ($\emptyset$) |
| $car \mathbf{A}=1$ |                                                |                         | un piano reale                                     |

Per distinguere tra loro il caso del cilindro reale o immaginario (o tra due piani reali o immaginari) la cosa più semplice solitamente è cercare almeno un punto reale che soddisfi l'equazione.


*Esempio*: Riconoscere le seguenti quadriche:

a) $xy+z^2+1=0$
b) $x^2-y^2+4z^2-4xz-z+3=0$
c) $x^2+y^2+z^2+2xy-3=0$

(a) La matrice dei coefficienti è: $\mathbf{A}=\begin{pmatrix}0 & \frac{1}{2} & 0 & 0 \\  \frac{1}{2} & 0 & 0 & 0 \\  0 & 0 & 1 & 0 \\  0 & 0 & 0 & 1\end{pmatrix}$

da cui: $\mathcal{I}_{4}=-\frac{1}{4}<0,\quad\mathcal{I}_{3}=-\frac{1}{4}\ne 0$

(quadrica non degenere a centro).
Poichè $\det \mathbf{A}<0$ si tratta di una ellissoide reale o di un iperboloide a due falde.
Per decidere calcoliamo gli autovalori di $\mathbf{B}$:

$\det(\mathbf{B}-\lambda \mathbf{I})=(1-\lambda)\left( \lambda^2-\frac{1}{4} \right)=0 \implies\lambda_{1}=1,\lambda_{2}=\frac{1}{2},\lambda_{3}=-\frac{1}{2}$

Poichè gli autovalori sono discordi, si tratta di un iperboloide a due falde.


(b) La matrice dei coefficienti è: $\mathbf{A}=\begin{pmatrix}1 & 0 & -2 & 0 \\  0 & -1 & 0 & 0 \\  -2 & 0 & 4 & -\frac{1}{2} \\  0 & 0 & -\frac{1}{2} & 3\end{pmatrix}$

da cui: $\mathcal{I}_{4}>0,\quad\mathcal{I}_{3}=0$

(quadrica non degenere non a centro).
Poichè $\det \mathbf{A}>0$ si tratta di un paraboloide iperbolico.


(c) La matrice dei coefficienti è: $\mathbf{A}=\begin{pmatrix}1 & 1 & 0 & 0 \\  1 & 1 & 0 & 0 \\  0 & 0 & 1 & 0 \\  0 & 0 & 0 & -3\end{pmatrix}$

da cui: $\mathcal{I}_{4}=0,\quad\mathcal{I}_{3}=0$

(quadrica degenere, cilindro o spezzata).
Per decidere, osserviamo che:

$Car\mathbf{A}=3$ in quanto $\begin{vmatrix}1 & 0 & 0 \\  0 & 1 & 0 \\  0 & 0 & -3\end{vmatrix}\ne 0$

quindi si tratta di un cilindro. Per determinarne il tipo, calcoliamo gli autovalori di $\mathbf{B}$:

$\det$