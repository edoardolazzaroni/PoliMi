#INDEX of all personal appointments

```dataview
LIST
FROM "PoliMi/Calendari/Calendario personale"
dv.pages('#favorite').sort(f=>f.file.name,"desc").limit(9).file.link
````