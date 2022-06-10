---
title: linkDownloadFileTypes
description: Bestandsextensies bepalen die automatisch worden bijgehouden als downloadkoppelingen.
feature: Variables
exl-id: 5089571a-d387-4ac7-838f-8bc95b2856fb
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# linkDownloadFileTypes

Wanneer [`trackDownloadLinks`](trackdownloadlinks.md) (AppMeasurement) of [`clickCollectionEnabled`](trackdownloadlinks.md) (Web SDK) is ingeschakeld en een bezoeker klikt op een koppeling, controleert AppMeturement de URL van de koppeling op bestandstypeextensies. Als de koppeling-URL een bijbehorend bestandstype bevat, wordt automatisch een aanvraag voor een downloadkoppeling naar de afbeelding verzonden.

Gebruiken `linkDownloadFileTypes` om aan te passen welke bestandsextensies u wilt tellen als downloadkoppelingen.

>[!NOTE]
>
>Alleen de werkelijke klikken worden automatisch bijgehouden. De volgende typen koppelingen worden niet automatisch bijgehouden:
>
>* Het bestand wordt automatisch gedownload wanneer een pagina wordt geladen
>* Downloads die na een omleiding teweegbrengen
>* Klik met de rechtermuisknop en selecteer Doel opslaan als...
>* Koppelingen waarin JavaScript wordt gebruikt, zoals `javascript:openLink()`
>
>Voor deze downloadtypen kunt u handmatig een [`link tracking`](../functions/tl-method.md) vraag.

Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

## Koppelingskwalificatie downloaden met de Web SDK-extensie

De [!UICONTROL Download link qualifier] in het tekstveld wordt regex gebruikt om te bepalen of een geklikte koppeling een downloadkoppeling kan zijn.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Onder [!UICONTROL Data Collection], stelt u de gewenste waarde in in het dialoogvenster **[!UICONTROL Download link qualifier]** tekstveld.

## Koppelingskwalificatie handmatig downloaden met implementatie van de Web SDK

[Configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) de SDK met [`downloadLinkQualifier`](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html#automaticLinkTracking). Het veld gebruikt regex op de aangeklikte URL om te bepalen of het een geldige downloadkoppeling is. Indien `downloadLinkQualifier` is niet gedefinieerd, wordt de standaardwaarde ingesteld op `\\.(exe|zip|wav|mp3|mov|mpg|avi|wmv|pdf|doc|docx|xls|xlsx|ppt|pptx)$`.

```json
alloy("configure", {
  "downloadLinkQualifier": "\\.(exe|zip|wav|mp3|mov|mpg|avi|wmv|pdf|doc|docx|xls|xlsx|ppt|pptx)$"
});
```

## Extensies downloaden met de Adobe Analytics-extensie

Extensies downloaden is een lijst met bestandsextensies die een veld hebben om meer toe te voegen onder het tabblad [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de **[!UICONTROL Download Extensions]** veld.

Bestandsextensies aan de lijst toevoegen door tekst in te voeren in het veld en te klikken **[!UICONTROL Add]**. Bestandsextensies uit de lijst verwijderen door op de respectievelijke extensies te klikken **&#39;X&#39;** pictogram.

## s.linkDownloadFileTypes in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.linkDownloadFileTypes` variabele is een tekenreeks met door komma&#39;s gescheiden bestandsextensies. Gebruik geen spaties.

Als deze variabele niet is gedefinieerd, werkt het automatisch bijhouden van downloadkoppelingen niet (zelfs als [`trackDownloadLinks`](trackdownloadlinks.md) is `true`).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
