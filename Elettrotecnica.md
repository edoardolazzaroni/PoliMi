
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

• **Proprietà della tensione**.
Indichiamo con $\gamma$ una linea orientata diretta dal punto $A$ al punto $B$ e con $−\gamma$ la stessa linea ma orientata nel verso opposto, cioè che va da $B$ ad $A$, come mostrato in figura.
Operativamente la misura di tensione lungo $−\gamma$ si ottiene invertendo l’inserimento dei morsetti del voltmetro. Vale la proprietà di disparità, ovvero:
$$V(−\gamma) =−V(\gamma)$$
La disparità ha l’ovvio significato che il lavoro svolto per spostare

la carica di prova da A a B è lo stesso in modulo ma opposto in

segno a quello che si svolge per spostarla da B ad A.

Ora consideriamo le linee orientate γ1 che va da A a B e γ2 che

va da B a C (crf. figura 1.13). La loro unione dà origine alla linea

complessiva γ= γ1 ∪γ2 che va da A a C. Sia v1 = V(γ1) la ten-

sione misurata lungo γ1 e v2 = V(γ2) la tensione misurata lungo

γ2. Indichiamo poi con V(γ) la misura lungo la linea complessiva.

Vale allora la proprietà additiva della tensione:

V(γ) = V(γ1 ∪γ2) = V(γ1) + V(γ2) = v1 + v2.

Combiniamo ora le due proprietà e consideriamo le tre linee

γ1, γ2 e γ3 orientate come mostrato in figura 1.14 (cioè con γ2

orientata in modo discorde alle altre) e la linea unione γ= γ1 ∪

(−γ2) ∪γ3. Abbiamo eseguito le relative misure di tensione v1 =

V(γ1), v2 = V(γ2) e v3 = V(γ3). Dalla proprietà di disparità si ha

Figure 1.12: Inversione

dell’orientamento di una linea.

Figure 1.13: γ= γ1 ∪γ2.che V(−γ2) =−v2 e dunque applicando la proprietà di additività

concludiamo che

v(γ) = V(γ1 ∪(−γ2) ∪γ3) = v1−v2 + v3.

La misura di tensione lungo un cammino orientato è dato dalla somma

algebrica (cioè con segno) delle misure eseguite lungo i tratti parziali,

prendendo con segno positivo le misure eseguite con orientamento con-

corde al cammino e con segno negativo le discordi.

• Proprietà della variabile corrente.

Sia σ una superficie orientata come in figura 1.11 e con−σ la

stessa superficie ma orientata nel verso opposto (cfr. figura 1.15).

Operativamente, la misura di corrente lungo−σ si ottiene in-

vertendo l’inserimento dei morsetti dell’amperometro. Vale la

proprietà di disparità:

I(−σ) =−I(σ).

Ora consideriamo le superfici σ1 e σ2, orientate in modo concorde

e che condividono parte della loro frontiera. La loro unione dà

origine alla superficie complessiva σ = σ1 ∪σ2. Se i1 = I(σ1)

e i2 = I(σ2) sono i valori delle misure delle correnti attraverso

le superfici parziali mentre i= I(σ) è la misura attraverso la

superficie complessiva, la proprietà additiva delle correnti dice

che:

i= I(σ) = I(σ1 ∪σ2) = I(σ1) + I(σ2) = i1 + i2.

Infine siano σ1, σ2 e σ3 tre superfici orientate come in figura e

cioè con σ2 orientata in modo discorde alle prime due e sia σ =

σ1 ∪(−σ2) ∪σ3. Si sono eseguite le relative misure di corrente

i1, i2 e i3. Dalla proprietà di disparità si ha che i(−σ2) =−i2 e

dall’additività che:

i= I(σ1 ∪(−σ2) ∪σ3) = i1−i2 + i3.

capitolo 1 11

Figure 1.14: γ= γ1 ∪(−γ2) ∪γ3.

Figure 1.15: La superficie−σ è orientata

nel verso opposto rispetto alla σ in

figura 1.11. Notate che l’orientamento

della superficie è determinato dalla

modalità di inserimento dei terminali

dell’amperometro.12 nota1:il modello circuitale

Figure 1.16: σ = σ1 ∪σ2).

Figure 1.17: σ = σ1 ∪(−σ2) ∪σ3.

La misura di corrente attraverso una superficie orientata è dato dalla

somma algebrica (cioè con segno) delle misure eseguite attraverso le sotto-

superfici parziali che la formano prendendo con segno positivo le misure

eseguite con orientamento concorde e con segno negativo le discordi.