---
description: De verwerkingsregels kunnen gebeurtenissen teweegbrengen die op de variabelen van de Gegevens van de Context worden gebaseerd.
subtopic: Processing rules
title: Een gebeurtenis instellen met een contextdatavariabele
feature: Admin Tools
uuid: 4a6018eb-03e2-4ec8-874b-e48bf716e103
exl-id: f0af0e23-c08a-4f82-85b4-25064eeaa3c6
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 11%

---

# Een gebeurtenis instellen met een contextdatavariabele

De verwerkingsregels kunnen gebeurtenissen teweegbrengen die op de variabelen van de Gegevens van de Context worden gebaseerd.

De variabelen van contextgegevens worden gespecificeerd in AppMeasurement in het volgende formaat:

```
 s.contextData['search_term']
```

De [!UICONTROL Context Variables] lijst bevat alle variabelen die in de afgelopen 30 dagen naar de rapportsuite zijn verzonden. Als u de naam van de variabele van de contextgegevens kent maar het niet naar de huidige rapportreeks hebt verzonden, kunt u een waarde toevoegen door de veranderlijke naam te typen en te klikken **[!UICONTROL Add variable name context data]**:

![](assets/add-context-variable.png)

De volgende regeldefinitie breidt zich uit op de [Een contextgegevensvariabele naar een eVar kopiëren](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md) regel om ook een gebeurtenis in te stellen voor elke hit die een specifieke variabele van de contextgegevens bevat:

| Regelset | Waarde |
|---|---|
| Voorwaarde | Als de contextgegevens &#39;search_term&#39; zijn ingesteld |
| Handeling | Gebeurtenis &#39;zoeken&#39; instellen |

Bijvoorbeeld:

![](assets/processing_rule_set_event.png)

Zie [Contextgegevensvariabelen](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/contextdata.html) in de Help bij de implementatie.
