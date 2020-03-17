---
description: De verwerkingsregels kunnen gebeurtenissen teweegbrengen die op de variabelen van de Gegevens van de Context worden gebaseerd.
subtopic: Processing rules
title: Een gebeurtenis instellen met een variabele van een contextgegevens
topic: Admin tools
uuid: 4a6018eb-03e2-4ec8-874b-e48bf716e103
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Een gebeurtenis instellen met een variabele van een contextgegevens

De verwerkingsregels kunnen gebeurtenissen teweegbrengen die op de variabelen van de Gegevens van de Context worden gebaseerd.

De variabelen van contextgegevens worden gespecificeerd in AppMeasurement in het volgende formaat:

```
 s.contextData['search_term']
```

De [!UICONTROL Context Variables] lijst bevat alle variabelen die de afgelopen 30 dagen naar de rapportsuite zijn verzonden. Als u de naam van de variabele van contextgegevens kent maar niet het in de huidige rapportreeks hebt verzonden, kunt u een waarde toevoegen door de veranderlijke naam te typen en te klikken **[!UICONTROL Add variable name context data]**:

![](assets/add-context-variable.png)

De volgende regeldefinitie breidt zich op het [Exemplaar uit een Variabele van de Gegevens van de Context aan een eVar](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md) regel om een gebeurtenis op elke slag ook te plaatsen die een specifieke variabele van contextgegevens bevat:

| Regelset | Waarde |
|---|---|
| Voorwaarde | Als de contextgegevens &#39;search_term&#39; zijn ingesteld |
| Handeling | Gebeurtenis &#39;zoeken&#39; instellen |

Bijvoorbeeld:

![](assets/processing_rule_set_event.png)

Zie [Contextgegevensvariabelen](https://marketing.adobe.com/resources/help/en_US/sc/implement/context_data_variables.html) in de Help bij Implementatie.
