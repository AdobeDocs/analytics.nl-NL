---
title: Minuut
description: De minuut waarop metrisch voorkwam.
feature: Dimensions
exl-id: 63f13083-321f-4fd8-9352-e413e1ebf168
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Minuut

De dimensie &#39;Minute&#39; rapporteert de minuut dat een bepaalde metrische waarde is opgetreden (naar beneden afgerond). Het eerste afmetingspunt is de eerste minuut in de datumwaaier, en het laatste afmetingspunt is de laatste minuut in de datumwaaier. Deze dimensie is waardevol voor trended rapporten, aangezien het u toestaat om metriek in tijd te zien. Gezien hoe korrelig deze dimensie is, beveelt Adobe aan het bereik van de rapportagedatum te beperken tot één of twee dagen.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

De punten van Dimension omvatten een bepaalde minuut binnen de de datumwaaier van een rapport naast zijn datum. Het is opgemaakt als `HH:MM YYYY-MM-DD`. Dimension-objecten beginnen met `00:00` is gelijk aan middernacht op die dag, terwijl de waarden beginnen met `23:59` gelijk aan 23:59 PM voor die dag.
