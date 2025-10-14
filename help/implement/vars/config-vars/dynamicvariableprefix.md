---
title: dynamicVariablePrefix
description: Hiermee kunt u de tekenreeks aanpassen die dynamische variabelen identificeert.
feature: Appmeasurement Implementation
exl-id: fe208723-0cf2-4899-be7a-8f23c6501c11
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# dynamicVariablePrefix

Dynamische variabelen zijn een kortstondig concept waarmee u waarden van de ene variabele naar de andere kunt kopiëren. Deze zijn nuttig voor lange variabelewaarden, omdat ze de URL-lengte van een afbeeldingsaanvraag verkorten. Zie [&#x200B; Dynamische variabelen &#x200B;](../page-vars/dynamic-variables.md) voor meer informatie over dit concept.

Dynamische variabelen gebruiken standaard het voorvoegsel `D=` . Met de variabele `dynamicVariablePrefix` kunt u de tekenreeks aanpassen die dynamische variabelen identificeert. Het is hoofdlettergevoelig.

## Dynamisch veranderlijke prefix die het Web SDK gebruikt

De SDK van het Web gebruikt geen dynamische veranderlijke het formatteren. In plaats daarvan kunt u DataStream-toewijzing gebruiken om meerdere doelvelden te vullen met één Source-veld. Zie [&#x200B; Dynamische variabelen die het Web SDK &#x200B;](../page-vars/dynamic-variables.md#dynamic-variables-using-the-web-sdk) voor meer informatie gebruiken.

Als u gegevens rechtstreeks naar Adobe Analytics verzendt zonder zich aan een schema te houden, gebruikt het de volgende variabele:

* [&#x200B; voorwerp van Gegevens &#x200B;](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.dynamicVariablePrefix`

## Dynamische variabele voorvoegsel met Adobe Analytics-extensie

Dynamic Variable Prefix is een veld onder de accordion [!UICONTROL Global Variables] bij het configureren van de Adobe Analytics-extensie.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Global Variables] uit, zodat het veld [!UICONTROL Dynamic Variable Prefix] zichtbaar wordt.

Dit veld bevat standaard `D=` . U kunt de waarde wijzigen als u een ander prefix voor een dynamische variabele wilt gebruiken. U kunt elke gewenste waarde gebruiken, mits deze overeenkomt met de tekencodering op uw site.

## s.dynamicVariablePrefix in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De variabele `s.dynamicVariablePrefix` is een tekenreeks die een reeks tekens kan bevatten. Als deze variabele niet is gedefinieerd, gebruikt AppMeasurement standaard de tekenreeks `D=` .

```js
// An example that changes the dynamic variable prefix
s.dynamicVariablePrefix="..";

// This eVar uses the above customized dynamic variable prefix to set eVar to page URL
s.eVar1="..g";
```
