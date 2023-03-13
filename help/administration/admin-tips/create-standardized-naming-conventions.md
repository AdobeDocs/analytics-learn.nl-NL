---
title: Standaardnaamconventies maken
description: De gestandaardiseerde Naamgevingsconventies zijn van toepassing op zowel de variabelenaam zelf wanneer deze wordt ingeschakeld in de API voor AA-beheer als op de waarden die worden doorgegeven aan de dimensie.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
exl-id: 0fe3b981-0d9b-4f12-a6ca-63a4140f4baf
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# Standaardnaamconventies maken

**WAT:** De gestandaardiseerde naamgevingsconventies zijn van toepassing op zowel de variabelenaam zelf wanneer deze is ingeschakeld in de Adobe Analytics (AA)-beheerinterface als op de waarden die worden doorgegeven aan de dimensie. (Paginanamen zouden dus &quot;paginanaam (v1)&quot; zijn als variabelenaam en de ingevoerde paginanamen moeten uniform zijn en een specifieke structuur/hiërarchie volgen, zoals &quot;sitename|homepage&quot; of &quot;sitename|zoekopdracht|zoekresultaten&quot;).

**WAAROM:** Namen van conventies zijn een uitstekende manier om alles uniform te houden en de interface begrijpelijk te houden voor uw gebruikers. Als u deze van het begin creeert en hen in het platform en de code afdwingt, zullen deze gemakkelijker aan schaal zijn.

**HOE:** De interface en het etiketteren doc zouden voor zowel &quot;Naam&quot;als &quot;Beschrijving&quot;moeten aanpassen - dit zal uw gebruikers van het moeten sparen een document van Excel en hen toestaan om uw gegevens direct in de interface te begrijpen. Het wordt ook aanbevolen om alles wat nodig is voor de consistentie te beperken.

Het is altijd verstandig om paginanamen ook op het platform consistent te houden (of schermnamen voor apps). U kunt bijvoorbeeld eigenschap &quot;instellen:section:subsectie:subsectie:unieke paginanaam&quot; in een variabele/dimensie. Als al deze gebieden in uw gegevenslaag afzonderlijk zijn, kon u zelfs de paginanaam direct in uw JS dossier/Lancering bouwen. Als al deze elementen ook in hun eigen dimensies zijn ingesteld, kunt u specifieke eigenschappen of gebieden van uw site/app eenvoudiger indelen en meer inzicht krijgen in verkeer en stromen.

Alles wat het voor gebruikers gemakkelijker maakt om de gegevens te vinden en te begrijpen, inclusief iets eenvoudigs zoals naamconventies, zal het gebruik van Adobe Analytics verhogen en het bedrijf betere inzichten bieden.

## Auteurs

Dit document is medegeschreven door:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager bij NortonLifeLock Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, senior consultant bij Adobe
