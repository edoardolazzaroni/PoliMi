

# **Capitolo I: Il modello circuitale**


## 1.1 **Sistemi elettrici e loro modelli**

In questo corso, acquisiremo la capacità di eseguire l’analisi dei sistemi elettrici. Dalla descrizione di un dato sistema in termini di elementi che lo compongono e di come sono connessi tra di loro, impareremo una metodologia generale per calcolare il valore delle grandezze elettriche che lo descrivono e con esse a capire come funziona e a che cosa serve. L’obiettivo verrà raggiunto diventando padroni di un modello matematico fondamentale dell’Ingegneria chiamato il **modello circuitale**.

Va precisato che il termine di sistema elettrico può riferirsi a realtà fisiche molto diverse tra loro e tutte fondamentali per la preparazione dell’Ingegnere dell’area ICT (Information and Communication Technology). Facciamo degli esempi._

- Un primo tipo di sistema elettrico è rappresentato dalla rete di trasporto/distribuzione dell’energia elettrica. Questa è formata da un insieme di fili di rame, chiamati conduttori, che collegano punti in cui l’energia viene prodotta (*es*: le centrali elettriche, impianti fotovoltaici...) ai punti in cui viene utilizzata (*es*: le nostre abitazioni, gli impianti industriali, le linee di trasporto metropolitano o dei treni). Tali reti hanno dimensioni dell’ordine delle centinaia di chilometri dato che si possono estendere su tutto il territorio di una nazione.
- Un secondo esempio, altrettanto rilevante, è rappresentato dai sistemi della micro e nano elettronica. Questo secondo esempio di rete non ha lo scopo di trasportare energia bensì di elaborare l’informazione. L’energia elettrica nel primo esempio e l’informazione nel secondo sono rappresentate (o determinate) da alcune grandezze fisiche misurabili chiamate <u>grandezze descrittive</u>.

Nonostante la spaventosa differenza di scala geometrica tra una rete per l’energia e un processore elettronico il comportamento elettrico di questi sistemi può venire descritto dallo stesso modello circuitale. La tecnica di modeling, cioè la costruzione del modello, si basa sull’identificazione delle grandezze fisiche descrittive che chiameremo tensione e corrente elettrica e sulla scrittura delle leggi che le governano. Nel modello, le grandezze fisiche sono sostituite da variabili matematiche (indicate $v, i$) mentre le leggi fisiche si traducono in equazioni che legano tali variabili, come mostrato in figura:
![[Elettrotecnica-1792681850745.webp|274]]
#Figura (1). *Il processo di modeling*


D’altra parte, è importante fin da subito sottolineare che, sebbene molto potente, il modello circuitale, al pari di ogni modello dell’Ingegneria, è in grado di cogliere solo alcuni aspetti della realtà fisica che vuole rappresentare. Come tale esso ha dei limiti di validità. Per questo

motivo è importante non solo apprenderne l’uso ma anche saper

riconoscere i suoi limiti di applicazione.