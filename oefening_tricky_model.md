---
permalink: /oefening_tricky_model.html
title: "Oefening: Tricky modellering"
categories: verdieping
---

Een kort verhaaltje geeft, al iets minder dan een gestructureerde set gegevens, vrij duidelijk weer welke onderdelen er in het ERD moeten komen. Lastiger wordt het, wanneer je vanuit een wat complexere casus hoofd- en bijzaken moet scheiden om tot de kern van je model te komen.   
In deze opdracht ga je vanuit een wat langere casus een ERD opstellen.

# Doel
- ERD opstellen vanuit een complexere casus
- Scheiden van hoofd- en bijzaak

# Voorkennis
- ERD syntax

# Opgave
Teken een ERD dat past bij de onderstaande casus.   

De belangrijkste dienstverlening van hotel "Zeezicht" is het beschikbaar stellen van kamers aan gasten, uiteraard tegen vergoeding. Van de kamers worden de volgende gegevens bijgehouden: kamernummer, aantal bedden (max. 3), met- of zonder bad, met of zonder tv, en de basisprijs. Bovendien is van belang of in de kamer mag worden gerookt. Alleen kamers met meer dan 1 bed kunnen een bad hebben. Kamers met 3 bedden kunnen ook een balkon hebben.   

Kamers worden vooraf door gasten geboekt. Bij een boeking wordt eerst vastgesteld of het om een "nieuwe" of een "oude" gast gaat. Gaat het om een nieuwe gast, dan moeten eerst gegevens van de gast worden geregistreerd: naam, adres, woonplaats, geb.datum (overige gegevens worden bij de aankomst geregistreerd). De gast krijgt bovendien een uniek gastennummer. Bij een boeking worden de boekingsdatum, de aankomst- en de vertrekdatum vastgelegd. Eventueel kan er sprake zijn van een kortingspercentage. Bovendien wordt een boekingsnummer toegewezen.   

Een boeking bestaat uit een of meer kamerreserveringen. Per kamerreservering is het aantal gasten (per kamer) en het verblijfstype van belang: volpension (V), halfpension (H) of alleen ontbijt (O).   

Bij aankomst worden de gasten ingeschreven (checkin). Als het om nieuwe gasten gaat, worden naam, adres, woonplaats en geboortedatum geregistreerd (van de boekende gast is dit reeds geschied). Bovendien wordt aangegeven, of het een roker- of niet-roker betreft. Verder is het nummer van het identificatiebewijs (bijv. paspoort) van belang. Ook krijgt de gast een uniek gastennummer. Als de gast niet de boekende gast is wordt ook bijgehouden wie de boekende gast was voor de betreffende gast. Daarna krijgt de gast een van de bij de boeking gereserveerde kamers toegedeeld. Na inlevering van zijn paspoort krijgt hij/zij een gastenpasje met een uniek pasnummer (nieuw volgnummer).  

Bij aankomst wordt de boeking meteen gefactureerd en betaald. Het te betalen bedrag is afhankelijk van de verblijfsduur, de basisprijs per kamer en de toeslag per persoon voor het verblijfstype (O €20,-, H €60,- en V €100,-). Het kortingspercentage heeft alleen betrekking op de basisprijs van de kamer.   

Tijdens hun verblijf maken de gasten extra onkosten, die betrekking hebben op het gebruik van bepaalde producten (waaronder ook diensten vallen). Van deze producten zijn de volgende gegevens relevant: productcode, productsoort (H = hapje, D = drankje, R = rookwaar, T = telefoontik), omschrijving en prijs. Op vertoon van het pasje wordt telkens een nota aangemaakt met een uniek notanummer, het pasnummer van de gast, de datum en natuurlijk de productcode en de hoeveelheid van het betreffende product. Bij zijn vertrek levert de gast zijn pasje in ter vernietiging, betaalt de nota's en ontvangt zijn paspoort weer terug.