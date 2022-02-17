---
title: Taal
description: De voorkeurstaal in de browser.
feature: Dimensions
exl-id: 590406a4-d336-42c7-8048-e7cd8e611d43
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---

# Taal

De dimensie &#39;Taal&#39; toont de bovenste talen waarin bezoekers inhoud liever zien. Deze dimensie is waardevol wanneer u de meest frequente voorkeurstalen van bezoekers wilt begrijpen om hulp bij lokalisatiepogingen te bieden.

>[!NOTE]
>
>Met deze dimensie wordt de taal van uw site niet verzameld. Als u de taal van uw site in een dimensie wilt verzamelen, raadt Adobe u aan een aangepaste variabele te gebruiken, zoals een [eVar](evar.md).

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een raadplegingstabel intern aan Adobe. De opzoekwaarde is gebaseerd op de `Accept-Language` HTTP-header in afbeeldingsaanvragen. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak.

## Dimension-items

Dimension-items bevatten vriendelijke namen van de voorkeurstalen van bezoekers. Voorbeelden zijn `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"`, en `"Spanish (Spain)"`. Als een afbeeldingsaanvraag geen geldige taal bevat in de HTTP-header, is het dimensiepunt `"None"`.
