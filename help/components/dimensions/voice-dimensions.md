---
title: De afmetingen van de Steekanalyse
description: De afmetingen van de Steekanalyse
feature: Dimensions
exl-id: 6e1275c4-3b17-4c65-a308-d420ea1acdf6
source-git-commit: c2adf6d2e328378332cc290ba2dfd75ee6587ef6
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# De afmetingen van de Steekanalyse

Wanneer u [!UICONTROL Voice and Chatbots] op [[!UICONTROL Application reporting]](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/app-reporting.md) toelaat, worden de volgende afmetingen (en [ metriek ](../metrics/voice-metrics.md)) gecreeerd. U kunt [ variabelen van de Contextgegevens ](/help/implement/vars/page-vars/contextdata.md) gebruiken om hen aan de gewenste koordwaarde te plaatsen. Wanneer toegelaten in de montages van de rapportreeks, [ worden de regels van de Verwerking ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) automatisch gecreeerd die de dimensies van de stemanalyse van de kaart aan hun bijbehorende variabele van contextgegevens.

| Dimension-naam | Beschrijving | Variabele van contextgegevens |
| --- | --- | --- |
| Type spraakfout | Het type fout dat is aangetroffen. | `a.voiceerrortype` |
| Spraaktaal | De taal die de gebruiker met uw stem app in wisselwerking staat. | `a.voicelanguage` |
| Spraakintentie | De opdracht die de gebruiker wil uitvoeren. | `a.voiceintent` |
| Reactie van Voice-app | De reactie die de stem-app aan de gebruiker heeft geretourneerd. | `a.voiceappresponse` |
| Spraakverificatie | De voor authentiek verklaarde staat van de gebruiker wanneer het in wisselwerking staan met stem app. | `a.voiceauthentication` |
| Interesten-ID | De id van het punt van interesse. | `a.loc.poi.id` |

{style="table-layout:auto"}
