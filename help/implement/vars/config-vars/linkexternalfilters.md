---
title: linkExternalFilters
description: Gebruik de variabele linkExternalFilters om het automatisch volgen van de afsluitverbinding te helpen.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 1%

---


# linkExternalFilters

AppMeasurement biedt de capaciteit om verbindingen automatisch te volgen die buiten uw plaats richten. Als [`trackExternalLinks`](trackexternallinks.md) deze optie is ingeschakeld, wordt een verzoek om een afbeelding naar rechts verzonden wanneer een bezoeker op een koppeling klikt om uw site te verlaten. De `linkExternalFilters` en [`linkInternalFilters`](linkinternalfilters.md) variabelen bepalen welke verbindingen als intern/extern worden beschouwd.

Als deze variabele een waarde bevat, gedraagt het automatisch volgen van de uitgangsverbinding zich als een lijst van gewenste personen. Als een koppelingsklik niet aan om het even welke `linkExternalFilters` waarden aanpast, wordt het beschouwd als geen uitgangsverbinding. De volledige URL wordt op basis van deze variabele gecontroleerd. Als [`linkLeaveQueryString`](linkleavequerystring.md) wordt toegelaten, wordt het vraagkoord ook onderzocht.

>[!TIP]
>
>Gebruik deze variabele alleen als u precies weet welke domeinen u als exit-koppelingen wilt beschouwen. Veel organisaties vinden dat het gebruiken voldoende `linkInternalFilters` is voor hun behoeften voor het bijhouden van de exit-koppeling en gebruiken deze functie niet `linkExternalFilters`.

Als u zowel `linkInternalFilters` als `linkExternalFilters` gelijktijdig gebruikt, moet de geklikte verbinding aanpassen `linkExternalFilters` en niet aanpassen **** `linkInternalFilters` om als uitgangsverbinding te worden beschouwd. Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

## Uitgaande Verbindingen - Spoor in de Lancering van het Adobe Experience Platform

Het veld Track is een lijst met door komma&#39;s gescheiden filters (meestal domeinen) die tijdens het configureren van de Adobe Analytics-extensie onder de [!UICONTROL Link Tracking] accordeon valt.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL Link Tracking] [!UICONTROL Outbound Links - Track] veld onthult.

Plaats filters die u altijd als extern wilt beschouwen in dit veld. Scheid meerdere domeinen met een komma zonder spatie.

## s.linkExternalFilters in de aangepaste code-editor van AppMeasurement en Launch

De `s.linkExternalFilters` variabele is een tekenreeks met filters (zoals domeinen) die u als afsluitkoppelingen wilt gebruiken. Scheid meerdere domeinen met een komma zonder spaties.

```js
s.linkExternalFilters = "example.com,example.net,example.org";
```

Bekijk het volgende implementatievoorbeeld alsof dit is ingeschakeld `adobe.com`:

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
