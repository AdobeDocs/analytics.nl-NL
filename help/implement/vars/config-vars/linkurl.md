---
title: linkURL
description: Overschrijf de automatisch gegenereerde link-URL die AppMeasurement gebruikt in koppelingsvolgaanroepen.
feature: Appmeasurement Implementation
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
role: Admin, Developer
source-git-commit: 24101efe2b860734c9d176ba8be8f17e26429442
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---

# linkURL

Wanneer een koppelingenvolgvraag naar Adobe wordt verzonden, detecteert AppMeasurement de URL waarop is geklikt. Deze URL helpt het verbindingstype, zoals downloadverbindingen en uitgangsverbindingen bepalen. Gebruik de variabele `linkURL` om de gedetecteerde URL te overschrijven.

Er zijn geen dimensies in Analysis Workspace die rapporteren over deze variabele. Het bevolkt de `page_event_var1` kolom in [ het voer van Gegevens ](/help/export/analytics-data-feed/data-feed-overview.md). Als u URL van een klikte verbinding wilt volgen, adviseert Adobe gebruikend een douanevariabele, zoals a [ Prop ](../page-vars/prop.md). Het gebruik van [ Activity Map ](/help/analyze/activity-map/overview.md) kan helpen de gegevensinzameling voor geklikte verbindingen stroomlijnen.

## URL koppelen met de Web SDK

De koppeling-URL wordt toegewezen aan de volgende variabelen:

* [ voorwerp XDM ](/help/implement/aep-edge/xdm-var-mapping.md): `web.webInteraction.URL`
* [ voorwerp van Gegevens ](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.linkURL` of `data.__adobe.analytics.pev1`

## URL koppelen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.linkURL in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.linkURL` is een tekenreeks die de volledige URL van de aangeklikte koppeling bevat. Deze variabele vult geen dimensies in die beschikbaar zijn in de rapportage.

```js
s.linkURL = "https://example.com";
```

Als het derde argument van [ tl () ](../functions/tl-method.md) methode niet wordt geplaatst, wordt de `linkURL` variabele gebruikt in plaats daarvan.
