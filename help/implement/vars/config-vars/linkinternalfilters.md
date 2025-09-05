---
title: linkInternalFilters
description: Gebruik de variabele linkInternalFilters om het automatisch volgen van de uitgangsverbinding te helpen.
feature: Appmeasurement Implementation
exl-id: eaa6e64a-ebd5-4e6b-913f-1a6c315579c8
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# linkInternalFilters

AppMeasurement biedt de mogelijkheid om koppelingen die buiten uw site wijzen automatisch bij te houden. Als [`trackExternalLinks`](trackexternallinks.md) (AppMeasurement) of [`clickCollectionEnabled`](trackdownloadlinks.md) (Web SDK) is ingeschakeld, wordt een verzoek om een afbeelding naar Adobe verzonden, aangezien een bezoeker op een koppeling klikt om uw site te verlaten. De variabelen [`linkExternalFilters`](linkexternalfilters.md) en `linkInternalFilters` bepalen welke koppelingen als intern/extern worden beschouwd.

Als deze variabele een waarde bevat, gedraagt het automatisch volgen van de uitgangsverbinding zich als een lijst van gewezen personen. Als een koppelingsklik niet overeenkomt met een `linkInternalFilters` -waarde, wordt deze beschouwd als een afsluitkoppeling. De volledige URL wordt op basis van deze variabele gecontroleerd. Als [`linkLeaveQueryString`](linkleavequerystring.md) is ingeschakeld, wordt de queryreeks ook gecontroleerd.

Als u zowel `linkInternalFilters` als `linkExternalFilters` gelijktijdig gebruikt, moet de geklikte verbinding `linkExternalFilters` **aanpassen en** niet `linkInternalFilters` aanpassen om als uitgangsverbinding te worden beschouwd. Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

De kaart van de activiteit gebruikt deze variabele helpen bepalen welke verbindingen intern aan uw plaats zijn. Adobe raadt u aan deze variabele in te stellen voor implementaties die activiteitenoverzicht gebruiken.

>[!NOTE]
>
>`linkInternalFilters` en [ Interne filters URL ](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) zijn afzonderlijke eigenschappen die afzonderlijke doeleinden vervullen. De variabele `linkInternalFilters` werkt specifiek voor het bijhouden van koppelingen. Interne URL-filters zijn een Admin-instelling die helpt bij de dimensies van verkeersbronnen, zoals Refering Domain.

## Koppelingen afsluiten in de Web SDK

Koppelingen worden automatisch gekwalificeerd als een afsluitkoppeling als het doeldomein van de koppeling afwijkt van de huidige `window.location.hostname` . Web SDK biedt geen configuratievariabelen aan om automatische uitgangsverbindingsopsporing te wijzigen. Als u de domeinen moet aanpassen die als uitgangsverbinding kwalificeren, kunt u douanelogica in `onBeforeEventSend` callback gebruiken.

Zie [ Automatische verbinding het volgen ](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html#automaticLinkTracking) in de documentatie van SDK van het Web voor meer informatie.

## Uitgaande koppelingen - Nooit bijhouden met Adobe Analytics-extensie

Het veld Nooit bijhouden is een lijst met door komma&#39;s gescheiden filters (meestal domeinen) onder de accordeon [!UICONTROL Link Tracking] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Link Tracking] uit, zodat het veld [!UICONTROL Outbound Links - Never Track] zichtbaar wordt.

Plaats filters die u nooit als uitgangsverbindingen in dit gebied wilt worden gevolgd. Scheid meerdere domeinen met een komma zonder spatie.

## s.linkInternalFilters in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.linkInternalFilters` is een tekenreeks met filters (zoals domeinen) die u als intern voor uw site beschouwt. Scheid meerdere filters met een komma zonder spaties.

```js
s.linkInternalFilters = "example.com,example.net";
```

Bekijk het volgende implementatievoorbeeld alsof deze zich op `adobe.com` bevindt:

```html
<script>
  s.trackExternalLinks = true;
  s.linkInternalFilters = "adobe.com";
</script>

<!-- The following link is an exit link because it does not match the anything under linkInternalFilters -->
<a href = "example.org">Example link 2</a>
```
