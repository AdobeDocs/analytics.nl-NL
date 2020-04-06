---
description: 'null'
title: Overzicht van het deelvenster Kenmerken
uuid: bb345642-4f45-4fb8-82d0-803248dd52ea
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Overzicht van het deelvenster Kenmerken

>[!IMPORTANT] Het deelvenster Kenmerken is beschikbaar voor alle klanten van de Adobe Analytics Ultimate-, Premier-, Select- en Foundation-SKU&#39;s.

Het attributiepaneel is een [Attribution IQ](../../attribution-iq.md) -functie waarmee u veel nieuwe typen attributiemodellen kunt toevoegen aan vrije-vormtabellen, visualisaties en berekende metriek. Alle attributiemodellen hebben twee componenten:

* **Attributiemodel:** Het model beschrijft de distributie van omzettingen in de klappen in een groep. Bijvoorbeeld, eerste aanraking of laatste aanraking.
* **Het terugkijkvenster van de attributen:** In het terugzoekvenster wordt beschreven welke groepen hits worden beschouwd voor elk model. Bijvoorbeeld bezoek of bezoeker.

## Attributiemodellen

| UI-pictogram | Attributiemodel | Definitie | Wanneer gebruiken |
| --- | --- | --- | --- |
| ![Laatste aanraking](assets/last_touch1.png) | Laatste aanraking | Geeft 100% krediet aan het aanraakpunt dat het laatst voor de conversie optrad. | Het eenvoudigste en meest gangbare attributiemodel. Het wordt vaak gebruikt voor omzettingen met een korte bezinningscyclus. Last Touch wordt vaak gebruikt door teams die marketingacties voor zoekopdrachten beheren of interne zoektrefwoorden analyseren. |
| ![Eerste aanraking](assets/first_touch.png) | Eerste aanraking | Biedt 100% krediet aan het aanraakpunt dat het eerst in het terugkijkvenster van de attributie wordt gezien. | Een ander algemeen attributiemodel dat nuttig is voor het analyseren van marketingkanalen die bedoeld zijn om merkbekendheid te geven of klanten aan te trekken. Het wordt vaak gebruikt door display- of sociale marketingteams, maar is ook ideaal voor het beoordelen van de doeltreffendheid van on-site productaanbevelingen. |
| ![Zelfde aanraking](assets/same_touch.png) | Zelfde aanraking | Verleent 100% krediet aan de klap waar de omzetting plaatsvond. Als een aanraakpunt niet optreedt bij dezelfde druk als bij een conversie, wordt het item ingesloten onder &quot;Geen&quot;. | Een handig model bij het evalueren van de inhoud of gebruikerservaring die direct op het moment van de conversie werd gepresenteerd. Product- of ontwerpteams gebruiken dit model vaak om de doeltreffendheid van een pagina te beoordelen waar conversie plaatsvindt. |
| ![Lineair](assets/linear.png) | Lineair | Biedt hetzelfde krediet aan elk aanraakpunt dat wordt weergegeven voor een conversie. | Nuttig voor conversies met langere omrekeningscycli of gebruikerservaring die frequentere betrokkenheid van klanten vereisen. Het wordt vaak gebruikt door teams die de doeltreffendheid van meldingen voor mobiele apps meten of met producten op basis van abonnementen. |
| ![U-vorm](assets/u_shaped.png) | U-vorm | Biedt 40% krediet aan de eerste interactie, 40% aan de laatste interactie, en verdeelt de resterende 20% aan om het even welke aanraakpunten tussenin. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt aan beide een krediet van 50% toegekend. | Een goed model voor degenen die interacties waarderen die een omzetting introduceerden of gesloten, maar nog steeds hulpinteractie willen erkennen. De U-Vormen attributie wordt algemeen gebruikt door teams die een evenwichtigere benadering kiezen maar meer krediet aan kanalen willen geven die gevonden of gesloten een omzetting. |
| ![J-Shaped](assets/j_shaped.png) | J-Shaped | Geeft 60% krediet aan de laatste interactie, 20% krediet aan de eerste interactie, en verdeelt de resterende 20% aan om het even welke aanraakpunten tussenin. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt 75% aan de laatste interactie besteed en wordt 25% aan de eerste. | Dit model is ideaal voor diegenen die aan vinders en sluiters voorrang geven, maar zich willen concentreren op het sluiten van interacties. De J-Vormen attributie wordt vaak gebruikt door teams die een evenwichtigere benadering kiezen en meer krediet aan kanalen willen geven die een omzetting sluiten. |
| ![Omgekeerde J-vorm](assets/inverse_j.png) | Omgekeerd J | Biedt 60% krediet aan het eerste aanraakpunt, 20% aan het laatste aanraakpunt en verdeelt de resterende 20% aan de tussenliggende aanraakpunten. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt 75% aan de eerste interactie toegekend en wordt 25% aan de laatste toegekend. | Dit model is ideaal voor diegenen die prioriteit geven aan vinders en sluiters, maar zich willen richten op het zoeken naar interacties. De attributie Inverse J wordt gebruikt door teams die een evenwichtigere benadering kiezen en meer krediet willen geven aan kanalen die een omzetting in gang hebben gezet. |
| ![Aangepast](assets/custom.png) | Aangepast | Hiermee kunt u de gewichten opgeven die u wilt geven aan de eerste aanraakpunten, de laatste aanraakpunten en de tussenliggende aanraakpunten. De opgegeven waarden worden genormaliseerd naar 100%, zelfs als de ingevoerde aangepaste getallen niet bij 100 komen te liggen. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor interactie met twee aanraakpunten wordt de middelste parameter genegeerd. De eerste en laatste aanraakpunten worden vervolgens genormaliseerd tot 100% en de kredieten worden dienovereenkomstig toegewezen. | Dit model is ideaal voor diegenen die volledige controle over hun attributiemodel willen en specifieke behoeften hebben die andere attributiemodellen niet vervullen. |
| ![Tijdverlies](assets/time_decay.png) | Verval | Volgt en exponentieel verval met een aangepaste parameter voor de halfwaardetijd, waarbij de standaardwaarde 7 dagen is. Het gewicht van elk kanaal is afhankelijk van de hoeveelheid tijd die is verstreken tussen het starten van het aanraakpunt en de uiteindelijke conversie. De formule die wordt gebruikt om krediet te bepalen is `2^(-t/halflife)`, waarbij `t` de hoeveelheid tijd tussen een aanraakpunt en een conversie is. Alle aanraakpunten worden vervolgens genormaliseerd tot 100%. | Ideaal voor teams die regelmatig videoreclame of -markten uitvoeren tegen evenementen met een vooraf bepaalde datum. Hoe langer een conversie plaatsvindt na een marketinggebeurtenis, hoe minder krediet wordt gegeven. |
| ![Deelname](assets/participation.png) | Deelname | Biedt 100% krediet aan alle unieke aanraakpunten. Het totale aantal omzettingen wordt opgevoerd in vergelijking met andere attributiemodellen. De participatie dedupliceert kanalen die veelvoudige tijden worden gezien. | Uitstekend om te begrijpen wie vaak klanten worden blootgesteld aan een bepaalde interactie. Mediaorganisaties gebruiken dit model vaak om de snelheid van de inhoud te berekenen. De detailhandelorganisaties gebruiken vaak dit model om te begrijpen welke delen van hun plaats aan omzetting kritiek zijn. |

>[!NOTE] Het volgende algoritmische toewijzingsmodel is momenteel beschikbaar in [Adobe Analytics Labs](https://docs.adobe.com/content/help/en/analytics/analyze/tech-previews/overview.html) en zal uiteindelijk deel uitmaken van een algemene release.

| UI-pictogram | Attributiemodel | Definitie | Wanneer gebruiken |
| --- | --- | --- | --- |
| ![Algorithmic](assets/algorithmic.png) | [Algorithmic](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/algorithmic.md) | Gebruikt statistische technieken om dynamisch de optimale allocatie van krediet voor de geselecteerde maatstaf vast te stellen. | Nuttig om guesswork of heuristiek te voorkomen wanneer u het juiste toewijzingsmodel voor uw bedrijf kiest. |

## Venster opzoeken

Een terugzoekvenster is de hoeveelheid tijd die een conversie moet terugkijken om aanraakpunten op te nemen. Attributiemodellen die meer krediet geven aan de eerste interacties zien grotere verschillen bij het weergeven van verschillende terugkijkvensters.

* **Het terugkijkvenster van de bezoek:** Kijkt terug naar het begin van het bezoek waar een conversie plaatsvond. De terugkijkvensters van het bezoek zijn smal, aangezien zij niet voorbij het bezoek kijken. De raadplegingsvensters van het bezoek respecteren de gewijzigde bezoekdefinitie in virtuele rapportreeksen.

* **Het terugkijkvenster van de bezoeker:** Kijkt naar alle bezoeken terug tot de eerste van de maand van de huidige datumwaaier. De terugkijkvensters van de bezoeker zijn breed, aangezien zij vele bezoeken kunnen overspannen. Als het bereik van de rapportdatum bijvoorbeeld 15 september tot en met 30 september is, omvat het bereik van de terugzoekdatum van de bezoeker 1 september tot en met 30 september.

## Voorbeeld

Bekijk het volgende voorbeeld:

1. Op 15 september arriveert een bezoeker via een betaalde zoekadvertentie naar uw site en verlaat vervolgens zijn site.
2. Op 18 september arriveert de bezoeker opnieuw naar uw site via een link naar sociale media die hij van een vriend heeft gekregen. Ze voegen verschillende artikelen aan hun winkelwagentje toe, maar kopen niets.
3. Op 24 september stuurt uw marketingteam hen een e-mail met een coupon voor sommige objecten in hun winkelwagentje. Ze passen de coupon toe, maar gaan naar verschillende andere sites om te zien of er andere coupons beschikbaar zijn. Ze vinden een andere advertentie via een advertentie en kopen uiteindelijk $50.

Afhankelijk van het terugkijkvenster en het attributiemodel, ontvangen de kanalen verschillende kredieten. Hieronder volgen enkele belangrijke voorbeelden:

* Met **eerste aanraking** en een **bezoek terugkijkvenster**, kijkt de attributie slechts naar het derde bezoek. Tussen e-mail en display was e-mail de eerste, dus e-mail krijgt 100% krediet voor de aankoop van $50.
* Met **eerste aanraking** en een terugkijkvenster **van de** bezoeker, kijkt de attributie naar alle drie bezoeken. De betaalde zoekopdracht was de eerste, dus krijgt deze 100% krediet voor de aankoop van $50.
* Met **lineair** en een **venster** voor het terugzoeken van bezoekers wordt het krediet verdeeld over e-mail en de weergave. Beide kanalen krijgen elk $25 krediet.
* Met **lineair** en een terugkijkvenster **van de** bezoeker wordt het krediet verdeeld tussen betaalde onderzoek, sociaal, e-mail, en vertoning. Elk kanaal krijgt $12,50 krediet voor deze aankoop.
* Met **J-vormig** en een terugkijkvenster **van de** bezoeker, is de krediet verdeeld tussen betaalde onderzoek, sociale, e-mail, en vertoning.
   * 60% krediet wordt gegeven aan vertoning, voor $30.
   * 20% krediet wordt gegeven voor betaalde zoekopdrachten, voor $10.
   * De resterende 20% is verdeeld tussen sociale media en e-mail, wat elk $5 geeft.
* Met **Tijdverlies** en een terugzoekvenster **van de** bezoeker wordt het krediet verdeeld over betaalde zoekopdracht, sociale gegevens, e-mail en weergave. De standaardhalfwaardetijd van 7 dagen gebruiken:
   * Tussenruimte van 0 dagen tussen aanraakpunt weergeven en conversie. `2^(-0/7) = 1`
   * Tussenruimte van 0 dagen tussen aanraakpunt en conversie via e-mail. `2^(-0/7) = 1`
   * Tussenruimte van 6 dagen tussen sociale aanraakpunten en conversie. `2^(-6/7) = 0.552`
   * Tussenruimte van 9 dagen tussen betaald aanraakpunt en conversie. `2^(-9/7) = 0.41`
   * Het normaliseren van deze waarden resulteert in het volgende:
      * Weergave: 33,8%, $ 16,88
      * E-mail: 33,8% voor $ 16,88
      * Sociaal: 18,6%, krijgt $ 9,32
      * Betaalde zoekopdracht: 13,8%, met $ 6,92

>[!TIP] Andere conversiegebeurtenissen, zoals orders of aangepaste gebeurtenissen, worden ook verdeeld als de kredieten tot meer dan één kanaal behoren. Als twee kanalen bijvoorbeeld via een lineair toewijzingsmodel een bijdrage leveren aan een aangepaste gebeurtenis, krijgen beide kanalen 0,5 van de aangepaste gebeurtenis. Deze gebeurtenisfracties worden bij alle bezoeken opgeteld en vervolgens afgerond naar het dichtstbijzijnde gehele getal voor rapportage.

## Kenmerken gebruiken met marketingkanalen

Toen de marketingkanalen voor het eerst werden geïntroduceerd, hadden ze alleen de eerste en laatste aanraakafmetingen. Met deze extra attributiemodellen zijn expliciete eerste/laatste aanraakafmetingen niet meer nodig. Adobe biedt algemene afmetingen voor **marketingkanalen** , zodat deze kunnen worden gebruikt met het gekozen toewijzingsmodel. Deze generieke de afmetingen van de Kanalen van de Marketing gedragen zich identiek aan de Afmetingen van het Kanaal van de Laatste Aanraking, maar verschillend geëtiketteerd om verwarring te verhinderen wanneer het gebruiken van marketing kanalen met een verschillend attributiemodel.

Aangezien de afmetingen van de marketingkanalen afhankelijk zijn van een traditionele &quot;visit&quot;-definitie (zoals gedefinieerd door hun verwerkingsregels), kan de definitie van hun &quot;visit&quot; niet worden gewijzigd met behulp van virtuele-rapportsuites.

## Kenmerken gebruiken met variabelen van meerdere waarden

Sommige afmetingen in Analytics kunnen veelvoudige waarden op één enkele slag bevatten. Veelvoorkomende voorbeelden zijn list vars en de productvariabele.

Wanneer de attributie wordt toegepast op multi-value klappen, krijgen alle waarden in de zelfde klappers de zelfde creditering. Aangezien vele waarden dit krediet kunnen ontvangen, kan het rapporttotaal verschillend zijn dan als u elk individueel lijnpunt samenstelde. Het rapporttotaal wordt gededupliceerd, terwijl elke afzonderlijke waarde van de dimensie juiste kredieten krijgt.

## Kenmerken gebruiken met segmentatie

Attributie wordt altijd uitgevoerd vóór segmentatie en segmentatie wordt uitgevoerd voordat rapportfilters worden toegepast. Dit concept is ook op virtuele rapportsuites van toepassing gebruikend segmenten.

Als u bijvoorbeeld een VRS maakt met een toegepast segment &quot;Weergaveits&quot;, kunt u andere kanalen in een tabel zien met behulp van bepaalde attributiemodellen.

![Virtuele rapportsuite met alleen weergave](assets/vrs-aiq-example.png)

>[!NOTE] Als een segment klappen onderdrukt die uw metrisch bevatten, zullen die metrische instanties niet aan om het even welke afmeting worden toegeschreven. Nochtans, zal een gelijkaardig rapportfilter eenvoudig sommige afmetingswaarden verbergen, zonder enige invloed op metriek die per het attributiemodel wordt verwerkt. Als gevolg hiervan kunnen een segment en filter met vergelijkbare definities soms lagere waarden voor het segment retourneren.
