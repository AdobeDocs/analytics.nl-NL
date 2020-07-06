---
title: Taal
description: De voorkeurstaal in de browser.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# Taal

De dimensie &#39;Taal&#39; toont de bovenste talen waarin bezoekers inhoud liever zien. Deze dimensie is waardevol wanneer u de meest frequente voorkeurstalen van bezoekers wilt begrijpen om hulp bij lokalisatiepogingen te bieden.

>[!NOTE]
>
>Met deze dimensie wordt de taal van uw site niet verzameld. Als u de taal van uw site in een dimensie wilt verzamelen, raadt Adobe u aan een aangepaste variabele te gebruiken, zoals een [eVar](evar.md).

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een interne opzoektabel van Adobe. De opzoekwaarde is gebaseerd op de `Accept-Language` HTTP-header in afbeeldingsaanvragen. Als u een bibliotheek AppMeasurement gebruikt (zoals door Adobe Experience Platform Launch), werkt deze afmeting uit de doos.

## Dimensiewaarden

Dimensiewaarden bevatten vriendelijke namen van de voorkeurstalen van bezoekers. Voorbeelden zijn `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"`en `"Spanish (Spain)"`. Als een afbeeldingsaanvraag geen geldige taal in de HTTP-header bevat, is de waarde van de dimensie `"None"`.
