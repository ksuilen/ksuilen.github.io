---
permalink: /howto_installatie.html
title: "Howto guides - installatie"
---
# Gebruiken en installeren van R & RStudio
Op deze pagina vind je informatie over het gebruiken en installeren van R & RStudio en over de Notebooks die we daarin aanmaken. 

## RStudio
Allereerst is het goed om te weten dat je verschillende keuzes hebt:
- **RStudio Cloud gebruiken**.  
Gebruik je incidenteel RStudio en heb je weinig behoefte om te installeren, wil je vooral even proberen: gebruik dan [RStudio Cloud](https://rstudio.cloud/). Deze is gratis te gebruiken en geschikt voor proefstuderen en incidenteel gebruik. Je maakt hier zelf een account aan. Zie voor meer info de [guide](https://rstudio.cloud/learn/guide).   
Eventuele bestanden moet je altijd eerst uploaden naar de cloud server! 

    **Let op**: Deze versie is slechts 15 uur per maand te gebruiken volgens de huidige voorwaarden, dat zal te weinig zijn om de oriëntatie mee door te komen.

- **RStudio server van FHICT gebruiken**.  
Heb je behoefte aan wat meer mogelijkheden en loop je tegen de grenzen aan van de cloud versie? Dan hebben we binnen FHICT een eigen RStudio server. Dit kan handig zijn als je lokaal vast loopt, geen nieuw account op RStudio Cloud aan wil maken, of je eigen installatie niet om zeep wil helpen :). Ga naar de [FHICT Rstudio server](https://rstudio.app.fhict.nl/) en log in met je **I account (nummer zonder @fhict.nl)**. Het werkt vergelijkbaar met RStudio Cloud.   
Eventuele bestanden moet je dus altijd eerst uploaden (naar de FHICT server)! 

- **Installeer R & RStudio lokaal op je eigen machine**.  
Dit is aan te raden als je zelf controle wilt over welke libraries je wilt kunnen installeren, je lokale bestanden makkelijk wilt kunnen gebruiken en als je met diverse databronnen wilt kunnen koppelen.  
Ga je de verdieping ICT & Business doen, kies dan dit.  
Je moet hier **2 stappen** voor doen, in deze volgorde:
    1. Installeer de programmeertaal R.  
    Dit is de zogenaamde 'interpreter' die R code kan uitvoeren. Via [deze site](https://cloud.r-project.org/) kom je bij de download pagina uit. Check vervolgens welk besturingssysteem je nodig hebt en pak de meest recente installer (.exe voor Windows of .pkg voor Mac)
    2. Installeer de ontwikkelomgeving Rstudio.  
    Dit is de user interface waarin je handig je Notebooks (werkbestanden) kan bewerken, net zoiets als Visual Studio. Je kunt Rstudio [hier vinden](https://rstudio.com/products/rstudio/download/). Let op dat je de Free/Open Source versie pakt voor jouw besturingssysteem.  
    
    Kom je er niet uit? [Er zijn voldoende tutorials te vinden](https://bfy.tw/QRhs).

## Notebooks
We gebruiken eigenlijk altijd zogenaamde Notebooks. Dat zijn .Rmd (RMarkdown) bestanden waar je uitleg, code (chunks) & output samen kunt voegen. Dit zorgt o.a. voor herhaalbaarheid en leesbaarheid van je stappen, een hele verbetering t.o.v. data analyse in MS Excel.   
Rstudio opent standaard niet met een Notebook. Dat moet je zelf openen of aanmaken als je aan de slag gaat. Check bijvoorbeeld eens [deze guide](https://rmarkdown.rstudio.com/lesson-2.html).