---
title: Eenvoudige stapels voor meer efficiëntie en zelfbediening - deel 1
description: Leer de belangrijkste uitdagingen waarmee analytische teams vandaag worden geconfronteerd, en onze aanbevelingen om hen te overwinnen die strategieën buiten Adobe Analytics UI gebruiken.
solution: Analytics
exl-id: 5d1077fd-d006-4a85-bf1c-54f6b2d31934
source-git-commit: 1181bfa62c5ec3d465aec5d1293e927c2c56f288
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---

# Adobe Analytics: Eenvoudige stapels voor meer efficiëntie en zelfbediening

**Deel 1: Buiten de gebruikersinterface**

In dit artikel worden de belangrijkste uitdagingen beschreven waarmee analytische teams vandaag worden geconfronteerd, en onze aanbevelingen om deze uit te schakelen met behulp van strategieën buiten de Adobe Analytics-interface.

## Belangrijkste uitdagingen voor analyseteams

Veel analytische teams hebben een onevenwichtige verdeling van het werk. In plaats van een combinatie van 80% analyse en 20% implementatie, zitten veel organisaties in het omgekeerde. Zij zien het grootste deel van hun inspanningen besteed aan het opzetten, rapporteren en verlenen van steun in tegenstelling tot het produceren van analyse die waardeinzichten drijft.

Analyseteams vinden hun productiviteit en efficiëntie om verschillende redenen afgenomen. Deze omvatten de voortdurend veranderende en evoluerende implementaties, het proberen om organisatorisch vertrouwen in de gegevens te handhaven, en het verminderen van de omzet van analisten. Door de omzet te reduceren vermijdt u het langdurige proces van training van nieuwe teamleden voor onvertrouwde, aangepaste implementatiehulpmiddelen.

Andere belangrijke uitdagingen waarmee analisten worden geconfronteerd:

* **Concurrentie:** De online en multi-kanaals detailhandel groeit concurrerender.
* **Klantenverwachtingen:** De ervaringen en marketingstrategieën van de klant worden complexer.
* **Gegevenswaarde:** De waarde van nauwkeurige gegevens en inzichten om een concurrerend voordeel te drijven groeit belangrijker.
* **Verwachtingen voor belanghebbenden:** Zakelijke partners, belanghebbenden en managers vragen steeds meer om gegevens voordat ze worden goedgekeurd.
* **Projectbeheer:** Het analytische team daalt in verzoeken om gegevensinzameling voor een nooit eindigende stroom van nieuwe eigenschappen uit te voeren, terwijl het produceren van nauwkeurige rapporten, het instappen van nieuwe analisten, en het ontdekken van het volgende nieuwe inzicht.

## Toetsen voor efficiëntie: Buiten de gebruikersinterface

1. Houd uw [Referentie voor ontwerp van oplossing](/help/implementation/implementation-basics/creating-and-maintaining-an-sdr.md) (SDR) up-to-date:

   * De SDR is de belangrijkste bron van waarheid voor de definitie en het beoogde gebruik van alle variabelen in de analytische implementatie.
   * SDR is de belangrijkste referentie waarmee gebruikers vertrouwd moeten zijn om waarde uit uw gebruikersinterface van Adobe Analytics te halen.
   * Het is belangrijk dat deze update en versioning worden uitgevoerd (u kunt een eenvoudige datumnotatie gebruiken).

1. Documentatie en governance inzake gegevensverzameling - technische specificaties:

   De tech-specificatie heeft een beperkter publiek dan de SDR, maar is net zo belangrijk, zo niet belangrijker, voor een volledig functionele implementatie. Een goede technische specificatie zou alle ontwikkeling, QA, en de middelen van het markeringsbeheer moeten zijn nodig om de oplossing uit te voeren. Zorg ervoor dat u zoveel documenten bijhoudt als nodig zijn voor unieke implementatiearchitecturen.

   **Technische specificaties**

   _Hoofdlettergebruik:_ Instructies die beschrijven hoe scripts voor gegevensverzameling moeten worden samengesteld

   _Primaire gebruikers:_ Ontwikkelaars

   _Andere opmerkingen:_

   * Zeer technisch document dat speciaal voor uw implementatieomgevingen is ontworpen
   * Nuttig voor zowel initiële implementatie als daaropvolgende onderhoud/referentie
   * Gerangschikt op oplossingstype (bijvoorbeeld, campagne het volgen, paginadetagegevens, etc.)
   * Primair document moet worden bijgewerkt en onderhouden naarmate SDR-wijzigingen worden aangebracht
   * Centrale opslagplaats
   * Gesynchroniseerde versienummers voor SDR en Tech Spec

1. Communiceer en documenteer de intentie van het oplossingsontwerp bij lancering:

   * Communiceren met de gebruiker in mening
   * Wanneer het lanceren of het verbeteren van gegevensinzameling, creeer eenvoudige samenvattingen die met belanghebbenden kunnen worden gedeeld
   * Verbeter behoorlijk veranderlijk gebruik uit de poort
   * Stuur een samenvattingsbericht voor de aankondiging van de lancering naar de belangrijkste belanghebbenden en analisten
   * Een bibliotheek maken die kan worden gebruikt ter ondersteuning van kantooruren, teamenablement-sessies of voor teamspecifieke instapsessies

1. Documentatie over gegevensverzameling, beheer en gegevenshygiëne - AHD:

   Het Analytics Health Dashboard (AHD) duikt diep in een _enkel_ rapportsuite en biedt een weergave van gegevens die in elke component (eVar, prop en gebeurtenis) zijn verzameld. Dit kan helpen wijzen op als het verzamelen van gegevens in een component is gestopt zodat kunt u actie ondernemen om de kwestie te verbeteren. U kunt dit dashboard op elk ogenblik in de toekomst voor om het even welk rapportreeks in werking stellen.

   Analytics Health Dashboard (AHD):

   _Hoofdlettergebruik:_ Momentopname van elke metrisch en afmeting die door één enkele rapportreeks wordt gevangen

   _Primaire gebruikers:_ toonaangevende analytische kmo&#39;s en/of Dev

   _Andere opmerkingen:_
   * Wordt geleverd via Excel met behulp van een aangepaste integratie van de API voor het rapporteren van Adobe
   * Gebruikers moeten API-toegang voor Analytics-webservices hebben
   * Er zijn opties voor halfautomatiseren

1. Win door de wereld van vakspecialisten (KMO&#39;s) uit te breiden:

   * KMO&#39;s oprichten binnen de verschillende teams in de organisatie
   * Bouw hun aanwezigheid door versies en wins te socialiseren
   * Gebruik regelmatig kantooruren om de trainers te helpen trainen en af te snijden op ad-hoctaken

Meer informatie over strategie en leiderschap bij de [Klant geslaagd](https://experienceleague.adobe.com/docs/customer-success/customer-success/overview.html) hub.