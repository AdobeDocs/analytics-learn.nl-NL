---
title: Verschillen tussen de gesegmenteerde bouwer en snelle segmenten in Analysis Workspace
description: De segmenten kunnen één van de krachtigste hulpmiddelen in uw toolkit van de gegevensanalyse zijn. Leer de verschillen tussen het gebruiken van de segmentbouwer en snelle segmenten in Analysis Workspace voor efficiency.
feature: Segmentation
role: User
level: Beginner
doc-type: article
kt: KT-13118
source-git-commit: 9484b2e981d78be59b6ea16eeae2cf6f212c81ab
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---


# Verschillen tussen de gesegmenteerde bouwer en snelle segmenten in Analysis Workspace

De segmenten kunnen één van de krachtigste hulpmiddelen in uw toolkit van de gegevensanalyse zijn. Leer de verschillen tussen het gebruiken van de segmentbouwer en snelle segmenten in Analysis Workspace voor efficiency.

>[!TIP]
>
> Klik op de afbeelding onder aan de pagina om een handige herinnering te downloaden wanneer u elk gereedschap in Analysis Workspace gebruikt.

De segmenten kunnen één van de krachtigste hulpmiddelen in uw toolkit van de gegevensanalyse zijn. Wanneer u naar specifieke groepen verkeer, plaatssecties, of klantenreizen wilt kijken, kan het gebruiken van segmenten een grote manier zijn om uw analyse op een bepaalde ondergroep van verkeer aan uw plaats te concentreren. Omdat ik uit een detailhandelmilieu kom, zijn sommige van de nuttigste segmenten ik voor verschillende soorten klantengroepen, bijvoorbeeld nieuwe vs. bestaande klanten, klanten die in een rekening tegenover gasten worden ondertekend, etc. heb gemaakt. Maar u kunt hen voor verschillende plaatssecties ook maken, klanten die specifieke acties uitvoeren, of om het even wat anders u aan kunt denken!

**Er zijn twee belangrijke manieren om segmenten te bouwen:**

* Het gebruiken van de segmentbouwer in het componentenmenu
* Snelle segmenten boven in een deelvenster gebruiken

Als u uw segment gebruikend de segmentbouwer bouwt, kunt u het bewaren aan hergebruik in andere projecten. Dit is een goede manier om zich op specifieke groepen klanten, bijvoorbeeld, mensen te kunnen concentreren die bepaalde secties van de plaats bezoeken en dan een aankoop maken. Anderzijds, als u een verkennende analyse uitvoert en verschillende segmentmontages wilt testen, kan de snelle segmentbouwer een grote hulp zijn. Laten we eens kijken naar enkele van de belangrijkste voordelen van elke methode.

## Snelle segmenten

Boven aan elk deelvenster kunt u op het snelsegmentpictogram (een trechter met het plus-symbool) klikken om de builder te openen. Op deze manier kunt u een segment op elk niveau maken (hit, visit of bezoeker) met maximaal drie voorwaarden. Net als de belangrijkste segmentbouwer, geeft dit u een aanwijzing op de rechterkant die merkt als het segment gegevens en % van totale verkeersbevolking inbegrepen in het segment terugkeert, hoewel dit een meer vereenvoudigde versie is dan de volledige mening van het segmentvolume die in de segmentbouwer wordt getoond. Wanneer u meerdere voorwaarden toevoegt, kunt u de operatoren &#39;en&#39; en &#39;of&#39; gebruiken. Helaas, is er geen &quot;toen&quot;optie voor snelle segmenten, zodat als u opeenvolgende segmenten nodig hebt zult u de volledige segmentbouwer moeten gebruiken. Er geldt ook een limiet van één container in een snelsegment. Omdat het echt bedoeld is om voor basissegmenten te worden gebruikt die kunnen worden gemaakt en snel worden uitgegeven. Als een snel segment eenmaal is toegepast op een deelvenster of is opgeslagen, kan het niet meer worden bewerkt in het deelvenster.

Wanneer het doen van een verkennende analyse, en u wilt verschillende soorten segmenten testen om te zien hoe de verschillende klantengroepen reageren of hoe de verschillende categorieën presteren - het gebruiken van snelle segmenten is veel sneller dan het gebruiken van de segmentbouwer. Bovendien, zijn deze segmenten slechts beschikbaar in het project zij binnen werden gecreeerd, zodat als het blijkt om niet de resultaten te verstrekken u wilt, te hoeven u zich niet ongerust te maken over het schrappen van het bewaarde segment van de master lijst. Als na het testen van de segmenten u zich realiseert dat het in andere projecten nuttig zal zijn, kunt u altijd de &quot;open bouwer&quot;knoop klikken om het segment in de volledige segmentbouwer te openen om het als normaal segment te bewaren. Zodra u dat doet, echter, zult u niet meer het in de snelle segmentbouwer kunnen uitgeven.

![Snel segment](assets/quick-segement.png)

## Segment Builder

De segmentbouwer kan worden betreden door + symbool boven de lijst van segmenten in het linkermenu van componenten te klikken, of van het klikken van de componentendropdown en het selecteren van &quot;Create Segment...&quot;in tegenstelling tot de snelle segmenten, heeft dit alle opties beschikbaar aan u. Als u meerdere voorwaarden wilt toevoegen, kunt u opeenvolgende segmenten maken met de operator &#39;then&#39;. Met opeenvolgende segmenten kunt u ook &#39;logische groep&#39; gebruiken als niveau (in plaats van een hit, visit of bezoeker). De segmentbouwer zal u ook toestaan om in een beschrijving aan de segmenten toe te voegen, die context kan toevoegen over wie het segment bouwde of welk type van gegevens het is gebouwd om te filtreren, of zelfs eenvoudig &quot;markeringen&quot;aan het segment voor organisatorische doeleinden toe te voegen die allebei niet binnen de snelle segmentbouwer mogelijk zijn.

Het gebruiken van de segmentbouwer is essentieel wanneer uw segment meer dan 3 voorwaarden gaat hebben, als u containers moet gebruiken, of opeenvolgende segmenten wilt. De volledige segmentbouwer heeft veel meer opties om complexere segmenten te maken, die u kunnen helpen verschillende klantentypes, categorieën, klantenreizen, etc. onderbreken. Zodra deze segmenten zijn gecreeerd en bewaard, worden zij toegevoegd aan de master lijst van segmenten, betekenend zij kunnen worden geëtiketteerd, worden goedgekeurd, worden gedeeld, in veelvoudige rapporten worden gebruikt, en aan de Experience Cloud worden gepubliceerd. Het publiceren in de Experience Cloud staat u toe om het segment in andere producten van de Adobe, zoals in Adobe Target voor verpersoonlijkingsgericht te gebruiken. De segmenten die in de segmentbouwer worden gebouwd kunnen niet in het snelle segmentpaneel worden uitgegeven, zult u de segmentbouwer moeten openen om het even welke veranderingen in hen aan te brengen. Gelukkig, verstrekt de voorproefvisualisatie aan het recht een gedetailleerdere analyse van het verkeer het segment de laatste 90 dagen zou brengen, betekenend is het gemakkelijker om zeker te zijn het segment in brengt wat u het wilt alvorens te sparen.

![Segment Builder](assets/segment-builder-quick.png)

## Gevallen gebruiken

In verschillende industrieën, zou uw gebruik voor de bouw van douanesegmenten kunnen verschillen. In het kader van de divisie e-commerce van een grote detailhandelaar, voeren wij vaak verkennende analyses uit om te bepalen welke wegen klanten aan aankoop nemen. Wanneer we pieken of dalingen in acties zoals het toevoegen van producten aan karretjes of het plaatsen van orden zien, is dit waar het gebruiken van de snelle segmenten in handvatten kan komen. Tijdens een analyse kan ik snel een segment voor een specifiek type van klant of voor een bepaalde actie/een verbinding tot stand brengen die zij op klikken. Door niet het moeten de segmentbouwer openen en elk segment opslaan, kan ik de voorwaarden snel toevoegen, en dan hen verwijderen enkel zo snel. Dit bespaart veel tijd wanneer we proberen uit te leggen waarom we een verandering op onze site zien.

Alternatief, zijn er tijden dat de segmentbouwer mijn kant-aan is geweest. Niet elke klant is het zelfde, en vaak willen wij naar specifieke soorten klanten kijken die door acties of wegen worden geïdentificeerd die zij nemen. Door de segmentbouwer te gebruiken, kunnen wij veelvoudige voorwaarden toevoegen om de verschillende soorten klanten te identificeren en de segmenten te bewaren zodat zij door veelvoudige analisten kunnen worden gedeeld en worden gebruikt. Het is belangrijk dat deze typen segmenten consistent zijn in de verschillende rapporten. Daarom is het beter dat er één wordt opgebouwd die iedereen kan gebruiken dan elke persoon die zijn eigen versie bouwt, omdat de resultaten kunnen verschillen.

Over het algemeen, zowel zijn de snelle segmenten als de segmentbouwer uitstekende hulpmiddelen aan gebruik in uw analyse. Ze hebben elk hun doel, voordelen en nadelen. Bekijk onze handige downloadbare tips en trucs hieronder voor een snelle naslaggids.

## Auteur

Dit document is geschreven door:

![Mandy George](assets/mandy-george.jpg)

**Mandy George**, Digital Analyst III op Best Buy Canada

Adobe Analytics Champion

## Download

[![Snelle segmenten downloaden](assets/quick-segments-download-small.jpg)](assets/Adobe_Analytics_Segments_Vs_Segment_Builder_Reference_Guide.pdf)
