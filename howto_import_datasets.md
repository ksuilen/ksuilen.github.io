---
permalink: /howto_import_datasets.html
title: "Howto guides - importing data"
---
# Data bronnen
R is bij uitstek geschikt om data uit diverse bronnen te importeren/ te gebruiken. Vaak zul je met gestructureerde data (data in bv tabelvorm) werken naar R kan ook met ongestructureerde data (tekst bv ) werken.  Veelvoorkomend zijn:
- CSV/XLSX/TXT
- Databases, zoals MySQL, SQLite, MSSQL..
- API's
- JSON
We  gaan hier in op een aantal voorbeelden, maar een google opdracht op *Rstudio import data from...* helpt je vaak al!

## 1. Importeren van CSV/Excel/TXT data
Data in CSV, Excel (xlsx) of .txt bestanden zijn over het algemeen vrij eenvoudig te importeren. Zeker als je net begint met R, zijn dit de meest gebruikte data bronnen. Toch zijn er wel wat aandachtspunten die je kunnen helpen om probleemloos de data in je Notebook te krijgen.

Voor alle soorten textbestanden gedlt dat je even moet checken mbv Excel of een text editor als Visual Studio Code of Atom of Notepad of de bestanden:
- Kolomkoppen gebruiken
- Er niet nog bv uitleg of iets dergelijks in verwerkt zit op de eerste regels. Die moet je er dan even uit halen

in dit [**support artikel**](https://support.rstudio.com/hc/en-us/articles/218611977-Importing-Data-with-RStudio) wordt uitgelegd hoe je dat doet.
Een paar aandachtspunten:
- Kopieer de code die rechtsonder in t venstertje `code preview` wordt getoond, behalve het `View(...)` stukje,
- Plak dat stuk code in een nieuwe chunk, liefst bovenin, nadat je libraries hebt geladen.
- Run de chunk om te controleren.
- Daarmee gaat het knitten van je code vaak ook al meteen een stuk beter omdat je geen fouten krijgt mbt data die neit gevonden kan worden.
- Om XLSX files te laden, heb je de library `readxl` of `read_excel` nodig. Je kan data uit een specifieke worksheet importeren daar deze als 2e paramter in de import mee te geven. bv: `my_data <- read_excel("my_file.xls","sheet2")`
- CSV en TXT werken het beste icm de `readr` library. 

## 2. Importeren van data uit een database
Databases komen in vele varianten en van vele leveranciers. Hier proberen we je te helpen om te werken met 2 veelgebruikte databases in het startsemester: een SQLite database en een MySQL database. Dit is de situatie waar we vanuit gaan:
- SQLite databases zijn zogenaamde *portable databases* : databases in de vorm van een bestandje (bv een)

