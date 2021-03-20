---
title: Einde van levensduur voor bronnen van volledige verwerkingsgegevens
description: Redenen voor het einde van de levensduur en vergelijkingen tussen de API voor het invoegen van gegevens in bulk en de gegevensbronnen voor volledige verwerking.
translation-type: tm+mt
source-git-commit: 2e077db74b7719f49aec513fc99dad33a4d5b831
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 3%

---


# Einde van levensduur voor bronnen van volledige verwerkingsgegevens

Al enkele jaren kunt u met de Full Processing Data Sources gegevens op aanraakniveau naar Adobe Analytics verzenden. Deze gegevens zijn op dezelfde manier verwerkt als gegevens die zijn verzameld via onze JavaScript-bibliotheken en de SDK van de mobiele app. In 2020, gaf Adobe [Bulk API van de Invoeging van Gegevens](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) vrij, die de zelfde functies zoals Volledige Gegevensbronnen van de Verwerking, maar met extra eigenschappen uitvoert. Dit onderwerp verstrekt details over extra functionaliteit die door de Invoeging API van Gegevens van het Bulk wordt verstrekt en schetst verschillen in dossierformaten.

Vanaf 25 maart, 2021, zal Adobe nieuwe Volledige verbindingen van de Gegevensbronnen van de Verwerking verhinderen worden gecreeerd. Bestaande verbindingen blijven ondersteund totdat de service volledig is afgekeurd. De afschrijving vindt plaats in 2021, maar er is nog geen specifieke datum vastgesteld.

## Waarom zijn we aan het einde van deze functie?

De BDIA (Bulk Data Insertion API) biedt extra functionaliteit en bestrijkt alle gebruiksgevallen die worden ondersteund door Volledige verwerking. We geloven dat u beter van dienst bent met de API voor het invoegen van gegevens in bulk.

## Belangrijkste verschillen tussen de volledige gegevensbronnen van de Verwerking en de Invoeging API van de Gegevens van het Bulk

* Bij het invoegen van bulkgegevens kunnen meerdere bestanden worden verzonden die parallel kunnen worden verwerkt. U kunt Bezoekersgroepen gebruiken om de continuïteit van de bezoeker en de toewijzing van de eVar te garanderen.
* De Invoeging van de Gegevens van het bulk heeft gegevensbevestiging evenals fout behandelende mogelijkheden, zo verwijderend sommige administratieve werk van het voorleggen van klapgegevens.
* Bulk gegevens invoegen ondersteunt verschillende opties voor bezoekers-id&#39;s. U kunt zowel de Analytics-id als de Marketing Cloud-id verzenden (zie [Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) voor meer informatie). Bovendien, kunt u uw eigen identiteitskaart als [zaad gebruiken voor het produceren van ECID](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#customer-id-and-experience-cloud-visitor-id-seeds).
* De toevoeging van bulkgegevens steunt de Variabelen van Lijst en van de Context- Gegevens.
* De toevoeging van bulkgegevens steunt geen Activity Map gegevens.

## Belangrijkste verschillen in bestandsindeling en inhoud

* De toevoeging van bulkgegevens heeft een aantal extra vereiste gebieden. Zie de [documentatie](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) voor meer informatie.
* Voor continuïteit en attributie van bezoekers moeten rijen binnen bestanden in chronologische volgorde worden gesorteerd. Zie [Bezoekersgroepen](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#visitor-groups) voor meer informatie over de volgorde van bezoekersactiviteiten in verschillende bestanden.
* Voor het invoegen van bulkgegevens moeten bestanden .csv gecomprimeerd zijn in .gzip-indeling.
* BDIA gebruikt &quot;timestamp&quot;in plaats van &quot;date&quot;.

Voor meer details, zie de volgende vergelijking van de gebiedswaarden beschikbaar in de Invoeging van Gegevens van de Bulk (BDIA) en Volledige Gegevensbronnen van de Verwerking (FPDS).

## Vergelijking van de veldwaarden in BDIA en FPDS

| BDIA, FPDS, beide | BDIA-variabele | Variabele voor volledige verwerkingskolom | Beschrijving |
| --- | --- | --- | --- |
| BDIA | amlh | Niet ondersteund | Tip voor Adobe Audience Manager-locatie. Zie geldige id-waarden in de onderstaande tabel met lijsten voor AAM regio. |
| Beide | browserHeight | browserHeight | Browserhoogte in pixels (bijvoorbeeld 768) |
| Beide | browserWidth | browserWidth | Browserbreedte in pixels (bijvoorbeeld 1024) |
| Beide | campaign | campagne | Code voor bijhouden van conversiecampagne |
| Beide | channel | kanaal | Kanaaltekenreeks (bijvoorbeeld Sectie Sport) |
| Beide | colorDepth | colorDepth | Kleurdiepte van monitor in bits (bijvoorbeeld 24) |
| Beide | connectionType | connectionType | Verbindingstype van de bezoeker (LAN of modem) |
| BDIA | contextData.key | Niet ondersteund | Sleutelwaardeparen worden in opgegeven door de koptekst &quot;contextData.product&quot; of &quot;contextData.color&quot; te noemen |
| Beide | cookiesEnabled | cookiesEnabled | `Y` of  `N` voor als de bezoeker cookies van een eerste sessie ondersteunt |
| Beide | currencyCode | currencyCode | Valutacode inkomsten (bijvoorbeeld `USD`) |
| BDIA | clientID.[customerIDType].authState | Niet ondersteund | De geverifieerde status van de bezoeker. Ondersteunde waarden zijn: 0, 1, 2, UNKNOWN, AUTHENTICATED, LOGGED_OUT of &#39;&#39; (hoofdlettergevoelig). Twee opeenvolgende enkele citaten (&#39;&#39;) veroorzaken dat de waarde wordt weggelaten van het vraagkoord, dat aan 0 vertaalt wanneer de slag wordt gemaakt. Houd rekening met de ondersteunde numerieke waarden voor authState: 0 = UNKNOWN, 1 = AUTHENTICATED, 2 = LOGGED_OUT. Het customerIDType kan om het even welke alfanumerieke koord zijn, maar zou als case gevoelig moeten worden beschouwd. |
| BDIA | clientID.[customerIDType].id | Niet ondersteund | De klant-id die moet worden gebruikt. Het customerIDType kan om het even welke alfanumerieke koord zijn, maar zou als case gevoelig moeten worden beschouwd. |
| BDIA | clientID.[customerIDType].isMCSeed | Niet ondersteund | Of dit het zaad voor identiteitskaart van de Bezoeker van de Marketing Cloud is of niet. Ondersteunde waarden zijn: 0, 1, TRUE, FALSE, &#39;&#39; (hoofdlettergevoelig). Als u 0, FALSE of twee opeenvolgende enkele aanhalingstekens (&#39;&#39;) gebruikt, wordt de waarde weggelaten uit de querytekenreeks. Het customerIDType kan om het even welke alfanumerieke koord zijn, maar zou als case gevoelig moeten worden beschouwd. |
