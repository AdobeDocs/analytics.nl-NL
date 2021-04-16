---
description: Veelgestelde vragen over gegevensfeeds
keywords: Gegevensfeed;taak;vóór kolom;na kolom;hoofdlettergevoeligheid
title: Veelgestelde vragen over gegevensfeeds
exl-id: 1bbf62d5-1c6e-4087-9ed9-8f760cad5420
translation-type: tm+mt
source-git-commit: c6d4095fdf86be52c7921aed84b9229ac3b27f82
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---

# Veelgestelde vragen over gegevensfeeds

Veelgestelde vragen over gegevensfeeds.

## Wat is het verschil tussen kolommen met een `post_` prefix en kolommen zonder een `post_` prefix?

Kolommen zonder het voorvoegsel `post_` bevatten gegevens precies zoals deze naar gegevensverzameling zijn verzonden. Kolommen met het voorvoegsel `post_` bevatten de waarde na verwerking. De voorbeelden die een waarde kunnen veranderen zijn veranderlijke persistentie, verwerkingsregels, de regels van VISTA, muntomzetting, of andere server-zijlogica Adobe van toepassing. Adobe raadt aan waar mogelijk de `post_`-versie van een kolom te gebruiken.

Als een kolom geen `post_` versie (bijvoorbeeld, `visit_num`) bevat, dan kan de kolom als een postkolom worden beschouwd.

## Hoe verwerken gegevensfeeds hoofdlettergevoeligheid?

In Adobe Analytics worden de meeste variabelen voor rapportagedoeleinden als niet-hoofdlettergevoelig beschouwd. &#39;sneeuw&#39;, &#39;sneeuw&#39;, &#39;SNOW&#39; en &#39;sNow&#39; worden bijvoorbeeld allemaal beschouwd als dezelfde waarde. Hoofdlettergevoeligheid blijft behouden in gegevensfeeds.

Als u verschillende variaties ziet van dezelfde waarde tussen kolommen die niet na het plaatsen worden weergegeven (bijvoorbeeld &#39;sneeuw&#39; in de voorkolom en &#39;sneeuw&#39; in de postkolom), gebruikt uw implementatie zowel waarden in hoofdletters als in kleine letters op uw site. De gevalvariatie in de postkolom werd eerder overgegaan en in het virtuele koekje opgeslagen, of rond de zelfde tijd voor die rapportreeks verwerkt.

## Worden bots gefilterd door de regels van de Admin console bot inbegrepen in gegevensvoer?

Gegevensfeeds omvatten geen bots die zijn gefilterd door [Regels voor Admin-console bot](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/bot-removal/bot-removal.html).

## Waarom zie ik veelvoudige `000` waarden in `event_list` of `post_event_list` de kolom van de gegevensvoer?

Sommige spreadsheeteditors, vooral Microsoft Excel, afronden automatisch zeer grote aantallen. De `event_list` kolom bevat vele komma-afgebakende aantallen, soms veroorzakend Excel om het als groot aantal te behandelen. De laatste cijfers worden afgerond op `000`.

Adobe raadt u aan `hit_data.tsv`-bestanden niet automatisch te openen in Microsoft Excel. Gebruik in plaats daarvan het dialoogvenster Gegevens importeren van Excel en zorg ervoor dat alle velden worden behandeld als tekst.

## Waarom kan ik &quot;Uurly&quot;-bestanden niet extraheren uit gegevens die ouder zijn dan zeven dagen?

Voor gegevens die ouder zijn dan 7 dagen, worden de &quot;Uur&quot;dossiers van een dag gecombineerd in één enkel &quot;Dagelijks&quot;dossier.

Voorbeeld: Op 9 maart 2021 wordt een nieuwe gegevensfeed gemaakt en de gegevens van 1 januari 2021 tot en met 9 maart worden als &quot;Uur&quot; geleverd. De &quot;Uurly&quot;-bestanden van vóór 2 maart 2021 worden echter gecombineerd tot één &quot;Dagelijks&quot;-bestand. U kunt alleen &#39;Uurly&#39;-bestanden extraheren uit gegevens die jonger zijn dan 7 dagen na de aanmaakdatum. In dit geval, van 2 maart tot en met 9 maart.
