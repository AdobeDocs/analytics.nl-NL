---
title: Dynamische zoekopdrachten
description: Leer hoe u dynamische zoekopdrachten kunt gebruiken en hoe u deze kunt inschakelen. Omvat dragers, mobiele attributen, en werkend systeemtypes.
exl-id: 644bf34b-312d-483a-a590-2dd8d6a773a5
feature: Data Feeds
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Dynamische zoekopdrachten

Met dynamische zoekopdrachten kunt u extra opzoekbestanden in uw gegevensfeed ontvangen die anders niet beschikbaar zijn. Met deze instelling kunnen de volgende opzoektabellen worden verzonden met elk gegevensbestand met gegevensinvoer:

* **Naam vervoerder**: Biedt extra context voor de `carrier` kolom. De bestandsnaam die is opgenomen is `carrier.tsv`.
* **Mobiele kenmerken**: Biedt extra context voor de `mobile_id` kolom, inclusief alle functies die voor elk mobiel apparaat worden bijgehouden. De bestandsnaam die is opgenomen is `mobile_attributes.tsv`.
* **Type besturingssysteem**: Biedt een alternatieve context voor de `os` kolom. Beide `operating_systems.tsv` en `operating_system_type.tsv` gebruiken `os` kolom als de sleutel, maar slechts `operating_system_type.tsv` is een dynamische zoekopdracht.

## Dynamische zoekopdrachten inschakelen

Als u de vermelde opzoekbestanden wilt ontvangen, moet u aan alle volgende voorwaarden voldoen:

* De sleutelkolom moet in de gegevensvoer worden omvat.
   * Voor `carrier.tsv`, moet u `carrier`.
   * Voor `mobile_attributes.tsv`, moet u `mobile_id`.
   * Voor `operating_system_type.tsv`, moet u `os`.
* De volgende kolommen moeten **uitgesloten**. Als om het even welk van deze kolommen in de gegevensvoer inbegrepen zijn, zijn de extra raadplegingslijsten niet inbegrepen.
   * `user_agent`
   * `ch_hdr`
   * `ch_js`

Als uw gegevensfeed voldoet aan de vereisten voor het opnemen en uitsluiten van kolommen, neemt u contact op met de klantenservice met de id van de gegevensfeed en vraagt u om dynamische zoekopdrachten mogelijk te maken.

## Verwijzing naar opzoekkoptekst

Kolomkoppen voor deze opgezochte bestanden veranderen niet in de loop der tijd, zodat de kopteksten niet in elk gegevensbestand van de gegevensinvoer worden opgenomen. Gebruik deze kolomkoppen als referentie of download hun respectievelijke `.tsv` bestand.

+++**Naam vervoerder**
Downloaden [carrier_headers.tsv](assets/carrier_headers.tsv) of verwijs naar de onderstaande koppen.

`carrier`
`Carrier Name`
+++

+++**Mobiele kenmerken**
Downloaden [mobile_attributes_headers.tsv](assets/mobile_attributes_headers.tsv) of verwijs naar de onderstaande koppen.

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

+++**Type besturingssysteem**
Downloaden [operating_system_type_headers.tsv](assets/operating_system_type_headers.tsv) of verwijs naar de onderstaande koppen.

`os`
`Operating System Type`
+++
