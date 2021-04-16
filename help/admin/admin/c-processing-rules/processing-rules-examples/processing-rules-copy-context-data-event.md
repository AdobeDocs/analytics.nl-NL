---
description: De verwerkingsregels kunnen gebeurtenissen teweegbrengen die op de variabelen van de Gegevens van de Context worden gebaseerd.
subtopic: Processing rules
title: Een gebeurtenis instellen met een contextdatavariabele
feature: Admin Tools
uuid: 4a6018eb-03e2-4ec8-874b-e48bf716e103
exl-id: f0af0e23-c08a-4f82-85b4-25064eeaa3c6
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 12%

---

# Een gebeurtenis instellen met een contextdatavariabele

De verwerkingsregels kunnen gebeurtenissen teweegbrengen die op de variabelen van de Gegevens van de Context worden gebaseerd.

De variabelen van contextgegevens worden gespecificeerd in AppMeasurement in het volgende formaat:

```
 s.contextData['search_term']
```

De lijst [!UICONTROL Context Variables] bevat alle variabelen die in de voorafgaande 30 dagen naar de rapportreeks zijn verzonden. Als u de naam van de variabele van contextgegevens kent maar niet het in de huidige rapportreeks hebt verzonden, kunt u een waarde toevoegen door de variabelenaam te typen en **[!UICONTROL Add variable name context data]** te klikken:

![](assets/add-context-variable.png)

De volgende regeldefinitie breidt zich op [Kopieer een Variabele van de Gegevens van de Context aan een eVar](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md) regel uit om een gebeurtenis op elke slag ook te plaatsen die een specifieke variabele van contextgegevens bevat:

| Regelset | Waarde |
|---|---|
| Voorwaarde | Als de contextgegevens &#39;search_term&#39; zijn ingesteld |
| Handeling | Gebeurtenis &#39;zoeken&#39; instellen |

Bijvoorbeeld:

![](assets/processing_rule_set_event.png)

Zie [Contextgegevensvariabelen](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/contextdata.html) in de Help bij de implementatie.
