---
title: Cohortanalyse gebruiken om het gedrag van de klant te begrijpen
description: Om klantenervaring en opbrengst te verbeteren, moeten de ondernemingen klantengedrag begrijpen. Cohortanalyse kan helpen om betrokkenheid en behoud te begrijpen, wat leidt tot acties zoals het verbeteren van het creëren van rekeningen en het creëren van campagnes voor high-volume maanden.
feature: Cohort Analysis
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13213
thumbnail: KT-13213.jpeg
source-git-commit: 5988e9d68f0c2200168da56373259bdf9f4f901b
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---


# Cohortanalyse gebruiken om het gedrag van de klant te begrijpen

Om klantenervaring en opbrengst te verbeteren, moeten de ondernemingen klantengedrag begrijpen. Cohortanalyse kan helpen om betrokkenheid en behoud te begrijpen, wat leidt tot acties zoals het verbeteren van het creëren van rekeningen en het creëren van campagnes voor high-volume maanden.

Het analyseren van digitale prestaties is essentieel om te begrijpen hoe de klanten met een zaken in wisselwerking staan en welke acties kunnen worden genomen om hun ervaring te verbeteren. In dit blogbericht bekijken we hoe we cohortanalyse kunnen gebruiken om het gedrag van klanten beter te begrijpen.

## Deel 1: Digitale prestaties vergelijken tussen eerste en Return-bezoeken

### Werkgebied instellen

Een klant is op zoek naar een beter begrip van de digitale prestaties in de afgelopen twee jaar en overweegt een programma voor loyaliteit te ontwikkelen om de digitale prestaties te stimuleren. Om te beginnen kunnen we de huidige sitemix tussen nieuwe en herhaalde gebruikers bekijken om te begrijpen hoe de twee groepen bezoekers zich vandaag gedragen.

Huidige digitale prestaties

1. In 2022 was 62% van de bestellingen afkomstig van eerste bezoeken, tegen 38% van bestellingen van terugkeerbezoeken (onder voorbehoud van cookies, meerdere apparaten).
1. Voor beide, 11,6% versus 11,4%, zetten de eerste bezoeken een iets hogere conversie uit dan terugkeerbezoeken.
1. Vergeleken met 2021 daalden de omrekeningskoersen voor beide segmenten.

![Bezoektabel](assets/visits-table.png)

## Deel 2: Cohortanalyse - Bezoek Eetbare Rangschikkingen Wereldwijde Pro

De volgende vraag die moet worden beantwoord, is: Hoeveel bezoekers keren in 2022 elke maand terug naar de site?

### Kennismaken met Cohortanalyse

Cohortanalyse is een handig hulpmiddel om te begrijpen hoe cohorten in de loop der tijd met een merk omgaan. Om te beginnen hebben we bepaald welke vragen moesten worden beantwoord:

1. Wat is in een bepaald jaar de gemiddelde aanhoudperiode per maand?
1. Hoeveel bezoekers van de site retourneren per maand in een bepaald jaar?
1. Wat is de invloed van logins op het behoud?
1. Zijn er specifieke producten die een hogere retentie hebben veroorzaakt?

Procedure voor het instellen van de cohortabel

1. Datumbereik instellen op Jan tot december 2022
1. **Opnamecriteria:** Bezoeken
1. **Retourcriteria:** Bezoeken
1. **Korreligheid:** Maand
1. **Instellingen:** Bij rolberekening \*\*Hiermee kunt u de retentie berekenen op basis van de vorige kolom, niet op basis van de opgenomen kolom. Dit betekent dus dat een gebruiker in elk van de maanden is opgenomen\*\*
1. **Segmenten:** u kunt specifieke segmenten selecteren om deze analyse verder te sturen
   1. Specifieke landingspagina&#39;s
   1. Apparaattype
   1. Marketingkanalen
   1. enz.

### De resultaten interpreteren

**In 2022:**

1) Maanden met de hoogste aanhoudingspercentages +1 maand omvatten januari, april en november
1) Maanden met de meeste volumes zijn februari en mei
1) Er zijn ongeveer 1.000 bezoekers die elke maand naar de site terugkeren

![2022-retentietabel](assets/2022-retention-table.png)

**In 2021:**

1) Maanden met de hoogste aanhoudingspercentages +1 maand omvatten april, januari en maart
1) Maanden met de meeste volumes zijn februari en mei

![2021 Bewaartabel](assets/2021-retention-table.png)

**Actiepunten:**

Maak een segment op basis van ~1.000 Bezoekers en leer er meer over:

- Waar bevinden ze zich?
- Welke producten kopen ze het hele jaar door?
- Van welke winkels kopen ze?

Belangrijkste maanden benadrukken de mogelijkheid om de schijf vast te houden op basis van het volume:

- Zijn er specifieke tactieken die extra kleverigheid in februari en mei kunnen drijven om van volume te profiteren?

Herhaal de analyse voor bestellingen die Herhalingsaankopen moeten begrijpen

- Zijn de hoogste bewaarpercentages van +1 maand voor dezelfde maanden?
- Zijn de hoogste maanden van Bezoekingen hetzelfde voor bestellingen?

## Deel 3: Twee metriek toevoegen aan opnamecriteria

### Inzicht in het effect van aanmelding

Aangezien deze cliënt de waarde van een Loyalty- programma probeert te begrijpen, omvatte de volgende stap in de analyse het toevoegen van in de Login succesgebeurtenis als metrisch van de Opname aan de Cohort.

Voorbehoud: De analyse van de cohort kan niet voor berekende metriek (zoals het Tarief van de Omzetting) of niet-geheelmetriek (zoals Opbrengst) worden gebruikt. Alleen metriek die in segmenten kan worden gebruikt, kan in Cohortanalyse worden gebruikt en kan alleen met >1 tegelijk worden verhoogd.

Is de site waarschijnlijker gebruikers te behouden die zich aanmelden?

Wat zou het effect zijn als wij meer gebruikers aan login konden krijgen? Is dat een kleverere ervaring?

### De tabel Cohort instellen

1. **Datumbereik instellen:** tot januari tot en met december 2022
1. **Opnamecriteria:** Bezoek + gebeurtenis met succes aanmelden
1. **Retourcriteria:** Bezoeken
1. **Korreligheid:** Maand
1. **Instellingen:** Bij rolberekening \*\*Hiermee kunt u de retentie berekenen op basis van de vorige kolom, niet op basis van de opgenomen kolom. Dit betekent dus dat een gebruiker in elk van de maanden is opgenomen\*\*

### De resultaten interpreteren

**In 2022:**

1) Maanden met de hoogste aanhoudingspercentages +1 maand omvatten januari, april en november (dezelfde maanden als de eerste cohortingtabel)
1) Maanden met het grootste volume zijn februari en mei en december
1) Er zijn ~2500 bezoekers die elke maand \*\*meer dan twee keer\*\* retourneren

**Actiepunten:**

Bekijk de gebruikerservaring van de site om gebruikers te vragen een account te maken tijdens de afhandeling

![Tabel 4](assets/cohort-table-4.png)

## Deel 4: Aangepaste Dimension-cohort

Aangepaste Dimension-kleur: Maak cohorten op basis van de geselecteerde dimensie in plaats van op tijd gebaseerde cohorts (standaard). Veel klanten willen hun cohorten met iets anders dan tijd analyseren en de nieuwe functie van de Cohort van de Dimension van de Douane biedt u de flexibiliteit om cohorten te bouwen die op afmetingen van hun kiezen worden gebaseerd. Met afmetingen zoals marketingkanaal, campagne, product, pagina, regio of een andere dimensie in Adobe Analytics kunt u zien hoe de retentie verandert op basis van de verschillende waarden van deze dimensies. De

Bij de definitie van het aangepaste Dimension Cohort-segment wordt de dimensie-item alleen toegepast als onderdeel van de opnemingsperiode, niet als onderdeel van de terugkeerdefinitie.

Nadat u de optie Aangepaste Dimension-kleur hebt gekozen, kunt u de gewenste afmeting naar de neerzetzone slepen. Dit staat u toe om gelijkaardige afmetingspunten over de zelfde tijdspanne te vergelijken. U kunt bijvoorbeeld de prestaties van steden naast elkaar vergelijken

zijde, producten, campagnes, enz. Het zal uw hoogste 14 afmetingspunten terugkeren. U kunt echter een filter gebruiken (dit filter openen door de muis boven de dimensie te houden die is aangesleept) om alleen gewenste dimensie-items weer te geven. Een aangepaste Dimension-cohort kan niet worden gebruikt met de functie Latentietabel.

### Welke Producten drijven de sitepijkheid?

In de tabel Aangepaste Dimension-cohort worden producten gemarkeerd die een hogere retentiesnelheid hebben dan gemiddeld.  Met deze tabel kunt u uw beste producten identificeren om interne en externe marketingcampagnes met producten die de aandacht verdienen, te stimuleren.

**In feb:** 3 producten met hoge retentiepercentages

1) Product 1
1) Product 2
1) Product 3

**In maart:**

1) Product 1
1) Product 2
1) Product 3 — levert vaak hogere retentie op dan gemiddeld retentie.

![Tabel 5](assets/cohort-table-5.png)

## Conclusie

Cohortanalyse en Custom Dimension Cohort zijn krachtige tools voor een beter begrip van het gedrag van klanten en voor het verbeteren van de digitale prestaties. Door behoudsaantallen, login tarieven, en het effect van specifieke producten te analyseren, kunnen de ondernemingen gegevens-gedreven besluiten nemen om de klantenervaring te verbeteren en de groei te drijven.

## Auteur

Dit document is geschreven door:

![Jennifer Yacenda](assets/jennifer-yacenda.png)

**Jennifer Yacenda**, Senior Director bij Marriott

Adobe Analytics Champion