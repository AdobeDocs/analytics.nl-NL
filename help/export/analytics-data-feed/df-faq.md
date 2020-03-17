---
description: Veelgestelde vragen over gegevensfeeds
keywords: Data Feed;job;pre column;post column;case sensitivity
title: Veelgestelde vragen over gegevensfeeds
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Veelgestelde vragen over gegevensfeeds

Veelgestelde vragen over gegevensfeeds.

## Wat is het verschil tussen kolommen met een `post_` prefix en kolommen zonder een `post_` prefix?

Kolommen zonder het `post_` voorvoegsel bevatten precies de gegevens die naar de gegevensverzameling zijn verzonden. Kolommen met een `post_` voorvoegsel bevatten de waarde na verwerking. Voorbeelden die een waarde kunnen wijzigen, zijn variabeleresistentie, verwerkingsregels, VISTA-regels, valutaconversie of andere serverlogica die Adobe toepast. Adobe raadt u aan de `post_` versie van een kolom waar mogelijk te gebruiken.

Als een kolom geen `post_` versie bevat (bijvoorbeeld `visit_num`), kan de kolom worden beschouwd als een postkolom.

## Hoe verwerken gegevensfeeds hoofdlettergevoeligheid?

In Adobe Analytics worden de meeste variabelen voor rapportagedoeleinden als hoofdlettergevoelig beschouwd. &#39;sneeuw&#39;, &#39;sneeuw&#39;, &#39;SNOW&#39; en &#39;sNow&#39; worden bijvoorbeeld allemaal beschouwd als dezelfde waarde. Hoofdlettergevoeligheid blijft behouden in gegevensfeeds.

Als u verschillende variaties ziet van dezelfde waarde tussen kolommen die niet na het plaatsen worden weergegeven (bijvoorbeeld &#39;sneeuw&#39; in de voorkolom en &#39;sneeuw&#39; in de postkolom), gebruikt uw implementatie zowel waarden in hoofdletters als in kleine letters op uw site. De gevalvariatie in de postkolom werd eerder overgegaan en in het virtuele koekje opgeslagen, of rond de zelfde tijd voor die rapportreeks verwerkt.