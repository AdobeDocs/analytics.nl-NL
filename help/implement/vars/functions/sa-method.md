---
title: sa
description: Wijzig de rapportsuite op elk gewenst moment in de implementatie.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# sa

Met de `sa()` methode kunt u een rapportsuite op elk gewenst moment op de pagina dynamisch wijzigen. Als u gegevens naar verschillende rapportreeksen wilt verzenden zonder dat de pagina opnieuw wordt geladen, kunt u deze methode gebruiken.

## De sa-methode gebruiken in Adobe Experience Platform Launch

Er is geen flexibele manier om rapportsuite in de interface te wijzigen. U kunt rapportsuite instellen onder de [!UICONTROL Library Management] accordeon wanneer u de extensie Adobe Analytics configureert. U kunt de rapportsuite echter niet wijzigen of bijwerken met regels. Als u de waarden van de rapportsuite wilt bijwerken nadat deze zijn ingesteld, gebruikt u de aangepaste code-editor volgens de syntaxis van AppMeasurement.

## s.sa() in de aangepaste code-editor van AppMeasurement en Launch

Roep de `s.sa()` methode aan om de reeks van het bestemmingsrapport te veranderen. Zijn enige argument is een koord dat een identiteitskaart van de rapportreeks, of veelvoudige rapportreeks IDs bevat die door een komma wordt afgebakend. Het argument van ID van de rapportsuite is vereist. Gebruik geen spaties in het tekenreeksargument.

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
