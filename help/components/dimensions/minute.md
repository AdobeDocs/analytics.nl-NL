---
title: Minuut
description: De minuut waarop metrisch voorkwam.
translation-type: tm+mt
source-git-commit: 2c262e5345c39a71a6a54062c607273528294b24
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Minuut

De dimensie &#39;Minute&#39; rapporteert de minuut dat een bepaalde metrische waarde is opgetreden (naar beneden afgerond). De waarde van de eerste dimensie is de eerste minuut in het datumbereik en de laatste waarde van de dimensie is de laatste minuut in het datumbereik. Deze dimensie is waardevol voor trended rapporten, aangezien het u toestaat om metriek in tijd te zien. Gezien hoe korrelig deze dimensie is, raadt Adobe aan het bereik van de rapportdatum te beperken tot één of twee dagen.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimensiewaarden

De waarden van de dimensie omvatten een bepaalde minuut binnen de de datumwaaier van een rapport naast zijn datum. Het is opgemaakt als `HH:MM YYYY-MM-DD`. De waarden van de afmeting beginnen met `00:00` gelijken aan middernacht op die dag, terwijl de waarden die met `23:59` gelijken aan 11:59 voor die dag beginnen.
