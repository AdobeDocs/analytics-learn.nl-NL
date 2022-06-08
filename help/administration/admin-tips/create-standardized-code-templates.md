---
title: Standaardcodesjablonen maken
description: 'Voor een basislijnimplementatie (d.w.z. wat uw bedrijf KPIs voor alle plaatsen van Adobe Analytics moet hebben), zou uw org één enkele implementatiemethode moeten hebben waar mogelijk. '
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---


# Standaardcodesjablonen maken

**WAT:** Voor een &quot;basislijn&quot;implementatie (d.w.z. wat uw bedrijf KPIs moet hebben voor alle plaatsen van Adobe Analytics), zou uw org één enkele implementatiemethode moeten hebben waar mogelijk. Gebruik bijvoorbeeld dezelfde gegevenslaagstructuur op verschillende sites en gebruik dezelfde regel/aangepaste code voor tagbeheer om bijvoorbeeld interne zoekopdrachten of informatie over het bezoekersprofiel vast te leggen.

**WAAROM:** Dankzij een herhaalbare en schaalbare basislijnimplementatie wordt het toevoegen van nieuwe elementen of nieuwe sites/apps een gestroomlijnde, lage inspanningsinspanning terwijl uw implementatie ook schoon en gemakkelijk blijft om problemen op te lossen. Met een uniforme methode wordt het ook gemakkelijker voor nieuwe beheerders/ontwikkelaars om online te komen en te begrijpen waarmee zij werken.

**HOE:** Eén indelingssjabloon gebruiken om aan ontwikkelaars door te geven wanneer een nieuwe site of tagverbetering online komt. Een woorddocument werkt meestal goed, waarbij u de volgende items kunt omtrekken:

* Variabelen die worden geïmplementeerd, hun doel en wanneer. Bijvoorbeeld:

| AA-variabele | Beschrijving | Wanneer/waar moet worden ingesteld | Instellen |
|--- |--- |--- |--- |
| eVar8 | Trefwoorden voor intern zoeken | Bij het landen van de interne pagina met zoekresultaten | gegevenslaag |
| event8 | Aantal interne zoekopdrachten | Bij het landen van de interne pagina met zoekresultaten | Beginregel |

* Details over het instellen. Dit is waar u om het even welke voorwerpen van de gegevenslaag nodig en hun syntaxis evenals om het even welke regels zou specificeren TMS die moeten worden gevormd en de details van de regelopstelling.
* De gevallen van de test om ervoor te zorgen worden behandeld in QA en alle variabelen u verwacht om in een succesvol testgeval te zien. Beschrijf wat een succesvolle implementatie zou moeten omvatten wanneer de ontwikkelaar deze verbetering test.

In het ideale geval hoeft dit document alleen te worden getweend voor de volgende site waar u de basisbeginselen bijwerkt, zoals de naam van de eigenschap, de naamgevingsconventie voor pagina&#39;s, enzovoort. U hoeft het wiel niet telkens opnieuw uit te vinden en u kunt meer tijd besparen.

## Auteurs

Dit document is medegeschreven door:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager bij NortonLifeLock Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, senior consultant bij Adobe
