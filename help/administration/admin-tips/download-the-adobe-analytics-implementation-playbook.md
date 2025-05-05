---
title: Afspeelboek voor Adobe Analytics-implementatie downloaden
description: Een Business Requirements Doc (doorgaans BRD genoemd) is een zeer belangrijk stuk documentatie waaraan belangrijke belanghebbenden, zakelijke gebruikers en technische gebruikers willen samenwerken. Het is een plaats voor het documenteren van al uw gewenste KPIs, het melden van vereisten, om het even welk gegevenspunt u wenst om te zien wanneer uw implementatie van aa volledig is.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10530.jpg
kt: 10530
exl-id: aab53a12-3f11-49c9-aba4-dc926bcf776b
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '1803'
ht-degree: 0%

---

# Afspeelboek voor Adobe Analytics-implementatie downloaden

Voordat u aan de slag gaat, [het afspeelboek downloaden](assets/aa-implementation-playbook.xlsx).

## Tabblad Zakelijke vereisten

**WAT:** Een Business Requirements Doc (doorgaans BRD genoemd) is een zeer belangrijk stuk documentatie waaraan belangrijke belanghebbenden, zakelijke gebruikers en technische gebruikers willen samenwerken. Het is een plaats voor het documenteren van al uw gewenste KPIs, rapporteringsvereisten, en om het even welk gegevenspunt u wenst om te zien wanneer uw implementatie van Adobe Analytics (AA) volledig is.

**WAAROM:** Dit dient als een springpunt voor de volgende documentatie (SDR, tech spec, enz.) en is een gemeenschappelijke bron van waarheid voor een overeengekomen eindstaat van AA. In dit document worden gedachten over de verschillende teams in de organisatie georganiseerd, zodat u uw implementatie verder kunt ontwikkelen of verbeteren.

**HOE:** Het documenteren van de bedrijfsvereisten wordt algemeen gedaan door de eind - bedrijfsgebruikers van AA, maar het is belangrijk om terugkoppelen van technologiegebruikers te krijgen aangezien er technische uitdagingen kunnen zijn om nota te nemen en bepaalde gegevenspunten meer inspanning dan anderen kunnen vereisen, die factoren in prioriteitstelling.

Vraag jezelf af: &quot;Wat zijn de dingen die we op onze site willen volgen&quot;, &quot;welke datapunten zijn belangrijk voor mij bij het melden van het gebruik&quot;, en het allerbelangrijkste: &quot;hoe zullen deze datapunten beslissingen beïnvloeden&quot;. Het is belangrijk om elk van uw bedrijfsvereisten op een gegevenspunt te verzekeren dat kan worden gebruikt om bedrijfsbesluiten te informeren. Het kan bijvoorbeeld verleidelijk zijn om elke klik op uw site bij te houden, maar aan het einde van de dag, welke inzichten leent u uit die rapportage?

Begin met het invullen van kolom C in de onderstaande screenshot (Bedrijfsvereiste). Dit zou moeten zijn als &quot;hoeveel interne onderzoeken op onze plaats&quot;worden voltooid of &quot;welke interne campagnevlek het meest effectief in termen van beelden is&quot;. Nadat u dit detailniveau hebt ingevuld, kunt u kolom B (Categorie) opnieuw invullen en de vereisten groeperen in categorieën zoals &quot;Zoeken&quot; of &quot;Interne promotie&quot;. Deze categorieën moeten exact overeenkomen met de technische specificaties.

U geeft ook aan of u denkt dat het gebruik van een eVar, gebeurtenis, proxy of combinatie zal leiden tot wat u wilt bijhouden.

En tot slot zal de kolom van de Status van de Implementatie als statuscontrole dienen aangezien u begint om dingen aan uw plaats toe te voegen.

![Document met zakelijke vereisten](assets/brd-template.png)

## Variabele toewijzen, tabblad (document/SDR coderen)

**WAT:** Een document met codes (doorgaans SDR genoemd) is een essentieel stuk documentatie dat waardevol is voor zowel technische als zakelijke gebruikers van AA. Het maakt een lijst van elke variabele in gebruik door rapportreeksen samen met alle relevante details voor de veranderlijke montages, hoe de variabele wordt uitgevoerd, en wat zijn doel in rapportering is. Net als uw eigenschappendocument moet dit een levend, goed beheerd Excel-document zijn met een puntpersoon die verantwoordelijk is voor het up-to-date houden van dit document, aangezien tagging-verbeteringen of implementatiewijzigingen worden geïntroduceerd.

**WAAROM:** Dit document heeft vele doelen, maar het belangrijkste is het volgende:

* Voor iedereen die nog niet vertrouwd is met uw implementatie (nieuwe huur, bedrijfseigenaar die de beschikbare rapporten beter wil begrijpen, enz.) In dit document wordt de beste weergave gegeven van alle variabelen die zijn geïmplementeerd en van hun doel, zodat individuen zichzelf kunnen dienen voor het leren van uw AA-instelling.
* Voor de eigenaar/technische gebruiker van het product van AA, zal dit document als herinnering dienen hoe andere variabelen opstelling zijn en welke variabelen voor gebruik wanneer het toevoegen van een nieuwe dimensie beschikbaar zijn.

**HOE:** Begin door van alle Adobe uit-van-de-doos variabelen (pagina, product, geo, enz.), evenals eVars, steunen, gebeurtenissen, en lijstvariabelen in een doc van Excel een lijst te maken. Dit zou één lusje per plaats/rapportreeks moeten hebben.
Voor elk van deze afmetingen voeg ik de volgende kolommen toe:
* **Naam:** Geef een eenvoudige en korte naam op die de meeste gebruikers kunnen begrijpen. Dit moet zo intuïtief zijn dat een nieuwe gebruiker de variabele kan ophalen en begrijpen wat de variabele moet vastleggen.
* **Omschrijving:** Meer informatie over waar de variabele voor wordt gebruikt en welke gegevens deze bijhoudt. Ik houd dit kort en eenvoudig en heb het de beschrijving die in de interface wordt gebruikt aanpassen. In het ideale geval wil ik niet dat mijn gebruikers ooit het etiketterende document hoeven te raadplegen. Dus als er een nieuwe dimensie wordt ingesteld op de achterkant van de beheerder, voeg ik daar dezelfde beschrijving aan toe. Op deze manier kan de gebruiker rechtstreeks in Workspace op het informatiepictogram klikken om te begrijpen wat een dimensie is - een Excel-document hoeft niet te worden opgehaald!

![Pagina-URL vereenvoudigd](assets/page-url-simplified.png)

* **Code:** De code van de achterkant die de waarde plaatst. Dit kan het gebied van de gegevenslaag op de pagina zijn, of u kunt roepen dat dit met een regel van de Lancering, een verwerkingsregel, enz. wordt gedaan.
* **Classificatierapporten:** Alle classificatierapporten uitschrijven die met de Classification Importer of de Classification Rule Builder worden uitgevoerd
* **Bereik oplossing:** Ik vind het nuttig om van alle eigenschappen (minstens degenen die meer dan standaardvariabelen gebruiken) in kleine kolommen een lijst te maken en een controleteken voor elke dimensie toe te voegen die op dat bezit wordt geplaatst. Op deze manier kunt u eenvoudig filteren op een specifieke eigenschap en snel zien waar een bepaalde dimensie wordt ingesteld.
* **Configuratie:** De montages van de gebruikersinterface van Admin voor elke variabele (d.w.z. voor eVars - vervaldatum, toewijzing, verkoop, enz.)

Screenshot van voorbeeld SDR:
![Voorbeeld-SDR.](assets/sample-sdr.png)

Het wordt ook aangeraden dit coderingsdocument te gebruiken om gratis variabelen en eventuele junkvariabelen bij te houden. Wanneer een afmeting niet meer nuttig is, zal dev gewoonlijk enige tijd nodig hebben om het te schrappen. Zelfs daarna kan caching voorkomen, of u kunt zich realiseren dat de dimensie ook elders werd geplaatst. Het opschonen van dimensies is niet eenvoudig en vereist vaak geduld. Hier volgen enkele tips om je rommel onder het bed te houden, zodat je gebruikers niet in verwarring raken terwijl ze het bijhouden.

* Alle afmetingen/gebeurtenissen die niet worden gebruikt, zijn &#39;free&#39; of &#39;being delete&#39;
   * Als de dimensie in de afgelopen 90 dagen junkwaarden heeft, wordt ze &#39;verwijderd&#39;
   * Als de dimensie de afgelopen 90 dagen vrij en duidelijk is, is ze &quot;vrij&quot;
   * Markeer deze als dusdanig onder &#39;Naam&#39; in het gecodeerde document, zodat u er gemakkelijk voor kunt filteren. Ik houd deze ongecontroleerd in het etiketteren document (de gegevensfilter van Excel) zodat de gebruikers hen niet zien
   * Markeer deze als de naam van de eVar in de interface, zodat gebruikers deze niet vinden in een zoekopdracht (dat wil zeggen: &#39;(v6)&#39;) en verwijder de beschrijving in de interface
* Op deze manier kunt u, wanneer u een nieuwe dimensie nodig hebt, eenvoudig filteren op &#39;gratis&#39; in de kolom &#39;Naam&#39; om een schone dimensie te zoeken die u kunt gebruiken
* Voor de &quot;worden geschrapt&quot;afmetingen en de gebeurtenissen, adviseer ik u hiervan het volgen gebruikend Werkruimte:
   * Maak een project dat alleen zichtbaar is voor beheerders met drie tabellen: Vars, props en gebeurtenissen. Ik gebruik &#39;instances&#39; voor de specifieke eVars en voor &#39;props&#39; maak ik bijvoorbeeld HIT-segmenten met &#39;prop5 bestaat&#39;.
   * Datum instellen op Laatste 90 dagen
   * Gebruik het bovenstaande als rijen in de 3 tabellen, samen met exemplaren
   * Zodra iets aan &quot;0&quot;krijgt, merk ik het als &quot;vrij&quot;in het etiketteren document en verwijder het uit het project van de Werkruimte

Op deze manier zijn je gegevens altijd schoon, en je hebt een duidelijk idee van je rommel.

![Overzicht van variabelen en gebeurtenissen](assets/variables-and-events-overview.png)

## Tabblad Eigenschappen

**WAT:** In een eigenschappendocument moeten al uw digitale eigenschappen worden vermeld, zoals websites, mobiele apps, andere gereedschappen (chatten, feedback enzovoort), of deze eigenschappen nu zijn gelabeld met Adobe Analytics of niet. Dit zou als gecentraliseerd, levend document over zaken en technologiegebruikers moeten dienen.

**WAAROM:** Dit geeft u een duidelijk beeld van de reis van uw gebruiker over al uw digitale eigenschappen, en wat Adobe Analytics doet en niet behandelt zodat kunt u beginnen om het etiketteren aan om het even welke eigenschappen toe te voegen waar het mist. Door uw digitale ecosysteem op deze manier op te zetten, kunt u potentiële mogelijkheden in het etiketteren van strategie identificeren om een volledig overzicht van de reis van uw gebruiker te krijgen. Bijvoorbeeld - hebt u een globale rapportreeks nodig om over veelvoudige domeinen/plaatsen te volgen? Is er een overdracht van bezoekersidentiteitskaart nodig tussen domeinen of app aan hybride ervaring? Moeten interne URL-filters worden bijgewerkt voor interdomeintracering?

**HOE:** Identificeer een eigenaar van het doc om bestuur en één enkele bron van verantwoordelijkheid voor het beheren van updates te verstrekken.
Hier geeft u het volgende weer op het tabblad Eigenschappen:
* **Naam eigenschap:** Dit kan een domein, subdomein, toepassingsnaam, enz. zijn. Zelfs binnen het zelfde domein, als sommige delen van het afzonderlijk worden beheerd (zoals door een verschillend team, of een verschillende technologie), zouden deze uit moeten worden gescheiden.
* **Koppeling (URL)** aan eigenschap indien beschikbaar
* **Eigenaar en contactpersonen:** Lijst de belangrijkste eigenaar of de contacten voor het bezit
* **Labelmethode:** Velen van ons hebben verschillende codemethoden en -implementaties (Starten, JS-bestanden, AEP, enz.). U kunt dit indien nodig verder naar beneden splitsen (zoals door codeversie of het systeem van het markeringsbeheer), maar dit is bedoeld om spoor van al uw verschillende codemethodes en versies te houden, waar de code moet worden bijgewerkt, en hoe het moet worden gehandhaafd. Als u Adobe Launch gebruikt, geeft u de naam van de eigenschap Launch op.

Denk eraan dat u alle digitale eigenschappen opneemt, zelfs als deze niet zijn gecodeerd met Adobe Analytics. Zo krijgt u meer inzicht in uw digitale landschap en in de manier waarop uw gebruikers met al uw eigenschappen omgaan.

Het wordt aanbevolen dit document zo eenvoudig mogelijk te houden en het niet met teveel informatie op te slaan, zodat het gemakkelijk te interpreteren blijft door verschillende delen van de organisatie. Analyseteams begrijpen het digitale landschap vaak beter dan andere teams, zodat dit document vaak door andere teams en managers wordt gebruikt om een grondig overzicht te geven.

>[!TIP]
>
>Een naam-/eigenschapdimensie maken in Adobe Analytics. Als u in Adobe Analytics een speciale dimensie (meestal een eVar) hebt die de naam van de site/app aangeeft, kunt u segmenteren, problemen oplossen, virtuele rapportsuite maken, enz. De voordelen zijn eindeloos, vooral wanneer het combineren van veelvoudige plaatsen in één (globale) rapportreeks. De sleutel zorgt ervoor dat uw ontwikkelingsteams altijd deze waarde in de eigenschappen afmeting plaatsen, met inbegrip van alle paginaladingen (s.t vraag/trackState) en alle douanegebeurtenissen (s.tl vraag/trackAction). Verwerkingsregels kunnen een waardevol hulpmiddel zijn om u te helpen deze waarden behoorlijk en consequent plaatsen.

[Bekijk deze video van Doug Moore](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=nl-NL){target="_blank"} voor meer informatie over het invullen van de implementatie playbook.

## Auteurs

Dit document is medegeschreven door:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager bij NortonLifeLock Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, senior consultant bij Adobe
