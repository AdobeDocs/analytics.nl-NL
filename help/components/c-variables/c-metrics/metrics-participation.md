---
description: De metriek van de participatie wijst volledige krediet van succesgebeurtenissen aan alle waarden van een eVar toe die tijdens een bezoek werden overgegaan. Metrische gegevens over deelname zijn handig om te bepalen welke pagina's, campagnes of andere aangepaste variabelewaarden het meest bijdragen aan het succes van uw site. De deelname is gebaseerd op bezoeken. Alle eVar waarden in een bezoek voorafgaand aan en met inbegrip van de klap wanneer een gebeurtenis voorkomt ontvangen deelnemingskrediet ongeacht het aflopen plaatsen.
title: Deelname
topic: Metrics
uuid: a7fa791d-0a77-429e-808e-4f97bb9ae5fc
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Deelname

De metriek van de participatie wijst volledige krediet van succesgebeurtenissen aan alle waarden van een eVar toe die tijdens een bezoek werden overgegaan. Metrische gegevens over deelname zijn handig om te bepalen welke pagina&#39;s, campagnes of andere aangepaste variabelewaarden het meest bijdragen aan het succes van uw site. De deelname is gebaseerd op bezoeken. Alle eVar waarden in een bezoek voorafgaand aan en met inbegrip van de klap wanneer een gebeurtenis voorkomt ontvangen deelnemingskrediet ongeacht het aflopen plaatsen.

Zie Deelname [bezoeker - Ad hoc Analyse](/help/components/c-variables/c-metrics/metrics-visitor-participation.md) voor meer informatie over hoe Ad hoc Analyse participatie gebruikt.

De metriek van de participatie heeft twee montages per omzettingsgebeurtenis:

* **Uitgeschakeld**: De standaardstatus van elke conversiegebeurtenis. Deelnamegegevens worden niet verzameld voor deze gebeurtenis.
* **Ingeschakeld**: Deelnamegegevens worden verzameld voor deze gebeurtenis.

> [!NOTE] U kunt deelname inschakelen voor maximaal 100 aangepaste gebeurtenissen. Buiten dat, kunt u deelnemingsmetriek in de [Berekende Bouwer van Metriek](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/participation_metric.html) tot stand brengen.

Wanneer deze optie is ingeschakeld, zijn deelnamemetriek automatisch beschikbaar in alle conversierapporten. Nochtans, kunnen de metriek van de participatie ook in specifieke verkeersrapporten op uw verzoek worden bekeken. U kunt naar keuze om deelnemingsmetriek verzoeken beschikbaar in bepaalde rapporten van het douaneverkeer zijn.

## Voorbeeld van deelname aan inkomsten {#section_DAB6C348201B454BB4ED01313AA777AF}

Stel de volgende volgorde in:

1. Een gebruiker navigeert naar uw site en zoekt naar &quot;schoenen&quot;.
1. De gebruiker zoekt vervolgens naar &quot;tennisschoenen&quot;.
1. De gebruiker klikt op een koppeling naar de productpagina, voegt het item toe aan de winkelwagentje en koopt $120.

Als u de inkomsten weergeeft in het rapport Interne zoektermen, ziet u het volgende op basis van de geselecteerde toewijzing:

* **Eerste**: &quot;schoenen&quot; krijgen krediet voor de $120. &quot;tennisschoenen&quot; zouden $0 krijgen.
* **Laatste**: &quot; tennisschoenen &quot; krijgen krediet voor de 120 dollar . &quot;schoenen&quot; krijgen $0.
* **Lineair**: Elke campagne zou $60 krediet krijgen.

   Deelname is vergelijkbaar met lineaire allocatie, behalve dat alle waarden volledig worden vergoed. Als u de optie Inkomsten (deelname) als maatstaf gebruikt, wordt de toewijzing genegeerd. In dit voorbeeld wordt $120 voor beide zoektermen gerapporteerd.

>[!MORELIKETHIS]
>
>* [Metrische berekeningen](/help/components/c-variables/c-metrics/metrics-calculations.md)

