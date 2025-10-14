---
title: linkDownloadFileTypes
description: Bestandsextensies bepalen die automatisch worden bijgehouden als downloadkoppelingen.
feature: Appmeasurement Implementation
exl-id: 5089571a-d387-4ac7-838f-8bc95b2856fb
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# linkDownloadFileTypes

Wanneer [`trackDownloadLinks`](trackdownloadlinks.md) (AppMeasurement) of [`clickCollectionEnabled`](trackdownloadlinks.md) (Web SDK) is ingeschakeld en een bezoeker op een koppeling klikt, controleert AppMeasurement de URL van de koppeling op bestandsextensies. Als de koppeling-URL een bijbehorend bestandstype bevat, wordt automatisch een aanvraag voor een downloadkoppeling naar de afbeelding verzonden.

Gebruik `linkDownloadFileTypes` om aan te passen welke bestandsextensies u wilt tellen als downloadkoppelingen.

>[!NOTE]
>
>Alleen de werkelijke klikken worden automatisch bijgehouden. De volgende typen koppelingen worden niet automatisch bijgehouden:
>
>* Het bestand wordt automatisch gedownload wanneer een pagina wordt geladen
>* Downloads die na een omleiding teweegbrengen
>* Klik met de rechtermuisknop en selecteer Doel opslaan als...
>* Koppelingen met JavaScript, zoals `javascript:openLink()`
>
>Voor deze downloadtypen kunt u handmatig een [`link tracking`](../functions/tl-method.md) -aanroep verzenden.

Als een geklikte koppeling overeenkomt met zowel de afsluitings- als de downloadkoppelingscriteria, heeft het type downloadkoppeling prioriteit.

## Koppelingskwalificatie downloaden met de Web SDK-extensie

Het tekstveld [!UICONTROL Download link qualifier] gebruikt regex om te bepalen of een geklikte koppeling in aanmerking komt als een downloadkoppeling.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder [!UICONTROL Adobe Experience Platform Web SDK] .
1. Stel onder [!UICONTROL Data Collection] de gewenste waarde in het tekstveld **[!UICONTROL Download link qualifier]** in.

## Koppelingskwalificatie handmatig downloaden met implementatie van de Web SDK

[&#x200B; vorm &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=nl-NL) SDK gebruikend [`downloadLinkQualifier` &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html?lang=nl-NL#automaticLinkTracking). Het veld gebruikt regex op de aangeklikte URL om te bepalen of het een geldige downloadkoppeling is. Wanneer `downloadLinkQualifier` niet is gedefinieerd, wordt de standaardwaarde ingesteld op `\\.(exe|zip|wav|mp3|mov|mpg|avi|wmv|pdf|doc|docx|xls|xlsx|ppt|pptx)$` .

```json
alloy("configure", {
  "downloadLinkQualifier": "\\.(exe|zip|wav|mp3|mov|mpg|avi|wmv|pdf|doc|docx|xls|xlsx|ppt|pptx)$"
});
```

## Extensies downloaden met de Adobe Analytics-extensie

Download Extensions is een lijst met bestandsextensies met een veld waarmee u onder de accordeon [!UICONTROL Link Tracking] meer kunt toevoegen wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Link Tracking] uit, zodat het veld **[!UICONTROL Download Extensions]** zichtbaar wordt.

Voeg bestandsextensies toe aan de lijst door tekst in te voeren in het veld en op **[!UICONTROL Add]** te klikken. Verwijder dossieruitbreidingen uit de lijst door hun respectieve **&quot;X&quot;te klikken** pictogram.

## s.linkDownloadFileTypes in AppMeasurement en de de uitbreiding van de Analyse douane code redacteur

De variabele `s.linkDownloadFileTypes` is een tekenreeks met door komma&#39;s gescheiden bestandsextensies. Gebruik geen spaties.

Als deze variabele niet is gedefinieerd, werkt het automatisch bijhouden van downloadkoppelingen niet (zelfs als [`trackDownloadLinks`](trackdownloadlinks.md) `true` is).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
