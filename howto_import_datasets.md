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

We gaan hier in op een aantal voorbeelden, maar een google opdracht op *Rstudio import data from...* helpt je vaak al!


## 1. Importeren van CSV/Excel/TXT data
Data in CSV, Excel (xlsx) of .txt bestanden zijn over het algemeen vrij eenvoudig te importeren. Zeker als je net begint met R, zijn dit de meest gebruikte data bronnen. Toch zijn er wel wat aandachtspunten die je kunnen helpen om probleemloos de data in je Notebook te krijgen.

Voor alle soorten textbestanden gedlt dat je even moet checken mbv Excel of een text editor als Visual Studio Code of Atom of Notepad of de bestanden:
- Kolomkoppen gebruiken
- Er niet nog bv uitleg of iets dergelijks in verwerkt zit op de eerste regels. Die moet je er dan even uit halen

in dit [**support artikel**](https://support.rstudio.com/hc/en-us/articles/218611977-Importing-Data-with-RStudio) wordt uitgelegd hoe je dat doet.
Een paar aandachtspunten:
- Als je de import dataset wizard gebruikt voor excel/csv: Kopieer de code die rechtsonder in t venstertje `code preview` wordt getoond, behalve het `View(...)` stukje,
- Plak dat stuk code in een nieuwe chunk, liefst bovenin, nadat je libraries hebt geladen.
- Run de chunk om te controleren.
- Daarmee gaat het knitten van je code vaak ook al meteen een stuk beter omdat je geen fouten krijgt mbt data die neit gevonden kan worden.
- Om XLSX files te laden, heb je de library `readxl` of `read_excel` nodig. Je kan data uit een specifieke worksheet importeren daar deze als 2e paramter in de import mee te geven. bv: `my_data <- read_excel("my_file.xls","sheet2")`
- CSV en TXT werken het beste icm de `readr` library. 

## 2. Importeren van data uit een database
**let op:** We gaan hier alleen in op het verbidning maken met een databse. hoe je SQL kan gebruiken in R/Rstudio komt in een ander artikel aan bod.

Databases komen in vele varianten en van vele leveranciers. Hier proberen we je te helpen om te werken met 2 veelgebruikte databases in het startsemester: een SQLite database en een MySQL database. Dit is de situatie waar we vanuit gaan:
- SQLite databases zijn zogenaamde *portable databases* : databases in de vorm van een bestandje (bv een .db of .sqlite bestand)
- MySQL is een hosted database (bv op de FHICT servers) : deze benaderen we via een url & eventueel mbv een vpn verbinding.

### Verbinden met een SQLite database
1. Library gebruiken/installeren. Meest gebruikte is `library(RSQLite)`
2. Verbinding maken (connectie), met het huiste bestand, bijvoorbeeld: `con <- dbConnect(SQLite(), "verkopen.db")`
3. `con` is het object/element dat je in het vervolg gebruikt om queries uit te voeren op de database.
3. Test door bv alle tabelnamen op te halen : `dbListTables(con)`

Je hebt het nu voor elkaar om gegevens uit de database op te kunnen vragen. Dat kan door een SQL chunk in te voegen in je notebook en de output van de SQL querie in een data frame op te slaan. 1 voorbeeld. 

**let op:** de bovenste regel zijn da parameters van een SQL chunk 
![sql voorbeeld](assets/img/db_example_1.png) 

Meer informatie en hulp:
[Datacamp tutorial](https://www.datacamp.com/community/tutorials/sqlite-in-r)
[R tutorial & hulpfiles](https://db.rstudio.com/databases/sqlite/)

### Verbinden met een MySQL database
Om  gegevens uit een MySQL database op te kunnen halen moet je een paar zaken weten/regelen:
- Heb je een actieve VPN verbinding nodig? Dat is bv bij de FHICT MySQL databases wel nodig! zorg dan dat deze actief is.
- Je hebt een url, username en wachtwoord nodig. die van de fhict MySQL database kun je bv vinden via de [selfservice portal](https://selfservice.app.fhict.nl/Database/Mysql)

Als je dit weet/geregeld hebt, werkt het vergelijkbaar met SQLite, met het verschil dat de connectie opbouwen net iets uitgebreider is.

1. Library gebruiken/installeren `library(RMariaDB)` en `library(DBI)`. Deze libraries bevatten *drivers* voor verschillende database types
2. Verbinding maken mbv een connectie string, bv :
> `con = dbConnect(RMariaDB::MariaDB(), user='dbi123456', password='Wachtwoord', dbname='dbi123456', host='studmysql01.fhict.local')`
3. Zie voor het opvragen van data de zelfde aanpak als bij SQLite.

Meer info via dit [artikel](https://db.rstudio.com/databases/my-sql/)
## 3. Verbinden met een API
Application Programming Interfaces zijn een soort digitale butlers, waarbij data via een url kan worden opgevraagd.
bijvoorbeels iets als:
>`http://myorg.com/api/getUsers`
zou een JSON text bestand met alle users terug kunnen geven.

Veel bekende cloud diensten hebben (betaalde) API's die je kan gebruiken. denk bv aan Spotify of Google Analytics. Om gebruik te kunnen maken van zo'n dienst heb je vaak een developer account nodig, en krijg je een eigen *sleutel* waarmee de API jou kan identificeren en de juiste toegang geeft.

In R zijn er vaak kant en klaar libraries die veel van de handelingen in t werken met een APi (authenticatie etc) voor je regelen.

Dit is een onderwerp dat past bij de verdieping (en verder), maar mocht je hier mee aan de slag willen, check dan bv eens:
- [Spotify & R tutorial](https://medium.com/swlh/accessing-spotifys-api-using-r-1a8eef0507)
- [Open Weather map](https://github.com/mukul13/ROpenWeatherMap)
