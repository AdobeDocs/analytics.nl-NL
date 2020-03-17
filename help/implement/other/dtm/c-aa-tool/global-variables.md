---
description: Veldbeschrijvingen en informatie over variabelen wanneer u Dynamic Tag Management gebruikt om Adobe Analytics te implementeren.
keywords: Dynamic Tag Management;global variables;server variable;evar;props;dynamic variable prefix;dynamic variable
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: Algemene variabelen
uuid: d759320a-96ee-4073-b5fd-5257b7033003
translation-type: tm+mt
source-git-commit: 664d0cde8b8b17c86b47858611d459026aab0bef

---


# Algemene variabelen

Veldbeschrijvingen en informatie over variabelen wanneer u Dynamic Tag Management gebruikt om Adobe Analytics te implementeren.

Deze variabelen worden op alle regelbakens voor het laden van de pagina geactiveerd. U kunt hetzelfde effect bereiken door een [regel voor het laden van pagina&#39;s](/help/implement/other/dtm/c-rules/t-rules-page-conditions.md) te gebruiken die op alle pagina&#39;s kan worden geactiveerd. These variables might not fire in [Direct-Call](/help/implement/other/dtm/c-rules/t-rules-direct-conditions.md) and [Event-Based](/help/implement/other/dtm/c-rules/t-rules-event-conditions.md) rules.

## Algemene variabelen - Veldbeschrijvingen {#section_2917F62FCC8D43F982B2612A702DEF81}

**[!UICONTROL  *`Property`*]** > ![](assets/settings_gear.png) **[!UICONTROL Edit Tool]** > **[!UICONTROL Global Variables]**

| Element | Beschrijving |
|--- |--- |
| Server | De vooraf gedefinieerde variabele vult de dimensie Servers in Adobe Analytics. Zie [Server](../../../vars/page-vars/server.md). |
| eVars | [De variabelen](../../../vars/page-vars/evar.md) van eVar worden gebruikt voor de bouw van de rapporten van de douaneomzetting. |
| Props | [Prop-variabelen](../../../vars/page-vars/prop.md) worden gebruikt voor het samenstellen van aangepaste verkeersrapporten. |
| Dynamisch variabele voorvoegsel | Een speciaal voorvoegsel voor het begin van de waarde. Het standaardvoorvoegsel is &quot;D=&quot;. Zie [Dynamische variabelen](../../../vars/page-vars/dynamic-variables.md |
