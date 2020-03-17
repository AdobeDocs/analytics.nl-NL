---
title: dynamicVariablePrefix
description: Hiermee kunt u de tekenreeks aanpassen die dynamische variabelen identificeert.
translation-type: tm+mt
source-git-commit: ''

---


# dynamicVariablePrefix

Dynamische variabelen zijn een kortstondig concept waarmee u waarden van de ene variabele naar de andere kunt kopiëren. Deze zijn nuttig voor lange variabelewaarden, omdat ze de URL-lengte van een afbeeldingsaanvraag verkorten. Zie [Dynamische variabelen](../page-vars/dynamic-variables.md) voor meer informatie over dit concept.

Dynamische variabelen gebruiken standaard het voorvoegsel `D=`. Met de `dynamicVariablePrefix` variabele kunt u de tekenreeks aanpassen die dynamische variabelen identificeert. Het is hoofdlettergevoelig.

## Dynamische variabele voorvoegsel in Adobe Experience Platform Starten

Dynamic Variable Prefix is een veld onder de [!UICONTROL Global Variables] accordeon tijdens het configureren van de extensie Adobe Analytics.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL Global Variables] [!UICONTROL Dynamic Variable Prefix] veld onthult.

Dit veld bevat `D=` standaard. U kunt de waarde wijzigen als u een ander prefix voor een dynamische variabele wilt gebruiken. U kunt elke gewenste waarde gebruiken, mits deze overeenkomt met de tekencodering op uw site.

## s.dynamicVariablePrefix in AppMeasurement en Launch, aangepaste code-editor

De `s.dynamicVariablePrefix` variabele is een tekenreeks die een reeks tekens kan bevatten. Als deze variabele niet wordt bepaald, gebruikt AppMeasurement het koord `D=` door gebrek.

```js
// An example that changes the dynamic variable prefix
s.dynamicVariablePrefix="..";

// This eVar uses the above customized dynamic variable prefix to set eVar to page URL
s.eVar1="..g";
```
