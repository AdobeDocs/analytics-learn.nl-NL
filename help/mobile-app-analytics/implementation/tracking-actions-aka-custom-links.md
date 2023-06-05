---
title: Handelingen bijhouden (aangepaste AKA-koppelingen) in een mobiele app met de SDK van het Experience Platform
description: Acties zijn gebeurtenissen die in uw mobiele app voorkomen. In deze video leert u hoe u de API trackAction kunt gebruiken om een handeling bij te houden en te meten.
feature: Mobile SDK
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Mobile
role: Developer, Data Engineer
level: Experienced
exl-id: 541c51b8-638e-43b4-90ac-0ce94290a141
source-git-commit: 4d467928756950074620388645523021b21fb0d5
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# Handelingen bijhouden (aangepaste AKA-koppelingen) in een mobiele app met de SDK van het Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Acties zijn gebeurtenissen die in uw mobiele app voorkomen. In deze video leert u hoe u de API trackAction kunt gebruiken om een handeling bij te houden en te meten.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12&learn=on)

Dit is de API die u moet gebruiken om alle handelingen te volgen die niet op het scherm worden geladen. Als het scherm omhoog komt, dan gebruik trackState, die een klap van de paginamening teweegbrengt. Anders gebruikt u trackAction om variabelen te verzenden die zijn gekoppeld aan de handeling die plaatsvindt.

Deze gegevens worden weergegeven als `contextData`, wat ook betekent dat u dan zult moeten gebruiken [!UICONTROL Processing Rules] om de mobiele gegevens van `contextData` variabelen en toewijzen in [!DNL eVars], [!DNL Props], Gebeurtenissen, enz. in Adobe Analytics.

Voor meer informatie over trackAction raadpleegt u de [documentatie](https://developer.adobe.com/client-sdks/documentation/getting-started/track-events/#track-user-actions-for-adobe-analytics).
