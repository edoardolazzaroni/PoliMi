

# **Capitolo I: Il modello circuitale**


## 1.1 **Sistemi elettrici e loro modelli**

In questo corso, acquisiremo la capacità di eseguire l’analisi dei sistemi elettrici. Dalla descrizione di un dato sistema in termini di elementi che lo compongono e di come sono connessi tra di loro, impareremo una metodologia generale per calcolare il valore delle grandezze elettriche che lo descrivono e con esse a capire come funziona e a che cosa serve. L’obiettivo verrà raggiunto diventando padroni di un modello matematico fondamentale dell’Ingegneria chiamato il **modello circuitale**.

Va precisato che il termine di sistema elettrico può riferirsi a realtà fisiche molto diverse tra loro e tutte fondamentali per la preparazione dell’Ingegnere dell’area ICT (Information and Communication Technology). Facciamo degli esempi.

Un primo tipo di sistema elettrico è rappresentato dalla rete di

trasporto/distribuzione dell’energia elettrica. Questa è formata da

un insieme di fili di rame, chiamati conduttori, che collegano punti

in cui l’energia viene prodotta, es. le centrali elettriche, impianti

fotovoltaici, ai punti in cui viene utilizzata, es. le nostre abitazioni,

gli impianti industriali, le linee di trasporto metropolitano o dei treni.

Tali reti hanno dimensioni dell’ordine delle centinaia di chilometri

dato che si possono estendere su tutto il territorio di una nazione. La

figura 1.1 mostra un esempio stilizzato di rete per l’energia.

Un secondo esempio, altrettanto rilevante, è rappresentato dai sis-

temi della micro e nano elettronica. Per es., la figura 1.2 riporta una

tipica scheda elettronica (detta anche "board"), che possiamo trovare

all’interno di un computer o di un controllore di un’automobile, dove

un certo numero di componenti sono collegati tra loro da micro-piste

di rame.

Questo secondo esempio di rete non ha lo scopo di trasportare en-

ergia bensì di elaborare l’informazione. L’energia elettrica nel primo

esempio e l’informazione nel secondo sono rappresentate (o deter-

Figure 1.1: Esempio stilizzato di rete

di distribuzione dell’energia: da una

centrale di produzione tradizionale

e da un campo eolico (energia rin-

novabile) partono dei fili di rame che

trasportano l’energia sotto forma di

variabili elettriche alle abitazioni dove

viene utilizzata.

Figure 1.2: Una scheda elettronica.

Figure 1.3: Collegamenti con piste di

rame sul retro della scheda6 nota1:il modello circuitale

minate) da alcune grandezze fisiche misurabili chiamate grandezze

descrittive. Alcuni dei componenti che si vedono sulla scheda in fig.

1.2 sono a loro volta dei sistemi elettrici formati al loro interno da

una rete complessa di collegamenti. La fig. 1.4 mostra uno di questi

componenti chiamato microprocessore, mostrato chinato coi contatti

esterni rivolti verso l’alto, e che funziona da cpu (central processing

unit) di un computer.

Oltre che nei computer e lap-top troviamo i microprocessori negli

smart-phones, nei controlli dei robots, autovetture, aeroplani, nei

sistemi di comunicazione via satellite, ecc.. Un micro-processore ha

le dimensioni dell’ordine del centimetro quadrato e può contenere

miliardi di micro/nano componenti, detti dispositivi, collegati tra

loro da micro-conduttori di rame.

Nonostante la spaventosa differenza di scala geometrica tra una

rete per l’energia e un processore elettronico il comportamento elet-

trico di questi sistemi può venire descritto dallo stesso modello cir-

cuitale. La tecnica di modeling, cioè la costruzione del modello, si

basa sull’identificazione delle grandezze fisiche descrittive che chi-

ameremo tensione e corrente elettrica e sulla scrittura delle leggi

che le governano. Nel modello, le grandezze fisiche sono sostitu-

ite da variabili matematiche (indicate v, i) mentre le leggi fisiche

si traducono in equazioni che legano tali variabili, come mostrato

schematicamente in figura 1.5.

Il modello circuitale consente di esplorare fenomeni elettrici e non

che vanno oltre gli esempi, seppur rilevanti, precedentemente ac-

cennati e che sconfinano nella ricerca più visionaria. Basti pensare,

spostandosi nel campo della biologia e bioingegneria, che gli im-

pulsi nervosi con cui il nostro cervello funziona sono degli impulsi

elettrici che si muovono in un circuito biologico. Questo consente di

interfacciare sistemi elettrici costruiti dall’uomo, quali ad es. un arto

artificiale, con il nostro sistema nervoso/cervello.

D’altra parte, è importante fin da subito sottolineare che, sebbene

molto potente, il modello circuitale, al pari di ogni modello dell’Ingegneria,

è in grado di cogliere solo alcuni aspetti della realtà fisica che vuole

rappresentare. Come tale esso ha dei limiti di validità. Per questo

motivo è importante non solo apprenderne l’uso ma anche saper

riconoscere i suoi limiti di applicazione.