---
title: Browser
description: De naam en versie van de gebruikte browser.
feature: Dimensions
exl-id: 2bdf2a5a-3482-43fa-b2e1-fbea892918fb
source-git-commit: 206df584deab5f6f9b8eeb09d9c8ad4983424eea
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 1%

---

# Browser

De &#39;[!UICONTROL Browser]&#39; [dimensie](overview.md) meldt de naam en versie van de browser die de hit verzendt. Deze dimensie is handig wanneer u de meest gebruikte browsers wilt meten die bezoekers gebruiken. Wanneer u nieuwe versies van uw site test, kunt u deze tests uitvoeren in de bovenste browsers in deze dimensie om de inspanningen voor kwaliteitscontrole te maximaliseren.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een raadplegingstabel intern aan Adobe. De opzoekwaarde is gebaseerd op de `User-Agent` HTTP-header in afbeeldingsaanvragen. Adobe partners met [DeviceAtlas](https://deviceatlas.com/) om raadplegingen tussen gebruikersagent en browser te handhaven.

* Voor de implementaties van AppMeasurementen, werkt deze dimensie uit de doos.
* Voor de implementaties van SDK van het Web, laat toe [!UICONTROL Device Lookup] wanneer [configureren van een gegevensstroom](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=nl-NL).

## Dimension-items

Dimension-items omvatten de gebruikte browsernamen en -versies. Verschillende versies van dezelfde browser zijn afzonderlijke dimensie-items.

Sommige dimensie-items bevatten `"(unknown version)"` in plaats van hun versienummer. Dit afmetingspunt verwijst naar een recente browser versie die de Adobe nog niet aan hun raadplegingslijsten heeft toegevoegd. Aangezien browsers vaak worden bijgewerkt, worden de `"(unknown version)"` voor een bepaalde browser algemeen en tijdelijk is. Adobe werkt opzoektabellen doorgaans bij tijdens maandelijkse onderhoudsreleases.