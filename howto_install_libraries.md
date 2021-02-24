---
permalink: /howto_install_libraries.html
title: "Howto guides"
---
# Over libraries (packages)
Omdat ieder project eigen functionaliteit behoeft, en je niet iedere keer het wiel opnieuw wil uitvinden, kun je gebruik maken van setjes voorgedefinieerde functionaliteit. Zie Rstudio als een kale Word of Excel, waarbij je de ribbon vult met knoppen door zelf libraries (of packages zoals programmeurs zeggen) toe te voegen.
Zo hebben specifieke databronnen vaak hun eigen library (denk aan [GoogleAnalyticsR](https://code.markedmondson.me/googleAnalyticsR/), SQLServer/MySQL of [SpotifyR](https://www.rdocumentation.org/packages/spotifyr/versions/1.0.0)])

## Installeren  nieuwe libraries
Krijg je een melding in je notebook met iets n de richting van `could not find..` of `could not load..` dan heb je dikke kans dat de betreffende library nog niet geinstalleerd is bij jou.

Libraries installeren **doe je niet vanuit een Notebook**, omdat dit een eenmalige actie is. het gebruiken van een library doe je wel in je notebook.

Installatie kan op 2 manieren:
- Via de GUI van Rstudio. klik op Install en vervolgens tik je de naam van je library in.
![installatie 1](assets/img/lib_install_1.png)  
Zoals jeziet kun je hier ook al vinden welke libraries er al geinstalleerd zijn.
![installatie 2](assets/img/lib_install_2.png)

- Ben je iets handiger dan dat, wil je sneller aan de slag of meot je evt issues oplossen? dan gebruik je uiteraard de console! mbv een `install.packages()` commando geef je dan aan welke library je wil hebben. bv: 
    `install.packages("tidyverse")`

    De console vind je normaal gesproken links onderaan.

## Gebruiken library
Omdat Notebooks geschikt zijn om over te dragen aan iemand anders en jouw bevindingen te reproduceren, moet die persoon ook weten welke libraries je daarvoor gebruikt hebt. Daarom laadt je in ieder notebook expliciet de benodigde libraries in.

Goed gebruik is om dat meteen in t begin van je document te doen en daar 1 chunk te maken waarin je de setup doet. Zoiets als hieronder dus:
> `library("tidyverse")`  
> `library("ggplot2")`

Dan kom je neit halverwege allerlei nieuwe libraries tegen en heb je een goed beeld van de benodigde afhankelijkheden.