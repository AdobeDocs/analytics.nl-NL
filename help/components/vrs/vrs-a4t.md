---
description: Speciale overwegingen bij het gebruik van virtuele A4T- en Adobe Analytics-rapportensuites
title: Virtuele rapportsuites en Analytics voor Doel (A4T)
feature: VRS
exl-id: b81e5100-f512-4219-a8ab-5d7f6219d206
source-git-commit: 7a47d837eeae65f2e98123aca78029bfeb7ffe9d
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Virtuele rapportsuites en Analytics voor Doel (A4T)

Houd rekening met deze voorbehouden wanneer u virtuele rapportsuites gebruikt in de context van Adobe Target:

* U kunt gegevens niet rechtstreeks van Target naar een virtuele rapportsuite verzenden, alleen naar een echte rapportsuite.
* U kunt over activiteiten A4T binnen een virtuele rapportreeks rapporteren. Nochtans, zijn de gegevens A4T beperkt tot die rijen die het virtuele segment van de rapportreeks (en om het even welke andere toegepaste segmenten) aanpassen. Als u bijvoorbeeld een virtuele rapportsuite voor uw EMEA-klanten hebt gemaakt, weerspiegelen de A4T-gegevens in die virtuele rapportsuite alleen de Target-gegevens voor uw EMEA-klanten.
* U kunt geen segmenten van een virtuele rapportsuite voor activering opnieuw naar Target publiceren.
