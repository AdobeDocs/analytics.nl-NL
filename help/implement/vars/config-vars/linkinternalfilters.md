---
title: linkInternalFilters
description: Gebruik de variabele linkInternalFilters om het automatisch volgen van de uitgangsverbinding te helpen.
exl-id: eaa6e64a-ebd5-4e6b-913f-1a6c315579c8
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# linkInternalFilters

AppMeasurement biedt de capaciteit om verbindingen automatisch te volgen die buiten uw plaats richten. Als [`trackExternalLinks`](trackexternallinks.md) is ingeschakeld, wordt een verzoek om een afbeelding naar de rechterkant van de Adobe verzonden wanneer een bezoeker op een koppeling klikt om uw site te verlaten. De variabelen [`linkExternalFilters`](linkexternalfilters.md) en `linkInternalFilters` bepalen welke verbindingen als intern/extern worden beschouwd.

Als deze variabele een waarde bevat, gedraagt het automatisch volgen van de uitgangsverbinding zich als een lijst van gewezen personen. Als een verbindingsklik geen `linkInternalFilters` waarden aanpast, wordt het beschouwd als een uitgangsverbinding. De volledige URL wordt op basis van deze variabele gecontroleerd. Als [`linkLeaveQueryString`](linkleavequerystring.md) wordt toegelaten, wordt het vraagkoord ook onderzocht.

Als u zowel `linkInternalFilters` als `linkExternalFilters` gelijktijdig gebruikt, moet de aangeklikte verbinding `linkExternalFilters` **en** niet `linkInternalFilters` aanpassen om als uitgangsverbinding te worden beschouwd. Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

De kaart van de activiteit gebruikt deze variabele helpen bepalen welke verbindingen intern aan uw plaats zijn. Adobe raadt u aan deze variabele in te stellen voor implementaties die een activiteitenoverzicht gebruiken.

>[!NOTE]
>
>`linkInternalFilters` en  [Interne URL-](/help/admin/admin/internal-url-filter-admin.md) filters zijn afzonderlijke functies die voor verschillende doeleinden worden gebruikt. De variabele `linkInternalFilters` werkt specifiek voor het volgen van de uitgangsverbinding. Interne URL-filters zijn een Admin-instelling die helpt bij de dimensies van verkeersbronnen, zoals Refering Domain.

## Uitgaande koppelingen - Nooit bijhouden met tags in Adobe Experience Platform

Het veld Nooit bijhouden is een lijst met door komma&#39;s gescheiden filters (gewoonlijk domeinen) onder de accordeon [!UICONTROL Link Tracking] wanneer de Adobe Analytics-extensie wordt geconfigureerd.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Link Tracking] uit, zodat het veld [!UICONTROL Outbound Links - Never Track] zichtbaar wordt.

Plaats filters die u nooit als uitgangsverbindingen in dit gebied wilt worden gevolgd. Scheid meerdere domeinen met een komma zonder spatie.

## s.linkInternalFilters in AppMeasurement en aangepaste code-editor

De variabele `s.linkInternalFilters` is een tekenreeks met filters (zoals domeinen) die u als intern voor uw site beschouwt. Scheid meerdere filters met een komma zonder spaties.

```js
s.linkInternalFilters = "example.com,example.net";
```

Bekijk het volgende implementatievoorbeeld alsof het zich op `adobe.com` bevond:

```html
<script>
  s.trackExternalLinks = true;
  s.linkInternalFilters = "adobe.com";
</script>

<!-- The following link is an exit link because it does not match the anything under linkInternalFilters -->
<a href = "example.org">Example link 2</a>
```
