---
title: sa
description: Wijzig de rapportsuite op elk gewenst moment in de implementatie.
feature: Appmeasurement Implementation
exl-id: 524857a7-c820-4985-86c7-fcf21a0809bd
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# sa

Met de methode `sa()` kunt u een rapportsuite op elk gewenst moment op de pagina dynamisch wijzigen. Als u gegevens naar verschillende rapportreeksen wilt verzenden zonder dat de pagina opnieuw wordt geladen, kunt u deze methode gebruiken.

## Het behandelen van rapportsuites die het Web SDK gebruiken

Web SDK werkt door gegevens naar een specifieke DataStream te verzenden, die gegevens naar de gewenste Analytics Report Suite(s) doorstuurt. Één enkele DataStream kan gegevens aan veelvoudige Reeksen van het Rapport door:sturen. Deze sectie is op zowel de uitbreiding van SDK van het Web als manueel het uitvoeren van het Web SDK van toepassing.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op **[!UICONTROL Datastreams]** aan de linkerkant.
1. Klik op de gewenste gegevensstroom of klik op **[!UICONTROL New Datastream]** .
1. Klik op **[!UICONTROL Add Service]** en selecteer vervolgens **[!UICONTROL Adobe Analytics]** .
1. Voer de gewenste rapportsuite-id in. Als u dezelfde gegevens naar meerdere rapportsets wilt verzenden, klikt u op **[!UICONTROL Add Report Suite]** .
1. Klik op **[!UICONTROL Save]** als alle gewenste rapportsuites zijn ingevoerd.

## De gewenste DataStream instellen met de extensie Web SDK

De uitbreiding van SDK van het Web verstrekt een drop-down lijst DataStream voor elke milieu. U kunt ook handmatig de DataStream-id invoeren.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder [!UICONTROL Adobe Experience Platform Web SDK] .
1. Kies onder [!UICONTROL Datastreams] de gewenste DataStream in de vervolgkeuzelijst voor elke omgeving.
1. Klik op **[!UICONTROL Save]**.

## Plaats manueel gewenste Datasstream die het Web SDK uitvoert

Stel de configuratievariabele `datastreamId` in op de DataStream-id. De DataStream-id bevindt zich aan de rechterkant wanneer u een DataStream bekijkt in de gegevensverzameling van Adobe Experience Platform.

```js
alloy("configure", {
  datastreamId: "example-a01f-4458-8cec-ef61de241c93",
  orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg"
});
```

Zie [ SDK van het Web ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=nl-NL) in de documentatie van SDK van het Web voor meer informatie vormen.

## Rapportsuite wijzigen met de Adobe Analytics-extensie

Er is geen flexibele manier om rapportsuite in de interface te wijzigen. U kunt rapportsuite instellen onder de accordeon [!UICONTROL Library Management] wanneer u de Adobe Analytics-extensie configureert. U kunt de rapportsuite echter niet wijzigen of bijwerken met regels. Als u de waarden van de rapportsuite wilt bijwerken nadat deze zijn ingesteld, gebruikt u de aangepaste code-editor volgens de syntaxis van AppMeasurement.

## s.sa() in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

Roep de methode `s.sa()` aan om de doelrapportsuite te wijzigen. Zijn enige argument is een koord dat een identiteitskaart van de rapportreeks, of veelvoudige rapportreeks IDs bevat die door een komma wordt afgebakend. Het argument van ID van de rapportsuite is vereist. Gebruik geen spaties in het argument string.

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
