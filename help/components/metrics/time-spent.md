---
title: Hoe Tijd besteed wordt berekend in Adobe Analytics
description: Een geaggregeerde pagina van de gebruikte afmetingen en metriek in de tijd.
feature: Metrics
exl-id: 71e9b856-8a0a-47be-a73f-4dc7d639a5de
source-git-commit: 03502f42473791bec930cc688c0b7905acf12de6
workflow-type: tm+mt
source-wordcount: '1532'
ht-degree: 4%

---

# Overzicht van de tijd

Diverse [!UICONTROL 'time spent'] [ metriek ](overview.md) en de afmetingen worden aangeboden over de producten van Adobe Analytics. Deze pagina kan helpen de gewenste afmeting of metrisch doorbreken die u zoekt.

## Metrische gegevens over &#39;tijd besteed&#39;

| Metrisch | Definitie | Beschikbaar in |
|---|---|---|
| [[!UICONTROL Total seconds spent]](total-seconds-spent.md) | Vertegenwoordigt de totale hoeveelheid tijd bezoekers met een specifiek afmetingspunt in wisselwerking staan. Bevat de instantie van een waarde en persistentie voor alle volgende treffers. In het geval van props wordt de doorgebrachte tijd ook geteld bij volgende koppelingsgebeurtenissen. | Analysis Workspace, Report Builder (ook wel &#39;totale tijd besteed&#39; genoemd), Data Warehouse |
| [[!UICONTROL Time spent per visit] (Seconden) ](time-spent-per-visit.md) | Ongeveer *Totale bestede seconden / (bezoek-grenzen)*<br> vertegenwoordigt de gemiddelde hoeveelheid tijdbezoekers met een specifiek afmetingspunt tijdens elk bezoek in wisselwerking staan. **Nota**: Deze metrisch kan niet onafhankelijk worden berekend omdat de noemer van deze functie intern metrisch is. | Analysis Workspace |
| [[!UICONTROL Time spent per visitor] (Seconden) ](time-spent-per-visitor.md) | Ongeveer *Totale bestede seconden/unieke bezoeker*<br> vertegenwoordigt de gemiddelde hoeveelheid tijdbezoekers met een specifiek afmetingspunt over het leven van de bezoeker (lengte van hun koekje) in wisselwerking staan. **Nota**: Deze metrisch kan niet onafhankelijk worden berekend omdat de noemer van deze functie intern metrisch is. | Analysis Workspace |
| [!UICONTROL Time Spent/User (State)] | Ongeveer *Totale mobiele app bestede toepassingsseconden/unieke mobiele App bezoekers*<br> vertegenwoordigt de gemiddelde hoeveelheid tijd mobiele App bezoekers met een specifiek afmetingspunt over het leven van de bezoeker (lengte van hun koekje) in wisselwerking staan. **Nota**: Deze metrisch kan niet onafhankelijk worden berekend omdat de noemer van deze functie intern metrisch is. | Analysis Workspace |
| [[!UICONTROL Average time spent on site] (Seconden) ](average-time-on-site.md) | Vertegenwoordigt de totale hoeveelheid tijd bezoekers met een specifiek afmetingspunt, per opeenvolging met een afmetingspunt in wisselwerking staan. Het is niet alleen beperkt tot &quot;site&quot;-gemiddelden, zoals de naam suggereert. Zie de sectie &#39;Hoe tijd besteed wordt&#39; voor meer informatie over reeksen.<br>**Nota**: Deze metrische waarde verschilt zeer waarschijnlijk van &quot;Tijd die per Bezoek&quot;op een niveau van het afmetingspunt toe te schrijven aan de verschillen in de noemer in de berekening besteedt. | Analysis Workspace, Report Builder (weergegeven in minuten) |
| [[!UICONTROL Average time on site]](average-time-on-site.md) | Dit is zelfde metrisch zoals *Gemiddelde tijd besteed aan plaats (Seconden)*, behalve geformatteerd als Tijd (`hh:mm:ss`) | Analysis Workspace |
| [!UICONTROL Average time spent on page] | Vervangen metrisch.<br> In plaats daarvan raadt de Adobe u aan [[!UICONTROL Average time spent on site]](average-time-on-site.md) te gebruiken als er een gemiddelde tijd voor een dimensie-item nodig is. | Report Builder (wanneer een dimensie in het verzoek is) |

## Afmetingen van &#39;bestede tijd&#39;

| Dimension | Definitie | Beschikbaar in |
| --- | --- | --- |
| [[!UICONTROL Time spent per visit - granular]](../dimensions/time-spent-per-visit.md) | De totale tijd die tijdens het bezoek is doorgebracht, is ingekort tot de dichtstbijzijnde seconde en is van toepassing op elke hit die deel uitmaakte van het bezoek. Dit is een bezoek-vlakke dimensie. | Analysis Workspace |
| [[!UICONTROL Time spent per visit - bucketed]](../dimensions/time-spent-per-visit.md) | De korrelige afmeting wordt in 9 verschillende bereiken opgesloten. Dit is een bezoek-vlakke dimensie. Bereiken zijn:<ul><li>Minder dan 1 minuut</li><li>1-5 minuten</li><li>5-10 minuten</li><li>10-30 minuten</li><li>30-60 minuten</li><li>1-2 uur</li><li>2-5 uur</li><li>5-10 uur</li><li>10-15 uur</li></ul>**Nota**: Er kunnen geen emmers hoger zijn dan dit, omdat een bezoek na 12 uren van activiteit verloopt. | Analysis Workspace, Report Builder |
| [[!UICONTROL Time spent on page - granular]](../dimensions/time-spent-on-page.md) | De totale tijd die aan elke treffer wordt doorgebracht, die aan de dichtstbijzijnde seconde wordt beknot. Dit is een dimensie op raakniveau en bevat zowel paginaweergaven als koppelingsgebeurtenissen. Ondanks zijn naam is het niet beperkt tot de &quot;pagina&quot;dimensie. | Analysis Workspace |
| [[!UICONTROL Time spent on page - bucketed]](../dimensions/time-spent-on-page.md) | De korrelige dimensie die in 10 verschillende waaiers wordt gekapt; nochtans, telt de gespikte dimensie slechts paginameningen (en sluit verbindingsgebeurtenissen uit). Dit is een raakvlak. Bereiken zijn:<ul><li>minder dan 15 seconden</li><li>15 tot 29 seconden</li><li>30 tot 59 seconden</li><li>1 tot 3 minuten</li><li>3 tot 5 minuten</li><li>5 tot 10 minuten</li><li>10 tot 15 minuten</li><li>15 tot 20 minuten</li><li>20 tot 30 minuten</li><li>meer dan 30 minuten</li></ul> | Analysis Workspace |

## Hoe &#39;Time Spent&#39; wordt berekend

Adobe Analytics gebruikt expliciete waarden (inclusief koppelingsgebeurtenissen en videoweergaven) om de doorgebrachte tijd te berekenen.

>[!NOTE]
>
>Zonder koppelingsgebeurtenissen zoals [!UICONTROL Video Views] of [!UICONTROL Exit Links] is de tijd die u aan de laatste keer hebt doorgebracht tijdens een bezoek, onbekend. Om vergelijkbare redenen heeft [!UICONTROL Bounce Visits] (d.w.z. bezoeken met één hit) ook geen &#39;tijd besteed&#39; aan het programma.

De **teller** in alle tijd bestede berekeningen is totale bestede seconden.

De **noemer** is niet beschikbaar als afzonderlijke metrisch in Adobe Analytics. Voor meetgegevens op raakniveau &#39;tijd besteed&#39; is de noemer reeksen. Een reeks is een opeenvolgende reeks resultaten waarbij een bepaalde variabele dezelfde waarde bevat (door deze in te stellen, naar voren te spreiden of voort te zetten). &#39;Spread forward&#39; verwijst naar de persistentie tussen paginaweergaven (d.w.z. over volgende koppelingsgebeurtenissen), voor het berekenen van de doorgebrachte tijd.

* In het geval van [!UICONTROL Page Name] of andere afmetingen op raakniveau is de noemer bijvoorbeeld in wezen [!UICONTROL 'Instances'] of [!UICONTROL 'Page Views'] , maar met opnieuw laden en niet-ingestelde waarden (bijvoorbeeld koppelingsgebeurtenissen) geteld als één enkele interactie (een reeks).

* Bounce- en exit-hits worden ook uit de noemer verwijderd omdat de tijd die is besteed niet bekend is.

## Veelgestelde vragen

+++Kunnen alle metriek &#39;bestede tijd&#39; op om het even welke dimensie worden toegepast?

De metriek &#39;bestede tijd&#39; die op om het even welke dimensie kan worden toegepast zijn:

* [[!UICONTROL Total seconds spent]](total-seconds-spent.md)

* [[!UICONTROL Time spent per visit] (seconden)](time-spent-per-visit.md)

* [[!UICONTROL Time spent per visitor] (seconden)](time-spent-per-visitor.md)

* [[!UICONTROL Average time spent on site] (seconden)](average-time-on-site.md)

+++

+++Welke tijd bestede dimensie wordt het best gebruikt in uitsplitsingen met andere dimensies?

De [[!UICONTROL Time Spent on Page – granular]](../dimensions/time-spent-on-page.md) -dimensie is een afmeting op raakniveau. Als je dit opsplitst naar een andere dimensie, zal je de seconden vertellen dat een hit bleef waar ook de afbraakdimensie aanwezig was.
In het onderstaande voorbeeld is de zoekterm &#39;classificfieds&#39; gekoppeld aan raaktijden van 54 seconden, 59 seconden, enz., wat er wellicht op duidt dat bezoekers tijd doorbrengen bij het lezen van inhoud die voor die termijn is geretourneerd.

![ Schermafbeelding van een tijd die op paginapport wordt doorgebracht ](assets/time-spent1.png)

+++

+++Welke metrische waarde is geschikt voor de afmeting van [!UICONTROL Time Spent on Page – granular]?

Elke meting. De dimensie geeft de tijd weer die wordt besteed aan de exacte hit waar de gebeurtenis heeft plaatsgevonden. Hogere tijd betekent dat een bezoeker langer op een pagina (hit) is gebleven waar de gebeurtenis heeft plaatsgevonden.

![ het rapport dat van Workspace een douane metrisch gebruikt met een tijd doorgebrachte afmeting toont ](assets/time-spent2.png)

+++

+++Hoe verschilt [!UICONTROL Average Time Spent on Site] van [!UICONTROL Time Spent per Visit] ?

Het verschil is de noemer in metrisch:

* [[!UICONTROL Average time spent on site]](average-time-on-site.md) gebruikt de reeksen die een dimensie-item bevatten.

* [[!UICONTROL Time spent per visit]](time-spent-per-visit.md) gebruikt het aantal bezoeken

Dit heeft tot gevolg dat deze meetgegevens bij een bezoek vergelijkbare resultaten opleveren, maar dat ze bij een treffer anders zijn.

+++

+++Waarom komen de uitsplitstotalen met [!UICONTROL Average Time Spent on Site] niet overeen met het bovenliggende regelitem?

Omdat [!UICONTROL Average Time Spent on Site] van ongebroken opeenvolgingen van een dimensie afhangt, en het binnenrapport niet van het buitenrapport afhangt wanneer het berekenen van deze looppas.

Neem bijvoorbeeld het volgende bezoek.

| Nummer Actief | 1 | 2 | 3 |
|---|---|---|---|
| **bestede Seconden** | 30 | 100 | 10 |
| **de Naam van de Pagina** | Home | Product | Home |
| **Datum** | 1 jan. | 1 jan. | 1 jan. |

Bij het berekenen van de tijd die voor de Homepage wordt doorgebracht, zou deze (30+10)/2=20 zijn, maar het onderbreken van die tijd per dag zou geven (30+10)/1=40 aangezien de dag één enkele ononderbroken looppas van 1 Januari heeft.

Dit heeft tot gevolg dat deze meetgegevens bij een bezoek vergelijkbare resultaten opleveren, maar dat ze bij een treffer anders zijn.

+++

## Voorbeelden van [!UICONTROL Time Spent] -berekeningen

Veronderstel de volgende reeks servervraag voor één enkele bezoeker binnen één enkel bezoek is:

| Naar hit# | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|---|---|---|---|---|---|---|---|
| **Bezoek verstreken tijd (in sec)** | 0 | 30 | 80 | 180 | 190 | 230 | 290 |
| **bestede Seconden** | 30 | 50 | 100 | 10 | 40 | 60 | - |
| **Type van Actief** | Pagina | Koppeling | Pagina | Pagina | Pagina | Pagina | Pagina |
| **de Naam van de Pagina** | Home | - | Product | Home | Home (opnieuw laden) | Kar | Bevestiging van bestelling |
|  |  |  |  |  |  |  |  |
| **prop1** | A (set) | A (spread forward) | niet ingesteld | B (set) | B (set) | A(set) | C (set) |
| **prop1 bestede seconden** | 30 | 50 | - | 10 | 40 | 60 | - |
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

Tijd besteed per bezoek (korrelig): 290
Tijd besteed aan pagina (korrelig): 10, 30, 40, 50, 60, 100

Een aantal aanvullende opmerkingen ter ondersteuning van het voorbeeld:

* Alle gebruikte berekeningen zijn gebaseerd op de verstreken tijd van het bezoek, die bij de eerste treffer van het bezoek bij nul begint.

* &quot;Seconden besteed&quot; is het verschil tussen de tijdstempel van de huidige hit en de tijdstempel van de volgende hit. Als gevolg daarvan heeft de laatste treffer van het bezoek (en stormen) geen tijd doorgebracht.

* Een &quot;reeks&quot; is een opeenvolgende reeks resultaten waarbij een bepaalde variabele dezelfde waarde bevat (door deze in te stellen, door:sturen of blijvend). Bijvoorbeeld, prop1 &quot;A&quot;heeft twee opeenvolgingen: treffers 1 &amp; 2 en druk 6. Waarden bij de laatste treffer van het bezoek beginnen geen nieuwe reeks omdat de laatste treffer geen tijd heeft doorgebracht. De gemiddelde tijd die aan plaats wordt doorgebracht gebruikt opeenvolgingen in de noemer.

   * Alleen ten behoeve van de doorgebrachte tijd worden de punten &#39;doorgestuurd&#39;, van paginakoppen tot volgende treffers voor koppelingen, zoals hierboven voor pop1 op hit 2 wordt getoond. Hierdoor kan de waarde die is ingesteld voor prop1 bij hit 1 (&quot;A&quot;), de tijd verzamelen die is besteed aan hit 2.

   * Vars verzamelen de tijd die wordt besteed aan elke treffer waarbij de eVar is ingesteld of aanhoudt. De persistentie van eVar wordt gedefinieerd door de eVar-instellingen in Analytics > Admin.
