---
title: Streaming mediaservices en dimensies
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Ads] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: 3f17bacc-8c36-499a-a863-9298e2d54370
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Streaming mediaservices en dimensies

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Ads] voor een rapportreeks toelaat. Zie [&#x200B; Streaming Media en metriek &#x200B;](../metrics/sm-ads.md) voor beschikbare metriek.*

Streaming-mediaservices en -dimensies bieden extra rapportagefunctionaliteit voor gegevensverzameling via Streaming-mediaservices-bibliotheken. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Analytics for Streaming Media Ad-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Ads]** onder [&#x200B; Media die &#x200B;](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Dimension-naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
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

Naast de bovenstaande afmetingen maakt Adobe automatisch de volgende classificatieafmetingen. U moet classificatiegegevens uploaden om rapporten te bekijken die deze afmetingen gebruiken.

| Classificatienaam | Bovenliggende dimensie | Beschrijving |
| --- | --- | --- |
| Element-id | [&#x200B; Inhoud &#x200B;](sm-core.md) | De unieke id voor de inhoud van het media-element. Voorbeelden zijn de aflevering-id van de tv-serie, de id van het filmelement of de livegebeurtenis. Deze id&#39;s worden doorgaans afgeleid van metagegevensautoriteiten zoals EIDR, TMS/Gracenote, Rovi of van andere bedrijfseigen of interne systemen. |
| Inhoudsbeoordeling | [&#x200B; Inhoud &#x200B;](sm-core.md) | De classificatie zoals gedefinieerd door de ouderlijke richtlijnen van TV. |
| Eerste luchtdatum | [&#x200B; Inhoud &#x200B;](sm-core.md) | De datum waarop de inhoud voor het eerst op de televisie is uitgezonden. Aangezien deze classificatiedimensie een tekenreeks is, is elke datumnotatie toegestaan. Adobe raadt u aan een consistente datumnotatie te gebruiken, zoals `YYYY-MM-DD` . |
| Eerste digitale datum | [&#x200B; Inhoud &#x200B;](sm-core.md) | De datum waarop de inhoud voor het eerst via een digitaal kanaal of platform is verzonden. Aangezien deze classificatiedimensie een tekenreeks is, is elke datumnotatie toegestaan. Adobe raadt u aan een consistente datumnotatie te gebruiken, zoals `YYYY-MM-DD` . |
| Ad-lengte | Advertentie | De lengte van de video en, in seconden. |
| Advertentienaam | Advertentie | De vriendelijke naam van de advertentie. Het is het indelingsequivalent van &#39;Ad name (variable)&#39;. |
| Creative-id | Advertentie | De id van de advertentie. |
| Naam pod | Pod Advertentie | De vriendelijke naam van de advertentiepod. |
| Podpositie | Pod Advertentie | De verschuiving van het advertentieeinde binnen de inhoud, in seconden. |

{style="table-layout:auto"}
