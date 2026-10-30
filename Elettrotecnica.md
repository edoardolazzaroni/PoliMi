
# **Capitolo I: Il modello circuitale**


## 1.1 **Sistemi elettrici e loro modelli**

In questo corso, acquisiremo la capacità di eseguire l’analisi dei sistemi elettrici. Dalla descrizione di un dato sistema in termini di elementi che lo compongono e di come sono connessi tra di loro, impareremo una metodologia generale per calcolare il valore delle grandezze elettriche che lo descrivono e con esse a capire come funziona e a che cosa serve. L’obiettivo verrà raggiunto diventando padroni di un modello matematico fondamentale dell’Ingegneria chiamato il **modello circuitale**.

Va precisato che il termine di sistema elettrico può riferirsi a realtà fisiche molto diverse tra loro e tutte fondamentali per la preparazione dell’Ingegnere dell’area ICT (Information and Communication Technology). Facciamo degli esempi._

- Un primo tipo di sistema elettrico è rappresentato dalla rete di trasporto/distribuzione dell’energia elettrica. Questa è formata da un insieme di fili di rame, chiamati conduttori, che collegano punti in cui l’energia viene prodotta (*es*: le centrali elettriche, impianti fotovoltaici...) ai punti in cui viene utilizzata (*es*: le nostre abitazioni, gli impianti industriali, le linee di trasporto metropolitano o dei treni). Tali reti hanno dimensioni dell’ordine delle centinaia di chilometri dato che si possono estendere su tutto il territorio di una nazione.
- Un secondo esempio, altrettanto rilevante, è rappresentato dai sistemi della micro e nano elettronica. Questo secondo esempio di rete non ha lo scopo di trasportare energia bensì di elaborare l’informazione. L’energia elettrica nel primo esempio e l’informazione nel secondo sono rappresentate (o determinate) da alcune grandezze fisiche misurabili chiamate <u>grandezze descrittive</u>.

Nonostante la spaventosa differenza di scala geometrica tra una rete per l’energia e un processore elettronico il comportamento elettrico di questi sistemi può venire descritto dallo stesso modello circuitale. La tecnica di modeling, cioè la costruzione del modello, si basa sull’identificazione delle grandezze fisiche descrittive che chiameremo **TENSIONE** e **CORRENTE** elettrica e sulla scrittura delle leggi che le governano. Nel modello, le grandezze fisiche sono sostituite da variabili matematiche (indicate $v, i$) mentre le leggi fisiche si traducono in equazioni che legano tali variabili, come mostrato in figura:

![[Elettrotecnica-1792681850745.webp|281]]
#Figura (1.1). *Il processo di modeling*


D’altra parte, è importante fin da subito sottolineare che, sebbene molto potente, il modello circuitale, al pari di ogni modello dell’Ingegneria, è in grado di cogliere solo alcuni aspetti della realtà fisica che vuole rappresentare. Come tale esso ha dei limiti di validità. Per questo motivo è importante non solo apprenderne l’uso ma anche saper riconoscere i suoi limiti di applicazione.



## 1.2 **Le grandezze descrittive: tensione e corrente**

Gli uomini hanno imparato a descrivere e dominare i fenomeni elettrici ammettendo che essi siano dovuti ad una proprietà della materia chiamata carica elettrica. La carica elettrica si manifesta in quanto i corpi che la possiedono esercitano l’un l’altro delle interazioni (cioè delle forze). Esistono due tipi distinti di carica elettrica, indicati convenzionalmente come cariche di tipo positivo e di tipo negativo. Tra cariche elettriche dello stesso tipo si misura una forza che tende a respingerle mentre tra cariche di tipo opposto tale forza è di tipo attrattivo.
![[Elettrotecnica-1792683598892.webp|228]]
#Figura(1.2). *Azioni tra cariche puntiformi*

La figura mostra qualitativamente le forze che si esercitano tra cariche puntiformi, cioè le cui dimensioni siano trascurabili.

Gli atomi che formano la materia sono composti da particelle che possiedono sia carica positiva che negativa in egual numero e che tendono quindi a neutralizzare vicendevolmente gli effetti.
Questo fa si che a livello macroscopico i corpi materiali non manifestano particolari effetti elettrici. Per “scatenare” tali fenomeni è necessario che, attraverso una qualche azione, alcune cariche dello stesso tipo siano in eccesso nel corpo in modo da prevalere su quelle di tipo opposto. È allora evidente che per sottrarre/apportare alcune cariche al corpo è necessario applicare una forza che vinca la forza di tipo attrattivo/repulsivo, rispettivamente, che le lega alle altre cariche del corpo, cioè è necessario compiere un lavoro. Un primo aspetto comune a tutti i fenomeni elettrici è che affinché essi si manifestino deve esistere un’azione attraverso cui si separano cariche elettriche di tipo opposto eseguendo un lavoro.

Il primo esperimento in cui l’elettrizzazione della materia fu condotta in modo controllato e ripetibile, fu quello eseguito da Alessandro Volta alla fine del 1799 quando riuscì a costruire il primo esempio di pila elettrica. La **pila di Volta** è composta da dischi di rame e zinco disposti in modo alternato uno sull’altro interponendo tra loro una spugna imbevuta in una soluzione di acido (solforico).
![[Elettrotecnica-1792683805443.webp|346]]
#Figura(1.3). *Il circuito con la pila di Volta*

Per effetto della reazione chimica che ha luogo tra i due metalli, alcuni atomi con un eccesso di carica positiva, detti ioni positivi, vengono spostati verso un capo della pila mentre contemporaneamente ioni negativi si spostano al capo opposto. In questo modo dunque il lavoro proveniente dalla reazione chimica si trasforma nel lavoro elettrico necessario per attuare la separazione delle cariche. Volta si accorse che quando due fili metallici collegati agli estremi della pila venivano impugnati si avvertiva la sensazione di essere attraversati da un fluido, una sensazione che oggi potremmo definire "elettrizzante".

Alla luce delle nostre conoscenze oggi sappiamo che ciò accade perché le cariche positive e negative separate dal lavoro chimico della pila si ricongiungono muovendosi lungo il cammino che si viene a formare lungo i due conduttori metallici e l’uomo che li impugna. Si viene così a formare un circuito chiuso lungo cui le cariche si mettono in movimento dando vita ad una circolazione continua (o flusso) di carica. Convenzionalmente si attribuisce a tale circolazione il verso del movimento delle cariche positive.

L’esperimento mette in luce due aspetti della manifestazione elettrica:

a) esiste un dispositivo, la pila, che funziona come generatore del fenomeno elettrico in quanto è in grado di separare cariche di segno opposto svolgendo un lavoro;
b) si instaura un movimento continuo di cariche elettriche lungo un percorso chiuso.

L’esperimento della pila di Volta rappresenta un <mark class="hltr-yellow">caso elementare di circuito elettrico</mark> e ad ognuno dei due aspetti fondamentali dell’esperimento, lavoro elettrico e movimento di cariche, siamo in grado di associare una grandezza elettrica descrittiva del fenomeno.


La **tensione** elettrica è una grandezza fisica associata ad una linea $\gamma$ orientata nello spazio, cioè su cui è stato fissato un verso di percorrenza, che congiunge due punti A e B.

> [!important] Definizione
> Chiamiamo tensione elettrica lungo la linea $\gamma$ e la indichiamo come $V(\gamma)$ il lavoro elettrico che noi dobbiamo compiere in antagonismo alle forze elettriche per muovere lungo tale linea una carica di prova positiva e unitaria. L’unità di misura della tensione è il volt $[V]$, dal nome dell’inventore della pila.


Chiaramente il lavoro da noi svolto sarà positivo se il movimento della carica di prova avviene effettivamente in opposizione alle forze elettriche che agiscono su di essa oppure sarà negativo (cioè non svolto da noi ma assorbito) se il movimento avviene concordemente alle forze elettriche. Pertanto la tensione elettrica è una <u>grandezza dotata di segno</u>.
![[Elettrotecnica-1792684263435.webp|209]]
#Figura(1.4). *La tensione elettrica lungo la linea $\gamma$ è indicata come $V(\gamma)$*



Per definire la seconda grandezza elettrica, si supponga di voler misurare il flusso di carica all’interno del filo metallico. A tale proposito si taglia il filo venendo a formare la superficie sezione $\sigma$.
![[Elettrotecnica-1792684407984.webp|412]]
#Figura(1.5). *Il filo viene sezionato identificando così la sezione $\sigma$ di cui si deve scegliere un verso di attraversamento.*

Si fissa arbitrariamente un verso di attraversamento come positivo che induce un orientiamo della superficie $\sigma$ e si conta la quantità netta di carica positiva che attraversa la superficie.

> [!important] Definizione
> La corrente elettrica in un mezzo conduttivo (cioè che ne consente la circolazione) è una grandezza descrittiva associata ad una superficie $\sigma$ orientata, che indichiamo come $I(\sigma)$, definita come la quantità di carica elettrica netta che attraversa la sezione nell’unità di tempo.
> L’unità di misura della corrente è chiamata ampere $[A]$, in onore del fisico francese che la studiò.


L’aggettivo <u>netta</u> si riferisce al fatto che in un dato istante di osservazione la superficie in esame potrebbe essere attraversata da una carica $Q_{1}$ che si muove concorde col verso di orientazione assunto ed una carica $Q_{2}$ che invece si muove in senso opposto. La carica netta in questo caso è data da $Q_{1}−Q_{2}$.

Anche il valore della corrente è <u>dotato di segno</u>, ad indicare se il flusso netto di carica è concorde o discorde rispetto al senso di attraversamento fissato sulla superficie.


### 1.2.1 **Gli strumenti di misura**

Per potere rilevare operativamente le grandezze tensione e corrente sono stati costruiti appositi strumenti di misura che chiamiamo <u>voltmetro</u> ed <u>amperometro</u>.

I due strumenti sono composti da un organo di lettura che fornisce il valore della grandezza in modo digitale o analogico, due morsetti contraddistinti dal segno “più” e “meno” e una coppia di cordoni terminanti in due puntali metallici. I cordoni costituiscono la sonda dello strumento e cioè l’ente geometrico lungo cui o attraverso cui si esegue la misura. Per la misura di tensione i cordoni del voltmetro costituiscono la linea $\gamma$ come mostrato in figura. Si noti che il verso di misura indotto sulla linea è quello che entra dal morsetto “meno” ed esce dal “più”.
![[Elettrotecnica-1792685313603.webp|211]]
#Figura(1.6). *Misura della tensione: i cordoni del voltmetro definiscono la linea lungo cui avviene la misura*


La misura di corrente richiede che il filo metallico in cui scorre il flusso di cariche venga sezionato lungo $\sigma$ come mostrato in figura e che i puntali dell’amperometro si appoggino sulle due facce che si vengono a formare (cfr figura 1.11). In questo caso, l’orientamento indotto sulla superficie $\sigma$ è il verso di attraversamento che va dal morsetto “più” al morsetto “meno” dell’amperometro.
![[Elettrotecnica-1792685397278.webp|260]]
#Figura(1.7). *Misura della corrente: il morsetto “più” e il morsetto “meno” dell’amperometro definiscono l’orientamento della superficie $\sigma$*


Osserviamo che da un punto di vista matematico, le misure di tensione o di corrente istituiscono una relazione che ad un ente geometrico astratto fa corrispondere uno ed un solo numero reale (dotato di segno). Si dirà allora, ad esempio, che lungo una certa linea orientata $v_{i}$ è una tensione di $−2.1 \ V$ o di $5.0 \ V$ o che la corrente che attraversa una certa superficie orientata vale $0.5 \ A$ o $−3 \ mA$.


### 1.2.2 **Proprietà della tensione e della corrente**

L’uso del voltmetro e dell’amperometro mostra che la misura di tensione e quella di corrente godono della proprietà di essere **dispari** e della proprietà **additiva**.
Vediamo dette proprietà esaminando per primo il caso della tensione e poi quello della corrente.


- #### **Proprietà della tensione**:

Indichiamo con $\gamma$ una linea orientata diretta dal punto $A$ al punto $B$ e con $−\gamma$ la stessa linea ma orientata nel verso opposto, cioè che va da $B$ ad $A$, come mostrato in figura.![[Elettrotecnica-1793026797692.webp|237]]
#Figura(1.8). *Inversione dell'orientamento di una linea*

Operativamente la misura di tensione lungo $−\gamma$ si ottiene invertendo l’inserimento dei morsetti del voltmetro. Vale la **proprietà di disparità**, ovvero:
$$V(−\gamma) =−V(\gamma)$$
La disparità ha l’ovvio significato che il lavoro svolto per spostare la carica di prova da $A$ a $B$ è lo stesso in modulo ma opposto in segno a quello che si svolge per spostarla da $B$ ad $A$.

Ora consideriamo le linee orientate $\gamma_{1}$ che va da $A$ a $B$ e $\gamma_{2}$ che va da $B$ a $C$. La loro unione dà origine alla linea complessiva $\gamma= \gamma_{1} \cup \gamma_{2}$ che va da $A$ a $C$. Sia $v_{1} = V(\gamma_{1})$ la tensione misurata lungo $\gamma_{1}$ e $v_{2} = V(\gamma_{2})$ la tensione misurata lungo $\gamma_{2}$. Indichiamo poi con $V(\gamma)$ la misura lungo la linea complessiva. Vale allora la **proprietà additiva** della tensione:
$$V(\gamma) = V(\gamma_{1} \cup \gamma_{2}) = V(\gamma_{1}) + V(\gamma_{2}) = v_{1} + v_{2}$$
![[Elettrotecnica-1793026884117.webp|282]]
#Figura(1.9). *$\gamma=\gamma_{1}\cup \gamma_{2}$*

<u>Combiniamo ora le due proprietà</u> e consideriamo le tre linee $\gamma_{1}, \gamma_{2}, \gamma_{3}$ orientate come mostrato in figura (cioè con $\gamma_{2}$ orientata in modo discorde alle altre) e la linea unione $\gamma= \gamma_{1} \cup (-\gamma_{2}) \cup \gamma_{3}$. Abbiamo eseguito le relative misure di tensione $v_{1} = V(\gamma_{1}), v_{2} = V(\gamma_{2})$ e $v_{3} = V(\gamma_{3})$. Dalla proprietà di disparità si ha che $V(−\gamma_{2}) =−v_{2}$ e dunque applicando la proprietà di additività concludiamo che:
$$v(\gamma) = V(\gamma_{1} \cup (−\gamma_{2}) \cup \gamma_{3}) = v_{1} − v_{2} + v_{3}$$
![[Elettrotecnica-1793026990833.webp|282]]
#Figura(1.10). *$\gamma=\gamma_{1}\cup(-\gamma_{2})\cup \gamma_{3}$*

La misura di tensione lungo un cammino orientato è dato dalla somma algebrica (cioè con segno) delle misure eseguite lungo i tratti parziali, prendendo con segno positivo le misure eseguite con orientamento concorde al cammino e con segno negativo le discordi.



- #### **Proprietà della variabile corrente**:

Sia $\sigma$ una superficie orientata come in [[#1.2.1 **Gli strumenti di misura**|figura 1.7]] e con $-\sigma$ la stessa superficie ma orientata nel verso opposto (figura 1.11).
![[Elettrotecnica-1793027627951.webp|244]]
#Figura(1.11). *La superficie $−\sigma$ è orientata nel verso opposto rispetto alla $\sigma$ in figura 1.7. Notate che l’orientamento della superficie è determinato dalla modalità di inserimento dei terminali dell’amperometro*

Operativamente, la misura di corrente lungo $−\sigma$ si ottiene invertendo l’inserimento dei morsetti dell’amperometro. Vale la **proprietà di disparità**:
$$I(−\sigma) =−I(\sigma)$$

Ora consideriamo le superfici $\sigma_{1}$ e $\sigma_{2}$, orientate in modo concorde e che condividono parte della loro frontiera. La loro unione dà origine alla superficie complessiva $\sigma = \sigma_{1}\cup \sigma_{2}$. Se $i_{1}= I(\sigma_{1})$ e $i_{2} = I(\sigma_{2})$ sono i valori delle misure delle correnti attraverso le superfici parziali mentre $i= I(\sigma)$ è la misura attraverso la superficie complessiva, la **proprietà additiva** delle correnti dice che:
$$i= I(\sigma) = I(\sigma_{1} \cup \sigma_{2}) = I(\sigma_{1}) + I(\sigma_{2}) = i_{1} + i_{2}$$

![[Elettrotecnica-1793027739783.webp|275]]
#Figura(1.12). *$\sigma=\sigma_{1}\cup \sigma_{2}$*

Infine siano $\sigma_{1}, \sigma_{2}, \sigma_{3}$ tre superfici orientate come in figura e cioè con $\sigma_{2}$ orientata in modo discorde alle prime due e sia $\sigma = \sigma_{1}\cup(−\sigma_{2})\cup \sigma_{3}$. Si sono eseguite le relative misure di corrente $i_{1}, i_{2}$ e $i_{3}$. Dalla proprietà di disparità si ha che $i(−\sigma_{2}) =−i_{2}$ e dall’additività che:
$$i= I(\sigma_{1}\cup(−\sigma_{2})\cup \sigma_{3}) = i_{1}−i_{2} + i_{3}$$

![[Elettrotecnica-1793027803553.webp|306]]
#Figura(1.13). *$\sigma = \sigma_{1}\cup(−\sigma_{2})\cup \sigma_{3}$*

La misura di corrente attraverso una superficie orientata è dato dalla somma algebrica (cioè con segno) delle misure eseguite attraverso le sottosuperfici parziali che la formano prendendo con segno positivo le misure eseguite con orientamento concorde e con segno negativo le discordi.


### 1.2.3 **Leggi delle tensioni e delle correnti**

Le grandezze fisiche tensione e corrente che misuriamo in un sistema elettrico possono variare nel tempo a seconda dello stato e del modo di funzionamento del sistema; per esempio è chiaro che all’accensione di una apparecchiatura elettrica si assiste a delle fasi transitorie in cui è naturale attendersi che le tensioni e le correnti varino nel tempo prima di raggiungere i valori desiderati. Tuttavia, nella prima parte del corso è lecito trascurare le fasi transitorie e concentrarsi sullo scenario in cui tutte le grandezze elettriche assumono valori costanti nel tempo. Chiamiamo questa condizione **Regime Stazionario** o anche funzionamento in continua (<u>indicato anche come DC</u>, "direct current"). 

In un sistema elettrico operante in regime stazionario, valgono rigorosamente le seguenti evidenze sperimentali:

- Si consideri una linea $\gamma$ chiusa, cioè tale che il punto di partenza e di arrivo coincidono come mostrato in figura 1.14:
	![[Elettrotecnica-1793029408509.webp|209]]
	#Figura(1.14). *Linea chiusa, ovvero il punto di partenza $A$ e di arrivo $B$ coincidono*
	
	L’evidenza mostra come la tensione elettrica misurata lungo tale linea vale $V(\gamma) = 0$.
	Supponiamo ora che tale linea chiusa sia composta dai percorsi parziali $\gamma_{1}, \gamma_{2}, \gamma_{3}, \gamma_{4}$, orientati come mostrato in figura 1.15, lungo cui si sono eseguite le relative misure parziali di tensione $v_{1} = V(\gamma_{1}), v_{2} = V(\gamma_{2}), v_{3} = V(\gamma_{3}), v_{4} = V(\gamma_{4})$.
	![[Elettrotecnica-1793029472172.webp|229]]
	#Figura(1.15). *La linea chiusa $\gamma$ è composta da quattro percorsi parziali*
	
	Muovendosi lungo $\gamma$ in senso orario e applicando la proprietà additiva e quella di disparità, si ottiene:
	$$v_{1}−v_{2}+v_{3}−v_{4} = 0$$

Generalizzando, possiamo quindi enunciare la seguente legge fondamentale:

> [!important] Definizione
> **Legge delle tensioni**: la somma algebrica (cioè tenendo conto dei segni) delle tensioni misurate lungo una linea $\gamma$ chiusa è uguale a zero.


Dalla legge delle tensioni discende un’altra importante conseguenza. Con riferimento alla figura seguente si considerino per iniziare le due linee $\gamma_{1}$ e $\gamma_{2}$ che partono dal punto $A$ e portano attraverso due percorsi alternativi al medesimo punto $B$.
![[Elettrotecnica-1793029657439.webp|297x215]]

#Figura(1.16). *Le linee in figura hanno gli stessi estremi e orientamento, cioè sono cammini che partono da $A$ e arrivano in $B$*

Per la legge delle tensioni applicata alla linea chiusa unione
$$\gamma_{1} \cup(−\gamma_{2})$$
si ottiene:
$$v_{1}−v_{2} = 0 \rightarrow v_{1} = v_{2}$$

Lo stesso ragionamento si estende alla linea $\gamma_{3}$ per cui $v_{1} = v_{3}$.
Questo indica che tensioni misurate lungo cammini diversi ma che collegano gli stessi punti estremi $A$ e $B$ hanno lo stesso valore.

**In regime stazionario dunque, la tensione dipende solo dagli estremi del cammino lungo cui è misurata ed è quindi lecito indicarla in modo sintetico come $v_{BA}$ intendendola come la tensione del punto $B$ rispetto al punto $A$**:
$$v_{1} = v_{2} = v_{3} = v_{BA}$$

- La seconda evidenza sperimentale che si registra in regime stazionario riguarda la variabile corrente. A tale proposito, consideriamo una superficie chiusa $\sigma$, ad esempio come mostrato nella figura seguente:
	![[Elettrotecnica-1793030001726.webp|187]]
	#Figura(1.17). *Esempio di superficie chiusa orientata $\sigma$. Il senso positivo di attraversamento è assunto quello che va dall’interno all’esterno*
	
	L’evidenza sperimentale mostra come la corrente che attraversa tale superficie è zero, ovvero $I(\sigma) = 0$.
	Ora si supponga che la superficie cubica chiusa $\sigma$ sia formata dall’unione di superfici parziali, diciamo per esempio dalle sei facce che la compongono con l’orientamento mostrato in figura:![[Elettrotecnica-1793030327959.webp|273]]
	#Figura(1.18). *Superfici parziali che compongono $\sigma$ e relativo orientamento per la misura di corrente*
	
	In particolare, le superfici colorate in azzurro e verde sono orientate dall’esterno verso l’interno, mentre le superfici colorate in rosso sono orientate dall’interno verso l’esterno. Indicando per semplicità:
	$$I(\sigma_{k}) = i_{k}$$le misure di corrente eseguite sulle superfici parziali ed applicando le proprietà additiva e di essere dispari, vale il seguente bilancio attraverso $\sigma$:
	$$−i_{1}−i_{2} + i_{3}−i_{4}−i_{5} + i_{6} = 0$$

Generalizzando possiamo dedurre la seguente legge fondamentale:

> [!important] Definizione
> **Legge delle correnti**: la somma algebrica (cioè tenendo conto dei segni) delle correnti misurate attraverso una superficie $σ$ chiusa è uguale a zero.


Un modo alternativo di enunciare la legge delle correnti consiste nel riscrivere il bilancio trasportando tutte le (misure) correnti negative al membro di destra:
$$i_{3} + i_{6} = i_{1} + i_{2} + i_{4} + i_{5}$$

I termini a primo membro rappresentano la somma delle correnti uscenti da $\sigma$ mentre i termini al secondo membro sono la somma delle correnti entranti. La legge delle correnti impone che tali somme debbano eguagliarsi, cioè che la corrente totale che entra in una superficie chiusa sia pari alla corrente totale che ne fuori esce.



## 1.3 **Il circuito elettrico**

Le grandezze elettriche e le loro proprietà sono state fino a qui descritte in termini astratti riferendosi ad una regione qualunque di spazio. Passiamo ora ad ambientarle nella struttura particolare di un circuito elettrico inteso come interconnessione di dispositivi elementari.

I componenti/dispositivi elettrici sono fabbricati combinando materiali che da un punto di vista elettrico possiedono proprietà opposte: gli **isolanti** ed i **conduttori**.
- Per isolante ideale noi intendiamo un materiale che a fronte della applicazione di una tensione elettrica finita $v\ne0$, per esempio applicandogli una pila elettrica, sia attraversato da una <mark class="hltr-yellow">corrente nulla</mark> $i=0$. Un tale materiale dunque si oppone al passaggio di corrente anche in presenza di tensioni significative. Materiali isolanti sono per esempio la carta, il legno o la plastica.
- Viceversa un materiale conduttore ideale è quello in cui può circolare una corrente finita $i\ne0$ anche in <mark class="hltr-yellow">assenza di tensione</mark> $v=0$. Un conduttore reale è quello che consente la circolazione di correnti significative anche in presenza di tensioni molto piccole. Materiali conduttori sono tutti i metalli o l’acqua.

Alle due categorie estreme ora introdotte si deve aggiungere quella dei **semi-conduttori** i quali in natura presentano <u>proprietà elettriche intermedie tra il conduttore e l’isolante</u> e possono essere trasformati nell’uno o nell’altro attraverso opportuni trattamenti tecnologici. La loro grande flessibilità ha di fatto reso possibile l’enorme sviluppo della micro-elettronica. Un dispositivo elementare è avvolto da una superficie di materiale isolante attraverso la quale non può esserci passaggio di carica, cioè corrente.
Questa superficie isolante ha la funzione di confinare la parte interna del dispositivo dall’ambiente esterno e di protezione. La superficie isolante è poi attraversata in pochi punti da parti di materiale conduttore che funzionano come tramite o porta con l’ambiente esterno.

Tali parti conduttrici vengono chiamate **terminali** o **morsetti** o ancora **poli** del dispositivo. L’interazione elettrica del dispositivo con l’ambiente esterno avviene esclusivamente attraverso i suoi poli.

![[Elettrotecnica-1793030901235.webp|354]]
#Figura(1.19). *Elementi circuitali*

Gli elementi in figura sono dispositivi con due, tre e quattro poli rispettivamente a cui daremo il nome di <u>bipolo, tripolo e quadripolo</u>.

Inizieremo col considerare il caso di circuiti formati interconnettendo tra loro un numero arbitrario di dispositivi con due poli, cioè di bipoli, e chiameremo **nodo** ogni punto in cui due terminali di bipoli vengono connessi. Per esempio, il circuito in figura 1.20 contiene 6 bipoli e 4 nodi indicati con $A, B, C, D$.
![[Elettrotecnica-1793031354078.webp|246]]
#Figura(1.20). *Esempio di circuito*

Caratterizziamo elettricamente il bipolo $1$ collegato ai nodi $A$ e $B$ inserendo opportunamente gli strumenti voltmetro e amperometro:
![[Elettrotecnica-1793031405465.webp|192]]
#Figura(1.21). *Inserimento del voltmetro e amperometro sul bipolo $1$*

- L’inserimento del voltmetro avviene collegando i puntali ai due morsetti del bipolo in modo che lungo il voltmetro cada la tensione da misurare; si dice che <u>il voltmetro viene collegato in parallelo</u>;
- L’inserimento dell’amperometro avviene tagliando il filo ad uno dei morsetti ed inserendo lo strumento in modo che sia attraversato dalla corrente da misurare; si dice che <u>l’amperometro viene collegato in serie</u>.

Si noti dalla figura 1.21 come tale inserimento corrisponda a rilevare la misura della tensione $v_{AB}$ cioè della tensione del morsetto o nodo $A$ rispetto al morsetto o nodo $B$ e della corrente $i_{A}$ entrante nel bipolo dal morsetto $A$.
La particolare modalità di inserimento degli strumenti verrà indicata d’ora in poi semplicemente disegnando accanto al bipolo un arco di linea orientato che specifica il verso di misura della tensione e sul filo accanto al corrispondente terminale una freccia che indica il verso della misura di corrente:![[Elettrotecnica-1793031500153.webp|225]]
#Figura(1.22). *Verso assunto nella misura della tensione e della corrente*

Nel linguaggio della teoria dei circuiti diremo semplicemente che $v_{AB}$ e $i_{A}$ sono le variabili tensione e corrente del bipolo (o associate al bipolo), sottintendendo che esse rappresentano nel modello le misure delle grandezze fisiche corrispondenti. Ricordiamo anche che tali misure possono assumere valore positivo, negativo o nullo.

Si supponga ora di misurare al terminale $B$ la corrente entrante $i_{B}$. Dalla legge delle correnti assumendo una superficie chiusa che avvolge il bipolo $1$, ricaviamo:
$$i_{A} + i_{B} = 0 \rightarrow i_{B} =−i_{A}$$
che ci dice che la misura al terminale $B$ si deduce da quella eseguita in $A$. Concludiamo dunque che <mark class="hltr-yellow">ai capi di un bipolo esiste solo una corrente indipendente che ne caratterizza completamente il flusso di carica</mark>.![[Elettrotecnica-1793031649832.webp|204]]
#Figura(1.23). *Applicazione della legge delle correnti al bipolo*

Ragioniamo ora sulle tensione e supponiamo di misurare la tensione $v_{BA}$, cioè del mosetto $B$ rispetto al morsetto $A$. Dalla legge delle tensioni (o dalla proprietà di disparità) ricaviamo che:
$$v_{AB} + v_{BA} = 0 \rightarrow v_{BA} =−v_{AB}$$
e dunque che <mark class="hltr-yellow">ai capi di un bipolo esiste solo una tensione indipendente che ne caratterizza completamente il lavoro elettrico svolto per spostare lungo il bipolo una carica di prova</mark>.![[Elettrotecnica-1793031837872.webp|198]]
#Figura(1.24). *Applicazione della legge delle tensioni al bipolo*


Quindi, un dispositivo elettrico con due morsetti è descritto completamente da una corrente ed una tensione; si dice anche che i due morsetti con le relative grandezze formano una **porta elettrica** o anche un **lato**.

Poiché un bipolo è descritto da due grandezze e dalle rispettive convenzioni di misura nasce spontanea l’idea di coordinare tra di loro tali convenzioni di misura. La figura 1.25 mostra un primo modo di abbinare le due misure prendendo il verso di misura della corrente entrante dal morsetto verso cui è rivolta la freccia che descrive l’orientazione della misura di tensione. Questa modalità viene riferita come **convenzione degli utilizzatori**.
![[Elettrotecnica-1793031950798.webp|200]]
#Figura(1.25). *Convenzione degli utilizzatori*


La figure 1.26 invece mostra un modo alternativo di coordinare le misure prendendo il verso della corrente uscente dal morsetto verso cui è rivolta la freccia della tensione. Questa modalità si dice **convenzione dei generatori**.
![[Elettrotecnica-1793032042881.webp|212]]
#Figura(1.26). *Convenzione dei generatori*



## 1.4 **Le leggi di Kirchoff**

Siamo ora in grado di tornare al circuito completo mostrato in [[#1.3 **Il circuito elettrico**|figura 1.20]]: ogni bipolo è descritto elettricamente da una tensione e da una corrente che supponiamo misurate con la convenzione degli utilizzatori. Rivediamo la legge delle correnti ambientandola sul circuito. Per questo consideriamo, per prima, la superficie chiusa $\sigma_{1}$ indicata in figura 1.27 che orientiamo dall’interno verso l’esterno.
![[Elettrotecnica-1793032550236.webp|294]]
#Figura(1.27). *Le linee tratteggiate rosse e blu mostrano la traccia sul foglio delle due superfici chiuse $\sigma_{1}$ e $\sigma_{2}$. La KCL bilancia le correnti che attraversano tali superfici*

Notiamo che per costruzione in un circuito elettrico le correnti possono circolare solo nei bipoli e nei loro terminali esterni e che la superficie $\sigma_{1}$ interseca i morsetti dei bipoli $2, 3, 4, 6$. La legge delle correnti si riduce a:
$$i_{2} + i_{3} − i_{4} − i_{6} = 0 \quad(1.1)$$

In termini generali possiamo allora enunciare la seguente:

> [!important] Definizione
> **Legge di Kirchhoff delle correnti** (**KCL**): la somma algebrica (cioè con segno) delle correnti (cioè delle misure di corrente) dei bipoli i cui terminali vengono intersecati da una superficie chiusa è sempre zero.


Tale somma con segno viene anche chiamato **bilancio di corrente**.

E’ istruttivo (e rilevante nella pratica) notare come il bilancio di corrente $(1.1)$ si possa riscrivere portando le correnti che compaiono col segno meno al membro di destra:
$$i_{2} + i_{3} = i_{4} + i_{6}$$
Questa riscrittura corrisponde ad interpretare la legge KCL come: la somma delle correnti dei bipoli il cui verso (di misura) è entrante in $\sigma_{1}$ è uguale alla somma delle correnti dei bipoli il cui verso è uscente dalla medesima.


Si consideri ora la superficie chiusa indicata con $\sigma_{2}$ che circonda il nodo $3$. La superficie interseca esclusivamente i morsetti dei bipoli che sono collegati al nodo, cioè $3, 5$ e $6$. Orientando la superficie dall’interno all’esterno, la legge di Kirchhoff delle correnti diventa nel caso particolare:
$$i_{3}−i_{5}−i_{6} = 0 \quad (1.2)$$

e si può enunciare nel modo seguente:

> [!important] Definizione
> **Legge di Kirchhoff delle correnti al nodo**: la somma algebrica (cioè con segno) delle correnti che escono (o in modo del tutto equivalente che entrano) da un nodo di un circuito è sempre zero.


Anche in questo caso, il bilancio di corrente si può riscrivere:
$$i_{3} = i_{5} + i_{6}$$
e pensare nei termini: la somma delle correnti entranti al nodo è pari alla somma delle correnti ivi uscenti.


Passiamo ora alle tensioni facendo riferimento alla figura 1.28 che mostra le relative misure sui vari bipoli. Ci focalizziamo sulla linea chiusa $\gamma_{1}$ tratteggiata in rosso, che supponiamo orientata in senso orario. Essa descrive un percorso chiuso tra i nodi $B →A →D →C →B$.
![[Elettrotecnica-1793032824107.webp|295]]
#Figura(1.28). *Cammini chiusi $\gamma_{1}$ e $\gamma_{2}$ lungo cui si bilanciano le tensioni*

Attualizziamo la legge delle tensioni osservando ora che ogni tratto del percorso chiuso corrisponde alla tensione misurata su di un bipolo. Si ha:
$$v_{1}−v_{6} + v_{5}−v_{2} = 0 \quad (1.3)$$

In teoria dei circuiti, si indica con il nome di "**cammino**" la sequenza ordinata di bipoli (o lati) che si incontrano muovendosi lungo un certo percorso. **Un cammino chiuso viende detto maglia**.

> [!important] Definizione
> **Legge di Kirchhoff delle tensioni** (**KVL**): la somma algebrica delle tensioni misurate lungo una maglia è zero.


Osserviamo anche che la $(1.3)$ può essere riscritta come:
$$v_{1}−v_{6} = v_{2}−v_{5}$$

Le tensioni a membro di sinistra corrispondono alla somma lungo il cammino che parte da $B$ e va a $D$ (attraverso $A$) mentre il membro di destra è la somma delle tensioni lungo un secondo cammino sempre da $B$ a $D$ (attraverso $C$). Questa seconda espressione della legge di Kirchhoff delle tensioni dunque corrisponde ad imporre che le tensioni raccolte lungo cammini diversi ma con gli stessi estremi devono essere uguali tra loro. Per esempio, facendo riferimento alla maglia descritta da $\gamma_{2}$ tratteggiata in blu in figura 1.29, si può scrivere direttamente che:
$$v_{2} = v_{3} + v_{5}$$
anziché
$$v_{2}−v_{3}−v_{5} = 0$$

La validità della legge di Kirchhoff delle tensioni ha come conseguenza che la tensione elettrica misurata tra due nodi qualunque di un circuito elettrico è sempre la stessa indipendentemente dal percorso lungo cui avviene la misura. Questo ci permette di introdurre il concetto di **tensione di nodo** o **potenziale** di nodo.

Allo scopo, si assuma in modo arbitrario un nodo del circuito come nodo di riferimento, per esempio in figura 1.29 il riferimento sia il nodo $A$, e si misurino le tensioni degli altri nodi rispetto al nodo di riferimento.
![[Elettrotecnica-1793033245095.webp|297]]
#Figura(1.29).

la tensione relativa di un nodo rispetto al riferimento è detta tensione di nodo o potenziale e viene indicata con la lettera “$e$” mettendo al pedice il numero o la lettera che identifica il nodo di misura. Nella figura, prendendo $A$ come riferimento, si hanno le seguenti tensioni di nodo:
$$e_{B} = v_{BA} =−v_{1}, e_{C} = v_{CA} =−v_{4}, e_{D} = v_{DA} =−v_{6}$$

Notiamo che, ragionando in modo inverso, dalla conoscenza dei potenziali di nodo è possibile ricavare le tensioni dei bipoli. In generale infatti si ha che per il generico bipolo connesso tra i nodi $k$ e $j$, in cui indichiamo con $e_{k}$ ed $e_{j}$ i rispettivi potenziali rispetto ad un riferimento qualunque, la tensione misurata ai capi del bipolo, cioè $v_{kj}$, vale:
$$v_{kj}= e_{k}−e_{j}.$$
![[Elettrotecnica-1793033419221.webp|214]]
#Figura(1.30). *Dai potenziali ai nodi a cui un bipolo è connesso si risale alla sua tensione*


#### #Esercizio(Leggi di Kirchoff) (1)

> [!question] Esercizio
> ![[Elettrotecnica-1793113870627.webp|352x238]]
> Nella rete di bipoli mostrata in figura sono i valori di alcune correnti indicate in rosso, cioè:
> $$i_{2}=1A;\quad i_{6}=-2A;\quad i_{7}=3A$$
> Determinare per primo il valore della corrente $i_{3}$ scrivendo una sola KCL. Successivamente completare determinando le correnti incognite.


#### #Esercizio(Leggi di Kirchoff) (2)

> [!question] Esercizio
> ![[Elettrotecnica-1793114056557.webp|362x276]]
> Nella rete di bipoli mostrata in figura sono ora noti i valori di alcune tensioni indicate in rosso in figura, cioè:
> $$v_{1} = 1V;\quad v_{3} =−1V;\quad v_{4} =−2V;\quad v_{5} = 3V$$
> Determinare per primo il valore della tensione $v_{7}$ scrivendo una sola KVL. Successivamente completate determinando le altre tensioni incognite.
> Quindi si fissi il nodo $E$ come riferimento e si determinino i potenziali ai rimanenti nodi.



## 1.5 **Dispositivi con più di due terminali e loro modelli**

Un primo esempio di dispositivo con più di due terminali è il tripolo elettrico disegnato in figura:
![[Elettrotecnica-1793189529523.webp|171]]
#Figura(1.31). *Un tripolo*

In questo caso, le grandezze elettriche che si possono misurare sono tre tensioni e tre correnti, tuttavia è facile verificare che solo un sottoinsieme di queste risultano tra di loro indipendenti. Infatti applicando la legge delle correnti ad una superficie chiusa che racchiude in se il tripolo, si ricava la relazione:
$$i_{1} + i_{2} + i_{3} = 0 \rightarrow i_{3} =−i_{1}−i_{2}$$

mentre dalla legge delle tensioni lungo un cammino chiuso che tocca i tre terminali, si ha:
$$v_{13}−v_{12}−v_{23} = 0 \rightarrow v_{12} = v_{13}−v_{23}$$

Si conclude che <mark class="hltr-yellow">in un tripolo solo due correnti e due tensioni sono tra di loro indipendenti e dunque possono essere assunte come variabili descrittive</mark>.

E’ facile verificare che questa proprietà si estende facilmente al caso di un generico $N$-polo, cioè di un dispositivo con $N$ terminali. Nel caso generale, l’$N$-polo ha $N−1$ correnti e $N−1$ tensioni indipendenti.
Il procedimento che si adotta per determinare il sottoinsieme di tensioni e correnti da utilizzare come variabili descrittive è quello di scegliere arbitrariamente un terminale come riferimento comune e quindi di scegliere le correnti entranti agli $N−1$ nodi rimanenti e le $N−1$ tensioni misurate tra gli $N−1$ nodi e il riferimento.

![[Elettrotecnica-1793189797821.webp|379]]
#Figura(1.32). *(<u>Sinistra</u>) possibile scelta delle due tensioni e correnti che descrivono un tripolo: si assume come nodo comune di riferimento il numero $3$; (<u>Destra</u>) analogia con il caso di due bipoli*

Come esempio, la figura 1.32 mostra per un tripolo il caso in cui come riferimento si è assunto il nodo $3$ e quindi le due tensioni indipendenti risultano $v_{13}$ e $v_{23}$. Con questa scelta, come correnti indipendenti si assumeranno quelle entranti in tutti i nodi tranne quello di riferimento, ovvero nel caso specifico $i_{1}$ e $i_{2}$.

![[Elettrotecnica-1793190133801.webp|279]]
#Figura(1.33). *(<u>Sinistra</u>) Scelta delle due tensioni e correnti che descrivono un tripolo quando si assume come nodo comune di riferimento il numero $2$; (<u>Destra</u>) Analogia con il caso di due bipoli*

La figura 1.33 mostra un secondo esempio nel quale il riferimento viene assunto nel nodo $2$.
Nella parte (destra) delle figure 1.33 e 1.34 viene mostrata la seguente proprità: dal punto di vista delle leggi di Kirchhoff, il tripolo è del tutto analogo al caso di due bipoli collegati tra di loro nel nodo di riferimento.

Generalizzando, si ha che **un dipositivo con $N$ terminali (cioè un $N$-polo), al fine delle leggi di Kirchhoff, può essere ricondotto al caso di un insieme di $N−1$ bipoli collegati tra loro nel nodo scelto come riferimento**.
Ogni coppia di terminali formata da un nodo ed il nodo di riferimento identifica una porta elettrica o lato in quanto, al pari di un bipolo, è descritta dall’informazione composta da una tensione ed una corrente.
![[Elettrotecnica-1793190373969.webp|228]]
#Figura(1.34). *Tripolo in cui il nodo comune viene raddoppiato in modo da formare un modello circuitale di tipo doppio bipolo*

Questo punto di vista diventa ancora più evidente se il nodo di riferimento nel caso del tripolo viene raddoppiato in modo da formare le due coppie di terminali $a−a′$ e $b−b′$ in figura 1.34, che definiscono esplicitamente le due porte, le quali sono poi collegate a due bipoli esterni. Il collegamento ai bipolo esterni assicura che la corrente $i_{1}$ entrante in $a$ sarà uguale a quella uscente in $a′$ mentre la corrente $i_{2}$ entrante in $b$ sarà uguale a quella uscente in $b′$.
In queste condizioni, si dice che l’elemento a quattro terminali che si è venuto a formare in figura 1.34 (racchiuso con linea tratteggiata) si comporta, o può essere descritto, come un (modello) **doppio bipolo**.
Si badi che il modello di doppio bipolo si differenzia da un dispositivo quadripolo generico: quest'ultimo infatti è in generale descritto da 3 tensioni e 3 correnti indipendenti, cioè da tre porte elettriche. Il modello doppio bipolo in figura invece è descritto da sole due correnti e due tensioni indipendenti, cioè da due porte. Il doppio bipolo che abbiamo derivato partendo dal tripolo (raddoppiandone un terminale) rappresenta un caso particolare di modello di tipo doppio bipolo e viene spesso indicato come <u>doppio bipolo tripolare</u>.

Il caso più generale di modello doppio bipolo è invece quello mostrato di seguito, in cui le due porte non sono necessariamente collegate tra loro. Dal punto di vista della scrittura delle leggi di Kirchhoff il doppio bipolo è analogo (e quindi può essere ricondotto) a quello di due bipoli non necessariamente collegati tra di loro.
![[Elettrotecnica-1793190473261.webp|421]]
#Figura(1.35). *Modello generico di doppio bipolo in cui le porte non sono collegate*

Infine la figura 1.36 mette in evidenza come sia sempre possibile utilizzare il modello di doppio bipolo per descrivere un dispositivo tripolo:
![[Elettrotecnica-1793190527710.webp|278]]
#Figura(1.36). *l dispositivo tripolo si può ottenere dal modello doppio bipolo collegando i terminali di quest’ultimo in modo opportuno*


#### #Esercizio(Tripoli/doppi bipoli) (1)

> [!question] Esercizio
> ![[Elettrotecnica-1793190843752.webp|303]]
> Il circuito mostrato in figura contiene un tripolo e sono noti i valori delle correnti:
> $$i_{1} = 1A;\quad i_{6} = 2A;\quad i_{7} = 3A$$
> Determinare il valore delle correnti $i_{3}$ ed $i_{4}$ nel tripolo. Notate che è possibile trasformare il tripolo in un insieme di due bipoli $3$ e $4$ connessi al nodo comune $C$ come mostrato in figura:
> ![[Elettrotecnica-1793190851431.webp|303x210]]


#### #Esercizio(Tripoli/doppi bipoli) (2)

> [!question] Esercizio
> ![[Elettrotecnica-1793190953778.webp|304x212]]
> Nella rete mostrata in figura sono ora noti i valori delle tensioni:
> $$v_{2} = 2V;\quad v_{3} = 3V;\quad v_{4} = 4V;\quad v_{5} = 5V$$
> Determinare le tensioni $v_{7}, v_{1}$ e $v_{6}$.


#### #Esercizio(Tripoli/doppi bipoli) (3)

> [!question] Esercizio
> ![[Elettrotecnica-1793191047400.webp|306x198]]
> Infine il circuito in figura contiene un doppio bipolo e sono note le correnti:
> $$i_{1} = 1A;\quad i_{4} = 4A;\quad i_{5} = 5A$$
> Determinate i valori di $i_{2}, i_{3}$, e di $I_{x}$ e $I_{y}$.



## 1.6 **Il teorema di Tellegen**

Torniamo a considerare il generico circuito elettrico prendendo come esempio quello mostrato in figura 1.37. Notate che ogni "scatola" (elemento) che lo forma può rappresentare il modello di un bipolo oppure una porta di un $N$-polo o doppio bipolo. Si assume di coordinare le misure di corrente e tensione su ogni elemento con la stessa convenzione, per esempio quella degli utilizzatori.
![[Elettrotecnica-1793191314588.webp|250]]
#Figura(1.37). *Generico circuito*

Si sceglie a caso un insieme di valori delle correnti $i_{1}, i_{2},\cdots, i_{6}$ col solo vincolo che questi soddisfino le KCL e quindi si sceglie a caso un insieme di valori delle tensioni $v_{1}, v_{2},\cdots, v_{6}$ purché soddisfino le KVL.

> [!important] Definizione
> E’ possibile mostrare che vale la seguente relazione detta **teorema di Tellegen**:
> $$\sum_{k=1}^6v_{k}\cdot i_{k}=0\quad (1.4)$$

<u>Dimostrazione</u>:
dopo aver scritto per esteso la sommatoria:
$$v_{1}\cdot i_{1} + v_{2}\cdot i_{2} + v_{3}\cdot i_{3} + v_{4}\cdot i_{4} + v_{5}\cdot i_{5} + v_{6}\cdot i_{6}$$
esprimiamo le tensioni sui vari elementi in funzione dei potenziali ai nodi. Per far questo dobbiamo prendere uno qualunque dei nodi come riferimento.
Assumendo il nodo $A$ come riferimento si hanno i tre potenziali ai nodi:
$$e_{B} = v_{BA} =−v_{1},\quad e_{C} = v_{CA} =−v_{4},\quad e_{D} = v_{DA} =−v_{6}$$
La sommatoria si può scrivere:
$$−e_{B}\cdot i_{1} + (e_{C}-e_{B})\cdot i_{2} + (e_{D}−e_{B})\cdot i_{3}−e_{C}\cdot i_{4} + (e_{C}−e_{D})\cdot i_{5}−e_{D}\cdot i_{6}$$
e quindi riordinare in modo da raccogliere i termini che contengono lo stesso potenziale ai nodi:
$$e_{B}\cdot (−i_{1}−i_{2}−i_{3}) + e_{C}\cdot (i_{2}−i_{4} + i_{5}) + e_{D}\cdot (−i_{6}−i_{5} + i_{3})$$

E’ facile realizzare che ogni termine nell’ultima formulazione è dato dal prodotto del potenziale di nodo (per esempio $e_{B}$) moltiplicato per la sommatoria delle correnti uscenti dal medesimo nodo (per esempio $−i_{1}−i_{2}−i_{3}$).
Valendo la KCL, questi termini sono nulli portando alla $(1.4)$.

Si può riassumere a parole: scelto per ogni elemento (bipolo o porta) di un circuito tensione e corrente, con la stessa convenzione di misura, nella sola ipotesi che tali variabili soddisfino alle KVL e KCL la sommatoria dei prodotti $v_{k}\cdot i_{k}$ estesa a tutti gli elementi vale zero.
Il prodotto $v_{k}\cdot i_{k}$ è detto **potenza virtuale**.




# **Capitolo II: Legame costitutivo**


## 2.1 **Il principio di identità del bipolo**

Immaginiamo di eseguire un esperimento in cui un dato bipolo $B$ che vogliamo studiare sia collegato ad una rete esterna che possiamo variare. Questa è indicata come $N_{k}$ (come "network" $k$-esima), dove il pedice $k$ indicizza una certa configurazione della rete.
![[Elettrotecnica-1793195428924.webp|227]]
#Figura(2.1).

Per ogni configurazione della rete $N_{k}$ misuriamo i valori della corrente e tensione capi di $B$. Dette coppie di valori $(i_{k}, v_{k})$, riportate nel piano $i-v$ definiscono una curva ben precisa. Indipendentemente da ciò che è collegato esternamente a $B$, ogni qualvolta la corrente assume un dato valore (per esempio $\overline{i}$) la tensione assume il valore corrispondente (per esempio $\overline{v}$) individuato sulla curva:
![[Elettrotecnica-1793195475296.webp|237]]
#Figura(2.2).


> [!important] Definizione
> Si può affermare che: in un bipolo, mantenuto in condizioni operative normali, tra la tensione e corrente misurate ai sui capi esiste una relazione che non dipende da ciò che ad esso è collegato, ma dipende esclusivamente dalla sua natura.
> Questo legame si può esprimere da un’equazione, che nella sua forma implicita denotiamo con $\mathbf{f(v,i)=0}$, detta **equazione caratteristica** o **legame costitutivo**.



## 2.2 **Il bipolo resistore**

Il simbolo che rappresenta un resistore è mostrato in figura 2.3 dove è riportato il verso della tensione e della corrente, misurate con la <u>convenzione degli utilizzatori</u> ed il parametro $R$ detto **resistenza**.
![[Elettrotecnica-1793196179401.webp|172]]
#Figura(2.3).

Il suo legame costitutivo o equazione caratteristica è dato da:
$$v = R \ i \quad (2.1)$$

Dunque l’equazione caratteristica è un legame di proporzionalità diretta attraverso il parametro resistenza, questa si misura in ohm $[Ω]$.
La figura 2.4 illustra la curva caratteristica nel piano $i-v$ che è una retta passante per l’origine degli assi avente pendenza $R$.
![[Elettrotecnica-1793196208464.webp|292]]
#Figura(2.4).

Nella forma $(2.1)$ la variabile tensione è una funzione della corrente, <mark class="hltr-yellow">il resistore si dice controllabile in corrente</mark>.
Nel caso in cui $R \ne 0$ è anche possibile invertire la $(2.1)$ riscrivendola:
$$i=\frac{1}{R}\ v = G \ v \quad (2.2)$$

dove il parametro $G=\frac{1}{R}$ si chiama **conduttanza** e si misura in siemens $[S=\Omega^{-1}]$.
Nella forma $(2.2)$ <mark class="hltr-yellow">la variabile corrente è funzione della tensione cioè è controllata in tensione</mark>. Si conclude che se $R \ne 0$ il resistore è controllabile anche in tensione. Si noti che $(2.1)$ e $(2.2)$ sono due equazioni esplicite. Esse si possono anche riscrivere nella forma implicita:
$$f (v, i) = v−R i= 0$$

a cui spesso facciamo riferimento nella Teoria.
Infine, è istruttivo considerare i casi limite in cui $R \rightarrow 0$ e $G \rightarrow 0$ (cioè $R \rightarrow \infty$).


### 2.2.1 **Caso $R \rightarrow 0$**

La retta caratteristica riduce progressivamente la sua pendenza fino, al limite, ad adagiarsi sull’asse della corrente come mostrato in figura:
![[Elettrotecnica-1793196361006.webp|299]]
#Figura(2.5).

Dalla $(2.1)$, si ottiene:
$$v = 0 \quad \forall i$$

e si dice che il resistore si comporta come un **corto circuito**, ovvero <u>ai sui capi la tensione è nulla qualunque sia la corrente che lo attraversa</u>. Il simbolo del corto circuito è mostrato in figura:
![[Elettrotecnica-1793196429703.webp|154]]
#Figura(2.6).

**Attenzione!** Il bipolo corto circuito è controllabile in corrente infatti la tensione si può scrivere come una funzione della corrente:
$$v = 0 \cdot i$$
ma <u>non è controllabile in tensione</u>.


### 2.2.2 **Caso $R \rightarrow \infty$ cioè $G \rightarrow 0$**

In questo caso la retta caratteristica aumenta progressivamente la sua pendenza fino ad adagiarsi sull’asse della tensione come mostrato in figura:
![[Elettrotecnica-1793196615288.webp|224]]
#Figura(2.7).

Dalla $(2.2)$, si ottiene:
$$i= 0 \quad \forall v$$

e si dice che il resistore si comporta come un **circuito aperto** ovvero <u>la corrente che lo attraversa è nulla qualunque sia la tensione ai sui capi</u>. Il simbolo del circuito aperto è mostrato in figura:
![[Elettrotecnica-1793196661487.webp|126]]
#Figura(2.8).

**Attenzione!** Il bipolo circuito aperto è controllabile in tensione potendo scrivere la sua corrente come una funzione della tensione:
$$i= 0 \cdot v$$
ma <u>non è controllabile in corrente</u>.



## 2.3 **Generatore ideale di tensione**

Il simbolo di questo bipolo elementare è mostrato in figura 2.9 dove accanto è riportato il parametro $E$, misurato in volt, che ne determina il legame costitutivo.
![[Elettrotecnica-1793196885537.webp|148]]
#Figura(2.9).

Questo infatti è dato da:
$$v = E \quad (1.3)$$
Dunque l’equazione caratteristica semplicemente impone il valore di tensione ai capi del generatore indipendentemente dal valore della corrente che lo attraversa. La figura 2.10 mostra come la curva caratteristica del generatore ideale di tensione sia una retta parallela all’asse delle correnti.
![[Elettrotecnica-1793196907136.webp|218]]
#Figura(2.10).

Ne consegue che questo bipolo <u>è controllabile in corrente ma non in tensione</u>. L’equazione $(2.3)$ può infatti pensarsi scritta in modo che la tensione sia una funzione della corrente nel modo seguente:
$$v = E + i \cdot 0$$

che non si può invertire per esplicitare la corrente in funzione della tensione. Il caso limite $E \rightarrow 0$ è tale per cui la retta caratteristica del generatore ideale di tensione tende a coincidere con l’asse delle correnti, che corrisponde al legame:
$$v = 0 \quad \forall i$$
![[Elettrotecnica-1793197276503.webp|230]]
#Figura(2.11).

Quando il generatore di tensione viene spento (cioè $E= 0 \ V$) si comporta come il corto circuito di [[#2.2.1 **Caso $R rightarrow 0$**|figura 2.6]].



## 2.4 **Generatore ideale di corrente**

Il simbolo del generatore di corrente è mostrato in figura 2.12 dove accanto al simbolo è riportato il parametro $I_{s}$, misurato in ampere, che ne determina il legame costitutivo.
![[Elettrotecnica-1793197449301.webp|177]]
#Figura(2.12).

Questo infatti è dato da:
$$i= I_{s} \quad (1.4)$$

Dunque, in questo caso, l’equazione caratteristica semplicemente impone il valore di corrente che scorre attraverso il generatore indipendentemente dal valore della tensione ai suoi capi. La figura 2.13 mostra come la curva caratteristica del generatore ideale di corrente sia una retta parallela all’asse delle tensioni.
![[Elettrotecnica-1793197628932.webp|179]]
#Figura(2.13).

Questo bipolo elementare è controllabile in tensione ma non in corrente. L’equazione $(2.4)$ può infatti pensarsi riscritta in modo tale che la corrente sia una funzione della tensione:
$$i= Is + v \cdot 0$$

che chiaramente non può essere invertita in modo da esplicitare la tensione in funzione della corrente. Il caso limite $I_{s} \rightarrow 0$ è tale per cui la retta caratteristica del generatore ideale di corrente tende a coincidere con l’asse delle tensioni, che corrisponde al legame:
$$i= 0 \quad \forall v$$
![[Elettrotecnica-1793197652623.webp|211]]
#Figura(2.14).

Dunque, spegnendo un generatore di corrente (cioè $I_{s} = 0 A$) si ottiente un circuito aperto come mostrato di [[#2.2.2 **Caso $R rightarrow infty$ cioè $G rightarrow 0$**|figura 2.8]].



## 2.5 **Osservazione sulle convenzioni di misura $V-I$**

Durante l’analisi di circuiti, la convenzione di misura adottata sui singoli bipoli può indurre a qualche dubbio/perplessità. Per questo motivo, riesaminiamo qui il ruolo della convenzione adottata per i vari tipi di bipolo.

Nel caso di un resistore, si è visto che misurando $v$ ed $i$ con la convenzione degli utilizzatori, come in [[#2.2 **Il bipolo resistore**|figura 2.3]], il legame costitutivo è:
$$v = R \cdot i$$

Invertiamo ora il segno della misura di corrente, cioè usiamo come variabile alla porta la corrente $i'=−i$, come mostrato in figura:
![[Elettrotecnica-1793197858615.webp|114]]
#Figura(2.15). *Convenzione dei generatori in un resistore*

Dalla $(2.1)$, otteniamo:
$$v =−R \ i' \quad (2.5)$$

Dunque, se adottiamo la convenzione dei generatori nel legame costitutivo del resistore compare un segno meno. Per questo comunemente **per i bipoli di tipo resistore è naturale assumere la convenzione di misura degli utilizzatori in modo che valga la $(2.1)$ col segno positivo**.

Esaminiamo ora il caso di un generatore di tensione, il cui legame costitutivo con la convenzione degli utilizzatori mostrata in [[#2.3 **Generatore ideale di tensione**|figura 2.9]] è:
$$v = E$$

Se invertiamo il segno della corrente alla porta, cioè $i'=−i$, come mostrato in figura 2.16 (Sinistra) vediamo che il legame costitutivo rimane invariato in quanto la corrente non compare nell’espressione. La stessa conclusione vale per il generatore ideale di corrente, in cui si assuma la convenzione di misura dei generatori come mostrato in figura 2.16 (Destra). Per questo motivo **per i bipoli di tipo generatore ideale si adotta indifferentemente la convenzione di misura degli utilizzatori o dei generatori**.
![[Elettrotecnica-1793198138993.webp|356]]
#Figura(2.16). *Convenzione dei generatori in un generatore di tensione (<u>Sinistra</u>) ed in uno di corrente (<u>Destra</u>)*



## 2.6 **Dispositivi fisici, modelli e limiti di validità**

Il modello di resistore è in grado di rappresentare il caso di un oggetto filiforme, cioè la cui lunghezza sia ordini di grandezza superiore rispetto all’area (o meglio alla radice quadrata dell’area) della sua sezione. La figura 2.17 mostra il caso di un oggetto cilindrico di sezione costante, la cui area sia $S$, e di lunghezza $L$.
![[Elettrotecnica-1793198264146.webp|649]]
#Figura(2.17).

Quando viene inserito in un circuito chiuso in modo che lo attraversi una corrente elettrica "di opportuna intensità" si vede che la tensione che nasce ai sui capi è data da:
$$v = R \cdot i$$
dove:
$$R=\rho \ \frac{L}{S} \quad(1.6)$$

La resistenza del filo è determinato dal parametro $\rho$, chiamato **resistività**, che dipende dal tipo di materiale che forma il filo e dai fattori geometrici $L$ ed $S$.
Per esempio, un filo di rame, la cui resistività è circa $\rho_{cu} = 1.69 \cdot 10^{-8} \ \Omega \ m$, di sezione pari a $1 \ mm^2 = 10^{−6} \ m^2$ e di lunghezza pari a $L= 10 \ m$ ha una resistenza di:
$$R= 1.6910^{−8}\cdot \frac{10}{10^{-6}} \approx 0.16 \ \Omega$$

Il rame è un ottimo conduttore e viene utilizzato per realizzare i fili di collegamento tra i componenti di un sistema elettrico; dato che la resistenza dei fili è comunemente trascurabile rispetto a quella dei componenti, i fili si possono modellare come corto circuito $R \approx 0 \ \Omega$.

Anche i modelli elettrici hanno dei <u>limiti di validità</u>. Nel caso del resistore fisico, il legame $v = R\cdot i$ è valido fino a che la corrente che scorre rimane in un <u>certo intervallo di valori</u>. Vedremo che questo è determinato da un’altra grandezza elettrica chiamata **potenza elettrica** e data dal prodotto $v\cdot i$.

Vedremo anche come l’uso di modelli ideali di generatore può, in certe condizioni, portare a dei problemi matematici che non hanno soluzione. In questo caso, l’eccessiva semplificazione fa si che il modello non sia più attinente alla realtà.




# **Capitolo III: Analisi di circuiti resistivi**


## 3.1 **Circuito serie**

Iniziamo con lo svolgere l’analisi del circuito elementare mostrato in figura, composta da una singola maglia di resistori alimentati da un generatore ideale di tensione. Con il termine "**analisi del circuito**" intendiamo che, assegnato il modo in cui i componenti sono collegati tra di loro ed i loro legami costitutivi, vogliamo determinare tutte le correnti e le tensioni del circuito. Tuttavia, nella pratica risolutiva si cerca di individuare un sottoinsieme il più possibile ristretto di correnti o di tensioni che si assumono come incognite del problema.
Il valore di dette incognite si ottiene imponendo la validità delle leggi di Kirchhoff e delle equazioni caratteristiche di ciascun elemento; per prima cosa elenchiamo dette leggi/equazioni per il circuito in figura 3.1:
![[Elettrotecnica-1793199284734.webp|294]]
#Figura(3.1).

- Applicando la legge di Kirchhoff delle correnti ai nodi del circuito, cioè nei punti di collegamento dei bipoli, si ha:$$i_{m} = i_{1} = i_{2} = i_{3} \quad (3.1)$$
- Si scrivono i legami costitutivi:$$v_{1} = R_{1} i_{1}\\v_2 = R_{2} i_{2}\\v_{3} = R_{3} i_{3}\\v_{4} = E$$$$(3.2)$$
- Si scrive la laegge di Kirchoff delle tensioni per la maglia:$$v_{4}=v_{1}+v_{2}+v_{3}\quad (3.3)$$

Il procedimento risolutivo consiste nell’organizzare opportunamente le equazioni di sopra in accordo coi seguenti passaggi logici:

1. Si assume $i_{m}$, la corrente che scorre nella maglia, come incognita del problema in quanto dalla sua conoscenza e dalla $(3.1)$ si possono facilmente dedurre i valori di tutte le altre correnti del circuito;
2. Si sostituisce $i_{m}$ nelle $(3.2)$ ottenendo:$$v_{1}=R_{1}i_{m}\\v_{2}=R_{2}i_{m}\\v_{3}=R_{3}i_{m}\\v_{4}=E$$$$(3.4)$$
3. Infine, si sostituiscono le $(3.4)$ nella $(3.3)$ pervenendo all'equazione finale:$$E=i_{m}(R_{1}+R_{2}+R_{3})\quad(3.5)$$

È quindi possibile risolvere quest'ultima equazione e ricavare l'espressione della corrente $i_{m}$:
$$i_{m}=\frac{E}{R_{1}+R_{2}+R_{3}}\quad (3.6)$$

e da essa determinare quella delle correnti nei resistori e della loro tensione, ottenendo:

> [!important] Formula
> $$v_{k}=E\frac{R_{k}}{R_{1}+R_{2}+R_{3}}\quad (3.7)$$
> 
> per $k=1,2,3$, che viene detta **formula del partitore di tensione**.
> 
> È facile verificare che la trattazione mostrata per tre resistori si estende al caso generale in cui i resistori collegati nella maglia siano $N$.
> Questo tipo di collegamento si dice di tipo serie in quanto i resistori sono attraversati dalla stessa corrente $i_{m}$ e le loro tensioni si sommano lungo la maglia.
> Nel caso generale si ottiene:
> $$i_{m}=\frac{E}{\sum_{i=1}^N R_{i}}\quad (3.8)$$
> e quindi:
> $$v_{k}=E\frac{R_{k}}{\sum_{i=1}^N R_{i}}\quad (3.9)$$
> per $k=1,\cdots,N$.



#Esempio Applichiamo il metodo al circuito in esempio in figura:
![[Elettrotecnica-1793200407011.webp|291]]
#Figura(3.2). *Esempio numerico di circuito serie*

Si ottiene:
$$i_{m}=\frac{24}{30+20+10}=0.4 \ A$$
e quindi:
$$v_{1}=0.4\cdot 30=12 \ V; \quad v_{2}=0.4\cdot 20=8 \ V; \quad v_{3}=0.4\cdot 10=4 \ V$$

Si noti che $v_{1}+v_{2}+v_{3}=12+8+4=24 \ V$, cioè il valore di tensione impresso dal generatore, come deve essere dalla KVL applicata alla maglia; inoltre il valore $24 \ V$ si ripartisce tra i resistori in modo proporzionale alle resistenze.



## 3.2 **Circuito parallelo**

Nel secondo esempio analizziamo il circuito descritto in figura 3.3 (Sinistra) dove tre resistori ed un generatore ideale di corrente sono collegati ai medesimi nodi $A, B$: questo circuito viene talvolta chiamato "binodale".
Nella implementazione pratica questo circuito viene spesso realizzato sostituendo i due nodi con due conduttori (considerati ideali e modellabili come corto circuito) come mostrato in figura 3.3 (Destra).
![[Elettrotecnica-1793200741170.webp|524]]
#Figura(3.3). *(<u>Sinistra</u>) Circuito binodale; (<u>Destra</u>) realizzazione in cui i nodi vengono sostituiti da due corto circuiti*

Le leggi/equazioni che governano i due circuiti sono le stesse come di seguito riportato, quindi <u>è indifferente considerare l’uno o l’altro</u>:

- Dalla legge di Kirchoff delle tensioni si ha:$$v_{AB}=v_{1}=v_{2}=v_{3}\quad(3.10)$$
- Si scrivono i legami costitutivi nella forma controllata in tensione:$$i_{1}=G_{1}v_{1}\\i_{2}=G_{2}v_{2}\\i_{3}=G_{3}v_{3}\\i_{4}=I_{s}$$$$(3.11)$$
	dove $G_{K}=\frac{1}{R_{k}}$ indica la conduttanza del resistore $k$-esimo.

- Si scrive la legge di Kirchhoff delle correnti al nodo $A$ per il circuito in figura (sinistra) o equivalentemente alla superficie chiusa tratteggiata in rosso nel circuito in figura (destra):$$i_{4}=i_{1}+i_{2}+i_{3}\quad (3.12)$$
Il procedimento risolutivo segue i seguenti passaggi logici:

1. Si assume $v_{AB}$, cioè la tensione misurata ai nodi, come incognita del problema in quanto dalla sua conoscenza e dalla $(3.10)$ si possono facilmente dedurre i valori di tutte le altre tensioni del circuito;
2. Si sostituisce $v_{AB}$ nelle $(3.11)$ ottenendo:$$i_{1}=G_{1}v_{AB}\\i_{2}=G_{2}v_{AB}\\i_{3}=G_{3}v_{AB}\\i_{4}=I_{s}$$$$(3.13)$$
3. Infine, si sostituiscono le $(3.13)$ nella $(3.12)$ pervenendo all'equazione finale:$$I_{s}=v_{AB}(G_{1}+G_{2}+G_{3})\quad(3.14)$$
È quindi possibile risolvere tale equazione e ricavare l'espressione della tensione $v_{AB}$:
$$v_{AB}=\frac{I_{s}}{G_{1}+G_{2}+G_{3}}\quad (3.15)$$
e da essa determinare quella delle tensioni sui resistori e della loro corrente; si ottiene infatti:

> [!important] Formula
> $$i_{k}=I_{s}\frac{G_{k}}{G_{1}+G_{2}+G_{3}}\quad (3.16)$$
> 
> per $k=1,2,3$, che viene detta **formula del partitore di corrente**.
> 
> E’ facile verificare che la trattazione mostrata per tre resistori si estende al caso generale in cui i resistori collegati ai nodi siano $N$.
> Questo tipo di collegamento si dice di tipo parallelo in quanto i resistori hanno ai loro capi la stessa tensione $v_{AB}$ ed inoltre le loro correnti si sommano al nodo (o attraverso una superficie chiusa).
> Nel caso generale si ottiene:
> $$v_{AB}=\frac{I_{s}}{\sum_{i=1}^N G_{i}}\quad (3.17)$$
> e quindi:
> $$i_{k}=I_{s}\frac{G_{k}}{\sum_{i=1}^N G_{i}}=I_{s}\frac{\frac{1}{R_{k}}}{\sum_{i=1}^N \frac{1}{R_{i}}}\quad(3.18)$$
> per $k=1,\cdots,N$.

> [!tip] Formula
> La formula $(3.18)$ vale per qualunque numero $N$ di resistori in parallelo, tuttavia è istruttivo analizzare nello specifico il caso $N = 2$ di soli due resistori. In questo caso, per esempio nel calcolo di $i_{2}$, si trova:
> $$i_{k}=I_{s}\frac{\frac{1}{R_{1}}}{\frac{1}{R_{1}}+\frac{1}{R_{2}}}=I_{s}\frac{R_{2}}{R_{1}+R_{2}}$$
> Similmente per $i_{2}$ vale:
> $$i_{k}=I_{s}\frac{\frac{1}{R_{2}}}{\frac{1}{R_{1}}+\frac{1}{R_{2}}}=I_{s}\frac{R_{1}}{R_{1}+R_{2}}$$
> 


#Esempio Applichiamo il metodo al circuito in figura:
![[Elettrotecnica-1793202627352.webp|346]]
#Figura(3.4). *Circuito in parallelo con tre resistori*

Si ha:
$$v_{AB}=\frac{11}{\frac{1}{1}+\frac{1}{2}+\frac{1}{3}}=11\cdot\frac{6}{11}=6 \ V$$
da cui:
$$i_{1}=6\cdot \frac{1}{1}=6 \ A;\quad i_{2}=6\cdot \frac{1}{2}=3 \ A;\quad i_{3}=6\cdot \frac{1}{3}=2 \ A$$

Si noti che $i_{1}+i_{2}+i_{3}=11 \ A$, cioè il valore di corrente imposto dal generatore, come deve essere dalla KCL, inoltre il valore $11 \ A$ si ripartisce tra i resistori in modo proporzionale alle conduttanze e quindi inversamente proporzionale ai valori delle resistenze.


#Esempio Analizziamo il circuito in figura:
![[Elettrotecnica-1793202913169.webp|268]]
#Figura(3.5). *Circuito parallelo con due resistori*

In questo caso risulta:
$$i_{1}=1\cdot \frac{10}{11}\approx 0.91 \ A;\quad i_{2}=\cdot \frac{1}{11}\approx 0.09 \ A$$
cioè la corrente impressa dal generatore si ripartisce in modo da scorrere in larga misura nel resistore che "offre minore resistenza" (cioè maggiore conduttanza).



## 3.3 **Equivalenze tra bipoli**

Aggregando tra di loro bipoli elementari (es. resistori, generatori, corto circuiti) è possibile costruire circuiti elettrici composti, se tali circuiti composti sono collegati/accessibile all’esterno attraverso due terminali essi stessi sono dei bipoli (composti).
La figura 3.6 mostra due esempi di bipoli composti ottenuti (a sinistra) connettendo resistori e (a destra) collegando generatori ideali e resistori:
![[Elettrotecnica-1793291788401.webp|435]]
#Figura(3.6). *Bipoli composti ottenuti aggregando bipoli elementari*

I bipoli composti sono descritti dalle grandezze descrittive $v$ ed $i$ misurate ai morsetti e da un’equazione caratteristica che lega le grandezze descrittive, esattamente come in un bipolo elementare. Da ora in poi, dunque, <mark class="hltr-yellow">col termine bipolo ci riferiremo sia un bipolo elementare che ad un bipolo composto</mark>.

Si consideri ora un bipolo che chiamiamo Bipolo $A$, che si suppone composto da numerosi elementi collegati tra loro ed è descritto da un’equazione caratteristica in forma implicita $f_{A}(v, i) = 0$. Il Bipolo $A$ è collegato ad un bipolo esterno (che in generale può essere composto) che chiamiamo Rete Esterna, come mostrato in figura 3.7:
![[Elettrotecnica-1793291870868.webp|333]]
#Figura(3.7). *(<u>Alto</u>) Bipolo $A$ collegato ad una rete esterna; (<u>Basso</u>) Il Bipolo $A$ viene sostituito dal Bipolo $B$*

Si supponga che esista un bipolo, che chiameremo Bipolo $B$, molto più semplice di $A$, nel senso che $B$ è composta da pochissimi elementi (vedremo più avanti che esso può essere formato da un solo componente, un resistore, oppure da due elementi, un resistore ed un generatore ideale). Il Bipolo $B$ ha una caratteristica del tipo $f_{B}(v, i) = 0$.

> [!important] Definizione
> **Proprietà di equivalenza**: il Bipolo $B$ si dice equivalente al Bipolo $A$ se la sua caratteristica è uguale a quella di $A$, cioè $f_{A}(v, i) = f_{B}(v, i)$ (a meno di un fattore moltiplicativo, ad esempio la caratteristica $3v−i= 0$ è uguale a $6v−2i= 0$).

In particolare, se il Bipolo $B$ equivalente ad $A$ viene sostituito ad esso come mostrato in figura 3.7 (Basso), la Rete Esterna "non si accorge della sostituzione" in quanto le sue equazioni (leggi di Kirchhoff e legami costitutivi) rimangono gli stessi e quindi i valori delle variabili elettriche che le risolvono (indicate in figura come $v_{k}, i_{k}$) rimangono le stesse.
Il circuito equivalente lo è ai fini esterni, cioè al fine di calcolare le variabili elettriche nella Rete Esterna.

Una strategia di analisi dei circuiti elettrici che deriva dalla proprietà di equivalenza è quello di determinare il circuito equivalente di sottoparti complesse del circuito, collegate al resto come bipolo, e di sostituire ad esse il relativo bipolo equivalente in modo da semplificare la soluzione.



## 3.4 **Equivalente di circuiti di tipo serie**

Determiniamo l’equazione caratteristica di un bipolo composto dalla serie di $N$ bipoli elementari. Come mostrato in figura useremo il caso $N= 3$ come esempio illustrativo:
![[Elettrotecnica-1793292399780.webp|265]]
#Figura(3.8).

Il bipolo composto è descritto ai morsetti esterni dalle variabili $v$ ed $i$. Nell’ipotesi che ogni bipolo elementare sia **controllabile in corrente** e descritto dalla generica equazione caratteristica $v_{k}=f_{k}(i_{k})$ si ha:
$$i_{1}=i_{2}=i_{3}=i\\v_{1}=f_{1}(i_{1})\\v_{2}=f_{2}(i_{2})\\v_{3}=f_{3}(i_{3})\\v=v_{1}+v_{2}+v_{3}$$$$(3.19)$$
Da cui deriva l'espressione che definisce formalmente la caratteristica del bipolo composto:
$$v=f_{1}(i)+f_{2}(i)+f_{3}(i)\quad(3.20)$$


### 3.4.1 **Resistori in serie**

Si consideri ora lo scenario in cui i bipoli elementari siano resistori di resistenza $R_{k}$ come in figura e quindi $f_{k}(i_{k}) = R_{k}\cdot i_{k}$.
![[Elettrotecnica-1793292584414.webp|448]]
#Figura(3.9).

Dalla $(3.20)$ risulta:
$$v=R_{1}\cdot i+R_{2}\cdot i+R_{3}\cdot i=(R_{1}+R_{2}+R_{3})\cdot i\quad(3.21)$$

da cui si deduce che il bipolo composto ha una caratteristica di tipo resistore (cioè $V= R\cdot i$) dove il coefficiente $R$ è dato dalla somma delle tre resistenze elementari. Il bipolo composto è dunque equivalente ai fini esterni ad un unico resistore di valore:
$$R_{eq}=R_{1}+R_{2}+R_{3}$$

#Esempio Consideriamo il circuito in figura composto da una sola maglia:
![[Elettrotecnica-1793292753947.webp|466]]
#Figura(3.10).

I tre resistori in serie possono essere sostituiti da un unico resistore $R_{eq}=30+20+10=60 \ \Omega$ come mostrato nel circuito semplificato in figura (Destra). In quest'ultimo è ora molto più semplice calcolare $i_{m}=\frac{24}{60}=0.4 \ A$.

Si noti come nel circuito semplificato in figura 3.10 (Destra) si sia persa dell’informazione rispetto al circuito originale (per esempio $v_{1}$), tuttavia dopo aver determinato $i_{m}$ nel circuito semplificato, questa informazione può essere riguadagnata sostituendo il valore di detta corrente nel circuito originale. Per esempio $v_{1} = i_{m}\cdot 30= 12 \ V$.


### 3.4.2 **Serie di generatori di tensione**

Componiamo in serie due generatori di tensione ideali come mostrato in figura:
![[Elettrotecnica-1793293416413.webp|403]]
#Figura(3.11).

Si ha $v_{1} = E_{1}$ e $v_{2} =−E_{2}$ (si noti che nell’ottica della $(3.20)$ ciò corrisponde a $f_{1}(i_{1}) = E_{1} + i_{1} \cdot 0$ e $f_{2}(i_{2}) =−E_{2} + i_{2} \cdot 0$) da cui:
$$v=v_{1}+v_{2}=E_{1}-E_{2}\quad(3.22)$$
Il tipo di legame costitutivo del bipolo composto è dunque quello di un generatore ideale di tensione equivalente, cioè $v = E_{eq}$ per qualunque corrente, dove la tensione impressa $E_{eq}$ è data dalla somma con segno dei valori dei generatori elementari.

#Esempio Vediamo un’estensione della composizione serie risolvendo l’esercizio in figura:
![[Elettrotecnica-1793293537742.webp|419]]
#Figura(3.12).

Bilanciando le tensioni lungo la maglia:
$$v_{1}+E_{1}+v_{1}+E_{2}+v_{3}-E_{3}=0$$
e quindi usando la legge di Ohm si ha:
$$i_{m}R_{4}+E_{1}+i_{m}R_{1}+E_{2}+i_{m}R_{3}-E_{3}=0$$
che ordinata diventa:
$$i_{m}(R_{4}+R_{1}+R_{3})=E_{3}-E_{1}-E_{2}$$

Quest’ultima equazione è la stessa che governa il circuito mostrato in figura 3.12 (Destra) dove i generatori di tensione sono stati fatti "scivolare" lungo la maglia in modo da rendere più evidente che sono in serie. Lo stesso vale per i resistori.
Componendo in serie i generatori ed i resistori il circuito si semplifica in un generatore di tensione equivalente:
$$E_{eq}=E_{3}-E_{1}-E_{2}$$
collegato ad un resistore equivalente di valore:
$$R_{eq}=R_{4}+R_{1}+R_{3}$$


### 3.4.3 **Serie con generatore ideale di corrente**

La presenza di un generatore ideale di corrente in un circuito composto serie, come mostrato nelle figure:
![[Elettrotecnica-1793293809678.webp|417]]
#Figura(3.13). *Serie di un generatore di corrente con un generatore di tensione*

![[Elettrotecnica-1793293849062.webp|426]]
#Figura(3.14). *Serie di un generatore di corrente con un resistore*

dà origine a casi particolari in cui non è più possibile applicare la trattazione in $(3.20)$: infatti in questo caso **il generatore di corrente non è controllabile in corrente** e dunque non ammette equazione del tipo $v = f (i)$.
La soluzione si trova semplicemente osservando che in entrambi i casi in figura sono tali che la corrente $i$ del bipolo composto deve essere uguale a quella impressa, cioè $i= I_{s}$ e dunque che ai fini esterni il bipolo composto è equivalente ad un generatore di corrente di valore $I_{s}$.



## 3.5 **Equivalente di circuiti di tipo parallelo**

Passiamo al caso di un bipolo composto ottenuto collegando in parallelo $N$ bipoli elementari. Quale esempio illustrativo, useremo il caso $N= 3$ come mostrato in figura:
![[Elettrotecnica-1793294080240.webp|335]]
#Figura(3.15).

Le variabili $v$ ed $i$ descrivono il bipolo composto ai suoi morsetti esterni. Nell’ipotesi che ogni bipolo elementare sia **controllabile in tensione**, cioè descritto da un’equazione caratteristica del tipo $i_{k} = g_{k}(v_{k})$, avremo che:
$$v_{1}=v_{2}=v_{3}=v\\i_{1}=g_{1}(v_{1})\\i_{2}=g_{2}(v_{2})\\i_{3}=g_{3}(v_{3})\\i=i_{1}+i_{2}+i_{3}$$$$(3.23)$$
Da cui si deriva l'espressione che definisce formalmente la caratteristica del bipolo composto:
$$i=g_{1}(v)+g_{2}(v)+g_{3}(v)\quad(3.24)$$


### 3.5.1 **Resistori in parallelo**

Si consideri ora la circostanza in cui i bipoli elementari siano resistori di resistenza $R_{k}$ come in figura 3.16 e quindi $g_{k}(v_{k}) = G_{k} \cdot v_{k}$, dove $G_{k} = \frac{1}{R_{k}}$ è la conduttanza.
![[Elettrotecnica-1793294328069.webp|470]]
#Figura(3.16).

Dalla $(3.24)$ risulta:
$$i=G_{1}\cdot v+G_{2}\cdot v+G_{3}\cdot v=(G_{1}+G_{2}+G_{3})\cdot v=\left( \frac{1}{R_{1}}+\frac{1}{R_{2}}+\frac{1}{R_{3}} \right)\cdot v\quad(3.25)$$

da cui si deduce che il bipolo composto ha una caratteristica di tipo resistore (cioè $i= G\cdot v$) dove il coefficiente $G$ è dato dalla somma delle tre conduttanze elementari. Il bipolo composto è dunque equivalente ai fini esterni ad un unico resistore la cui conduttanza vale:
$$G_{eq}=G_{1}+G_{2}+G_{3}$$
o, se si preferisce, la cui resistenza vale:
$$R_{eq}=\frac{1}{\frac{1}{R_{1}}+\frac{1}{R_{2}}+\frac{1}{R_{3}}}\quad(3.26)$$

Vale anche la pena di osservare come tali formule sono di carattere generale e si estendono facilmente al caso $N$ qualunque, per cui $G_{eq}=\sum_{i=1}^N G_{i}$.
Esse assumono una forma da ricordare nel caso di soli due resistori, per $N= 2$ dalla $(3.26)$ si ottiene:
$$R_{eq}=\frac{1}{\frac{1}{R_{1}}+\frac{1}{R_{2}}}=\frac{R_{1}\cdot R_{2}}{R_{1}+R_{2}}$$

#Esempio Ritorniamo ad analizzare il circuito in figura 3.5 già risolto nell'esempio della [[#3.2 **Circuito parallelo**|sezione 3.2]]:
![[Elettrotecnica-1793294733779.webp|240]]
#Figura(3.17). *Circuito parallelo con due resistori*

Sfruttando l’uso dell’equivalente, siamo ora in grado di seguire un procedimento diverso, ovvero possiamo prima calcolare la resistenza equivalente del bipolo collegato al generatore di corrente:
$$R_{eq}=\frac{1\cdot 10}{1+10}=\frac{10}{11}\ \Omega$$
e quindi calcolare la tensione "a cavallo" del generatore di corrente:
$$v=1\cdot \frac{10}{11}=\frac{10}{11} \ V$$
da cui sarà poi immediato ricavare $i_{1}=\frac{10}{11} \ A$ ed $i_{2}=\frac{1}{11} \ A$.


#### #Esercizio(serie/parallelo di resistori) (1)

> [!question] Esercizio
> ![[Elettrotecnica-1793378297836.webp|325x179]]
> #Figura(3.18). *Circuito a scala*
> 
> Si consideri il circuito a scala mostrato in figura 3.18, ci viene richiesto di calcolare le correnti $I_{x}, I_{y}$. Si procede utilizzando la composizione serie e parallelo dei resistori e quindi il partitore di corrente.
> 
> *Suggerimento*: $6 \ \Omega$ e $3\ \Omega$ sono in parallelo e la loro composizione in serie con $4\ \Omega$ ciò porta al circuito in figura 3.19 (Alto). Questo si riduce ulteriormente, $4\ \Omega$ in serie con $2\ \Omega$ e la loro composizione in parallelo con $12\ \Omega$ porta al circuito in figura 3.19 (Basso). Da questo si calcola agevolmente $I_{z}$:
> $$I_z{} = \frac{18}{4+2}= 3\ A$$
> 
> Ora si procede a ritroso tra i circuiti successivamente ridotti, così dal circuito in figura 3.19 (Alto), nota $I_{z}$ si calcola $I_{r}$ col partitore di corrente:
> $$I_{r}=I_{z}\frac{12}{12+6}=2 \ A$$
> Infine tornando al circuito di partenza in figura 3.18, si può valutare $I_{x}$ e $I_{y}$, ovvero:
> $$I_{x}=I_{r}\frac{6}{3+6}=\frac{4}{3}\ A\\I_{y}=I_{r}\frac{3}{3+6}=\frac{2}{3}\ A$$
> 
> Si noti che $I_{x}+I_{y}=I_{r}$ come deve essere.
> 
> ![[Elettrotecnica-1793378358994.webp|276x143]]![[Elettrotecnica-1793378367995.webp|276x209]]
> #Figura(3.19). *Riduzioni del circuito a scala*


#### #Esercizio(serie/parallelo di resistori) (2)

> [!question] Esercizio
> ![[Elettrotecnica-1793378518848.webp|247x231]]
> #Figura(3.20). *Rete resistiva*
> 
> Si consideri ora il circuito resistivo in figura, ci viene richiesto di calcolare la resistenza equivalente vista ai morsetti $B−D$.
> Questo significa che la rete va pensata collegata ad una rete esterna ai morsetti specificati come mostrato in figura 3.21:
> 
> ![[Elettrotecnica-1793378577631.webp|331]]
> #Figura(3.21). *Calcolo di $R_{eq}$ ai morsetti specificati $B-D$*
> 
> In questo caso la corrente i scorre attraverso le resistenze $R_{2}$ ed $R_{4}$ che sono dunque in serie. Viceversa, le resistenze $R_{1}$ ed $R_{3}$ sono "<u>flottanti</u>" (cioè in serie con un circuito aperto) e quindi hanno correnti nulle. Vale dunque:
> $$R_{eq} = R_{2} + R_{4}$$
> 
> Quanto vale la resistenza vista ai morsetti $A−C$ e quella vista ai morsetti $A−B$?


#### #Esercizio(serie/parallelo di resistori) (3)

> [!question] Esercizio
> ![[Elettrotecnica-1793378918070.webp|215]]
> #Figura(3.22). *Esempi di vari circuiti con resistori in parallelo/serie*
> 
> Analizziamo ora i circuiti mostrati in figura 3.22 partendo dal primo caso $A$.
> 
> **A)** In questa configurazione $R_{1}$ ed $R_{2}$ sono in parallelo, infatti $v_{1} = v_{2}$ e $I_{s} = i_{1} + i_{2}$. Quindi applicando la formula del partitore di corrente si ha per esempio:
> $$i_{2}=I_{s}\frac{R_{1}}{R_{1}+R_{2}}$$
> e la relativa tensione vale:
> $$v_{2}=i_{2}R_{2}=I_{s}\frac{R_{1}R_{2}}{R_{1}+R_{2}}$$
> che correttamente conferma la composizione parallelo dei due resistori.
> 
> **B)** $R_{1}$ è in serie con $R_{3}$ mentre $R_{4}$ è in serie con $R_{2}$. Le composizioni serie di questi resistori sono poi in parallelo al generatore di corrente. Quindi applicando il partitore di corrente:
> $$i_{1}=I_{s}\frac{R_{2}+R_{4}}{(R_{1}+R_{3})+(R_{2}+R_{4})}$$
> oppure:
> $$i_{2}=I_{s}\frac{R_{1}+R_{3}}{(R_{1}+R_{3})+(R_{2}+R_{4})}$$
> e la tensione del generatore vale:
> $$v_{x}=I_{s}\frac{(R_{1}+R_{3})(R_{2}+R_{4})}{(R_{1}+R_{3})+(R_{2}+R_{4})}$$
> 
> **C)** Si ha che $R_{3}$ ed $R_{4}$ sono in parallelo ed $R_{1}$ è in parallelo con $R_{2}$. Dal partitore di corrente troviamo:
> $$i_{1}=I_{s}\frac{R_{2}}{R_{1}+R_{2}}\\i_{3}=I_{s}\frac{R_{4}}{R_{3}+R_{4}}$$
> e quindi:
> $$I_{x}=i_{1}-i_{3}=I_{s}\frac{R_{2}}{R_{1}+R_{2}}-I_{s}\frac{R_{4}}{R_{3}+R_{4}}$$
> 
> Volendo si può anche ricavare la tensione:
> $$v_{x}=i_{3}R_{3}+i_{1}R_{1}=I_{s}\frac{R_{4}R_{3}}{R_{3}+R_{4}}+I_{s}\frac{R_{2}R_{1}}{R_{1}+R_{2}}$$


### 3.5.2 **Parallelo di generatori di corrente**

Componiamo in parallelo due generatori ideali di corrente come mostrato in figura:
![[Elettrotecnica-1793379643910.webp|505]]
#Figura(3.23).

Si ha $i_{1}=−I_{s_{1}}$ (<u>attenzione al segno!</u>), $i_{2} = I_{s_{2}}$ e $i_{3} = I_{s_{3}}$ (si noti che nell’ottica della $(3.24)$ ciò corrisponde a $g_{1}(v_{1}) =−I_{s_{1}} + v_{1} \cdot 0, g_{2}(v_{2}) = I_{s_{2}} + v_{2} \cdot 0$ e $g_{3}(v_{3}) = I_{s_{3}} + v_{3} \cdot 0$, da cui:
$$i=i_{1}+i_{2}+i_{3}=-I_{s_{1}}+I_{s_{2}}+I_{s_{3}}\quad(3.27)$$

Il tipo di legame costitutivo del bipolo composto è dunque quello di un generatore ideale di corrente equivalente, cioè $i= I_{eq}$ per qualunque valore di tensione, dove la corrente impressa $I_{eq}$ è data dalla somma con segno dei valori dei generatori elementari.


Esaminiamo ora il circuito in figura 3.24 (Sinistra)
![[Elettrotecnica-1793379741173.webp|452]]
#Figura(3.24).

Sommando le correnti al nodo $A$ si ha:
$$-I_{s_{4}}+\frac{v_{1}}{R_{1}}+I_{s_{2}}+\frac{v_{3}}{R_{3}}=0$$

Quindi osservando che $v_{1}=v_{3}=v_{AB}$ e riordinando si ottiene:
$$-I_{s_{4}}-I_{s_{2}}=v_{AB}\left( \frac{1}{R_{1}}+\frac{1}{R_{3}} \right)$$

Quest’ultima equazione è la stessa che governa il circuito mostrato in figura 3.24 (Destra), dove i generatori di corrente sono stati "spostati" (ma senza cambiare i punti in cui sono connessi) in modo da rendere evidente che sono in parallelo. Lo stesso vale per i resistori.
E’ ora possibile comporre i generatori di corrente ed i resistori in parallelo.


### 3.5.3 **Parallelo con generatore ideale di tensione**

La presenza di un generatore ideale di tensione in un circuito composto parallelo, come mostrato nella figura dà origine a un caso particolare in cui non è più possibile applicare la trattazione generale in $(3.24)$: infatti in questo caso **il generatore di tensione non è controllabile in tensione** e dunque non ammette equazione del tipo $i= f (v)$.
![[Elettrotecnica-1793380000228.webp|425]]
#Figura(3.25). *Parallelo con generatore ideale di tensione*

Tuttavia, la soluzione si trova semplicemente osservando come la tensione $v$ del bipolo composto sia "forzata" al valore $v = E_{s}$ dal generatore di tensione e dunque che ai fini esterni il bipolo composto è equivalente ad un generatore di tensione di valore $E_{eq} = E_{s}$.



## 3.6 **Casi senza soluzione o con indeterminazione**

Componendo in serie o in parallelo generatori ideali rispettivamente di corrente o tensione è possibile costruire sulla carta circuiti che non ammettono soluzione e quindi che non corrispondono a circuiti fisici. Taluni chiamano questi **circuiti patologici**.
Si osservi per esempio il circuito serie in figura:
![[Elettrotecnica-1793380162553.webp|305]]
#Figura(3.26). *Circuito patologico serie*

Se $I_{s_{1}} \ne I_{s_{2}}$, al nodo interno $n$ è violata la legge di Kirchhoff delle correnti, <u>il problema non ammette soluzione</u>. Per intenderci, sarebbe come voler risolvere un sistema di due equazioni nelle incognite $x$ ed $y$ del tipo:
$$\begin{cases}
x=1\\x=2
\end{cases}$$
Nel caso in cui, invece, $I_{s_{1}} = I_{s_{2}}$, non si ha violazione della KCL in $n$, in questo caso, ai fini esterni, la composizione serie è equivalente ad un solo generatore di valore $I_{eq} = I_{s_{1}} = I_{s_{2}}$.
La rete esterna si può risolvere, tuttavia dopo aver determinato $v$ non è possibile ripartire questo valore tra $v_{1}$ e $v_{2}$, avendo come unica informazione che $v_{1} + v_{2} = v$. Si ha una **indeterminazione di alcune variabili**.


#Esempio Nel circuito mostrato in figurasi ha che i due generatori di corrente, non violando la KCL al nodo $n$, sono equivalenti ai fini esterni ad un solo generatore di valore $I_{s}= 1 \ A$, come mostrato in figura 3.27 (Destra).
![[Elettrotecnica-1793380395382.webp|408]]
#Figura(3.27). *Circuito indeterminato*

Dunque, $i= 1 \ A$ e quindi dalla legge di Ohm (<u>attenzione al segno!</u>) $v =−1 \cdot 4=−4 \ V$.
Ora, tornando sul circuito di partenza sappiamo che $v_{1} + v_{2} =−4 \ V$ ma abbiano un grado di indeterminazione in $v_{1}$ e $v_{2}$ (posso fissare ad arbitrio una di loro).
Nell’analogia matematica, ciò corrisponde ad un sistema in $x$ ed $y$ del tipo:
$$\begin{cases}
x=1\\x=1
\end{cases}$$
che è **indeterminato** nella variabile $y$.

La stessa discussione vale per il circuito parallelo in figura:
![[Elettrotecnica-1793380526978.webp|297]]
#Figura(3.28). *Circuito patologico parallelo*

Se $E_{1} \ne E_{2}$, è violata la legge di Kirchhoff delle tensioni, <u>il problema non ammette soluzione</u>. Infine, nel caso in cui, invece, $E_{1} = E_{2}$, non si ha violazione della KVL, ai fini esterni, la composizione parallelo è equivalente ad un solo generatore di valore $E_{eq} = E_{1} = E_{2}$.
La rete esterna si può risolvere, tuttavia dopo aver determinato $i$ non è possibile ripartire questo valore di corrente tra $i_{1}$ e $i_{2}$, avendo come unica informazione che $i_{1} + i_{2} = i$. Si ha una **indeterminazione nelle due correnti**.



## 3.7 **Trasformazione serie-parallelo dei generatori reali**

Rimangono da considerare **due casi notevoli di bipolo composto**:

1) Il primo è formato dalla connessione serie di un generatore ideale di tensione e una resistenza, che viene talvolta indicato come modello del generatore reale di tensione o semplicemente modello serie:![[Elettrotecnica-1793380975833.webp|412]]
#Figura(3.29). Modello serie
	Componendo le caratteristiche dei due bipoli elementari (cioè sommando le tensioni nella maglia) è facile ottenere la caratteristica del bipolo composto:$$v=R_{s}\cdot i+E_{s}\quad(3.30)$$la cui rappresentazione grafica è mostra in figura:


2) Il secondo caso è formato