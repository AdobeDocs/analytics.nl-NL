---
title: Browser
description: De naam en versie van de gebruikte browser.
translation-type: tm+mt
source-git-commit: 4a7b3a00bdbf557c219de530e3e692c2b2db4a84
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---


# Browser

De dimensie Browser rapporteert de naam en de versie van de browser die de hit verzendt. Deze dimensie is handig om te begrijpen welke browsers bezoekers het meest gebruiken. Wanneer u nieuwe versies van uw site test, kunt u deze tests uitvoeren in de bovenste browsers in deze dimensie om de inspanningen voor kwaliteitscontrole te maximaliseren.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een interne opzoektabel van Adobe. De opzoekwaarde is gebaseerd op de `User-Agent` HTTP-header in afbeeldingsaanvragen. Als u een AppMeturement-bibliotheek gebruikt (bijvoorbeeld via Adobe Experience Platform Launch), werkt deze dimensie buiten het vak.

## Dimensiewaarden

Tot de waarden voor dimensies behoren de gebruikte browsernamen en -versies. Verschillende versies van dezelfde browser zijn afzonderlijke waarden voor afmetingen.

Sommige dimensiewaarden bevatten `"(unknown version)"` in plaats van hun versienummer. Deze waarde verwijst naar een recente browserversie die Adobe niet aan hun raadplegingstabellen heeft toegevoegd. Aangezien browsers regelmatig bijwerken, is de `"(unknown version)"` versie voor een bepaalde browser gebruikelijk en tijdelijk. Adobe werkt opzoektabellen gewoonlijk bij tijdens maandelijkse onderhoudsreleases.
