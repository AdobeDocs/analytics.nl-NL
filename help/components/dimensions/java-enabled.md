---
title: Java ingeschakeld
description: Hiermee wordt bepaald of Java is ingeschakeld in de browser.
translation-type: tm+mt
source-git-commit: 226c54b782651ea8c6f4b7bb8030a1513c440a1d
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Java ingeschakeld

De dimensie &#39;Java ingeschakeld&#39; bepaalt of Java is ingeschakeld voor de browser op dat moment. Het is handig als u op Java gebaseerde functionaliteit op uw site wilt introduceren en wilt weten hoeveel bezoekers Java al hebben ingeschakeld. Voor mensen die Java hebben uitgeschakeld, kunt u een alternatief of instructies opgeven voor het inschakelen van deze functie.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van het [`v` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeasurement verzamelt deze gegevens door te detecteren of Java is ingeschakeld in de browser. Als u een AppMeturement-bibliotheek gebruikt (bijvoorbeeld via Adobe Experience Platform Launch), werkt deze dimensie buiten het vak. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `v` vraagkoord omvat die &quot;Y&quot;of &quot;N&quot;bevat als u deze afmeting zou willen gebruiken.

## Dimensiewaarden

Dimensiewaarden zijn &quot;Enabled&quot;, &quot;Disabled&quot; en &quot;Unknown&quot;.

* **Ingeschakeld**: Java is ingeschakeld in de browser. De `v` queryreeks bevatte de waarde &quot;Y&quot;.
* **Uitgeschakeld**: Java is uitgeschakeld in de browser of ondersteunt Java anders niet. De `v` queryreeks bevatte de waarde &quot;N&quot;.
* **Onbekend**: AppMeasurement kon de steun van Java niet bepalen. De `v` queryreeks is niet aanwezig in de afbeeldingsaanvraag.
