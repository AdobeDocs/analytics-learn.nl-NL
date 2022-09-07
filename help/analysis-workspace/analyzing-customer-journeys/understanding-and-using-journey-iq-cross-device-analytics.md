---
title: IQ voor reizen begrijpen en gebruiken - Apparaatanalyse
description: Wanneer gebruikers met uw merk communiceren, doen zij dat op vele manieren en op meerdere apparaten. Apparaatanalyse kan worden geïntegreerd met de Adobe Experience Platform Identity Service om te bepalen hoe apparaten aan personen worden toegewezen. Vervolgens wordt deze informatie gebruikt om een apparaatweergave van gebruikersgedrag te maken. Dit leidt ertoe dat we in staat zijn om analyses uit te voeren op mensen, niet op apparaten.
feature: CDA
topics: null
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
role: User
level: Intermediate
exl-id: 3748d5d7-d250-4057-8131-afdc66c80200
source-git-commit: 01e6e84f748e359aeb42c9be3afa52088f41018b
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%

---

# Begrijpen en gebruiken [!DNL Journey IQ] - Apparaatanalyse

Wanneer gebruikers met uw merk communiceren, doen zij dat op vele manieren en op meerdere apparaten. Apparaatanalyse kan worden geïntegreerd met de [!DNL Adobe Experience Platform Identity Service] om te identificeren hoe de apparaten aan mensen in kaart brengen. Vervolgens wordt deze informatie gebruikt om een apparaatweergave van gebruikersgedrag te maken. Dit leidt ertoe dat we in staat zijn om analyses uit te voeren op mensen, niet op apparaten.

## Overzicht van apparaatanalyse

### Ik ben niet mijn apparaten

Wanneer gebruikers met uw merk werken, doen ze dat op verschillende manieren en op meerdere &quot;oppervlakken&quot; of &quot;apparaten&quot;. Ze kunnen een webbrowser gebruiken op een pc of mobiel apparaat, of ze kunnen een mobiele app gebruiken. In traditionele digitale analyses, die opgroeiden in gegevensverzameling gebaseerd op cookies, wordt elk van deze oppervlakken weergegeven als een unieke &quot;bezoeker&quot;. Dit betekent dat elk van uw menselijke gebruikers wordt vertegenwoordigd als veelvoudige unieke bezoekers.

Hier is een voorbeeld. Stel dat Isabelle op de volgende manier met uw merk communiceert:

*Isabelle is drie bezoekers*
![Traditionele analytische reis](assets/cda-isabelle-journey-traditional-analytics.png)

Met behulp van traditionele analyses wordt de reis van Isabelle in drie stukken gebroken. Zij wordt vertegenwoordigd als drie unieke bezoekers, die elk een verschillend apparaat gebruikten om geïsoleerde taken uit te voeren. Wat nodig is, is een verenigde, cross-device weergave van de interacties van Isabelle. [!DNL Journey IQ: Cross-Device Analytics] biedt deze weergave.

*Isabelle is één persoon*
![Reis voor apparaatanalyse](assets/cda-isabelle-journey-cross-device-analytics.png)

### Een apparaatweergave biedt betere analysemogelijkheden

Een persoonlijk-centrische, cross-device weergave van het gedrag van Isabelle kan een belangrijk verschil maken voor uw analyse. De traditionele aanpak op bezoekersbasis geeft u bijvoorbeeld niet het volledige beeld van de doeltreffendheid van marketingkanalen. Laten we eens kijken naar de reis van Isabelle, waarbij we ons richten op welk kanaal krediet ontvangt voor haar productweergave en voor haar aankoop. We gebruiken [!UICONTROL last-touch] Toewijzing voor eenvoud, maar hetzelfde probleem doet zich voor met elk attributiemodel wanneer u het gedrag van Isabelle opsplitst in verschillende bezoekers. Het gebruik van de traditionele, op bezoekers gebaseerde kijk op de wereld geeft zeer verschillende, zelfs misleidende resultaten:

*Traditionele analyse versus apparaatanalyse*
![kanaaltoewijzing](assets/channel-attribution.png)

U ziet dat het e-mailkanaal in de apparaatweergave krediet ontvangt voor zowel de productweergave als de aankoop, die de werkelijke beleving van Isabelle nauwkeuriger weergeeft.

Lees meer over:

* Hoe [!DNL Cross-Device Analytics] Werken
* Vereisten voor [!DNL Cross-Device Analytics]
* Apparaatgegevens interpreteren
* Apparaatgegevens analyseren in Analysis Workspace

## Hoe [!DNL Cross-Device Analytics] Werken

[!DNL Journey IQ: Cross-Device Analytics (CDA)] integreert met de [!DNL Adobe Experience Platform Identity Service], waarbij de [!DNL Device Graph] om te identificeren hoe de apparaten aan mensen in kaart brengen. Vervolgens wordt deze informatie gebruikt om een apparaatweergave van gebruikersgedrag te maken. CDA bevat ongeëvenaarde mogelijkheden en tools om uw onderneming te helpen het gebruik van meerdere apparaten en de ervaring van klanten op deze apparaten te begrijpen in hun interactie met uw merk. Het bevindt zich als een laag onder Analysis Workspace om diepgaand inzicht te verschaffen in persoonlijke publieksanalyse en attributie, segmentatie en reisanalyse door middel van krachtige hulpmiddelen, zoals [!UICONTROL Fallout], [!DNL Flow], [!DNL Cohort], [!DNL Segment IQ] en [!DNL Attribution IQ].

### De [!DNL Cross-Device Virtual Report Suite]

CDA wordt aangeboden door middel van een speciaal soort cross-device [[!UICONTROL Virtual Report Suite]](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html). Dit staat u toe om de originele op apparaat-gebaseerde rapportreeks te blijven gebruiken aangezien u dwars-apparatenanalyses in uw organisatie introduceert. Het instellen van een CDA VRS is eenvoudig.

Kies in stap een van de VRS-ontwikkelaars de optie [!UICONTROL report suite] die door Adobe als CDA-Toegelaten is gevormd:

*Kies een basis voor CDA (bron)[!UICONTROL report suite]*
![[!UICONTROL Virtual Report Suite] Stap één](assets/cda-vrs-step-one.png)

Vervolgens inschakelen [!UICONTROL Report Time Processing] en [!UICONTROL cross-device stitching]:

*Inschakelen [!UICONTROL report-time processing] en[!UICONTROL cross-device stitching]*
![[!UICONTROL Virtual Report Suite] Stap twee](assets/cda-vrs-step-two.png)

Voltooi de VRS-instelling en sla deze op. Het CDA VRS wordt in Analysis Workspace weergegeven met een speciaal pictogram ernaast, zoals hieronder wordt getoond:

*De CDA VRS selecteren in Analysis Workspace*
![[!UICONTROL Virtual Report Suite] Stap drie](assets/cda-vrs-step-three.png)

>[!TIP]
>
>U kunt maximaal CDA maken [!UICONTROL virtual report suites] zoals u bovenop de CDA-Toegelaten basis wilt [!UICONTROL report suite].

### Historie herstellen

Soms duurt het even voordat uw gebruikers zich aanmelden en voor de [!DNL Device Graph] om hen te identificeren en hun apparaten samen in kaart te brengen. CDA gebruikt een terugblik-achtervenster van 30 dagen, die het toestaat om een eerder niet geïdentificeerde bezoeker als persoon tot 30 dagen in het verleden opnieuw te verklaren.

Hoe helpt dit? Herinnert de gebruikersreis van Isabelle uit de bovenstaande discussie:

![[!DNL Cross-Device Analytics] Reis](assets/cda-isabelle-journey-cross-device-analytics.png)

Het is mogelijk dat Isabelle zich pas heeft aangemeld voordat hij de aankoop maakte en dat de [!DNL Device Graph] Kon de toestellen van Isabelle pas ergens na haar aankoop in kaart brengen. Maar de terugblik van de CDA van 30 dagen staat CDA toe om het verleden van Isabelle op een persoonniveau te herbevestigen, die u van het dwars-apparaat mening van haar reis voorzien die u nodig hebt.

>[!NOTE]
>
>Aangezien de geschiedenis kan worden aangepast, betekent dit dat uw gegevens in de loop der tijd kunnen veranderen in een CDA-toepassing [!UICONTROL virtual report suite]. Houd dit in mening aangezien u inzichten van een op CDA-Gebaseerde analyse deelt.

## Vereisten voor [!UICONTROL Cross-Device Analytics]

CDA is inbegrepen bij [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html). Vanaf september 2019, [!DNL Analytics Ultimate] klanten die aan de onderstaande voorwaarden voldoen, komen in aanmerking om gebruik te maken van CDA. De voorwaarden voor CDA zijn als volgt:

* Uw bedrijf moet de [!DNL Adobe Experience Platform Identity Service Device Graph].
* U moet alles implementeren wat vereist is voor de [!DNL Device Graph] inclusief [Experience Cloud-ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/home.html) en ID synchroniseren met de grafiek.
* Het is momenteel niet mogelijk twee IMS-organen met één IMS-instantie te gebruiken [!DNL Device Graph], dus moet u standaardiseren op één IMS-org.
* De [!DNL Device Graph]en bepaalde componenten van CDA worden gehost in [!DNL Microsoft Azure]. Dit betekent [!DNL Analytics] gegevens worden heen en weer gekopieerd tussen Adobe verwerkingscentrum en Adobe in [!DNL Microsoft Azure]. Sommige [!DNL Analytics] gegevens worden opgeslagen in [!DNL Azure]. Uw bedrijf moet met deze regeling instemmen.
* CDA vereist een &quot;cross-device&quot; [!UICONTROL report suite]. Dat wil zeggen: [!UICONTROL report suite] Als u CDA gebruikt, moet u gegevens van meerdere verschillende apparaattypen of &quot;oppervlakken&quot; opnemen, zoals het bureaublad, het mobiele web en de mobiele app. Vanaf september 2019, het volume van de servervraag voor dit [!UICONTROL report suite] moet 100MM servervraag/dag of minder zijn. (De grenzen van het het vraagvolume van de Server zullen in de komende maanden stijgen.)

## Apparaatgegevens interpreteren

### Personen zonder bezoekers

Binnen de CDA [!UICONTROL Virtual Report Suite], zult u een paar veranderingen zien. De [!UICONTROL Unique Visitors] De metrische waarde wordt vervangen door twee nieuwe metriek: [!UICONTROL People] en [!UICONTROL Unique Devices]. Deze nieuwe meetgegevens geven u veel beter inzicht in de omvang van het publiek.

*Personen en unieke apparaten*
![CDA [!UICONTROL People Metric]](assets/cda-people-metric.png)

In de [[!UICONTROL Segment Builder]](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html)de [!UICONTROL Visitor] segmentcontainer is vervangen door een [!UICONTROL Person] segmentcontainer. Met een CDA VRS kunt u apparaatsegmenten maken, zoals:

* Personen die meer dan één apparaat gebruiken
* Personen die hun reis op een mobiel apparaat beginnen en later op een desktopapparaat kopen
* Bezoek waarbij mensen meerdere apparaten gebruiken om een taak uit te voeren

*Persoonssegmenten*
![[!DNL Segment Builder] [!UICONTROL Person] Container](assets/cda-segment-builder-person-container.png)

### Dimension Persistentie

Binnen een CDA VRS, dimensies zoals [!DNL eVars] blijft nu automatisch aanwezig op verschillende apparaten. Een [!DNL eVar] dat wordt gevormd als:

* Toewijzing: Recentste (laatste)
* Vervalt na: Aanschaffen

zal nu automatisch van één apparaat aan een andere blijven tot de gebeurtenis van de Aankoop in brand wordt gestoken.

## Apparaatgegevens analyseren in Analysis Workspace

### Persoonlijke analyse van het publiek

Heb je je ooit afgevraagd hoeveel mensen met je merk communiceren? Wilt u weten hoeveel en welk type apparaten ze gebruiken? Hoe overlapt hun gebruik? Met een CDA VRS kunt u een apparaatoverschrijdend systeem maken [Venn-diagrammen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/venn.html) en apparaten per persoon [histogrammen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/histogram.html).

*Persoonlijke publieksanalyse*
![Venn en histogram](assets/cda-venn-and-histogram.png)

### Cross-device [!DNL Flow]

Met CDA en Analysis Workspace kunt u visualiseren hoe mensen in de loop der tijd van het ene apparaat naar het andere bewegen [[!DNL Flow visualization]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/flow/flow.html). Je kunt zien waar ze op hun reis wegvallen, en waar ze verdergaan.

*[!DNL Flow]met CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Cross-device [!DNL Fallout]

U kunt waarschijnlijk verschillende [[!DNL Fallout visualizations]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html) om te analyseren hoe goed de gebruikers het door een bepaalde reeks stappen maken alvorens succes te bereiken. Wist u uw mening over deze [!DNL Fallout visualizations] is beperkt wanneer gebruik wordt gemaakt van traditionele apparaatgebaseerde analysemogelijkheden? De volgende stap kan alleen worden uitgevoerd in dezelfde browser of app als de vorige stap als de volgende stap is geslaagd. In op apparaten gebaseerde analyses bent u blind voor mensen die de volgende stap met succes op een ander apparaat voltooien.

Geen zorgen, CDA heeft u bedekt. CDA maakt de apparaatweergave die [!DNL Fallout visualizations] veel, veel nuttiger. Het gaat er immers om of de persoon uiteindelijk ergens in zijn taak is geslaagd.

*[!DNL Fallout]met CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Omdat CDA een laag van dwars-apparatengegevens onder Analysis Workspace creeert, zal al uw analyse met een dwars-apparatenperspectief worden gearomatiseerd. Eén krachtig voorbeeld is [[!DNL Attribution IQ]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution/attribution.html). [!DNL Attribution IQ] in Analysis Workspace kunt u meerdere attributiemodellen naast elkaar vergelijken. Met behulp van deze mogelijkheid kunt u nu vergelijken hoe verschillende apparaten tot succes bijdragen.

Stel dat u wilt begrijpen hoe vaak een mobiele telefoon het eerste apparaat is dat wordt gebruikt in een interactie die uiteindelijk tot succes leidt. Dit staat voor de &#39;aanschafsnelheid&#39; van de mobiele telefoon. CDA + [!DNL Attribution IQ] Hiermee kunt u deze analyse uitvoeren:

*[!DNL Attribution IQ]met CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

Zie voor meer informatie de [[!DNL Cross-Device Analytics] Help-documentatie](https://experienceleague.adobe.com/docs/analytics/components/cda/cda-home.html).
