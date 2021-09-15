---
title: linkDownloadFileTypes
description: Bestandsextensies bepalen die automatisch worden bijgehouden als downloadkoppelingen.
exl-id: 5089571a-d387-4ac7-838f-8bc95b2856fb
source-git-commit: 49bf0a459a096e011ff60724aa5bee4fb7721a21
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# linkDownloadFileTypes

Wanneer [`trackDownloadLinks`](trackdownloadlinks.md) wordt toegelaten en een bezoeker op een verbinding klikt, controleert AppMeturement URL van de verbinding voor filetype uitbreidingen. Als de koppelings-URL een bestandstype bevat dat wordt gevonden in `linkDownloadFileTypes`, wordt automatisch een aanvraag voor een downloadkoppelingsafbeelding verzonden.

Gebruik `linkDownloadFileTypes` om aan te passen welke dossieruitbreidingen u als downloadverbindingen wilt tellen.

>[!NOTE]
>
>Alleen de werkelijke klikken worden automatisch bijgehouden. De volgende typen koppelingen worden niet automatisch bijgehouden:
>
>* Het bestand wordt automatisch gedownload wanneer een pagina wordt geladen
>* Downloads die na een omleiding teweegbrengen
>* Klik met de rechtermuisknop en selecteer Doel opslaan als...
>* Koppelingen die JavaScript gebruiken, zoals `javascript:openLink()`

>
>Voor deze downloadtypes, kunt u [`tl()`](../functions/tl-method.md) methode manueel roepen.

Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

## Extensies downloaden met tags in Adobe Experience Platform

Download Extensions is een lijst met bestandsextensies met een veld waarmee u onder de accordeon [!UICONTROL Link Tracking] meer items kunt toevoegen wanneer u de Adobe Analytics-extensie configureert.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Link Tracking] uit, zodat het veld [!UICONTROL Download Extensions] zichtbaar wordt.

Voeg bestandsextensies toe aan de lijst door tekst in te voeren in het veld en te klikken op [!UICONTROL Add]. Verwijder bestandsextensies uit de lijst door op het desbetreffende X-pictogram te klikken.

## s.linkDownloadFileTypes in AppMeasurement en een aangepaste code-editor

De variabele `s.linkDownloadFileTypes` is een tekenreeks met door komma&#39;s gescheiden bestandsextensies. Gebruik geen spaties.

Als deze variabele niet is gedefinieerd, werkt het automatisch bijhouden van downloadkoppelingen niet (zelfs als [`trackDownloadLinks`](trackdownloadlinks.md) `true` is).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
