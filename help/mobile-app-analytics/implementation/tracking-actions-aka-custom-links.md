---
title: Handelingen bijhouden (aangepaste AKA-koppelingen) in een mobiele app met de SDK van het Experience Platform
description: 'Acties zijn gebeurtenissen die in uw mobiele app voorkomen. In deze video leert u hoe u de API trackAction kunt gebruiken om een handeling bij te houden en te meten. '
feature: Mobile SDK
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Mobile
role: '"Developer, Data Engineer"'
level: Ervaren
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Handelingen bijhouden (aangepaste AKA-koppelingen) in een mobiele toepassing met de SDK van het Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Acties zijn gebeurtenissen die in uw mobiele app voorkomen. In deze video leert u hoe u de API trackAction kunt gebruiken om een handeling bij te houden en te meten.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

Dit is de API die u moet gebruiken om alle handelingen te volgen die niet op het scherm worden geladen. Als het scherm omhoog komt, dan gebruik trackState, die een klap van de paginamening teweegbrengt. Anders gebruikt u trackAction om variabelen te verzenden die zijn gekoppeld aan de handeling die plaatsvindt.

Deze gegevens worden ingevoerd als `contextData`, wat ook betekent dat u [!UICONTROL Processing Rules] zult moeten gebruiken om de mobiele gegevens van die `contextData` variabelen te nemen en het in [!DNL eVars], [!DNL Props], Gebeurtenissen, enz. in kaart te brengen. in Adobe Analytics.

Raadpleeg de [documentatie](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference) voor meer informatie over trackAction.
