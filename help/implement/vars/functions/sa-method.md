---
title: sa
description: Wijzig de rapportsuite op elk gewenst moment in de implementatie.
feature: Variables
exl-id: 524857a7-c820-4985-86c7-fcf21a0809bd
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# sa

De `sa()` Met deze methode kunt u een rapportsuite op elk gewenst moment op de pagina dynamisch wijzigen. Als u gegevens naar verschillende rapportreeksen wilt verzenden zonder dat de pagina opnieuw wordt geladen, kunt u deze methode gebruiken.

## Het behandelen van rapportsuites die SDK van het Web gebruiken

De SDK van het Web werkt door gegevens naar een specifieke DataStream te verzenden, die gegevens naar de gewenste Analytics Report Suite(s) door:sturen. Één enkele DataStream kan gegevens aan veelvoudige Reeksen van het Rapport door:sturen. Deze sectie is op zowel de uitbreiding van SDK van het Web als manueel het uitvoeren van SDK van het Web van toepassing.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klikken **[!UICONTROL Datastreams]** links.
1. Klik op de gewenste gegevensstroom of klik op **[!UICONTROL New Datastream]**.
1. Klikken **[!UICONTROL Add Service]** selecteert u vervolgens **[!UICONTROL Adobe Analytics]**.
1. Voer de gewenste rapportsuite-id in. Als u dezelfde gegevens naar meerdere rapportsets wilt verzenden, klikt u op **[!UICONTROL Add Report Suite]**.
1. Zodra alle gewenste rapportsuites zijn ingegaan, klik **[!UICONTROL Save]**.

## Stel de gewenste gegevensstroom in met de extensie Web SDK

De uitbreiding van SDK van het Web verstrekt een drop-down lijst DataStream voor elk milieu. U kunt ook handmatig de DataStream-id invoeren.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Onder [!UICONTROL Datastreams]kiest u de gewenste gegevensstroom in de vervolgkeuzelijst voor elke omgeving.
1. Klik op **[!UICONTROL Save]**.

## Plaats manueel gewenste Datasstream die SDK van het Web uitvoert

Stel de `edgeConfigId` configuratievariabele aan identiteitskaart DataStream De DataStream-id bevindt zich aan de rechterkant wanneer u een DataStream bekijkt in de gegevensverzameling van Adobe Experience Platform.

```js
alloy("configure", {
  "edgeConfigId": "example-a01f-4458-8cec-ef61de241c93",
});
```

Zie [De SDK van het web configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) in de documentatie van SDK van het Web voor meer informatie.

## Rapportsuite wijzigen met de Adobe Analytics-extensie

Er is geen flexibele manier om rapportsuite in de interface te wijzigen. U kunt de rapportsuite instellen onder de [!UICONTROL Library Management] accordeon bij het configureren van de Adobe Analytics-extensie. U kunt de rapportsuite echter niet wijzigen of bijwerken met regels. Als u de waarden van de rapportsuite wilt bijwerken nadat deze zijn ingesteld, gebruikt u de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.sa() in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

Roep de `s.sa()` methode om de reeks van het bestemmingsrapport te veranderen. Zijn enige argument is een koord dat een identiteitskaart van de rapportreeks, of veelvoudige rapportreeks IDs bevat die door een komma wordt afgebakend. Het argument van ID van de rapportsuite is vereist. Gebruik geen spaties in het argument string.

```js
s.sa("examplersid");
```

U kunt bijvoorbeeld de rapportsuite wijzigen als de gebruiker een specifieke actie op uw site uitvoert.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// If the visitor plays a video, you can add a video report suite
s.sa("examplersid,videorsid");

// Then send an image request
s.t();
```
