---
title: Uur van de dag
description: Het numerieke uur van de dag, ongeacht welke dag.
translation-type: tm+mt
source-git-commit: 226c54b782651ea8c6f4b7bb8030a1513c440a1d
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Uur van de dag

De dimensie &#39;Uur van dag&#39; rapporteert het numerieke uur van een bepaalde dag als een dimensie-waarde. Bijvoorbeeld, als u een rapport hebt dat 1 Januari - 7 overspant, het eerste uur van elke daggroepen in de zelfde afmetingswaarde. Dit rapport is waardevol als u een rapport wilt dat door relatieve tijd van dag wordt uitgesplitst, maar geen statische uren als afmetingswaarden wilt. Het is vooral waardevol als afmeting in geplande rapporten, aangezien deze afmeting met de geselecteerde datumwaaier rolt.

Deze dimensie is gebaseerd op de tijdzone van de rapportreeks, en niet de lokale tijdzone van de bezoeker. Als uw rapportsuite bijvoorbeeld in Mountain-tijd is en een bezoeker in Californië uw site bezoekt om 10:00 uur Pacific-tijd, bezoeken de treffers onder de waarde `11:00 AM` Dimensie. Als u een afmeting wilt die de tijd van de lokale bezoeker registreert, adviseert Adobe gebruikend het [getTimeParting](/help/implement/vars/plugins/gettimeparting.md) stop - binnen.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimensiewaarden

Dimensiewaarden omvatten `12:00 AM` - `11:00 PM`, die het uur van de dag vertegenwoordigt waarop de treffer heeft plaatsgevonden (naar beneden afgerond). Als een hit bijvoorbeeld om 15.58 uur wordt gegenereerd, wordt deze gegroepeerd onder de waarde voor de dimensie van `3:00 PM`.
