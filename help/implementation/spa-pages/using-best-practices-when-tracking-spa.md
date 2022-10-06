---
title: Aanbevolen werkwijzen voor implementatie van toepassingen voor één pagina (SPA)
description: Leer enkele tips en trucs voor het implementeren van Adobe Analytics op toepassingen voor één pagina (SPA). Dit omvat het gebruiken van de Markeringen van het Experience Platform, de geadviseerde implementatiemethode.
feature: Implementation Basics
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: Developer, Data Engineer
level: Intermediate
exl-id: 8fe63dd1-9629-437f-ae07-fe1c5a05fa42
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '1288'
ht-degree: 0%

---

# Aanbevolen werkwijzen voor implementatie van toepassingen voor één pagina (SPA) {#implementation-best-practices-for-single-page-appliations}

Leer enkele aanbevolen procedures voor het implementeren van [!DNL Adobe Analytics] op toepassingen voor één pagina (SPA). Dit omvat het gebruik van [!DNL Experience Platform Tags], de aanbevolen uitvoeringsmethode.

EERSTE OPMERKINGEN:

* De onderstaande inhoud verwijst naar het gebruik van [!DNL Experience Platform Tags] om Adobe Analytics op uw site te implementeren. Deze overwegingen zijn van toepassing als [!DNL Experience Platform Tags] wordt niet gebruikt, daarom moet u hen aan uw implementatiemethode aanpassen.
* Er zijn verschillen in SPA en daarom moet u uw aanpak aanpassen aan uw behoeften.

## Eenvoudig diagram van het werken met SPA in [!DNL Experience Platform Tags] {#simple-diagram-of-working-with-spas-in-tags}

![SPA voor analyses in labels](assets/spa_for_analyticsinlaunch.png)

**OPMERKING:** Dit is een vereenvoudigd diagram hoe SPA pagina&#39;s in een implementatie van Adobe Analytics worden behandeld gebruikend [!DNL Experience Platform Tags]. In de volgende secties worden de stappen en problemen beschreven die in overweging moeten worden genomen.

## Gegevenslaag instellen {#set-the-data-layer}

Wanneer nieuwe inhoud wordt geladen of wanneer een actie op een SPA pagina voorkomt, *de gegevenslaag eerst bijwerken*. Dat moet gebeuren **voor** een aangepaste gebeurtenis die een regel activeert, wordt uitgevoerd in [!DNL Experience Platform Tags]. Zo weet u zeker dat de juiste waarden uit de gegevenslaag naar Codes en vervolgens naar Adobe Analytics worden geduwd.

Hier volgt een voorbeeldgegevenslaag. Elk van deze elementen kan veranderen op basis van de openingsweergave of de volgende wijziging van de weergave op basis van een actie die op de SPA pagina is uitgevoerd. Bij een volledige of meerderheidswijziging is het bijvoorbeeld een algemene vereiste om een unieke waarde &quot;[!DNL pageName]&quot; waarde om onderscheid te maken tussen de weergaven in Adobe Analytics-rapportage.

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

## Stel aangepaste gebeurtenissen in en luister naar deze gebeurtenissen in [!DNL Experience Platform Tags] {#setting-custom-events-and-listening-in-tags}

Wanneer de nieuwe inhoud laadt of wanneer een actie op de SPA pagina voorkomt, moeten de Markeringen van het Experience Platform worden geïnformeerd om een regel in werking te stellen die gegevens verzendt naar [!DNL Analytics]. Hiervoor zijn een paar benaderingen: [!UICONTROL Direct Call rules] of Aangepaste gebeurtenissen.

* [!UICONTROL Direct Call rules]: Een [!UICONTROL direct call rule] die wordt uitgevoerd wanneer deze rechtstreeks vanaf de pagina wordt aangeroepen. Als het laden van de pagina of de handeling eenvoudig of uniek is en u kunt elke keer een specifieke set instructies uitvoeren (bijvoorbeeld [!DNL eVar4] naar X en activeren [!DNL event2] elke keer), dan is deze benadering geschikt. Zie [!DNL Experience Platform Tags] documentatie voor meer informatie over het maken van [!UICONTROL direct call rules].
* Aangepaste gebeurtenissen: Als u dynamisch een payload met unieke waarden voor gebeurtenissen op SPA pagina&#39;s moet koppelen, gebruikt u aangepaste JavaScript-gebeurtenissen en luistert u ernaar in [!DNL Experience Platform Tags]. Gebruik de payload om gegevenselementen en analytische variabelen in te stellen in Codes. Deze methode wordt als de beste praktijk beschouwd, aangezien deze behoefte gewoonlijk overheersend is voor SPA. In de onderstaande voorbeelden wordt de methode voor aangepaste gebeurtenissen gebruikt.

**Voorbeelden:** [In dit](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) Help-document, er zijn koppelingen naar voorbeeldsites SPA die deze implementeren [!DNL Analytics] en andere Experience Cloud-oplossingen. In deze voorbeelden worden de volgende aangepaste gebeurtenissen gebruikt:

* **[!DNL Event-view-start]**: Uitvoeren aan het begin van de weergave of de status die wordt geladen.
* **[!DNL Event-view-end]**: Uitvoeren wanneer een weergave-/statuswijziging optreedt en alle SPA componenten op de pagina klaar zijn met laden. Dit is de gebeurtenis die doorgaans gegevens naar Adobe Analytics verzendt.
* **[!DNL Event-action-trigger]**: Uitvoeren wanneer een gebeurtenis op de pagina plaatsvindt, behalve het laden van de weergave of status. Voorbeelden hiervan zijn een klikgebeurtenis of een kleinere inhoudswijziging zonder een weergavewijziging.

Raadpleeg de pagina&#39;s en documenten waarnaar hierboven wordt verwezen voor meer informatie over hoe en wanneer deze gebeurtenissen worden uitgevoerd. U hoeft niet dezelfde gebeurtenisnamen te gebruiken in uw implementatie. Het functionele gebruiksscenario voor de gebruikte methode is van essentieel belang om te begrijpen als de aanbevolen beste praktijk voor elke methode. In de volgende video ziet u een voorbeeld SPA pagina en voorbeeldcode in [!DNL Experience Platform Tags] die naar de aangepaste gebeurtenissen luistert.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## s.t() of s.tl() uitvoeren in het dialoogvenster [!DNL Experience Platform Tags] {#running-s-t-or-s-tl-in-the-launch-rule}

Een belangrijk begrip voor [!DNL Analytics] wanneer u met een SPA werkt, is het verschil tussen `s.t()` en `s.tl()`. De code activeert een van deze methoden in [!DNL Experience Platform Tags] gegevens verzenden naar [!DNL Analytics].

* **s.t()** - De &#39;t&#39; staat voor &#39;track&#39; en dit staat voor een paginaweergave. Als de weergave voldoende verandert dat u  *overwegen* het een nieuwe &quot;pagina&quot;is, gebruik deze vraag. Een unieke waarde instellen voor de [!DNL s.pageName] variabele en gebruik `s.t()` om de gegevens naar [!DNL Analytics].

* **s.tl()** - De &quot;tl&quot; staat voor &quot;trackkoppeling&quot; en dit staat voor een koppelingsklik of een kleine wijziging in de inhoud. Als de weergavewijziging minimaal is, gebruikt u `s.tl()` om een unieke waarde over te gaan over de interactie aan [!DNL Analytics]. Deze variabele die wordt doorgegeven, is niet [!DNL s.pageName], omdat dit wordt genegeerd in Analytics wanneer `s.tl()` de vraag wordt ontvangen.

**TIP:** Als algemene richtlijn geldt dat als het scherm met meer dan 50% verandert, u de opdracht `s.t()` de vraag van de paginaweergave. Anders, gebruik `s.tl()`. Gebruik uw oordeel echter bij het overwegen van acties die een nieuwe &quot;pagina&quot;vormen en hoe dat in Adobe Analytics-rapporten moet worden gepresenteerd.

De volgende video laat zien waar en hoe u kunt activeren `s.t()` of `s.tl()` in tags.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Variabelen wissen {#clear-variables}

De juiste gegevens verzenden naar [!DNL Analytics] op het juiste moment. In een SPA-omgeving wordt een waarde opgeslagen in een [!DNL Analytics] variabele blijft bestaan en wordt opnieuw aangeboden in [!DNL Analytics], mogelijk wanneer u dit niet meer wilt. Er bestaat een functie in het dialoogvenster [!DNL Analytics] [!DNL Tags] uitbreiding om de variabelen te ontruimen om ervoor te zorgen dat de volgende vraag niet correct gegevens verzendt naar [!DNL Analytics].

In het bovenstaande diagram worden variabelen gewist *na* u verzendt gegevens. In werkelijkheid kan dit vóór OF na de vraag gebeuren, echter consistent in uw [!DNL Experience Platform Tags] regels voor een schonere uitvoering. Als u variabelen wist *voor* u voert uit `s.t()`, plaats de nieuwe variabelen onmiddellijk na de vraag en ga dan te werk om de nieuwe gegevens naar te verzenden [!DNL Analytics].

**OPMERKING:** Variabelen wissen is niet altijd nodig wanneer deze worden uitgevoerd `s.tl()`. Deze vraag vereist het gebruik van [!DNL linkTrackVars] variabele die moet worden geïnstrueerd [!DNL Analytics] welke variabelen moeten worden ingesteld. Dit gebeurt automatisch [!DNL Experience Platform Tags] via configuratie. Hiermee wordt voorkomen dat foutvariabelen worden ingesteld in tegenstelling tot het gedrag met `s.t()` roept in een SPA milieu. Om de schoonste en betrouwbaarste implementatie te verzekeren, is het waarschijnlijk gemakkelijker om de duidelijke variabelen functie voor beide vraag in een SPA milieu te gebruiken.

In de volgende video ziet u waar en hoe u variabelen kunt wissen in [!DNL Tags].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Aanvullende overwegingen {#additional-considerations}

### De vensters van de Code van de douane in [!DNL Experience Platform Tags] {#custom-code-windows-in-tags}

In de [!DNL Tags] [!DNL Analytics] extensie, er zijn twee plaatsen waar aangepaste code kan worden ingevoegd: De &quot;[!UICONTROL library management]&quot; en &quot;[!UICONTROL Configure tracker using custom code]&quot; secties.

![Tags Analytics, aangepaste codevensters](assets/launch_analyticscustomcodewindows.png)

Bij een van deze locaties wordt de code in de eerste pagina één keer uitgevoerd om de SPA pagina te laden. Als de code moet worden uitgevoerd bij een weergave- of actiewijziging, implementeert u die code in het juiste **[!UICONTROL rule]** (bijvoorbeeld &quot;pagina laden: event-view-end&quot;regel), om ervoor te zorgen dat de code telkens als uitvoert [!UICONTROL rule] loopt. Wanneer u de handeling maakt in het dialoogvenster [!UICONTROL rule], set *Extension = Core* en *Type handeling = aangepaste code*.

### &quot;Hybride&quot; SPA en traditionele locaties {#hybrid-spa-and-traditional-sites}

Sommige sites bestaan uit een combinatie van traditionele en SPA pagina&#39;s. In dit geval, gebruik een strategie die voor beide paginatypen werkt. Wanneer u aangepaste gebeurtenissen op de site configureert en regels activeert in [!DNL Experience Platform Tags], zorg ervoor dat dubbele treffers niet naar worden verzonden [!DNL Analytics] gebaseerd op wijzigingen in de hash enzovoort. In dit geval onderdrukt u een van de paginaweergaven om te voorkomen dat dubbele gegevens naar Adobe Analytics worden doorgegeven.

Als u besluit de functionaliteit in uniek te scheiden [!UICONTROL rules] voor meer controle, herinner aan document dat u dit hebt gedaan. Als u een [!UICONTROL rule]dezelfde wijziging aan te brengen in de andere [!UICONTROL rule].

### Integratie met [!DNL Target] gebruiken van A4T {#integration-with-target-using-a4t}

Wanneer u integreert met [!DNL Target] met behulp van A4T bevestigen dat de [!DNL Target] en [!DNL Analytics] aanvragen die worden verzonden in dezelfde weergave of handeling geven dezelfde waarde voor de SDID-parameter door. Zo zorgt u ervoor dat de gegevens op de achtergrond correct worden gesynchroniseerd.

Om deze klappen te bekijken, gebruik debugger of pakket controlehulpmiddel. Adobe verstrekt een Foutopsporing van het Experience Platform voor dit doel. Het is een Chrome-extensie die [hier gedownload](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob?hl=en). [!DNL Target] moet eerst op de pagina worden uitgevoerd. Dit kan ook in debugger worden geverifieerd.

## Aanvullende bronnen {#additional-resources}

* [SPA discussie over de forums van de Adobe](https://experienceleaguecommunities.adobe.com:443/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940)
* [Referentie Architectuur plaatsen om te tonen hoe te om SPA in Experience Platform Launch uit te voeren](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)
