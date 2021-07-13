---
description: Meer informatie over hoe gegevens voor Adobe Analytics worden verzameld.
subtopic: Get started
title: Over dataverzameling
uuid: 4dd9a23d-ad49-4841-8f4c-32c3993851f2
feature: Grondbeginselen van rapporten en analyses
role: User, Admin
exl-id: 34a7be55-519a-4e04-95a3-99b0f6e04b3e
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# Over dataverzameling

Meer informatie over hoe gegevens voor Adobe Analytics worden verzameld.

Elke Adobe-paginacontracten hebben een klein fragment van JavaScript-code die is geautoriseerd voor Adobe. Deze code wordt verschaft door uw accountmanager.

Op hoog niveau wordt het gegevensverzamelingsproces als volgt gestroomd:

![](assets/data_collection.png)

1. Een bezoeker bezoekt een webpagina die de code voor gegevensverzameling bevat.
1. Terwijl de pagina wordt geladen, verzendt de code van de gegevensverzameling een beeldverzoek (genoemd een Webbaken) naar de servers van de Adobe gegevensinzameling. De afbeeldingsaanvraag bevat de gegevens die u wilt verzamelen over de interactie van de bezoeker met uw website.
1. Adobe slaat de gegevens op in rapportsuites. U kunt zich aanmelden om toegang te krijgen tot de gegevens van de rapportsuite en rapporten genereren met betrekking tot bezoekersactiviteiten op uw website.

Gegevensverzameling gaat erg snel en heeft geen merkbare invloed op de laadtijden van de pagina. De verzamelde gegevens omvatten paginameningen die uit het klikken van browser **opnieuw laden** of **Terug** knopen voortvloeien. De JavaScript-code wordt ook uitgevoerd wanneer de pagina uit de cache wordt opgehaald.

Zie [Gegevensverzameling in Analytics.](/help/import/home.md)
