

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
#Figura(1.4): La tensione elettrica lungo la linea $\gamma$ è indicata come $V(\gamma)$.

Per definire la seconda grandezza elettrica, si supponga di voler

misurare il flusso di carica all’interno del filo metallico. A tale propos-

ito si taglia il filo venendo a formare la superficie sezione σ.

Figure 1.9: Il filo viene sezionato iden-

tificando così la sezione σ di cui si deve

scegliere un verso di attraversamento.Si fissa arbitrariamente un verso di attraversamento come posi-

tivo che induce un orientiamo della superficie σ e si conta la quantità

netta di carica positiva che attraversa la superficie. La corrente elet-

trica in un mezzo conduttivo (cioè che ne consente la circolazione)

è una grandezza descrittiva associata ad una superficie σ orientata,

che indichiamo come I(σ), definita come la quantità di carica elettrica

netta che attraversa la sezione nell’unità di tempo. L’aggettivo netta

si riferisce al fatto che in un dato istante di osservazione la superficie

in esame potrebbe essere attraversata da una carica Q1 che si muove

concorde col verso di orinetazione assunto ed una carica Q2 che in-

vece si muove in senso opposto. La carica netta in questo caso è data

da Q1−Q2. L’unità di misura della corrente è chiamata ampere [A],

in onore del fisico francese che la studiò. Anche il valore della corrente

è dotato di segno, ad indicare se il flusso netto di carica è concorde o

discorde rispetto al senso di attraversamento fissato sulla superficie.