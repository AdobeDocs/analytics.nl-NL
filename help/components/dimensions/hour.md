---
title: Uur
description: Het uur waarop metrisch voorkwam.
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---


# Uur

De dimensie &#39;Uur&#39; rapporteert het uur dat een bepaalde metrische waarde optrad (naar beneden afgerond). Het eerste afmetingspunt is het eerste uur in de datumwaaier, en het laatste afmetingspunt is het laatste uur in de datumwaaier. Deze dimensie is waardevol voor trended rapporten, aangezien het u toestaat om metriek in tijd te zien.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

De punten van Dimension omvatten een bepaald uur binnen de de datumwaaier van een rapport naast zijn datum. Het is opgemaakt als `HH:HH YYYY-MM-DD`.

## zomertijd

De Tijd van de Besparing van het daglicht is een praktijk waarbij de klokken een uur vooruit in de lente worden geplaatst, en een uur in de herfst terugzetten. Als de tijdzone van een rapportreeks DST gebruikt, past Adobe gegevens dienovereenkomstig voor dat uur aan.

* **Wanneer zomertijd begint**: In maart, tonen de rapporten typisch een uurhiaat in gegevens waar de Tijd van de Besparing van het Daglicht begint. Het uur bestond niet, dus het maakt geen deel uit van gegevensverzameling. Let op: een kleine hoeveelheid gegevens kan dit uur nog wel bereiken. De servers van de gegevensinzameling van Adobe nemen verscheidene seconden (tot een minuut) om de aanpassingen van DST in overweging te nemen.
* **Wanneer zomertijd eindigt**: In november, tonen de rapporten typisch een dubbel-gestapeld uur waar de Tijd van de Besparing van het Daglicht beëindigt. Het uur gebeurde twee keer, dus beide uren worden samengevoegd in rapporten.
