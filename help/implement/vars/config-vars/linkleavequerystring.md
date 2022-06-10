---
title: linkLeaveQueryString
description: Staat het behoud van vraagkoorden in verbinding het volgen dimensies toe.
feature: Variables
exl-id: 266f7d9c-803d-4dbe-95a1-282230012878
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# linkLeaveQueryString

AppMeasurement strips vraagt tekenreeksen van verbinding het volgen URLs door gebrek. Gebruik de `linkLeaveQueryString` variabele om vraagkoorden in verbinding het volgen dimensies te bewaren.

Bij sommige afsluitkoppelingen en downloadkoppelingen kan het belangrijke gedeelte van de URL zich in de queryreeks bevinden. Bijvoorbeeld een downloadkoppeling, zoals `https://example.com/download.asp?filename=myfile.exe` bevat belangrijke koppelingsinformatie in het vraagkoord.

Als de informatie van het verbinden niet in URLs op uw plaats is, is het gebruiken van deze variabele niet noodzakelijk. Door querytekenreeksen te verwijderen uit URL&#39;s die koppelingen bijhouden, beperkt u het aantal unieke waarden dat de dimensie bevat.

Inschakelen `linkLeaveQueryString` is van toepassing op alle afmetingen voor het bijhouden van koppelingen (inclusief aangepaste koppelingen, afsluitkoppelingen en downloadkoppelingen).

>[!TIP]
>
>Deze variabele heeft geen invloed op afmetingen buiten het bijhouden van koppelingen. Het beïnvloedt slechts douaneverbindingen, uitgangsverbindingen, en downloadverbindingen.

## De koorden van de verbindingsvraag van de handvatverbinding gebruikend Web SDK

Tekenreeksen voor query&#39;s worden niet uit het XDM-veld verwijderd `web.webInteraction.URL`. Als u querytekenreeksen uit dit XDM-veld wilt verwijderen, kunt u deze bewerken met `onBeforeEventSend`.

## URL-parameters behouden met de Adobe Analytics-extensie

[!UICONTROL Keep URL Parameters] is een selectievakje onder [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Keep URL Parameters] selectievakje.

Schakel dit vakje in als u querytekenreeksen wilt opnemen in de afmetingen voor het bijhouden van koppelingen.

## s.linkLeaveQueryString in AppMeasurement en de aangepaste code-editor van de extensie Analytics

De `s.linkLeaveQueryString` variable is a boolean. De standaardwaarde is `false`.

* Als deze variabele is ingesteld op `true`, querytekenreeksen blijven behouden in URL&#39;s voor het bijhouden van koppelingen.
* Als deze variabele is ingesteld op `false` of niet gedefinieerd, querytekenreeksen worden verwijderd van URL&#39;s voor het bijhouden van koppelingen.

```js
s.linkLeaveQueryString = true;
```

## Voorbeeld

Wees voorzichtig wanneer u deze variabele instelt op true, aangezien dit invloed kan hebben op koppelingsvolgfilters, zoals [`linkInternalFilters`](linkinternalfilters.md), [`linkExternalFilters`](linkexternalfilters.md), en [`linkDownloadFiletypes`](linkdownloadfiletypes.md).

Bekijk het volgende voorbeeld alsof het was `adobe.com`:

```html
<script>
  s.linkInternalFilters = "adobe.com";
  s.linkLeaveQueryString = true;
</script>

<!--This link is not an exit link because the internal filter matches part of the query string -->
<a href = "example.com?r=adobe.com">Example link</a>
```
