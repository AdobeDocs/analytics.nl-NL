---
title: Uur van de dag
description: Het numerieke uur van de dag, ongeacht welke dag.
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Uur van de dag

De dimensie &#39;Uur van dag&#39; rapporteert het numerieke uur van een bepaalde dag als een dimensie-item. Bijvoorbeeld, als u een rapport hebt dat 1 Januari - 7 overspant, het eerste uur van elke daggroepen in het zelfde afmetingspunt. Dit rapport is waardevol als u een rapport wilt dat door relatieve tijd van dag wordt uitgesplitst, maar geen statische uren als afmetingspunten wilt. Het is vooral waardevol als afmeting in geplande rapporten, aangezien deze afmeting met de geselecteerde datumwaaier rolt.

Deze dimensie is gebaseerd op de tijdzone van de rapportreeks, en niet de lokale tijdzone van de bezoeker. Als uw rapportsuite bijvoorbeeld in Mountain-tijd is en een bezoeker in Californië uw site bezoekt om 10:00 uur Pacific-tijd, bezoeken de treffers onder het item `11:00 AM` Dimensie. Als u een afmeting wilt die de tijd van de lokale bezoeker registreert, adviseert Adobe het gebruiken van [getTimeParting](/help/implement/vars/plugins/gettimeparting.md) stop - binnen.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

Dimension-items zijn onder andere `12:00 AM` - `11:00 PM`, die het uur vertegenwoordigen van de dag waarop de treffer heeft plaatsgevonden (naar beneden afgerond). Als een hit bijvoorbeeld om 15.58 uur wordt gegenereerd, wordt deze gegroepeerd onder het dimensie-item van `3:00 PM`.

## zomertijd

De Tijd van de Besparing van het daglicht is een praktijk waarbij de klokken een uur vooruit in de lente worden geplaatst, en een uur in de herfst terugzetten. Als de tijdzone van een rapportreeks DST gebruikt, past Adobe gegevens dienovereenkomstig voor dat uur aan.

* **Wanneer zomertijd begint**: In maart, tonen de rapporten typisch een uurhiaat in gegevens waar de Tijd van de Besparing van het Daglicht begint. Het uur bestond niet, dus het maakt geen deel uit van gegevensverzameling. Let op: een kleine hoeveelheid gegevens kan dit uur nog wel bereiken. De servers van de gegevensinzameling van Adobe nemen verscheidene seconden (tot een minuut) om de aanpassingen van DST in overweging te nemen.
* **Wanneer zomertijd eindigt**: In november, tonen de rapporten typisch een dubbel-gestapeld uur waar de Tijd van de Besparing van het Daglicht beëindigt. Het uur gebeurde twee keer, dus beide uren worden samengevoegd in rapporten.
