---
title: Metagegevens van videoservices streamen
description: Beschikbare afmetingen wanneer u [!UICONTROL Video Metadata] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: e476c19a-9542-4a6f-9b79-5f801e2a7bf8
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Metagegevens van videoservices streamen

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Video Metadata] voor een rapportreeks toelaat. Zie [ Streaming media diensten videometriek van metriek ](../metrics/sm-video-metadata.md) voor beschikbare metriek.*

Streaming media services en dimensies bieden aanvullende rapportagefunctionaliteit voor gegevensverzameling via bibliotheken voor het verzamelen van streaming mediaservices. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Analytics for Streaming Media Ad-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Video Metadata]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Dimension-naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Toevoegen | Het type geladen advertentie. | TBD | `a.media.adLoad` |
| Dagdeel | De tijd van de dag waarop de inhoud werd uitgezonden of afgespeeld. Elke tekenreekswaarde wordt ondersteund. | Media starten, Media sluiten | `a.media.dayPart` |
| Episode | Het afleveringsnummer. | Media starten, Media sluiten | `a.media.episode` |
| Type mediatarent | Het type diervoeder. | Media starten, Media sluiten | `a.media.feed` |
| Genre | Het type of de groep inhoud zoals gedefinieerd door de inhoudsproducent. Deze dimensie ondersteunt meerdere waarden, gescheiden door komma&#39;s. | Media starten, Media sluiten | `a.media.genre` |
| MVPD | De MVPD zoals opgegeven door Adobe-verificatie. | Media starten, Media sluiten | `a.media.pass.mvpd` |
| Netwerk | De netwerk- of kanaalnaam | Media starten, Media sluiten | `a.media.network` |
| Seizoen | Het seizoensnummer waartoe de show behoort. | Media starten, Media sluiten | `a.media.season` |
| Tonen | De naam van het programma of de serie. | Media starten, Media sluiten | `a.media.show` |
| Tekst tonen | Een geheel getal dat het type inhoud vertegenwoordigt.<br>`0`: Volledige episode <br>`1`: Voorproef of aanhangwagen <br>`2`: Clip <br>`3`: Andere | Media starten, Media sluiten | `a.media.type` |

{style="table-layout:auto"}
