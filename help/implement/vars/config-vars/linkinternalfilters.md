---
title: linkInternalFilters
description: Gebruik de variabele linkInternalFilters om het automatisch volgen van de uitgangsverbinding te helpen.
translation-type: tm+mt
source-git-commit: ec93137d0b5334e312fe0ec42953457243117d4a
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 1%

---


# linkInternalFilters

AppMeasurement biedt de capaciteit om verbindingen automatisch te volgen die buiten uw plaats richten. Als [`trackExternalLinks`](trackexternallinks.md) deze optie is ingeschakeld, wordt een verzoek om een afbeelding naar de rechterkant van de Adobe verzonden wanneer een bezoeker op een koppeling klikt om de site te verlaten. De [`linkExternalFilters`](linkexternalfilters.md) en `linkInternalFilters` variabelen bepalen welke verbindingen als intern/extern worden beschouwd.

Als deze variabele een waarde bevat, gedraagt het automatisch volgen van de uitgangsverbinding zich als een lijst van afgewezen personen. Als een verbindingsklik geen waarden aanpast, wordt het beschouwd als een uitgangsverbinding. `linkInternalFilters` De volledige URL wordt op basis van deze variabele gecontroleerd. Als [`linkLeaveQueryString`](linkleavequerystring.md) wordt toegelaten, wordt het vraagkoord ook onderzocht.

Als u zowel `linkInternalFilters` als `linkExternalFilters` gelijktijdig gebruikt, moet de geklikte verbinding aanpassen `linkExternalFilters` en niet aanpassen **** `linkInternalFilters` om als uitgangsverbinding te worden beschouwd. Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

De kaart van de activiteit gebruikt deze variabele helpen bepalen welke verbindingen intern aan uw plaats zijn. Adobe raadt u aan deze variabele in te stellen voor implementaties die een activiteitenoverzicht gebruiken.

>[!NOTE]
>
>`linkInternalFilters` en [Interne URL-filters](/help/admin/admin/internal-url-filter-admin.md) zijn afzonderlijke functies die voor verschillende doeleinden worden gebruikt. De `linkInternalFilters` variabele werkt specifiek voor het volgen van de uitgangsverbinding. Interne URL-filters zijn een Admin-instelling die helpt bij de dimensies van verkeersbronnen, zoals Refering Domain.

## Uitgaande koppelingen - Nooit track in Adobe Experience Platform Launch

Het veld Nooit bijhouden is een lijst met door komma&#39;s gescheiden filters (gewoonlijk domeinen) onder de [!UICONTROL Link Tracking] accordeon wanneer de Adobe Analytics-extensie wordt geconfigureerd.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL Link Tracking] [!UICONTROL Outbound Links - Never Track] veld onthult.

Plaats filters die u nooit als uitgangsverbindingen in dit gebied wilt worden gevolgd. Scheid meerdere domeinen met een komma zonder spatie.

## s.linkInternalFilters in AppMeasurement en Launch, aangepaste code-editor

De `s.linkInternalFilters` variabele is een tekenreeks met filters (zoals domeinen) die u als intern voor uw site beschouwt. Scheid meerdere filters met een komma zonder spaties.

```js
s.linkInternalFilters = "example.com,example.net";
```

Bekijk het volgende implementatievoorbeeld alsof dit is ingeschakeld `adobe.com`:

```html
<script>
  s.trackExternalLinks = true;
  s.linkInternalFilters = "adobe.com";
</script>

<!-- The following link is an exit link because it does not match the anything under linkInternalFilters -->
<a href = "example.org">Example link 2</a>
```
