---
permalink: /howto_mockdata.html
title: "Howto guides - Mockdata"
categories: howto
---
# Waarom Mockdata?
Mockdata, of testdata, is heel handig om bijvoorbeeld te oefenen met je vaardigheden of je Notebooks te prepareren voordat je de echte klantdata krijgt. Stel dat je bijvoorbeeld wacht op een export of database toegang, dan kun je door gebruik te maken van het datamodel van de dataset zelf vast oefendata maken. Ook kan goede testdata het makkelijker maken om te begrijpen wat er niet klopt als je tegen problemen aan loopt tijdens de ontwikkeling van je Notebook.

# Bepalen eisen aan je mockdata
Een datamodel beschrijft welke relaties, kolommen & datatypes je data bevat. Met behulp van een ER-Model kun je dat opstellen. Als je werkt met externe data via API's, dan kun je gebruik maken van de API documentatie. Zo beschrijven Google en Spotify welke data ze aanleveren en in welk formaat.  
Je moet je voor het genereren bijvoorbeeld afvragen:
- Hoeveel records heb ik nodig?
- Moet er (statistische) spreiding in mijn data zitten?
- Zitten er onderlinge afhankelijkheden in mijn data (als waarde a = x, dan b = y)
- Wil ik ook 'foute' data genereren, bijvoorbeeld lege cellen/waardes?

# Realiseren Mockdata
In de praktijk kun je vaak toe met de eerste optie, Mockaroo. Soms kan het voor het verder bewerken van je mock data handig zijn met Excel nog wat te doen. Als je eenvoudige data wil, dan kan R deze misschien ook voor je genereren.
## [Mockaroo](http://www.mockaroo.com){:target="_blank"}
Op zich wijst Mockaroo zichzelf wel, en er zijn legio tutorials te vinden. Toch een paar tips:
- Gebruik **Custom Lists** als datatype als je zelf wilt bepalen uit welke range van waardes je een kolom wilt vullen. Bijvoorbeeld: je wilt klantendata genereren en hebt een kolom `abonnementsvorm` die de waardes **Gold**,**Silver**, of **Bronze** heeft. Met een custom list en een custom distribution kun je dan dingen aangeven als dat voor iedere Gold klant er 3 Silver en 5 Bronze klanten zijn.
![mockdata 1](assets/img/mock_1.png)
- Je kunt via de ingebouwde syntax/formules nog meer aanpassen, zie de [formula help](https://www.mockaroo.com/help/formulas){:target="_blank"}

## Excel
Excel is behoorlijk krachtig als het gaat om databewerking en door slim gebruik te maken van diverse (minder bekende) functies kun je je eigen data nog aardig vorm geven. Een paar voorbeelden:

### 1. Excel - Normaal verdeelde data aanmaken
Als je een beetje iets van statistiek weet, dan zegt het begrip [normaal verdeling](https://nl.wikipedia.org/wiki/Normale_verdeling) je wel iets. In Excel kun je op basis van een gemiddelde en een standaard deviatie een dataset genereren. Zie dit voorbeeld voor waardes die rond de 500 liggen met een standaard deviatie van 25.
![mockdata 2](assets/img/mock_2.png)
> Formule `=ROUND(NORM.INV(RAND();$B$2;$B$1);0)`
met het bekende plusje sleep je de waarde (492) omlaag en genereer je meerdere waardes.

### 2. Excel - Samenvoegen
Een veelgebruikte functie is het samenvoegen van 2 of meer tekstwaardes, het zogenaamde *concateneren*. Dat doe je bijvoorbeeld als je emailadressen wilt maken van de voor- en achternamen.
![mockdata 3](assets/img/mock_3.png)
> Formule `=CONCAT(A2;".";B2;"@";"mydomain.com")`

### 3. Excel - Lookup
Een van de meest gebruikte functies in Excel is misschien de [(V/H)Lookup functie](https://exceljet.net/excel-functions/excel-vlookup-function). Deze kun je bijvoorbeeld gebruiken om artikelnummers te vertalen naar categoriën.   
Stel: je wil een artikel dat eindigt op een cijferrange (1 tm 3 bv) koppelen aan een categorie *witgoed*:
- Eerst het meest rechts karakter uit het artikelnr halen mbv de `Right` functie.
- Die waarde als nummer converteren mbv de `INT` functie.
- Resultaat aan de VLookup meegeven. Let op de $ bij de opzoektabel 
![mockdata 4](assets/img/mock_4.png)
> Formule  `=VLOOKUP(INT(RIGHT(A2;1));$D$1:$E$11;2;FALSE)`

## R
Als je eenvoudige data (een lijst met random nummers o.i.d.) wilt genereren, kan dat ook in R zelf. Zie dit [ebook voor het hoe en wat](https://bookdown.org/ndphillips/YaRrr/generating-random-data.html)