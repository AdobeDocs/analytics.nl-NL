---
title: linkDownloadFileTypes
description: Bestandsextensies bepalen die automatisch worden bijgehouden als downloadkoppelingen.
translation-type: tm+mt
source-git-commit: 8f7baa770f800ffe800e760f1eca59911d3db348

---


# linkDownloadFileTypes

Wanneer `trackDownloadLinks` is ingesteld op `true` en een bezoeker op een koppeling klikt, controleert AppMeturement de URL van de koppeling op bestandstypeextensies. Als de koppeling-URL een bestandstype bevat dat is gevonden in `linkDownloadFileTypes`, wordt automatisch een aanvraag voor een downloadkoppeling naar een afbeelding verzonden.

Gebruik deze optie `linkDownloadFileTypes` om aan te passen welke bestandsextensies u wilt tellen als downloadkoppelingen.

> [!NOTE] Alleen de werkelijke klikken worden automatisch bijgehouden. De volgende typen koppelingen worden niet automatisch bijgehouden:
>
> * Het bestand wordt automatisch gedownload wanneer een pagina wordt geladen
> * Downloads die na een omleiding teweegbrengen
> * Klik met de rechtermuisknop en selecteer Doel opslaan als...
> * Koppelingen waarin JavaScript wordt gebruikt, zoals `javascript:openLink()`
>
> 
Voor deze downloadtypen kunt u de `tl()` functie handmatig aanroepen.

Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

## Extensies downloaden in Adobe Experience Platform Launch

Download Extensions is een lijst met bestandsextensies met een veld waarmee u onder de accordeon meer items kunt toevoegen wanneer u de extensie Adobe Analytics configureert. [!UICONTROL Link Tracking]

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL Link Tracking] [!UICONTROL Download Extensions] veld onthult.

Voeg bestandsextensies toe aan de lijst door tekst in te voeren in het veld en te klikken [!UICONTROL Add]. Verwijder bestandsextensies uit de lijst door op het desbetreffende X-pictogram te klikken.

## s.linkDownloadFileTypes in AppMeasurement en Launch, aangepaste code-editor

De `s.linkDownloadFileTypes` variabele is een tekenreeks met door komma&#39;s gescheiden bestandsextensies. Gebruik geen spaties.

Als deze variabele niet is gedefinieerd, werkt het automatisch bijhouden van downloadkoppelingen niet (zelfs als `trackDownloadLinks` dit `true`het geval is).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v"
```
