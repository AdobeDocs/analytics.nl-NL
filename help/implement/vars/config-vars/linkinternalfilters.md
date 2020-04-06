---
title: linkInternalFilters
description: Gebruik de variabele linkInternalFilters om het automatisch volgen van de uitgangsverbinding te helpen.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkInternalFilters

AppMeasurement biedt de capaciteit om verbindingen automatisch te volgen die buiten uw plaats richten. Als [`trackExternalLinks`](trackexternallinks.md) deze optie is ingeschakeld, wordt een verzoek om een afbeelding naar rechts verzonden wanneer een bezoeker op een koppeling klikt om uw site te verlaten. De [`linkExternalFilters`](linkexternalfilters.md) en `linkInternalFilters` variabelen bepalen welke verbindingen als intern/extern worden beschouwd.

Als deze variabele een waarde bevat, gedraagt het automatisch volgen van de uitgangsverbinding zich op een zwarte lijst-als manier. Als een verbindingsklik geen waarden aanpast, wordt het beschouwd als een uitgangsverbinding. `linkInternalFilters` De volledige URL wordt op basis van deze variabele gecontroleerd. Als [`linkLeaveQueryString`](linkleavequerystring.md) wordt toegelaten, wordt het vraagkoord ook onderzocht.

Als u zowel `linkInternalFilters` als `linkExternalFilters` gelijktijdig gebruikt, moet de geklikte verbinding aanpassen `linkExternalFilters` en niet aanpassen **** `linkInternalFilters` om als uitgangsverbinding te worden beschouwd. Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

>[!NOTE] `linkInternalFilters` en [Interne URL-filters](/help/admin/admin/internal-url-filter-admin.md) zijn afzonderlijke functies die voor verschillende doeleinden worden gebruikt. De `linkInternalFilters` variabele werkt specifiek voor het volgen van de uitgangsverbinding. Interne URL-filters zijn een Admin-instelling die helpt bij de dimensies van verkeersbronnen, zoals Refering Domain.

## Uitgaande koppelingen - Nooit bijhouden in Adobe Experience Platform Starten

Het veld Nooit bijhouden is een lijst met door komma&#39;s gescheiden filters (meestal domeinen) onder de [!UICONTROL Link Tracking] accordeon wanneer u de extensie Adobe Analytics configureert.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL Link Tracking] [!UICONTROL Outbound Links - Never Track] veld onthult.

Plaats filters die u nooit als uitgangsverbindingen in dit gebied wilt worden gevolgd. Scheid meerdere domeinen met een komma zonder spatie.

## s.linkInternalFilters in AppMeasurement en Launch, aangepaste code-editor

De `s.linkInternalFilters` variabele is een tekenreeks met filters (zoals domeinen) die u als intern voor uw site beschouwt. Scheid meerdere filters met een komma zonder spaties.

```js
s.linkInternalFilters = "example.com,example.net,example.org";
```

Bekijk het volgende implementatievoorbeeld alsof dit is ingeschakeld `adobe.com`:

```html
<script>
  s.trackExternalLinks = true;
  s.linkInternalFilters = "adobe.com";
</script>

<!-- The following link is an exit link because it does not match the anything under linkInternalFilters -->
<a href = "example.com">Example link 2</a>
```
