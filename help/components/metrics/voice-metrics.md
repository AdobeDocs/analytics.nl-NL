---
title: Metrische spraakanalyse
description: Metrische spraakanalyse
feature: Metrics
exl-id: 3c1b4e4e-d8d2-446f-9582-a2ce5580a8d3
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 1%

---

# Metrische spraakanalyse

Wanneer u [!UICONTROL Voice and Chatbots] op [[!UICONTROL Application reporting]](/help/admin/tools/manage-rs/edit-settings/app-reporting.md) toelaat, worden de volgende metriek (en [ afmetingen ](../dimensions/voice-dimensions.md)) gecreeerd. U kunt [ variabelen van de Contextgegevens ](/help/implement/vars/page-vars/contextdata.md) gebruiken om hen aan een waarde van `1` (of meer indien van toepassing) te plaatsen. Wanneer toegelaten in de montages van de rapportreeks, [ worden de regels van de Verwerking ](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md) automatisch gecreeerd die metriek van de stemanalyse aan hun bijbehorende variabele van contextgegevens in kaart brengen.

| Metrische naam | Beschrijving | Variabele van contextgegevens |
| --- | --- | --- |
| Voicubetters | Triggers wanneer een bevel aan een stemmedewerker wordt uitgegeven. | `a.voiceutterances` |
| Sessie einde stem | Triggers wanneer de stem-app wordt gesloten. | `a.voiceendsession` |
| Spraakfout | Triggers wanneer de stem-app een fout aantreft. | `a.voiceerror` |

{style="table-layout:auto"}
