---
title: IQ voor reizen begrijpen en gebruiken - Apparaatanalyse
description: Wanneer gebruikers met uw merk communiceren, doen zij dat op vele manieren en op meerdere apparaten. Apparaatanalyse kan worden geïntegreerd met de Adobe Experience Platform Identity Service om te bepalen hoe apparaten aan personen worden toegewezen. Vervolgens wordt deze informatie gebruikt om een apparaatweergave van gebruikersgedrag te maken. Dit leidt ertoe dat we in staat zijn om analyses uit te voeren op mensen, niet op apparaten.
feature: cda
topics: null
audience: all
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
translation-type: tm+mt
source-git-commit: 24ad92b0ccdf1112e3ed4a0968cd47db757598c3
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 3%

---


# Werken met en begrijpen [!DNL Journey IQ] - Apparaatanalyse

Wanneer gebruikers met uw merk communiceren, doen zij dat op vele manieren en op meerdere apparaten. Apparaatanalyse kan worden geïntegreerd met de functie [!DNL Adobe Experience Platform Identity Service] om te bepalen hoe apparaten worden toegewezen aan personen. Vervolgens wordt deze informatie gebruikt om een apparaatweergave van gebruikersgedrag te maken. Dit leidt ertoe dat we in staat zijn om analyses uit te voeren op mensen, niet op apparaten.

## Overzicht van apparaatanalyse

### Ik ben niet mijn apparaten

Wanneer gebruikers met uw merk werken, doen ze dat op verschillende manieren en op meerdere &quot;oppervlakken&quot; of &quot;apparaten&quot;. Ze kunnen een webbrowser gebruiken op een pc of mobiel apparaat, of ze kunnen een mobiele app gebruiken. In traditionele digitale analyses, die opgroeiden in gegevensverzameling gebaseerd op cookies, wordt elk van deze oppervlakken weergegeven als een unieke &quot;bezoeker&quot;. Dit betekent dat elk van uw menselijke gebruikers wordt vertegenwoordigd als veelvoudige unieke bezoekers.

Hier is een voorbeeld. Stel dat Isabelle op de volgende manier met uw merk communiceert:

*Isabelle is drie bezoekers*![Traditional Analytics Journey](assets/cda-isabelle-journey-traditional-analytics.png)

Met behulp van traditionele analyses wordt de reis van Isabelle in drie stukken gebroken. Zij wordt vertegenwoordigd als drie unieke bezoekers, die elk een verschillend apparaat gebruikten om geïsoleerde taken uit te voeren. Wat nodig is, is een verenigde, cross-device weergave van de interacties van Isabelle. [!DNL Journey IQ: Cross-Device Analytics] biedt deze weergave.

*Isabelle is één persoon*![Reizigersreis voor apparaatanalyse](assets/cda-isabelle-journey-cross-device-analytics.png)

### Een apparaatweergave biedt betere analysemogelijkheden

Een persoonlijk-centrische, cross-device weergave van het gedrag van Isabelle kan een belangrijk verschil maken voor uw analyse. De traditionele aanpak op bezoekersbasis geeft u bijvoorbeeld niet het volledige beeld van de doeltreffendheid van marketingkanalen. Laten we eens kijken naar de reis van Isabelle, waarbij we ons richten op welk kanaal krediet ontvangt voor haar productweergave en voor haar aankoop. We gebruiken [!UICONTROL last-touch] attributie voor eenvoud, maar hetzelfde probleem doet zich voor met elk attributiemodel wanneer u het gedrag van Isabelle opsplitst in verschillende bezoekers. Het gebruik van de traditionele, op bezoekers gebaseerde kijk op de wereld geeft zeer verschillende, zelfs misleidende resultaten:

*Traditionele analyse versus attributie van*![kanaal voor apparaatanalyse](assets/channel-attribution.png)

U ziet dat het e-mailkanaal in de apparaatweergave krediet ontvangt voor zowel de productweergave als de aankoop, die de werkelijke beleving van Isabelle nauwkeuriger weergeeft.

Lees meer over:

* Hoe [!DNL Cross-Device Analytics] werkt
* Vereisten voor [!DNL Cross-Device Analytics]
* Apparaatgegevens interpreteren
* Apparaatgegevens analyseren in Analysis Workspace

## Hoe [!DNL Cross-Device Analytics] werkt

[!DNL Journey IQ: Cross-Device Analytics (CDA)] integreert met de [!DNL Adobe Experience Platform Identity Service], die of de [[!DNL Co-op Grafiek]](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) gebruiken of [!DNL Private Graph] identificeren hoe de apparaten aan mensen in kaart brengen. Vervolgens wordt deze informatie gebruikt om een apparaatweergave van gebruikersgedrag te maken. CDA bevat ongeëvenaarde mogelijkheden en tools om uw onderneming te helpen het gebruik van meerdere apparaten en de ervaring van klanten op deze apparaten te begrijpen in hun interactie met uw merk. Het bevindt zich als een laag onder Analysis Workspace om diepgaand inzicht te verschaffen in persoonlijke publieksanalyse en attributie tussen apparaten, segmentatie en reisanalyse met krachtige instrumenten zoals [!UICONTROL Fallout], [!DNL Flow], [!DNL Cohort], [!DNL Segment IQ] en [!DNL Attribution IQ].

### De [!DNL Cross-Device Virtual Report Suite]

CDA wordt aangeboden door middel van een speciaal soort kruisapparaat [[!UICONTROL Virtual Report Suite]](https://docs.adobe.com/content/help/en/analytics/components/virtual-report-suites/vrs-about.html). Dit staat u toe om de originele op apparaat-gebaseerde rapportreeks te blijven gebruiken aangezien u dwars-apparatenanalyses in uw organisatie introduceert. Het instellen van een CDA VRS is eenvoudig.

In stap één van VRS bouwer, kies [!UICONTROL report suite] die door Adobe als CDA-Toegelaten is gevormd:

*Kies een CDA-Toegelaten basis (bron)[!UICONTROL report suite]*![[!UICONTROL Virtual Report Suite] Stap Één](assets/cda-vrs-step-one.png)

Schakel vervolgens in [!UICONTROL Report Time Processing] en schakel [!UICONTROL cross-device stitching]:

*Schakel[!UICONTROL report-time processing]en[!UICONTROL cross-device stitching]*![[!UICONTROL Virtual Report Suite] stap twee in](assets/cda-vrs-step-two.png)

Voltooi de VRS-instelling en sla deze op. Het CDA VRS wordt in Analysis Workspace weergegeven met een speciaal pictogram ernaast, zoals hieronder wordt getoond:

*Selecteer CDA VRS in Analysis Workspace*![[!UICONTROL Virtual Report Suite] Stap drie](assets/cda-vrs-step-three.png)

>[!TIP]
>
>U kunt net zoveel CDA maken [!UICONTROL virtual report suites] als u wilt boven op de basis voor CDA [!UICONTROL report suite].

### Historie herstellen

Soms duurt het even voordat uw gebruikers zich aanmelden [!DNL Co-op Graph] of [!DNL Private Graph] ze identificeren en hun apparaten in kaart brengen. CDA gebruikt een terugblik-achtervenster van 30 dagen, die het toestaat om een eerder niet geïdentificeerde bezoeker als persoon tot 30 dagen in het verleden opnieuw te verklaren.

Hoe helpt dit? Herinnert de gebruikersreis van Isabelle uit de bovenstaande discussie:

![[!DNL Cross-Device Analytics] Reis](assets/cda-isabelle-journey-cross-device-analytics.png)

Het is mogelijk dat Isabelle pas inlogde voordat hij de aankoop maakte en dat de apparatuur van Isabelle pas enige tijd na haar aankoop in kaart werd gebracht [!DNL Co-op Graph] of [!DNL Private Graph] niet in kaart werd gebracht. Maar de terugblik van de CDA van 30 dagen staat CDA toe om het verleden van Isabelle op een persoonniveau te herbevestigen, die u van het dwars-apparaat mening van haar reis voorzien die u nodig hebt.

>[!NOTE]
>
>Aangezien de geschiedenis kan worden aangepast, betekent dit dat uw gegevens in de loop der tijd kunnen veranderen in een CDA-Toegelaten [!UICONTROL virtual report suite]. Houd dit in mening aangezien u inzichten van een op CDA-Gebaseerde analyse deelt.

## Vereisten voor [!UICONTROL Cross-Device Analytics]

CDA is inbegrepen bij [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html). Vanaf september 2019 kunnen [!DNL Analytics Ultimate] klanten die aan de onderstaande voorwaarden voldoen, gebruikmaken van CDA. De voorwaarden voor CDA zijn als volgt:

* Uw bedrijf moet lid zijn van de [!DNL Adobe Experience Platform Identity Service] [!DNL Co-op Grafiek] [of een](https://docs.adobe.com/content/help/en/device-co-op/using/home.html)[!DNL Adobe Experience Platform Identity Service Private Graph].
* U moet alles implementeren wat vereist is voor [!DNL Co-op Graph] of [!DNL Private Graph] inclusief [Experience Cloud-id (ECID)](https://docs.adobe.com/content/help/nl-NL/id-service/using/home.html) en id-synchronisatie met de grafiek. Naast technische vereisten [!DNL Co-op Graph] heeft de ECB ook andere wettelijke en contractuele vereisten.
* Het is momenteel niet mogelijk om twee IMS-organen met één enkele IMS-instantie te gebruiken [!DNL Private Graph], dus u moet de IMS-org standaardiseren. In sommige gevallen is het mogelijk dat een klant met meerdere IMS-organen de IMS-code [!DNL Co-op Graph] in combinatie met CDA gebruikt.
* De CDA [!DNL Co-op graph] en [!DNL Private Graph]en bepaalde componenten daarvan worden gehost in [!DNL Microsoft Azure]. Dit betekent dat [!DNL Analytics] gegevens op en neer worden gekopieerd tussen Adobe verwerkingscentrum en Adobe aanwezigheid in [!DNL Microsoft Azure]. Sommige [!DNL Analytics] gegevens worden opgeslagen in [!DNL Azure]. Uw bedrijf moet met deze regeling instemmen.
* CDA vereist een &quot;cross-device&quot; [!UICONTROL report suite]. Dat wil zeggen dat de gegevens die [!UICONTROL report suite] u voor CDA gebruikt, gegevens moeten bevatten van verschillende apparaattypen of &#39;oppervlakken&#39;, zoals het bureaublad, het mobiele web en de mobiele app. Vanaf september 2019 [!UICONTROL report suite] moet het volume van de servervraag voor dit 100MM servervraag/dag of minder zijn. (De grenzen van het het vraagvolume van de Server zullen in de komende maanden stijgen.)
* Vanaf september 2019 zijn de [!DNL Co-op Graph] en [!DNL Private Graph] beschikbaar in Noord-Amerika. Het schema voor de aanwezigheid van grafieken in EMEA en APAC zal in de toekomst worden bekendgemaakt. Als u in die regio&#39;s bent, moedigen wij u aan om nu al naar deze voorwaarden te beginnen kijken zodat u klaar bent om te gaan wanneer de grafiek beschikbaar wordt.

## Apparaatgegevens interpreteren

### Personen zonder bezoekers

Binnen de CDA [!UICONTROL Virtual Report Suite], zult u een paar veranderingen zien. De [!UICONTROL Unique Visitors] metrische waarde wordt bijvoorbeeld vervangen door twee nieuwe metriek: [!UICONTROL People] en [!UICONTROL Unique Devices]. Deze nieuwe meetgegevens geven u veel beter inzicht in de omvang van het publiek.

*Personen en unieke apparaten*![CDA [!UICONTROL People Metric]](assets/cda-people-metric.png)

In [[!UICONTROL Segment Builder]](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-build.html), is de [!UICONTROL Visitor] segmentcontainer vervangen door een [!UICONTROL Person] segmentcontainer. Met een CDA VRS kunt u apparaatsegmenten maken, zoals:

* Personen die meer dan één apparaat gebruiken
* Personen die hun reis op een mobiel apparaat beginnen en later op een desktopapparaat kopen
* Bezoek waarbij mensen meerdere apparaten gebruiken om een taak uit te voeren

*Individuele segmenten*![[!DNL Segment Builder][!UICONTROL Person] Container](assets/cda-segment-builder-person-container.png)

### Dimension Persistentie

Binnen een CDA VRS blijven dimensies, zoals [!DNL eVars] nu automatisch aanwezig op verschillende apparaten. Bijvoorbeeld, een [!DNL eVar] die als wordt gevormd:

* Toewijzing: Recentste (laatste)
* Vervalt na: Aanschaffen

zal nu automatisch van één apparaat aan een andere blijven tot de gebeurtenis van de Aankoop in brand wordt gestoken.

## Apparaatgegevens analyseren in Analysis Workspace

### Persoonlijke analyse van het publiek

Heb je je ooit afgevraagd hoeveel mensen met je merk communiceren? Wilt u weten hoeveel en welk type apparaten ze gebruiken? Hoe overlapt hun gebruik? Met behulp van een CDA VRS kunt u [Venn-diagrammen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/venn.html) en [histogrammen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/histogram.html)maken voor afzonderlijke apparaten.

*Persoonlijke publieksanalyse*![Venn en Histogram](assets/cda-venn-and-histogram.png)

### Cross-Device [!DNL Flow]

Met CDA en Analysis Workspace kunt u visualiseren hoe mensen in de loop der tijd van het ene apparaat naar het andere bewegen in de [[!DNL-stroomvisualisatie]](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/flow/flow.html). Je kunt zien waar ze op hun reis wegvallen, en waar ze verdergaan.

*[!DNL Flow]met CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Cross-Device [!DNL Fallout]

U kunt waarschijnlijk verschillende [[!DNL-evaluatievisualisaties]](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html) gebruiken om te analyseren hoe goed gebruikers dit in een bepaalde reeks stappen doen voordat het programma succesvol wordt. Wist u dat uw visie op deze opties beperkt [!DNL Fallout visualizations] is wanneer u traditionele apparaatgebaseerde analyses gebruikt? De volgende stap kan alleen worden uitgevoerd in dezelfde browser of app als de vorige stap als de volgende stap is geslaagd. In op apparaten gebaseerde analyses bent u blind voor mensen die de volgende stap met succes op een ander apparaat voltooien.

Geen zorgen, CDA heeft u bedekt. CDA creëert de apparaatweergave die [!DNL Fallout visualizations] veel nuttiger is. Het gaat er immers om of de persoon uiteindelijk ergens in zijn taak is geslaagd.

*[!DNL Fallout]met CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Omdat CDA een laag van dwars-apparatengegevens onder Analysis Workspace creeert, zal al uw analyse met een dwars-apparatenperspectief worden gearomatiseerd. Een krachtig voorbeeld is via [[!DNL-Attribution IQ]](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html). [!DNL Attribution IQ] in Analysis Workspace kunt u meerdere attributiemodellen naast elkaar vergelijken. Met behulp van deze mogelijkheid kunt u nu vergelijken hoe verschillende apparaten tot succes bijdragen.

Stel dat u wilt begrijpen hoe vaak een mobiele telefoon het eerste apparaat is dat wordt gebruikt in een interactie die uiteindelijk tot succes leidt. Dit staat voor de &#39;aanschafsnelheid&#39; van de mobiele telefoon. Met CDA + [!DNL Attribution IQ] kunt u deze analyse uitvoeren:

*[!DNL Attribution IQ]met CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

Raadpleeg de [[!DNL Cross-Device Analytics] Help-documentatie](https://docs.adobe.com/content/help/en/analytics/components/cda/cda-home.html)voor meer informatie.
