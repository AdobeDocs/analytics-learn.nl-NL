---
title: Een gegevenslaag gebruiken om analytische variabelen in te stellen via labels
description: Leer over het gebruiken van een gegevenslaag voor het betrekken van de gegevens van de Analyse en andere oplossingen van Experience Cloud.
feature: Launch Implementation
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Een gegevenslaag gebruiken om analytische variabelen in te stellen via [!DNL Tags] {#use-a-data-layer-to-set-analytics-variables-in-adobe-analytics-via-tags}

Een gegevenslaag gebruiken voor [!DNL Analytics] en andere Experience Cloud oplossingen zijn een goede praktijk . Leer in deze video hoe u waarden uit de gegevenslaag kunt trekken en deze kunt gebruiken in [!DNL Experience Platform Tags] om variabelen te vullen in Adobe Analytics.

## Gegevenslagen {#data-layers}

A _gegevenslaag_ is een framework van JavaScript-objecten dat ontwikkelaars toevoegen aan digitale webpagina&#39;s. De oplossingen van de analyse gebruiken uiteindelijk de gegevenslaag om rapporten te bevolken. Tagbeheersystemen, waaronder [!DNL Experience Platform Tags]) zijn de tussenpersonen die de gegevenslaag lezen, de waarden aan variabelen in kaart brengen, en die gegevens naar digitale ervaringsoplossingen verzenden.

Aanvullende informatie over gegevenslagen in het dialoogvenster [Experience Cloud-documentatie](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=en) en de blog [Gegevenslagen: Van Buzzword naar aanbevolen procedures](https://blog.adobe.com/en/2014/03/13/data-layers-buzzword-best-practice).

## gegevenslagen, [!DNL Experience Platform Tags], en Adobe Analytics{#data-layers-launch-and-adobe-analytics}

1. Definieer of identificeer een standaard voor een gegevenslaag die u op uw site wilt gebruiken.

   1. Plaats de gegevenslaag zo hoog mogelijk in de hoofdsectie van de pagina en vóór de vraag aan [!DNL Experience Platform Tags]. Dit zorgt ervoor dat de waarden direct toegankelijk zijn via [!DNL Tags] en door Adobe oplossingen die hoog op de pagina moeten zijn, zoals Adobe Target.

1. Vul de gegevens in de gegevenslaag.
1. In [!DNL Experience Platform Tags], maakt u &quot;[!UICONTROL data elements]&quot; die de gegevenspunten in de gegevenslaag in kaart brengen. Deze gegevenselementen worden overal gebruikt [!DNL Experience Platform Tags] in [!UICONTROL rules] en [!UICONTROL extensions].
1. In beide [!DNL Analytics] algemene variabelen van extensie, sectie of in een [!DNL Tags rule], wijst u de waarden toe in [!UICONTROL data elements] tot [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName]en andere [!DNL Analytics] variabelen.
1. Trigger een baken dat de gegevens naar verzendt [!DNL Analytics].

De volgende video doorloopt u het proces.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)

>[!NOTE]
>
>De specifieke gegevenslaag die in deze video wordt gebruikt kan niet als &quot;beste praktijken&quot;voor uw organisatie worden beschouwd. Het gebruik van een gegevenslaag om belangrijke gegevens aan uw digitale marketingoplossingen te koppelen, is de beste manier.