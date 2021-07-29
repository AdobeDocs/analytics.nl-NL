---
title: linkExternalFilters
description: Gebruik de variabele linkExternalFilters om het automatisch volgen van de afsluitverbinding te helpen.
exl-id: 7d4e8d96-17ee-4a04-9a57-37d2056ee9a7
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# linkExternalFilters

AppMeasurement biedt de capaciteit om verbindingen automatisch te volgen die buiten uw plaats richten. Als [`trackExternalLinks`](trackexternallinks.md) is ingeschakeld, wordt een verzoek om een afbeelding naar de rechterkant van de Adobe verzonden wanneer een bezoeker op een koppeling klikt om uw site te verlaten. De variabelen `linkExternalFilters` en [`linkInternalFilters`](linkinternalfilters.md) bepalen welke verbindingen als intern/extern worden beschouwd.

Als deze variabele een waarde bevat, gedraagt het automatisch volgen van de uitgangsverbinding zich als een lijst van gewenste personen. Als een verbindingsklik geen `linkExternalFilters` waarden aanpast, wordt het niet beschouwd als een uitgangsverbinding. De volledige URL wordt op basis van deze variabele gecontroleerd. Als [`linkLeaveQueryString`](linkleavequerystring.md) wordt toegelaten, wordt het vraagkoord ook onderzocht.

>[!TIP]
>
>Gebruik deze variabele alleen als u precies weet welke domeinen u als exit-koppelingen wilt beschouwen. Vele organisaties vinden dat het gebruiken van `linkInternalFilters` voldoende voor hun behoeften van het uitgangsverbinding volgen is, en gebruiken `linkExternalFilters` niet.

Als u zowel `linkInternalFilters` als `linkExternalFilters` gelijktijdig gebruikt, moet de aangeklikte verbinding `linkExternalFilters` **en** niet `linkInternalFilters` aanpassen om als uitgangsverbinding te worden beschouwd. Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

## Uitgaande koppelingen - Bijhouden met tags in Adobe Experience Platform

Het gebied van het Spoor is een komma-gescheiden lijst van filters (gewoonlijk domeinen) onder [!UICONTROL Link Tracking] accordion wanneer het vormen van de uitbreiding van Adobe Analytics.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Link Tracking] uit, zodat het veld [!UICONTROL Outbound Links - Track] zichtbaar wordt.

Plaats filters die u altijd als extern wilt beschouwen in dit veld. Scheid meerdere domeinen met een komma zonder spatie.

## s.linkExternalFilters in AppMeasurement en aangepaste code-editor

De variabele `s.linkExternalFilters` is een tekenreeks met filters (zoals domeinen) die u kunt gebruiken om koppelingen af te sluiten. Scheid meerdere domeinen met een komma zonder spaties.

```js
s.linkExternalFilters = "example.com,example.net,example.org";
```

Bekijk het volgende implementatievoorbeeld alsof het zich op `adobe.com` bevond:

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
