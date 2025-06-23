---
title: linkLeaveQueryString
description: Staat het behoud van vraagkoorden in verbinding het volgen dimensies toe.
feature: Appmeasurement Implementation
exl-id: 266f7d9c-803d-4dbe-95a1-282230012878
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# linkLeaveQueryString

AppMeasurement verwijdert standaard querytekenreeksen van URL&#39;s die koppelingen bijhouden. Gebruik de variabele `linkLeaveQueryString` om querytekenreeksen te behouden in de afmetingen voor het bijhouden van koppelingen.

Bij sommige afsluitkoppelingen en downloadkoppelingen kan het belangrijke gedeelte van de URL zich in de queryreeks bevinden. Een downloadkoppeling zoals `https://example.com/download.asp?filename=myfile.exe` bevat bijvoorbeeld belangrijke koppelingsgegevens in de queryreeks.

Als de informatie van het verbinden niet in URLs op uw plaats is, is het gebruiken van deze variabele niet noodzakelijk. Door querytekenreeksen te verwijderen uit URL&#39;s die koppelingen bijhouden, beperkt u het aantal unieke waarden dat de dimensie bevat.

Als u `linkLeaveQueryString` inschakelt, geldt dit voor alle afmetingen voor het bijhouden van koppelingen (inclusief aangepaste koppelingen, afsluitkoppelingen en downloadkoppelingen).

>[!TIP]
>
>Deze variabele heeft geen invloed op afmetingen buiten het bijhouden van koppelingen. Het beïnvloedt slechts douaneverbindingen, uitgangsverbindingen, en downloadverbindingen.

## De koorden van de verbindingsvraag van de handvatverbinding gebruikend het Web SDK

Tekenreeksen voor query&#39;s worden niet uit het XDM-veld verwijderd `web.webInteraction.URL` . Als u querytekenreeksen uit dit XDM-veld wilt verwijderen, kunt u deze bewerken met `onBeforeEventSend` .

## URL-parameters behouden met de Adobe Analytics-extensie

[!UICONTROL Keep URL Parameters] is een selectievakje onder de accordeon van [!UICONTROL Link Tracking] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Link Tracking] uit, zodat het selectievakje [!UICONTROL Keep URL Parameters] zichtbaar wordt.

Schakel dit vakje in als u querytekenreeksen wilt opnemen in de afmetingen voor het bijhouden van koppelingen.

## s.linkLeaveQueryString in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.linkLeaveQueryString` is een booleaanse waarde. De standaardwaarde is `false` .

* Als deze variabele is ingesteld op `true` , blijven querytekenreeksen behouden in URL&#39;s voor het bijhouden van koppelingen.
* Als deze variabele is ingesteld op `false` of niet is gedefinieerd, worden querytekenreeksen verwijderd van URL&#39;s voor het bijhouden van koppelingen.

```js
s.linkLeaveQueryString = true;
```

## Voorbeeld

Wees voorzichtig wanneer u deze variabele instelt op true, aangezien dit invloed kan hebben op koppelingsvolgfilters zoals [`linkInternalFilters`](linkinternalfilters.md) , [`linkExternalFilters`](linkexternalfilters.md) en [`linkDownloadFiletypes`](linkdownloadfiletypes.md) .

Bekijk het volgende voorbeeld alsof het op `adobe.com` was:

```html
<script>
  s.linkInternalFilters = "adobe.com";
  s.linkLeaveQueryString = true;
</script>

<!--This link is not an exit link because the internal filter matches part of the query string -->
<a href = "example.com?r=adobe.com">Example link</a>
```
