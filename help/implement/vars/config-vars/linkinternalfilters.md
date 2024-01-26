---
title: linkInternalFilters
description: Gebruik de variabele linkInternalFilters om het automatisch volgen van de uitgangsverbinding te helpen.
feature: Variables
exl-id: eaa6e64a-ebd5-4e6b-913f-1a6c315579c8
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# linkInternalFilters

AppMeasurement biedt de mogelijkheid om koppelingen die buiten uw site wijzen automatisch bij te houden. Indien [`trackExternalLinks`](trackexternallinks.md) (AppMeasurement) of [`clickCollectionEnabled`](trackdownloadlinks.md) (Web SDK) is ingeschakeld, wordt een verzoek om een afbeelding naar de rechterkant van de Adobe verzonden wanneer een bezoeker op een koppeling klikt om uw site te verlaten. De [`linkExternalFilters`](linkexternalfilters.md) en `linkInternalFilters` variabelen bepalen welke koppelingen als intern/extern worden beschouwd.

Als deze variabele een waarde bevat, gedraagt het automatisch volgen van de uitgangsverbinding zich als een lijst van gewezen personen. Als een koppeling niet overeenkomt met een `linkInternalFilters` waarden, wordt het beschouwd als een uitgangsverbinding. De volledige URL wordt op basis van deze variabele gecontroleerd. Indien [`linkLeaveQueryString`](linkleavequerystring.md) wordt toegelaten, wordt het vraagkoord ook onderzocht.

Als u beide `linkInternalFilters` en `linkExternalFilters` tegelijkertijd, moet de geklikte verbinding aanpassen `linkExternalFilters` **en** niet overeenkomen `linkInternalFilters` te worden beschouwd als een exitkoppeling. Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

De kaart van de activiteit gebruikt deze variabele helpen bepalen welke verbindingen intern aan uw plaats zijn. Adobe raadt aan deze variabele in te stellen voor implementaties die een activiteitenoverzicht gebruiken.

>[!NOTE]
>
>`linkInternalFilters` en [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md) Dit zijn afzonderlijke functies die voor verschillende doeleinden worden gebruikt. De `linkInternalFilters` variabele werkt specifiek voor het volgen van de uitgangsverbinding. Interne URL-filters zijn een Admin-instelling die helpt bij de dimensies van verkeersbronnen, zoals Refering Domain.

## De verbindingen van de uitgang in SDK van het Web

Koppelingen worden automatisch gekwalificeerd als een afsluitkoppeling als het doeldomein van de koppeling afwijkt van het huidige `window.location.hostname`. De SDK van het Web biedt geen configuratievariabelen aan om automatische uitgangsverbindingsopsporing te wijzigen. Als u de domeinen moet aanpassen die als uitgangsverbinding kwalificeren, kunt u douanelogica in gebruiken `onBeforeEventSend` callback.

Zie [Automatisch koppelingen bijhouden](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html#automaticLinkTracking) in de documentatie van SDK van het Web voor meer informatie.

## Uitgaande koppelingen - Nooit bijhouden met Adobe Analytics-extensie

Het veld Nooit bijhouden is een door komma&#39;s gescheiden lijst met filters (meestal domeinen) onder het veld [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Outbound Links - Never Track] veld.

Plaats filters die u nooit als uitgangsverbindingen in dit gebied wilt worden gevolgd. Scheid meerdere domeinen met een komma zonder spatie.

## s.linkInternalFilters in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

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
