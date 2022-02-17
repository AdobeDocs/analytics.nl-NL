---
title: sa
description: Wijzig de rapportsuite op elk gewenst moment in de implementatie.
feature: Variables
exl-id: 524857a7-c820-4985-86c7-fcf21a0809bd
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---

# sa

De `sa()` Met deze methode kunt u een rapportsuite op elk gewenst moment op de pagina dynamisch wijzigen. Als u gegevens naar verschillende rapportreeksen wilt verzenden zonder dat de pagina opnieuw wordt geladen, kunt u deze methode gebruiken.

## De methode sa gebruiken met tags in Adobe Experience Platform

Er is geen flexibele manier om rapportsuite in de interface te wijzigen. U kunt de rapportsuite instellen onder de [!UICONTROL Library Management] accordeon bij het configureren van de Adobe Analytics-extensie. U kunt de rapportsuite echter niet wijzigen of bijwerken met regels. Als u de waarden van de rapportsuite wilt bijwerken nadat deze zijn ingesteld, gebruikt u de aangepaste code-editor volgens de syntaxis van AppMeasurement.

## s.sa() in AppMeasurement en aangepaste code-editor

Roep de `s.sa()` methode om de reeks van het bestemmingsrapport te veranderen. Zijn enige argument is een koord dat een identiteitskaart van de rapportreeks, of veelvoudige rapportreeks IDs bevat die door een komma wordt afgebakend. Het argument van ID van de rapportsuite is vereist. Gebruik geen spaties in het tekenreeksargument.

```js
s.sa("examplersid");
```

## Voorbeeld

U kunt de rapportsuite wijzigen als de gebruiker een specifieke actie op uw site uitvoert.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// If the visitor plays a video, you can add a video report suite
s.sa("examplersid,videorsid");

// Then send an image request
s.t();
```
