---
title: Uw analytische traceringsserver en rapportsuite-id identificeren
description: Wanneer vestiging Adobe Analytics, of wanneer het van verwijzingen voorzien in andere oplossingen van Experience Cloud, is het vaak nuttig of zelfs noodzakelijk om Analytics "het Volgen Server"te kennen die u gebruikt, of ook de "Reeks van het Rapport"die u gegevens naar verzendt. In deze video ziet u hoe u beide waarden kunt vinden, ongeacht of u Adobe Analytics al hebt geïmplementeerd.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 474e68e2937c82efa459b6ed8048a4abd2753285
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Analyses identificeren [!DNL tracking server] en [!UICONTROL report suite ID] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Wanneer vestiging Adobe Analytics, of wanneer van verwijzingen voorzien in andere oplossingen van Experience Cloud, is het vaak nuttig of zelfs noodzakelijk om de Analytics &quot;volgende server&quot;te kennen die u gebruikt, of ook &quot;[!UICONTROL report suite]&quot;die u gegevens naar verzendt. In deze video ziet u hoe u beide waarden kunt vinden, ongeacht of u Adobe Analytics al hebt geïmplementeerd.

>[!IMPORTANT]
>
>Dit artikel en deze video zijn van toepassing op een &quot;AppMeasurement&quot;-implementatie van Adobe Analytics en niet op een implementatie die gebruikmaakt van de Web SDK.

## Na de implementatie {#after-implementation}

Nadat u Analytics op een site hebt geïmplementeerd, vindt u de [!DNL tracking server] en de [!DNL report suite ID] rechts in het trackingbaken. [!DNL tracking server] is hostname in het baken, zodat is gemakkelijk te vinden. De id&#39;s van [!UICONTROL report suite] zijn een door komma&#39;s gescheiden lijst rechts na &quot;/b/ss/&quot; in de padnaam van het baken.

Om het baken, evenals alle andere informatie te zien die aan Analytics en andere oplossingen van Experience Cloud komt, installeer de [ &quot;Ervaar de Uitbreiding van de Debugger van de Wolk&quot;Chrome ](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=nl).

## Voor implementatie {#before-implementation}

**[!DNL Tracking server]** - Als u nog niet bent begonnen met uw Adobe Analytics-implementatie, kiest u een subdomein voor &quot;.sc.omtr dc.net&quot; [!DNL tracking server] . Bijvoorbeeld, laten we zeggen dat ik een online hoesje heb genaamd &quot;Jim&#39;s Brims.&quot; Ik kan mijn [!DNL tracking server] eenvoudig instellen op:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Report suite]** - Als u een lijst wilt zien van uw [!UICONTROL report suites] die zijn gemaakt, meldt u zich aan bij [!DNL Analytics] en gaat u naar [!UICONTROL Admin] > [!UICONTROL Report Suites] in het bovenste menu om een lijst met [!UICONTROL report suites] weer te geven, inclusief hun id en titel.

Bekijk de video hieronder voor meer informatie.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12&learn=on)
