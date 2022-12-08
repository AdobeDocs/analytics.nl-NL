---
description: U kunt waarden vergelijken met veelvoorkomende spelfouten en deze bijwerken zodat ze correct worden weergegeven in rapporten.
subtopic: Processing rules
title: Waarden in een rapport opschonen
feature: Admin Tools
uuid: fcd72afc-3a3c-47a9-a5e4-53389dba7d83
exl-id: 109005a3-2ea4-4b61-a733-d1019218ec56
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 12%

---

# Waarden in een rapport opschonen

U kunt waarden vergelijken met veelvoorkomende spelfouten en deze bijwerken zodat ze correct worden weergegeven in rapporten.

Gebruik de meest restrictieve optie die beschikbaar is om ervoor te zorgen dat andere waarden niet per ongeluk met elkaar overeenkomen. U kunt een rapport over de variabele (prop1 in het onderstaande voorbeeld) in werking stellen en naar de termijnen zoeken u om te vervangen om ervoor te zorgen het niet onbedoelde waarden aanpast. Tekenreeksvergelijkingen zijn niet hoofdlettergevoelig.

| Regelset | Waarde |
|---|---|
| Voorwaarde | Als prop1 begint met winkelen |
| Handeling | Overschrijf de waarde van prop1 naar Aangepaste waarde voor winkelen |

Bijvoorbeeld:

![](assets/clean-up-values-in-report.png)
