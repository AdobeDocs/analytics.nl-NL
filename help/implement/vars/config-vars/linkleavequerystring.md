---
title: linkLeaveQueryString
description: Staat het behoud van vraagkoorden in verbinding het volgen dimensies toe.
translation-type: tm+mt
source-git-commit: e500332fe16887fa004858b07b59644837e183aa

---


# linkLeaveQueryString

AppMeasurement strips vraagt tekenreeksen van verbinding het volgen URLs door gebrek. Gebruik de variabele linkLeaveQueryString om vraagkoorden in verbinding het volgen dimensies te bewaren.

Bij sommige afsluitkoppelingen en downloadkoppelingen kan het belangrijke gedeelte van de URL zich in de queryreeks bevinden. Een downloadkoppeling zoals `https://example.com/download.asp?filename=myfile.exe` bevat bijvoorbeeld belangrijke koppelingsgegevens in de queryreeks.

Als de informatie van het verbinden niet in URLs op uw plaats is, is het gebruiken van deze variabele niet noodzakelijk. Door querytekenreeksen te verwijderen uit URL&#39;s die koppelingen bijhouden, beperkt u het aantal unieke waarden dat de dimensie bevat.

Inschakelen is van toepassing `linkLeaveQueryString` op alle afmetingen voor het bijhouden van koppelingen (inclusief aangepaste koppelingen, afsluitkoppelingen en downloadkoppelingen).

> [!TIP] Deze variabele heeft geen invloed op afmetingen buiten het bijhouden van koppelingen. Het beïnvloedt slechts douaneverbindingen, uitgangsverbindingen, en downloadverbindingen.

## URL-parameters behouden in Adobe Experience Platform Launch

[!UICONTROL Keep URL Parameters] is een selectievakje onder de [!UICONTROL Link Tracking] accordeon wanneer u de extensie Adobe Analytics configureert.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Vouw de [!UICONTROL Link Tracking] accordeon uit, zodat het [!UICONTROL Keep URL Parameters] selectievakje zichtbaar wordt.

Schakel dit vakje in als u querytekenreeksen wilt opnemen in de afmetingen voor het bijhouden van koppelingen.

## s.linkLeaveQueryString in de aangepaste code-editor van AppMeasurement en Launch

De `s.linkLeaveQueryString` variabele is een booleaanse waarde. De standaardwaarde is `false`.

* Als deze variabele is ingesteld op `true`, blijven querytekenreeksen behouden in URL&#39;s voor het bijhouden van koppelingen.
* Als deze variabele is ingesteld op `false` of niet is gedefinieerd, worden querytekenreeksen verwijderd van URL&#39;s voor het bijhouden van koppelingen.

```js
s.linkLeaveQueryString = true;
```

## Voorbeeld

Wees voorzichtig wanneer u deze variabele instelt op true, aangezien dit invloed kan hebben op koppelingsvolgfilters zoals `linkInternalFilters`, `linkExternalFilters`en `linkDownloadFiletypes`.

Bekijk het volgende voorbeeld alsof het op `adobe.com`:

```html
<script>
  s.linkInternalFilters = "adobe.com";
  s.linkLeaveQueryString = true;
</script>

<!--This link is not an exit link because the internal filter matches part of the query string -->
<a href = "example.com?r=adobe.com">Example link</a>
```
