---
title: Deelvenster Adobe Analytics-toewijzing en terugzoekvensters
description: Leer hoe u het deelvenster Kenmerken en het terugzoekvenster kunt gebruiken om het gedrag van de klant te begrijpen en aan te passen hoe de dimensie-items krediet krijgen voor succesgebeurtenissen.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-06-20T00:00:00Z
jira: KT-13181
thumbnail: KT-13181.jpeg
source-git-commit: ae6fb85c3903986940463a4133f7b46f5efb64e1
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 0%

---


# Deelvenster Adobe Analytics-toewijzing en terugzoekvensters

Wanneer ik voor het eerst nadacht over de [deelvenster voor kenmerken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=en) en **lookback-venster** Ik werd onmiddellijk herinnerd aan het begrip &quot;*tijdreis&quot;*; Toen werd ik natuurlijk ook herinnerd aan onze typische reactie op vele nieuwe instrumenten zoals deze, om het gewoon uit te stellen om het te gebruiken, omdat ze er zo ingewikkeld uitzien.

Ik bedoel eerlijk gezegd, kijk gewoon naar al die opties, switches, deelvensters, lezingen en knoppen.  En serieus, laten we het hebben over die gecompliceerde knipperende lichten, slangen, kooien... WACHT!  Dit is niet het moment om afleiding te krijgen in het praten over tijdmachines, we hebben gewoon geen tijd... of doen we dat?

Ik geef toe **deelvenster voor kenmerken** is een vrij complex instrument; onze typische taak als analisten is echter om dag in dag uit een ander van onze favoriete en zeer complexe instrumenten te gebruiken om ook te kijken naar wat er in het verleden is gebeurd . Dat gereedschap heet ***Adobe Analytics***!  Dus ja, om onze zeer relevante vraag te beantwoorden, denk ik dat deze twee dingen zeggen dat we genoeg tijd hebben.

Daarom waarom zouden we iets als een beetje angst moeten toestaan om zo&#39;n verbazingwekkende, gesofisticeerde en krachtige hulpmiddelen als deze die ons letterlijk in staat stellen om te kijken, in de weg te staan *achterwaarts* in de tijd , elke dag ?

Want dit is TIJDREIS, mensen!  We hebben het allemaal over dat soort dingen.  Juist??!

Dus, wat wachten we op - een glanzende metalen auto, een politiedoos, of een oude telefoontoestel met de bedrading van een oude paraplu als antenne om op onze deur te komen?

Nee!  We hebben nog iets beters, dus laten we er maar aan vasthouden!

Nou... je krijgt het idee.


Nu we allemaal enthousiast zijn over tijdreizen, laten we een diepe adem nemen, een stap terug, bepalen wat de **deelvenster voor kenmerken** *echt* is, en onderbreek de dingen een beetje:

![Attributie](assets/attribution.png)

*Afbeelding 1 - Getallen die inline met de onderstaande tekst worden weergegeven*

In **toewijzing** Overweeg eenvoudig hoe gebeurtenissen/acties kunnen worden veroorzaakt door een individu, meerdere personen of een van de verschillende gebeurtenissen in de loop der tijd.

Volgens [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=en), *toewijzing* biedt analisten de mogelijkheid om aan te passen hoe *Dimension* objecten ontvangen krediet voor *succesgebeurtenissen*.


**⛔** DETOUR: Een korte opmerking om aan te geven dat **toewijzingsmodellen** worden zo vaak geassocieerd met **afzetkanalen** dat ik doelbewust *doorgehaald* KANAAL in de bovenstaande afbeelding om te illustreren dat het mogelijk is om **toewijzing** analyse tegen de meeste andere ***dimensie***.


In feite, is zelden om het even welke bepaalde klantenreis echt lineair en zelfs minder vaak voorspelbaar.  Bovendien zal elke klant in zijn eigen tempo te werk gaan; vaak kunnen ze teruggaan, vastlopen, uitvallen of andere niet-lineaire gedragingen volgen. Deze biologische acties maken het moeilijk of praktisch onmogelijk om de impact van marketinginspanningen op de hele reis van de klant te kennen. Ook wordt het hierdoor lastig om meerdere datakanalen aan elkaar te koppelen.

Dat klopt.  Laat je &#39;domino&#39;-analogieën bij de deur staan en open voor concepten die meer op de lijn liggen van het vlindereffect en de snaartheorie - maar net als alle andere dingen moeten we beginnen met een aantal basisprincipes.

## **Attributiemodellen**

Als wij **deelvenster voor kenmerken** We kunnen echter verschillende dingen gaan zien.  Bijvoorbeeld de **toewijzingsmodellen** laten zien hoe onze *conversies* (d.w.z. ***succeswaarden***) kan over *treffers* in een bepaalde groep.

Eenvoudig gezet, als **10 personen** een **GROTE RODE KNOP** om door een deur te stappen, onze **toewijzingsmodellen** zullen ons vertellen welke van hen **10 personen** wij willen &quot; krediet &quot; toekennen - of beter gezegd : hoe *veel* &quot; verdienste &quot; willen wij hen toewijzen - voor het drukken op de knop .

![Knop](assets/button.png)

Met dit in gedachten zijn er enkele voorbeelden van hoe **toewijzingsmodellen** die **10 personen**:

- **Eerste aanraking**: Dit model werkt precies zoals het klinkt door **100% krediet** aan de *first* persoon die door de deur liep.  Marktdeelnemers gebruiken deze aanpak eerder voor tactieken zoals ***sociale media*** of ***display***; het is echter ook een grote tactiek om vaak te gebruiken voor de doeltreffendheid van aanbevelingen ter plaatse voor producten.
- **Laatste aanraking**: Deze tactiek werkt ook precies zoals het klinkt, maar geeft in plaats daarvan **100% krediet** naar de LAST-persoon die door de deur liep.  Dit model wordt doorgaans gebruikt voor het analyseren van zaken zoals ***natuurlijke ( organische ) zoekopdracht*** en andere *op korte termijn* marketingcycluscampagnes.
- **Lineair**: Dit model verdeelt evend krediet over IEDERE ENKELE PERSOON die door de deur liep.

Hier wordt echter de nodige voorzichtigheid geboden, omdat u de resultaten zeer snel kunt verspreiden wanneer u deze tactiek toepast, rekening houdend met hoe langer de tactiek loopt en hoe groter het publiek dat deze bereikt.

- **U-vorm**: Deze benadering wijst toe **40%** van het krediet aan de *eerste persoon* in de deur, spreads **20%** van het krediet *iedereen tussen* en geeft vervolgens **40%** aan de **laatste** door. Dit model wordt meestal gebruikt in situaties waarin u een **lange conversie-/verkoopcyclus** bevattende *verschillende aanraakpunten* onderweg.  In dit geval is het uw bedoeling om vooral de nadruk te leggen op de ***first*** en ***last*** marketing tactiek die tot de klant het omzetten bijdroeg.
- **J**-**Vorm** en **Omgekeerd J**:
   - Denk na over **U-vorm**, maar in plaats daarvan wijst dit model **60%** krediet aan de *laatste persoon* door de deur lopen; **20%** aan de *first* en vervolgens *delen* de resterende **20%** dwars *iedereen anders* in het midden.  **Omgekeerd J** doet precies het tegenovergestelde.

Het is de bedoeling om de meeste nadruk te leggen, ofwel op de *begin* of de *end* van uw campagne; maar u wilt toch een bepaald bedrag aan krediet toekennen aan de bijdragende post aan de andere kant en tegelijkertijd de &quot; kleine jongens &quot; erkennen .

- **Tijdverlies**: Ik zou deze niet delen. Dit model heeft letterlijk een halfwaardetijd die exponentieel vervalt - in de loop der tijd!  In dit geval worden de *default* parameter voor de halfwaardetijd van dit model is **7 dagen**.  De manier waarop het werkt, is vervolgens van toepassing *gewicht* aan elk **marketingkanaal**, *op basis van de hoeveelheid tijd* die na de *eerste aanraakpunt* en wanneer de klant omzet.

  **Tijdverlies** en **U-vormige attributiemodellen** worden beide typisch gebruikt om langer-genoemd campagnes te meten, maar zoals u kunt zien, hebben zij lichtjes verschillende doelstellingen, die op hoe uiteindelijk zij worden gebaseerd *wegen* de waarde van het resultaat.

- **Aangepast**: Je kiest en kiest wie er geld krijgt.  Het is jouw campagne!

Voor aanvullende informatie over deze en andere attributiemodellen: [klik hier](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=en)

Om dit nog interessanter te maken, praten we over het terugdraaien van de klok!

## **Venster opzoeken**

Nu is het tijd om je geest op een hoger niveau te zetten.  Hier voegen we letterlijk het tijdreiselement toe aan onze analyse - en opnieuw beginnen we met de basis.

***Adobe*** define **terugzoekvensters** als &quot; de hoeveelheid tijd die een conversie moet terugkijken om aanraakpunten op te nemen . Attributiemodellen die meer krediet geven aan eerste interacties zien grotere verschillen bij het weergeven van verschillende terugkijkvensters.&quot;


Met andere woorden: **terugzoekvensters** bepalen gedurende welke periode *conversies* worden overwogen en *context* naar de analyse van de toerekeningswaarde. ***Adobe Analytics*** biedt drie typen **terugzoekvensters**:

- **Het terugkijkvenster van de bezoek:** Kijkt terug naar het begin van een ***bezoek*** wanneer er een conversie heeft plaatsgevonden , geeft deze inzicht in de onmiddellijke interacties die tot conversies hebben geleid .

  Dit is doorgaans de kortste **lookback-venster** te gebruiken.
- **Het terugkijkvenster van de bezoeker:** Kijkt naar alles ***bezoeken*** back-up maken tot de eerste maand van de geselecteerde **datumbereik**, die een veel breder beeld van de interactie van de klant aanbieden en helpt patronen in tijd identificeren.
- **Aangepast terugzoekvenster:** Hiermee kunt u de **toewijzingsvenster** buiten de verslaglegging **datumbereik** tot en met *maximum* van **90 dagen**.  Het biedt *flexibiliteit* bij het vastleggen van aanraakpunten die zijn opgetreden *buiten* de geselecteerde **datumbereik**, en zorgen voor een alomvattende analyse.

Door een bepaalde instelling aan te passen **lookback-venster** kunnen analisten vervolgens de impact van een of meer aanraakpunten binnen specifieke tijdframes onderzoeken en meer inzicht krijgen in de invloed van de verschillende tijdsduur op de toewijzingsresultaten.

## **Alles bijeenbrengen**

Wat betekent dit voor ons als analisten?

De **deelvenster voor kenmerken** en **lookback-venster** geven ons de macht om voorbij de alledaagse, oppervlakte-vlakke gegevens te kijken, en dieper in de klantenreis te duiken. Door te begrijpen welke aanraakpunten de grootste invloed hadden op *conversies* We kunnen echter weloverwogen beslissingen nemen over onze marketingstrategieën en de middelen effectiever toewijzen.

Herinner me, nadat u hebt **toewijzingsmodellen** en **terugzoekvensters** geselecteerd, kunt u uw gegevens nog verder manipuleren door het met te filtreren  **segment,** of een andere component die u op dit punt wilt gebruiken.  Bovendien beschikt u over alle functionaliteit van een traditionele werkruimte nadat het deelvenster is gerenderd.

## **Tot slot de tenuitvoerlegging ervan**

Nu je de concepten hebt, stel je voor dat je een marketingcampagne voert en probeert te bepalen welk kanaal het is *meest effectief* voor het besturen van omzettingen. Met de hulp van de **deelvenster voor kenmerken** niet alleen de **laatste aanraking**, maar ook de **eerste aanraking**, **zelfde aanraking** en andere **model** u bepaalt welke **kanalen** zijn *meest effectief* bij het besturen van uw *conversies*. Deze informatie kan vervolgens worden gebruikt om *optimaliseren* uw campagnes en verbetert de algehele prestaties eenvoudig door de klok terug te draaien met **lookback-venster** van uw keuze!

Nu je hebt gezien wat het kan doen, mag je niet misleid of geïntimideerd worden door de schijnbaar complexe kenmerken van het attributiepaneel.  **Gezicht**.  *Embrace* het.  Begrijp het*.* MAAR DE MEESTE - *Gebruik het in uw voordeel.* De **deelvenster voor kenmerken** en **lookback-venster** zijn de sleutels om een dieper inzicht in uw klanten en hun reis met uw merk te ontsluiten.

Nu kunnen we reizen &quot;[terug in de tijd](https://youtu.be/gVryJmZNFdU)&quot; met vertrouwen en gebruik de kracht van onze vertrouwde tijdmachine (ook bekend als ***Adobe Analytics***) om gegevensgestuurde beslissingen te nemen.
