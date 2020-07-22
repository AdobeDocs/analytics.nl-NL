---
title: Java ingeschakeld
description: Hiermee wordt bepaald of Java is ingeschakeld in de browser.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Java ingeschakeld

De dimensie &#39;Java ingeschakeld&#39; bepaalt of Java is ingeschakeld voor de browser op dat moment. Het is handig als u op Java gebaseerde functionaliteit op uw site wilt introduceren en wilt weten hoeveel bezoekers Java al hebben ingeschakeld. Voor mensen die Java hebben uitgeschakeld, kunt u een alternatief of instructies opgeven voor het inschakelen van deze functie.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van het [`v` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeasurement verzamelt deze gegevens door te detecteren of Java is ingeschakeld in de browser. Als u een bibliotheek AppMeasurement gebruikt (zoals door Adobe Experience Platform Launch), werkt deze afmeting uit de doos. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `v` vraagkoord omvat die &quot;Y&quot;of &quot;N&quot;bevat als u deze afmeting zou willen gebruiken.

## Dimensie-items

Dimensie-items zijn &quot;Ingeschakeld&quot;, &quot;Uitgeschakeld&quot; en &quot;Onbekend&quot;.

* **Ingeschakeld**: Java is ingeschakeld in de browser. De `v` queryreeks bevatte de waarde &quot;Y&quot;.
* **Uitgeschakeld**: Java is uitgeschakeld in de browser of ondersteunt Java anders niet. De `v` queryreeks bevatte de waarde &quot;N&quot;.
* **Onbekend**: AppMeasurement kon de steun van Java niet bepalen. De `v` queryreeks is niet aanwezig in de afbeeldingsaanvraag.
