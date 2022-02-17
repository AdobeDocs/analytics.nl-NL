---
title: linkDownloadFileTypes
description: Bestandsextensies bepalen die automatisch worden bijgehouden als downloadkoppelingen.
feature: Variables
exl-id: 5089571a-d387-4ac7-838f-8bc95b2856fb
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# linkDownloadFileTypes

Wanneer [`trackDownloadLinks`](trackdownloadlinks.md) is ingeschakeld en een bezoeker op een koppeling klikt, controleert AppMeasurement de URL van de koppeling op bestandsextensies. Als de koppelings-URL een bestandstype bevat dat is gevonden in `linkDownloadFileTypes`wordt automatisch een aanvraag voor een downloadkoppelingsafbeelding verzonden.

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
>Voor deze downloadtypen kunt u handmatig de opdracht [`tl()`](../functions/tl-method.md) methode.

Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

## Extensies downloaden met tags in Adobe Experience Platform

Extensies downloaden is een lijst met bestandsextensies die een veld hebben om meer toe te voegen onder het tabblad [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Download Extensions] veld.

Bestandsextensies aan de lijst toevoegen door tekst in te voeren in het veld en te klikken [!UICONTROL Add]. Verwijder bestandsextensies uit de lijst door op het desbetreffende X-pictogram te klikken.

## s.linkDownloadFileTypes in AppMeasurement en een aangepaste code-editor

De `s.linkDownloadFileTypes` variabele is een tekenreeks met door komma&#39;s gescheiden bestandsextensies. Gebruik geen spaties.

Als deze variabele niet is gedefinieerd, werkt het automatisch bijhouden van downloadkoppelingen niet (zelfs als [`trackDownloadLinks`](trackdownloadlinks.md) is `true`).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
