---
title: Uur
description: Het uur waarop metrisch voorkwam.
feature: Dimensions
exl-id: 323c46dd-87d0-487a-b954-e5ccbc1b919d
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---

# Uur

De &#39;Uur&#39; [dimensie](overview.md) meldt het uur dat een bepaalde metrische waarde voorkwam (naar beneden afgerond). Het eerste afmetingspunt is het eerste uur in de datumwaaier, en het laatste afmetingspunt is het laatste uur in de datumwaaier. Deze dimensie is waardevol voor trended rapporten, aangezien het u toestaat om metriek in tijd te zien.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

De punten van het Dimension omvatten een bepaald uur binnen de de datumwaaier van een rapport naast zijn datum. Het is opgemaakt als `HH:HH YYYY-MM-DD`.

## zomertijd

De Tijd van de Besparing van het daglicht is een praktijk waarbij de klokken een uur vooruit in de lente worden geplaatst, en een uur in de herfst terugzetten. Als de tijdzone van een rapportreeks DST gebruikt, past de Adobe gegevens dienovereenkomstig voor dat uur aan.

* **Wanneer zomertijd begint**: In maart, tonen de rapporten typisch een uurhiaat in gegevens waar de Tijd van de Besparing van het Daglicht begint. Het uur bestond niet, dus het maakt geen deel uit van gegevensverzameling. Let op: een kleine hoeveelheid gegevens kan dit uur nog wel bereiken. De servers van de gegevensinzameling van de Adobe nemen verscheidene seconden (tot een minuut) om de aanpassingen van DST in aanmerking te nemen.
* **Wanneer de zomertijd eindigt**: In november, tonen de rapporten typisch een dubbel-gestapeld uur waar de Tijd van de Besparing van het Daglicht beëindigt. Het uur gebeurde twee keer, dus beide uren worden samengevoegd in rapporten.
