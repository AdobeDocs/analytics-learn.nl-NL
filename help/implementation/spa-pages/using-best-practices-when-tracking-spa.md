---
title: 'Best practices gebruiken bij het bijhouden van toepassingen voor één pagina (SPA) in Adobe Analytics '
description: In dit document worden verschillende aanbevolen procedures beschreven die u moet volgen en waarvan u weet dat u Adobe Analytics gebruikt om toepassingen voor één pagina (SPA) bij te houden. Dit document zal zich op het gebruiken van Experience Platform Launch concentreren, dat de geadviseerde implementatiemethode is.
feature: Implementation Basics
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: "Developer, Data Engineer"
level: Intermediate
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '1646'
ht-degree: 0%

---


# Best practices gebruiken bij het bijhouden van toepassingen voor één pagina (SPA) in Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

In dit document worden verschillende aanbevolen procedures beschreven die u moet volgen en waarvan u weet dat u Adobe Analytics gebruikt om toepassingen voor één pagina (SPA) bij te houden. Dit document zal zich op het gebruiken van Adobe [!DNL Experience Platform Launch] concentreren, die de geadviseerde implementatiemethode is.

EERSTE OPMERKINGEN:

* Bij de onderstaande items wordt ervan uitgegaan dat u [!DNL Experience Platform Launch] gebruikt om te implementeren op uw site. De overwegingen zouden nog bestaan als u [!DNL Experience Platform Launch] niet gebruikt, maar u zou hen aan uw implementatiemethode moeten aanpassen.
* Alle SPA zijn verschillend, zodat kunt u sommige volgende punten moeten aanpassen om aan uw behoefte te voldoen, maar wij wilden sommige beste praktijken met u delen; dingen waar je over moet nadenken terwijl je Adobe Analytics implementeert op SPA pagina&#39;s.

## Eenvoudig diagram van het werken met SPA in [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![spa voor analyse in lancering](assets/spa_for_analyticsinlaunch.png)

**NOTA:** Zoals vermeld, is dit een vereenvoudigd diagram van hoe SPA pagina&#39;s in een implementatie van Adobe Analytics gebruikend worden behandeld  [!DNL Experience Platform Launch]. In de volgende secties van deze pagina zullen we de stappen en eventuele problemen bespreken die u zorgvuldig moet overwegen of aanpakken.

## De gegevenslaag {#setting-the-data-layer} instellen

Wanneer nieuwe inhoud op een SPA pagina wordt geladen, of wanneer een actie op een SPA pagina plaatsvindt, één van de eerste dingen u zou moeten doen is de gegevenslaag bijwerken. Dit moet gebeuren VOORDAT de aangepaste gebeurtenis wordt geactiveerd en regels worden geactiveerd in [!DNL Experience Platform Launch], zodat [!DNL Experience Platform Launch] de nieuwe waarden kan ophalen uit de gegevenslaag en deze naar Adobe Analytics kan duwen.

Hieronder volgt een voorbeeldgegevenslaag, waarvan de elementen kunnen worden gewijzigd bij het wijzigen van de weergave of bij actie op de SPA. Op een volledig scherm/meerderheidswijziging zou het bijvoorbeeld gebruikelijk zijn om een element &quot;[!DNL pageName]&quot; te wijzigen, zodat de nieuwe kan worden vastgelegd in [!DNL Experience Platform Launch] en naar Adobe Analytics kan worden verzonden.

```JavaScript
<script>
    digitalData = {
        pageInstanceID: "Launch Demo Site",
        page:{
            pageInfo:{
                pageID: '2745374',
                pageName: 'acs demo - product listing page'
            },
            attributes:{
                project: "Experience Platform Launch Project"
            }
        },
        user : [ {
          "profile" : [ {
            "attributes" : {
              "gender" : "male",
              "age" : "35"
            }
          } ]
        }],
        libraries : {
          adobe : {
            launch : {
              state : 0, // 0 = not loaded , 1 = loaded
              domain : "assets.adobedtm.com"
            }
          }
        }

     };
    </script>
```

## Aangepaste gebeurtenissen instellen en luisteren in [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Wanneer nieuwe inhoud op de pagina wordt geladen, of wanneer een actie op de site plaatsvindt, wilt u [!DNL Experience Platform Launch] op de hoogte brengen zodat deze een regel kan uitvoeren en gegevens kan verzenden naar [!DNL Analytics]. Er zijn een paar verschillende manieren om dit te doen: [!UICONTROL Direct Call] [!UICONTROL rules] of Aangepaste gebeurtenissen.

* [!UICONTROL Direct Call] [!UICONTROL Rules]: in  [!DNL Experience Platform Launch], kunt u opstelling een  [!UICONTROL direct call] [!UICONTROL rule] die uitvoert wanneer het direct van de pagina wordt geroepen. Als het laden van de pagina of de handeling op uw site heel eenvoudig is, of als deze uniek is en elke keer een specifieke set instructies kan uitvoeren (stel [!DNL eVar4] in op X en activeer [!DNL event2] elke keer), kunt u een [!UICONTROL direct call] [!UICONTROL rule] gebruiken. Zie [!DNL Experience Platform Launch] documentatie betreffende het maken van [!UICONTROL direct call] [!UICONTROL rules].
* Aangepaste gebeurtenissen: Voor meer functionaliteit, en voor de capaciteit om een lading met verschillende waarden dynamisch vast te maken, zou u douanegebeurtenissen JavaScript moeten plaatsen en naar hen in [!DNL Experience Platform Launch] luisteren, waar u de lading kunt gebruiken om variabelen te plaatsen en de gegevens naar Adobe Analytics te verzenden. Het is waarschijnlijker dat u deze functionaliteit nodig zult hebben, en daarom wordt deze optie beschouwd als beste praktijken. Elke functie op uw site kan echter bepalen welke methode het meest geschikt is. We gaan in dit document verder, ervan uitgaande dat u deze methode voor aangepaste gebeurtenissen moet gebruiken.

**Voorbeelden:** In  [](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) document THISHelp, zijn er verbindingen aan steekproef SPA plaatsen die  [!DNL Analytics] (en andere oplossingen van Experience Cloud) hebben uitgevoerd, evenals documenten beschrijvend wat is uitgevoerd. In deze SPA zijn de volgende aangepaste gebeurtenissen gebruikt:

* [!DNL event-view-start]: Deze gebeurtenis moet worden uitgevoerd wanneer de weergave start van de weergave of status die wordt geladen.
* [!DNL event-view-end]: Deze gebeurtenis moet ook worden geactiveerd wanneer een weergave-/statuswijziging heeft plaatsgevonden en alle SPA componenten op de pagina klaar zijn met laden. Dit is de gebeurtenis die typisch een vraag in Adobe Analytics teweegbrengt.
* [!DNL event-action-trigger]: Deze gebeurtenis moet worden gestart wanneer er gebeurtenissen op de pagina plaatsvinden, behalve het laden van de weergave of status. Dit kan een klikgebeurtenis zijn of een kleinere inhoudsverandering zonder een meningsverandering.

Zie de pagina&#39;s/documenten waarnaar hierboven wordt verwezen voor meer informatie over hoe en wanneer deze worden geactiveerd. U hoeft niet dezelfde gebeurtenisnamen te gebruiken, maar de hier vermelde functionaliteit wordt aanbevolen. In de volgende video wordt een voorbeeldsite weergegeven en wordt aangegeven waar [!DNL Experience Platform Launch] zich bevindt om te luisteren naar aangepaste gebeurtenissen.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## s.t() of s.tl() uitvoeren in [!DNL Experience Platform Launch] [!UICONTROL Rule] {#running-s-t-or-s-tl-in-the-launch-rule}

Een van de belangrijkste dingen die [!DNL Analytics] moet begrijpen wanneer u met een SPA werkt, is het verschil tussen `s.t()` en `s.tl()`. U zult één van deze methodes in [!DNL Experience Platform Launch] teweegbrengen om gegevens naar [!DNL Analytics] te verzenden, maar u moet weten wanneer om elke te verzenden.

* **s.t()** - De &#39;t&#39; staat voor &#39;track&#39; en is een normale paginaweergave. Hoewel URL niet kan veranderen, verandert de mening genoeg dat u *zou overwegen* het een nieuwe &quot;pagina&quot;zou? Als zo, plaats s.[!DNL pageName] veranderlijk en gebruik `s.t()` om de vraag in [!DNL Analytics] te verzenden

* **s.tl()** - De &quot;tl&quot; staat voor &quot;trackkoppeling&quot; en wordt gewoonlijk gebruikt voor het bijhouden van klikken of kleine wijzigingen in de inhoud op de pagina, in tegenstelling tot een volledige schermwijziging. Als de wijziging op de pagina klein is, zodat u deze niet als een volledige nieuwe pagina wilt beschouwen, gebruikt u `s.tl()` en maakt u zich geen zorgen over het instellen van de variabele s.pageName, aangezien [!DNL Analytics] deze zal negeren.

**TIP:** Sommige mensen gebruiken een algemene richtlijn die bepaalt dat als het scherm meer dan 50% verandert, het als paginaweergave en gebruik moet worden beschouwd  `s.t()`. Als het minder dan 50% van verandering in het scherm is, gebruik `s.tl()`. Het is echter volledig aan u en wat u als een nieuwe &quot;pagina&quot;beschouwt en hoe u uw plaats in Adobe Analytics wilt volgen.

De volgende video laat zien waar/hoe `s.t()` of `s.tl()` in Launch by Adobe moet worden geactiveerd.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Variabelen {#clearing-variables} wissen

Wanneer u uw site met Adobe Analytics bijhoudt, wilt u natuurlijk alleen de juiste gegevens op het juiste moment naar [!DNL Analytics] sturen. In een SPA milieu, kan een waarde die in een [!DNL Analytics] variabele wordt gevolgd voortbestaan en opnieuw worden verzonden naar [!DNL Analytics], potentieel wanneer wij het niet meer willen. Daarom is er een functie in [!DNL Analytics] [!DNL Launch] uitbreiding om de variabelen te ontruimen, zodat u een nieuwe leisteen hebt wanneer u het volgende beeldverzoek in werking stelt en gegevens naar [!DNL Analytics] verzendt.

In het diagram hierboven, hebben wij het vermeld aan het eind van het proces, ontruimend de variabelen *after* u in de slag verzendt. In werkelijkheid kan het of vóór OF worden gedaan nadat de slag wordt verzonden binnen, maar zou in uw [!DNL Experience Platform Launch] regels moeten consistent zijn, zodat u altijd of voor of na het plaatsen van variabelen en het verzenden van hen binnen ontruimen. Herinner me, als u de variabelen *before* gaat ontruimen u `s.t()` in werking stelt, zorg ervoor dat u eerst de variabelen ontruimt, dan de nieuwe variabelen plaatst, en dan definitief de nieuwe gegevens naar [!DNL Analytics] verzendt.

**NOTA:** Het ontruimen van variabelen is niet altijd nodig wanneer het lopen  `s.tl()`, omdat  `s.tl()` het gebruik van de  [!DNL linkTrackVars] variabele naast het vereist telkens om te vertellen  [!DNL Analytics] welke variabelen zullen worden geplaatst (automatisch toegevoegd achter de scènes in  [!DNL Experience Platform Launch]). Dit betekent dat foutvariabelen meestal niet worden weergegeven wanneer u `s.tl()` gebruikt, maar het wordt sterk aanbevolen wanneer u `s.t()` in een SPA omgeving gebruikt. Dit alles gezegd hebbende, zou ik het als beste praktijk willen adviseren om de Duidelijke functie van Variabelen voor zowel `s.t()` als `s.tl()` in een SPA milieu te gebruiken, enkel om kwaliteitsgegevensinzameling te verzekeren.

In de volgende video ziet u waar/hoe u de variabelen in [!DNL Launch] wist.

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Aanvullende overwegingen {#additional-considerations}

### Aangepaste codevensters in [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

In de [!DNL Launch] [!DNL Analytics] uitbreiding, zijn er twee plaatsen waar u douanecode kunt opnemen: De sectie [!UICONTROL library management] en de extra sectie &quot;[!UICONTROL Configure Tracker Using Custom Code]&quot;.

![Aangepaste venster Analyse starten](assets/launch_analyticscustomcodewindows.png)

Het is belangrijk om te weten dat één van beide plaatsen werkelijk slechts de code in hen zal in werking stellen eens, wanneer de aanvankelijke paginading op uw SPA pagina gebeurt. Als de code moet worden uitgevoerd op een wijziging van de weergave of op een actie op uw site, moet u een extra handeling toevoegen aan de betreffende **[!UICONTROL rule]** (bijvoorbeeld in het item &quot;page load: event-view-end&quot; [!UICONTROL rule]), zodat de code elke keer wordt uitgevoerd dat [!UICONTROL rule] loopt. Wanneer u die handeling maakt in de [!UICONTROL rule], stelt u *Extension = Core* en *Action Type = Custom Code* in.

### &quot;Hybride&quot; SPA/Reguliere sites {#hybrid-spa-regular-sites}

Sommige sites bestaan uit een combinatie van &quot;gewone&quot; pagina&#39;s en SPA pagina&#39;s. In dit geval, zult u een strategie moeten gebruiken die voor beide paginatypen werkt. Wanneer u uw aangepaste gebeurtenissen op de site configureert en de regels in [!DNL Experience Platform Launch] activeert, moet u ervoor zorgen dat er geen dubbele treffers vanuit de pagina naar [!DNL Analytics] gaan, gebaseerd op wijzigingen in de hash, enz. (als dat is hoe u ervoor hebt gekozen om de [!DNL Experience Platform Launch] regel teweeg te brengen). In dit geval moet u een van de paginaweergaven onderdrukken, zodat u geen onjuiste gegevens krijgt in Adobe Analytics.

Als u besluit om de functionaliteit in afzonderlijke [!UICONTROL rules] uit te breken zodat u meer controle over het hebt, ben zeker om te herinneren/document dat u dit hebt gedaan, zodat om het even welke veranderingen in één [!UICONTROL rule] ook aan andere [!UICONTROL rule] kunnen worden aangebracht, die uw [!DNL Analytics] gegevensintegriteit beschermen.

### Integratie met [!DNL Target] via A4T {#integration-with-target-via-a4t}

Een korte callout hier. Als u met [!DNL Target] gebruikend A4T integreert, zorg ervoor dat [!DNL Target] verzoek en [!DNL Analytics] verzoek op de zelfde meningsverandering zelfde SDID hebben. Hierdoor worden uw gegevens op de juiste wijze gesynchroniseerd op de oplossingen.

Om de klappen te zien, gebruik debugger of pakketsniffer programma. U kunt ook de Experience Cloud Debugger gebruiken, een Chrome-extensie die [HERE](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj) kan worden gedownload. [!DNL Target] moet eerst op de pagina worden geactiveerd, zodat u dat ook kunt controleren in de JavaScript-console of het foutopsporingsprogramma.

## Aanvullende resources {#additional-resources}

* [SPA discussie over de forums van de Adobe](https://forums.adobe.com/thread/2451022)
* [Referentie Architectuur plaatsen om te tonen hoe te om SPA in Experience Platform Launch uit te voeren](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)