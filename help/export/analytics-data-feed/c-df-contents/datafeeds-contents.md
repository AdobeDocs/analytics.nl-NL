---
description: In deze sectie worden de bestanden beschreven die worden gevonden in een levering van de gegevensfeed.
keywords: Gegevensfeed;taak;inhoud;manifest;bestand;opzoeken;raakgegevens;inhoud van levering
subtopic: data feeds
title: Inhoud van gegevensfeed - overzicht
feature: Data Feeds
exl-id: 7456ed99-c2f3-4b19-a63e-6b4e457e7d55
source-git-commit: 6b8366b451be1612331f517ee80fd57744deafdc
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 0%

---

# Inhoud gegevensfeed - overzicht

In de volgende secties wordt beschreven hoe u toegang krijgt tot de bestanden in een gegevensdoorvoerlevering en hoe u deze kunt begrijpen.

## Toegang krijgen tot inhoud van gegevensfeed

De inhoud van een gegevensfeed openen:

1. Meld u aan bij de doelsite van de gegevensfeed.

   Dit is de doelsite die u instelt bij het maken van de gegevensinvoer, zoals een Amazon S3- of Google Cloud Platform bucket.

1. Download het gecomprimeerde gegevensbestand naar uw lokale computer.

1. Pak het gecomprimeerde bestand uit met een programma dat ondersteuning biedt `.tar.gz` bestandsextensies.

1. Open de `hit_data.tsv` in uw spreadsheet of databasetoepassing van keuze om onbewerkte gegevens voor die dag weer te geven. —>

## Manifest-bestand {#feed-manifest}

Het manifestbestand bevat de volgende gegevens over elk bestand dat deel uitmaakt van de geüploade gegevensset:

* Bestandsnaam
* Bestandsgrootte
* MD5-hash
* Aantal records in het bestand

Het manifestbestand heeft dezelfde indeling als een Java JAR-manifestbestand.

Het manifestbestand wordt altijd als een afzonderlijk bestand geleverd `.txt` , zodat het bestaan ervan erop wijst dat de volledige gegevensset voor die aanvraagperiode al is geleverd. Manifest-bestanden krijgen een naam op basis van het volgende:

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

Sommige feeds zijn geconfigureerd om een `.fin` bestand in plaats van een `.txt` manifest. De `.fin` geeft aan dat het uploaden is voltooid, maar dat de metagegevens in het uploaden een oudere indeling hebben.

## Bestanden opzoeken

Sommige gegevensinvoerkolommen voeren een getal uit dat overeenkomt met de werkelijke waarde. Opzoekbestanden worden gebruikt om een getal uit een kolom met gegevensinvoer af te stemmen op een werkelijke waarde. De waarde &quot;497&quot; in het dialoogvenster `browser` De kolom met de aanraakgegevens geeft aan dat de aanraakactie afkomstig is uit &quot;Microsoft Internet Explorer 8&quot; als u in `browser.tsv`.

Let erop dat de `column_headers.tsv` en `event_list.tsv` zijn specifiek voor de gegevensinvoer en rapportreeks. Andere bestanden, zoals `browser.tsv`, zijn generiek.

De opzoekbestanden worden samen geleverd in een gecomprimeerd ZIP-bestand met de volgende naam:

```text
[rsid]_[YYYY-mm-dd]-lookup_data.[compression_suffix]
```

* **`column_headers.tsv`**: Een enkele rij met de kolomkoppen voor `hit_data.tsv`.
* **`browser.tsv`**: Hiermee wordt de browser-id toegewezen (de `browser` voederkolom) aan de browser vriendschappelijke naam.
* **`browser_type.tsv`**: Hiermee wordt de browser-id toegewezen (de `browser` voederkolom) aan het browser type.
* **`color_depth.tsv`**: Hiermee wordt de kleurdiepte-id toegewezen (de `color` voederkolom) aan kleurdiepte.
* **`connection_type.tsv`**: Hiermee wordt de verbindingstype-id toegewezen (de `connection_type` voederkolom) aan het verbindingstype.
* **`country.tsv`**: Wijst de land-id toe (de `country` voederkolom) aan de naam van het land.
* **`javascript_version.tsv`**: Hiermee wordt de JavaScript-versie-id toegewezen (de `javascript` voederkolom) aan de versie JavaScript.
* **`languages.tsv`**: Wijst de taal-id (de `language` voederkolom) aan taal.
* **`operating_systems.tsv`**: Hiermee wordt de id van het besturingssysteem toegewezen (de `os` voederkolom) aan de naam van het werkende systeem.
* **`plugins.tsv`**: Wijst de insteekmodule-id&#39;s toe (de `plugin` voederkolom) aan elke respectieve plug-in naam.
* **`resolution.tsv`**: Wijst de resolutie-id (de `resolution` voederkolom) aan de monitorresolutie.
* **`referrer_type.tsv`**: Hiermee wordt de id van het verwijzingstype toegewezen (de `ref_type` voederkolom) aan het referentietype.
* **`search_engines.tsv`**: Wijst de zoekmachine-id (de `search_engine` voederkolom) aan de naam van het onderzoeksmotor.
* **`event.tsv`**: Hiermee wordt elke gebeurtenis-id toegewezen (de `event_list` voederkolom) aan zijn respectieve gebeurtenisnaam.

## Gegevensbestanden verbergen

De gegevens worden verstrekt in een `hit_data.tsv` bestand. De hoeveelheid gegevens in dit bestand wordt bepaald door de leveringsindeling (uur- of dagbestand en enkele of meerdere bestanden). Dit bestand bevat alleen raakgegevens. De kolomkoppen worden afzonderlijk bij de opzoekbestanden geleverd. Elke rij in dit bestand bevat één serveraanroep.

De dossiers die door Adobe worden geleverd variëren gebaseerd op het type van gegevensvoer dat u hebt gevormd. Alle bestanden worden gecodeerd met ISO-8859-1.

* `[rsid]` verwijst naar de rapportsuite-id waaruit de gegevensinvoer afkomstig is.
* `[index]` wordt alleen gebruikt in meerdere bestandsfeeds en verwijst naar de juiste volgorde van gepagineerde bestanden.
* `[YYYY-mm-dd]` verwijst naar de begindag waarop de gegevensinvoer wordt bedoeld.
* `[HHMMSS]` wordt alleen gebruikt in uurvoer en verwijst naar het beginuur waarvoor de gegevensinvoer bestemd is.
* `[compression_suffix]` verwijst naar het type compressie dat wordt gebruikt. Doorgaans worden gegevensfeeds gecomprimeerd tot `tar.gz` of `zip` bestanden.
* `[format_suffix]` verwijst naar het bestandstype. De bestandsindeling van de gegevensfeed is doorgaans `.tsv`.

### Dagelijks, één bestand

Nadat de gegevens voor een dag worden verzameld, ontvangt u één enkel gecomprimeerd gegevensdossier en een manifestdossier. Het gegevensbestand heeft de naam:

`[rsid]_[YYYY-mm-dd].[compression_suffix]`

Bij uitname bevat het gegevensbestand één bestand `hit_data.tsv` met alle gegevens voor die dag, evenals raadplegingsdossiers voor om het even welke vereiste kolommen.

### Dagelijks, meerdere bestanden

Nadat de gegevens voor een dag worden verzameld, ontvangt u één of meerdere samengeperste gegevensdossiers en een manifestdossier. Het gegevensbestand heeft de naam:

`[index]-[rsid]_[YYYY-mm-dd].[compression_suffix]`

Bij uitname bevat elk gegevensbestand één bestand `[index]-[rsid]_[YYYY-mm-dd].[format_suffix]` die ongeveer 2 GB van niet samengeperste gegevens, evenals raadplegingsdossiers voor om het even welke vereiste kolommen bevat.

### Uur, één bestand

Nadat de gegevens een uur lang zijn verzameld, ontvangt u één gecomprimeerd gegevensbestand en een manifestbestand. Het gegevensbestand heeft de naam:

`[rsid]_[YYYYmmdd]-[HHMMSS].[compression_suffix]`

Bij uitname bevat het gegevensbestand één bestand `hit_data.tsv` bestand met alle gegevens voor dat uur en opzoekbestanden voor vereiste kolommen.

### Uur, meerdere bestanden

Nadat de gegevens een uur lang zijn verzameld, ontvangt u een of meer gecomprimeerde gegevensbestanden en een manifestbestand. De gegevensbestanden krijgen de volgende naam:

`[index]-[rsid]_[YYYYmmdd]-[HHMMSS].[format_suffix].[compression_suffix]`

Bij uitname bevat elk gegevensbestand één bestand `[index]-[rsid]_[YYYYmmdd]-[HHMMSS].[format_suffix]` bestand dat ongeveer 2 GB niet-gecomprimeerde gegevens bevat, en opzoekbestanden voor vereiste kolommen.

## Gegevensbestandsgrootte

De grootte van het dossier van raakgegevens varieert zeer afhankelijk van het aantal variabelen actief gebruikt en de hoeveelheid verkeer die naar rapportreeks wordt verzonden. Een gegevensrij is echter gemiddeld ongeveer 500B (gecomprimeerd) of 2KB (niet-gecomprimeerd). Vermenigvuldigen dit met het aantal servervraag kan een ruwe schatting op verstrekken hoe groot een dossier van de gegevensvoer is. Wanneer uw organisaties gegevensdoorvoerbestanden ontvangen, kunt u een nauwkeuriger getal vinden door het aantal rijen te delen `hit_data.tsv` op basis van de totale bestandsgrootte.