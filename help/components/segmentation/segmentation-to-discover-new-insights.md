---
title: Wacht even een segment... met segmentatie om nieuwe inzichten in Analysis Workspace te ontdekken
description: Leer hoe u segmenten in Adobe Analytics gebruikt om nieuwe inzichten te ontdekken uit uw Analysis Workspace-visualisaties en vrije-vormtabellen.
feature: Segmentation
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13268
thumbnail: KT-13268.jpeg
source-git-commit: b11a329ca3f5c676aea08c7037e5ee87003edfe6
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 1%

---


# Wacht nu even een segment... Het gebruiken van segmenten om nieuwe inzichten in Analysis Workspace te ontdekken

Of je nu een nieuwe Adobe Analytics-gebruiker bent of een geseizoenpro, je maakt nogal wat gebruik van segmenten in je Analysis Workspace-projecten. Als [Adobe Experience League](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=nl-NL) beschrijft, &quot;de segmenten staan u toe om ondergroepen van bezoekers te identificeren die op kenmerken of websiteinteractie worden gebaseerd.&quot; Hoewel het basisresultaat van deze functie erin bestaat groepen gebruikers te isoleren, bezoeken te brengen of te bezoeken aan uw site, kan een scherpe analist zoals uzelf creatief worden met dit programma en nieuwe manieren vinden om inzicht te krijgen in uw sitetaken. De lijst met mogelijke opties is enorm, dus aarzel niet om uw eigen opties te maken en deze te delen met anderen bij uw organisatie of online in gemeenschappen als de [Adobe Analytics Community](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community) op Experience League of de [#Slack meten](https://www.measure.chat/) gemeenschap.

Als u een snelle vernieuwing nodig hebt voor het maken van een segment, raadpleegt u de documentatie bij het Experience League over het gebruik van het gereedschap [Segment Builder](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=nl-NL) in Analysis Workspace.

## Segmenten vergelijken en contrasteren

In Analysis Workspace kunt u twee segmenten vergelijken met &quot;[Segmentvergelijking](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html?lang=nl-NL)&quot;. Segmentvergelijking vindt u in het gedeelte Deelvensters van de linkernavigatiebalk:

![Seg 01](assets/seg01.png)

Soms hebt u echter geen volledig vergelijkingspaneel nodig om uw eindgebruikers inzicht in de persoonlijke sleutel te geven. Gelukkig kunnen sommige eigenschappen ook in een standaardpaneel worden vergeleken.

De [Visualisatie vendiagram](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/venn.html?lang=nl-NL) Deze functie kan u helpen bij het maken van een snelle vergelijking, zodat u de overlappende sessies, bestellingen, gebruikers enz. kunt aanwijzen en bekijken. tussen 2-3 aangepaste segmenten. U kunt ook snel segmenten maken door met de rechtermuisknop op een van de overlappende secties te klikken:

![Seg 02](assets/s02.png)

Soms bevindt de belangrijke informatie zich niet in de overlappende gegevens, maar in de gegevens die elkaar niet overlappen. Een snelle manier om dit te bekijken is een exemplaar van één segment tot stand te brengen en het te maken een &quot;Uitsluiten&quot;segment:

![Seg 03](assets/s03.png)

Door het segment &quot;exclude&quot; te stapelen met het andere segment in uw vergelijking, kunt u nu snel berekenen hoeveel bezoeken uw menupagina raakten zonder ook de homepage in de zelfde zitting te bekijken:

![Seg 04](assets/s04.png)

## Stapelaanval

Op dezelfde manier kunt u de elkaar kruisende gegevens van een diagram van Venn tot stand brengen door eenvoudig om het even welke segmenten samen te stapelen. Er is geen limiet voor het aantal segmenten of de afzonderlijke afmetingen die u stapelt. Als ik bijvoorbeeld snel wilde weten welke dagen van de week vorige maand mijn site een bezoek had op een mobiele telefoon, met name een Samsung Galaxy A52s, die mijn menu- en voedingspagina&#39;s wel zag, maar mijn homepage NIET zag, kan ik deze snel als volgt bouwen:

![Seg 05](assets/s05.png)

Maar nog beter, zodra ik die perfecte ondergroep van mijn gebruiker of bezoekbasis vind, kan ik al die waarden selecteren, met de rechtermuisknop klikken, en een segment onmiddellijk creëren:

![Seg 06](assets/s06.png)

![Seg 07](assets/s07.png)

![Seg 08](assets/s08.png)

Dat is veel macht in één segment.

## Een segment getallen voor een aantal segmenten

Vele gebruikers kijken vaak naar nominale, ordinale, of intervalwaarden wanneer het bouwen van segmenten - dingen zoals een bezochte pagina, een leeftijdswaaier van gebruikers, of het aantal bezoeken een gebruiker in het verleden heeft gemaakt. Nochtans, kunt u verhoudingsgegevens ook gebruiken wanneer het creëren van een segment door deze waarden - of zij standaardafmetingen, standaardmetriek, of douanevariabelen en metriek voor uw organisatie zijn te sluiten.

De tijd die bijvoorbeeld op de pagina wordt doorgebracht of de tijd die per bezoek wordt besteed, heeft vooraf gebouwde beschikbare emmers:

![Seg 09](assets/s09.png)

Het is echter mogelijk dat deze niet altijd in de behoeften van uw organisatie passen. De meeste bezoeken van de site zijn wellicht korter dan 10 minuten. U kunt korrelmetingen gebruiken om emmers van verschillende grootte te maken. Hier is gecreeerd om bezoeken te bekijken die tussen 1 minuut, 1 seconde en 1 minuut, 30 seconden duren:

![10 sep.](assets/s10.png)

Zodra gecreeerd, kan ik nu beginnen mijn bezoeken, orden, en andere gebeurtenissen door de verschillende gespikte tijdgroepen te bekijken die ik heb aangepast:

![11 seg.](assets/s11.png)

U kunt zelfs beginnen te onderzoeken hoe uw Zeer belangrijke Indicatoren van Prestaties (KPIs) als factor van hoeveel tijd een gebruiker besteedt, hoeveel pagina&#39;s zij in een bezoek raken, hoeveel tijden zij in het verleden, of een andere numerieke waarde hebben bezocht - fundamenteel toelatend u om metrisch als factor van een andere metrisch te bekijken:

![12 seg.](assets/s12.png)

De mogelijkheden om segmenten te gebruiken om nieuwe inzichten te vinden zijn eindeloos! Dit is gewoon een uitgangspunt. Probeer er zelf een paar uit en laat de gemeenschap weten wat u ontdekt: [Adobe Analytics Community](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community) op Experience League of de [#Slack meten](https://www.measure.chat/) gemeenschap.

Gelukkig segmenteren!

## Auteur

Dit document is geschreven door:

![Dan Cummings](assets/seg13.png)

**Dan Cummings**, Sr. Product Engineering Analytics Manager bij McDonald&#39;s Corporation

Adobe Analytics Champion

