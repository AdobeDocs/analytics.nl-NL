---
description: Informatie over hoe Adobe toegang biedt tot gegevensbronnen.
subtopic: Data sources
title: Hoe de Gegevensbronnen werken
topic: Developer and implementation
uuid: ee9e6e74-9b00-4733-9a4b-d9f2b954cc7c
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Hoe de Gegevensbronnen werken

Informatie over hoe Adobe toegang biedt tot gegevensbronnen.

>[!NOTE] Na verzending via de gegevensbronnen zijn geïmporteerde gegevens niet meer te onderscheiden van gegevens die met andere methoden zijn verzameld (JavaScript-baken, ActionSource, API voor gegevensinvoeging, enz.). U kunt de gegevens niet verwijderen nadat u deze hebt geïmporteerd.

![](assets/data_sources_overview.png)

Er zijn twee methoden beschikbaar voor het verzenden van gegevens:

* [FTP](/help/import/c-data-sources/datasrc-how-data-sources-works.md#section_0E70022648F94061AF5B4AD6C7145243)
* [API](/help/import/c-data-sources/datasrc-how-data-sources-works.md#section_65DACC9CE00C437BBFDD02D19C25A4BD)

## FTP {#section_0E70022648F94061AF5B4AD6C7145243}

U kunt op FTP gebaseerde gegevensbronnen tot stand brengen en beheren door marketingrapporten, die de dossieroverdracht van FTP gebruiken om gegevensdossiers in Gegevensbronnen in te voeren. Nadat u een gegevensbron hebt gemaakt, biedt Adobe u een FTP-locatie waarmee u gegevensbronbestanden kunt uploaden. Zodra geupload, vinden de Gegevensbronnen automatisch plaats en verwerken hen. Na verwerking zijn de gegevens beschikbaar voor marketingrapporten.

## API {#section_65DACC9CE00C437BBFDD02D19C25A4BD}

Adobe biedt een API voor gegevensbronnen waarmee u uw toepassingen programmatisch kunt koppelen aan gegevensbronnen. Dit elimineert de behoefte aan een intermediaire server van FTP, en brengt gegevens via HTTP, ZEEP, en REST over.

Zie [Gegevensbronnen API Documentatie](https://github.com/AdobeDocs/analytics-1.4-apis/tree/master/docs/data-sources-api).
