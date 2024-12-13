---
title: Metagegevensafmetingen voor streaming media
description: Beschikbare afmetingen wanneer u [!UICONTROL Video Metadata] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: e476c19a-9542-4a6f-9b79-5f801e2a7bf8
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# Metagegevensafmetingen voor streaming media

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Video Metadata] voor een rapportreeks toelaat. Zie [ Streaming de metriek van videometrische gegevens van Media ](../metrics/sm-video-metadata.md) voor beschikbare metriek.*

Streaming media en dimensies bieden extra rapportagefunctionaliteit voor gegevensverzameling via bibliotheken voor het streamen van media. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Streaming Media Collection]** vereist. Neem contact op met het accountteam van de Adobe voor meer informatie.

Wanneer u **[!UICONTROL Video Metadata]** onder [ Media die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Naam Dimension | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Toevoegen | Het type geladen advertentie. | TBD | `a.media.adLoad` |
| Dagdeel | De tijd van de dag waarop de inhoud werd uitgezonden of afgespeeld. Elke tekenreekswaarde wordt ondersteund. | Media starten, Media sluiten | `a.media.dayPart` |
| Episode | Het afleveringsnummer. | Media starten, Media sluiten | `a.media.episode` |
| Type mediatarent | Het type diervoeder. | Media starten, Media sluiten | `a.media.feed` |
| Genre | Het type of de groep inhoud zoals gedefinieerd door de inhoudsproducent. Deze dimensie ondersteunt meerdere waarden, gescheiden door komma&#39;s. | Media starten, Media sluiten | `a.media.genre` |
| MVPD | De MVPD zoals opgegeven door verificatie van de Adobe. | Media starten, Media sluiten | `a.media.pass.mvpd` |
| Netwerk | De netwerk- of kanaalnaam | Media starten, Media sluiten | `a.media.network` |
| Seizoen | Het seizoensnummer waartoe de show behoort. | Media starten, Media sluiten | `a.media.season` |
| Tonen | De naam van het programma of de serie. | Media starten, Media sluiten | `a.media.show` |
| Tekst tonen | Een geheel getal dat het type inhoud vertegenwoordigt.<br>`0`: Volledige episode <br>`1`: Voorproef of aanhangwagen <br>`2`: Clip <br>`3`: Andere | Media starten, Media sluiten | `a.media.type` |

{style="table-layout:auto"}
