---
permalink: /oefening_films3.html
title: "Oefening: Films 3"
categories: verdieping
---

Vroeger was er zoiets als een videotheek, waar je videobanden en later dvd's en blueray's kon huren. Tegenwoordig kun je films online "huren" op verschillende plekken.   
We stappen in een tijdmachine en gaan terug in de tijd naar een  videoverhuurbedrijf waar ze videobanden verhuren.

# Doel
- SQL subqueries en joins toepassen

# Voorkennis
- Importeren van een database;
- SQL basis + subqueries en joins

# Opgave
- Importeer de database op een manier zodat je er via RStudio bij kunt;
- Maak een Notebook aan en leg connectie naar de database;
- Maak per vraag (zie hieronder) een SQL chunk aan met boven de chunk de vraag en in de chunk de SQL statements om de vraag te beantwoorden.

**Tips**: 
- Misschien is het handig om eerst een ERD te tekenen, om inzicht te krijgen hoe de database in elkaar zit;
- Schrijf net onder de vraag je stappenplan op, help jezelf om complexere vragen in stukjes op te breken (zie voorbeeld voor vraag 1 en 2 in het bestand met verwachte uitkomsten) 


Vragen:
1. Hoe luidt de langste filmtitel? 
2. Welke films behoren tot hetzelfde genre als de film 'Batman'? 
3. Welke films duren even lang als de film El Cid en behoren tot hetzelfde genre? 
4. Welke films hebben regisseurs die oorlogfilms gemaakt hebben, nog meer gemaakt? Geef het regisseurnummer, filmtitel en het genre en sorteer daarbij op regisseurnummer. 
5. Geef de titel en de speelduur van de langste Tekenfilm.
6. Geef het genre, de titel en de speelduur van alle films die binnen hun genre het langst zijn. Sorteer op genre en daarbinnen op titel. 
7. Welke films, gemaakt voor 1940, zijn net zo lang als de kortste Western die tussen 1950 en 1960 is gemaakt? 
8. Welke leden zijn het kortst lid? Geef naam en datum toetreding. 
9. Welke leden zijn het langst lid? Geef naam en datum toetreding. 
10. Welke films zijn door Don Siegel geregisseerd? Geef titel. 
11. Welke regisseur regisseerde de film Cliffhanger? 
12. Welke na-oorlogse regisseurs hebben nog nooit actiefilms gemaakt? Geef naam regisseur. 
13. Welke regisseurs hebben UITSLUITEND actiefilms gemaakt? Geef naam regisseur. 
14. Welke films hebben al meer opgebracht dan €125, door verhuur, als we aannemen dat de gemiddelde verhuurprijs €5, per keer bedraagt. 
15. Welke films zijn nog niet uitgebracht op band? 
16. Welke acteurs zijn ook regisseurs? Geef een alfabetische namenlijst. 
17. Welke acteurs, geboren na 1960, hebben nog nooit een rol gespeeld in een horrorfilm? Geef naam en geboortejaar. Sorteer het overzicht op geboortejaar en daarbinnen op naam. 
18. Welke leden huren op dit moment films van het genre Drama? 
19. Welke leden huren op dit moment UITSLUITEND films van het genre Drama? 
20. Wie zijn de jongste regisseurs? Geef naam en geboortejaar. 
21. Welke overleden regisseur is de oudste van allen? Geef de naam en de leeftijd. 
22. Onderzoek of alle banden met daarop een kopie van de film: This Is The Army verhuurd zijn. 
23. Geef de naam van de regisseur en de titel van zijn/haar films van het genre Horror. 
24. Geef de naam, het telefoonnummer en de titel van alle films die lid 752 op dit moment huurt. 
25. Welke acteurs spelen in welke films, die gehuurd worden door het lid T. Rexanus? Geef titel en namen acteurs. 
26. Geef de titel en de rolnaam van alle films waarin acteur Michael Douglas gespeeld heeft. 
27. Welke acteurs, die meespeelden in de film The Sting, zijn overleden? Geef naam acteur en zijn leeftijd. 
28. Wie speelde in welke film de rol van Buffalo Bill? 
29. In welke, door hen zelf geregisseerde films, spelen de regisseurs een rol(letje)? Geef naam regisseur, de titel van de film en de rolnaam die zij in hun film speelde. 
30. Wat is de langste film, uitgebracht door Warner Bros, waarin Sylvester Stallone een rol heeft?
31. Welke thrillers worden slechts op 1 band uitgebracht? Sorteer het overzicht op titel. 
32. Van welke regisseurs zijn drie of meer films bekend? 

## Materialen:
- [Database](assets/file/DATABASE_FILM.zip)
- [Verwachte uitkomsten](assets/file/films3.pdf)