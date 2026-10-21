
___


> [!hint]
> Per aspera ad astra.


```contributionGraph
title: Contributions
graphType: default
dateRangeValue: 180
dateRangeType: LATEST_DAYS
startOfWeek: "1"
showCellRuleIndicators: true
titleStyle:
  textAlign: center
  fontSize: 15px
  fontWeight: normal
dataSource:
  type: PAGE
  value: ""
  dateField:
    formatType: moment
    type: FILE_MTIME
  filters: []
fillTheScreen: false
enableMainContainerShadow: false
cellStyleRules:
  - id: Ocean_a
    color: "#8dd1e2"
    min: 1
    max: 2
  - id: Ocean_b
    color: "#63a1be"
    min: 2
    max: 3
  - id: Ocean_c
    color: "#376d93"
    min: 3
    max: 5
  - id: Ocean_d
    color: "#012f60"
    min: 5
    max: 9999

```

```dataviewjs

this.container.style.minHeight = "1000px";
const { renderCalendar } = app.plugins.plugins["obsidian-full-calendar"];
let today = moment().format("GGGG-[W]WW");
let rawData = await dv.io.csv("DataStores/csv/" + moment().format("GGGG-[W]WW") + ".csv");
let entries = rawData.map((p) => ({
backgroundColor: p.calendar == 'family' ? '#452538' : '#4d95f7',
borderColor: this.app.vault.getAbstractFileByPath(p.id + ".md") ? '#406f0b' : '#4d95f7',
allDay: p.allDay,
start: DateTime.fromISO(p.start).toJSDate(),
end: DateTime.fromISO(p.end).toJSDate()|
|id: p.id + ".md",|
|title: this.app.vault.getAbstractFileByPath(p.id + ".md") ? '📄' + p.title : p.title,|
|}));|
|// console.log(entries.array());|
|let isMobile = window.innerWidth < 500;|
|let calendar = renderCalendar(this.container, [entries.array()], {|
||
|weekNumbers: true,|
|initialView: 'dayGridMonth',|
|eventClick: async (info) => {|
|console.log(info.event.id)|
|let fileExists = await this.app.vault.adapter.exists(info.event.id);|
|if (fileExists) {|
|let file = this.app.vault.getAbstractFileByPath(info.event.id);|
|console.log(file)|
|if (info.jsEvent.getModifierState("Control")|
|\| info.jsEvent.getModifierState("Meta")) {|
|let leaf = this.app.workspace.createLeafBySplit(this.app.workspace.getMostRecentLeaf(), "vertical");|
|await leaf.openFile(file);|
|calendar.render();|
|} else {|
|let leaf = this.app.workspace.getMostRecentLeaf();|
|await leaf.openFile(file);|
|}|
|}|
|},|
|eventMouseEnter: (info) => {|
|console.log(info)|
|const path = info.event.id;|
|this.app.workspace.trigger("hover-link", {|
|event: info.jsEvent,|
|source: "custom-cal",|
|hoverParent: info.jsEvent.target,|
|targetEl: info.jsEvent.target,|
|linktext: path,|
|sourcePath: path|
|});|
|}|
||
|});|
|calendar.setOption('weekNumbers', true)|
|calendar.setOption('firstDay', 1)|
|calendar.setOption('scrollTime', 7)|
|calendar.setOption('displayEventEnd', false)|
|calendar.setOption('displayEventTime', false)|
||
||
|calendar.render();|
||
|```|
```

- ## Impegni del giorno 📋 :

	[[kanban-default.base|Kanban (elenco tasks)]]:
	
	**Università 🎓**:
	
	 [[Finire capitolo 5 di GAL]]
	 [[finire capitolo 6 GAL]]
	 [[finire esempi GAL]]
	 [[inserire immagini nel file di GAL]]
	 [[finire mappa C(89)]]
	 [[guardare esercitazione GAL-2]]
	 [[riguardare appunti esercitazioni analisi 1]]
	
	
	**Altro 🏖️**:
	
	 [[Leggere almeno un capitolo]]
	 [[Caricare tavoletta grafica]]
	 [[Caricare cuffie]]
	 [[Sistemare stanza]]
	 [[Preparare zaino uni]]
	 

- ## Repository dei corsi 📚:
	
	[[Geometria e Algebra Lineare]]
	[[Fondamenti di Informatica]]
	[[Algoritmi e Principi dell'Informatica]]


- ## Link utili 🔗:
	
	[<font color="#0070c0">Polimi.it</font>](https://www.polimi.it)
	[<font color="#76923c">WeBeep</font>](https://webeep.polimi.it/my/courses.php)
	[<font color="#00b0f0">Outlook</font>](https://outlook.cloud.microsoft/mail/)
	[<font color="#000000">GitHub</font>](https://github.com)
	[<font color="#ff0000">Palestra Giuriati</font>](https://ecomm.sportrick.com/sportpolimi)


- ## Obiettivi ✅ :
	
		- Studiare almeno 6 ore al giorno
		- Ricominciare palestra (2/3 volte a settimana)
		- Finire Power
		- Ridurre l'utilizzo di Instagram a massimo 30 min al giorno
		- Iniziare a lavorare ad Hært



Calendario integrato in Obsidian, impegni conservati nella cartella [[Calendario]].
Integrazione con Copilot (harness Opencode), dotato di [[copilot]].

Questo vault è gestito e sincronizzato mediante [[Github]].