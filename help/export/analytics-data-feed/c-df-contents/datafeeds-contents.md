---
description: In deze sectie worden de bestanden beschreven die in een levering van de gegevensfeed zijn gevonden.
keywords: Gegevensfeed;taak;inhoud;manifest;bestand;opzoeken;raakgegevens;inhoud van levering
subtopic: data feeds
title: Inhoud van gegevensfeed - overzicht
feature: Grondbeginselen van rapporten en analyses
uuid: 82a86314-4841-4133-a0dc-4e7c6cd14fc1
exl-id: 7456ed99-c2f3-4b19-a63e-6b4e457e7d55
translation-type: tm+mt
source-git-commit: 05c85e0eee25a04be154d8bcae9b133791667d75
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Inhoud van gegevensfeed - overzicht

In deze sectie worden de bestanden beschreven die in een levering van de gegevensfeed zijn gevonden.

## Manifest-bestand

Het manifestbestand bevat de volgende gegevens over elk bestand dat deel uitmaakt van de geüploade gegevensset:

* Bestandsnaam
* Bestandsgrootte
* MD5-hash
* Aantal records in het bestand

Het manifestbestand heeft dezelfde indeling als een Java JAR-manifestbestand.

Het manifestdossier wordt altijd geleverd als afzonderlijk `.txt` dossier, zodat zijn bestaan erop wijst dat de volledige gegevensreeks voor die verzoekperiode reeds is geleverd. Manifest-bestanden krijgen een naam op basis van het volgende:

```text
[rsid]_[YYYY-mm-dd].txt
```

Een typisch manifestdossier bevat gegevens gelijkend op het volgende:

```text
Datafeed-Manifest-Version: 1.0
 Lookup-Files: 1
 Data-Files: 1
 Total-Records: 611

 Lookup-File: rsid_date-lookup_data.tar.gz
 MD5-Digest: af6de42d8b945d4ec1cf28360085308
 File-Size: 63750

 Data-File: 01-rsid_date.tsv.gz
 MD5-Digest: 9c70bf783cb3d0095a4836904b72c991
 File-Size: 122534
 Record-Count: 611
```

Elk manifestbestand bevat een koptekst die het totale aantal opzoekbestanden, gegevensbestanden en het totale aantal records in alle gegevensbestanden aangeeft. Deze koptekst wordt gevolgd door meerdere secties met informatie voor elk bestand dat is opgenomen in de gegevensdoorvoerlevering.

Sommige feeds zijn geconfigureerd om een `.fin`-bestand in plaats van een `.txt`-manifest te ontvangen. De `.fin` geeft aan dat het uploaden is voltooid, maar bevat geen metagegevens over het uploaden.

## Bestanden opzoeken

Sommige gegevensinvoerkolommen voeren een getal uit dat overeenkomt met de werkelijke waarde. Opzoekbestanden worden gebruikt om een getal uit een kolom met gegevensinvoer af te stemmen op een werkelijke waarde. De waarde &quot;497&quot; in de kolom `browser` hit data geeft bijvoorbeeld aan dat de hit afkomstig is van &quot;Microsoft Internet Explorer 8&quot; als u in `browser.tsv` kijkt.

De `column_headers.tsv` en `event_list.tsv` zijn specifiek voor de gegevensinvoer en rapportsuite. Andere bestanden, zoals `browser.tsv`, zijn generiek.

De opzoekbestanden worden samen geleverd in een gecomprimeerd ZIP-bestand met de volgende naam:

```text
[rsid]_[YYYY-mm-dd]-lookup_data.[compression_suffix]
```

* [!DNL column_headers.tsv] (aangepast voor deze gegevensinvoer)
* [!DNL browser.tsv]
* [!DNL browser_type.tsv]
* [!DNL color_depth.tsv]
* [!DNL connection_type.tsv]
* [!DNL country.tsv]
* [!DNL javascript_version.tsv]
* [!DNL languages.tsv]
* [!DNL operating_systems.tsv]
* [!DNL plugins.tsv]
* [!DNL resolution.tsv]
* [!DNL referrer_type.tsv]
* [!DNL search_engines.tsv]
* [!DNL event_lookup.tsv] (aangepast voor deze gegevensinvoer)

## Gegevensbestanden verbergen

De gegevens van de aanraking worden verstrekt in een [!DNL hit_data.tsv] dossier. De hoeveelheid gegevens in dit bestand wordt bepaald door de leveringsindeling (uur- of dagbestand en enkele of meerdere bestanden). Dit bestand bevat alleen raakgegevens. De kolomkoppen worden afzonderlijk bij de opzoekbestanden geleverd. Elke rij in dit bestand bevat één serveraanroep.

De dossiers die door Adobe worden geleverd variëren gebaseerd op het type van gegevensvoer dat u hebt gevormd. Alle bestanden worden gecodeerd met ISO-8859-1.

* `[rsid]` verwijst naar de rapportsuite-id waaruit de gegevensinvoer afkomstig is.
* `[index]` wordt alleen gebruikt in meerdere bestandsfeeds en verwijst naar de juiste volgorde van gepagineerde bestanden.
* `[YYYY-mm-dd]` verwijst naar de begindag waarop de gegevensinvoer wordt bedoeld.
* `[HHMMSS]` wordt alleen gebruikt in uurvoer en verwijst naar het beginuur waarvoor de gegevensinvoer bestemd is.
* `[compression_suffix]` verwijst naar het type compressie dat wordt gebruikt. Doorgaans worden gegevensfeeds gecomprimeerd in `tar.gz`- of `zip`-bestanden.

### Dagelijks, één bestand

Nadat de gegevens voor een dag worden verzameld, ontvangt u één enkel gecomprimeerd gegevensdossier en een manifestdossier. Het gegevensbestand heeft de naam:

`[rsid]_[YYYY-mm-dd].[compression_suffix]`

Wanneer geëxtraheerd, bevat het gegevensbestand één `hit_data.tsv` dossier met alle gegevens voor die dag, evenals raadplegingsdossiers voor om het even welke vereiste kolommen.

### Dagelijks, meerdere bestanden

Nadat de gegevens voor een dag worden verzameld, ontvangt u één of meerdere samengeperste gegevensdossiers en een manifestdossier. Het gegevensbestand heeft de naam:

`[index]-[rsid]_[YYYY-mm-dd].[compression_suffix]`

Wanneer geëxtraheerd, bevat elk gegevensbestand één `hit_data.tsv` die ongeveer 2 GB van ongecomprimeerde gegevens, evenals raadplegingsdossiers voor om het even welke vereiste kolommen bevat.

### Uur, één bestand

Nadat de gegevens een uur lang zijn verzameld, ontvangt u één gecomprimeerd gegevensbestand en een manifestbestand. Het gegevensbestand heeft de naam:

`[rsid]_[YYYYmmdd]-[HHMMSS].[compression_suffix]`

Wanneer geëxtraheerd, bevat het gegevensbestand één `hit_data.tsv` dossier met alle gegevens voor dat uur, evenals raadplegingsdossiers voor om het even welke vereiste kolommen.

### Uur, meerdere bestanden

Nadat de gegevens een uur lang zijn verzameld, ontvangt u een of meer gecomprimeerde gegevensbestanden en een manifestbestand. Het gegevensbestand heeft de naam:

`[index]-[rsid]_[YYYYmmdd]-[HHMMSS].[compression_suffix]`

Wanneer geëxtraheerd, bevat elk gegevensbestand één `hit_data.tsv` die ongeveer 2 GB van ongecomprimeerde gegevens, evenals raadplegingsdossiers voor om het even welke vereiste kolommen bevat.

## Gegevensbestandsgrootte

De grootte van het dossier van raakgegevens varieert zeer afhankelijk van het aantal variabelen actief gebruikt en de hoeveelheid verkeer die naar rapportreeks wordt verzonden. Een gegevensrij is echter gemiddeld ongeveer 500B (gecomprimeerd) of 2KB (niet-gecomprimeerd). Vermenigvuldigen dit met het aantal servervraag kan een ruwe schatting op verstrekken hoe groot een dossier van de gegevensvoer is. Wanneer uw organisaties gegevensdoorvoerbestanden ontvangen, kunt u een nauwkeuriger getal vinden door het aantal rijen in `hit_data.tsv` te delen door de totale bestandsgrootte.
