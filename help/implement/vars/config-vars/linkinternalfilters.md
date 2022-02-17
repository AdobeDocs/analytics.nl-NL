---
title: linkInternalFilters
description: Gebruik de variabele linkInternalFilters om het automatisch volgen van de uitgangsverbinding te helpen.
feature: Variables
exl-id: eaa6e64a-ebd5-4e6b-913f-1a6c315579c8
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# linkInternalFilters

AppMeasurement biedt de capaciteit om verbindingen automatisch te volgen die buiten uw plaats richten. Indien [`trackExternalLinks`](trackexternallinks.md) is ingeschakeld, wordt een verzoek om een afbeelding naar de rechterkant van de Adobe verzonden wanneer een bezoeker op een koppeling klikt om uw site te verlaten. De [`linkExternalFilters`](linkexternalfilters.md) en `linkInternalFilters` variabelen bepalen welke koppelingen als intern/extern worden beschouwd.

Als deze variabele een waarde bevat, gedraagt het automatisch volgen van de uitgangsverbinding zich als een lijst van gewezen personen. Als een koppeling niet overeenkomt met een koppeling `linkInternalFilters` waarden, wordt het beschouwd als een uitgangsverbinding. De volledige URL wordt op basis van deze variabele gecontroleerd. Indien [`linkLeaveQueryString`](linkleavequerystring.md) wordt toegelaten, wordt het vraagkoord ook onderzocht.

Als u beide `linkInternalFilters` en `linkExternalFilters` tegelijkertijd, moet de geklikte verbinding aanpassen `linkExternalFilters` **en** niet overeenkomen `linkInternalFilters` te worden beschouwd als een exitkoppeling. Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

De kaart van de activiteit gebruikt deze variabele helpen bepalen welke verbindingen intern aan uw plaats zijn. Adobe raadt u aan deze variabele in te stellen voor implementaties die een activiteitenoverzicht gebruiken.

>[!NOTE]
>
>`linkInternalFilters` en [Interne URL-filters](/help/admin/admin/internal-url-filter-admin.md) Dit zijn afzonderlijke functies die voor verschillende doeleinden worden gebruikt. De `linkInternalFilters` variabele werkt specifiek voor het volgen van de uitgangsverbinding. Interne URL-filters zijn een Admin-instelling die helpt bij de dimensies van verkeersbronnen, zoals Refering Domain.

## Uitgaande koppelingen - Nooit bijhouden met tags in Adobe Experience Platform

Het veld Nooit bijhouden is een door komma&#39;s gescheiden lijst met filters (meestal domeinen) onder het veld [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Outbound Links - Never Track] veld.

Plaats filters die u nooit als uitgangsverbindingen in dit gebied wilt worden gevolgd. Scheid meerdere domeinen met een komma zonder spatie.

## s.linkInternalFilters in AppMeasurement en aangepaste code-editor

De `s.linkInternalFilters` variabele is een tekenreeks met filters (zoals domeinen) die u als intern voor uw site beschouwt. Scheid meerdere filters met een komma zonder spaties.

```js
s.linkInternalFilters = "example.com,example.net";
```

Neem het volgende implementatievoorbeeld alsof het actief is `adobe.com`:

```html
<script>
  s.trackExternalLinks = true;
  s.linkInternalFilters = "adobe.com";
</script>

<!-- The following link is an exit link because it does not match the anything under linkInternalFilters -->
<a href = "example.org">Example link 2</a>
```
