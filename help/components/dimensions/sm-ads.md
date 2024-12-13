---
title: Streaming media en afmetingen
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Ads] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: 3f17bacc-8c36-499a-a863-9298e2d54370
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Streaming media en afmetingen

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Ads] voor een rapportreeks toelaat. Zie [ Streaming Media en metriek ](../metrics/sm-ads.md) voor beschikbare metriek.*

Streaming media en dimensies bieden extra rapportagefunctionaliteit voor gegevensverzameling via bibliotheken voor het streamen van media. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Streaming Media Collection]** vereist. Neem contact op met het accountteam van de Adobe voor meer informatie.

Wanneer u **[!UICONTROL Media Ads]** onder [ Media die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Naam Dimension | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Advertentie | De unieke id voor de advertentie. | Advertentie starten, en sluiten | `a.media.ad.name` |
| Advertentienaam (variabele) | De vriendelijke naam van de advertentie. Er is ook een classificatiedimensie met de naam &#39;Advertentienaam&#39; beschikbaar, die een soortgelijk doel biedt. Deze dimensie en de classificatie worden behandeld als twee verschillende dimensies. | Advertentie starten, en sluiten | `a.media.ad.friendlyName` |
| Naam van speler toevoegen | De naam van de speler die de advertentie rendert. | Advertentie starten, en sluiten | `a.media.ad.playerName` |
| Ad length (variabel) | De lengte van de video en, in seconden. | Advertentie starten, en sluiten | `a.media.ad.length` |
| Pod Advertentie | De unieke id voor de advertentiepod. | Advertentie starten, en sluiten | `a.media.ad.pod` |
| Positie van advertentie | De indexpositie van de advertentie binnen het bovenliggende element en het einde (geïndexeerd op 0). | Advertentie starten, en sluiten | `a.media.ad.podPosition` |
| Adverteerder | Het bedrijf of merk in de advertentie. | Advertentie starten, en sluiten | `a.media.ad.advertiser` |
| Campagne-id | De id van de advertentiecampagne | Advertentie starten, en sluiten | `a.media.ad.campaign` |

{style="table-layout:auto"}

Naast de bovenstaande afmetingen worden met Adobe automatisch de volgende indelingsafmetingen gemaakt. U moet classificatiegegevens uploaden om rapporten te bekijken die deze afmetingen gebruiken.

| Classificatienaam | Bovenliggende dimensie | Beschrijving |
| --- | --- | --- |
| Element-id | [ Inhoud ](sm-core.md) | De unieke id voor de inhoud van het media-element. Voorbeelden zijn de aflevering-id van de tv-serie, de id van het filmelement of de livegebeurtenis. Deze id&#39;s worden doorgaans afgeleid van metagegevensautoriteiten zoals EIDR, TMS/Gracenote, Rovi of van andere bedrijfseigen of interne systemen. |
| Inhoudsbeoordeling | [ Inhoud ](sm-core.md) | De classificatie zoals gedefinieerd door de ouderlijke richtlijnen van TV. |
| Eerste luchtdatum | [ Inhoud ](sm-core.md) | De datum waarop de inhoud voor het eerst op de televisie is uitgezonden. Aangezien deze classificatiedimensie een tekenreeks is, is elke datumnotatie toegestaan. Adobe raadt aan een consistente datumnotatie te gebruiken, zoals `YYYY-MM-DD` . |
| Eerste digitale datum | [ Inhoud ](sm-core.md) | De datum waarop de inhoud voor het eerst via een digitaal kanaal of platform is verzonden. Aangezien deze classificatiedimensie een tekenreeks is, is elke datumnotatie toegestaan. Adobe raadt aan een consistente datumnotatie te gebruiken, zoals `YYYY-MM-DD` . |
| Ad-lengte | Advertentie | De lengte van de video en, in seconden. |
| Advertentienaam | Advertentie | De vriendelijke naam van de advertentie. Het is het indelingsequivalent van &#39;Ad name (variable)&#39;. |
| Creative-id | Advertentie | De id van de advertentie. |
| Naam pod | Pod Advertentie | De vriendelijke naam van de advertentiepod. |
| Podpositie | Pod Advertentie | De verschuiving van het advertentieeinde binnen de inhoud, in seconden. |

{style="table-layout:auto"}
