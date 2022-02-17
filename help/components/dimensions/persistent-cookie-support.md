---
title: Permanente ondersteuning voor cookies
description: Hiermee wordt bepaald of de bezoeker blijvende cookies kan ondersteunen.
feature: Dimensions
exl-id: ced69e41-d992-4c5a-8541-920aeb7186ae
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Permanente ondersteuning voor cookies

De dimensie &#39;Permanente ondersteuning voor cookies&#39; laat zien of de treffer een bezoeker-id heeft gebruikt die afkomstig is van een permanente bron. De meest voorkomende permanente bron is een cookie, maar kan ook mobiele headers en andere bronnen gebruiken.

## Deze dimensie vullen met gegevens

Adobe bepaalt de waarde van deze afmeting server-kant die op de bron van het herkenningsteken van de slag wordt gebaseerd. Er is geen manier om deze rechtstreeks in te stellen. Het werkt uit de doos voor alle implementaties.

## Dimension-items

* **`Enabled`**: De bezoekersidentificatie van de hit is afkomstig van een bron die doorgaans aanhoudt. De meest voorkomende voorbeelden zijn `aid`, `fid`, of `mid` query-tekenreeksparameters, aangezien deze hun waarden afleiden van een cookie.
* **`Disabled`**: De bezoekersidentificatie van de hit kwam van een bron die Adobe niet als blijvend herkent, zoals IP + user agent string. Dit dimensie-item bevat ook aangepaste id&#39;s voor bezoekers die de opdracht [`visitorID`](/help/implement/vars/config-vars/visitorid.md) variabele.

## Verschil tussen &#39;Cookie support&#39; en &#39;Permanente ondersteuning voor cookies&#39;

* **Cookie-ondersteuning**: AppMeasurement probeert een generiek cookie in te stellen. Het item Dimensie is gebaseerd op de vraag of het cookie correct is ingesteld.
* **Permanente ondersteuning voor cookies**: Het item Dimensie is gebaseerd op het feit of de id van de hit afkomstig is van een permanente bron, zoals een cookie.
