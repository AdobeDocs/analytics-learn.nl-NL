---
title: Het ontgrendelen van inzichten met histogrammen; voorbij gemiddelden in Analytics
description: Ontdek het effect van histogrammen in analyses op inzichten boven gemiddelden.
feature: Visualizations
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-08-18T00:00:00Z
jira: KT-13833
thumbnail: KT-13833.jpeg
source-git-commit: f38a35067bf95fe02200d1409e3e70c1ef28abb3
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 0%

---


# Inzichten met histogrammen ontgrendelen: boven de gemiddelden in Analytics

_Ontdek het effect van histogrammen in analyses op inzichten boven gemiddelden. Histogrammen tonen gegevenspatronen in het gedrag van de klant, de betrokkenheid van de bezoeker, technische prestaties, en vormfouten, toelatend diepere inzichten en geïnformeerde besluiten in de Werkruimte van de Adobe._

Laten we naar binnen springen. U moet [histogrammen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/histogram.html?lang=nl-NL). Ik ga uitleggen waarom, maar ik wil jullie eerste vraag beantwoorden: Wat is een histogram in de wereld? Ik begrijp het. Meestal, als je een hoop staven ziet opstijgen, denk je dat het een staafgrafiek is. Ja, histogrammen zien er ongeveer hetzelfde uit, maar ik verzeker u dat ze anders zijn. In een staafdiagram worden de items vergeleken en in een histogram ziet u hoe vaak een variabele is opgetreden. Kijk eens. Hier is een staafdiagram:

![Staafdiagram 1](assets/bar-chart-1.png)

We hebben zes modellen, en we kunnen de inkomsten voor elk model vergelijken. We zien dat het model van Johannesburg de meeste inkomsten heeft, terwijl Berlijn het minste heeft.

Laten we nu eens kijken naar een histogram:

![Histogram 1](assets/histogram-1.png)

Onder aan de x-as hebben we het aantal eenheden dat door elke klant is aangeschaft. De eerste balk geeft aan hoe vaak een klant één eenheid heeft gekocht, de tweede balk toont hoeveel klanten twee eenheden hebben gekocht, enzovoort, tot klanten tien of meer eenheden hebben gekocht.

Hoe is dit nuttig? We zien dat de meeste mensen slechts één eenheid kopen. Het blijft afnemen tot we aan vijf eenheden komen. Dan daalt het weer tot we tien eenheden krijgen. Dit wijst erop dat klanten echt graag meervouden van vijf willen kopen, en misschien zouden we speciale prijzen of verpakkingen moeten aanbieden om daarvan te profiteren. Maar er zijn zeker ook veel andere toepassingen.

## Betrokkenheid van bezoekers

Als uw site of toepassing afhankelijk is van herhaald verkeer, wilt u weten hoeveel bezoekers er terugkomen en hoe vaak. Een van de eenvoudigste histogrammen die u kunt gebruiken, is te weten te komen hoeveel bezoekers meerdere keren terugkeren. Als je dat histogram in de loop der tijd volgt, kun je je vooruitgang zien, want hopelijk worden de tralies aan de rechterkant groter en de balken aan de linkerkant korter.

Misschien wilt u mensen op de site houden en artikelen lezen. Een histogram waarin wordt aangegeven hoeveel bezoekers verschillende aantallen artikelen lezen, geeft u inzicht in de mate van betrokkenheid. Waarom is dat nuttig? De meeste bezoekers lezen één artikel en vertrekken, maar sommige zeer geëngageerde bezoekers lezen drie artikelen en vertrekken. Dat is fantastische informatie! Nu weet u dat u de pagina in de eerste en derde artikelen moet aanpassen om bezoekers één artikel te laten lezen.

## Werking van de klant

De eigenaar van het product voor patiëntendossiers in een ziekenhuissysteem vroeg me om wat gegevens. Er waren zes regio&#39;s waaruit je je medische dossiers kon opvragen. Ze wilde weten hoeveel mensen op meer dan één klikte. Ik heb een histogram gemaakt waarin werd aangegeven hoeveel bezoekers op de opties 1, 2, 3, 4, 5 of 6 klikten. Dat lijkt misschien overdreven, maar meer dan de helft van de bezoekers klikte op ten minste twee opties en 3,2 procent van de bezoekers klikte op alle zes. Met dat histogram voor haar, leapte ze in actie, rangschikte haar routekaart, en vereenvoudigde de opties tot twee. Hierdoor werd de ervaring van de patiënt veel eenvoudiger.

## Technische prestaties

Als u een histogram instelt voor het aantal bezoekers dat technische fouten ervaart, kunt u een goed begrip opdoen van de technische prestaties van uw site. Veel bezoekers die te maken hebben met veel technische fouten zijn een teken om prioriteit te geven aan deze technische oplossingen.

## Werken met formulierprestaties

Foutberichten op een formulier zijn anders. Dit zijn bezoekersfouten, geen fouten van uw kant. Maar u zou van een histogram kunnen profiteren die u toont hoeveel bezoekers ervaren hoeveel fouten. Als u een histogram ziet waarin wordt aangegeven dat veel bezoekers veel fouten ondervinden, kan dat hun fout zijn. Dit zou een goede indicatie zijn dat uw formulier velden met een slechte naam, onduidelijke instructies of wellicht een ontwerp bevat dat verplichte velden verbergt.

## Waarom geen berekend metrisch?

Je kan je afvragen hoe dit anders is dan alleen een berekende metrische waarde. Hé, ik hou van een goede berekende metrische waarde. Ik denk dat het absoluut essentiële hulpmiddelen zijn om de prestaties van uw site te begrijpen. De kwestie voor vele van de gebruiksgevallen die ik heb vermeld, is dat een gemiddelde u de grootte van het probleem kan tonen maar het werkingsgebied van het verduisteren. Bekijk hoe histogrammen u aanvullende informatie geven voor een aantal van de bovenstaande gebruiksgevallen:

- Betrokkenheid bezoeker - Als u gemiddeld 1,2 artikelen hebt gelezen, is het duidelijk om het eerste artikel aan te passen. Je zult missen dat er nog een grote groep is die afsluit na het lezen van het derde artikel, wat het histogram duidelijk maakt.

  ![Histogram 2](assets/histogram-2.png)

- Technische fouten - Als je gemiddeld 8,7 fouten per bezoeker zou zien, zou je weten dat je een probleem had. Het histogram kan u laten zien dat 97% van de bezoekers een of minder fouten ervaart, maar dat een handvol uitschieters het gemiddelde omhoog drijft. Je zou dan kunnen besluiten dat het niet de moeite waard is om veel tijd te wijden aan het verbeteren van de ervaring voor die kleine groep uitschieters.

  ![Histogram 3](assets/histogram-3.png)

- Formulierfouten - Als u gemiddeld 3,6 berichten per bezoeker hebt voor een formulierfout, is dat een indicator voor een probleem. Je zou hetzelfde uitschietende probleem kunnen hebben als de technische fouten, maar er is ook inzicht in wat je kunt bereiken door een piek in het histogram te zien bij een bepaald aantal fouten. Een enorme piek bij één fout? Dit zou een algemeen probleem kunnen zijn dat al deze bezoekers ervaren of misschien kregen ze allemaal een andere fout. Een gigantische piek met drie fouten? Ah, nu is dat interessant. Als dat een onderzoek ertoe aanzet dat het de zelfde drie fouten toont, hebt u binnen op gegevens gecentreerd die u een inzicht in uw bezoekers geven en helpt u bevestigen wat waarschijnlijk een groep onderling verwant problemen is.

  ![Histogram 4](assets/histogram-4.png)

Zoals je kunt zien, hebben histogrammen niet alleen hun eigen toepassingen, maar ze verergeren ook het inzicht dat je verkrijgt van een gemiddelde. Het is een out-of-the-box visualisatie in Adobe Analytics en eenvoudig te maken. Hopelijk zijn deze gebruiksgevallen nuttig voor u of inspireren ze. Gelukkig visualiseren!

## Auteur

Dit document is geschreven door:

![Gitai Ben-Ammi](assets/gitai-headshot.png)

**Gitai Ben-Ammi**, Belangrijkste consultant bij Concentrix Catalyst

Adobe Analytics Champion
