---
title: Permanente ondersteuning voor cookies
description: Hiermee wordt bepaald of de bezoeker blijvende cookies kan ondersteunen.
feature: Dimensions
exl-id: ced69e41-d992-4c5a-8541-920aeb7186ae
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Permanente ondersteuning voor cookies

De &#39;Permanente ondersteuning voor cookies&#39; [dimensie](overview.md) toont of de hit een bezoeker-id heeft gebruikt die afkomstig is van een blijvende bron. De meest voorkomende permanente bron is een cookie, maar kan ook mobiele headers en andere bronnen gebruiken.

## Deze dimensie vullen met gegevens

Adobe bepaalt de waarde van deze afmetingsserver-kant die op de bron van het herkenningsteken van de slag wordt gebaseerd. Er is geen manier om deze rechtstreeks in te stellen. Het werkt uit de doos voor alle implementaties.

## Dimension-items

* **`Enabled`**: De bezoekersidentificatie van de hit is afkomstig van een bron die doorgaans aanhoudt. De meest voorkomende voorbeelden zijn `aid`, `fid`, of `mid` query-tekenreeksparameters, aangezien deze hun waarden afleiden van een cookie.
* **`Disabled`**: De bezoekersidentificatie van de hit is afkomstig van een bron die door de Adobe niet als blijvend wordt herkend, zoals een IP + user agent-tekenreeks. Dit dimensie-item bevat ook aangepaste id&#39;s voor bezoekers die de opdracht [`visitorID`](/help/implement/vars/config-vars/visitorid.md) variabele.

## Verschil tussen ondersteuning voor cookies en ondersteuning voor permanente cookies

* **Cookie-ondersteuning**: AppMeasurement probeert een algemeen cookie in te stellen. Het item Dimensie is gebaseerd op de vraag of het cookie correct is ingesteld.
* **Permanente ondersteuning voor cookies**: Het item van de dimensie is gebaseerd op het feit of de id van de treffer afkomstig is van een blijvende bron, zoals een cookie.
