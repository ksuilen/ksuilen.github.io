---
permalink: /oefening_structuur.html
title: "Oefening: Structuur naar ERD"
categories: verdieping
---

Wat een ERD is kun je op Canvas en op internet vinden. Snappen wat een ERD is, is één ding en er eentje zelf kunnen maken wat anders. In deze oefening ga je aan de hand van een paar voorgestructureerde sets gegevens een ERD opstellen en een aantal vragen beantwoorden. 

Het opstellen van ene ERD vanuit voorgestructureerde gegevens is net iets makkelijker dan vanuit een verhaal, of vanuit je eigen idee, een ERD opstellen omdat bijna alle "onzinnige" informatie al voor je gefilterd en gestructureerd is. 

# Doel
- ERD op kunnen stellen op basis van gestructureerde gegevens; 
- ERD kunnen analyseren aan de hand van vragen.

# Voorkennis
- ERD syntax (symbolen en notatie)

# Opgave
1. Stel, de ISSD gebruikt de onderstaande gegevensstructuur voor het uitlenen en reserveren van materialen.    
De eigenschappen die **_dikgedrukt en schuin_** worden weergegeven, zijn de uniek identificerende eigenschappen.   
Teken het ERD en beantwoord de vragen onder de tabel.   

| Entiteit      | Eigenschappen                                             |
|---------------|-----------------------------------------------------------|
| ITEM          | **_artikelnummer_**, fabrikant, typenaam                  |
| EXEMPLAAR     | **_barcode_**, artikelnummer, plaats                      |
| UITLENING     | **_barcode_**, **_pasnummer_**, verloopdatum              |
| RESERVERING   | **_artikelnummer_**, **_pasnummer_**, reserveringsdatum   |
| STUDENT       | **_pasnummer_**, naam, klas                               |

Vragen:
* (a) Leg uit of student Jan het item "Arduino Rich Shield" meerdere malen tegelijk kan reserveren. Waarom wel of niet?
* (b) Leg uit of student Jan en Marian gelijktijdig een item met artikelnummer 90343211234 geleend kunnen hebben. Waarom wel of niet?
* (c) Leg uit of medewerker Piet het item "Ultrosone sensor" kan lenen. Waarom wel of niet?

2. Er zijn twee maneges vlakbij Tilburg: Manege Boszicht en Manege Hoefslag. Hieronder vind je voor beide de gegevensstructuur.   
De eigenschappen die **_dikgedrukt en schuin_** worden weergegeven, zijn de uniek identificerende eigenschappen.   
Teken voor beide maneges een eigen ERD en beantwoord daarna de vragen verderop.   

**Manege Boszicht**   

| Entiteit      | Eigenschappen                                         |
|---------------|-------------------------------------------------------|
| RUITER        | **_ruiternr_**, naam, adres, telnr                    |
| RESERVERING   | **_ruiternr_**, **_paardnaam_**, **_datum_**, tijd    |
| PAARD         | **_paardnaam_**, ras, leeftijd, geschikt              |

**Manege Hoefslag**   

| Entiteit      | Eigenschappen                                                 |
|---------------|---------------------------------------------------------------|
| RUITER        | **_ruiternr_**, naam, adres, telnr                            |
| RESERVERING   | **_resnr_**, ruiternr, paardnaam, ponynaam, datum, tijd       |
| PAARD         | **_paardnaam_**, ras, leeftijd, geschikt                      |
| PONY          | **_ponynaam_**, ras, leeftijd, schofthoogte, moeder, vader    |   

Vragen:   
* (a) Leg uit of ruiter Femke op manege Boszicht het paard Fury meerdere malen kan reserveren. Wanneer wel en wanneer niet?
* (b) Leg voor beide maneges uit of Femke en Suzanne hetzelfde paard bij die manege op dezelfde dag kunnen reserveren. Waarom wel of niet?
* (c) Leg uit of manege Boszicht meerdere paarden hebben met de naam Fury. Waarom wel of niet?
* (d) Leg uit of ruiter Femke op manege Hoefslag op hetzelfde moment zowel een paard als een pony kan reserveren. Waarom wel of niet?