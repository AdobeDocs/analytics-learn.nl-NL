---
title: Een gegevenslaag gebruiken om analytische variabelen in te stellen in Experience Platform [!DNL tags]
description: Leer hoe u een gegevenslaag gebruikt voor het aanschaffen van analysegegevens en andere oplossingen voor Experiencen Cloud.
feature: Tags
topics: Development
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: a45667a8d7ccb46b9e33bd11a78fac9714a61df5
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Een gegevenslaag gebruiken om analytische variabelen in te stellen in Experience Platform [!DNL tags]

Een gegevenslaag gebruiken voor [!DNL Analytics] en andere oplossingen voor Experiencen Cloud zijn een goede praktijk . Leer in deze video hoe u waarden uit de gegevenslaag kunt trekken en deze in het Experience Platform kunt gebruiken [!DNL tags] om variabelen te vullen in Adobe Analytics.

## Gegevenslagen

A _gegevenslaag_ is een framework van JavaScript-objecten dat ontwikkelaars toevoegen aan digitale webpagina&#39;s. Analyseoplossingen gebruiken uiteindelijk de gegevenslaag om rapporten te vullen. Tagbeheersystemen, inclusief Experience Platform [!DNL tags]) zijn de tussenpersonen die de gegevenslaag lezen, de waarden aan variabelen in kaart brengen, en die gegevens naar digitale ervaringsoplossingen verzenden.

Aanvullende informatie over gegevenslagen in het dialoogvenster [Documentatie Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=en).

## Gegevenslagen, Experience Platform [!DNL tags], en Adobe Analytics

1. Definieer of identificeer een standaard voor een gegevenslaag die u op uw site wilt gebruiken.

   1. Plaats de gegevenslaag zo hoog mogelijk in de hoofdsectie van de pagina en vóór de vraag aan Experience Platform [!DNL tags]. Dit zorgt ervoor dat de waarden direct toegankelijk zijn via [!DNL tags] en door oplossingen te Adoben die hoog op de pagina moeten zijn, zoals Adobe Target.

1. Vul de gegevens in de gegevenslaag.
1. In Experience Platform [!DNL tags], maakt u &quot;[!UICONTROL data elements]&quot; die de gegevenspunten in de gegevenslaag in kaart brengen. Deze gegevenselementen worden in het hele Experience Platform gebruikt [!DNL tags] in [!UICONTROL rules] en [!UICONTROL extensions].
1. In een van beide [!DNL Analytics] algemene variabelen van extensie, sectie of in een [!DNL Tags rule], wijst u de waarden toe in [!UICONTROL data elements] tot [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName]en andere [!DNL Analytics] variabelen.
1. Trigger een baken dat de gegevens naar verzendt [!DNL Analytics].

De volgende video doorloopt u het proces.

>[!NOTE]
>
> Starten is nu **[!DNL tags]**

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>De specifieke gegevenslaag die in deze video wordt gebruikt kan niet als &quot;beste praktijken&quot;voor uw organisatie worden beschouwd. Het gebruik van een gegevenslaag om belangrijke gegevens aan uw digitale marketingoplossingen te koppelen, is de beste manier.
