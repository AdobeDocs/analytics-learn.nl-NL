---
title: Aangepaste koppeling bijhouden zonder tagbeheer
description: Voor veel acties op de pagina, zou het volgen niet als een paginamening moeten worden behandeld. In deze video leert u hoe u een koppelingsmarkering kunt coderen naar Analytics als u geen tagbeheer gebruikt (zoals Experience Platform Launch). Zie de code en leer een belangrijke tip.
feature: Implementatie van toepassingen
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
role: Developer, Data Engineer
level: Intermediate
exl-id: e4567b1c-414e-44ad-982f-52b0150e7eda
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Aangepaste koppeling bijhouden zonder tagbeheer {#custom-link-tracking-without-a-tag-manager}

Voor veel acties op de pagina, zou het volgen niet als een paginamening moeten worden behandeld. In deze video leert u hoe u een koppelingsmarkering kunt coderen naar Analytics als u geen tagbeheer gebruikt (zoals Adobe [!DNL Experience Platform Launch]). Zie de code en leer een belangrijke tip.

## Een s.tl()-baken verzenden {#sending-an-s-tl-beacon}

Er zijn twee functies die gegevens naar Adobe Analytics verzenden:

1. s.t() - Een baken van het type &quot;track&quot;, dat een hit in de paginaweergave is, waardoor de paginaweergaven voor de opgegeven paginanaam toenemen en andere variabelen worden ingesteld
1. s.tl() - een &quot;track link&quot;-baken, dat vaak een &quot;aangepaste link&quot; hit/baken wordt genoemd, dat de paginaweergaven niet verhoogt en de pageName-variabele negeert. Dit wordt meestal gebruikt voor het bijhouden van kleinere handelingen op de pagina die geen nieuwe pagina/scherm laden, of andere handelingen die niet resulteren in een nieuwe pagina die wordt geladen.

>[!NOTE]
>
>In deze video tonen we u hoe u een aangepaste aanraakactie codeert wanneer u GEEN tagbeheer gebruikt, zoals Adobe [!DNL Experience Platform Launch]. Wij adviseren dat u [!DNL Experience Platform Launch], onze beste-praktijkaanbeveling voor implementatie gebruikt. Als u echter code wilt opnemen in een `s.tl()`, gaat u als volgt te werk.

>[!VIDEO](https://video.tv.adobe.com/v/25832/?quality=12)

## Voorbeeldcode {#sample-code}

Hier volgt de voorbeeldcode die wordt gebruikt voor de aangepaste koppeling in de video:

```JavaScript
<a href="#" onclick="
    s.linkTrackVars='events,eVar2,prop2';
    s.linkTrackEvents=s.events='event2';
    s.eVar2='facebook share';
    s.prop2='facebook share';
    s.tl(this,'o','Social Share');
    s.manageVars('clearVars',s.linkTrackVars,1);">
    Click here to share on FaceBook
</a>
```

Raadpleeg de [documentatie](https://marketing.adobe.com/resources/help/en_US/sc/implement/function_tl.html) voor meer informatie over aangepaste koppelingen.
