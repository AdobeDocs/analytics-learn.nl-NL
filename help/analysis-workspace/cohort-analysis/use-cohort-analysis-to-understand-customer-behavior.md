---
title: Cohortanalyse gebruiken om het gedrag van de klant te begrijpen
description: Om klantenervaring en opbrengst te verbeteren, moeten de ondernemingen klantengedrag begrijpen. Cohortanalyse kan helpen om betrokkenheid en behoud te begrijpen, wat leidt tot acties zoals het verbeteren van het creëren van rekeningen en het creëren van campagnes voor high-volume maanden.
feature: Visualizations
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13213
thumbnail: KT-13213.jpeg
exl-id: 23dd43c5-47e4-46c7-88ee-66c7f62ca9cf
source-git-commit: d24bab984f57dbf197c5f6fb39d0a82e6fcf2ad2
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 0%

---

# Cohortanalyse gebruiken om het gedrag van de klant te begrijpen

Om klantenervaring en opbrengst te verbeteren, moeten de ondernemingen klantengedrag begrijpen. Cohortanalyse kan helpen om betrokkenheid en behoud te begrijpen, wat leidt tot acties zoals het verbeteren van het creëren van rekeningen en het creëren van campagnes voor high-volume maanden.

Het analyseren van digitale prestaties is essentieel om te begrijpen hoe de klanten met een zaken in wisselwerking staan en welke acties kunnen worden genomen om hun ervaring te verbeteren. In dit blogbericht bekijken we hoe we cohortanalyse kunnen gebruiken om het gedrag van klanten beter te begrijpen.

## Deel 1: Digitale prestaties vergelijken tussen eerste en Return Visits

### Het werkgebied instellen

Een klant is op zoek naar een beter begrip van de digitale prestaties in de afgelopen twee jaar en overweegt een loyaliteitsprogramma te ontwikkelen om de digitale prestaties te stimuleren. Om te beginnen kunnen we de huidige sitemix tussen nieuwe en herhaalde gebruikers bekijken om te begrijpen hoe de twee groepen bezoekers zich vandaag gedragen.

Huidige digitale prestaties

1. In 2022 was 62% van de bestellingen afkomstig van eerste bezoeken, tegen 38% van bestellingen van terugkeerbezoeken (onder voorbehoud van cookies, meerdere apparaten).
1. Voor beide, 11,6% versus 11,4%, zetten de eerste bezoeken een iets hogere conversie uit dan terugkeerbezoeken.
1. Vergeleken met 2021 daalden de omrekeningskoersen voor beide segmenten.

![ lijst van Bezoeken ](assets/cohort1.png)

## Deel 2: Cohortanalyse - Bezoek Eetbare Regelingen Wereldwijd Product

De volgende vraag die moet worden beantwoord, is: Wat is het aantal bezoekers dat in 2022 elke maand naar de site terugkeert om de kleverigheid van het digitale kanaal en de mogelijkheid om herhaalde kopers te besturen?

### Kennismaken met Cohortanalyse

Cohortanalyse is een handig hulpmiddel om te begrijpen hoe cohorten in de loop der tijd met een merk omgaan. Om te beginnen hebben we bepaald welke vragen moesten worden beantwoord:

1. Wat is in een bepaald jaar de gemiddelde aanhoudperiode per maand?
1. Hoeveel bezoekers van de site retourneren per maand in een bepaald jaar?
1. Wat is de invloed van logins op het behoud?
1. Zijn er specifieke producten die een hogere retentie hebben veroorzaakt?

Procedure voor het instellen van de cohortabel

1. Datumbereik instellen op Jan tot december 2022
1. **criteria van de Opname:** bezoeken
1. **criteria van de Terugkeer:** bezoeken
1. **Korreligheid:** Maand
1. **Montages:** Rolling Berekening
\*\*Hiermee kunt u de retentie berekenen op basis van de vorige kolom, niet op basis van de opgenomen kolom. Dit betekent dus dat een gebruiker in elk van de maanden is opgenomen\*\*
1. **Segmenten:** u kunt specifieke segmenten selecteren om deze analyse verder te drijven
   1. Specifieke landingspagina&#39;s
   1. Apparaattype
   1. Marketingkanalen
   1. enz.

### De resultaten interpreteren

**in 2022:**

1) Maanden met de hoogste aanhoudingspercentages +1 maand omvatten januari, april en november
1) Maanden met de meeste volumes zijn februari en mei
1) Er zijn ongeveer 1.000 bezoekers die elke maand naar de site terugkeren

![ 2022 bewaarlijst ](assets/cohort2.png)

**in 2021:**

1) Maanden met de hoogste aanhoudingspercentages +1 maand omvatten april, januari en maart
1) Maanden met de meeste volumes zijn februari en mei

![ 2021 lijst van het Behoud ](assets/cohort3.png)

**punten van de Actie:**

Maak een segment op basis van ~1.000 Bezoekers en leer er meer over:

- Waar bevinden ze zich?
- Welke producten kopen ze het hele jaar door?
- Van welke winkels kopen ze?

Belangrijkste maanden benadrukken de mogelijkheid om de schijf vast te houden op basis van het volume:

- Zijn er specifieke tactieken die extra kleverigheid in februari en mei kunnen drijven om van volume te profiteren?

Herhaal de analyse voor bestellingen die Herhalingsaankopen moeten begrijpen

- Zijn de hoogste bewaarpercentages van +1 maand voor dezelfde maanden?
- Zijn de hoogste maanden van Bezoekingen hetzelfde voor bestellingen?

## Deel 3: Twee meetwaarden toevoegen aan inclusiecriteria

### Inzicht in het effect van aanmelding

Aangezien deze cliënt de waarde van een Loyalty- programma probeert te begrijpen, omvatte de volgende stap in de analyse het toevoegen van in de Login succesgebeurtenis als metrisch van de Opname aan de Cohort.

Voorzichtigheid: de analyse van de cohort kan niet voor berekende metriek (zoals het Tarief van de Omzetting) of niet-geheelmetriek (zoals Opbrengst) worden gebruikt. Alleen metriek die in segmenten kan worden gebruikt, kan in Cohortanalyse worden gebruikt en kan alleen met >1 tegelijk worden verhoogd.

Is de site waarschijnlijker gebruikers te behouden die zich aanmelden?

Wat zou het effect zijn als wij meer gebruikers aan login konden krijgen? Is dat een kleverere ervaring?

### De tabel Cohort instellen

1. **vastgestelde Waaier van de Datum:** aan Jan aan Dec 2022
1. **criteria van de Opname:** bezoeken + Login succesgebeurtenis
1. **criteria van de Terugkeer:** bezoeken
1. **Korreligheid:** Maand
1. **Montages:** Rolling Berekening
\*\*Hiermee kunt u de retentie berekenen op basis van de vorige kolom, niet op basis van de opgenomen kolom. Dit betekent dus dat een gebruiker in elk van de maanden is opgenomen\*\*

### De resultaten interpreteren

**in 2022:**

1) Maanden met de hoogste aanhoudingspercentages +1 maand omvatten januari, april en november (dezelfde maanden als de eerste cohortingtabel)
1) Maanden met het grootste volume zijn februari en mei en december
1) Er zijn ~2500 bezoekers die elke maand \*\*meer dan twee keer\*\* retourneren

**punten van de Actie:**

Bekijk de gebruikerservaring van de site om gebruikers te vragen een account te maken tijdens de afhandeling

![ Lijst 4 van de Cohort ](assets/cohort4.png)

## Deel 4: Aangepaste Dimension-cohort

Aangepaste Dimension-cohort: maak cohorten op basis van de geselecteerde dimensie in plaats van op tijd gebaseerde cohorts (standaard). Veel klanten willen hun cohorten met iets anders dan tijd analyseren en de nieuwe functie van de Cohort van de Douane van Dimension biedt u de flexibiliteit om cohorten te bouwen die op afmetingen van hun kiezen worden gebaseerd. Met afmetingen zoals marketingkanaal, campagne, product, pagina, regio of een andere dimensie in Adobe Analytics kunt u zien hoe de retentie verandert op basis van de verschillende waarden van deze dimensies. De

Bij de definitie van het aangepaste Dimension Cohort-segment wordt de dimensie-item alleen toegepast als onderdeel van de opnemingsperiode, niet als onderdeel van de terugkeerdefinitie.

Nadat u de optie Aangepaste Dimension-kleur hebt gekozen, kunt u de gewenste dimensie naar de neerzetzone slepen. Dit staat u toe om gelijkaardige afmetingspunten over de zelfde tijdspanne te vergelijken. U kunt bijvoorbeeld de prestaties van steden naast elkaar vergelijken

zijde, producten, campagnes, enz. Het zal uw hoogste 14 afmetingspunten terugkeren. U kunt echter een filter gebruiken (dit filter openen door de muis boven de dimensie te houden die is aangesleept) om alleen gewenste dimensie-items weer te geven. Een aangepaste Dimension-code kan niet worden gebruikt met de functie Latentietabel.

### Welke Producten drijven de sitepijkheid?

In de aangepaste Dimension Cohort-tabel worden producten gemarkeerd die een hogere retentiesnelheid hebben dan gemiddeld.  Met deze tabel kunt u uw beste producten identificeren om interne en externe marketingcampagnes met producten die de aandacht verdienen, te stimuleren.

**in Feb:** 3 producten stand-out met hogere behoudtarieven

1) Product 1
1) Product 2
1) Product 3

**in Mar:**

1) Product 1
1) Product 2
1) Product 3 — levert vaak hogere retentie op dan gemiddeld retentie.

![ Lijst van de Cohort 5 ](assets/cohort5.png)

## Conclusie

Cohortanalyse en Custom Dimension Cohort zijn krachtige tools voor een beter begrip van het gedrag van klanten en voor het verbeteren van de digitale prestaties. Door behoudsaantallen, login tarieven, en het effect van specifieke producten te analyseren, kunnen de ondernemingen gegevens-gedreven besluiten nemen om de klantenervaring te verbeteren en de groei te drijven.

## Auteur

Dit document is geschreven door:

![ Jennifer Yacenda ](assets/jennifer-yacenda.png)

**Jennifer Yacenda**, Hogere Directeur bij Marriott

Adobe Analytics Champion
