

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

- Il primo è formato dalla connessione serie di un generatore ideale di tensione e una resistenza, che viene talvolta indicato come modello del generatore reale di tensione o semplicemente **modello serie**:![[Elettrotecnica-1793380975833.webp|282]]
	#Figura(3.29). *Modello serie*
	Componendo le caratteristiche dei due bipoli elementari (cioè sommando le tensioni nella maglia) è facile ottenere la caratteristica del bipolo composto:$$v=R_{s}\cdot i+E_{s}\quad(3.30)$$la cui rappresentazione grafica è mostrata in figura:![[Elettrotecnica-1793381074372.webp|310]]
	#Figura(3.30). *Composizione grafica di tipo serie*
	
	Si noti che la caratteristica complessiva è una retta di pendenza pari a $R_{s}$ che interseca l’asse delle tensioni (luogo dei punti in cui $i= 0$) nel valore $v = E_{s}$ (detto tensione a vuoto) e l’asse delle correnti (luogo dei punti in cui $v = 0$) nel valore $i=\frac{−E_{s}}{R_{s}}$ (corrente di corti circuito).


- Il secondo caso è formato dalla connessione parallelo di un generatore ideale di corrente e una resistenza, che potremo indicare come modello del generatore reale di corrente o semplicemente **modello parallelo**:![[Elettrotecnica-1793381256952.webp|279]]
	#Figura(3.31). *Modello parallelo*
	Componendo le caratteristiche (cioè sommando le correnti al nodo) dei due bipoli elementari si ottiene la caratteristica del bipolo composto:$$i=v\cdot \frac{1}{R_{p}}-I_{p}$$la cui rappresentazione grafica è mostrata in figura:![[Elettrotecnica-1793381368409.webp|361]]
	#Figura(3.32). *Composizione grafica di tipo parallelo*
	Anche in questo secondo caso la caratteristica complessiva è una retta non passante per l’origine degli assi $(i, v)$. Tale retta caratteristica ha pendenza $R_{p}$ ed interseca l’asse delle tensioni $(i= 0)$ nel valore $v = I_{p} \cdot R_{p}$ (tensione a vuoto) e l’asse delle correnti $(v = 0)$ nel valore $i=−I_{p}$ (corrente di corto circuito).


<mark class="hltr-yellow">Poiché il circuito serie e quello parallelo sono rappresentati dallo stesso tipo di caratteristica sarà possibile renderli equivalenti tra loro per una opportuna scelta dei loro parametri circuitali</mark>. Per uguagliare le due caratteristiche si può imporre che le due rette abbiano la stessa pendenza, cioè $R_{p} = R_{s}$ e quindi che abbiano la stessa tensione a vuoto $E_{s} = I_{p}\cdot R_{p}$ o equivalentemente la stessa corrente di corto circuito $−I_{p} =-\frac{E_{s}}{R_{s}}$.

Da queste si ottengono le condizioni per il **passaggio da modello parallelo a serie**:
$$R_{s}=R_{p}\\E_{s}=I_{p}\cdot R_{p}$$$$(3.31)$$
e quelle per il **passaggio da serie a parallelo**:
$$R_{p}=R_{s}\\I_{P}=\frac{E_{s}}{R_{s}}$$$$(3.32)$$

Qualche semplice applicazione aiuta a fissare queste formule di trasformazione.

#Esempio Si consideri il generatore reale tipo serie:
![[Elettrotecnica-1793381745152.webp|483]]
#Figura(3.33). *Esempio di trasformazione serie parallelo*

Il corrispondente modello parallelo si ottiene dai conti:
$$I_{p}=\frac{12}{3}=4 \ A;\quad R_{p}=R_{s}=3 \ \Omega$$


Similmente, dato il generatore reale tipo parallelo in figura:
![[Elettrotecnica-1793381844742.webp|489]]
#Figura(3.34). *Esempio di trasformazione serie parallelo*

Il corrispondente modello serie risulta:
$$E_{s}=0.1\cdot 50=5 \ V;\quad R_{s}=R_{p}=50 \ \Omega$$

in cui <u>fare attenzione al verso corretto del generatore ideale di tensione</u>.


#### #Esercizio(composizione dei generatori) (1)

> [!question] Esercizio
> ![[Elettrotecnica-1793693709161.webp|389x192]]
> #Figura(3.35). *Circuito di immediata soluzione*
> 
> Dato il circuito in figura, calcolare come prima variabile la corrente $i_{a}$, quindi calcolate $i_{b}, i_{c}$ e la tensione $v_{d}$. 
> 
> Dopo avere letto la sezione successiva, determinate la <u>potenza elettrica erogata</u> dal generatore di corrente.


#### #Esercizio(composizione dei generatori) (2)

> [!question] Esercizio
> Dato il circuito in figura (Sinistra), si utilizzi la trasformazione serie/parallelo dei generatori per calcolare la tensione $v_{AB}$. Successivamente, si calcolino le correnti $i_{1}, i_{2}$ ed $i_{3}$ verificando che soddisfano la KCL al nodo $A$ (o $B$). Si assuma:
> $$R_{1} = R_{2} = R_{3} = 10 \ \Omega$$
> 
> ![[Elettrotecnica-1793694104554.webp|576]]
> #Figura(3.36). *Connessione parallelo di generatori reali di tensione/resistori*
> 
> Il procedimento è evidenziato in figura 3.36 (Destra): consiste nel trasformare i due generatori di tipo serie in parallelo. Sul circuito trasformato è poi possibile eseguire ulteriori semplificazioni come mostrato in figura 3.37, dove $R_{eq} = \frac{10}{3} \ \Omega$. Risulta quindi:
> $$v_{AB} = 3 \cdot \frac{10}{3}= 10 \ V$$
> 
> ![[Elettrotecnica-1793694153664.webp|472]]
> #Figura(3.37). *Composizione parallelo di generatori di corrente e resistenze*
> 
> Sostituendo questo valore nel circuito originale, figura 3.36(Sinistra), si può poi ricavare:
> $$i_{1}=\frac{V_{AB}-40}{10}=-3 \ A\\i_{2}=\frac{V_{AB}+10}{10}=2 \ A\\i_{3}=\frac{V_{AB}}{10}=1 \ A$$$$(3.34)$$


#### #Esercizio(composizione dei generatori) (3)

> [!question] Esercizio
> ![[Elettrotecnica-1793694403428.webp|348]]
> #Figura(3.38). *Collegamento serie di generatori reali di corrente e resistori*
> 
> Si analizzi il circuito mostrato in figura, in cui si chiede di determinare le due correnti $i_{x}$ ed $i_{y}$. Applicando la trasformazione parallelo-serie dei due generatori è facile ricavare immediatamente che:
> $$i_{x} = \frac{I_{s_{1}} \cdot R_{1}−I_{s_{3}} \cdot R_{3}}{R_{1} + R_{2} + R_{3}}$$
> 
> e quindi:
> $$i_{y} = i_{x} + I_{s_{3}}$$



## 3.8 **Potenza elettrica**

La concomitanza di una tensione e di una corrente elettrica in un bipolo (o ad una delle porte di un $N$-polo) corrisponde al manifestarsi di fenomeni di natura energetica. E’ esperienza comune che per far funzionare un dispositivo elettrico è necessario fornirgli energia (per esempio collegandolo ad una presa elettrica sfruttando l’energia chimica di una pila) o che il funzionamento di un dispositivo elettrico produce calore.

Tali fenomeni vengono studiati attraverso una nuova grandezza fisica molto importante nelle applicazioni: la **potenza elettrica**: per introdurla, consideriamo il circuito elementare in figura 3.39 dove una pila (o batteria) alimenta un bipolo ai capi del quale si misura una tensione $v$ ed una corrente $i$:
![[Elettrotecnica-1793694929188.webp|217]]
#Figura(3.39). *Aspetti energetici di un circuito elementare*

Si supponga di osservare il funzionamento del circuito durante un intervallo di tempo $\Delta t$. Ricordiamo che la tensione $v$ rappresenta il lavoro elettrico che si deve svolgere su una carica elettrica unitaria per spostarla dal punto $B$ al punto $A$ lungo una qualunque linea che abbia tali punti come estremi. Fisicamente tale lavoro è svolto dalla batteria ed è "sfruttato" o meglio è assorbito dal bipolo ad esso connesso. Dunque, se $\Delta Q$ rappresenta la carica elettrica totale che nell’intervallo $\Delta t$, entra dal morsetto $A$ del bipolo (attraverso la sezione del filo), si ha che la quantità:
$$L(\Delta t) = v\cdot \Delta Q$$
è il **lavoro elettrico assorbito dal bipolo** nell’intervallo $\Delta t$. Dividendo tale lavoro per l’intervallo di osservazione si ricava **il lavoro per unità di tempo** o **potenza elettrica** $p$:
$$p=\frac{\mathcal{L}(\Delta t)}{\Delta t}=v\cdot\frac{\Delta Q}{\Delta t}=v\cdot i$$

<mark class="hltr-yellow">La potenza elettrica è dunque data dal prodotto della tensione per la corrente</mark>.

La figura 3.40 mostra schematicamente l’esecuzione di un celebre esperimento dovuto a James Prescott Joule in cui un resistore elettrico alimentato da una pila viene inserito in uno strumento adiabatico (cioè isolato termicamente) in grado di misurare la quantità di calore prodotto al suo interno (questo avviene attraverso un termometro che fornisce la temperatura di un fluido interno):
![[Elettrotecnica-1793695073258.webp|176]]
#Figura(3.40). *Esperimento col calorimetro*

Con tale esperimento Joule dimostrò come il passaggio della corrente elettrica nel resistore corrispondesse alla generazione di calore (effetto Joule) e come tale calore fosse proporzionale al valore di $v \cdot i$.

Da un punto di vista fisico ne traiamo la seguente pittura: il prodotto $v \cdot i$ con $v$ ed $i$ misurate con la <u>convenzione degli utilizzatori</u>, rappresenta la **potenza elettrica assorbita** o **entrante** in un bipolo (o da una delle porte di un $N$-polo). la potenza viene misura in **watt** = ampere $\times$ volt $[W]$. Nel caso specifico del resistore fisico, il lavoro elettrico che corrisponde a tale potenza viene convertito in modo irreversibile in calore che si disperde nell’ambiente. Il resistore fisico può solo assorbire potenza e non erogarne. In accordo con questa evidenza sperimentale si ha che per il bipolo resistore, la cui caratteristica è $v = R \cdot i$ con $R > 0$, la potenza assorbita:
$$p=v\cdot i=R\cdot i^2=\frac{v^2}{R} \ge 0$$

è sempre positiva o nulla, esso viene detto **bipolo passivo**. La figura 3.41 mostra un modo comune di evidenziare la potenza $p$ assorbita da un resistore:
![[Elettrotecnica-1793695291251.webp|207]]
#Figura(3.41). *Bipolo passivo $p\ge 0 \ W$*


La figura 3.42, invece, mostra il caso di un generatore ideale di tensione ed uno di corrente. Si prenda per esempio il primo, la sua caratteristica impone $v = E_{s}$ ma nulla dice circa la variabile corrente il cui valore dipende da ciò che vi è ad esso collegato.
![[Elettrotecnica-1793695690737.webp|322]]
#Figura(3.42). *Bipoli attivi, $p$ può essere positiva, negativa o nulla*

In questo caso la potenza elettrica assorbita potrà essere positiva, negativa o nulla ed il bipolo, non essendo passivo, viene detto **attivo**. Fisicamente <mark class="hltr-yellow">un bipolo attivo rappresenta il modello di un dispositivo che è in grado di erogare potenza elettrica</mark>. Per esempio, un generatore di tensione è il modello (ideale) di una pila la quale è in grado di sfruttare il lavoro chimico interno per "immettere" lavoro elettrico all’interno del circuito elettrico: dal punto di vista del sistema circuito il generatore può erogare lavoro.


#Esempio Svolgiamo l’analisi del circuito mostrato in figura valutando le potenze elettriche in gioco:
![[Elettrotecnica-1793695844283.webp|246]]
#Figura(3.43). *Calcolo della potenza in un circuito*

La KVL si scrive:
$$20+i_{m}\cdot 10=10$$
da cui:
$$i_{m}=\frac{10-20}{10}=-1 \ A$$
Indichiamo con $p_{10 \ V}, p_{20 \ V}$ le **potenze assorbite** dai due generatori da $10$ e $20$ volt rispettivamente mentre indichiamo con $p_{R}$ la potenza assorbita dal resistore. Si ha:
$$p_{10 \ V}=10 \ V \cdot(+1 \ A)=+10 \ W\\p_{20 \ V}=20 \ V \cdot(-1 \ A)=-20 \ W\\p_{R}=(10 \ V- 20 \ V)\cdot(-1 \ A)=+10 \ W$$$$(3.35)$$

Osserviamo che: il generatore da $20 \ V$ assorbe una potenza elettrica negativa. Questo può anche essere riformulato dicendo che questo generatore eroga $20 \ W$. D’altra parte sia il generatore da $10 \ V$ che il resistore assorbono potenza e ciò è coerente fisicamente in quanto il resistore è passivo mentre il generatore essendo attivo può sia erogare che assorbire.

Infine si osservi un altro risultato tutt’altro che casuale: **la somma delle potenze assorbite dà zero**. Questo è una <u>conseguenza del teorema di Tellegen</u> visto nel [[#1.6 **Il teorema di Tellegen**|primo capitolo]]: Le tensioni e correnti ricavate dall’analisi di in un circuito fisico soddisfano sicuramente le KVL e le KCL che sono condizione necessaria e sufficienti affinché valga Tellegen (in aggiunta le tensioni e correnti fisiche soddisfano anche i legami costitutivi).
Ne consegue che la somma delle potenze assorbite, nota bene che ora sono potenze fisiche non virtuali, estesa a tutto il circuito, deve bilanciarsi a zero:
$$\sum_{k=1}^{N_{el}}v_{k}\cdot i_{k}=\sum_{k=1}^{N_{el}}p_{k}=0\quad(3.36)$$

con $N_{el}$ numero di elementi (bipoli o porte elettriche del circuito).
Il teorema di Tellegen riformulato con le potenze fisiche viene detto **Conservazione della potenza elettrica**: questo ci dice che un circuito elettrico è un <u>sistema energeticamente chiuso dove le potenze di natura elettrica in gioco si bilanciano a zero</u>, quindi misurandole con la convenzione degli utilizzatori (potenze assorbite), ed escludendo il caso in cui tutto è nullo, si ha che almeno un elemento assorbe potenza negativa, ovvero eroga potenza.




# **Capitolo IV: Circuiti con generatori pilotati**


## 4.1 **Generatori pilotati**

Introduciamo ora una nuova classe di elementi circuitali che sono indispensabili per "riprodurre" nel modello circuitale il comportamento di alcuni dispositivi elettronici. Uno di tali dispositivi è il transistore ("*transistor*" dall’inglese "TRANSferring"+"resISTOR").
![[Elettrotecnica-1793696905839.webp|554]]
#Figura(4.1).

La figura 4.1 (Sinistra) mostra il simbolo adottato negli schemi elettronici per il transistore di tipo MOS (metallo, ossido, semiconduttore): si presenta come un tripolo coi tre morsetti, G ("gate"), D ("drain"), S ("source").

Tipicamente esso viene impiegato come mostrato in figura 1.1 (Destra) raddoppiando uno dei suoi morsetti (es. il source) in modo da formare un doppio bipolo (tripolare) che è poi collegato a due bipoli esterni.

Come studierete nel corso di Elettronica, questo dispositivo presenta equazioni costitutive diverse in funzione della regione in cui vien fatto funzionare. In una di queste regioni, le correnti e tensioni misurate alle due porte esterne soddisfano a:
$$i_{1}=0\\i_{2}=g\cdot v_{1}\\\\(4.1)$$
dove $g$ è un parametro chiamato **transconduttanza** (misurata in $\Omega^{-1}$).

Da queste equazioni si vede come la porta $1$ si comporti elettricamente come un circuito aperto, cioè un misuratore ideale della tensione $v_{1}$ ai suoi capi; la porta $2$ presenta invece un tipo di comportamento nuovo: la corrente alla porta $2$ è linearmente proporzionale alla tensione misurata alla porta $1$.
Se confrontiamo la seconda equazione in $(1.1)$ con quella del bipolo resistore (figura 4.2) $i= G \cdot v$, con $G= \frac{1}{R}$, notiamo qualche similitudine.
![[Elettrotecnica-1793697049120.webp|143]]
#Figura(4.2). *Il bipolo resistore, $i=G\cdot v$*

Tuttavia, la differenza fondamentale è che in un resistore il legame lineare è tra variabili "locali" misurate alla stessa porta, mentre <u>nel caso del transistore il legame lineare riguarda grandezze misurate a porte diverse</u>, è un legame "non locale" o di "**trasferimento**" (da cui il nome).

Per rappresentare tale comportamento serve un elemento circuitale nuovo il cui simbolo è mostrato in figura 4.3 chiamato il **generatore di corrente pilotato** (o comandato) **in tensione**:
![[Elettrotecnica-1793697163896.webp|191]]
#Figura(4.3). *Generatore di corrente pilotato in tensione*

Il nome generatore di corrente pilotato ed il simbolo può indurre ad associare questo elemento a quello di un generatore di corrente ideale. E’ invece preferibile osservare come il suo legame costitutivo lo renda simile all’estensione di un resistore al caso multi-porta.


La figura 4.4 mostra un altro modello di generatore pilotato: **il generatore di corrente pilotato in corrente**.
![[Elettrotecnica-1793697323537.webp|254]]
#Figura(4.4). *Generatore di corrente pilotato in corrente*

Le equazioni costitutive sono:
$$v_{1}=0\\i_{2}=\beta\cdot i_{1}\\ \\(4.2)$$

La porta $1$ si comporta come un corto circuito, un misuratore ideale di corrente. La corrente misurata $i_{1}$ controlla il valore della corrente $i_{2}$ alla porta $2$. Il parametro $\beta$, adimensionale, si dice **guadagno di corrente**.


Accanto ai modelli di generatore di corrente pilotati esistono analoghi modelli di generatore di tensione pilotato. In particolare, la figura 4.5 mostra un **generatore di tensione pilotato in tensione**:
![[Elettrotecnica-1793697552271.webp|215]]
#Figura(4.5). *Generatore di tensione pilotato in tensione*

le cui equazioni sono date da:
$$i_{1}=0\\v_{2}=\alpha\cdot v_{1}\\ \\(4.3)$$

La porta $1$ è un circuito aperto e misura la tensione $v_{1}$; la porta $2$ è un generatore di tensione il cui valore è determinato da $v_{1}$ attraverso il parametro, adimensionale, $\alpha$ detto **guadagno di tensione**.
Questo tipo di modello, vedremo, serve tra l’altro per descrivere circuitalmente il comportamento di amplificatore di tensione (dispositivo essenziale in elettronica).


Infine, la figura 4.6 mostra il modello del **generatore di tensione pilotato in corrente**:
![[Elettrotecnica-1793697598585.webp|207]]
#Figura(4.6). *Generatore di tensione pilotato in corrente*

le cui equazioni sono date da:
$$v_{0}\\v_{2}=r\cdot i_{1}\\ \\(4.4)$$

La porta $1$ è un corto circuito e misura la corrente $i_{1}$; la porta $2$ è un generatore di tensione il cui valore è determinato da $i_{1}$ attraverso il parametro, misurato in $\Omega$, $r$ detto **transresistenza**.

> [!warning] Attenzione
> Concludiamo questa sezione osservando che a seguito dell’introduzione dei generatori pilotati i generatori ideali di tensione e corrente vengono spesso indicati come generatori indipendenti per distinguerli dai comandati.



## 4.2 **Analisi di circuiti che contengono generatori pilotati**

L’analisi consiste nella scelta di un sottoinsieme di variabili elettriche (correnti e tensioni) come incognite del problema matematico e quindi nell’organizzare opportunamente la scrittura delle leggi di Kirchhoff e dei legami costitutivi.
Esiste un "flusso risolutivo" che nel seguito delineiamo solo in via di principio (cioè non in modo sistematico) nei seguenti passaggi:

- Si scelgono un sottoinsieme di variabili descrittive (correnti o tensioni) come incognite cercando di includere il più possibile le variabili che pilotano i generatori pilotati ed in modo che le altre variabili dello stesso tipo siano da esse determinabili. *Per esempio*, ipotizziamo che le incognite siano le correnti $I_{x}, I_{y}$;

- Le altre correnti negli $N$ elementi del circuito (bipoli o porte), che indichiamo come $i_{1}, \cdots , i_{N}$, vengono espresse in funzione delle incognite tramite le KCL (ed eventualmente il legame costitutivo di generatori di corrente pilotati in corrente, se presenti). Avremo:$$i_1 = k_1(I_x, I_y)\\ \\ \vdots \\ \\ i_{N} = k_{N} (I_{x}, I_{y}) \\ \\(4.5)$$
- Nell’ipotesi che tutti i bipoli (e $N$-porte) siano controllabili in corrente, sarà possibile esprimere le tensioni su di essi in funzione delle correnti tramite i loro legami costitutivi:$$v_{1}=r_{1}(i_{1})=\tilde{r}_{1}(I_{x},I_{y})\\ \\ \vdots \\ \\ v_{N}=r_{N}(i_{N})=\tilde{r}_{N}(I_{x}, I_{y})\\ \\(4.6)$$
- Infine, si scriverà un numero di leggi di Kirchhoff delle tensioni pari al numero delle incognite. Ogni KVL sarà una equazione lineare che bilancia le tensioni lungo una maglia $\mathcal{M}$ del tipo:$$\sum_{i \in \mathcal{M}}v_{i}=\sum_{{i\in\mathcal{M}}}\tilde{r}_{i}(I_{x}, I_{y})=0\quad(4.7)$$
Il risultato finale è un sistema composto da un numero di equazioni lineari del tipo $(4.7)$ pari al numero delle incognite dalla cui soluzione si otterranno le incognite $I_{x}, I_{y}$.


Il procedimento di principio delineato sopra può a primo acchito apparire poco chiaro, esplicitiamolo meglio:

#Esempio.

![[Elettrotecnica-1793698744204.webp|374]]
#Figura(4.7). *Circuito con generatore di corrente pilotato in corrente; la porta pilotante è rappresentata dal corto circuito tra i nodi $A$ e $B$; la porta pilotata è tra i nodi $C$ e $D$*

I dati del problema sono:
$$E_{1}=10 \ V;\\R_{1}=100 \ \Omega\\ \beta = 9;\\E_{2}=20 \ V; \\ R_{2}=1 \ k\Omega \\ \\(4.8)$$

I passaggi risolutivi visti prima ora di concretizzano in:

- Si assume come incognita la corrente pilotante $i_{2}$, cioè $I_{x}=i_{2}$. La conoscenza di questa corrente è sufficiente per dedurre tutte le altre correnti infatti applicando la KCL al nodo $C$ si ha:$$i_{1}=i_{2}+\beta i_{2}=(1+\beta)I_x$$
- Si scrivono i legami costitutivi sui resistori:$$v_{1}=R_{1}i_{1}=R_{1}(1+\beta)I_{x}\\v_{2}=R_{2}i_{2}=R_{2}I_{x}\\ \\(4.9)$$
- Infine serve individuare una maglia sulla quale le tensioni dei suoi elementi siano o note o funzioni dell’incognita, nell’esempio essa è la maglia esterna per la quale:$$E_{1}+v_{1}+v_{2}-E_{2}=0$$ovvero:$$E_{1}+R_{1}(1+\beta)I_{x}+R_{2}I_{x}-E_{2}=0$$da cui si ottiene l'**equazione risolutiva**:$$[R_{1}(1+\beta)+R_{2}]\cdot I_{x}=E_{2}-E_{1}$$Risolvendo si ottiene l'incognita:$$I_{x}=\frac{10}{2000}=5 \ mA$$da cui poi è facile risalire alle altre grandezze:$$i_{1}=(1+\beta)I_{x}=50 \ mA\\v_{1}=R_{1}i_{1}=5 \ V\\v_{2}=R_{2}I_{x}=5 \ V\\v_{CD}=E_{2}-v_{2}=15 \ V\\ \\(4.10)$$


In modo simile esiste un flusso risolutivo "duale" delineabile in via di principio in:

- Si assumono come incognite un gruppo di tensioni, per semplicità supponiamo siano solo due $V_{x}, V_y$;

- Le altre tensioni negli $N$ elementi del circuito (bipoli o porte), che indichiamo come $v_{1}, \cdots , v_{N}$, vengono espresse in funzione delle incognite tramite le KVL (ed eventualmente il legame costitutivo di generatori di tensione pilotati in tensione, se presenti). Avremo:$$v_{1}=k_{1}(V_{x},V_{y})\\ \\ \vdots \\ \\ v_{N}=k_{N}(V_{x}, V_{y})\\ \\(4.11)$$
- Nell'ipotesi che tutti i bipoli (e $N$-porte) siano controllabili in tensione, sarà possibile esprimere le correnti su di essi in funzione delle tensioni tramite i loro legami costitutivi:$$i_{1}=g_{1}(v_{1})=\tilde{g}_{1}(V_{x},V_{y})\\ \\ \vdots \\ \\i_{N}=g_{N}(v_{N})=\tilde{g}_{N}(V_{x},V_{y})\\ \\(4.12)$$
- Infine, si scriverà un numero di leggi di Kirchhoff delle correnti pari al numero delle incognite. Ogni KCL sarà una equazione lineare che bilancia le correnti attraverso un nodo $\mathcal{S}$ (o superficie chiusa) e sarà del tipo:$$\sum_{n\in \mathcal{S}}i_{n}=\sum_{n\in\mathcal{S}}\tilde{g}_{n}(V_{x},V_{y})=0\quad(4.13)$$
Il risultato finale è un sistema composto da un numero di equazioni lineari del tipo $(4.13)$ pari al numero delle incognite dalla cui soluzione si otterranno le incognite $V_{x}, V_{y}$.

Questo secondo flusso risolutivo è quello che storicamente ha avuto più successo in quanto è stato reso sistematico e quindi implementato nei codici software (o programmi) per la soluzione automatica dei circuiti elettrici, questi programmi sono detti simulatori circuitali.
Il metodo sistematico prende il nome di **Analisi Nodale** e verrà trattato nel dettaglio nella prossima sezione.



## 4.3 **Il metodo dell'Analisi Nodale**

<mark class="hltr-yellow">Nella sua forma semplice il metodo si applica nell’ipotesi che tutti gli elementi circuitali siano controllabili in tensione</mark>.

Dato un circuito formato da $N + 1$ nodi, che supponiamo di numerare da $0$ a $N$, e da $\mathcal{L}$ elementi (bipoli o porte di $N$-poli), il metodo consiste nei seguenti passi che descriveremo con l’aiuto dello schema mostrato in figura:
![[Elettrotecnica-1793699798595.webp|511]]
#Figura(4.8). (<u>Sinistra</u>) Tensioni o potenziali di nodo; (<u>Destra</u>) La tensione su un generico elemento si ricava dai potenziali ai nodi a cui è connesso: $v = e_{A}−e_{B}$, da cui si ricava la corrente $i= g(v) = \tilde{g}(e_{A}, e_{B})$

- Si fissa **arbitrio** un nodo come riferimento, supponiamo sia il numero $0$, e quindi come incognite del problema si assumono gli $N$ potenziali di nodo $e_{1}, e_{2}, \cdots , e_{N}$;
- Le tensioni sugli $\mathcal{L}$ elementi che compongono il circuito sono una funzione dei potenziali. Come mostrato in figura 4.8 (Destra) per il generico elemento collegato ai nodi $A$ e $B$, la tensione si scrive in funzione dei potenziali:$$v=e_{A}-e_{B}$$
- Nell’ipotesi che tutti i bipoli (e $N$-porta) siano controllabili in tensione, sarà possibile esprimere ogni corrente i nel generico elemento in funzione di una tensione e quindi, essendo quest’ultima una combinazione di potenziali, anche i sarà esprimibile come combinazione di potenziali. Si avrà:$$i=g(v)=\tilde{g}(e_{1},e_{2},\cdots,e_{N})$$
- Infine, avendo da determinare $N$ incognite, si scriverà un ugual numero di leggi di Kirchhoff delle correnti. Dette KCL impongono il bilancio delle correnti negli $N$ nodi, **senza considerare il riferimento**:$$\sum_{k\in Nodo}i_{k}=\sum_{k\in Node}\tilde{g}_{k}(e_{1},e_{2},\cdots,e_{N})=0\quad(4.14)$$
Il risultato finale è un sistema composto da $N$ equazioni lineari del tipo $(4.14)$ nelle $N$ incognite $e_{1}, e_{2}, \cdots , e_{N}$.


#Esempio.

Consolidiamo la comprensione applicando il metodo al circuito mostrato in figura. Si noti che i punti sul filo conduttore ideale collegato al nodo $0$ di riferimento han tutti lo stesso potenziale. Nel circuito compare un generatore di corrente pilotato dalla tensione $v_{12}$, dunque la porta di comando è data dal circuito aperto che possiamo immaginare esistere tra i nodi $1$ e $2$:
![[Elettrotecnica-1793700219875.webp|327]]
#Figura(4.9).

I dati del problema sono:
$$I_{s}=5 \ A\\R_{1}=R_{2}=R_{3}=1 \ \Omega\\g=2\ \Omega^{-1}\\ \\(4.15)$$

I passaggi dell'analisi nodale sono:

- Le incognite sono i potenziali di nodo $e_{1},e_{2}$;
- La tensione su $R_{1}$ è $e_{1}$, quella su $R_{3}$ è $e_{3}$ mentre la tensione su $R_{2}$ è data da:$$v_{12}=e_{1}-e_{2}$$
- È possibile esprimere le correnti in funzione dei potenziali tramite i legami costitutivi (infatti tutti gli elementi sono controllabili in tensione):$$i_{1}=\frac{e_{1}}{R_{1}}\\i_{2}=\frac{e_{1}-e_{2}}{R_{2}}\\i_{3}=\frac{e_{2}}{R_{3}}\\g\cdot v_{12}=g\cdot(e_{1}-e_{2})\\ \\(4.16)$$
- Infine, si impongono i bilanci di corrente nei due nodi:$$\begin{cases}
\frac{e_1}{R_1}+g\cdot(e_1-e_2)+\frac{e_1-e_2}{R_2}=0\\\frac{e_2}{R_3}-I_s-\frac{e_1-e_2}{R_2}=0
\end{cases}\quad (4.17)$$Riordiniamo:$$\begin{cases}(\frac{1}{R_1}+g+\frac{1}{R_2})\cdot e_1+(-g-\frac{1}{R_2})\cdot e_2=0\\-\frac{1}{R_2}\cdot e_1+(\frac{1}{R_2}+\frac{1}{R_3})\cdot e_2=I_s\end{cases}\quad(4.18)$$e sostituiamo i dati:$$\begin{cases}4e_1 -3e_2=0\\-e_1+2e_2=5\end{cases}\quad(4.19)$$

Otteniamo, come atteso, un <u>sistema lineare di due equazioni nelle due incognite</u>.
Dall’Algebra sappiamo che il problema matematico può avere una, nessuna o infinite soluzioni. Graficamente ogni equazione corrisponde ad una retta nel piano $e_{1}, e_{2}$ come mostrato in figura e la soluzione alla loro intersezione:
![[Elettrotecnica-1793700830659.webp|292]]
#Figura(4.10). *Rappresentazione grafica del sistema di due equazioni lineari, dove si è adottata la notazione $x = e_{1}$ e $y= e_{2}$*

<mark class="hltr-yellow">L’unicità della soluzione si avrà quando le pendenze delle due rette sono diverse, come nell’esempio svolto. Se le rette sono parallele, invece, avremo zero soluzione se esse non sono coincidenti (caso di sistema impossibile), mentre si avranno infinite soluzioni nel caso siano coincidenti (caso di sistema indeterminato). L’unicità della soluzione può essere espressa matematicamente nella condizione</mark>:
$$\det(\mathbf{A})\ne 0$$dove $\det(\cdot)$ indica il determinante e:$$\mathbf{A}=\begin{vmatrix}
4&-3\\-1&2
\end{vmatrix}\quad(4.20)$$è la matrice dei coefficienti del sistema lineare. Nel circuito dell'esempio si ha che:
$$\det(\mathbf{A})=8-3=5\ne 0$$
La soluzione è quindi **unica**.



## 4.4 **Analisi Nodale Modificata (MNA)**

<mark class="hltr-yellow">Nel caso in cui un elemento presente nel circuito non sia controllabile in tensione, il metodo dell’analisi nodale deve essere modificato</mark>.

Partiamo considerando il circuito mostrato in figura, con la relativa numerazione dei nodi e coi valori numerici:
![[Elettrotecnica-1793702238088.webp|313]]
#Figura(4.11). *Circuito con generatore di tensione connesso tra un nodo e il riferimento*

$$E_{s}=8 \ V\\R_{1}=R_{2}=R_{3}=1 \ \Omega\\g=2 \ \Omega^{-1}\\ \\(4.22)$$

In questo primo caso, un generatore ideale di tensione è collegato tra un nodo ed il riferimento. Il generatore di tensione ha un’equazione costitutiva del tipo $v = E_{s}$, dunque da essa non si può determinare la corrente $i_{G}$ che vi scorre in funzione della tensione ai suoi capi $v = e_{2}$, esso non è controllabile in tensione.
L’analisi nodale viene modificata assumendo $i_{G}$, cioè la corrente dell’elemento non controllabile in tensione, come incognita aggiuntiva del problema; in questo modo le incognite risultano $e_{1}, e_{2}$ e $i_{G}$. Le equazioni che scriveremo sono date da il bilancio delle correnti nei due nodi, come nell’analisi nodale semplice, <mark class="hltr-yellow">con l’aggiunta della relazione che il legame costitutivo dell’elemento non controllabile in tensione determina tra i potenziali di nodo</mark>:

$$\begin{cases}
\frac{e_{1}}{R_{1}}+g\cdot(e_{1}-e_{2})+\frac{e_{1}-e_{2}}{R_{2}}=0\\ \frac{e_{2}}{R_{3}}-\frac{e_{1}-e_{2}}{R_{2}}+i_{G}=0\\ e_{2}=E_{s}
\end{cases}\quad(4.23)$$

Sostituendo i numeri:
$$\begin{cases}
4e_{1}-3e_{2}=0\\-e_{1}+2e_{2}+i_{G}=0\\e_{2}=8 \ V
\end{cases}\quad(4.24)$$

Si giunge dunque ad un sistema di tre equazioni in tre incognite. Il metodo MNA è applicabile a qualunque tipo di circuito attraverso dei passaggi ben precisi che possono essere implementati in un codici automatici di calcolo (cioè programmi software) detti simulatori circuitali.
In generale il metodo MNA porta ad un numero relativamente grande di equazioni anche per piccoli circuiti, tuttavia questo non costituisce un problema in quanto il sistema di equazioni è poi risolto dal computer.

Per la soluzione "a mano", invece, laddove è possibile, si preferisce cercare di limitare la dimensione del problema da risolvere per evitare possibili errori di calcolo.

Per la soluzione a mano facciamo riferimento alla figura 4.12 e notiamo come sia ingenuo considerare $e_{2}$ come incognita in quanto essa è imposta al valore $e_{2} = E_{s} = 8 \ V$ dal generatore di tensione.
![[Elettrotecnica-1793702673458.webp|359]]
#Figura(4.12). *Nella soluzione a mano si assume come unica incognita $e_{1}$*

In tal modo, rimane come unica incognita il potenziale $e_{1}$ che potremo determinare direttamente scrivendo il bilancio al solo nodo $1$. Sostituendo i numeri avremo che il problema matematico si riduce alla sola:
$$\frac{e_{1}}{1}+2\cdot(e_{1}-8)+\frac{e_{1}-8}{1}=0\quad(4.25)$$

da cui $e_{1}=6 \ V$. Conoscendo $e_{1}= 6 \ V$ ed $e_{2}=8 \ V$ sarà poi possibile dedurre il valore di $i_{G}$ bilanciando le correnti al nodo $2$:
$$i_{G}=\frac{e_{1}-e_{2}}{1}-\frac{e_{2}}{1}=-10 \ A\quad(4.26)$$




<mark class="hltr-yellow">Un secondo caso da considerare è quello in cui l’elemento non controllabile in tensione sia collegato tra due nodi (e non al riferimento)</mark>, come nel circuito mostrato in figura coi dati numerici:
![[Elettrotecnica-1793702874907.webp|314]]
#Figura(4.13). *Circuito con generatore di tensione connesso tra due nodi*

$$E_{s}=1 \ V;\\I_{s}=1 \ A;\\R_{1}=R_{3}=1 \ \Omega;\\g=2 \ \Omega^{-1}\\ \\(4.27)$$

Scriviamo prima il metodo MNA genuino, come formulato in un codice automatico: le variabili incognite sono $e_{1},e_{2}$ e $i_{G}$. Si ha:
$$\begin{cases}
\frac{e_{1}}{R_{1}}+g\cdot(e_{1}-e_{2})+i_{G}=0 \\ \frac{e_{2}}{R_{3}}-i_{G}=I_{s}\\ e_{1}-e_{2}=E_{s}
\end{cases}\quad (4.28)$$

dove le prime due equazioni impongono il bilancio delle correnti ai nodi $1$ e $2$, mentre la terza esprime il legame costitutivo dell’elemento non controllato in tensione.
Le equazioni possono essere scritte in formato matriciale/vettoriale come:
$$\mathbf{A}\cdot \mathbf{\overrightarrow{x}}=\mathbf{\overrightarrow{b}}_{1}\cdot I_{s}+\mathbf{\overrightarrow{b}}_{2}\cdot E_{s}\quad(4.29)$$
dove:
$$\mathbf{A}= \begin{vmatrix}
\frac{1}{R_{1}}+g & -g & 1\\0 & \frac{1}{R_{3}} & -1\\ 1 & -1 & 0
\end{vmatrix};\quad\mathbf{\overrightarrow{b}}_{1}=\begin{vmatrix}
0 \\ 1 \\ 0
\end{vmatrix};\quad\mathbf{\overrightarrow{b}}_{2}=\begin{vmatrix}
0 \\ 0 \\ 1
\end{vmatrix}\quad \quad (4.30)$$
e le variabili incognite sono raccolte nel vettore seguente:
$$\mathbf{\overrightarrow{x}}=\begin{vmatrix}
e_{1} \\
e_{2} \\
i_{G}
\end{vmatrix}\quad(4.31)$$

La forma compatta $(4.29)$ sarà utilizzata nella nota seguente per esplorare le proprietà del sistema, cioè del circuito.

Sostituendo i valori numerici, invece, si ottiene:
$$\begin{cases}
\frac{e_{1}}{1}+2\cdot(e_{1}-e_{2})+i_{G}=0\\ \frac{e_{2}}{1}-1 \ A -i_{G}=0 \\
e_{1}-e_{2}=1 \ V
\end{cases}\quad(4.32)$$

Si lascia per esercizio la soluzione numerical di tale sistema.

Nell’implementazione a mano dell’analisi nodale è preferibile seguire il seguente procedimento che permette di ridurre la complessità risolutiva; il metodo discende dall’osservazione che il legame costitutivo del generatore di tensione impone un vincolo tra i potenziali $e_{1}$ ed $e_{2}$. Se per esempio si conoscesse $e_{1}$, sarebbe facile determinare $e_{2}$ come:
$$e_{2}=e_{1}-E_{s}=e_{1}-1 \ V\quad(4.33)$$
dunque questo ci permette di eliminare un'incognita.
La seconda osservazione è che la corrente $i_{G}$ compare nel bilancio al nodo $1$ con segno "$+$" mentre compare nel bilancio al nodo $2$ con segno "$-$". Sommando le due equazioni è dunque possibile eliminare $i_{G}$. L’equazione risultante:
$$\frac{e_{1}}{1}+2\cdot 1+\frac{(e_{1}-1)}{1}-1 \ A=0\quad(4.34)$$

esprime il bilancio attraverso una superficie chiusa che include al suo interno il generatore di tensione ed i nodi $1$ e $2$, come mostrato nella figura 4.14, tale superficie viene indicata col nome di **supernodo**:
![[Elettrotecnica-1793703659699.webp|313]]
#Figura(4.14). *Uso del supernodo*

Il metodo a mano dunque consiste nell’assumere come sola incognita $e_{1}$, esprimere $e_{2}$ in funzione di $e_{1}$ attraverso la $(4.33)$ e quindi scrivere il bilancio delle correnti attraverso il <u>supernodo</u> $(4.34)$. Risolvendo quest’ultima equazione si ottiene:
$$2e_{1}=0\rightarrow e_{1}=0 \ V$$
da cui $e_{2}=-1 \ V$. Volendo, bilanciando le correnti al nodo $1$, si determina:
$$i_{G}=-2\cdot E_{s}0-2 \ A$$


#Esempio Presentiamo un ulteriore esempio cui compare un generatore di tensione comandato dalla tensione $v_{A}$ come mostrato in figura coi parametri:
![[Elettrotecnica-1793703830229.webp|237]]
#Figura(4.15). *Uso del supernodo in presenza di un generatore pilotato*

$$E_{s}=3 \ V;\\ R_{1}=R_{2}=R_{3}=R_{4}=1 \ \Omega;\\ \alpha=1\\ \\(4.35)$$

In questo circuito sono due le porte che non sono controllabili in tensione: il generatore ideale $E_{s}$ e l’elemento $\alpha \cdot v_{A}$ collegato ai nodi $2$ e $34. Per queste due porte non è possibile esprimere le correnti che vi scorrono in funzione di tensioni e quindi di potenziali ai nodi.
Volendo applicare il metodo MNA genuino, quello implementabile automaticamente, dovremmo considerare 5 incognite e scrivere 5 equazioni. Lasciamo al lettore tale scrittura per esercizio. 

Mostriamo invece il metodo semplificato che meglio si presta alla soluzione a mano. Questo si basa sull’osservazione che $e_{1} = E_{s} = 3 \ V$ è nota.
Inoltre è possibile istituire un legame tra il potenziale $e_{3}$ ed il potenziale $e_{3} = v_{A}$:
$$e_{2}-e_{3}=\alpha e_{3}\rightarrow e_{2}=2e_{3}\quad(4.36)$$

In questo modo abbiamo ristretto le incognite alla sola $e_{3} = v_{A}$, basterà scrivere una equazione di bilancio delle correnti che non coinvolga nessuna delle correnti degli elementi non controllabili in tensione.
Tale equazione è il bilancio al supernodo che circonda i nodi $2$ e $3$:
$$\frac{e_{3}}{R_{4}}+\frac{2e_{3}}{R_{3}}+\frac{e_{3}-3 \ V}{R_{2}}+\frac{2e_{3}-3 \ V}{R_{1}}=0\quad(4.37)$$
da cui:
$$6e_{3}-3-3=0\rightarrow e_{3}= 1 \ V$$
e quindi $e_{2}=2 \ V$.




# **Capitolo V: Proprietà e teoremi dei circuiti lineari**


In questo capitolo esaminiamo le proprietà di un’ampia categoria di circuiti elettrici formati da un numero imprecisato (cioè qualunque) di resistori, generatori pilotati e generatori indipendenti collegati tra loro in tutti i modi possibili. Osserviamo come il legame costitutivo dei resistori e dei quattro generatori pilotati siano del tipo:
$$U= k \cdot W$$

dove $U$ e $W$ possono essere tensioni o correnti misurate alla stessa porta (nei resistori) o a porte diverse (nei generatori pilotati), mentre $k$ è un parametro reale (compreso il numero zero).
Questi legami sono di proporzionalità diretta (o lineari) tra le variabili in gioco.

Per i generatori indipendenti, invece il legame costitutivo è del tipo $v = E_{s}$ oppure $i= I_{s}$ dove $E_{s}$ e $I_{s}$ sono valori numerici reali non nulli. I generatori indipendenti non specificano legami di proporzionalità tra le variabili elettriche bensì introducono dei termini noti all’interno del problema matematico d’analisi.
Chiameremo questa categoria di sistemi elettrici col nome di **Circuiti Lineari**.


## 5.1 **Principio di sovrapposizione degli effetti**

Ricaviamo una proprietà generale dei circuiti lineari riferendosi al circuito "di test" mostrato in figura 5.1: esso contiene tutti i tipi di elementi di un circuito lineare generico (resistori, generatori indipendenti e un generatore do corrente pilotato dalla tensione $v_{2}$) mentre è sufficientemente semplice da condurre ad un problema matematico di limitata complessità.

Il problema d’analisi può, per esempio, venire formulato attraverso il metodo dell’analisi nodale applicata con intelligenza, ovvero trattando il generatore di tensione e la resistenza serie $R_{2}$ come un unico bipolo controllabile in tensione: in questo modo, basterà assumere come incognita la tensione di nodo $x$ e quindi bilanciare le correnti attraverso la superficie tratteggiata mostrata in figura:
![[Elettrotecnica-1793704485511.webp|386]]
#Figura(5.1).

Avremo:
$$-I_{s_{1}}+\frac{x}{R_{1}}+g\cdot(E_{s_{2}}-x)+\frac{x-E_{s_{2}}}{R_{2}}=0\quad(5.1)$$

Riordinando i termini, si ottiene l'equazione risolutiva:
$$\underbrace{ \left( \frac{1}{R_{1}}-g+\frac{1}{R_{2}} \right)}_{A}\cdot x=\underbrace{ 1}_{B_{1}}\cdot I_{s_{1}}+\underbrace{ \left( \frac{1}{R_{2}}-g \right)}_{B_{2}}\cdot E_{s_{2}}\quad(5.2)$$

L’incognita $x$ è moltiplicata per un coefficiente $A$ mentre il termine noto vede i valori impressi dai generatori indipendenti moltiplicati per due coefficienti $B_{1}$ e $B_{2}$. Detti coefficienti $A, B_{1}$ e $B_{2}$ sono determinati dai valori dei resistori e dei generatori pilotati (<u>non da quelli indipendenti</u>) e da come sono collegati tra loro.
Dunque, nell’ipotesi che il coefficiente $A \ne 0$, l’equazione ammette una ed una sola soluzione:
$$x=\underbrace{\frac{1}{A} \ B1}_{H_{1}}\cdot I_{s_{1}}+\underbrace{\frac{1}{A} \ B_{2}}_{H_{2}}\cdot E_{s_{2}}\quad(5.3)$$
in cui i valori dei generatori indipendenti sono moltiplicati per i coefficienti $H_{1}$ e $H_{2}$.
Facciamo le seguenti **osservazioni**:

- <u>Se i generatori indipendenti vengono spenti</u>, ponendo $I_{s_{1}} = 0$ e $E_{s_{2}} = 0$, la soluzione unica è quella nulla $x = 0$. Questo ci dice che i generatori indipendenti sono le **sorgenti** o **cause del fatto elettrico senza le quali nel circuito tutte le variabili sarebbero nulle**, ovvero il circuito sarebbe **spento** (o in <u>quiescenza</u>). Per questo motivo, talvolta i generatori indipendenti vengono indicati col nome di sorgente di tensione o di corrente.

- La variabile incognita $x$, come qualunque altra variabile nel circuito (si calcoli per esempio la corrente nel resistore $R_{1}$, essa sarà $i_{1}=\frac{x}{R_{1}}=\frac{H_{1}}{R_{1}}\cdot I_{s_{1}}+\frac{H_{2}}{R_{1}}\cdot E_{s_{2}}$ cioè di nuovo del tipo $i_{1}=\tilde{H}_{1}\cdot I_{s_{1}}+\tilde{H}_{2}\cdot E_{s_{2}}$; questo vale per ogni variabile nel circuito), risulta essere una combinazione lineare dei valori impressi dai generatori indipendenti. Cioè qualunque variabile che noi vogliamo osservare come la risposta o uscita del circuito sarà del tipo:$$x= H_{1} \cdot I_{s_{1}} + H_{2} \cdot E_{s_{2}}\quad(5.4)$$

Analizziamo ora lo scenario in cui nel circuito in figura 5.1 venga spento il generatore di tensione $E_{s_{2}}$ (che viene cortocircuitato) ed in cui l’unica sorgente sia $I_{s_{2}}$.
Dalla $(5.4)$ ricaviamo che la variabile di uscita $x$ assume il valore:
$$x'=H_{1}\cdot I_{s_{1}}$$
che rappresenta l'effetto dovuta alla sola causa $I_{s_{1}}$. In modo simile, possiamo spegnere il generatore di corrente $I_{s_{1}}$ (che diventa un circuito aperto) e lasciare agire la sola sorgente $E_{s_{2}}$, avremo l’effetto parziale:
$$x''=H_{2}\cdot E_{s_{2}}$$

Alla luce di queste considerazioni, possiamo affermare che l’espressione completa $(5.4)$ rappresenta la sovrapposizione degli effetti parziali dovuti a ciascuna sorgente (<u>indipendente</u>).
Le stesse osservazioni possono essere ripetute per il circuito mostrato nel [[#4.4 **Analisi Nodale Modificata (MNA)**|capitolo 4.4]]:
![[Elettrotecnica-1793705588150.webp|369]]
#Figura(5.2). *Circuito con generatore di tensione connesso tra due nodi*

Ricordiamo qui come le equazioni dell’Analisi Nodale Modificata portano al seguente sistema lineare:
$$\mathbf{A}\cdot \mathbf{\overrightarrow{x}}=\mathbf{\overrightarrow{b}}_{1}\cdot I_{s}+\mathbf{\overrightarrow{b}}_{2}\cdot E_{s}\quad(5.5)$$
dove:
$$\mathbf{A}= \begin{vmatrix}
\frac{1}{R_{1}}+g & -g & 1\\0 & \frac{1}{R_{3}} & -1\\ 1 & -1 & 0
\end{vmatrix};\quad\mathbf{\overrightarrow{b}}_{1}=\begin{vmatrix}
0 \\ 1 \\ 0
\end{vmatrix};\quad\mathbf{\overrightarrow{b}}_{2}=\begin{vmatrix}
0 \\ 0 \\ 1
\end{vmatrix}\quad \quad (5.6)$$

e le variabili incognite sono raccolte nel vettore seguente:
$$\mathbf{\overrightarrow{x}}=\begin{vmatrix}
e_{1} \\
e_{2} \\
i_{G}
\end{vmatrix}\quad(5.7)$$

Se la matrice $\mathbf{A}$ è **non singolare**, il sistema può essere risolto:
$$\mathbf{\overrightarrow{x}}=\mathbf{\overrightarrow{h}}\cdot I_{s}+\mathbf{\overrightarrow{k}}\cdot E_{s}\quad(5.8)$$

dove si sono introdotti i vettori:
$$\mathbf{\overrightarrow{h}}=(\mathbf{A}^{-1}\cdot\mathbf{\overrightarrow{b}}_{1})=\begin{vmatrix}
H_{1} \\
H_{2} \\
H_{3}
\end{vmatrix}\quad(5.9)\\
\mathbf{\overrightarrow{k}}=(\mathbf{A}^{-1}\cdot\mathbf{\overrightarrow{b}}_{2})=\begin{vmatrix}
K_{1} \\
K_{2} \\
K_{3}
\end{vmatrix}\quad(5.10)$$

Considerata allora una qualunque delle incognite, per esempio $x = e_{1}$, essa risulta data da una combinazione lineare delle sorgenti indipendenti:
$$e_{1}=x=H_{1}\cdot I_{s}+K_{1}\cdot E_{s}\quad(5.11)$$

Questo risultato, che esprime il **principio di sovrapposizione degli effetti**, si estende al caso generale in cui il circuito contenga un numero $\alpha$ qualunque di generatori indipendenti di corrente e un numero $\beta$ di generatori indipendenti di tensione, come mostrato in figura:
![[Elettrotecnica-1793706053053.webp|266]]
#Figura(5.3). *Generico circuito lineare in cui sono state messe in evidenza le sorgenti indipendenti. Una qualunque grandezza $x$ nel circuito, per esempio una tensione, risulta essere una combinazione lineari dei valori impressi dalle sorgenti*

Si avrà:
$$x=H_{1}\cdot I_{s_{1}}+\cdots +H_{\alpha}\cdot I_{s_{\alpha}}+K_{1}\cdot E_{s_{1}}+\cdots+K_{\beta}\cdot E_{s_{\beta}}\quad(5.12)$$

dove i coefficienti $H_{i}, K_{i}$ sono dei numeri reali che esprimono "l’<u>influenza</u>" di una data sorgente sulla variabile osservata.
Si potrà sfruttare questo risultato semplificando l’analisi del circuito in un insieme di problemi più semplici in cui agisce una sola sorgente per volta oppure gruppi di sorgenti per volta.

La figura 5.4 mostra il problema elementare in cui agisce <u>un solo generatore di corrente</u>, mentre la figura 5.5 mostra il problema elementare in cui agisce <u>un solo generatore di tensione</u>:
![[Elettrotecnica-1793706289329.webp|252]]
#Figura(5.4).
![[Elettrotecnica-1793706307037.webp|241]]
#Figura(5.5).


La soluzione completa sarà quindi ottenuta sommando le soluzioni parziali ottenute dai circuiti elementari.


#### #Esercizio 

Ripetiamo l'esercizio svolto nel [[#Esercizio(composizione dei generatori) (2)|terzo capitolo]] sfruttando la sovrapposizione degli effetti. Il circuito è riportato di seguito:
![[Elettrotecnica-1793706685603.webp|331]]
#Figura(5.6).

Spegniamo per primo $E_{s_{2}}$ e risolviamo il circuito semplificato in figura 5.7. Otteniamo:
![[Elettrotecnica-1793706721226.webp|232]]
#Figura(5.7).

dove $R_{2} \ || \ R_{3}=\frac{R_{2}R_{3}}{R_{2}+R_{3}}$. Quindi spegniamo $E_{s_{1}}$ e risolviamo il circuito semplificato in figura 5.8:![[Elettrotecnica-1793706822647.webp|277]]
#Figura(5.8).

da cui:
$$v_{AB}''=E_{s_{2}}\cdot (-1)\frac{R_{1} \ || \ R_{3}}{R_{2}+R_{1} \ || \ R_{3}}\quad(5.14)$$
dove $R_{1}\ || \ R_{3}=\frac{R_{1}R_{3}}{R_{1}+R_{3}}$. Sovrapponendo gli effetti si ha la soluzione completa:
$$v_{AB}=E_{s_{1}}\cdot K_{1}+E_{s_{2}}\cdot K_{2}$$

Sostituendo i numeri e ricordando i dati:
$$R_{1}=R_{2}=R_{3}=10 \ \Omega;\\E_{s_{1}}=40 \ V;\\E_{s_{2}}=10 \ V\\ \\(5.15)$$
Si calcola:
$$K_{1}=\frac{1}{3},\quad K_{2}=-\frac{1}{3}$$
da cui:
$$v_{AB}=\frac{E_{s_{1}}}{3}-\frac{E_{s_{2}}}{3}=\frac{40}{3}-\frac{10}{3}=10 \ V$$



## 5.2 **Equivalente Thévenin o tipo serie**

Siamo ora in grado di ricavare qual è il circuito equivalente più generale di una rete elettrica lineare comunque complessa ed accessibile esternamente da una coppia di morsetti (cioè un bipolo). Tale rete è mostrata in figura 5.9 e può contenere al suo interno resistori, generatori pilotati che formano l’insieme degli elementi resistivi, più generatori indipendenti, ovvero sorgenti di tensione e corrente:
![[Elettrotecnica-1793799730318.webp|401]]
#Figura(5.9). *Set-up sperimentale per determinare l’equivalente Thévenin*

Vogliamo determinare il legame che esiste tra le variabili $V$ ed $I$ misurate ai suoi morsetti. Per questo colleghiamo il bipolo ad una sorgente esterna di corrente che imprime una corrente $I$ che noi possiamo controllare e variare a nostro piacimento. Quale sarà la forma del legame serie $V= f (I)$?

Nella sola ipotesi che il circuito così costruito ammetta soluzione, vale il principio di sovrapposizione degli effetti che ci assicura che qualunque variabile in gioco sarà una combinazione lineare dei generatori indipendenti. Questo vale anche per la tensione $V$ che dunque si può scrivere:
$$V=H_{0}\cdot \mathbf{I}+\overbrace{H_{1}\cdot I_{s_{1}}+\cdots+K_{\beta}\cdot E_{s\beta'}}^{Generatori \ interni}\quad(5.16)$$

ovvero mettendo in evidenza l’effetto dovuto alla sorgente esterna $I$ a cui si aggiunge l’**effetto complessivo dovuto a tutti i generatori indipendenti interni**.
Per quanto riguarda il primo termine, si osserva che il coefficiente $H_{0}$ è dimensionalmente una resistenza e dunque è corretto indicarlo come $R_{eq}$. Il secondo termine è una tensione e quindi si può indicare come un unico valore $E_{eq}$. Con questa notazione, $(5.16)$ si riscrive:
$$V=R_{eq}\cdot I+E_{eq}\quad(5.17)$$

Questa espressione ci mostra che, nell’ipotesi di controllabilità in corrente, un bipolo lineare comunque complesso è equivalente alla serie di un generatore di tensione di valore $E_{eq}$ detta **tensione equivalente** con un resistore di valore $R_{eq}$ detta **resistenza equivalente**.
Ai fini esterni, la rete potrà essere sostituita dal circuito serie mostrato in figura, comunemente indicato come **equivalente Thévenin** o **equivalente serie**:
![[Elettrotecnica-1793800081718.webp|278]]
#Figura(5.10). *Circuito equivalente di Thévenin*


Il significato fisico dei due parametri del circuito equivalente è evidente se pensiamo alle due configurazioni sperimentali, dette prove semplici, che permettono la loro determinazione:

- Dalla $(5.17)$, si ha che:$$R_{eq}=\frac{V}{I}|_{generatore \ interno \ \ OFF}\quad\quad(5.18)$$Questa configurazione è mostrata in figura 5.11: **tutti i generatori indipendenti interni al bipolo sono spenti** mentre agisce all’esterno il generatore $I$. In questa condizione, $R_{eq}$ risulta essere il rapporto $\frac{V}{I}$.![[Elettrotecnica-1793800416079.webp|332]]
	#Figura(5.11). *Prova semplice per la determinazione di $R_{eq}$*


- In modo simile, dalla $(5.17)$ si ricava:$$E_{eq}=V|_{I=0}\quad\quad (5.19)$$Questa configurazione è mostrata in figura 5.12: **i generatori indipendenti interni al bipolo sono attivi mentre è spento il generatore esterno** $I= 0$. $E_{eq}$ risulta essere la tensione $V$ misurata "a vuoto" (cioè coi morsetti flottanti).![[Elettrotecnica-1793800501124.webp|422]]
	#Figura(5.12). *Prova semplice per la determinazione di $E_{eq}$*



#### #Esercizio(equivalenti) (1)

> [!question] Esercizio
> Ci viene richiesto di calcolare il circuito equivalente di tipo Thévenin del bipolo mostrato in figura ai morsetti $A-B$. Nella figura si riporta, con linea tratteggiata, la rete esterna che potrà essere connessa al bipolo.
> 
> ![[Elettrotecnica-1793800808350.webp|413x210]]
> #Figura(5.13). *Bipolo di cui si chiede l'eq. Thévenin*
> 
> 
> Applichiamo le due prove semplici:
> 
> - Per il calcolo di $R_{eq}$ si deve spegnere il generatore interno di tensione e applicare un generatore esterno di corrente, come mostrato in figura:![[Elettrotecnica-1793801115680.webp|315]]
> 	#Figura(5.14). *Prova semplice per la determinazione di $R_{eq}$*
> 	
> 	Notare che la corrente $I$ scorre nel resistore da $5 \ \Omega$ e poi si ripartisce in parti uguali tra i due resistori in parallelo da $10 \ \Omega$. La tensione $V$ che nasce ai capi $A-B$ è dunque data da:$$V=I\cdot 5 \ \Omega+\frac{I}{2}\cdot 10 \ \Omega=I\cdot\10 \ \Omega\longrightarrow R_{eq}=\frac{V}{I}=10 \ \Omega$$
> 	**Si noti come il valore di Req calcolato con la prova semplice definita in $(5.18)$ coincida con quello ottenuto usando le composizioni parallelo/serie dei resistori. La prova semplice rappresenta una generalizzazione della composizione parallelo/serie**.
> 
> 
> - Per il calcolo di $E_{eq}$ si mantiene acceso il generatore interno mentre si spegne quello esterno, ovvero si lasciano i morsetti $A-B$ flottanti con $I= 0$, come mostrato in figura:![[Elettrotecnica-1793801240834.webp|319]]
> 	#Figura(5.15). *Prova semplice per la determinazione di $E_{eq}$*
> 	
> 	Da questa è facile concludere che:$$E_{eq}=4 \ V \ \frac{10}{10+10}=2 \ V$$Da cui il circuito equivalente, ai fini esterni, mostrato in figura:![[Elettrotecnica-1793801409473.webp|428]]
> 	#Figura(5.16). *Equivalente serie*


#### #Esercizio(equivalenti) (2)

> [!question] Esercizio
> Nel secondo esercizio, ci viene richiesto di calcolare il circuito equivalente di tipo Thévenin del bipolo mostrato in figura, che contiene un generatore di corrente pilotato in corrente.
> 
> ![[Elettrotecnica-1793801560063.webp|249]]
> #Figura(5.17). *Bipolo composto contenente generatore pilotato*
> 
> 
> Applichiamo le due prove semplici:
> 
> - Per il calcolo di $R_{eq}$ spegneremo il generatore indipendente di tensione.
> 	**<u>Attenzione</u>**: **il generatore pilotato NON è una sorgente indipendente**, quindi si applica un generatore esterno di corrente, come mostrato in figura:
> 	![[Elettrotecnica-1793801934649.webp|246x208]]
> 	#Figura(5.18). *Prova semplice per la determinazione di $R_{eq}$*
> 	
> 	Bilanciando le correnti al nodo tratteggiato, siamo in grado di calcolare $I_{1}$ in funzione della corrente impressa $I$, infatti:$$I=4I+I_{1}\longrightarrow I_{1}=-3I$$da cui si ricava la tensione:$$v=v_{AB}=I_{1}\cdot 10 \ \Omega=(-30 \ \Omega)\cdot I$$e la $R_{eq}$:$$R_{eq}=-30 \ \Omega$$
> 	
> 
> Facciamo due **osservazioni**:
> 
> 1. In presenza di generatori pilotati non è in generale possibile calcolare la $R_{eq}$ utilizzando la composizione serie/parallelo di resistori ma è necessario utilizzare la definizione della prova semplice;
> 2. Con generatori pilotati, la $R_{eq}$ può risultare negativa.
> 
> 
> - Per il calcolo di $E_{eq}$ ripristiniamo il generatore indipendente di tensione e manteniamo a vuoto i morsetti $A-B$, come in figura:
> 	![[Elettrotecnica-1793802068581.webp|259x224]]
> 	#Figura(5.19). *Prova semplice per la determinazione di $E_{eq}$*
> 	
> 	In questa configurazione, si ha:$$0=4\cdot 0+I_{1}\longrightarrow I_{1}=0 \ A$$e quindi:$$E_{eq}=0\cdot 10 \ \Omega+5 \ V=5 \ V$$


#### #Esercizio(equivalenti) (3)

> [!question] Esercizio
> Nel terzo esercizio proposto, mostriamo come l’applicazione del concetto di equivalente possa semplificare la soluzione del circuito mostrato in figura (Sinistra), in cui viene richiesto di calcolare la corrente $I_{x}$ che circola in $R_{5}$.
> 
> ![[Elettrotecnica-1793802314941.webp|256]]
> #Figura (5.20).
> 
> $$E=9 \ V;\\R_{2}=R_{3}=3 \ \Omega\\R_{1}=R_{4}=R_{5}=6 \ \Omega\\ \\ (5.20)$$
> 
> 
> Il procedimento che si segue è quello di calcolare il circuito equivalente di tipo serie del bipolo collegato a $R_{5}$, come mostrato in figura 5.21 (Sinistra); quindi si collega il circuito equivalente alla resistenza $R_{5}$ come mostrato in figura 5.21 (Destra).
> ![[Elettrotecnica-1793802457826.webp|449]]
> #Figura(5.21). *Procedimento: si calcola l’equivalente ai morsetti $A-B$ (<u>Sinistra</u>) e si collega al resistore $R_{5}$ (<u>Destra</u>)*
> 
> Procediamo al <u>calcolo dell’equivalente Thévenin</u>:
> 
> - Per il calcolo di $R_{eq}$ spegniamo il generatore indipendente di tensione e applichiamo un generatore di corrente, come mostrato in figura:
> 	![[Elettrotecnica-1793802608992.webp|493]]
> 	#Figura(5.22). *Prova semplice per la determinazione di $R_{eq}$*
> 	
> 	Ragionando su questo circuito si vede come $R_{1}$ ed $R_{3}$ siano tra di loro in **parallelo** così come $R_{2}$ con $R_{4}$. Risulterà:$$v_{1}=I\frac{R_{3}}{R_{1}+R_{3}}\cdot R_{1}$$mentre:$$v_{2}=I\frac{R_{4}}{R_{2}+R_{4}}\cdot R_{2}$$e quindi:$$V=v_{1}+v_{2}=I\cdot(R_{1}||R_{3}+R_{4}||R_{2})$$Da cui si ricava che:$$R_{eq}=(R_{1}||R_{3}+R_{4}||R_{2})=2 \ \Omega+2 \ \Omega=4 \ \Omega$$Si noti come questo risultato si può ricavare ridisegnando il circuito come mostrato in figura 5.22 (Destra).
> 
> 
> - Per il calcolo di $E_{eq}$ determiniamo la tensione a vuoto nel circuito di figura:
> 	![[Elettrotecnica-1793802981001.webp|272]]
> 	#Figura(5.23). *Prova semplice per la determinazione di $E_{eq}$*
> 	
> 	In esso i resistori $R_{1}$ ed $R_{3}$ sono in serie così come i resistori $R_{2}$ ed $R_{4}$ sono in serie tra loro. Dunque:$$E_{eq}=E\frac{R_{3}}{R_{1}+R_{3}}-E\frac{R_{2}}{R_{2}+R_{4}}=9\frac{3}{9}-9\frac{6}{9}=-3 \ V$$Infine, sfruttando l’equivalente circuitale come in figura 5.21 (Destra), concludiamo che:$$I_{x}=\frac{-3 \ V}{4 \ \Omega+6 \ \Omega}=-0.3 \ A$$



## 5.3 **Equivalente Norton o tipo parallelo**

Data una rete elettrica lineare comunque complessa ed accessibile esternamente da una coppia di morsetti, vogliamo determinare il legame tra le variabili $V$ ed $I$ misurate ai suoi morsetti nella forma parallelo o controllata in tensione, cioè $I= g(V)$.
A questo fine applichiamo all’esterno un generatore di tensione come mostrato in figura:
![[Elettrotecnica-1793803213359.webp|360]]
#Figura(5.24). *Set-up sperimentale per determinare l’equivalente Norton*

Se il circuito così costruito ammetta soluzione, allora il principio di sovrapposizione degli effetti ci illumina sulla forma della variabile corrente $I$ che sarà del tipo:
$$I=K_{0}\cdot \mathbf{V}+\overbrace{H_{1}\cdot I_{s_{1}}+\cdots+K_{\beta}\cdot E_{s\beta'}}^{Generatori \ interni}\quad(5.21)$$

dove compaiono distinti l’effetto dovuto alla sorgente esterna $V$ e l’effetto complessivo dovuto a tutti i generatori indipendenti interni. Il primo coefficiente $K_{0}$ è dimensionalmente una conduttanza e può essere indicata come $G_{eq}$. Il secondo termine è una corrente e quindi si può indicare come un unico valore $I_{eq}$.
Con questa notazione, $(5.21)$ si riscrive:
$$I=G_{eq}\cdot V+I_{eq}\quad(5.22)$$

Questa espressione ci mostra che, nell’ipotesi di controllabilità in tensione, un bipolo lineare comunque complesso è equivalente ad un circuito elementare composto dal collegamento parallelo di un generatore di corrente di valore $I_{eq}$, detto **corrente equivalente**, e di un resistore di conduttanza $G_{eq}$, o se si preferisce di resistenza $R_{eq} = \frac{1}{G_{eq}}$.
Ai fini esterni, la rete potrà essere sostituita dal circuito parallelo mostrato in figura, comunemente indicato come **equivalente Norton** o **equivalente parallelo**.
![[Elettrotecnica-1793803531073.webp|328]]
#Figura(5.25). *Circuito equivalente di Norton; il resistore parallelo ha resistenza $R_{eq} = \frac{1}{G_{eq}}$*


Il significato fisico dei parametri dell’equivalente Norton emerge dalle **due prove semplici**, che permettono la loro determinazione:

- Dalla $(5.22)$ si ha che:$$G_{eq}=\frac{I}{V}|_{generatore \ interno \ \ OFF}\quad\quad(5.23)$$

	Questa configurazione è mostrata in figura:
	![[Elettrotecnica-1793803713768.webp|383]]
	#Figura(5.26). *Prova semplice per la determinazione di $G_{eq}$*
	
	**Tutti i generatori indipendenti interni al bipolo sono spenti mentre agisce all’esterno il generatore $V$**. In questa condizione, $G_{eq}$ risulta essere il rapporto $\frac{I}{V}$, cioè il rapporto tra la corrente che scorre nel bipolo a seguito dell’applicazione di una tensione.
	Si noti che, per lo stesso bipolo di partenza, **il circuito per il calcolo di $G_{eq}$ del modello Norton è esattamente lo stesso di quello usato per il calcolo di $R_{eq}$ nel modello Thévenin, ne consegue che tra questi parametri vale la relazione $G_{eq} = \frac{1}{R_{eq}}$**.


- In modo simile, dalla $(5.21)$ si ricava:$$I_{eq}=I|_{V=0}\quad \quad (5.24)$$Questa configurazione è mostrata in figura:
	![[Elettrotecnica-1793803953149.webp|413x219]]
	#Figura(5.27). *Prova semplice per la determinazione di $I_{eq}$; i morsetti del bipolo vengono cortocircuitati*
	
	I generatori indipendenti interni al bipolo sono accesi mentre è spento il generatore esterno $V= 0$. $I_{{eq}}$ risulta essere la corrente $I$ misurata coi morsetti $A-B$ cortocircuitati.



#### #Esercizio(equivalenti) (1)

> [!question] Esercizio
> Ripetiamo l’esercizio mostrato in [[#Esercizio(equivalenti) (1)|figura 5.13]] figura 5.13, riportato per comodità in figura ma ora con lo scopo di calcolarne l’equivalente Norton:
> ![[Elettrotecnica-1793804632165.webp|381]]
> #Figura(5.28).
> 
> 
> Applichiamo le due prove semplici:
> 
> - Per il calcolo di $G_{eq}$ si dovrà risolvere il circuito mostrato in figura:
> - 
> 	![[Elettrotecnica-1793804782529.webp|251]]
> 	#Figura(5.29). *Prova semplice per la determinazione di $G_{eq}$*
> 	
> 	Questo circuito è lo stesso risolto per calcolare la $R_{eq}$ di Thévenin tranne che ora si impone la tensione $V$. I calcoli saranno i medesimi:$$V=I\cdot 5 \ \Omega+\frac{I}{2}\cdot 10 \1 \Omega=I\cdot 10 \ \Omega\longrightarrow G_{eq}=\frac{I}{V}=0.1 \ \Omega^{-1}=\frac{1}{R_{eq}}$$
> 
> 
> - Per il calcolo di $I_{eq}$ si mantiene acceso il generatore interno mentre si cortocircuitano i morsetti esterni come mostrato in figura:
> - 
> 	![[Elettrotecnica-1793804902315.webp|334]]
> 	#Figura(5.30). Prova semplice per la determinazione di $I_{eq}$
> 	
> 	Da questa calcoliamo il parallelo di $5\ \Omega$ e $10\ \Omega$, che risulta $\frac{10}{3} \ \Omega$ e quindi calcoliamo la corrente erogata dal generatore:$$i_{1}=\frac{4 \ V}{10+\frac{10}{3}}=0.3 \ A$$Quindi si ha:$$I_{eq}=0.3 \ A(-1)\frac{10}{10+5}=-0.2 \ A$$La figura 5.31 mostra il circuito equivalente Norton confrontandolo con quello di Thévenin già calcolato. E’ evidente come il passaggio dall’uno all’altro può essere valutato con le trasformazioni serie/parallelo dei generatori reali viste nella [[#3.7 **Trasformazione serie-parallelo dei generatori reali**|terzo capitolo]]:
> 	
> 	![[Elettrotecnica-1793805084217.webp|439]]
> 	#Figura(5.31). *Circuito equivalente di Norton (<u>Sinistra</u>); confronto con l’eq. di Thévenin (<u>Destra</u>)*


#### #Esercizio(equivalenti) (2)

> [!question] Esercizio
> Nel secondo esercizio viene richiesto di determinare il circuito equivalente di tipo Norton del bipolo in figura:
> ![[Elettrotecnica-1793805312041.webp|277]]
> #Figura(5.32). *Bipolo con generatore di tensione pilotato in tensione*
> 
> 
> - Facciamo una nota importante: il parametro dell’equivalente Norton è la conduttanza $G_{eq}$ poiché si sta cercando il modello controllato in tensione. Tuttavia, nella pratica risolutiva e salvo casi particolari che vedremo nella prossima sezione, si può procedere alternativamente calcolando la $R_{eq}$, ovvero svolgendo una prova semplice in cui si applica un generatore di corrente, e quindi invertire la resistenza per determinare la conduttanza. La scelta di uno o dell’altro metodo dipende dalla facilità risolutiva del circuito che ne risulta. In questo esercizio, in presenza di un generatore pilotato da $v_{1}$, risulta più semplice controllare il bipolo in tensione come mostrato in figura:
> 	![[Elettrotecnica-1793805442570.webp|349x196]]
> 	#Figura(5.33). *Prova semplice per la determinazione di $G_{eq}$*
> 
> 	Analizzando questa configurazione, e osservando che $v_{1} = V$, troviamo:
> 	$$v_{2}=v_{1}+\alpha v_{1}=V\cdot(1+\alpha)$$
> 	da cui:
> 	$$I=\frac{I}{V}=\frac{1}{R_{1}}+\frac{(1+\alpha)}{R_{2}}$$
> 	
> 	E infine:
> 	$$G_{eq}=\frac{I}{V}=\frac{1}{R_{1}}+\frac{(1+\alpha)}{R_{2}}$$
> 
> 
> - Per il calcolo di $I_{eq}$ cortocircuitano i morsetti esterni come mostrato in figura:
> 	![[Elettrotecnica-1793805649683.webp|343]]
> 	#Figura(5.34). *Prova semplice per la determinazione di $I_{eq}$*
> 	
> 	E’ facile vedere che $v_{1} = v_{2} = 0 \ V$ e che:$$I_{eq}=0 \ A$$Com’era intuitivo aspettarsi poiché il bipolo non contiene sorgenti indipendenti, il suo circuito equivalente, sia di Norton che di Thévenin, è composto da un resistore di resistenza:$$R_{eq}=\frac{1}{G_{eq}}=\frac{1}{\frac{1}{R_{1}}+\frac{(1+\alpha)}{R_{2}}}$$



## 5.4 **Considerazioni conclusive**

Facciamo alcune note finali:

- Ci chiediamo, dato un bipolo lineare **esiste sempre il circuito equivalente** di tipo Thévenin o Norton? **La risposta è no**, l’esistenza dei due equivalenti dipende dalla controllabilità che ammette il bipolo.
	
	Consideriamo, per esempio, il semplice caso in cui il bipolo sia un generatore indipendente di corrente, che sappiamo non ammette la controllabilità in corrente. Le due prove semplici per il calcolo dell’eq. Thévenin portano a <u>due circuiti che NON hanno soluzione</u>, come mostrato in figura, in quanto violano la KCL.
	![[Elettrotecnica-1793806104745.webp|417]]
	#Figura(5.35). *Una sorgente di corrente non ammette equivalente Thévenin*
	
	Non è dunque possibile calcolare la $E_{eq}$ e nemmeno la $R_{eq}$ che risulta $\infty$. Il generatore indipendente di corrente ammette invece l’equivalente Norton formato da se stesso con una conduttanza $G_{eq} = 0$ in parallelo.
	
	
	In modo del tutto simile un bipolo formato da un solo generatore indipendente di tensione non ammette la controllabilità in corrente. Le due prove semplici per il calcolo dell’eq. Norton portano a <u>due circuiti che NON hanno soluzione</u>, come mostrato in figura, in quanto violano la KVL.![[Elettrotecnica-1793806180370.webp|423]]
	#Figura(5.36). *Una sorgente di tensione non ammette equivalente Norton*
	
	Non è dunque possibile calcolare la $I_{eq}$ e nemmeno la $G_{eq}$ che risulta $\infty$. Il generatore indipendente di tensione ammette invece l’equivalente Thévenin formato da se stesso con una resistenza $R_{eq} = 0$ in serie.


- Lo studio compiuto per calcolare gli equivalenti circuitali di un generico Bipolo Lineare, descritto dalle variabili alla porta $V$ ed $I$, ci ha condotti alle due forme esplicite $(5.17)$ e $(5.22)$. Queste possono essere riscritte nelle seguenti forme implicite:$$V-R_{eq}\cdot I-E_{eq}=0\\ \\ \\-G_{eq}\cdot V+I-I_{eq}=0$$
	che possono essere unificate nella forma implicita generale, talvolta indicata col nome di **modello affine**:$$M\cdot V+N\cdot I+C=0\quad\quad(5.25)$$dove $M, N$ e $C$ sono dei coefficienti reali (positivi, negativi o nulli).
	La scelta particolare di tali coefficienti riconduce il modello affine a casi noti:
		a) se $C= 0$, la $(5.25)$ si trasforma in:$$V=-\frac{N}{M}I$$cioè il modello si riduce a quello di un resistore di resistenza $\frac{−N}{M}$;
		b) se $N= 0$, la $(5.25)$ si trasforma in:$$I=-\frac{C}{M}$$cioè il modello si riduce a quello di una sorgente di tensione $E_{S} =\frac{−C}{M}$;
		c) se $M= 0$, la $(5.25)$ si trasforma in:$$I=-\frac{C}{N}$$cioè il modello si riduce a quello di una sorgente di corrente $I_{s}=\frac{−C}{N}$

	
	Assegnato che sia il legame costitutivo di un bipolo nella forma implicita $(5.25)$ è facile verificare se è controllabile in tensione e/o in corrente.
	
	Perché sia <mark class="hltr-yellow">controllabile in corrente</mark>, deve essere possibile esplicitare la tensione e quindi il **coefficiente $M$ deve essere non nullo**, infatti:$$V=\overbrace{-\frac{N}{M}}^{R_{eq}}\cdot I+\overbrace{-\frac{C}{M}}^{E_{eq}}\quad\quad(5.26)$$
	
	Affinchè sia <mark class="hltr-yellow">controllabile in tensione</mark>, deve essere possibile esplicitare la variabile corrente e quindi il **coefficiente $N$ deve essere non nullo**:$$I=\overbrace{-\frac{M}{N}}^{G_{eq}}\cdot V+\overbrace{-\frac{C}{N}}^{I_{eq}}\quad\quad(5.27)$$

> [!question] Quesiti
> - Dato il legame costitutivo:$$2 \cdot V-100\cdot I+16=0$$dire se il bipolo è controllabile in corrente, in tensione, e se è passivo. Disegnare un circuito elettrico equivalente.
> 
> - Dato il legame costitutivo:$$A \cdot V + B \cdot I= 0$$scrivere a quale condizione devono soddisfare i coefficienti $A$ e $B$ affinché il bipolo sia passivo.
> 
> - Un bipolo è descritto dal modello:$$2 \cdot V−100 \cdot I + 16= 0$$Quanto vale la corrente di cortocircuito?




# **Capitolo VI: Doppi bipoli**


## 6.1 **Il modello Doppio Bipolo**

Il modello di tipo doppio bipolo si applica per descrivere vari casi pratici di reti elettriche che siano accessibili all’esterno attraverso due coppie di morsetti. In questo senso, il doppio bipolo estende il modello del bipolo al caso due porte. Un primo caso pratico è quello di un generico circuito lineare (cioè composto da resistori, generatori pilotati ed eventualmente sorgenti indipendenti) che sia "chiuso" su due bipoli come mostrato in figura:
![[Elettrotecnica-1793807477897.webp|527]]
#Figura(6.1). *Circuito lineare collegato a due bipoli esterni*

Ogni coppia di morsetti esterni definisce una porta elettrica, in quanto la corrente entrante ad un morsetto esce dall’altro, ed è descritto da una corrente ed una tensione. In totale le variabili in gioco ai terminali del doppio bipolo sono quattro, $I_{1},V_{1},I_{2},V_{2}$.

Un altro caso, rilevante nelle applicazioni, è quello di un **tripolo elettrico** come quello mostrato in figura 6.2: il tripolo può essere descritto da un modello tipo doppio bipolo raddoppiando uno dei suoi tre morsetti in modo da formare due porte elettriche. Anche in questo caso si avranno quattro variabili elettriche descrittive. Si noti che in questo caso, a differenza del primo, tra i due terminali inferiori alle porte nati dallo sdoppiamento del morsetto comune esiste un corto circuito che li collega sicché il doppio bipolo viene talvolta indicato col nome di tripolare.
![[Elettrotecnica-1793807583297.webp|580]]
#Figura(6.2). *Un tripolo può venire modellato come doppio bipolo*



## 6.2 **Rappresentazioni R e G**

Determiniamo l’espressione matematica del legame costitutivo che lega le quattro variabili alle porte di un doppio bipolo partendo dalle rappresentazioni R e G.

Queste si ottengono generalizzando il procedimento visto nel [[#**Capitolo V Proprietà e teoremi dei circuiti lineari**|capitolo 5]] per il calcolo degli equivalenti serie (Thévenin) e parallelo (Norton) di un bipolo. Nel caso del bipolo, si procedeva imponendo una delle due grandezze alla porta attraverso l’applicazione di un generatore indipendente di corrente o di tensione. In un doppio bipolo, essendo due le porte, applicheremo due generatori indipendenti.

Partiamo dal caso mostrato in figura, che generalizza l’equivalente serie, in cui si impongono i valori delle due correnti $I_{2}$ ed $I_{2}$:
![[Elettrotecnica-1793896149187.webp|342]]
#Figura(6.3). *Set-up sperimentale per determinare la rappresentazione R*


Nell’ipotesi che il circuito così costituito ammetta, unica, la soluzione, ovvero che il doppio bipolo sia controllabile in corrente, è lecito applicare il <u>principio di sovrapposizione degli effetti</u>. Le due tensioni avranno espressioni matematiche che sono combinazione lineare dei due generatori esterni ed eventualmente di quelli interni se ce ne sono.
Tali espressione saranno del tipo:
$$V_{1}=r_{11}\cdot I_{1}+r_{12}\cdot I-2$+E_{1eq}\\ \\ V_{2}=r_{21}\cdot I_{1}+r_{22}\cdot I_{2}+E_{2eq}\\ \\ (6.1)$$

dove i coefficienti $r$ sono dimensionalmente delle resistenze in $\Omega$ che pesano l’effetto dei due generatori esterni, mentre i termini $E_{eq}$, misurati in volt, riassumo l’effetto dei generatori indipendenti interni sulle tensioni di porta; queste equazioni possono essere riscritte in forma compatta utilizzando la notazione attraverso vettori e matrici:
$$\overrightarrow{V}=\mathbf{R}\cdot\overrightarrow{I}+\overrightarrow{E}_{eq\quad(6.2)}$$

dove $\mathbf{R}$ indica la matrice dei coefficienti o parametri $R$:

$$\mathbf{R}=\begin{vmatrix}
r_{11} & r_{12} \\
r_{21} & r_{22}
\end{vmatrix}\quad(6.3)$$

mentre $\overrightarrow{V},\overrightarrow{I}, \overrightarrow{E}_{eq}$ indicano i vettori colonna:

$$\overrightarrow{V}=\begin{vmatrix}
V_{1} \\
V_{2}
\end{vmatrix};\quad\overrightarrow{I}=\begin{vmatrix}
I_{1} \\
I_{2}
\end{vmatrix};\quad\overrightarrow{E}_{eq}=\begin{vmatrix}
E_{1eq} \\
E_{2eq}
\end{vmatrix}\quad\quad(6.4)$$

Il significato fisico dei parametri risulta evidente dalle prove semplici attraverso le quali vengono definiti. Per esempio, i parametri che misurano l’effetto di $I_{1}$ sono:
$$r_{11}=\frac{V_{1}}{I_{1}}|_{I_{2}=0;\ gen. \ OFF}\\ \\ r_{21}=\frac{V_{2}}{I_{1}}|_{I_{2}=0, \ gen. \ OFF}\\ \\(6.5)$$
e corrispondono alla configurazione circuitale mostrata in figura:
![[Elettrotecnica-1793896648786.webp|342]]
#Figura(6.4). *Prova semplice per il calcolo di $r_{11}$ e $r_{21}$: agisce il solo generatore $I_{1}$, sono spente le sorgenti interne*


In modo simile, i parametri che misurano l’effetto di $I_{2}$ sono:
$$r_{12}=\frac{V_{1}}{I_{2}}|_{I_{1}=0;\ gen. \ OFF}\\ \\ r_{22}=\frac{V_{2}}{I_{2}}|_{I_{1}=0, \ gen. \ OFF}\\ \\(6.6)$$
e corrispondono alla configurazione circuitale mostrata in figura:
![[Elettrotecnica-1793896770900.webp|330]]
#Figura(6.5). *Prova semplice per il calcolo di $r_{12}$ e $r_{22}$: agisce il solo generatore $I_{2}$, sono spente le sorgenti interne*


Infine, i coefficienti:
$$E_{1eq}\quad=\quad V_{1}|_{I_{1}=0;I_{2}=0} \\ \\ E_{2eq}\quad=\quad V_{2}|_{I_{1}=0;I_{2}=0}\\ \\ (6.7)$$

Che corrispondono alla configurazione circuitale mostrata in figura:
![[Elettrotecnica-1793896907295.webp|357]]
#Figura(6.6). *Prova semplice per il calcolo di $E_{1eq}$ e $E_{2eq}$, entrambi i generatori esterni $I_{1}$ ed $I_{2}$ sono spenti, agiscono solo le sorgenti interne*


**Spesso, nelle applicazioni, il doppio bipolo NON contiene generatori indipendenti interni e quindi i coefficienti $E_{1eq}$ e $E_{2eq}$ sono nulli**.




Il caso mostrato in figura generalizza l’equivalente parallelo e consiste nell’imporre i valori delle due tensioni $V_{1}$ e $V_{2}$:
![[Elettrotecnica-1793897008784.webp|376]]
#Figura(6.7). *Set-up sperimentale per determinare la rappresentazione G*


Se il doppio bipolo é controllabile in tensione, le due correnti avranno espressione:

$$I_{11}=g_{11}\cdot V_{1}+g_{12}\cdot V_{2}+I_{1eq}\\ \\ I_{2}=g_{21}\cdot V_{1}+g_{22}\cdot V_{2}+I_{2eq}\\ \\(6.8)$$

dove i coefficienti $g$ sono ora dimensionalmente delle conduttanze in $\Omega^{-1}$ che pesano l’effetto dei due generatori esterni, mentre i termini $I_{eq}$, misurati in ampere, riassumo l’effetto dei generatori indipendenti interni sulle correnti di porta.
Queste equazioni possono essere riscritte in forma compatta utilizzando la notazione attraverso vettori e matrici:
$$\overrightarrow{I}=\mathbf{G}\cdot\overrightarrow{V}+\overrightarrow{I}_{eq}\quad(6.9)$$

dove $\mathbf{G}$ indica la matrice dei coefficienti o parametri $G$:

$$\mathbf{G}=\begin{vmatrix}
g_{11} & g_{12} \\
g_{21} & g_{22}
\end{vmatrix}\quad\quad(6.10)$$

mentre $\overrightarrow{I}_{eq}$ indica il vettore colonna:
$$\overrightarrow{I}_{eq}=\begin{vmatrix}
I_{1eq} \\
I_{2eq}
\end{vmatrix}\quad\quad(6.11)$$

È facile trovare una formula di trasformazione dalla rappresentazione serie $(6.2)$ a quella parallelo $(6.9)$. Per esempio, invertendo $(6.2)$ in modo da esplicitare il vettore delle correnti, si ha:
$$\overrightarrow{I}=\mathbf{R}^{-1}\cdot\overrightarrow{V}-\mathbf{R}^{-1}\cdot\overrightarrow{E}_{eq}$$
dove $\mathbf{R}^{-1}$ indica la matrice inversa. Confrontando con la $(6.9)$ vediamo che:
$$\mathbf{G}=\mathbf{R}^{-1}$$
e:
$$\overrightarrow{I}_{eq}=-\mathbf{R}^{-1}\cdot\overrightarrow{E}_{eq}$$

Il significato fisico dei parametri emerge dalle prove semplici. Per esempio, i parametri che misurano l’effetto di $V_{1}$ sono:
$$g_{11}\quad=\quad \frac{I_{1}}{V_{1}}|_{V_{2}=0;\ gen. \ OFF}\\ \\ g_{21}\quad=\quad \frac{I_{2}}{V_{1}}|_{V_{2}=0;\ gen. \ OFF}\\ \\(6.12)$$
e corrispondono alla configurazione circuitale mostrata in figura:
![[Elettrotecnica-1793898043516.webp|407]]
#Figura(6.8). *Prova semplice per il calcolo di $g_{11}$ e $g_{21}$: agisce il solo generatore $I_{1}$, sono spente le sorgenti interne*


In modo simile, i parametri che misurano l’effetto di $V_{2}$ sono:
$$g_{12}\quad=\quad \frac{I_{1}}{V_{2}}|_{V_{1}=0;\ gen. \ OFF}\\ \\ g_{22}\quad=\quad \frac{I_{2}}{V_{2}}|_{V_{1}=0;\ gen. \ OFF}\\ \\(6.13)$$
e corrispondono alla configurazione circuitale mostrata in figura:
![[Elettrotecnica-1793898174825.webp|430]]
#Figura(6.9). *Prova semplice per il calcolo di $g_{12}$ e $g_{22}$: agisce il solo generatore $V_{2}$, sono spente le sorgenti interne*


Infine, i coefficienti:
$$I_{1eq}\quad=\quad I_{1}|_{V_{1}=0;V_{2}=0} \\ \\ I_{2eq}\quad=\quad I_{2}|_{V_{1}=0;V_{2}=0}\\ \\ (6.14)$$

corrispondono alla configurazione circuitale mostrata in figura:
![[Elettrotecnica-1793898298255.webp|437]]
#Figura(6.10). *Prova semplice per il calcolo di $I_{1eq}$ e $I_{2eq}$, entrambi i generatori esterni $V_{1}$ e $V_{2}$ sono spenti, cioè corto circuitati, agiscono solo le sorgenti interne*



#### #Esercizio(vario) (1)

> [!question] Esercizio
> Ci proponiamo di calcolare i parametri della rappresentazione R del doppio bipolo mostrato in figura:
> 
> ![[Elettrotecnica-1793972883267.webp|308]]
> #Figura(6.11). *Circuito a stella*
> 
> 
> Esso nasce dal tripolo formato dal collegamento a stella di tre resistori. Data la semplicità, procediamo risolvendo direttamente la configurazione in cui agiscono entrambe le sorgenti esterne di corrente.
> Osservando che la corrente nel resistore $R_{3}$ è data da:
> $$i_{3}=I_{1}+I_{2}$$
> è facile determinare le due tensioni:
> $$V_{1}=I_{1}\cdot R_{1}+(I_{1}+I_{2})\cdot R_{3}\\ \\ V_{2}=I_{2}\cdot R_{2}+(I_{1}+I_{2})\cdot R_{3}\\ \\(6.15)$$
> 
> da cui, riordinando si ottiene la rappresentazione voluta:
> $$V_{1}=I_{1}\cdot \overbrace{(R_{1}+R_{3})}^{r_{11}}+I_{2}\cdot \overbrace{R_{3}}{r_{12}}\\ \\ V_{2}=I_{1}\cdot \underbrace{R_{3}}_{r_{21}}+I_{2}\cdot \underbrace{(R_{2}+R_{3})}_{r_{22}}\\ \\(6.16)$$
> 
> a cui corrisponde la matrice:
> $$\mathbf{R}=\begin{vmatrix}
> R_{1}+R_{3} & R_{3} \\
> R_{3} & R_{2}+R_{3}
> \end{vmatrix}\quad\quad(6.17)$$
> 
> Non essendovi generatori indipendenti interni al doppio bipolo, sono zero i termini $E_{eq}$.
> È possibile verificare la correttezza dei coefficienti applicando le prove semplici. *Per esempio*, la prova semplice $(6.5)$ corrisponde al circuito in figura, da cui si trova:
> 
> ![[Elettrotecnica-1793973360336.webp|332x167]]
> #Figura(6.12). *Prova semplice*
> 
> $$V_{1}=I_{1}\cdot(R_{1}+R_{3})$$
> 
> che conferma il valore di $r_{11}$. **Questo coefficiente che appartiene alla diagonale della matrice descrive un effetto locale alla porta $1$**, ovvero qual è l’effetto di $I_{1}$ su $V_{1}$ quando $I_{2}$ è spento. Dal circuito in figura, si ricava anche che:
> $$V_{2}=I_{1}\cdot R_{3}$$
> 
> che conferma il valore del coefficiente $r_{21}$. **Questo coefficiente estradiagonale descrive un effetto non locale o di trasferimento**, ovvero qual è l’effetto di $I_{1}$ alla porta $1$ su $V_{2}$ alla porta 2, quando $I_{2}$ è spento.


#### #Esercizio(circuito a triangolo)

> [!question] Esercizio
> Proponiamo ora il calcolo dei parametri G del doppio bipolo in figura:
> 
> ![[Elettrotecnica-1793973639781.webp|313x167]]
> #Figura(6.13). *Circuito a triangolo*
> 
> Questo doppio bipolo nasce dal tripolo formato dal **collegamento a triangolo di tre resistori**. Anche in questo caso è possibile procedere risolvendo direttamente la configurazione in cui agiscono entrambe le sorgenti esterne di tensione. Osservando che la tensione sul resistore $R_{12}$ è data da:
> $$v_{12}=V_{1}-V_{2}$$
> è facile determinare le due correnti di porta:
> $$I_{1}=\frac{V_{1}}{R_{13}}+\frac{V_{1}-V_{2}}{R_{12}}\\ \\I_{2}=\frac{V_{2}}{R_{23}}+\frac{V_{2}-V_{1}}{R_{12}} \\ \\(6.18)$$
> 
> da cui, riordinando si ha la rappresentazione voluta:
> $$I_{1}=V_{1}\cdot\overbrace{(\frac{1}{R_{13}}+\frac{1}{R_{12}})}^{g_{11}}+V_{2}\cdot\overbrace{-\frac{1}{R_{12}}}^{g_{12}}\\ \\ I_{2}=V_{1}\cdot\underbrace{-\frac{1}{R_{12}}}_{g_{21}}+V_{2}\cdot\underbrace{(\frac{1}{R_{13}}+\frac{1}{R_{12}})}_{g_{22}}\\ \\(6.19)$$
> 
> a cui corrisponde la matrice:
> $$\mathbf{G}=\begin{vmatrix}
> \frac{1}{R_{13}}+\frac{1}{R_{12}} & -\frac{1}{R_{12}} \\
> -\frac{1}{R_{12}} & \frac{1}{R_{23}}+\frac{1}{R_{12}}
> \end{vmatrix}\quad\quad(6.20)$$
> 
> Non essendovi generatori indipendenti interni al doppio bipolo, sono zero i termini $I_{eq}$.
> Anche in questo caso, è possibile verificare la correttezza dei coefficienti calcolati seguendo la via semplificata delle prove semplici. *Per esempio*, la prova semplice $(6.12)$ corrisponde al circuito in figura, da cui si trova:
> ![[Elettrotecnica-1793974323189.webp|321]]
> #Figura(6.14). *Prova semplice*
> 
> $$I_{1}=V_{1}\cdot\left( \frac{1}{R_{13}}+\frac{1}{R_{21}} \right)$$
> 
> che conferma il valore di $g_{11}$. **Questo coefficiente sulla diagonale di $\mathbf{G}$ descrive un effetto locale alla porta $1$**, ovvero qual è l’effetto di $V_{1}$ su $I_{1}$ quando $V_{2}$ è spento.
> Dal circuito in figura si ricava anche che:
> $$I_{2}=V_{1}\cdot-\frac{1}{R_{12}}$$
> 
> che conferma il valore del coefficiente $g_{21}$. **Questo coefficiente estradiagonale descrive un effetto non locale o di trasferimento**, ovvero qual è l’effetto di $V_{1}$ alla porta $1$ su $I_{2}$ alla porta $2$, quando $V_{2}$ è spento.
> 
> Osserviamo infine che in entrambi i circuiti analizzati vale la proprietà $r_{12} = r_{21}$ e $g_{12} = g_{21}$. Quando le matrici $\mathbf{R}$ o $\mathbf{G}$ di un doppio bipolo **soddisfano questa simmetria si dice che il doppio bipolo è reciproco**.


#### #Esercizio(vario) (2)

> [!question] Esercizio
> Si richiede il calcolo dei parametri R, cioè controllati dalle variabili corrente, del doppio bipolo composto mostrato in figura:
> 
> ![[Elettrotecnica-1793974736403.webp|373]]
> #Figura(6.15). *Doppio bipolo di cui si chiede i parametri R*
> 
> 
> 
> La **prima prova semplice** è mostrata in figura 6.16. Si osserva che:
> $$g\cdot v+v\frac{1}{R}=I_{2}=0\longrightarrow v=0$$
> e quindi:
> $$V_{1}=R \ I_{1}\longrightarrow r_{11}=R\\ \\ V_{2}=r \ I_{1}\longrightarrow r-
> _{21}=r$$
> 
> ![[Elettrotecnica-1793974875346.webp|381]]
> #Figura(6.16). *Prova semplice: agisce solo $I_{1}$*
> 
> 
> La **seconda prova semplice** è mostrata in figura 6.17. Osservando che:
> $$r\cdot I_{1}=0$$
> si ha:
> $$g\cdot v+v\frac{1}{R}=I_{2}\longrightarrow V_{2}=v=I_{2}\frac{1}{g+\frac{1}{R}}$$
> dunque:
> $$r_{22}=\frac{1}{g+\frac{1}{R}}$$
> 
> Inoltre,
> $$V_{1}=(g\cdot v) \ R=\frac{g \ R}{g+\frac{1}{R}}\ I_{2}$$
> quindi:
> $$r_{12}=\frac{g \ R}{g+\frac{1}{R}}$$
> 
> ![[Elettrotecnica-1793975097386.webp|411]]
> #Figura(6.17). *Prova semplice: agisce solo $I_{2}$*
> 
> 
> Infine, la **terza prova** consiste nel ripristinare il generatore indipendente interno e spegnere entrambi i generatori esterni come mostrato in figura; osservando che $g \cdot v = 0$ e $r \cdot I_{1} = 0$ si ha:
> 
> ![[Elettrotecnica-1793975200802.webp|488]]
> #Figura(6.18). *Prova semplice in cui agisce solo $A$*
> 
> $$E_{eq_{1}}=V_{1}=-A \ R \\ \\ E_{eq_{2}}=V_{2}=0$$
> 
> La rappresentazione completa risulta:
> 
> $$V_{1}=R\cdot I_{1}+\frac{g \ R}{g+\frac{1}{R}}\cdot I_{2}-A \ R\\ \\V_{2}=r\cdot I_{1}+\frac{1}{g+\frac{1}{R}}\cdot I_{2}\\ \\(6.21)$$



## 6.3 **Altre rappresentazioni: tipo H, H' e T, T'**

Il caso di un doppio bipolo è più ricco rispetto a quello del bipolo avendo a disposizione quattro variabili alle porte anziché due. Di conseguenza esistono altri modi di controllare le variabili indipendenti in un doppio bipolo.

- Una prima modalità è quella in cui si impone una variabile corrente ad una porta ed una tensione all’altra. Le relative rappresentazioni, cioè le equazioni costitutive, vengono dette i **parametri ibridi**. Un primo scenario è mostrato in figura, e consiste nell’imporre i valori di $I_{1}$ e $V_{2}$.
	![[Elettrotecnica-1793975612835.webp|376]]
	#Figura(6.19). *Set-up sperimentale per determinare la rappresentazione H*
	
	Se il doppio bipolo è controllabile in questa modalità ibrida, allora le variabili dipendenti $V_{1}$ e $I_{2}$ avranno espressione:$$V_{1}\quad=\quad h_{11}\cdot I_{1}+h_{12}\cdot V_{2}+E_{1eq}\\ \\I_{2}\quad=\quad h_{21}\cdot I_{1}+h_{22}\cdot V_{2}+I_{2eq}\\ \\(6.22)$$
	In questo caso i coefficienti $h$, che pesano l’effetto delle sorgenti esterne, non sono dimensionalmente omogenei tra loro: $h_{11}$ si misura in $\Omega$, $h_{22}$ in $\Omega^{-1}$ mentre $h_{12}$ e $h_{21}$ sono adimensionali.
	Infine, i termini $E_{1eq}$ e $I_{2eq}$ riassumo l’effetto dei generatori indipendenti interni sulle variabili di porta.
	Anche in questo caso, è abitudine raccogliere i parametri $h$ in una matrice:$$\mathbf{H}=\begin{vmatrix}
	h_{11} & h_{12} \\ h_{21} & h_{22}
	\end{vmatrix}\quad\quad(6.23)$$
	Le prove semplici mettono in evidenza il significato fisico dei parametri. Per esempio, i parametri che misurano l’effetto di $V_{1}$ sono:$$h_{11}=\frac{V_{1}}{I_{1}}|_{V_{2}=0; \ gen. \ OFF}\\ \\h_{21}=\frac{I_{2}}{I_{1}}|_{V_{2}=0; \ gen. \ OFF}\\ \\(6.24)$$
	e corrispondono alal configurazione circuitale mostrata in figura:
	![[Elettrotecnica-1793976051293.webp|377]]
	#Figura(6.20). *Prova semplice per il calcolo di $h_{11}$ e $h_{21}$: agisce il solo generatore $I_{1}$, sono spente le sorgenti interne*

	
	In modo simile, i parametri che misurano l’effetto di $V_{2}$ sono:$$h_{12}=\frac{V_{1}}{V_{2}}|_{I_{1}=0; \ gen. \ OFF}\\ \\h_{22}=\frac{I_{2}}{V_{2}}|_{I_{1}=0; \ gen. \ OFF}\\ \\(6.25)$$
	e corrispondono alla configurazione circuitale mostrata in figura:
	![[Elettrotecnica-1793976208161.webp|332]]
	#Figura(6.21). *Prova semplice per il calcolo di $h_{12}$ e $h_{22}$: agisce il solo generatore $V_{2}$, sono spente le sorgenti interne*


	Infine, i coefficienti:$$E_{1eq}\quad=\quad V_{1}|_{I_{1=0};V_{2}=0}\\ \\I_{2eq}\quad=\quad I_{2}|_{I_{1=0};V_{2}=0}\\ \\(6.26)$$
	corrispondono alla configurazione circuitale mostrata in figura:
	![[Elettrotecnica-1793976344305.webp|380]]
	#Figura(6.22). *Prova semplice per il calcolo di $E_{1eq}$ e $I_{2eq}$, entrambi i generatori esterni $I_{1}$ e $V_{2}$ sono spenti, agiscono solo le sorgenti interne*




Chiaramente è possibile invertire le variabili di controllo alle porte, cioè imporre i valori di $V_{1}$ ed $I_{2}$ come mostrato in figura:

![[Elettrotecnica-1793976436250.webp|374]]
#Figura(6.23). *Set-up sperimentale per determinare la rappresentazione H'*


Questa configurazione porta alla rappresentazione coi parametri $h'$:

$$I_{1}\quad=\quad h_{11}'\cdot V_{1}+h_{12}'\cdot I_{2}+I_{1eq}\\ \\V_{2}\quad=\quad h_{21}'\cdot V_{1}+h_{22}'\cdot I_{2}+E_{2eq}\\ \\(6.27)$$

e relativa matrice:

$$\mathbf{H}'=\begin{vmatrix}
h_{11}' & h_{12}' \\
h_{21}' & h_{22}'
\end{vmatrix}\quad \quad (6.28)$$



- Un’ulteriore modalità di controllo del doppio bipolo consiste nel fissare come indipendenti entrambe le grandezze ad una porta e ricavare quelle all’altra porta in funzione delle prime. I relativi parametri vengono detti di trasmissione. La prima forma ha espressione:$$V_{1}\quad=\quad t_{11}\cdot V_{2}+t_{12}\cdot(-I_{2})+V_{1eq}\\ \\I_{1}\quad=\quad t_{21}\cdot V_{2}+t_{22}\cdot(-I_{2})+I_{1eq}\\ \\(6.29)$$
	in cui si scelgono come variabili indipendenti la tensione $V_{2}$ e la corrente $−I_{2}$, cioè misurata uscente dalla porta $2$.
	
	La seconda forma ha espressione:$$V_{2}\quad=\quad t_{11}'\cdot V_{1}+t_{12}'\cdot(-I_{1})+V_{2eq}\\ \\I_{2}\quad=\quad t_{21}'\cdot V_{1}+t_{22}'\cdot(-I_{1})+I_{2eq}\\ \\(6.30)$$
	in cui si scelgono come variabili indipendenti la tensione $V_{1}$ e la corrente $−I_{1}$ uscente dalla porta $1$.
	
	Si noti che i parametri di trasmissione non possono essere determinati riferendosi a configurazioni sperimentali simili a quelle viste per le altre rappresentazioni: questo perché non è possibile applicare simultaneamente un generatore di corrente ed uno di tensione alla stessa porta. Questa applicazione simultanea richiede l’uso di un componente che vedremo in seguito, chiamato l’**amplificatore operazionale ideale**. I parametri $t$ possono essere derivati attraverso calcoli a partire da altre rappresentazioni, come mostrato in seguito.



#### #Esercizio(calcolo dei parametri H, T)


> [!question] Esercizio
> Si richiede il calcolo dei parametri H del doppio bipolo tripolare mostrato in figura:
> 
> ![[Elettrotecnica-1793978031344.webp|293]]
> #Figura(6.24). *Doppio bipolo di cui si chiedono i parametri H*
> 
> 
> Riportiamo di seguito per comodità la rappresentazione H, senza termini dovuti ai generatori indipendenti:
> $$V_{1}\quad=\quad h_{11}\cdot I_{1}+h_{12}\cdot V_{2}+E_{1eq}\\ \\I_{2}\quad=\quad h_{21}\cdot I_{1}+h_{22}\cdot V_{2}+I_{2eq}\\ \\(6.31)$$
> 
> 
> La **prima prova semplice** è mostrata in figura 6.25, da cui si ricava:
> $$V_{1}=I_{1}R_{a}\longrightarrow h_{11}=R_{a}\\ \\ I_{2}=-I_{1}\longrightarrow h_{21}=-1$$
> ![[Elettrotecnica-1793978187872.webp|294]]
> #Figura(6.25). *Prova semplice*
> 
> 
> La seconda prova è mostrata in figura 6.26, da cui si ricava:
> $$V_{1}=1 \ V_{2}\longrightarrow h_{12}=1\\ \\ I_{2}=\frac{V_{2}}{R_{b}}\longrightarrow h_{22}=\frac{1}{R_{b}}$$
> ![[Elettrotecnica-1793978307508.webp|259]]
> #Figura(6.26). *Prova semplice*
> 
> 
> La rappresentazione H è dunque data dalle equazioni:
> 
> $$V_{1}\quad=\quad R_{a}\cdot I_{1}+1\cdot V_{2}\\ \\I_{2}\quad=\quad(-1)\cdot I_{1}+\frac{1}{R_{b}}\cdot V_{2}\\ \\(6.32)$$
> 
> o se si preferisce dalla matrice:
> 
> $$\mathbf{H}=\begin{vmatrix}
> R_{1} & 1 \\
> -1 & \frac{1}{R_{b}}
> \end{vmatrix}\quad \quad(6.33)$$
> 
> 
> 
> 
> Supponiamo ora di voler ricavare i parametri $t$ del doppio bipolo in figura, partendo dai parametri $h$ appena calcolati. Ricordando che nella rappresentazione $t$ le variabili dipendenti cioè che esplicitiamo sono $V_{1}$ ed $I_{1}$, elaboriamo sulla seconda delle $(6.32)$ per ricavare $I_{1}$:
> $$I_{1}=-I_{2}+\frac{1}{R_{b}}\cdot V_{2}\quad(6.34)$$
> 
> Sostituendo quest’ultima equazione nella prima di $(6.32)$, si ottiene:
> $$V_{1}=-R_{a}\cdot I_{2}+\frac{R_{a}}{R_{b}}\cdot V_{2}+V_{2}\quad(6.35)$$
> 
> Infine riordinando le $(6.35)$ e $(6.34)$ si deriva la rappresentazione T:
> 
> $$V_{1}\quad=\quad\left( 1+\frac{R_{a}}{R_{b}} \right)\cdot V_{2}+R_{a}\cdot(-I_{2})\\ \\I_{1}\quad=\quad \frac{1}{R_{b}}\cdot V_{2}+1\cdot(-I_{2})\\ \\(6.36)$$
> 
> Si fa notare che la stessa rappresentazione T si può ottenere riferendosi al circuito mostrato in figura 6.27, in cui il doppio bipolo è collegato a due bipoli non meglio precisati. Supponendo note le variabili alla porta $2$, disegnate in blu, si possono ricavare quelle alla porta $1$, disegnate in rosso.
> ![[Elettrotecnica-1793978798454.webp|331]]
> #Figura(6.27). *Circuito per il calcolo diretto dei parametri T*
> 
> Si ha:
> $$i_{b}=\frac{V_{2}}{R_{b}}$$
> da cui:
> $$I_{1}=i_{b}+(-I_{2})=\frac{V_{2}}{R_{b}}+(-I_{2})$$
> Inoltre,
> $$V_{1}=I_{1}\cdot R_{a}+V_{2}=\left( 1+\frac{R_{a}}{R_{b}} \right)\cdot V_{2}+R_{a}\cdot(-I_{2})$$
> che completa la verifica.



## 6.4 **Rappresentazione implicita**

In modo del tutto analogo a quanto visto per il caso del bipolo e del suo modello affine, anche per il doppio bipolo è possibile riscrivere una delle sei rappresentazioni in modo implicito cioè riportando tutti i termine allo stesso membro e quindi uguagliando a zero.
La forma generale di tale rappresentazione implicita sarà del tipo:

$$m_{11}\cdot V_{1}+m_{12}\cdot V_{2}+n_{11}\cdot I_{1}+n_{12}\cdot I_{2}+c_{1}=0\\ \\m_{21}\cdot V_{1}+m_{22}\cdot V_{2}+n_{21}\cdot I_{1}+n_{22}\cdot I_{2}+c_{2}=0\\ \\(6.37)$$

dove i coefficienti $m, n, c$ sono numeri reali (incluso lo zero).

Viceversa, assegnata la forma implicita $(6.37)$, sarà possibile ricavare una particolare forma esplicita in cui si ricavano due delle quattro variabili in funzione delle rimanenti, **se e solo se la matrice dei coefficienti che moltiplicano le variabili da esplicitare è non singolare**.


Vediamo un *esempio* in cui supponiamo che il doppio bipolo ammetta e sia nota la rappresentazione R che riscriviamo di seguito in forma implicita:
$$(-1)\cdot V_{1}+0\cdot V_{2}+r_{11}\cdot I_{1}+r_{12}\cdot I_{2}+E_{eq_{1}}=0\\ \\0\cdot V_{1}+(-1)\cdot V_{2}+r_{21}\cdot I_{1}+r_{22}\cdot I_{2}+E_{eq_{2}}=0\\ \\(6.38)$$
Possiamo ora chiederci, quale condizione devono soddisfare i coeffici- enti affinché esistano le rappresentazioni $G, H, T$?

Per l’esistenza di $G$ si deve poter ricavare le due variabili $I_{1}$ ed $I_{2}$ dalle tensioni. I coefficienti che moltiplicano queste variabili sono quelli della matrice $\mathbf{R}$, dunque questa deve essere non singolare affinché esista $G$.

Per l’esistenza della rappresentazione H, ricordiamo che essa consiste nell’esplicitare le variabili $V_{1}$ ed $I_{2}$. I coefficienti che moltiplicano queste variabili in $(6.38)$ formano la matrice:
$$\begin{vmatrix}
-1 & r_{12} \\
0 & r_{22}
\end{vmatrix}\quad \quad(6.39)$$

Questa è non singolare sse $r_{22}\ne 0$.

Infine, la rappresentazione T consiste nell’esplicitare $V_{1}$ e $I_{1}$ i cui coefficienti danno:
$$\begin{vmatrix}
-1 & r_{11} \\
0 & r_{21}
\end{vmatrix}\quad \quad(6.40)$$

La rappresentazione T esiste sse $r_{21} \ne 0$.



## 6.5 **Trasformazioni stella triangolo**

Consideriamo i tripoli resistivi, definiti ai nodi esterni $1, 2,$ e $3$, mostrati in figura, chiamati **circuito a stella** (<u>Sinistra</u>) ed a **triangolo** (<u>Destra</u>):

![[Elettrotecnica-1793980270045.webp|569]]
#Figura(6.28). *Circuito a stella ed a triangolo*


Dimostriamo ora quali relazioni devono intercorrere tra i parametri di tali circuiti affinché siano **equivalenti ai fini esterni**. Imponendo la validità di tali relazioni sarà quindi possibile trasformare una stella di resistori in un triangolo e viceversa.
Per questo, passiamo ai relativi doppi bipoli tripolari prendendo ad arbitrio un polo come <u>nodo comune alle due porte</u>, decidiamo di prendere il nodo $3$.

La figura successiva riporta il doppio bipolo derivato dalla stella, di cui sappiamo dalla $(6.17)$ che la matrice $\mathbf{R}$ è data da:

$$\mathbf{R}^{\star}=\begin{vmatrix}
R_{1}+R_{3} & R_{3} \\
R_{3} & R_{2}+R_{3}
\end{vmatrix}\quad \quad(6.41)$$

![[Elettrotecnica-1793980431583.webp|338]]
#Figura(6.29). *Doppio bipolo a stella*


La figura 6.30 riporta il doppio bipolo derivato dal triangolo, di cui sappiamo dalla $(6.20)$ che la matrice $\mathbf{G}$ è data da:

$$\mathbf{G}^{\nabla}=\begin{vmatrix}
\frac{1}{R_{13}}+\frac{1}{R_{12}} & -\frac{1}{R_{12}} \\
-\frac{1}{R_{12}} & \frac{1}{R_{23}}+\frac{1}{R_{12}}
\end{vmatrix}\quad \quad(6.42)$$
![[Elettrotecnica-1793980630644.webp|350]]
#Figura(6.30). *Doppio bipolo a triangolo*


I due doppi bipoli sono equivalenti tra loro se le stesse rappresentazione hanno gli stessi parametri. Per imporre ciò, procediamo per primo a invertire la matrice $\mathbf{R}$ della stella per calcolarne la rappresentazione G:
$$G^{\star}=\frac{1}{R_{1}R_{2}+R_{1}R_{3}+R_{3}R_{2}}\begin{vmatrix}
R_{2}+R_{3} & -R_{3} \\
-R_{3} & R_{1}+R_{3}
\end{vmatrix}\quad \quad(6.43)$$

L’equivalenza stella-triangolo si ha sse $\mathbf{G}{\star} = \mathbf{G}^{\nabla}$.
Imponendo l’uguaglianza dei parametri $g_{12}$, si ha:
$$R_{12}=\frac{R_{1}R_{2}+R_{1}R_{3}+R_{3}R_{2}}{R_{3}}=R_{1}+R_{2}+\frac{R_{1}R_{2}}{R_{3}}\quad(6.44)$$

Quindi, imponendo l’uguaglianza dei parametri $g_{11}$ e $g_{11}$ e tenendo conto della $(6.44)$, si ricava:

$$R_{13}=\frac{R_{1}R_{2}+R_{1}R_{3}+R_{3}R_{2}}{R_{2}}=R_{1}+R_{3}+\frac{R_{1}R_{3}}{R_{2}}\\ \\(6.45)\\ \\ \\ \\R_{23}=\frac{R_{1}R_{2}+R_{1}R_{3}+R_{3}R_{2}}{R_{1}}=R_{2}+R_{3}+\frac{R_{2}R_{3}}{R_{1}}\\ \\(6.46)$$

**Queste relazioni rappresentano le trasformazioni stella-triangolo**.


Per ricavare le trasformazioni inverse, procediamo invertendo la matrice $\mathbf{G}$ del triangolo in modo da ricavarne la $\mathbf{R}$. Nel far ciò, per comodità, utilizziamo la notazione dei parametri $G_{ik}=\frac{1}{R_{ik}}$. Si ha :

$$\mathbf{R}^{\nabla}=\frac{1}{G_{12}G_{23}+G_{13}G_{12}+G_{12}G_{23}}\begin{vmatrix}
G_{23}+G_{12} & G_{12} \\
G_{12} & G_{13}+G_{12}
\end{vmatrix}\quad \quad (6.47)$$

Quindi imponiamo l’uguaglianza delle matrici $\mathbf{R}{\nabla} = \mathbf{R}^{\star}$. Partiamo coi termini $r_{12}$:
$$R_{3}=\frac{G_{12}}{G_{12}G_{23}+G_{13}G_{12}+G_{12}+G_{23}}\quad(6.48)$$

e poi passiamo ai termini $r_{11}$ e $r_{22}$ tenendo conto dell'ultima equazione, si ha:

$$R_{1}=\frac{G_{23}}{G_{13}G_{23}+G_{13}G_{12}+G_{12}+G_{23}}\quad(6.49)\\ \\R_{2}=\frac{G_{13}}{G_{13}G_{23}+G_{13}G_{12}+G_{12}+G_{23}}\quad(6.50)$$

**Queste relazioni rappresentano le trasformazioni triangolo-stella**.

Esse possono essere ulteriormente ridotte in una forma più semplice da ricordare; per questo, torniamo ad esprimere le conduttanze del circuito a triangolo in termini di resistenze, risulta:
$$R_{3}=\frac{R_{23}R_{12}}{R_{12}+R_{23}+R_{13}}\quad(6.51)\\ \\R_{1}=\frac{R_{13}R_{12}}{R_{12}+R_{23}+R_{13}}\quad(6.52)\\ \\R_{2}=\frac{R_{21}R_{23}}{R_{12}+R_{23}+R_{13}}\quad(6.53)$$


Riassumendo la procedura per la trasformazione stella-triangolo è illustrata in figura 6.31, dove per sottolineare il metodo indipendentemente dai simboli si sono rinominate le resistenze:
![[Elettrotecnica-1794084845063.webp|687]]
#Figura(6.31). *Trasformazione stella-triangolo*


La procedura per la trasformazione triangolo-stella è invece illustrata in figura:

![[Elettrotecnica-1794084883557.webp|677]]
#Figura(6.32). *Trasformazione triangolo-stella*



## 6.6 **Amplificatore operazionale**

In questa sezione descriviamo un componente elettronico estremamente diffuso nelle applicazioni e che, come vedremo, viene modellato come un due porta. Il comportamento elettrico presenta delle peculiarità che richiedono uno studio ad "hoc". Vedremo anche come tali peculiarità possono essere incorporate in un modello di comportamento ideale, cioè la cui complessità è ridotta all’essenziale.

Il dispositivo fisico amplificatore operazionale (op-amp *dall’inglese "operational amplifier"*) si presenta come un componente elettronico con molti morsetti esterni.
La figura mostra il caso di un op-amp con 5 morsetti, due di questi servono per alimentare il componente mentre i tre rimanenti sono quelli che elaborano le variabili elettriche in ingresso per produrre quella di uscita.
![[Elettrotecnica-1794136557568.webp|387]]

#Figura(6.33). *Dispositivo amplificatore operazionale*

La figura 6.34 mostra come il componente viene connesso a due batterie rappresentate da due generatori ideali di tensione collegate ad un filo di riferimento. Queste sorgenti "accendono" il dispositivo.
![[Elettrotecnica-1794136589499.webp|399]]
#Figura(6.34). *Collegamento dell’op-amp alle alimentazioni*


In questo modo si viene a formare un doppio bipolo in cui la porta uno è costituita dai due morsetti di ingresso $+$ e $−$ mentre la porta due è formata dal morsetto di uscita e dal riferimento. Il legame tra la tensione di ingresso $V_{i}$ e quella di uscita $V_{o}$ è descritto dalla curva caratteristica mostrata in figura:

![[Elettrotecnica-1794136761266.webp|364]]
#Figura(6.35). *Legame ingresso uscita*

Nella parte centrale della curva, in un intervallo centrato nell’origine degli assi, il legame è lineare di proporzionalità diretta:
$$V_{o}=A\cdot V_{i}$$
attraverso il parametro $A$ detto <u>amplificazione</u>.

Al di fuori di tale intervallo la curva spiana, ovvero la tensione di uscita raggiunge o un valore massimo (legato al valore dell’alimentazione positiva) o un valore minimo (dovuto all’alimentazione negativa) detti <u>valori di saturazione</u>.

Nell’ipotesi che funzioni nella zona lineare della sua caratteristica (ipotesi imposta nella maggior parte delle applicazioni), l’op-amp viene rappresentato come mostrato in figura (Sinistra), cioè omettendo le alimentazioni, e modellato ai fini esterni come il doppio bipolo in figura (Destra):
![[Elettrotecnica-1794137722137.webp|566]]
#Figura(6.36). *Modello realistico*

Questo modello, che definiremo "realistico in continua", comprende una resistenza di ingresso $R_{i}$ alla porta uno ed un generatore di tensione pilotato in tensione alla porta due.
Il modello potrebbe essere complicato ulteriormente introducendo altri effetti di second’ordine, per esempio una (piccola) resistenza di uscita $R_{o}$ in serie all’uscita. Tuttavia questo complicherebbe inutilmente la trattazione senza modificare le conclusioni.

Accanto al modello realistico, esiste un modello ideale ulteriormente semplificato che viene ampiamente utilizzato nelle fasi preliminari di progetto elettronico e che è indispensabile padroneggiare: il modello ideale si applica quando l’op-amp è inserito in una rete elettrica come mostrato in figura (Sinistra), dove la porta di ingresso e quella di uscita sono collegate a due bipoli esterni, inoltre **il morsetto d’uscita è collegato ad uno di quelli in ingresso attraverso un bipolo detto di retroazione**.
![[Elettrotecnica-1794137824132.webp|500]]
#Figura(6.37). *Op-amp inserito in una rete con retroazione e suo modello ideale di tipo doppio bipolo*

In queste condizioni, come verificheremo nell’analisi successiva, la tensione $V_{o}$ si mantiene di valore limitato (all’interno dell’intervallo di linearità) anche per valori infinitamente grandi dell’amplificazione $A$. Poiché vale:
$$V_{I}=\frac{V_{o}}{A}\quad\quad I_{i}=\frac{V_{i}}{R_{i}}$$
si ha che per $A\rightarrow \infty$:

$$V_{i}=0\\I_{i}=0\\ \\(6.54)$$

Quindi, l’op-amp inserito in una rete di retroazione e con amplificazione infinita si comporta come un doppio bipolo con tensione e corrente nulle alla porta di ingresso come mostrato in 6.37 (Destra).

Le equazioni $(6.54)$ rappresentano il legame costitutivo del modello di op-amp ideale.
Si noti come tali equazioni non forniscono alcuna informazione circa i valori della tensione $V_{o}$ e corrente Io alla porta di uscita. In pratica, il modello ideale di op-amp viene impiegato per semplificare l’analisi ed il progetto dei circuiti che lo contengono per valori sufficientemente grandi dell’amplificazione (*as esempio* $A > 100$).



#### #Esercizio(amplificatore operazionale) (1)

> [!question] Esercizio
> Approfondiamo ora la comprensione del significato di modello ideale svolgendo l’analisi del circuito esempio mostrato in figura:
> ![[Elettrotecnica-1794138116313.webp|312x192]]
> #Figura(6.38). *Circuito esempio con op-amp*
> 
> L’op-amp è collegato in ingresso ad una sorgente ideale di corrente ed a un resistore di uscita, inoltre una resistenza di retroazione $R_{f}$ (detta di "feedback") collega l’uscita con il nodo−in ingresso: in questo caso si parla di retroazione negativa ed è la configurazione che rende stabile il circuito.
> 
> Procederemo in due modi distinti:
> 
> 1) risolviamo il circuito utilizzando il modello realistico e quindi vediamo come si trasforma la soluzione quando $A\rightarrow \infty$;
> 2) risolviamo il circuito con il modello di op-amp ideale.
> 
> Vedremo che **le due strade portano allo stesso risultato finale**.
> 
> 
> - Sostituiamo il modello realistico nel circuito ottenendo lo schema mostrato in figura:
> 	![[Elettrotecnica-1794138293897.webp|291]]
> 	#Figura(6.39). *Soluzione con modello realistico*
> 	
> 	Assumiamo come incognita la tensione $Vi_{i}$ (fate attenzione al verso). Applicando la KVL alla maglia centrale, si ricava:$$V_{i}=\frac{-I_{s}}{\frac{1}{R_{i}}}+\frac{(1+A)}{R_{f}}\quad(6.55)$$e quindi quello di $V_{o}$:$$V_{o}=I_{s}\cdot\frac{-A}{\frac{1}{R_{i}}+\frac{(1+A)}{R_{f}}}\quad(6.56)$$Che cosa accade quando $A\rightarrow \infty$?
> 	In questa condizione limite, dalla $(6.55)$ si trova:$$V_{i}=0$$che conferma il modello di comportamento dato dalle $(6.54)$. Mentre dalla $(6.56)$, svolgendo il limite (<u>regola di De l’Hopital</u>), si ha:$$V_{o}=-I_{s}\cdot R_{f}\quad(6.57)$$che dà la soluzione della tensione in uscita e conferma che questo valore è finito anche per valori infinitamente grandi di $A$.
> 
> 
> - Nel secondo approccio, usiamo direttamente il modello ideale di op-amp all’interno del circuito come mostrato in figura:
> 	![[Elettrotecnica-1794138628716.webp|269]]
> 	#Figura(6.40). *Soluzione con modello ideale*
> 	
> 	In questo caso si ha che la corrente che scorre nel resistore $R_{f}$ è la stessa $I_{s}$ impressa dal generatore. Dunque:$$V_{f}=I_{s}\cdot R_{f}$$Inoltre applicando la KVL alla maglia che include $R_{o}$ passa da $R_{f}$ e quindi si chiude passando per i morsetti di ingresso dell’op-amp, abbiamo:$$V_{o}+V_{f}+0=0$$che dà:$$V_{o}=-V_{f}=-I_{s}\cdot R_{f}$$e coincide con la $(6.57)$.
> 
> 
> Concludiamo che:
> 
> 1) Il modello ideale fornisce esattamente lo stesso risultato del modello realistico se $A\to \infty$;
> 2) Tale risultato non dipende dal valore $A$ ma solo dal generatore e dal resistore di retroazione;
> 3) Nella pratica, per valori tipici di $A$ (*ad esempio* $≥102$), il risultato fornito dal modello ideale si differenzia da quello fornito dal modello realistico per meno di $\frac{1}{100}$. Questa precisione è più che sufficiente per l’analisi "a mano" e il predimensionamento elettronico.



## 6.7 **Stadi di amplificazione con op-amp**

Analizziamo il comportamento elettrico del circuito mostrato in figura utilizzando il modello ideale di op-amp. Notate come la tensione di uscita $V_{o}$ venga riportata all’ingresso, attraverso la resistenza di retroazione $R_{2}$.
![[Elettrotecnica-1794138963701.webp|403]]
#Figura(6.41). *Circuito invertente*

Il procedimento generale in questa tipologia di analisi è quello di <mark class="hltr-yellow">partire dall’ingresso dell’op-amp dove abbiamo tutta l’informazione e procedere risolvendo verso l’uscita</mark>. Dalla maglia di ingresso vediamo che:
$$i_{1}=\frac{E}{R_{1}}$$
mentre dal nodo di ingresso si ha:
$$i_{2}=i_{1}$$
La tensione sul resistore di retroazione risulta:
$$v_{1}=\frac{E}{R_{1}}\cdot R_{2}$$

Infine applicando la KVL alla maglia che passa per il resistore di uscita (o di carico) $R_{3}$ la resistenza $R_{2}$ e i morsetti di ingresso dell’op-amp si trova:
$$V_{o}=-v_{2}=E\cdot\frac{-R_{2}}{R_{1}}$$

Si noti come la $V_{o}$ **non dipenda dal resistore** $R_{3}$ collegato all’uscita.
Questo circuito dunque amplifica la tensione $E$ della sorgente in ingresso di un fattore che dipende dal rapporto $\frac{R_{2}}{R_{1}}$ e ne cambia il segno; per questo viene comunemente indicato come **stadio di amplificazione invertente**.

Completiamo l’analisi valutando la potenza elettrica assorbita dall’op-amp. Ricordiamo che <u>in un doppio bipolo la potenza elettrica assorbita è data dalla somma delle potenze assorbite dalle due porte che lo compongono</u>. In questo caso avremo:
$$p_{op \ - \ amp}=V_{i}\cdot I_{i}+V_{o}\cdot I_{o}=V_{o}\cdot I_{o}$$

ovvero la potenza assorbita dal doppio bipolo coincide con quella assorbita alla porta di uscita. Calcoliamo $I_{o}$:
$$I_{o}=i_{2}-i_{3}=\frac{E}{R_{1}}-\frac{V_{o}}{R_{3}}=\frac{E}{R_{1}}+E\cdot \frac{R_{2}}{R_{1}\cdot R_{3}}$$

Quindi la potenza assorbita vale:
$$p_{op \ - \ amp}=\left( -E\cdot \frac{E_{2}}{R_{1}} \right)\cdot\left[ \frac{E}{R_{1}}\left( 1+\frac{R_{2}}{R_{3}} \right) \right]$$

Per valori positivi di $E$ e resistori fisici ($R > 0$) la corrente $I_{o}$ è positiva mentre la tensione $V_{o}$ è negativa, dunque la potenza assorbita è negativa. **Il dispositivo op-amp eroga potenza elettrica**.
Potremmo chiederci: da dove viene tale potenza ? La risposta è semplice: dalle sorgenti di tensione interne che servono per alimentarlo. Si noti inoltre come la resistenza collegata $R_{3}$, che non ha effetto sulla $V_{o}$ ne ha su $Io_{o}$ e quindi sulla potenza erogata. Tale potenza aumenta al diminuire del valore di $R_{3}$.



#### #Esercizio(amplificatore operazionale) (2)

> [!question] Esercizio
> Nel secondo esercizio analizziamo il comportamento del circuito mostrato in figura:
> ![[Elettrotecnica-1794145857052.webp|337]]
> #Figura(6.42). *Stadio non invertente*
> 
> In questo caso per semplicità l’uscita non è stata connessa ad alcun carico. Dalla maglia di ingresso, utilizzando il modello ideale di op-amp, notiamo che:
> $$v_{1}=E$$
> cioè la tensione della sorgente cade tutta sul resistore $R_{1}$ la cui corrente è:
> $$i_{1}=\frac{E}{R_{1}}$$
> Tale corrente scorre anche nel resistore $R_{2}$ producendo una tensione:
> $$v_{2}=i_{2}\cdot R_{2}=\frac{E}{R_{1}}\cdot R_{2}$$
> Infine, dalla KVL alla maglia di uscita troviamo che:
> $$V_{o}=v_{1}+v_{2}=E\cdot\left( 1+\frac{R_{2}}{R_{1}} \right)$$
> 
> Questo circuito produce un’amplificazione della tensione di ingresso del fattore $1 + \frac{R2}{R_{1}}$ mantenendone il segno. Per questo viene comunemente indicato col nome di **stadio di amplificazione non invertente**.
> 
> Si noti che **la trattazione svolta NON muta se si tiene conto di un resistore collegato all’uscita**. Tuttavia il resistore di carico modificherà la corrente $I_{o}$.


#### #Esercizio(amplificatore operazionale) (3)

> [!question] Esercizio
> Infine, come ulteriore esempio vediamo cosa accade quando nel circuito in [[#Esercizio(amplificatore operazionale) (2)|figura 6.42]] la resistenza $R_{1} \to \infty$, cioè diventa un <u>circuito aperto</u>.
> Questo caso è mostrato in figura (Sinistra):
> ![[Elettrotecnica-1794146247195.webp|631]]
> #Figura(6.43). *Due modi di disegnare un inseguitore di tensione*
> 
> Dal circuito di sinistra, vediamo come la tensione al nodo $A$ rispetto al filo di riferimento è uguale a $E$ e quindi $V_{o} = E$ indipendentemente dal carico applicato.
> Per questo motivo questo circuito viene comunemente indicato col nome di **inseguitore di tensione**.
> 
> Nella figura 6.43 (Destra) l’inseguitore è ridisegnato come si usa fare negli schemi elettronici, si noti che la resistenza $R_{2}$ è stata sostituita da un filo (*per esempio* un corto circuito).
> Questa sostituzione è ininfluente dato che $R_{2}$ è attraversato da corrente nulla: è lecito chiedersi: ma a che serve un dispositivo che riporta una tensione tale e quale a se stessa ?
> 
> La risposta è che questo circuito "disaccoppia" ciò che è collegato in ingresso al nodo $+$ dal carico in uscita, ovvero l’ingresso e il carico non sono collegati elettricamente e non si influenzano tra di loro, possono dunque essere progettati separatamente in modo modulare.



## 6.8 **Trasformatore ideale**

Introduciamo il modello ideale di un altro dispositivo estremamente diffuso nelle applicazioni elettriche ed elettroniche: il **trasformatore**.

Sottolineiamo come il trasformatore fisico funziona in presenza di grandezze elettriche variabili nel tempo, come vedremo, nelle note successive; tuttavia il suo modello ideale può essere presentato nel contesto dei doppi bipoli.
Il simbolo adottato in Teoria dei circuiti è mostrato in figura, dove il parametro $k$ è indicato come <u>rapporto di trasformazione</u>:
![[Elettrotecnica-1794146635548.webp|324]]
#Figura(6.44). *Il doppio bipolo trasformatore ideale*


 Il legame costitutivo è dato da:
$$V_{1}=k\cdot V_{2}\\ \\I_{1}=-\frac{1}{k}\cdot I_{2}\\ \\(6.58)$$
e corrisponde alla matrice dei parametri di trasmissione $T$ data da:
$$\mathbf{T}=\begin{vmatrix}
k & 0 \\
0 & \frac{1}{k}
\end{vmatrix}\quad\quad(6.59)$$

Il comportamento è il seguente: la tensione $V_{1}$ é pari a $V_{2}$ amplificata del fattore $k$, mentre la corrente $I_{1}$ è data da $I_{2}$ (**cambiata di segno**) ridotta dello stesso fattore.

Se si calcola la potenza elettrica assorbita dal doppio bipolo sostituendo il legame costitutivo si ha:
$$p_{trans}=V_{1}\cdot I_{1}+V_{2}\cdot I_{2}=(K\cdot V_{2})\cdot\left( -\frac{1}{k}\cdot I_{2} \right)+V_{2}\cdot I_{2}=0$$
Ovvero <u>questo particolare bipolo assorbe una potenza elettrica totale nulla</u>. In altri termini osservando che:
$$V_{1}\cdot I_{1}=V_{2}\cdot(-I_{2})$$
si può affermare che la potenza elettrica assorbita (o entrante alla porta $1$) è uguale alle potenza erogata (o uscente) dalla porta $2$, come mostrato in figura:
![[Elettrotecnica-1794146920785.webp|413]]
#Figura(6.45). *Il trasformatore ideale eroga in uscita tutta e sola la potenza che assorbe in ingresso*


Questa figura mostra l’essenza del dispositivo trasformatore incorporata nel suo modello ideale: il trasformatore ideale riduce di un fattore $k$ la tensione $V_{1}$ in ingresso e contemporaneamente incrementa dello stesso fattore la corrente $I_{1}$ senza alterare la potenza in gioco. Per questo viene utilizzato in un vasto numero di applicazioni in cui si deve passare da una rete che lavora con valori elevati di tensione ad una che richiede tensioni molto più ridotte (*ad esempio* dalla rete di distribuzione ad un calcolatore).

Vediamo un’altra proprietà del trasformatore con l’aiuto in figura dove un bipolo equivalente di tipo serie è collegato alla porta $2$:
![[Elettrotecnica-1794147015462.webp|437]]
#Figura(6.46). *Il trasformatore ideale può venire impiegato per modificare i parametri di un bipolo*

Si vuole determinare il modello equivalente, cioè il legame $I, V$, visto alla porta $1$. Si ha:
$$-I_{2}=k\cdot I$$
e dunque dalla maglia alla porta $2$ si ricava:
$$V_{2}=-I_{2}\cdot R+E=K\cdot I\cdot R+E$$

Infine la tensione $V$ risulta:
$$V=k\cdot V_{2}=I\cdot(k^2 R)+k\cdot E$$

Il circuito equivalente alla porta $1$ è dato da una resistenza equivalente $k^2 \ R$ in serie ad un generatore di tensione equivalente di valore $k \ E$.




# **Capitolo VII: Regime sinusoidale e fasori**


## 7.1 **Grandezze sinusoidali**

In questa sezione impariamo a descrivere grandezze elettriche che sono funzioni sinusoidali del tempo. Indichiamo con $x(t)$ la generica tensione o corrente sinusoidale in un circuito elettrico, questa avrà un’espressione del tipo:

$$x(t)=X_{m}\cos(\omega t+\phi)\quad\quad(7.1)$$

dove il parametro $X_{m}$ viene detto **ampiezza** o valore di picco, $\omega$ è la **pulsazione** e $\phi$ la **fase** o angolo. Per comprendere il significato di tali parametri, partiamo considerando il caso semplificato in cui $\phi=0$ e dunque la grandezza si riduce a $x(t) = X_{m} \cos(\omega t)$ come mostrato in figura:
![[Elettrotecnica-1794148040908.webp|442]]
#Figura(7.1). *Funzione $X_{m} \cos(\omega t)$*

Il parametro $X_{m}$ semplicemente scala la funzione coseno (il cui massimo sappiamo valere uno) e la sua unità di misura è la stessa della grandezza $x(t)$ (*ad esempio* sarà in volt se la grandezza è una tensione o ampere se la grandezza è una corrente).
Poiché $\cos(· )$ è periodico di periodo $2\pi$, abbiamo che anche $x(t)$ è periodico ed il suo periodo $T$ è quel valore del tempo $t= T$ per cui l’argomento del coseno vale $2\pi$, ovvero:
$$\omega T=2\pi$$
da cui otteniamo:
$$T=\frac{2\pi}{\omega}\quad Periodo \ [s] \\ \\\omega = \frac{2\pi}{T}\quad  Pulsazione \ \left[ \frac{rad}{s} \right] \\ \\ f=\frac{1}{T}=\frac{\omega}{2\pi}\quad Frequenza \ [s^{-1}=Hz]$$

l'unità di misura della **frequenza** è l'Hertz [Hz].
Una grandezza periodica, che talvolta indicheremo anche come <u>segnale periodico</u> o forma d’onda periodica, con periodo $T$ ripete i suoi valori ogni $T$ secondi.

La frequenza è l’inverso del periodo, cioè ci dice quante volte si ripete un dato valore in un periodo. Consideriamo quale esempio il segnale di clock in un calcolatore che ha frequenza tipica di circa $3 \ GHz= 3 \cdot 10^{9} \ Hz$: questo significa che in un secondo esso si ripete 3 miliardi di volte, mentre il suo periodo è di circa $333$ pico $10^{-12}$ secondi.
Nella trasmissione 5G, attualmente si utilizzano dei segnali sinusoidali (portante) con frequenza fino a $90 \ GHz$, ovvero con periodo di circa $11$ pico secondi.

Veniamo ora al significato del parametro fase. Per questo <u>premettiamo il concetto di anticipo o ritardo di una funzione (o segnale) del tempo</u>. Sia $g(t)$ una funzione del tempo con andamento mostrato in figura (Alto) che raggiunge il suo massimo in $t_{0}$:
![[Elettrotecnica-1794160981768.webp|301]]
#Figura(7.2). *Shift temporale della funzione $g(t)$*


Dato un numero reale positivo $a$, consideriamo la funzione:
$$g(t+a)$$
il cui grafico è mostrato in figura (Medio). L’effetto del parametro $a$ è quello di **anticipare temporalmente** la forma d’onda rispetto a $g(t)$.
Infatti il massimo di $g(t + a)$ viene raggiunto quando l’argomento di $g(· )$ vale $t_{0}$, cioè in:
$$t+a=t_{0}\longrightarrow t=t_{0}-a$$
Viceversa la funzione del tempo:
$$g(t-a)$$
mostrata in figura (Basso) sarà **ritardata temporalmente** di $a$ rispetto a $g(t)$ e quindi raggiunge il suo massimo in $t_{0} + a$.
In sostanza l’effetto di un parametro sommato $a$ nell’argomento di una <mark class="hltr-yellow">funzione ha l’effetto di traslare nel tempo ("shifting") la forma d’onda</mark>.

Alla luce di ciò, riscriviamo la sinusoide $(7.1)$ nel modo seguente:

$$x(t)=X_{m}\cos\left[ \omega\left( t+\frac{\phi}{\omega} \right) \right]\quad \quad (7.2)$$

dove è evidente che $\frac{\phi}{\omega}$ gioca il ruolo del parametro $a$ visto prima, cioè rappresenta l’intervallo di tempo di cui viene anticipato il coseno come mostrato in figura:
![[Elettrotecnica-1794161324785.webp|445]]
#Figura(7.3). *Effetto del parametro fase*


Per esempio, si consideri quando tale intervallo vale un quarto di periodo, come mostrato in figura (Alto), da cui si ottiene la funzione $−X_{m} \sin(\omega \ t)$:
![[Elettrotecnica-1794161901648.webp|383]]
#Figura(7.4). *Sfasamento di $\frac{\pi}{2}$ (<u>Alto</u>) e di $-\frac{\pi}{2}$ (<u>Basso</u>)*

Ricordando che $\omega = \frac{2\pi}{T}$ si ha che la fase corrispondente vale:
$$\frac{\phi}{\omega}=\frac{T}{4}\longrightarrow \phi=\frac{\pi}{2}$$
ovvero:
$$\cos\left( \omega \ t+\frac{\pi}{2} \right)=-\sin(\omega \ t)$$

Se viceversa l’intervallo $\frac{\phi}{\omega}$ vale $\frac{−T}{4}$, come mostrato in figura 7.4 (Basso), si ottiene la funzione $X_{m} \sin(\omega \ t)$. In questo caso a fase corrispondente vale:
$$\frac{\phi}{\omega}=-\frac{T}{4}\longrightarrow \phi=-\frac{\pi}{2}$$
ovvero:
$$\cos\left( \omega \ t-\frac{\pi}{2} \right)=\sin(\omega \ t)$$

Da quest’ultima osserviamo come **la funzione seno può venire scritta come la corrispondente funzione coseno ritardata di $\frac{\pi}{2}$**.



## 7.2 **Richiami di trigonometria**

Riportiamo di seguito alcune relazioni trigonometriche, probabilmente già note, utili per la prosecuzione. Dati due angoli $\alpha$ e $\beta$ valgono le seguenti identità trigonometriche:
$$\cos^2\alpha+\sin^2\alpha=1\quad\quad(7.3)\\ \\ \cos(\alpha-\beta)=\cos \alpha\cdot \cos \beta+\sin \alpha\cdot \sin \beta\quad \quad(7.4)\\ \\cos(\alpha+\beta)=\cos \alpha\cdot \cos \beta-\sin \alpha\cdot \sin \beta\quad\quad(7.5)$$

Sommando la $(7.4)$ alla $(7.5)$ si ricava facilmente la **formula di prostaferesi** che permette di esprime il prodotto di sinusoide attraverso una somma:

$$\cos \alpha\cdot \cos \beta=\frac{1}{2}\cos(\alpha+\beta)+\frac{1}{2}\cos(\alpha-\beta)\quad\quad(7.6)$$

Infine riportiamo la relazione tra due modi di rappresentazione della funzione sinusoidale. Partendo dall’espressione $(7.1)$ applichiamo la $(7.5)$:

$$\begin{align}
x(t) &= X_{m}\cos(\omega \ t + \phi) \\ \\
&= (X_{m}\cos \phi)\cos(\omega t)+(-X_{m}\sin \phi)\sin(\omega \ t)
\end{align} \\ \\(7.7)$$
che può essere riscritta:
$$x(t)=A \cos(\omega \ t)+ B \sin(\omega \ t)\quad (7.8)$$
con la posizione:
$$A=X_{m}\cos \phi\\ \\B=-X_{m}\sin \phi\\ \\(7.9)$$

Tali relazioni ci permettono di passare dalla rappresentazione $(7.1)$ in termini di ampiezza e fase alla $(7.8)$ dove compare la somma di un coseno ed un seno.

Invertendo le $(7.9)$, troviamo:
$$X_{m}=\sqrt{A^2+B^2}\\ \\ \phi=-atan\left( \frac{B}{A} \right)\\ \\(7.10)$$

dove $atan(· )$ indica la funzione arcotangente.
Quest’ultime ci permettono il passaggio inverso dalla rappresentazione $(7.8)$ in termini di somma di un coseno ed un seno alla $(7.1)$ dove compaiono ampiezza e fase.



## 7.3 **Sorgenti sinusidali e bipoli dinamici**

Iniziamo col valutare cosa accade quando una sorgente sinusoidale:
$$v_{s}(t)=E\cos(\omega t)$$
viene inserita all’interno di un circuito resistivo, ovvero formato da resistenze, generatori pilotati e/o più in generale da doppi bipoli.
Ci riferiamo ai circuiti elementari mostrati in figura:
![[Elettrotecnica-1794210422680.webp|456]]
#Figura(7.5). *Reti resistive con generatore sinusoidale*

Sul singolo resistore $R$ continua a valere la legge di Ohm tra i valori istantanei delle correnti e tensioni ai suoi capi, cioè:
$$v(t)=R \ i(t)$$

Quindi per il circuito in figura (Sinistra) si ha:
$$i(t)=\frac{1}{R}v_{s}(t)=\frac{1}{R}E\cos(\omega t)$$
