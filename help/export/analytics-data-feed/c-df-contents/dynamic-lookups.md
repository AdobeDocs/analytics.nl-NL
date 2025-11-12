---
title: Dynamische zoekopdrachten
description: Leer hoe u dynamische zoekopdrachten kunt gebruiken en hoe u deze kunt inschakelen. Omvat dragers, mobiele attributen, en werkend systeemtypes.
exl-id: 12327239-06a2-4092-b27d-b94da39abf30
feature: Data Feeds
source-git-commit: 705a1716ed0205594fc6c75023c8805024ce7df7
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Dynamische zoekopdrachten

Met dynamische zoekopdrachten kunt u extra opzoekbestanden in uw gegevensfeed ontvangen die anders niet beschikbaar zijn. Met deze instelling kunnen de volgende opzoektabellen worden verzonden met elk gegevensbestand met gegevensinvoer:

* **naam van de Drager**: Verstrekt extra context voor de `carrier` kolom. De opgenomen bestandsnaam is `carrier.tsv` .
* **Mobiele attributen**: Verstrekt extra context voor de `mobile_id` kolom, met inbegrip van alle eigenschappen die voor elk mobiel apparaat worden gevolgd. De opgenomen bestandsnaam is `mobile_attributes.tsv` .
* **Werkend systeemtype**: Verstrekt een afwisselende context voor de `os` kolom. Zowel `operating_systems.tsv` als `operating_system_type.tsv` gebruiken de kolom `os` als de sleutel, maar alleen `operating_system_type.tsv` is een dynamische zoekopdracht.

## Dynamische zoekopdrachten inschakelen {#enable-dynamic-lookups}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_dynamic_lookups"
>title="Dynamische zoekopdrachten inschakelen"
>abstract="Selecteer deze optie als u extra opzoekbestanden in de gegevensfeed wilt ontvangen die anders niet beschikbaar zijn. Met deze instelling kunnen de volgende opzoektabellen worden verzonden met elk gegevensbestand met gegevensinvoer:<ul><li>Naam vervoerder</li><li>Mobiele kenmerken</li><li>Type besturingssysteem</li></ul>"

<!-- markdownlint-enable MD034 -->

Als u de vermelde opzoekbestanden wilt ontvangen, moet u aan alle volgende voorwaarden voldoen:

* De sleutelkolom moet in de gegevensvoer worden omvat.
   * Voor `carrier.tsv` moet u `carrier` opnemen.
   * Voor `mobile_attributes.tsv` moet u `mobile_id` opnemen.
   * Voor `operating_system_type.tsv` moet u `os` opnemen.
* De volgende kolommen moeten **worden uitgesloten**. Als een van deze kolommen is opgenomen in de gegevensfeed, wordt de `mobile_attributes.tsv` dynamische zoekopdracht niet opgenomen.
   * `user_agent`
   * `ch_hdr`
   * `ch_js`

Als uw gegevensfeed voldoet aan de vereisten voor het opnemen en uitsluiten van kolommen, neemt u contact op met de klantenservice met de id van de gegevensfeed en vraagt u om dynamische zoekopdrachten mogelijk te maken.

## Verwijzing naar opzoekkoptekst

Kolomkoppen voor deze opgezochte bestanden veranderen niet in de loop der tijd, zodat de kopteksten niet in elk gegevensbestand van de gegevensinvoer worden opgenomen. Gebruik deze kolomkoppen als referentie of download het respectievelijke `.tsv` -bestand.

+++**naam van de Drager**
Download [&#x200B; drager_headers.tsv &#x200B;](assets/carrier_headers.tsv) of verwijs de hieronder kopballen.

`carrier`
`Carrier Name`
+++

+++**Mobiele attributen**
Download [&#x200B; mobile_attributes_headers.tsv &#x200B;](assets/mobile_attributes_headers.tsv) of verwijs de hieronder kopballen.

`mobile_id`
`Manufacturer`
`Device`
`Device Type`
`Operating System`
`Diagonal Screen Size`
`Screen Height`
`Screen Width`
`Cookie Support`
`Color Depth`
`MP3 Audio Support`
`AAC Audio Support`
`AMR Audio Support`
`Midi Monophonic Audio Support`
`Midi Polyphonic Audio Support`
`QCELP Audio Support`
`GIF87 Image Support`
`GIF89a Image Support`
`PNG Image Support`
`JPG Image Support`
`3GPP Video Support`
`MPEG4 Video Support`
`3GPP2 Video Support`
`WMV Video Support`
`MPEG4 Part 2 Video Support`
`Stream MP4 AAC LC Video Support`
`Stream 3GP H264 Level 10b Video Support`
`Stream 3GP AAC LC Video Support`
`3GP AAC LC Video Support`
`Stream MP4 H264 Level 11 Video Support`
`Stream MP4 H264 Level 13 Video Support`
`Stream 3GP H264 Level 12 Video Support`
`Stream 3GP H264 Level 11 Video Support`
`Stream 3GP H264 Level 10 Video Support`
`Stream 3GP H264 Level 13 Video Support`
`3GP AMR NB Video Support`
`3GP AMR WB Video Support`
`MP4 H264 Level 11 Video Support`
`3GP H263 Video Support`
`MP4 H264 Level 13 Video Support`
`Stream 3GP H263 Video Support`
`Stream 3GP AMR WB Video Support`
`3GP H264 Level 10b Video Support`
`MP4 ACC LC Video Support`
`Stream 3GP AMR NB Video Support`
`3GP H264 Level 10 Video Support`
`3GP H264 Level 13 Video Support`
`3GP H264 Level 11 Video Support`
`3GP H264 Level 12 Video Support`
`Stream HTTP Live Streaming Video Support`
+++

+++**Werkend systeemtype**
Download [&#x200B; operating_system_type_headers.tsv &#x200B;](assets/operating_system_type_headers.tsv) of verwijs de hieronder kopballen.

`os`
`Operating System Type`
+++
