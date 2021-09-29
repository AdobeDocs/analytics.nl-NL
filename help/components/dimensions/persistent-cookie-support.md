---
title: Permanente ondersteuning voor cookies
description: Hiermee wordt bepaald of de bezoeker blijvende cookies kan ondersteunen.
exl-id: ced69e41-d992-4c5a-8541-920aeb7186ae
source-git-commit: 82d6137bc9229bbaa997c6856690bf76c20b755c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Permanente ondersteuning voor cookies

De dimensie &#39;Permanente ondersteuning voor cookies&#39; laat zien of de treffer een bezoeker-id heeft gebruikt die afkomstig is van een permanente bron. De meest voorkomende permanente bron is een cookie, maar kan ook mobiele headers en andere bronnen gebruiken.

## Deze dimensie vullen met gegevens

Adobe bepaalt de waarde van deze afmeting server-kant die op de bron van het herkenningsteken van de slag wordt gebaseerd. Er is geen manier om deze rechtstreeks in te stellen. Het werkt uit de doos voor alle implementaties.

## Dimension-items

* **`Enabled`**: De bezoekersidentificatie van de hit is afkomstig van een bron die doorgaans aanhoudt. De gemeenschappelijkste voorbeelden omvatten `aid`, `fid`, of `mid` parameters van het vraagkoord, aangezien zij hun waarden uit een koekje afleiden.
* **`Disabled`**: De bezoekersidentificatie van de hit kwam van een bron die Adobe niet als blijvend herkent, zoals IP + user agent string. Dit dimensiepunt omvat ook aangepaste bezoekers-id&#39;s die de variabele [`visitorID`](/help/implement/vars/config-vars/visitorid.md) gebruiken.

## Verschil tussen &#39;Cookie support&#39; en &#39;Permanente ondersteuning voor cookies&#39;

* **Ondersteuning** voor cookie: AppMeasurement probeert een generiek cookie in te stellen. Het item Dimensie is gebaseerd op de vraag of het cookie correct is ingesteld.
* **Ondersteuning voor** permanente cookies: Het item Dimensie is gebaseerd op het feit of de id van de hit afkomstig is van een permanente bron, zoals een cookie.
