---
title: Hoe Tijd besteed wordt berekend in Adobe Analytics
description: Een geaggregeerde pagina van de gebruikte afmetingen en metriek in de tijd.
feature: Metrics
exl-id: 71e9b856-8a0a-47be-a73f-4dc7d639a5de
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '1614'
ht-degree: 4%

---

# Overzicht van de tijd

Diversen [!UICONTROL 'time spent'] [cijfers](overview.md) en dimensies worden aangeboden in Adobe Analytics-producten.

## Metrische gegevens over &#39;tijd besteed&#39;

| Metrisch | Definitie | Beschikbaar in |
|---|---|---|
| [!UICONTROL Total seconds spent] | Vertegenwoordigt de totale hoeveelheid tijd bezoekers met een specifiek afmetingspunt in wisselwerking staan. Bevat de instantie van een waarde en persistentie voor alle volgende treffers. In het geval van props wordt de doorgebrachte tijd ook geteld bij volgende koppelingsgebeurtenissen. | Analysis Workspace, Report Builder (ook wel &#39;totale tijd besteed&#39; genoemd), Data Warehouse |
| [!UICONTROL Time spent per visit] (Seconden) | Ongeveer *Totaal aantal bestede seconden / (bezoek-grenzen)*<br> Geeft de gemiddelde hoeveelheid tijd aan dat bezoekers tijdens elk bezoek met een specifieke dimensie-item communiceren. **Opmerking**: Deze metrische waarde kan niet onafhankelijk worden berekend omdat de noemer van deze functie een interne metrische waarde is. | Analysis Workspace |
| [!UICONTROL Time spent per visitor] (Seconden) | Ongeveer *Totaal aantal gebruikte seconden / unieke bezoeker*<br> Geeft de gemiddelde hoeveelheid tijd aan dat bezoekers interageren met een specifiek dimensie-item over het leven van de bezoeker (duur van hun cookie). **Opmerking**: Deze metrische waarde kan niet onafhankelijk worden berekend omdat de noemer van deze functie een interne metrische waarde is. | Analysis Workspace |
| [!UICONTROL Time Spent/User (State)] | Ongeveer *Totaal aantal seconden mobiele app besteed/unieke bezoekers van mobiele apps*<br> Geeft de gemiddelde hoeveelheid tijd aan dat mobiele App-bezoekers communiceren met een specifiek dimensie-item tijdens de levensduur van de bezoeker (de duur van hun cookie). **Opmerking**: Deze metrische waarde kan niet onafhankelijk worden berekend omdat de noemer van deze functie een interne metrische waarde is. | Analysis Workspace |
| [!UICONTROL Average time spent on site] (Seconden) | Vertegenwoordigt de totale hoeveelheid tijd bezoekers met een specifiek afmetingspunt, per opeenvolging met een afmetingspunt in wisselwerking staan. Het is niet alleen beperkt tot &quot;site&quot;-gemiddelden, zoals de naam suggereert. Zie de sectie &#39;Hoe tijd besteed wordt&#39; voor meer informatie over reeksen.<br>**Opmerking**: Deze maatstaf verschilt zeer waarschijnlijk van &#39;Tijd per bezoek&#39; op het niveau van dimensiepunten als gevolg van de verschillen in de noemer in de berekening. | Analysis Workspace, Report Builder (weergegeven in minuten) |
| [!UICONTROL Average time on site] | Dit is zelfde metrisch zoals *Gemiddelde tijd die ter plaatse is doorgebracht (seconden)*, behalve opgemaakt als Tijd (uu:mm:ss) | Analysis Workspace |
| [!UICONTROL Average time spent on page] | Vervangen metrisch.<br> In plaats daarvan, adviseren wij dat u &quot;Gemiddelde tijd die aan plaats wordt doorgebracht&quot;gebruikt als de gemiddelde tijd voor een afmetingspunt wordt vereist. | Report Builder (wanneer een dimensie in het verzoek is) |
| [!UICONTROL Total session length], ook bekend als [!UICONTROL Previous session length] | Alleen mobiele App SDK. <br>De volgende keer dat de app wordt gestart, is bepaald voor de vorige sessie. Deze maateenheid wordt berekend in seconden en telt niet wanneer de toepassing op de achtergrond wordt uitgevoerd, alleen wanneer deze wordt gebruikt. Dit is metrisch op sessieniveau.<br>Voorbeeld: we installeren app ABC en starten de toepassing gedurende 2 minuten en sluiten de app. Over deze sessietijd worden geen gegevens verzonden. De volgende keer dat we de app starten, [!UICONTROL Previous Session Length] wordt verzonden met een waarde van 120. | Gebruikersinterface voor Analysis Workspace, Report Builder, mobiele services |
| [!UICONTROL Average session length] (mobiel) | *Totale sessieduur / (Starten - eerste starten)*<br> Alleen mobiele App SDK. Dit is metrisch op sessieniveau. | Report Builder, gebruikersinterface voor mobiele services |

## Afmetingen van &#39;bestede tijd&#39;

| Dimension | Definitie | Beschikbaar in |
| --- | --- | --- |
| [!UICONTROL Time spent per visit - granular] | De totale tijd die tijdens het bezoek is doorgebracht, is ingekort tot de dichtstbijzijnde seconde en is van toepassing op elke hit die deel uitmaakte van het bezoek. Dit is een bezoek-vlakke dimensie. | Analysis Workspace |
| [!UICONTROL Time spent per visit - bucketed] | De korrelige afmeting wordt in 9 verschillende bereiken opgesloten. Dit is een bezoek-vlakke dimensie. Bereiken zijn:<ul><li>Minder dan 1 minuut</li><li>1-5 minuten</li><li>5-10 minuten</li><li>10-30 minuten</li><li>30-60 minuten</li><li>1-2 uur</li><li>2-5 uur</li><li>5-10 uur</li><li>10-15 uur</li></ul>**Opmerking**: Er kunnen geen emmers hoger zijn dan dit, omdat een bezoek vervalt na twaalf uur activiteit. | Analysis Workspace, Report Builder |
| [!UICONTROL Time spent on page - granular] | De totale tijd die aan elke treffer wordt doorgebracht, die aan de dichtstbijzijnde seconde wordt beknot. Dit is een dimensie op raakniveau en bevat zowel paginaweergaven als koppelingsgebeurtenissen. Ondanks zijn naam is het niet beperkt tot de &quot;pagina&quot;dimensie. | Analysis Workspace |
| [!UICONTROL Time spent on page - bucketed] | De korrelige dimensie die in 10 verschillende waaiers wordt gekapt; nochtans, telt de gespikte dimensie slechts paginameningen (en sluit verbindingsgebeurtenissen uit). Dit is een raakvlak. Bereiken zijn:<ul><li>minder dan 15 seconden</li><li>15 tot 29 seconden</li><li>30 tot 59 seconden</li><li>1 tot 3 minuten</li><li>3 tot 5 minuten</li><li>5 tot 10 minuten</li><li>10 tot 15 minuten</li><li>15 tot 20 minuten</li><li>20 tot 30 minuten</li><li>meer dan 30 minuten</li></ul> | Analysis Workspace |

## Hoe &#39;Time Spent&#39; wordt berekend

Adobe Analytics gebruikt expliciete waarden (inclusief koppelingsgebeurtenissen en videoweergaven) om te berekenen [!UICONTROL Time Spent].

>[!NOTE]
>
>Zonder koppeling zoals [!UICONTROL Video Views] of [!UICONTROL Exit Links], kan de tijd die is besteed aan de laatste treffer van een bezoek niet bekend zijn. Om soortgelijke redenen [!UICONTROL Bounce Visits] (d.w.z. bezoeken met één hit) hebben ook geen &quot;tijd besteed&quot;.

De **teller** in alle tijd die wordt besteed, zijn de totale gebruikte seconden.

De **noemer** is niet beschikbaar als een aparte metrische waarde in Adobe Analytics. Voor meetgegevens op raakniveau &#39;tijd besteed&#39; is de noemer reeksen. Een reeks is een opeenvolgende reeks resultaten waarbij een bepaalde variabele dezelfde waarde bevat (door deze in te stellen, naar voren te spreiden of voort te zetten). &#39;Spread forward&#39; verwijst naar de persistentie tussen paginaweergaven (d.w.z. over volgende koppelingsgebeurtenissen), voor het berekenen van de doorgebrachte tijd.

* Bijvoorbeeld in het geval van [!UICONTROL Page Name] of andere dimensies op raakniveau, de noemer is in wezen [!UICONTROL 'Instances'] of [!UICONTROL 'Page Views'], maar met opnieuw laden en niet-ingestelde waarden (bijvoorbeeld koppelingsgebeurtenissen) geteld als één interactie (een reeks).

* Bounce- en exit-hits worden ook uit de noemer verwijderd omdat de tijd die is besteed niet bekend is.

## Veelgestelde vragen

+++Kunnen alle metriek &#39;bestede tijd&#39; op om het even welke dimensie worden toegepast?

De metriek &#39;bestede tijd&#39; die op om het even welke dimensie kan worden toegepast zijn:

* [!UICONTROL Total seconds spent]

* [!UICONTROL Time spent per visit] (Seconden)

* [!UICONTROL Time spent per visitor] (Seconden)

* [!UICONTROL Average time spent on site] (Seconden)

+++

+++Welke tijd bestede dimensie wordt het best gebruikt in uitsplitsingen met andere dimensies?

De [!UICONTROL Time Spent on Page – granular] dimensie is een dimensie op raakniveau. Als je dit opsplitst naar een andere dimensie, zal je de seconden vertellen dat een hit bleef waar ook de afbraakdimensie aanwezig was.
In het onderstaande voorbeeld is de zoekterm &#39;classificfieds&#39; gekoppeld aan raaktijden van 54 seconden, 59 seconden, enz., wat er wellicht op duidt dat bezoekers tijd doorbrengen bij het lezen van inhoud die voor die termijn is geretourneerd.

![](assets/time-spent1.png)

+++

+++Wat metrisch tegenover de afmeting van past is [!UICONTROL Time Spent on Page – granular]?

Elke meting. De dimensie geeft de tijd weer die wordt besteed aan de exacte hit waar de gebeurtenis heeft plaatsgevonden. Hogere tijd betekent dat een bezoeker langer op een pagina (hit) is gebleven waar de gebeurtenis heeft plaatsgevonden.

![](assets/time-spent2.png)

+++

+++Hoe doet dit [!UICONTROL Average Time Spent on Site] verschillen van [!UICONTROL Time Spent per Visit]?

Het verschil is de noemer in metrisch:

* [!UICONTROL Average time spent on site] gebruikt de opeenvolgingen die een afmetingspunt omvatten.

* [!UICONTROL Time spent per visit] gebruikt het aantal bezoeken

Dit heeft tot gevolg dat deze meetgegevens bij een bezoek vergelijkbare resultaten opleveren, maar dat ze bij een treffer anders zijn.

+++

+++Why do breaktotale with [!UICONTROL Average Time Spent on Site] komt het bovenliggende regelitem niet overeen?

Omdat [!UICONTROL Average Time Spent on Site] hangt van ongebroken opeenvolgingen van een afmeting af, en het binnenrapport hangt niet van het buitenrapport af wanneer het berekenen van deze looppas.

Neem bijvoorbeeld het volgende bezoek.

| hit# | 1 | 2 | 3 |
|---|---|---|---|
| **Seconden besteed** | 30 | 100 | 10 |
| **Paginanaam** | Home | Product | Home |
| **date** | 1 jan. | 1 jan. | 1 jan. |

Bij het berekenen van de tijd die voor de Homepage wordt doorgebracht, zou deze (30+10)/2=20 zijn, maar het onderbreken van die tijd per dag zou geven (30+10)/1=40 aangezien de dag één enkele ononderbroken looppas van 1 Januari heeft.

Dit heeft tot gevolg dat deze meetgegevens bij een bezoek vergelijkbare resultaten opleveren, maar dat ze bij een treffer anders zijn.

+++

## Voorbeelden van [!UICONTROL Time Spent] berekeningen

Veronderstel de volgende reeks servervraag voor één enkele bezoeker binnen één enkel bezoek is:

| Naar hit# | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|---|---|---|---|---|---|---|---|
| **Bezoek verstreken tijd (in sec)** | 0 | 30 | 80 | 180 | 190 | 230 | 290 |
| **Seconden besteed** | 30 | 50 | 100 | 10 | 40 | 60 | - |
| **Type hit** | Pagina | Koppeling | Pagina | Pagina | Pagina | Pagina | Pagina |
| **Paginanaam** | Home | - | Product | Home | Home (opnieuw laden) | Kar | Bevestiging van bestelling |
|  |  |  |  |  |  |  |  |
| **prop1** | A (set) | A (spread forward) | niet ingesteld | B (set) | B (set) | A(set) | C (set) |
| **prop1 seconden doorgebracht** | 30 | 50 | - | 10 | 40 | 60 | - |
|  |  |  |  |  |  |  |  |
| **eVar1** | Rood (set) | Rood (blijft bestaan) | (verlopen) | Blauw (set) | Blauw (set) | Blauw (blijvend) | Rood (set) |
| **doorgebrachte eVar1 seconden** | 30 | 50 | - | 10 | 40 | 60 | - |

Op basis van de bovenstaande tabel worden de gebruikte tijdwaarden als volgt berekend:

| prop1 | Totaal aantal bestede seconden | Tijd besteed per bezoek | Tijd doorgebracht per bezoeker | Aantal reeksen | Gemiddelde tijd die op de locatie is doorgebracht |
|---|---|---|---|---|---|
| A | 30+50+60=140 | 140/1=140 | 140/1=140 | 2 | 140/2=70 |
| B | 10+40=50 | 50/1=50 | 50/1=50 | 1 | 50/1=50 |
| C | 0 | 0 | 0 | 0 | 0 |
| Niet-toegewezen tijd | 100 | - | - | - | - |

| eVar1 | Totaal aantal bestede seconden | Tijd besteed per bezoek | Tijd doorgebracht per bezoeker | Aantal reeksen | Gemiddelde tijd die op de locatie is doorgebracht |
|---|---|---|---|---|---|
| Rood | 30+50=80 | 80/1=80 | 80/1=80 | 1 | 80/1=80 |
| Blauw | 10+40+60=110 | 110/1=110 | 110/1=110 | 1 | 110/1=110 |
| Niet-toegewezen tijd | 100 | - | - | - | - |

Tijd besteed per bezoek (korrelig): 290 Tijd besteed aan pagina (korrelig): 10, 30, 40, 50, 60, 100

Een aantal aanvullende opmerkingen ter ondersteuning van het voorbeeld:

* Alle gebruikte berekeningen zijn gebaseerd op de verstreken tijd van het bezoek, die bij de eerste treffer van het bezoek bij nul begint.

* &quot;Seconden besteed&quot; is het verschil tussen de tijdstempel van de huidige hit en de tijdstempel van de volgende hit. Als gevolg daarvan heeft de laatste treffer van het bezoek (en stormen) geen tijd doorgebracht.

* Een &quot;reeks&quot; is een opeenvolgende reeks resultaten waarbij een bepaalde variabele dezelfde waarde bevat (door deze in te stellen, door:sturen of blijvend). Bijvoorbeeld, prop1 &quot;A&quot;heeft twee opeenvolgingen: treffers 1 &amp; 2 en druk 6. Waarden bij de laatste treffer van het bezoek beginnen geen nieuwe reeks omdat de laatste treffer geen tijd heeft doorgebracht. De gemiddelde tijd die aan plaats wordt doorgebracht gebruikt opeenvolgingen in de noemer.

   * Alleen ten behoeve van de doorgebrachte tijd worden de punten &#39;doorgestuurd&#39;, van paginakoppen tot volgende treffers voor koppelingen, zoals hierboven voor pop1 op hit 2 wordt getoond. Hierdoor kan de waarde die is ingesteld voor prop1 bij hit 1 (&quot;A&quot;), de tijd verzamelen die is besteed aan hit 2.

   * Vars verzamelen de tijd die wordt besteed aan elke treffer waarbij de eVar is ingesteld of aanhoudt. De persistentie van eVar wordt gedefinieerd door de eVar-instellingen in Analytics > Admin.
