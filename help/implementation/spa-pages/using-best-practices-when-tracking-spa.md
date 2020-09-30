---
title: 'Het gebruiken van Beste praktijken wanneer het Volgen van de Toepassingen van de Enige Pagina (SPA) in Adobe Analytics '
description: In dit document, zullen wij verscheidene beste praktijken beschrijven die u zou moeten volgen en zich van bewust zijn aangezien u Adobe Analytics gebruikt om de Toepassingen van de Enige Pagina (SPA) te volgen. Dit document zal zich op het gebruiken van Experience Platform Launch concentreren, dat de geadviseerde implementatiemethode is.
feature: implementation basics
topics: spa
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
translation-type: tm+mt
source-git-commit: 548ac75589383dfd4da4ae02412de91a0a3b28d6
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 0%

---


# Het gebruiken van Beste praktijken wanneer het Volgen van de Toepassingen van de Enige Pagina (SPA) in Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

In dit document, zullen wij verscheidene beste praktijken beschrijven die u zou moeten volgen en zich van bewust zijn aangezien u Adobe Analytics gebruikt om de Toepassingen van de Enige Pagina (SPA) te volgen. Dit document zal zich op het gebruiken van Adobe concentreren [!DNL Experience Platform Launch], die de geadviseerde implementatiemethode is.

EERSTE OPMERKINGEN:

* Bij de onderstaande items wordt ervan uitgegaan dat u gebruikt [!DNL Experience Platform Launch] om deze te implementeren op uw site. De overwegingen zouden nog bestaan als u niet gebruikt, [!DNL Experience Platform Launch]maar u zou hen aan uw implementatiemethode moeten aanpassen.
* Alle SPAs zijn verschillend, zodat kunt u enkele volgende punten moeten aanpassen om aan uw behoefte het best te voldoen, maar wij wilden sommige beste praktijken met u delen; dingen die u over moet denken aangezien u Adobe Analytics op SPA pagina&#39;s implementeert.

## Eenvoudig diagram van het werken met SPAs in [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![spa voor analyse in lancering](assets/spa_for_analyticsinlaunch.png)

**OPMERKING:** Zoals verklaard, is dit een vereenvoudigd diagram van hoe de pagina&#39;s van het KUUROORD in een implementatie van Adobe Analytics gebruikend worden behandeld [!DNL Experience Platform Launch]. In de volgende secties van deze pagina zullen we de stappen en eventuele problemen bespreken die u zorgvuldig moet overwegen of aanpakken.

## De gegevenslaag instellen {#setting-the-data-layer}

Wanneer de nieuwe inhoud op een pagina van het KUUROORD wordt geladen, of wanneer een actie op een pagina van het KUUROORD plaatsvindt, één van de eerste dingen u zou moeten doen is de gegevenslaag bij te werken. Dit moet gebeuren VOORDAT de aangepaste gebeurtenis wordt geactiveerd en regels worden geactiveerd [!DNL Experience Platform Launch][!DNL Experience Platform Launch] , zodat de nieuwe waarden uit de gegevenslaag kunnen worden opgehaald en in Adobe Analytics kunnen worden geplaatst.

Na is een laag van steekproefgegevens, waarvan de elementen op meningsverandering of actie op uw SPA konden worden veranderd. Bij een schermwijziging met volledige/meerderheid zou het bijvoorbeeld gebruikelijk zijn om een &quot;[!DNL pageName]&quot;-element te wijzigen, zodat de nieuwe kan worden vastgelegd in [!DNL Experience Platform Launch] en verzonden naar Adobe Analytics.

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

## Aangepaste gebeurtenissen en luisteren instellen in [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Wanneer nieuwe inhoud op de pagina wordt geladen, of wanneer een actie op de site plaatsvindt, zult u op de hoogte willen brengen [!DNL Experience Platform Launch] zodat deze een regel kan uitvoeren en gegevens kan verzenden naar [!DNL Analytics]. Er zijn een paar verschillende manieren om dit te doen: [!UICONTROL Direct Call] [!UICONTROL rules] of Aangepaste gebeurtenissen.

* [!UICONTROL Direct Call] [!UICONTROL Rules]: in [!DNL Experience Platform Launch], kunt u opstelling een [!UICONTROL direct call] [!UICONTROL rule] die uitvoert wanneer het direct van de pagina wordt geroepen. Als het laden van de pagina of de handeling op uw site heel eenvoudig is, of als deze uniek is en elke keer een specifieke set instructies kan uitvoeren (elke keer [!DNL eVar4] op X wordt ingesteld en [!DNL event2] wordt geactiveerd), kunt u een [!UICONTROL direct call] [!UICONTROL rule]instructie gebruiken. Zie [!DNL Experience Platform Launch] documentatie over het maken van [!UICONTROL direct call] bestanden [!UICONTROL rules].
* Aangepaste gebeurtenissen: Voor meer functionaliteit, en voor de capaciteit om een lading met verschillende waarden dynamisch vast te maken, zou u douanegebeurtenissen JavaScript moeten plaatsen en naar hen binnen luisteren [!DNL Experience Platform Launch], waar u de nuttige lading kunt gebruiken om variabelen te plaatsen en de gegevens naar Adobe Analytics te verzenden. Het is waarschijnlijker dat u deze functionaliteit nodig zult hebben, en daarom wordt deze optie beschouwd als beste praktijken. Elke functie op uw site kan echter bepalen welke methode het meest geschikt is. We gaan in dit document verder, ervan uitgaande dat u deze methode voor aangepaste gebeurtenissen moet gebruiken.

**Voorbeelden:** In [DIT](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) hulpdocument, zijn er verbindingen aan de plaatsen van steekproefSPA die [!DNL Analytics] (en andere oplossingen van Experience Cloud) hebben uitgevoerd, evenals documenten beschrijvend wat is uitgevoerd. In deze voorbeelden van SPA, zijn de volgende douanegebeurtenissen gebruikt:

* [!DNL event-view-start]: Deze gebeurtenis moet worden uitgevoerd wanneer de weergave start van de weergave of status die wordt geladen.
* [!DNL event-view-end]: Deze gebeurtenis zou moeten in brand worden gestoken zelfs wanneer een mening/een staatsverandering is voorgekomen en alle componenten van het KUUROORD op de pagina klaar zijn met laden. Dit is de gebeurtenis die typisch een vraag in Adobe Analytics teweegbrengt.
* [!DNL event-action-trigger]: Deze gebeurtenis moet worden gestart wanneer er gebeurtenissen op de pagina plaatsvinden, behalve het laden van de weergave of status. Dit kan een klikgebeurtenis zijn of een kleinere inhoudsverandering zonder een meningsverandering.

Zie de pagina&#39;s/documenten waarnaar hierboven wordt verwezen voor meer informatie over hoe en wanneer deze worden geactiveerd. U hoeft niet dezelfde gebeurtenisnamen te gebruiken, maar de hier vermelde functionaliteit wordt aanbevolen. In de volgende video wordt een voorbeeldsite weergegeven en wordt aangegeven waar wordt geluisterd [!DNL Experience Platform Launch] naar aangepaste gebeurtenissen.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## s.t() of s.tl() uitvoeren in de [!DNL Experience Platform Launch] [!UICONTROL Rule] {#running-s-t-or-s-tl-in-the-launch-rule}

Één van de belangrijkste dingen te begrijpen voor [!DNL Analytics] wanneer het werken met een SPA is het verschil tussen `s.t()` en `s.tl()`. U zult één van deze methodes in werking stellen [!DNL Experience Platform Launch] om gegevens naar te verzenden [!DNL Analytics], maar u moet weten wanneer om elk te verzenden.

* **s.t()** - De &#39;t&#39; staat voor &#39;track&#39; en is een normale paginaweergave. Wijzig de weergave, ook al verandert de URL niet, zo dat u deze als een nieuwe &quot;pagina&quot; zou *beschouwen* ? Als dat het geval is, stelt u de s in.[!DNL pageName] variabele en gebruik `s.t()` om de vraag te verzenden [!DNL Analytics]

* **s.tl()** - De &quot;tl&quot; staat voor &quot;trackkoppeling&quot; en wordt gewoonlijk gebruikt voor het bijhouden van klikken of kleine wijzigingen in de inhoud op de pagina, in tegenstelling tot een volledige schermwijziging. Als de wijziging op de pagina klein is, zodat u deze niet als een volledige nieuwe &quot;pagina&quot; wilt beschouwen, gebruikt u de variabele s.pageName `s.tl()` en maakt u zich er geen zorgen over dat deze wordt ingesteld, omdat [!DNL Analytics] deze anders wordt genegeerd.

**TIP:** Sommige gebruikers gebruiken een algemene richtlijn die bepaalt dat als het scherm meer dan 50% verandert, het als paginaweergave en gebruik moet worden beschouwd `s.t()`. Als de afbeelding voor minder dan 50% op het scherm wordt weergegeven, gebruikt u `s.tl()`. Het is echter volledig aan u en wat u als een nieuwe &quot;pagina&quot;beschouwt en hoe u uw plaats in Adobe Analytics wilt volgen.

De volgende video laat zien waar/hoe u kunt activeren `s.t()` of `s.tl()` in Launch by Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Variabelen wissen {#clearing-variables}

Wanneer u uw site met Adobe Analytics bijhoudt, wilt u natuurlijk alleen de juiste gegevens op het juiste moment [!DNL Analytics] naar sturen. In een milieu van het KUUROORD, kan een waarde die in een [!DNL Analytics] variabele wordt gevolgd voortbestaan en opnieuw worden verzonden naar [!DNL Analytics], potentieel wanneer wij het niet meer willen. Daarom is er een functie in de [!DNL Analytics][!DNL Launch] extensie om de variabelen te wissen, zodat u een nieuwe status krijgt wanneer u de volgende afbeeldingsaanvraag uitvoert en gegevens verzendt naar [!DNL Analytics].

In het diagram hierboven, hebben wij het vermeld aan het eind van het proces, ontruimend de variabelen *nadat* u in de slag verzendt. In werkelijkheid kan het of vóór OF nadat de treffer wordt verzonden binnen worden gedaan, maar zou in uw [!DNL Experience Platform Launch] regels consequent moeten zijn, zodat u altijd of voor of na het plaatsen van variabelen en het verzenden van hen binnen ontruimt. Herinner me, als u de variabelen gaat ontruimen *alvorens* u in werking stelt `s.t()`, zorg ervoor dat u eerst de variabelen ontruimt, dan de nieuwe variabelen plaatst, en dan definitief de nieuwe gegevens verzendt naar [!DNL Analytics].

**OPMERKING:** Het wissen van variabelen is niet altijd nodig bij het uitvoeren `s.tl()`, omdat `s.tl()` het gebruik van de [!DNL linkTrackVars] variabele naast de variabele elke keer vereist om te bepalen [!DNL Analytics] welke variabelen worden geplaatst (automatisch toegevoegd achter de scènes in [!DNL Experience Platform Launch]). Dit betekent dat foutvariabelen meestal niet worden weergegeven wanneer ze worden gebruikt, `s.tl()`maar dat dit zeer wordt aanbevolen bij gebruik `s.t()` in een SPA-omgeving. Al dat wordt gezegd, zou ik het als beste praktijk willen aanbevelen om de Duidelijke functie van Variabelen voor zowel `s.t()` als `s.tl()` in een milieu van het KUUROORD te gebruiken, enkel om kwaliteitsgegevensinzameling te verzekeren.

In de volgende video ziet u waar/hoe u de variabelen in kunt wissen [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Aanvullende overwegingen {#additional-considerations}

### Aangepaste codevensters in [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

In de [!DNL Launch][!DNL Analytics] extensie zijn er twee plaatsen waar u aangepaste code kunt invoegen: De [!UICONTROL library management] sectie en de extra sectie &quot;[!UICONTROL Configure Tracker Using Custom Code]&quot;.

![Aangepaste venster Analyse starten](assets/launch_analyticscustomcodewindows.png)

Het is belangrijk om te weten dat één van beide plaatsen werkelijk slechts de code in hen één keer gaat in werking stellen, wanneer de aanvankelijke paginading op uw pagina van het KUUROORD gebeurt. Als de code moet worden uitgevoerd op een wijziging van de weergave of op een actie op uw site, moet u een aanvullende actie toevoegen aan de betreffende code **[!UICONTROL rule]** (bijvoorbeeld in het laden van de pagina: event-view-end&quot; [!UICONTROL rule]), zodat de code elke keer wordt uitgevoerd dat [!UICONTROL rule] loopt. Wanneer u die handeling maakt in de [!UICONTROL rule], stelt u *Extensie = Core* en *Action Type = Custom Code* in.

### &quot;Hybride&quot; SPA/Reguliere sites {#hybrid-spa-regular-sites}

Sommige plaatsen zijn een combinatie &quot;regelmatige&quot;pagina&#39;s en de pagina&#39;s van het KUUROORD. In dit geval, zult u een strategie moeten gebruiken die voor beide paginatypen werkt. Wanneer u uw aangepaste gebeurtenissen op de site configureert en de regels in activeert, moet u ervoor zorgen dat er geen dubbele hits [!DNL Experience Platform Launch][!DNL Analytics] vanaf de pagina verschijnen, gebaseerd op wijzigingen in de hash, enz. (als u zo hebt gekozen om de [!DNL Experience Platform Launch] regel te activeren). In dit geval moet u een van de paginaweergaven onderdrukken, zodat u geen onjuiste gegevens krijgt in Adobe Analytics.

Als u besluit om de functionaliteit in afzonderlijke onderdelen te verdelen [!UICONTROL rules] zodat u meer controle over het hebt, moet u niet vergeten/documenteren dat u dit hebt gedaan, zodat eventuele wijzigingen in het ene onderdeel [!UICONTROL rule] ook in het andere [!UICONTROL rule] kunnen worden aangebracht, zodat de [!DNL Analytics] gegevensintegriteit wordt beschermd.

### Integratie met [!DNL Target] via A4T {#integration-with-target-via-a4t}

Een korte callout hier. Als u met het [!DNL Target] gebruiken van A4T integreert, zorg ervoor dat het [!DNL Target] verzoek en het [!DNL Analytics] verzoek op de zelfde meningsverandering zelfde SDID hebben. Hierdoor worden uw gegevens op de juiste wijze gesynchroniseerd op de oplossingen.

Om de klappen te zien, gebruik debugger of pakketsniffer programma. U kunt ook de Experience Cloud Debugger gebruiken, een Chrome-extensie die [HIER](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj)kan worden gedownload. [!DNL Target] moet eerst op de pagina worden geactiveerd, zodat u dat ook kunt controleren in de JavaScript-console of het foutopsporingsprogramma.

## Aanvullende resources {#additional-resources}

* [Bespreking van de SPA op de forums van Adobe](https://forums.adobe.com/thread/2451022)
* [De plaatsen van de Architectuur van de verwijzing om te tonen hoe te om SPA in Experience Platform Launch uit te voeren](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)