---
source-git-commit: ec42c462ac98a49b89f0fae29b3b561a6afe7820
workflow-type: tm+mt
source-wordcount: '2353'
ht-degree: 0%

---
# Fragmenten

## Legacy Report Builder {#legacy-arb}

>[!IMPORTANT]
>
>Een nieuwe en gestroomlijnde [ Report Builder ](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/report-buider-overview) werd vrijgegeven op 16 oktober, 2024. Deze functie wordt ondersteund in Mac-, Windows- en webbrowsers.
>Deze verouderde Report Builder-invoegtoepassing werkt nog steeds. U kunt [ uw erfeniswerkboeken ](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/convert-workbooks) in nieuwe Report Builder omzetten.

## Rapporten &amp; Analytics-aankondiging aan het einde van de levensduur {#ra-eol}

>[!IMPORTANT]
>
>Effectief **Januari 17, 2024**, beëindigde Adobe Rapporten &amp; Analytics en zijn begeleidende rapporten en eigenschappen. Op dat moment werken de rapporten en analyses en alle bijbehorende rapporten en programma&#39;s niet meer. De rapporten, visualisaties en onderliggende technologie die energierapporten en -analyses niet meer voldoen aan de Adobe-technologienormen. De meeste functies voor rapporten en analyses zijn beschikbaar in Analysis Workspace. Voor informatie, zie [ malplaatjes van het Gebruik ](/help/analyze/analysis-workspace/templates/use-templates.md).
> 
>Sinds de release van Analysis Workspace in 2015 zijn de functionaliteit en mogelijkheden van Rapporten en Analytics verplaatst naar Analysis Workspace en is een drempel voor pariteit van de workflow bereikt. Deze kennisgeving legt het einde van de levensduur uit.
>
>Lees meer over de Rapporten &amp; de aankondiging van het Eind van Analytics [ ](https://www.adobe.com/go/analytics_rnaeol_en).

## Sorteeropties voor componenten {#components-sort-options}

| Optie | Functie |
|---------|----------|
| [!UICONTROL **geadviseerd**] | Hiermee sorteert u componenten met de componenten die boven aan de lijst worden aanbevolen. Componenten die het vaakst en het laatst door u of anderen in uw organisatie worden gebruikt, worden hoger weergegeven in de lijst. |
| [!UICONTROL **alfabetisch**] | Hiermee worden componenten alfabetisch gesorteerd. |
| [!UICONTROL **Categorisch**] | Sorteert componenten volgens componenttype (afmetingen, metrisch, segment, datumbereik). |

{style="table-layout:auto"}

## Beperkte tests voor releasefase {#release-limited-testing}

>[!AVAILABILITY]
>
>De functionaliteit die in dit artikel wordt beschreven, bevindt zich in de Beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het de versieproces van de Analyse, zie [ de eigenschapversies van Adobe Analytics ](/help/release-notes/releases.md).

## Beperkte testsectie voor releasefase {#release-limited-testing-section}

>[!AVAILABILITY]
>
>De in deze sectie beschreven functionaliteit bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het de versieproces van de Analyse, zie [ de eigenschapversies van Adobe Analytics ](/help/release-notes/releases.md).


## Dislaimer plug-in {#plug-in}

>[!IMPORTANT]
>
>Deze insteekmodule wordt door Adobe Consulting geleverd als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De Adobe Customer Care biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met het Adobe-accountteam van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.


## Alleen beschikbaar voor bestaande klanten {#available-existing-customers}

>[!AVAILABILITY]
>
>De in deze sectie beschreven functionaliteit is alleen beschikbaar voor bestaande klanten die al een licentie voor de functionaliteit hebben. De functionaliteit wordt niet meer aangeboden als een extra toevoeging aan bestaande of nieuwe klanten.
>



## Attributiemodellen {#attribution-models-details}

Een attributiemodel bepaalt welke afmetingspunten krediet voor metrisch krijgen wanneer de veelvoudige waarden binnen het terugkijkvenster van metrisch worden gezien. Attributiemodellen zijn alleen van toepassing wanneer er meerdere dimensieitems zijn ingesteld in het terugzoekvenster. Als slechts één dimensie-item is ingesteld, krijgt dat dimensie-item 100% krediet, ongeacht het gebruikte attributiemodel.

| Pictogram | Attributiemodel | Definitie |
| :---: | :--- | --- |
| ![ Laatste aanraking ](/help/assets/icons/AttributeLastTouch.svg) | Laatste aanraking | Geeft 100% krediet aan het aanraakpunt dat het laatst voor de conversie optrad. Dit attributiemodel is doorgaans de standaardwaarde voor elke meting waarbij een attributiemodel niet op andere wijze is opgegeven. Organisaties gebruiken dit model doorgaans wanneer de conversietijd relatief kort is, zoals bij het analyseren van interne zoektrefwoorden. |
| ![ eerste aanraking ](/help/assets/icons/AttributeFirstTouch.svg) | Eerste aanraking | Geeft 100% krediet aan het aanraakpunt dat het eerst wordt weergegeven in het terugkijkvenster van de attributie. Organisaties gebruiken dit model doorgaans om inzicht te krijgen in merkbekendheid of aanschaf door klanten. |
| ![ Lineair ](/help/assets/icons/AttributeLinear.svg) | Lineair | Biedt hetzelfde krediet aan elk aanraakpunt dat wordt weergegeven voor een conversie. Dit is handig wanneer conversiecycli langer zijn of een frequentere betrokkenheid van klanten vereisen. Organisaties gebruiken dit toewijzingsmodel doorgaans om de doeltreffendheid van meldingen voor mobiele apps of voor producten op abonnementsbasis te meten. |
| ![Deelname](/help/assets/icons/AttributeParticipation.svg) | Deelname | Biedt 100% krediet aan alle unieke aanraakpunten. Aangezien elk aanraakpunt 100% krediet ontvangt, komt het metrische gegeven meestal uit op meer dan 100%. Als een dimensie-item meerdere afzonderlijke keren vóór een conversie wordt weergegeven, worden de waarden gededupliceerd naar 100%. Dit attributiemodel is ideaal in situaties waarin u wilt begrijpen welke aanraakpunten klanten het meest worden blootgesteld. Mediaorganisaties gebruiken dit model doorgaans om de snelheid van de inhoud te berekenen. De detailhandelorganisaties gebruiken typisch dit model om te begrijpen welke delen van hun plaats aan omzetting kritiek zijn. |
| ![ Zelfde aanraking ](/help/assets/icons/AttributeSameTouch.svg) | Zelfde aanraking | Verleent 100% krediet aan de zelfde gebeurtenis waar de omzetting plaatsvond. Als er geen aanraakpunt plaatsvindt op dezelfde gebeurtenis als bij een conversie, wordt dit punt ingesloten onder &quot;Geen&quot;. Dit attributiemodel wordt soms gelijkgesteld met het hebben van helemaal geen attributiemodel. Het is waardevol in scenario&#39;s waar u geen waarden van andere gebeurtenissen wilt die beïnvloeden hoe metrisch krediet aan afmetingspunten geeft. Product- of ontwerpteams kunnen dit model gebruiken om de doeltreffendheid van een pagina te beoordelen waar conversie plaatsvindt. |
| ![ Vormde U ](/help/assets/icons/AttributeUShaped.svg) | U-vorm | Biedt 40% krediet aan de eerste interactie, 40% aan de laatste interactie, en verdeelt de resterende 20% aan om het even welke aanraakpunten tussenin. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt aan beide een krediet van 50% toegekend. Dit attributiemodel wordt het best gebruikt in scenario&#39;s waar u eerste en laatste interactie het meest waart, maar wil geen extra interacties binnen volledig sluiten. |
| ![ Curve van J ](/help/assets/icons/AttributeJCurve.svg) | J Curve | Geeft 60% krediet aan de laatste interactie, 20% krediet aan de eerste interactie, en verdeelt de resterende 20% aan om het even welke aanraakpunten tussenin. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt 75% aan de laatste interactie besteed en wordt 25% aan de eerste. Net als bij U-Shaped, geeft dit attributiemodel de voorkeur aan de eerste en laatste interacties, maar is het zwaarder van belang voor de laatste interactie. |
| ![ Omgekeerde J ](/help/assets/icons/AttributeInverseJ.svg) | Omgekeerd J | Biedt 60% krediet aan het eerste aanraakpunt, 20% aan het laatste aanraakpunt en verdeelt de resterende 20% aan de tussenliggende aanraakpunten. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt 75% aan de eerste interactie toegekend en wordt 25% aan de laatste toegekend. Net als voor J-Shaped, geeft dit attributiemodel de voorkeur aan de eerste en laatste interacties, maar eerder de eerste interactie. |
| ![ Verval van de Tijd ](/help/assets/icons/AttributeTimeDecay.svg) | Tijdverlies | Volgt een exponentieel verval met een aangepaste parameter voor de halfwaardetijd, waarbij de standaardwaarde 7 dagen is. Het gewicht van elk kanaal is afhankelijk van de hoeveelheid tijd die is verstreken tussen het starten van het aanraakpunt en de uiteindelijke conversie. De formule die wordt gebruikt om krediet te bepalen is `2^(-t/halflife)`, waarbij `t` de hoeveelheid tijd tussen een aanraakpunt en een conversie is. Alle aanraakpunten worden vervolgens genormaliseerd tot 100%. Ideaal voor scenario&#39;s waarin u de toewijzing wilt meten aan de hand van een specifieke en significante gebeurtenis. Hoe langer een conversie plaatsvindt na deze gebeurtenis, hoe minder krediet wordt gegeven. |
| ![Aangepast](/help/assets/icons/AttributeCustom.svg) | Aangepast | Hiermee kunt u de gewichten opgeven die u wilt geven aan het eerste aanraakpunt, het laatste aanraakpunt en de tussenliggende aanraakpunten. De opgegeven waarden worden genormaliseerd naar 100%, zelfs als de ingevoerde aangepaste getallen niet bij 100 komen te liggen. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor interactie met twee aanraakpunten wordt de middelste parameter genegeerd. De eerste en laatste aanraakpunten worden vervolgens genormaliseerd tot 100% en de kredieten worden dienovereenkomstig toegewezen. Dit model is ideaal voor analisten die volledige controle willen hebben over hun attributiemodel en specifieke behoeften hebben waaraan andere attributiemodellen niet voldoen. |
| ![ Algorithmic ](/help/assets/icons/AttributeAlgorithmic.svg) | Algorithmic | Gebruikt statistische technieken om dynamisch de optimale allocatie van krediet voor de geselecteerde maatstaf vast te stellen. Het algoritme dat wordt gebruikt voor attributie is gebaseerd op de Harsanyi Dividend van coöperatieve speltheorie. Het dividend van Harsanyi is een generalisering van de Shapley-waardeoplossing (genoemd naar Lloyd Shapley, een Nobelprijswinnaar) voor het verdelen van krediet onder spelers in een spel met ongelijke bijdragen aan de uitkomst.<br> op een hoog niveau, wordt de attributie berekend als coalitie van spelers waaraan een overschot billijk moet worden verdeeld. De overtollige verdeling van elke coalitie wordt bepaald volgens het overschot dat eerder door elke subcoalitie (of eerder deelnemende dimensie-items) recursief werd gecreeerd. Voor meer details, zie John Harsanyi en de originele documenten van Lloyd Shapley:<br> Shapley, Lloyd S. (1953). Een waarde voor spelletjes van één persoon. *bijdragen aan de Theorie van Spelen, 2 (28)*, 307-317.<br> Harsanyi, John C. (1963). Een vereenvoudigd onderhandelingsmodel voor het on-person coöperatieve spel. *Internationale Economische Controle 4 (2)*, 194-220. |

{style="table-layout:auto"}

## Atributie terugzoekvenster {#attribution-lookback-window}

Een terugzoekvenster is de hoeveelheid tijd die een conversie moet terugkijken om aanraakpunten op te nemen. Als een dimensie-item buiten het terugzoekvenster wordt ingesteld, wordt de waarde niet opgenomen in attributieberekeningen.

* **14 Dagen**: Zoekt file tot 14 dagen vanaf toen de omzetting gebeurde.
* **30 Dagen**: Zoekt file tot 30 dagen vanaf toen de omzetting gebeurde.
* **60 Dagen**: Zoekt file tot 60 dagen vanaf toen de omzetting gebeurde.
* **90 Dagen**: Zoekt file tot 90 dagen vanaf toen de omzetting gebeurde.
* **Bezoek**: Zoekt file aan het begin van het bezoek waar een omzetting gebeurde.
* **Bezoeker (Meldend Venster)**: Zoekt bij alle bezoeken file tot de eerste van de maand van de huidige datumwaaier. Als het bereik van de rapportdatum bijvoorbeeld 15 september tot en met 30 september is, omvat het bereik van de terugzoekdatum van de bezoeker 1 september tot en met 30 september. Als u dit terugkijkvenster gebruikt, kunt u soms zien dat de afmetingspunten aan data buiten uw rapporterend venster worden toegeschreven.
* **Tijd van de Douane:** staat u toe om een venster van de douaneterugblik van te plaatsen wanneer een omzetting gebeurde. U kunt het aantal minuten, uren, dagen, weken, maanden of kwartalen opgeven. Bijvoorbeeld, als een omzetting op 20 februari gebeurde, zou een terugkijkvenster van vijf dagen alle afmetingstips van 15 februari tot 20 februari in het attributiemodel evalueren.

## Voorbeeld van kenmerk {#attribution-example}

Bekijk het volgende voorbeeld:

1. Op 15 september arriveert een persoon via een betaalde zoekadvertentie naar uw site en verlaat hij vervolgens.
1. Op 18 september arriveert de persoon opnieuw naar uw site via een link naar sociale media die hij van een vriend heeft gekregen. Ze voegen verschillende artikelen aan hun winkelwagentje toe, maar kopen niets.
1. Op 24 september stuurt uw marketingteam hen een e-mail met een coupon voor sommige objecten in hun winkelwagentje. Ze passen de coupon toe, maar gaan naar verschillende andere sites om te zien of er andere coupons beschikbaar zijn. Ze vinden een andere advertentie via een advertentie en kopen uiteindelijk $50.

Afhankelijk van het terugkijkvenster en het attributiemodel, ontvangen de kanalen verschillende kredieten. Hieronder volgen enkele voorbeelden:

* Gebruikend **eerste aanraking** en venster van de a **zittingsterugblik**, kijkt de attributie slechts het derde bezoek. Tussen e-mail en display was e-mail de eerste, dus e-mail krijgt 100% krediet voor de aankoop van $50.

* Gebruikend **eerste aanraking** en venster van de a **persoonraadpleging**, kijkt de attributie naar alle drie bezoeken. De betaalde zoekopdracht was de eerste, dus krijgt deze 100% krediet voor de aankoop van $50.

* Gebruikend **lineair** en venster van de a **zittingsterugblik**, is het krediet verdeeld tussen e-mail en vertoning. Beide kanalen krijgen elk $25 krediet.
Gebruikend **lineair** en het venster van de a **persoonraadpleging**, wordt het krediet verdeeld tussen betaald onderzoek, sociaal, e-mail, en vertoning. Elk kanaal krijgt $12,50 krediet voor deze aankoop.

* Gebruikend **j-Gegeld** en a **persoon terugkijkvenster**, wordt het krediet verdeeld tussen betaald onderzoek, sociaal, e-mail, en vertoning.

   * 60% krediet wordt gegeven aan vertoning, voor $30.
   * 20% krediet wordt gegeven voor betaalde zoekopdrachten, voor $10.
   * De resterende 20% is verdeeld tussen sociale media en e-mail, wat elk $5 geeft.

* Gebruikend **Verval van de Tijd** en venster van de a **persoonraadpleging**, wordt het krediet verdeeld tussen betaald onderzoek, sociaal, e-mail, en vertoning. De standaardhalfwaardetijd van 7 dagen gebruiken:

   * Tussenruimte van nul dagen tussen aanraakpunt weergeven en conversie. `2^(-0/7) = 1`
   * Ruimte van nul dagen tussen aanraakpunt en conversie via e-mail. `2^(-0/7) = 1`
   * Tussenruimte van zes dagen tussen sociale aanraakpunten en conversie. `2^(-6/7) = 0.552`
   * Tussenruimte van negen dagen tussen betaald aanraakpunt en conversie. `2^(-9/7) = 0.41`
   * Het normaliseren van deze waarden resulteert in het volgende:

      * Weergave: 33,8%, krijgt $16,88
      * E-mail: 33,8% ontvangt $ 16,88
      * Sociaal: 18,6%, $ 9,32
      * Betaalde zoekopdracht: 13,8%, krijgt $6,92

Conversiegebeurtenissen die doorgaans hele getallen bevatten, worden gedeeld als het krediet tot meer dan één kanaal behoort. Als twee kanalen bijvoorbeeld een bijdrage leveren aan een bestelling met behulp van een lineair toewijzingsmodel, krijgen beide kanalen 0,5 van die volgorde. Deze gedeeltelijke metriek worden samengevat over alle mensen dan rond gemaakt aan het dichtstbijzijnde geheel voor rapportering.

## Reisvisualisatievergelijkingen {#journey-visualization-comparisons}

Diverse visualisaties in de analyse van de Reis van de Klant worden ontworpen om de reizen te analyseren u aan uw klanten verstrekt.

Gebruik de volgende informatie om de visualisatie te kiezen die het beste aan uw behoeften voldoet.

| Functie | Reiscanvas | Fallout | Stroom |
|---------|----------|---------|---------|
| **Vooraf bepaalde opeenvolging van pagina&#39;s** | Ja </br> Combineert vooraf bepaalde en verkennende analyse. Het uiteindelijke pad wordt gebruikt wanneer vooraf gedefinieerde knooppunten op het pad worden gebruikt (bezoekers worden meegeteld zolang ze uiteindelijk van het ene vooraf gedefinieerde knooppunt naar het andere gaan). De directe (niet uiteindelijke) volgende knopen kunnen ook worden getoond. | Ja </br> de weg kan een uiteindelijke weg zijn of kan aan volgende aanraakpunt worden beperkt | Nee |
| **Verkennende opeenvolging van pagina&#39;s (ad hoc analyse)** | Ja </br> Combineert vooraf bepaalde en verkennende analyse. Het uiteindelijke pad wordt gebruikt wanneer vooraf gedefinieerde knooppunten op het pad worden gebruikt (bezoekers worden meegeteld zolang ze uiteindelijk van het ene vooraf gedefinieerde knooppunt naar het andere gaan). De directe (niet uiteindelijke) volgende knopen kunnen ook worden getoond. | Beperkt </br> staat u toe om directe reserve in een lijst van de Vrije vorm met de rechtermuisknop aan te klikken en te bekijken. | Ja </br> Verkennende slechts analyse. Altijd binnen één afmetingsinstantie tussen knooppunten. Dit betekent dat elk knooppunt het directe (niet uiteindelijke) volgende aanraakpunt langs het pad weergeeft. |
| **toont waar de mensen weggingen (uit vielen) en door (door vielen) werden voortgezet** | Ja </br> toont voor zowel vooraf bepaalde als verkennende reizen | Ja </br> toont vooraf bepaalde reizen | Ja </br> toont voor verkennende reizen |
| **Lineaire reizen** | Ja | Ja | Nee |
| **niet-lineaire reizen met veelvoudige ingangspunten en wegen** | Ja | Nee | Ja |
| **Primaire metrisch** | Elke metrische waarde, inclusief berekende metriek | Alleen sessie of persoon | Alleen voorkomen (padweergaven) |
| **Secundaire metrische** | Ja<p>Elke metrische waarde, inclusief berekende metriek</p> | Nee | Nee |
| **de steun van de Component in knopen of touchpoints** | Metriek, afmetingsitems, filters en datumbereiken. | Metriek, afmetingsitems, filters en datumbereiken. | Alleen afmetingsitems (behalve het begin- en eindpunt) |
| **vergelijk filters** | Nee | Ja<p>Voer zij aan zij vergelijkingen van twee verschillende filters in het zelfde rapport uit.</p> | Nee |
| **belemmering-en-dalingscomponenteninteractie** | Ja | Ja | Nee |
| **reizen van Adobe Journey Optimizer** | Ja </br> Open reizen van Journey Optimizer voor diepere analyse en aanpassing | Nee | Nee |

{style="table-layout:auto"}
