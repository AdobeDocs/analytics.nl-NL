---
title: Java ingeschakeld
description: Hiermee wordt bepaald of Java is ingeschakeld in de browser.
feature: Dimensions
exl-id: 2d4b4ea2-65ba-4d39-a040-f989b5eddc6e
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Java ingeschakeld

De functie Java ingeschakeld [dimensie](overview.md) Hiermee bepaalt u of Java is ingeschakeld voor de browser op dat moment. Het is handig als u op Java gebaseerde functionaliteit op uw site wilt introduceren en wilt weten hoeveel bezoekers Java al hebben ingeschakeld. Voor mensen die Java hebben uitgeschakeld, kunt u een alternatief of instructies opgeven voor het inschakelen van deze functie.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`v` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeasurement verzamelt deze gegevens door te bepalen of Java is ingeschakeld in de browser. Als u een bibliotheek met AppMeasurementen gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten het AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de opdracht `v` de parameter van het vraagkoord die &quot;Y&quot;of &quot;N&quot;bevat als u deze afmeting zou willen gebruiken.

## Dimension-items

Dimension-items zijn &quot;Ingeschakeld&quot;, &quot;Uitgeschakeld&quot; en &quot;Onbekend&quot;.

* **Ingeschakeld**: Java is ingeschakeld in de browser. De `v` queryreeks bevatte de waarde &quot;Y&quot;.
* **Uitgeschakeld**: Java is uitgeschakeld in de browser of ondersteunt Java anders niet. De `v` queryreeks bevatte de waarde &quot;N&quot;.
* **Onbekend**: AppMeasurement kan de Java-ondersteuning niet bepalen. De `v` queryreeks is niet aanwezig in de afbeeldingsaanvraag.
