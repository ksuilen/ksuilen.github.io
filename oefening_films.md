---
permalink: /oefening_films.html
title: "Oefening: Films"
categories: verdieping
---

Vroeger was er zoiets als een videotheek, waar je videobanden en later dvd's en blueray's kon huren. Tegenwoordig kun je films online "huren" op verschillende plekken.    
We stappen in een tijdmachine en gaan terug in de tijd naar een  videoverhuurbedrijf waar ze videobanden verhuren.

# Doel
- Basis SQL commando's toepassen

# Voorkennis
- Importeren van een database (zie ook de Howto die hierover gaat);
- SQL basis (select, from, where, distinct, in, not, null, between, like, and, or, not & basisfuncties rekenen: max, min, count, sum, avg).

**Tip**: Kijk bij de [Howto's](index_howtos) en [Cheatsheets](index_cheatsheets) (of zoek andere bronnen) als je ergens niet uit komt!

# Opgave
- Importeer de database op een manier zodat je er via RStudio bij kunt;
- Maak een Notebook aan en leg connectie naar de database;
- Maak per vraag (zie hieronder) een SQL chunk aan met boven de chunk de vraag en in de chunk de SQL statements om de vraag te beantwoorden.

**Tip**:  Misschien is het handig om eerst een ERD te tekenen, om inzicht te krijgen hoe de database in elkaar zit.   

Vragen:
1. Geef de titel en de speelduur van alle Westerns op volgorde van titel. 
2. Welke films zijn er gemaakt over Batman? Geef de titel. 
3. Welke films zijn geregisseerd door regisseur 161? Geef titel, speelduur en jaar. 
4. Welke films voorzien in een kinderbegeleiding tot 15-jaar? Geef titel en genre. Sorteer op genre. 
5. Welke films werden tussen 1988 en 1990 gemaakt? Geef titel en regisseurnummer. Sorteer op regisseurnummer. 
6. Welke films werden voor 1940 gemaakt en zijn in kleur opgenomen? Geef filmnr, titel en jaar. 
7. Hoe lang duurde de film Gone with the wind?
8. Geef de verschillende filmmaatschappijen alfabetische gerangschikt. 
9. Welke films zijn tussen 1950 en 1960 in zwart-wit gemaakt en hebben een 4-sters waardering? Geef titel, waardering, kleur en jaar. 
10. Welke titels hebben een 1-ster-waardering? 
11. Welke films hebben een speelduur van 80 tot 100 minuten? Geef titel en genre.
12. Van welke film is de kleur niet bekend? 
13. Welke films hebben de substring co (niet hoofdlettergevoelig) in hun titel? Geef de titel. 
14. Geef de filmnummers en titels van alle films met een 5-ster waardering. Sorteer op titel. 
15. Geef filmnummer, genre en titel van alle films waar een ouderbegeleiding geldt. Sorteer het overzicht naar genre en daarbinnen naar titel. 
16. Geef het filmnummer en de titel van alle films die behoren tot het genre Oorlog, Religieus, Rampen of Mysterie. 
17. Welke leden uit Lieshout zijn sinds wanneer lid? 
18. Welke leden hebben een bonuswaardering van drie? Geef naam en woonplaats. 
19. Wat is kortste en langste speelduur van alle aanwezige titels? 
20. Hoeveel films hebben geen nominaties gehad? 
21. Wat is de gemiddelde speelduur van Science fiction-films? 
22. Hoe luiden de filmtitels die alfabetisch gezien het eerst en het laatst voorkomen? 
23. Wat is de gemiddelde bonus in Eindhoven? 


## Materialen:
- [Database](assets/file/DATABASE_FILM.zip) in deze zip staan verschillende varianten van dezelfde database qua inhoud, en elk type gaat net iets anders om met bepaalde zaken en zal daardoor soms net iets anders reageren (FYI: de uitwerkingen zijn gebaseerd op de MySQL variant, gehost op FHICT infra)
- [Verwachte uitkomsten](assets/file/Films.pdf)