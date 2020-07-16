---
description: Veelgestelde vragen over gegevensfeeds
keywords: Data Feed;job;pre column;post column;case sensitivity
title: Veelgestelde vragen over gegevensfeeds
translation-type: tm+mt
source-git-commit: 966d1e8d47df03f6e4cedfedd62c1d3bc56a3606
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# Veelgestelde vragen over gegevensfeeds

Veelgestelde vragen over gegevensfeeds.

## Wat is het verschil tussen kolommen met een `post_` prefix en kolommen zonder een `post_` prefix?

Kolommen zonder het `post_` voorvoegsel bevatten precies de gegevens die naar de gegevensverzameling zijn verzonden. Kolommen met een `post_` voorvoegsel bevatten de waarde na verwerking. Voorbeelden die een waarde kunnen wijzigen, zijn variabeleresistentie, verwerkingsregels, VISTA-regels, valutaconversie of andere serverlogica die Adobe toepast. Adobe raadt u aan de `post_` versie van een kolom waar mogelijk te gebruiken.

Als een kolom geen `post_` versie bevat (bijvoorbeeld `visit_num`), kan de kolom worden beschouwd als een postkolom.

## Hoe verwerken gegevensfeeds hoofdlettergevoeligheid?

In Adobe Analytics worden de meeste variabelen voor rapportagedoeleinden als hoofdlettergevoelig beschouwd. &#39;sneeuw&#39;, &#39;sneeuw&#39;, &#39;SNOW&#39; en &#39;sNow&#39; worden bijvoorbeeld allemaal beschouwd als dezelfde waarde. Hoofdlettergevoeligheid blijft behouden in gegevensfeeds.

Als u verschillende variaties ziet van dezelfde waarde tussen kolommen die niet na het plaatsen worden weergegeven (bijvoorbeeld &#39;sneeuw&#39; in de voorkolom en &#39;sneeuw&#39; in de postkolom), gebruikt uw implementatie zowel waarden in hoofdletters als in kleine letters op uw site. De gevalvariatie in de postkolom werd eerder overgegaan en in het virtuele koekje opgeslagen, of rond de zelfde tijd voor die rapportreeks verwerkt.

## Worden bots gefilterd door de regels van de Admin console bot inbegrepen in gegevensvoer?

Gegevensfeeds omvatten geen bommen die zijn gefilterd door de [regels](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/bot-removal/bot-removal.html)van de Admin-console.
