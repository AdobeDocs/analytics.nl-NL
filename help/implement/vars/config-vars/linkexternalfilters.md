---
title: linkExternalFilters
description: Gebruik de variabele linkExternalFilters om het automatisch volgen van de afsluitverbinding te helpen.
feature: Appmeasurement Implementation
exl-id: 7d4e8d96-17ee-4a04-9a57-37d2056ee9a7
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# linkExternalFilters

AppMeasurement biedt de mogelijkheid om koppelingen die buiten uw site wijzen automatisch bij te houden. Als [`trackExternalLinks`](trackexternallinks.md) (AppMeasurement) of [`clickCollectionEnabled`](trackexternallinks.md) (Web SDK) is ingeschakeld, wordt een verzoek om een afbeelding naar Adobe verzonden, aangezien een bezoeker op een koppeling klikt om uw site te verlaten. De variabelen `linkExternalFilters` en [`linkInternalFilters`](linkinternalfilters.md) bepalen welke koppelingen als intern/extern worden beschouwd.

Als deze variabele een waarde bevat, gedraagt het automatisch volgen van de uitgangsverbinding zich als een lijst van gewenste personen. Als een koppelingsklik niet overeenkomt met een `linkExternalFilters` -waarde, wordt deze niet beschouwd als een afsluitkoppeling. De volledige URL wordt op basis van deze variabele gecontroleerd. Als [`linkLeaveQueryString`](linkleavequerystring.md) is ingeschakeld, wordt de queryreeks ook gecontroleerd.

>[!TIP]
>
>Gebruik deze variabele alleen als u precies weet welke domeinen u als exit-koppelingen wilt beschouwen. Veel organisaties vinden het gebruik van `linkInternalFilters` voldoende voor het bijhouden van afsluitingskoppelingen en gebruiken `linkExternalFilters` niet.

Als u zowel `linkInternalFilters` als `linkExternalFilters` gelijktijdig gebruikt, moet de geklikte verbinding `linkExternalFilters` **aanpassen en** niet `linkInternalFilters` aanpassen om als uitgangsverbinding te worden beschouwd. Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

## Koppelingen afsluiten in de Web SDK

Koppelingen worden automatisch gekwalificeerd als een afsluitkoppeling als het doeldomein van de koppeling afwijkt van de huidige `window.location.hostname` . Web SDK biedt geen configuratievariabelen aan om automatische uitgangsverbindingsopsporing te wijzigen. Als u de domeinen moet aanpassen die als uitgangsverbinding kwalificeren, kunt u douanelogica in `onBeforeEventSend` callback gebruiken.

Zie [ Automatische verbinding het volgen ](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html#automaticLinkTracking) in de documentatie van SDK van het Web voor meer informatie.

## Uitgaande koppelingen - Bijhouden met de Adobe Analytics-extensie

Het veld Track is een door komma&#39;s gescheiden lijst met filters (doorgaans domeinen) onder de accordeon [!UICONTROL Link Tracking] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Link Tracking] uit, zodat het veld [!UICONTROL Outbound Links - Track] zichtbaar wordt.

Plaats filters die u altijd als extern wilt beschouwen in dit veld. Scheid meerdere domeinen met een komma zonder spatie.

## s.linkExternalFilters in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.linkExternalFilters` is een tekenreeks met filters (zoals domeinen) die u kunt gebruiken om koppelingen af te sluiten. Scheid meerdere domeinen met een komma zonder spaties.

```js
s.linkExternalFilters = "example.com,example.net,example.org";
```

Bekijk het volgende implementatievoorbeeld alsof deze zich op `adobe.com` bevindt:

```html
<script>
  s.trackExternalLinks = true;
  s.linkExternalFilters = "example.com,example.net";
</script>

<!-- The following link is NOT considered an exit link, even though the link is outside adobe.com -->
<a href = "example.org">Example link 1</a>

<!-- The following link is an exit link because it matches the linkExternalFilters allowlist -->
<a href = "example.com">Example link 2</a>
```
