---
description: Informatie over hoe Adobe toegang tot Gegevensbronnen verleent.
subtopic: Data sources
title: Hoe de Gegevensbronnen werken
topic-fix: Developer and implementation
feature: Data Sources
exl-id: 3d56ca3f-6c45-48d0-bbd2-53d6babfbb83
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---

# Hoe de Gegevensbronnen werken

Informatie over hoe Adobe toegang tot Gegevensbronnen verleent.

>[!NOTE]
>
>Na verzending via de gegevensbronnen zijn geïmporteerde gegevens niet meer te onderscheiden van gegevens die met andere methoden zijn verzameld (JavaScript-baken, ActionSource, API voor gegevensinvoeging, enz.). U kunt de gegevens niet verwijderen nadat u deze hebt geïmporteerd.

![](assets/data_sources_overview.png)

Er zijn twee methoden beschikbaar voor het verzenden van gegevens:

* [FTP](/help/import/c-data-sources/datasrc-how-data-sources-works.md#section_0E70022648F94061AF5B4AD6C7145243)
* [API](/help/import/c-data-sources/datasrc-how-data-sources-works.md#section_65DACC9CE00C437BBFDD02D19C25A4BD)

## FTP {#section_0E70022648F94061AF5B4AD6C7145243}

U kunt op FTP gebaseerde gegevensbronnen tot stand brengen en beheren door marketingrapporten, die de dossieroverdracht van FTP gebruiken om gegevensdossiers in Gegevensbronnen in te voeren. Nadat u een gegevensbron hebt gemaakt, biedt Adobe u een FTP-locatie die u kunt gebruiken om gegevensbronbestanden te uploaden. Zodra geupload, vinden de Gegevensbronnen automatisch plaats en verwerken hen. Na verwerking zijn de gegevens beschikbaar voor marketingrapporten.

## API {#section_65DACC9CE00C437BBFDD02D19C25A4BD}

Adobe biedt een API van Gegevensbronnen aan die u programmatically uw toepassingen in Gegevensbronnen laat verbinden. Dit elimineert de behoefte aan een intermediaire server van FTP, en brengt gegevens via HTTP, ZEEP, en REST over.

Zie [API-documentatie voor gegevensbronnen](https://github.com/AdobeDocs/analytics-1.4-apis/tree/master/docs/data-sources-api).
