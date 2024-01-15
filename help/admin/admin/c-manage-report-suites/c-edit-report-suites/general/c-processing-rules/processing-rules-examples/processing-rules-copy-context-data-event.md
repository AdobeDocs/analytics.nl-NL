---
description: De verwerkingsregels kunnen gebeurtenissen teweegbrengen die op de variabelen van de Gegevens van de Context worden gebaseerd.
subtopic: Processing rules
title: Een gebeurtenis instellen met een variabele van een contextgegevens
feature: Admin Tools
role: Admin
exl-id: f0af0e23-c08a-4f82-85b4-25064eeaa3c6
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---

# Een gebeurtenis instellen met een variabele van een contextgegevens

De verwerkingsregels kunnen gebeurtenissen teweegbrengen die op de variabelen van de Gegevens van de Context worden gebaseerd.

Contextgegevensvariabelen worden in AppMeasurement in de volgende indeling opgegeven:

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
