---
title: Minuut
description: De minuut waarop metrisch voorkwam.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Minuut

De dimensie &#39;Minute&#39; rapporteert de minuut dat een bepaalde metrische waarde is opgetreden (naar beneden afgerond). Het eerste afmetingspunt is de eerste minuut in de datumwaaier, en het laatste afmetingspunt is de laatste minuut in de datumwaaier. Deze dimensie is waardevol voor trended rapporten, aangezien het u toestaat om metriek in tijd te zien. Gezien hoe korrelig deze dimensie is, raadt Adobe aan het bereik van de rapportdatum te beperken tot één of twee dagen.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimensie-items

Dimensie-items bevatten een bepaalde minuut binnen het datumbereik van een rapport naast de datum. Het is opgemaakt als `HH:MM YYYY-MM-DD`. Dimensie-items die beginnen met `00:00` equate to middernacht op die dag, terwijl waarden die beginnen met `23:59` gelijk zijn aan 23:59 voor die dag.
