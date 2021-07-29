---
title: linkLeaveQueryString
description: Staat het behoud van vraagkoorden in verbinding het volgen dimensies toe.
exl-id: 266f7d9c-803d-4dbe-95a1-282230012878
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# linkLeaveQueryString

AppMeasurement strips vraagt tekenreeksen van verbinding het volgen URLs door gebrek. Gebruik de `linkLeaveQueryString` variabele om vraagkoorden in verbinding het volgen dimensies te bewaren.

Bij sommige afsluitkoppelingen en downloadkoppelingen kan het belangrijke gedeelte van de URL zich in de queryreeks bevinden. Bijvoorbeeld, bevat een downloadverbinding zoals `https://example.com/download.asp?filename=myfile.exe` belangrijke verbindingsinformatie in het vraagkoord.

Als de informatie van het verbinden niet in URLs op uw plaats is, is het gebruiken van deze variabele niet noodzakelijk. Door querytekenreeksen te verwijderen uit URL&#39;s die koppelingen bijhouden, beperkt u het aantal unieke waarden dat de dimensie bevat.

Als u `linkLeaveQueryString` inschakelt, worden alle dimensies voor het bijhouden van koppelingen toegepast (inclusief aangepaste koppelingen, afsluitkoppelingen en downloadkoppelingen).

>[!TIP]
>
>Deze variabele heeft geen invloed op afmetingen buiten het bijhouden van koppelingen. Het beïnvloedt slechts douaneverbindingen, uitgangsverbindingen, en downloadverbindingen.

## URL-parameters behouden met tags in Adobe Experience Platform

[!UICONTROL Keep URL Parameters] is een selectievakje onder de  [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Breid [!UICONTROL Link Tracking] accordeon uit, die [!UICONTROL Keep URL Parameters] checkbox openbaart.

Schakel dit vakje in als u querytekenreeksen wilt opnemen in de afmetingen voor het bijhouden van koppelingen.

## s.linkLeaveQueryString in AppMeasurement en aangepaste code-editor

De variabele `s.linkLeaveQueryString` is een booleaanse waarde. De standaardwaarde is `false`.

* Als deze variabele wordt geplaatst aan `true`, vraagkoorden in verbinding het volgen URLs worden bewaard.
* Als deze variabele wordt geplaatst aan `false` of niet bepaald, worden de vraagkoorden gestript van verbinding het volgen URLs.

```js
s.linkLeaveQueryString = true;
```

## Voorbeeld

Wees voorzichtig wanneer het plaatsen van deze variabele aan waar, aangezien het verbindingsvolgende filters zoals [`linkInternalFilters`](linkinternalfilters.md), [`linkExternalFilters`](linkexternalfilters.md), en [`linkDownloadFiletypes`](linkdownloadfiletypes.md) kan beïnvloeden.

Bekijk het volgende voorbeeld alsof het op `adobe.com` was:

```html
<script>
  s.linkInternalFilters = "adobe.com";
  s.linkLeaveQueryString = true;
</script>

<!--This link is not an exit link because the internal filter matches part of the query string -->
<a href = "example.com?r=adobe.com">Example link</a>
```
