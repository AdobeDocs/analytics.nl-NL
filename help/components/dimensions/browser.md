---
title: Browser
description: De naam en versie van de gebruikte browser.
feature: Dimensions
exl-id: 2bdf2a5a-3482-43fa-b2e1-fbea892918fb
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# Browser

De dimensie Browser rapporteert de naam en de versie van de browser die de hit verzendt. Deze dimensie is handig om te begrijpen welke browsers bezoekers het meest gebruiken. Wanneer u nieuwe versies van uw site test, kunt u deze tests uitvoeren in de bovenste browsers in deze dimensie om de inspanningen voor kwaliteitscontrole te maximaliseren.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een raadplegingstabel intern aan Adobe. De opzoekwaarde is gebaseerd op de `User-Agent` HTTP-header in afbeeldingsaanvragen. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak.

## Dimension-items

Dimension-items omvatten de gebruikte browsernamen en -versies. Verschillende versies van dezelfde browser zijn afzonderlijke dimensie-items.

Sommige dimensie-items bevatten `"(unknown version)"` in plaats van hun versienummer. Dit afmetingspunt verwijst naar een recente browser versie die Adobe niet aan hun raadplegingslijsten heeft toegevoegd. Aangezien browsers vaak worden bijgewerkt, worden de `"(unknown version)"` voor een bepaalde browser algemeen en tijdelijk is. Adobe werkt opzoektabellen doorgaans bij tijdens maandelijkse onderhoudsreleases.
