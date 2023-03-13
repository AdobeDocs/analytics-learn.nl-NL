---
title: Een algemene rapportsuite gebruiken
description: Een enkele algemene rapportsuite kan op vele manieren helpen en uw implementatie echt vereenvoudigen.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536
exl-id: 490addfd-b810-4f15-b065-e0e58048c882
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Een algemene rapportsuite gebruiken

**WAT:** Het is verleidelijk om rapportsuites voor elk van uw plaatsen te creëren, maar dit kan snel uw ergste nachtmerrie worden - zowel in termen van het bemoeilijken van uw rapportering als van uw implementatie. Een enkele algemene rapportsuite kan op vele manieren helpen en uw implementatie echt vereenvoudigen.

**WAAROM:** Het creëren van een globale rapportreeks is uw enige optie voor het hebben van een verenigde mening van uw digitale eigenschappen en gebruikersreizen over elk bezit. Als u een mobiele app en website hebt, moet u de toepassingsgegevens en webgegevens altijd in één rapportsuite combineren om gebruik te maken van alle ritten op verschillende apparaten en om gebruikers bij te houden die beide eigenschappen als één enkele bezoeker in plaats van als afzonderlijke rapportsuites bezoeken, waar u een onsamenhangende gegevensset zou hebben met 2 bezoekers - 1 op elke eigenschap - zonder dat de crossover bekend is.

Hier volgen de voor- en nadelen van één rapportenpakket waarmee u uw opties kunt afwegen:

* PROS:
   * Eenvoudig inzicht krijgen in uw hele digitale landschap. Als u de dimensie &#39;properties&#39; (eVar) waarnaar in andere tips wordt verwezen, hebt geïmplementeerd, kunt u heel gemakkelijk één weergave van al uw sites en apps, verkeer en conversies krijgen. Dit overzicht is van essentieel belang voor het begrijpen van uw bedrijf in zijn geheel.
   * In dezelfde zin, kunt u nu zien hoe de gebruikers over al uw eigenschappen stromen en hun reis door uw digitaal landschap begrijpen.
   * Eenvoudige toediening. Wanneer het gebruiken van veelvoudige rapportreeksen, zult u de interface op verscheidene plaatsen, evenals verscheidene etiketterende documenten (of gecompliceerder) moeten handhaven. Alles op één plaats houden betekent dat er maar één plaats is om updates uit te voeren. Het maakt het ook veel makkelijker om toegang te verlenen.
   * Betere bruikbaarheid in de interface. Als uw gebruikers slechts één plaats te gaan hebben, hoeven zij niet over welke rapportreeks te denken om te selecteren. Houd in mening dat u niet veelvoudige rapportreeksen binnen het zelfde werkruimtescherm kunt gebruiken, en het hebben van verscheidene van hen kan uw gebruikers verwarren.
   * Minder serveraanroepen = minder kosten. Als u vraag aan veelvoudige rapportsuites maakt, verhoogt u uw kosten. Door de implementatie eenvoudig te houden, blijven uw kosten laag.
   * U kunt virtuele rapportsuites (VRS) eenvoudig gebruiken om plaats-specifieke gegevens binnen de globale rapportreeks en beperkte gebruikerstoestemmingen uit te breken die op VRS indien nodig worden gebaseerd. Zodra de gegevens in individuele rapportreeksen worden gescheiden, kunt u niet het rollen omhoog, maar als het reeds in één dataset (globale RS) wordt aangesloten, wordt het gemakkelijk gebroken.
* CONS:
   * Als u zeer afzonderlijke eigenschappen hebt waar de gebruikers niet van één aan andere snijden en nooit dit wordt verwacht, kunt u afzonderlijke rapportreeksen willen handhaven.
   * Als uw eigenschappen sterk verschillende etiketteren en rapporteringsbehoeften hebben, kan het zinvol zijn om afzonderlijke rapportreeksen in het belang van veranderlijke efficiency op te zetten. Het hebben van afzonderlijke rapportreeksen zal u meer flexibiliteit in het gebruiken van douanevariabelen (meer eVars) geven.
   * Uniques overschreden: Met de Adobe Analytics-interface kunt u slechts 500.000 unieke waarden binnen één dimensie voor een bepaalde tijdsperiode zien. Zodra u dit overschrijdt, zullen de waarden als &quot;uniques overschreden&quot;of &quot;laag verkeer&quot;in de interface worden gegroepeerd. Deze waarden blijven wel beschikbaar op de achtergrond (Data Warehouse, Gegevensfeeds), maar kunnen niet worden weergegeven in de interface. Als u zeer korrelige gegevens hebt (zoals gebruikersnaam, PSN, enz.), is het gemakkelijk om dit niveau te bereiken. Het hebben van afzonderlijke rapportsuites kan met deze kwestie helpen.

**HOE:** Beginnend met een nieuwe implementatie van aa en het gebruiken van één globale rapportreeks is eenvoudig en ongecompliceerd. U zou enkel de globale rapportreeks (voor Dev en voor Prod) in aa moeten creëren admin UI en de waarden van de zelfde rapportreeks van identiteitskaart (RSID) op al uw eigenschappen toepassen.

Voor het migreren van een multitagging-strategie met een unieke rapportsuite per eigenschap is meer strategie en planning nodig. Enkele overwegingen die u in gedachten zult moeten houden:

* Het richten van uw variabelen (d.w.z. eVar1 op Bezit A moet het zelfde gegevenspunt vangen zoals eVar1 op Bezit B)
* Consolidatie van alle verwerkingsregels, regels voor marketingkanalen, classificaties (SAINT en Rule Builder)
* Gegevensfeeds en gegevensbronnen migreren
* Een cut over de datum kiezen en dit communiceren met alle zakelijke gebruikers

## Auteurs

Dit document is medegeschreven door:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager bij NortonLifeLock Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, senior consultant bij Adobe
