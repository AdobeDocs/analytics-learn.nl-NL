---
title: Een gegevenslaag gebruiken om paginanaam en andere variabelen in Adobe Analytics in te stellen via Starten
description: Het gebruiken van een gegevenslaag voor Analytics en andere oplossingen van Experience Cloud wordt beschouwd als beste praktijken. In deze video leert u hoe u uw waarden uit de gegevenslaag kunt halen en deze in Launch kunt gebruiken om variabelen in Adobe Analytics te vullen.
feature: Launch Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
role: Developer, Data Engineer
level: Beginner
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: fe861dfd541c1b9cb3b233fa3f56d55054305fd9
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Een gegevenslaag gebruiken om paginanaam en andere variabelen in te stellen via [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

Het gebruiken van een gegevenslaag voor [!DNL Analytics] en andere oplossingen van Experience Cloud wordt beschouwd als beste praktijken. In deze video leert u hoe u uw waarden uit de gegevenslaag kunt halen en deze in [!DNL Experience Platform Launch] kunt gebruiken om variabelen in Adobe Analytics te vullen.

## Gegevenslagen {#data-layers}

Het wordt aanbevolen een gegevenslaag te gebruiken wanneer u werkt met gegevens op uw site en met Adobe Experience Cloud-oplossingen, vooral met Adobe Analytics. Een _gegevenslaag_ is een framework van JavaScript-objecten dat ontwikkelaars op pagina&#39;s invoegen. De gegevenslagen kunnen worden gebruikt door het volgen hulpmiddelen (met inbegrip van systemen van het markeringsbeheer zoals [!DNL Experience Platform Launch]) om rapporten te bevolken. Meer informatie over gegevenslagen vindt u in de [Experience Cloud-documentatie](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=en) of op de [W3C-site](https://www.w3.org/).

Zie ook de blog [Gegevenslagen: Van Buzzword tot Beste praktijken,](https://theblog.adobe.com/data-layers-buzzword-best-practice/), die u wat grote informatie over gegevenslagen, evenals een paar voorbeelden geeft.

## Gegevenslagen, [!DNL Experience Platform Launch] en Adobe Analytics (oh my?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Maak een standaard voor een gegevenslaag die u op uw site wilt gebruiken en waarnaar [!DNL Experience Platform Launch] kan verwijzen.

   1. Plaats deze gegevenslaag zo hoog mogelijk in het hoofd van de pagina, vóór de vraag aan [!DNL Experience Platform Launch], zodat de waarden onmiddellijk door [!DNL Launch] kunnen worden gebruikt, en door oplossingen van Adobe die hoog op de pagina, zoals Adobe Target moeten zijn.

1. Vul de gegevens in de gegevenslaag.
1. In [!DNL Experience Platform Launch], creeer &quot;[!UICONTROL data elements]&quot;die de gegevenspunten in de gegevenslaag van verwijzingen voorzien, en die door [!DNL Experience Platform Launch] in [!UICONTROL rules], [!UICONTROL extensions], etc. kunnen worden gebruikt.
1. Gebruik [!UICONTROL data elements] in of de [!DNL Analytics] uitbreiding globale variabelen of in een regel, toewijzend de waarden in [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName], of andere [!DNL Analytics] variabelen.
1. Trigger een baken dat de gegevens naar [!DNL Analytics] verzendt.

De volgende video doorloopt u het proces.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
