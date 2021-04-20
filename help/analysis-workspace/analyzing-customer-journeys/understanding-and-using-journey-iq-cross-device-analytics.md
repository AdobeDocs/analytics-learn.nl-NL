---
title: IQ voor reizen begrijpen en gebruiken - Apparaatanalyse
description: Wanneer gebruikers met uw merk communiceren, doen zij dat op vele manieren en op meerdere apparaten. Apparaatanalyse kan worden geïntegreerd met de Adobe Experience Platform Identity Service om te bepalen hoe apparaten aan personen worden toegewezen. Vervolgens wordt deze informatie gebruikt om een apparaatweergave van gebruikersgedrag te maken. Dit leidt ertoe dat we in staat zijn om analyses uit te voeren op mensen, niet op apparaten.
feature: CDA
topics: null
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
role: Business Practitioner
level: Intermediate
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 3%

---


# [!DNL Journey IQ] - Apparaatanalyse begrijpen en gebruiken

Wanneer gebruikers met uw merk communiceren, doen zij dat op vele manieren en op meerdere apparaten. Apparaatanalyse kan worden geïntegreerd met [!DNL Adobe Experience Platform Identity Service] om te bepalen hoe apparaten aan personen worden toegewezen. Vervolgens wordt deze informatie gebruikt om een apparaatweergave van gebruikersgedrag te maken. Dit leidt ertoe dat we in staat zijn om analyses uit te voeren op mensen, niet op apparaten.

## Overzicht van apparaatanalyse

### Ik ben niet mijn apparaten

Wanneer gebruikers met uw merk werken, doen ze dat op verschillende manieren en op meerdere &quot;oppervlakken&quot; of &quot;apparaten&quot;. Ze kunnen een webbrowser gebruiken op een pc of mobiel apparaat, of ze kunnen een mobiele app gebruiken. In traditionele digitale analyses, die opgroeiden in gegevensverzameling gebaseerd op cookies, wordt elk van deze oppervlakken weergegeven als een unieke &quot;bezoeker&quot;. Dit betekent dat elk van uw menselijke gebruikers wordt vertegenwoordigd als veelvoudige unieke bezoekers.

Hier is een voorbeeld. Stel dat Isabelle op de volgende manier met uw merk communiceert:

*Isabelle is drie*
![bezoekersTraditional Analytics Journey](assets/cda-isabelle-journey-traditional-analytics.png)

Met behulp van traditionele analyses wordt de reis van Isabelle in drie stukken gebroken. Zij wordt vertegenwoordigd als drie unieke bezoekers, die elk een verschillend apparaat gebruikten om geïsoleerde taken uit te voeren. Wat nodig is, is een verenigde, cross-device weergave van de interacties van Isabelle. [!DNL Journey IQ: Cross-Device Analytics] biedt deze weergave.

*Isabelle is één*
![persoonCross-Device Analytics Journey](assets/cda-isabelle-journey-cross-device-analytics.png)

### Een apparaatweergave biedt betere analysemogelijkheden

Een persoonlijk-centrische, cross-device weergave van het gedrag van Isabelle kan een belangrijk verschil maken voor uw analyse. De traditionele aanpak op bezoekersbasis geeft u bijvoorbeeld niet het volledige beeld van de doeltreffendheid van marketingkanalen. Laten we eens kijken naar de reis van Isabelle, waarbij we ons richten op welk kanaal krediet ontvangt voor haar productweergave en voor haar aankoop. We gebruiken [!UICONTROL last-touch] attributie voor eenvoud, maar hetzelfde probleem doet zich voor met elk attributiemodel wanneer u het gedrag van Isabelle opsplitst in verschillende bezoekers. Het gebruik van de traditionele, op bezoekers gebaseerde kijk op de wereld geeft zeer verschillende, zelfs misleidende resultaten:

*Traditionele analyse vs.*
![attributie Cross-Device Analyticschannel](assets/channel-attribution.png)

U ziet dat het e-mailkanaal in de apparaatweergave krediet ontvangt voor zowel de productweergave als de aankoop, die de werkelijke beleving van Isabelle nauwkeuriger weergeeft.

Lees meer over:

* Hoe werkt [!DNL Cross-Device Analytics]
* Vereisten voor [!DNL Cross-Device Analytics]
* Apparaatgegevens interpreteren
* Apparaatgegevens analyseren in Analysis Workspace

## Hoe werkt [!DNL Cross-Device Analytics]

[!DNL Journey IQ: Cross-Device Analytics (CDA)] integreert met  [!DNL Adobe Experience Platform Identity Service], gebruikend of de  [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) of  [!DNL Private Graph] om te identificeren hoe de apparaten aan mensen in kaart brengen. Vervolgens wordt deze informatie gebruikt om een apparaatweergave van gebruikersgedrag te maken. CDA bevat ongeëvenaarde mogelijkheden en tools om uw onderneming te helpen het gebruik van meerdere apparaten en de ervaring van klanten op deze apparaten te begrijpen in hun interactie met uw merk. Het bevindt zich als een laag onder Analysis Workspace om diepgaand inzicht te verschaffen in persoonlijke publieksanalyse en attributie, segmentatie en reisanalyse op verschillende apparaten met behulp van krachtige tools zoals [!UICONTROL Fallout], [!DNL Flow], [!DNL Cohort], [!DNL Segment IQ] en [!DNL Attribution IQ].

### De [!DNL Cross-Device Virtual Report Suite]

CDA wordt voorgesteld door een speciaal soort cross-device [[!UICONTROL Virtual Report Suite]](https://docs.adobe.com/content/help/en/analytics/components/virtual-report-suites/vrs-about.html). Dit staat u toe om de originele op apparaat-gebaseerde rapportreeks te blijven gebruiken aangezien u dwars-apparatenanalyses in uw organisatie introduceert. Het instellen van een CDA VRS is eenvoudig.

In stap één van VRS bouwer, kies [!UICONTROL report suite] die door Adobe als CDA-Toegelaten is gevormd:

*Kies een CDA-Toegelaten basis (bron)[!UICONTROL report suite]*
![[!UICONTROL Virtual Report Suite] Stap Één](assets/cda-vrs-step-one.png)

Schakel vervolgens [!UICONTROL Report Time Processing] in en schakel [!UICONTROL cross-device stitching] in:

*Inschakelen  [!UICONTROL report-time processing] en[!UICONTROL cross-device stitching]*
![[!UICONTROL Virtual Report Suite] Stap twee](assets/cda-vrs-step-two.png)

Voltooi de VRS-instelling en sla deze op. Het CDA VRS wordt in Analysis Workspace weergegeven met een speciaal pictogram ernaast, zoals hieronder wordt getoond:

*Selecteer CDA VRS in Analyse*
![[!UICONTROL Virtual Report Suite] WorkspaceStep Drie](assets/cda-vrs-step-three.png)

>[!TIP]
>
>U kunt zo veel CDA [!UICONTROL virtual report suites] tot stand brengen aangezien u op de CDA-Toegelaten basis [!UICONTROL report suite] houdt.

### Historie herstellen

Soms duurt het even voordat uw gebruikers zich aanmelden en [!DNL Co-op Graph] of [!DNL Private Graph] zich identificeren en hun apparaten in kaart brengen. CDA gebruikt een terugblik-achtervenster van 30 dagen, die het toestaat om een eerder niet geïdentificeerde bezoeker als persoon tot 30 dagen in het verleden opnieuw te verklaren.

Hoe helpt dit? Herinnert de gebruikersreis van Isabelle uit de bovenstaande discussie:

![[!DNL Cross-Device Analytics] Reis](assets/cda-isabelle-journey-cross-device-analytics.png)

Het is mogelijk dat Isabelle zich pas heeft aangemeld voordat de aankoop werd uitgevoerd en dat de [!DNL Co-op Graph] of [!DNL Private Graph] de apparaten van Isabelle pas enige tijd na de aankoop in kaart hebben gebracht. Maar de terugblik van de CDA van 30 dagen staat CDA toe om het verleden van Isabelle op een persoonniveau te herbevestigen, die u van het dwars-apparaat mening van haar reis voorzien die u nodig hebt.

>[!NOTE]
>
>Aangezien de geschiedenis kan worden aangepast, betekent dit dat uw gegevens in de loop der tijd kunnen veranderen in een CDA-Toegelaten [!UICONTROL virtual report suite]. Houd dit in mening aangezien u inzichten van een op CDA-Gebaseerde analyse deelt.

## Vereisten voor [!UICONTROL Cross-Device Analytics]

CDA is inbegrepen met [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html). Vanaf september 2019 kunnen [!DNL Analytics Ultimate]-klanten die aan de onderstaande voorwaarden voldoen, gebruikmaken van CDA. De voorwaarden voor CDA zijn als volgt:

* Uw bedrijf moet lid van [!DNL Adobe Experience Platform Identity Service] [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) zijn, of [!DNL Adobe Experience Platform Identity Service Private Graph] gebruiken.
* U moet alles implementeren dat vereist is voor [!DNL Co-op Graph] of [!DNL Private Graph], inclusief [Experience Cloud ID (ECID)](https://docs.adobe.com/content/help/en/id-service/using/home.html) en ID synchroniseren met de grafiek. Naast technische vereisten heeft de [!DNL Co-op Graph] andere wettelijke en contractuele vereisten.
* Het is momenteel niet mogelijk om twee IMS-organen te gebruiken met één [!DNL Private Graph], dus moet u standaardiseren op één IMS-org. In sommige gevallen is het mogelijk dat een klant met meerdere IMS-organen de [!DNL Co-op Graph] in combinatie met CDA gebruikt.
* De [!DNL Co-op graph] en [!DNL Private Graph], evenals bepaalde componenten van CDA worden ontvangen in [!DNL Microsoft Azure]. Dit betekent [!DNL Analytics] gegevens worden gekopieerd heen en weer tussen Adobe verwerkingscentrum en Adobe aanwezigheid in &lt;a1/. [!DNL Microsoft Azure] Sommige [!DNL Analytics] gegevens worden opgeslagen in [!DNL Azure]. Uw bedrijf moet met deze regeling instemmen.
* CDA vereist een &quot;cross-device&quot; [!UICONTROL report suite]. Dat wil zeggen dat de [!UICONTROL report suite] die u voor CDA gebruikt, gegevens moeten bevatten van verschillende apparaattypen of &quot;oppervlakken&quot;, zoals het bureaublad, het mobiele web en de mobiele app. Vanaf september 2019 moet het serveroproepvolume voor deze [!UICONTROL report suite] 100MM serveraanroepen/dag of minder zijn. (De grenzen van het het vraagvolume van de Server zullen in de komende maanden stijgen.)
* Vanaf september 2019 zijn [!DNL Co-op Graph] en [!DNL Private Graph] alleen beschikbaar in Noord-Amerika. Het schema voor de aanwezigheid van grafieken in EMEA en APAC zal in de toekomst worden bekendgemaakt. Als u in die regio&#39;s bent, moedigen wij u aan om nu al naar deze voorwaarden te beginnen kijken zodat u klaar bent om te gaan wanneer de grafiek beschikbaar wordt.

## Apparaatgegevens interpreteren

### Personen zonder bezoekers

Binnen CDA [!UICONTROL Virtual Report Suite], zult u een paar veranderingen zien. De metrische waarde [!UICONTROL Unique Visitors] wordt bijvoorbeeld vervangen door twee nieuwe metriek: [!UICONTROL People] en [!UICONTROL Unique Devices]. Deze nieuwe meetgegevens geven u veel beter inzicht in de omvang van het publiek.

*Personen en unieke*
![apparatenCDA  [!UICONTROL People Metric]](assets/cda-people-metric.png)

In [[!UICONTROL Segment Builder]](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-build.html), is [!UICONTROL Visitor] segmentcontainer vervangen door een [!UICONTROL Person] segmentcontainer. Met een CDA VRS kunt u apparaatsegmenten maken, zoals:

* Personen die meer dan één apparaat gebruiken
* Personen die hun reis op een mobiel apparaat beginnen en later op een desktopapparaat kopen
* Bezoek waarbij mensen meerdere apparaten gebruiken om een taak uit te voeren

*Person-level*
![[!DNL Segment Builder] [!UICONTROL Person] segmentsContainer](assets/cda-segment-builder-person-container.png)

### Dimension Persistentie

Binnen een CDA VRS, blijven de afmetingen zoals [!DNL eVars] nu automatisch over apparaten. Bijvoorbeeld, een [!DNL eVar] die als wordt gevormd:

* Toewijzing: Recentste (laatste)
* Vervalt na: Aanschaffen

zal nu automatisch van één apparaat aan een andere blijven tot de gebeurtenis van de Aankoop in brand wordt gestoken.

## Apparaatgegevens analyseren in Analysis Workspace

### Persoonlijke analyse van het publiek

Heb je je ooit afgevraagd hoeveel mensen met je merk communiceren? Wilt u weten hoeveel en welk type apparaten ze gebruiken? Hoe overlapt hun gebruik? Met behulp van een CDA VRS kunt u cross-device [Venn diagrammen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/venn.html) en apparaten-per-persoon [histogrammen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/histogram.html) maken.

*Persoonlijke*
![analyse van het publiekVenn en Histogram](assets/cda-venn-and-histogram.png)

### Cross-Device [!DNL Flow]

Met CDA en Analysis Workspace, kunt u visualiseren hoe de mensen zich van één apparaat aan een andere in tijd in [[!DNL Flow visualization]](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/flow/flow.html) bewegen. Je kunt zien waar ze op hun reis wegvallen, en waar ze verdergaan.

*[!DNL Flow]met CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Cross-Device [!DNL Fallout]

U kunt waarschijnlijk verschillende [[!DNL Fallout visualizations]](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html) gebruiken om te analyseren hoe goed gebruikers het door een bepaalde reeks stappen maken alvorens succes te bereiken. Wist u dat de weergave van deze [!DNL Fallout visualizations] beperkt is bij gebruik van traditionele apparaatgebaseerde analysemogelijkheden? De volgende stap kan alleen worden uitgevoerd in dezelfde browser of app als de vorige stap als de volgende stap is geslaagd. In op apparaten gebaseerde analyses bent u blind voor mensen die de volgende stap met succes op een ander apparaat voltooien.

Geen zorgen, CDA heeft u bedekt. CDA leidt tot de dwars-apparatenmening die [!DNL Fallout visualizations] veel, veel nuttiger maakt. Het gaat er immers om of de persoon uiteindelijk ergens in zijn taak is geslaagd.

*[!DNL Fallout]met CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Omdat CDA een laag van dwars-apparatengegevens onder Analysis Workspace creeert, zal al uw analyse met een dwars-apparatenperspectief worden gearomatiseerd. Één krachtig voorbeeld is door [[!DNL Attribution IQ]](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html). [!DNL Attribution IQ] in Analysis Workspace kunt u meerdere attributiemodellen naast elkaar vergelijken. Met behulp van deze mogelijkheid kunt u nu vergelijken hoe verschillende apparaten tot succes bijdragen.

Stel dat u wilt begrijpen hoe vaak een mobiele telefoon het eerste apparaat is dat wordt gebruikt in een interactie die uiteindelijk tot succes leidt. Dit staat voor de &#39;aanschafsnelheid&#39; van de mobiele telefoon. Met CDA + [!DNL Attribution IQ] kunt u deze analyse uitvoeren:

*[!DNL Attribution IQ]met CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

Raadpleeg de [[!DNL Cross-Device Analytics] Help-documentatie](https://docs.adobe.com/content/help/en/analytics/components/cda/cda-home.html) voor meer informatie.
