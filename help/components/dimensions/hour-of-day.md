---
title: Uur van dag
description: Het numerieke uur van de dag, ongeacht welke dag.
feature: Dimensions
exl-id: b9361534-7e58-41ed-9a38-c02aeed7a2d8
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Uur van dag

Het &#39;daguur&#39; [dimensie](overview.md) meldt het numerieke uur van een bepaalde dag als een dimensie-item. Bijvoorbeeld, als u een rapport hebt dat 1 Januari - 7 overspant, het eerste uur van elke daggroepen in het zelfde afmetingspunt. Dit rapport is waardevol als u een rapport wilt dat door relatieve tijd van dag wordt uitgesplitst, maar geen statische uren als afmetingspunten wilt. Het is vooral waardevol als afmeting in geplande rapporten, aangezien deze afmeting met de geselecteerde datumwaaier rolt.

Deze dimensie is gebaseerd op de tijdzone van de rapportreeks, en niet de lokale tijdzone van de bezoeker. Als uw rapportenpakket zich bijvoorbeeld in Mountain Time bevindt en een bezoeker in Californië uw site om 10:00 uur Pacific-tijd bezoekt, worden de treffers onder de `11:00 AM` dimensie-item. Als u een afmeting wilt die de tijd van de lokale bezoeker registreert, adviseert de Adobe het gebruiken van [getTimeParting](/help/implement/vars/plugins/gettimeparting.md) insteekmodule.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

Tot Dimension-items behoren `12:00 AM` - `11:00 PM`, die het uur vertegenwoordigt van de dag waarop de treffer heeft plaatsgevonden (naar beneden afgerond). Als een hit bijvoorbeeld om 15:58 uur wordt gegenereerd, wordt deze gegroepeerd onder het item Dimensie van `3:00 PM`.

## zomertijd

De Tijd van de Besparing van het daglicht is een praktijk waarbij de klokken een uur vooruit in de lente worden geplaatst, en een uur in de herfst terugzetten. Als de tijdzone van een rapportreeks DST gebruikt, past de Adobe gegevens dienovereenkomstig voor dat uur aan.

* **Wanneer zomertijd begint**: In maart, tonen de rapporten typisch een uurhiaat in gegevens waar de Tijd van de Besparing van het Daglicht begint. Het uur bestond niet, dus het maakt geen deel uit van gegevensverzameling. Let op: een kleine hoeveelheid gegevens kan dit uur nog wel bereiken. De servers van de gegevensinzameling van de Adobe nemen verscheidene seconden (tot een minuut) om de aanpassingen van DST in aanmerking te nemen.
* **Wanneer de zomertijd eindigt**: In november, tonen de rapporten typisch een dubbel-gestapeld uur waar de Tijd van de Besparing van het Daglicht beëindigt. Het uur gebeurde twee keer, dus beide uren worden samengevoegd in rapporten.
