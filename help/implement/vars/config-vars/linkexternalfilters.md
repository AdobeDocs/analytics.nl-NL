---
title: linkExternalFilters
description: Gebruik de variabele linkExternalFilters om het automatisch volgen van de afsluitverbinding te helpen.
feature: Variables
exl-id: 7d4e8d96-17ee-4a04-9a57-37d2056ee9a7
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# linkExternalFilters

AppMeasurement biedt de capaciteit om verbindingen automatisch te volgen die buiten uw plaats richten. Indien [`trackExternalLinks`](trackexternallinks.md) (AppMeasurement) of [`clickCollectionEnabled`](trackexternallinks.md) (Web SDK) is ingeschakeld, wordt een verzoek om een afbeelding naar de rechterkant van de Adobe verzonden wanneer een bezoeker op een koppeling klikt om uw site te verlaten. De `linkExternalFilters` en [`linkInternalFilters`](linkinternalfilters.md) variabelen bepalen welke koppelingen als intern/extern worden beschouwd.

Als deze variabele een waarde bevat, gedraagt het automatisch volgen van de uitgangsverbinding zich als een lijst van gewenste personen. Als een koppeling niet overeenkomt met een koppeling `linkExternalFilters` waarden, wordt het niet beschouwd als een exit link. De volledige URL wordt op basis van deze variabele gecontroleerd. Indien [`linkLeaveQueryString`](linkleavequerystring.md) wordt toegelaten, wordt het vraagkoord ook onderzocht.

>[!TIP]
>
>Gebruik deze variabele alleen als u precies weet welke domeinen u als exit-koppelingen wilt beschouwen. Veel organisaties vinden dat `linkInternalFilters` is voldoende voor de behoeften voor het bijhouden van de exit-koppeling en gebruikt deze niet `linkExternalFilters`.

Als u beide `linkInternalFilters` en `linkExternalFilters` tegelijkertijd, moet de geklikte verbinding aanpassen `linkExternalFilters` **en** niet overeenkomen `linkInternalFilters` te worden beschouwd als een exitkoppeling. Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

## De verbindingen van de uitgang in SDK van het Web

Koppelingen worden automatisch gekwalificeerd als een afsluitkoppeling als het doeldomein van de koppeling afwijkt van het huidige `window.location.hostname`. De SDK van het Web biedt geen configuratievariabelen aan om automatische uitgangsverbindingsopsporing te wijzigen. Als u de domeinen moet aanpassen die als uitgangsverbinding kwalificeren, kunt u douanelogica in gebruiken `onBeforeEventSend` callback.

Zie [Automatisch koppelingen bijhouden](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html#automaticLinkTracking) in de documentatie van SDK van het Web voor meer informatie.

## Uitgaande koppelingen - Bijhouden met de Adobe Analytics-extensie

Het veld Track is een lijst met door komma&#39;s gescheiden filters (meestal domeinen) onder het palet [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Outbound Links - Track] veld.

Plaats filters die u altijd als extern wilt beschouwen in dit veld. Scheid meerdere domeinen met een komma zonder spatie.

## s.linkExternalFilters in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.linkExternalFilters` variabele is een tekenreeks met filters (zoals domeinen) die u kunt afsluiten. Scheid meerdere domeinen met een komma zonder spaties.

```js
s.linkExternalFilters = "example.com,example.net,example.org";
```

Neem het volgende implementatievoorbeeld alsof het actief is `adobe.com`:

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
