---
title: Browser
description: De naam en versie van de gebruikte browser.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Browser

De dimensie Browser rapporteert de naam en de versie van de browser die de hit verzendt. Deze dimensie is handig om te begrijpen welke browsers bezoekers het meest gebruiken. Wanneer u nieuwe versies van uw site test, kunt u deze tests uitvoeren in de bovenste browsers in deze dimensie om de inspanningen voor kwaliteitscontrole te maximaliseren.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een interne opzoektabel van Adobe. De opzoekwaarde is gebaseerd op de `User-Agent` HTTP-header in afbeeldingsaanvragen. Als u een bibliotheek AppMeasurement gebruikt (zoals door Adobe Experience Platform Launch), werkt deze afmeting uit de doos.

## Dimensie-items

Dimensie-items omvatten de gebruikte browsernamen en -versies. Verschillende versies van dezelfde browser zijn afzonderlijke dimensie-items.

Sommige dimensie-items bevatten `"(unknown version)"` in plaats van hun versienummer. Dit dimensie-item verwijst naar een recente browserversie die Adobe niet heeft toegevoegd aan hun opzoektabellen. Aangezien browsers regelmatig bijwerken, is de `"(unknown version)"` versie voor een bepaalde browser gebruikelijk en tijdelijk. Adobe werkt opzoektabellen gewoonlijk bij tijdens maandelijkse onderhoudsreleases.
