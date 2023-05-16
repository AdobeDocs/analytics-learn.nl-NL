---
title: Breng uw gegevensanalyse naar het volgende niveau met Berekende Metriek
description: Leer hoe een peer deskundige Berekende Metriek gebruikt om nieuwe metriek tot stand te brengen zonder hun implementatie te veranderen en de gegevens te gebruiken die reeds worden verzameld om complexe bedrijfsvragen te helpen beantwoorden.
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13266
thumbnail: KT-13266.jpeg
source-git-commit: c64f2fde1b91edd9f3d6c0f87aa889ed2c613d9b
workflow-type: tm+mt
source-wordcount: '1566'
ht-degree: 0%

---


# Breng uw gegevensanalyse naar het volgende niveau met Berekende Metriek

De meeste nieuwe gebruikers van Adobe Analytics zijn vertrouwd met Segmenten als manier om hun gegevens te segmenteren en te dokken. Vandaag, wil ik u aan berekende metriek introduceren, het volgende beste hulpmiddel in uw analist toolbox.

Als geavanceerde functie van Adobe Analytics kunt u met berekende metriek nieuwe metriek maken zonder dat u de implementatie wijzigt met behulp van de gegevens die u al hebt verzameld. De Berekende Bouwer van Metriek kan veel verschillende wiskundige en statistische functies gebruiken, zodat kunt u metriek tot stand brengen die zelfs de meest complexe bedrijfsvragen beantwoordt.

## Aan de slag met berekende cijfers

Om met berekende metriek te beginnen, kijken een eenvoudig voorbeeld. Stel dat u wilt begrijpen of gebruikers die zichzelf online bedienen, een hogere gemiddelde orderwaarde (AOV) hebben dan gebruikers die hulp bieden. Ga als volgt te werk om een berekende metrische waarde op te bouwen om deze vraag te beantwoorden:

Als u de Berekende metrieke Builder wilt openen, klikt u met de bovenste navigatie → **Componenten** → **Berekende cijfers** → **+ Toevoegen.** U kunt ook op de knop **+ ondertekenen** boven **Metrisch** in het deelvenster Componenten.


![Calc 01](assets/calc01.png) ![Calc 02](assets/calc03.png) ![Calc 03](assets/calc02.png)

![Calc 04](assets/calc04.png)

*Beschrijvingen hieronder voor UI-items*

Zodra de Berekende Bouwer van Metriek opent, voeg en/of doe het volgende toe:

**A.** Een naam voor de berekende metrische waarde. Deze naam wordt weergegeven in de lijst met metrische componenten. Zorg er dus voor dat dit duidelijk is voor uzelf en anderen, zoals *Call Center AOV*.

**B.** Een beschrijving van de berekende metrische waarde. Deze beschrijving wordt weergegeven wanneer gebruikers op de knop &quot;**i**&#39; naast metrisch in de componentenlijst, zodat zeker ben het informatief is. Bijvoorbeeld voor Call Center AOV, zouden wij kunnen toevoegen *Berekent AOV voor de Begeleidende Orden van het Centrum van Vraag*.

**C.** De metrische indeling: Kies decimaal, tijd, percentage of valuta en voeg decimalen en polariteit toe. Hier kiezen we *Valuta voor de notatie, 0 voor het aantal decimalen, en* ⬆ *Goed (groen) voor polariteit.*

**D**. Als u tags gebruikt, waarmee u onderwerpen kunt toepassen en snel berekende metriek kunt zoeken, voegt u de tags toe die hier van toepassing zijn. We hebben toegevoegd *AOV* en *callcenter* -tags.

**E.** Deze sectie is voor vertoning - aangezien u berekende metrisch in sectie F bouwt, zal de formule hier tonen.

**F.** Hier, zult u afmetingen (H), metriek (I) of segmenten (J) slepen en laten vallen om uw berekende metrisch evenals de exploitanten voor de formule tot stand te brengen. Als u voor elke meting op het cogumwiel klikt, kunt u de opties Metrisch type (standaard/totaal) en Kenmerk wijzigen. *We slepen en neerzetten Belastingen van het callcenter, dan hieronder,*:￼*. We accepteren het standaard metrische type en attributiemodel.*

**G**. Gebruik deze **+Toevoegen** om extra voorwaarden of statische aantallen toe te voegen, die wij hier niet nodig hebben.

**K.** En ten slotte, terwijl u uw berekening bouwt, kunt u voorproef de gegevens van de afgelopen 90 dagen hier.

Nu wij AOV van het Centrum van de Vraag hebben gebouwd, hebben wij ook berekende metrisch voor Online AOV nodig. We zouden dit doen volgens dezelfde stappen die hierboven zijn beschreven.

Daarna, kunnen wij derde berekende metrisch bouwen, of gebruikend de Berekende Bouwer van Metriek of op de vlucht van binnen de vrije vormlijst, om het Centrum van de Vraag en Online AOV te vergelijken zodat komen wij omhoog met iets als dit:

![Calc 05](assets/calc05.png)

In ons voorbeeld zien we een aanzienlijke lift wanneer kopers het callcenter gebruiken om hen te helpen een aankoop te doen. Deze gegevens kunnen dan onze beslissingen over hoe te om klanten te helpen bij hun aankopen door, bijvoorbeeld, popup aanbiedingen of andere geleide ervaringen te krijgen.

## Segmenten gebruiken in berekende cijfers

Nu, kijken hoe wij segmenten in berekende metriek kunnen gebruiken om meer inzicht in klantengedrag, voorkeur, en motivaties te krijgen. Met segmenten en berekende metriek, kunnen wij genoeg over klanten leren om hun ervaring te verbeteren, opbrengst te verhogen, en klantentevredenheid en loyaliteit te verbeteren.

Uit de bovenstaande AOV-voorbeelden weten we al dat de aankoop van gesubsidieerde producten door callcenter doorgaans een hoger AOV heeft. Nochtans, vertellen andere metriek ons dat de meeste gebruikers niet het vraagcentrum voor aankopen gebruiken.

Welke winkelcategorieën - en gebruikerspaden door deze categorieën - resulteren dus in het hoogste AOV?  We kunnen dit ontdekken door segmenten te combineren met berekende meetwaarden.

Om dit te doen, moeten we eerst bezoeken-level creëren *include* en *uitsluiten* segmenten voor elke productcategorie. Opnemen of uitsluiten wordt bepaald door op de knop **Opties** in de rechterhoek van de container. Standaard is Inclusief.

![Calc 06](assets/calc06.png) ![Calc 07](assets/calc07.png)

Zodra wij deze segmenten hebben gecreeerd, kunnen wij berekende metrisch tot stand brengen om u het antwoord op uw vraag te geven. Wij openen de Berekende Bouwer van Metriek en doen het volgende:

1. Zoek naar de nieuwe segmenten en sleep de gewenste segmenten naar het grijze gebied boven aan het dialoogvenster **Definitie** doos. Als we bijvoorbeeld een AOV willen maken voor gebruikers die zowel de categorieën Vrouwen als Mannen hebben bezocht, maar niet die van Kid, kunnen we deze drie segmenten naar dat gebied slepen: *Inclusief vrouwen*, *Inclusief mannen*, en *Kid&#39;s uitsluiten*. We noemen dit *stapelsegmenten*.

   ![Calc 09](assets/calc09.png) ![Calc 08](assets/calc08.png)

1. Vervolgens slepen en neerzetten we de **Online-inkomsten** metrisch in de zelfde container, dan **Online bestellingen**. Aangezien de containers als wiskundige uitdrukkingen werken om orde van verrichtingen te bepalen, worden de punten in containers verwerkt vóór verdere processen, hoewel wij geen veelvoudige containers of processen in deze berekening hebben.
1. Wij veranderen de exploitant tussen de twee metriek in verdeling (.).
1. Wij selecteren **Valuta** als formaat, **0** decimalen, en **UP** voor polariteit.
1. Geef de berekende metrische waarde een naam en geef een beschrijving op.
1. Opslaan.

Als we klaar zijn, ziet onze berekende metrische vormgeving er als volgt uit:

![Calc 10](assets/calc10.png)

Nadat wij berekende metriek gebruikend gestapelde segmenten voor elke combinatie van bezoekerscategoriereis creëren en een blik nemen bij de gegevens, kijk wat wij leren! Gebruikers die tijdens hun bezoek zowel de categorie Vrouwen als de categorie Mannen bezoeken, hebben het hoogste AOV en in vergelijking met bezoekers van één categorie is de lift significant:

![Calc 11](assets/calc11.png) ![Calc 12](assets/calc12.png)

Als we dit weten, kunnen we de paginalay-out, de productplaatsing en het promotiemateriaal optimaliseren om meer mensen in deze categorieën te krijgen voordat we uitchecken.

## Waardevol, maar niet overal beschikbaar

**Dus - berekende meetwaarden, zowel eenvoudig als complex, zijn superwaardevol voor analisten!**

Deze cijfers zijn echter niet in alle gebieden van Adobe Analytics beschikbaar. U kunt berekende metriek niet gebruiken in:

- Uitval in Analysis Workspace
- Cohortanalyse in Analysis Workspace
- Data Warehouse
- Real Time-rapporten
- Huidige gegevensrapporten
- Analyses voor doel
- Report Builder

## Aanbevolen werkwijzen voor berekende metriek

Nu u weet hoe waardevol berekende metriek kan zijn, nemen een blik bij sommige beste praktijken in het bouwen van hen.

1. **Controleer de syntaxis van uw formule.** Zorg ervoor dat de syntaxis van de formule zowel correct is als volgt de syntaxis van Adobe Analytics om ervoor te zorgen dat u zinvolle informatie krijgt.
1. **Controleer de volgorde van de bewerkingen.** Zorg ervoor dat u de containers zorgvuldig gebruikt en plaats de dingen in de juiste wiskundige volgorde van de bewerkingen.
1. **Geen gegevens met dubbele telling**. U kunt dubbel-tellende gegevens vermijden door ervoor te zorgen dat de formule die in berekende metrisch wordt gebruikt niet de zelfde gegevens veelvoudige tijden telt. Dit wordt vaak bereikt door *Inclusief* en *Uitsluiten* de omstandigheden in de berekende metrische waarde of door het gebruik van segmenten.
1. **Tijdgranulariteit controleren.** Zorg ervoor berekende metrisch zelfde tijdgranulariteit zoals de bronmetriek heeft die in de formule wordt gebruikt.
1. **Gebruik nauwkeurige gegevens:** U krijgt alleen waardevolle resultaten als u nauwkeurige en betrouwbare gegevens gebruikt in de berekening.

## Aangepaste beste praktijken voor segmenten

Houd bij het maken van segmenten in Adobe Analytics rekening met de volgende tips:

1. **Houd het eenvoudig.** Vermijd overcomplicaties van het segment. Houd het zo eenvoudig mogelijk en gebruik alleen de voorwaarden die nodig zijn om de nauwkeurigheid te waarborgen.
1. **De juiste containertypen gebruiken**. Gebruik het juiste containertype (bezoeker, bezoek of hit) in de segmentdefinitie om onjuiste resultaten te voorkomen.
1. **Geen gegevens met dubbele telling**. Zoals met berekende metriek, zorg ervoor het segment niet de zelfde gegevens veelvoudige tijden telt. U kunt containers opnemen en uitsluiten.
   1. Wanneer een include-container wordt gebruikt, wordt deze *include* *alle inhoud van het bezoek* als een treffer overeenkomt met de voorwaarde tijdens het bezoek.
   1. Wanneer een container voor uitsluiten wordt gebruikt, wordt deze *sluit alle inhoud van het bezoek uit* als een treffer overeenkomt met de voorwaarde tijdens het bezoek.
1. **Containers goed nesten**. Bepaal welke gegevens worden opgenomen met behulp van de buitenste container en pas vervolgens geneste regels toe op de resterende gegevens. Aangezien de genestelde regels worden toegepast, doet de segmentstroom dienst als trechter, en de verdere regels zijn niet op om het even welke klappen van toepassing die de eerste regel uitsloot.
1. **Zorg ervoor dat de gegevens up-to-date zijn.** Zorg ervoor om nauwkeurige en bijgewerkte gegevens in de segmentdefinitie te gebruiken om nauwkeurige resultaten te krijgen.
1. **Test het segment.** Test altijd het segment om er zeker van te zijn dat het naar behoren werkt voordat u het naar anderen loslaat.
1. **Houd rekening met prestaties.** De segmenten kunnen rapportverwerking vertragen, zodat denk dat effect wanneer het bouwen van hen.

## Key Takeaways

Het combineren van segmenten en berekende meetwaarden in Adobe Analytics kan absoluut leiden tot een robuustere en effectievere gegevensanalyse. Door uw gegevens te segmenteren en te dicteren en berekeningen te maken voor vergelijking, kunt u meer inzicht krijgen in het gedrag van klanten dat u kunt gebruiken om uw marketingcampagnes te optimaliseren en op maat gemaakte dashboards en rapporten te maken. Nochtans, herinner dat de berekende metriek niet in alle gebieden van Adobe Analytics beschikbaar zijn, en zorg ervoor om beste praktijken te volgen om ervoor te zorgen u nauwkeurige en nuttige gegevens krijgt.


## Auteur

Dit document is geschreven door:

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, Senior Adobe Analytics Manager bij Adswerve

![Adswerve](assets/calc14.png)
