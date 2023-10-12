---
title: Uw analytische traceringsserver en rapportsuite-id identificeren
description: Wanneer vestiging Adobe Analytics, of wanneer het van verwijzingen voorzien in andere oplossingen van het Experience Cloud, is het vaak nuttig of zelfs noodzakelijk om Analytics "het Volgen Server"te kennen die u gebruikt, of ook de "Reeks van het Rapport"die u gegevens naar verzendt. In deze video ziet u hoe u beide waarden kunt vinden, ongeacht of u Adobe Analytics al hebt geïmplementeerd.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer, Data Engineer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 42bf16df9585d1f41206b81bf509a72c10f1d7f2
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 2%

---

# Hoe kan ik uw analysemogelijkheden identificeren? [!DNL tracking server] en [!UICONTROL report suite ID] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Wanneer u Adobe Analytics instelt of wanneer u ernaar verwijst in andere oplossingen voor Experiencen Cloud, is het vaak handig of zelfs noodzakelijk om te weten welke Analytics &quot;tracking server&quot; u gebruikt, of &quot;[!UICONTROL report suite]&quot; die u gegevens naar verzendt. In deze video ziet u hoe u beide waarden kunt vinden, ongeacht of u Adobe Analytics al hebt geïmplementeerd.

>[!IMPORTANT]
>
>Dit artikel en de video zijn op een &quot;AppMeasurement&quot;implementatie van Adobe Analytics, en niet een implementatie van toepassing gebruikend het Web SDK van toepassing.

## Na de implementatie {#after-implementation}

Na het implementeren van Analytics op een site kunt u de [!DNL tracking server] en de [!DNL report suite ID] in het trackingbaken. De [!DNL tracking server] is hostname in het baken, zodat is dat gemakkelijk te vinden. De [!UICONTROL report suite] IDs is een komma-gescheiden lijst recht na &quot;/b/ss/&quot; in de wegnaam van het baken.

Om het baken, evenals alle andere informatie te zien die aan Analytics en andere oplossingen van het Experience Cloud komt, installeer [Chrome-extensie &quot;Experience Cloud Debugger&quot;](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=nl).

## Voor implementatie {#before-implementation}

**[!DNL Tracking server]** - Als u nog niet bent begonnen met uw Adobe Analytics-implementatie, kiest u een subdomein voor &quot;.sc.omtr dc.net&quot; [!DNL tracking server]. Bijvoorbeeld, laten we zeggen dat ik een online hoesje heb genaamd &quot;Jim&#39;s Brims.&quot; Ik kan mijn [!DNL tracking server] tot:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Report suite]** - Een lijst met uw [!UICONTROL report suites] die zijn gemaakt, meldt u zich aan bij [!DNL Analytics] en ga naar [!UICONTROL Admin] > [!UICONTROL Report Suites] in het bovenste menu om een lijst met [!UICONTROL report suites], inclusief hun id en titel.

Bekijk de video hieronder voor meer informatie.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12&learn=on)
