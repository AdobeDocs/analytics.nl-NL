---
title: dynamicVariablePrefix
description: Hiermee kunt u de tekenreeks aanpassen die dynamische variabelen identificeert.
feature: Variables
exl-id: fe208723-0cf2-4899-be7a-8f23c6501c11
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# dynamicVariablePrefix

Dynamische variabelen zijn een kortstondig concept waarmee u waarden van de ene variabele naar de andere kunt kopiëren. Deze zijn nuttig voor lange variabelewaarden, omdat ze de URL-lengte van een afbeeldingsaanvraag verkorten. Zie [Dynamische variabelen](../page-vars/dynamic-variables.md) voor meer informatie over dit concept .

Dynamische variabelen gebruiken standaard het voorvoegsel `D=`. De `dynamicVariablePrefix` Met variabele kunt u de tekenreeks aanpassen die dynamische variabelen identificeert. Het is hoofdlettergevoelig.

## Dynamisch veranderlijke prefix die de SDK van het Web gebruikt

De SDK van het Web gebruikt geen dynamische variabele het formatteren. In plaats daarvan kunt u DataStream-toewijzing gebruiken om meerdere doelvelden te vullen met één bronveld. Zie [Dynamische variabelen met de Web SDK](../page-vars/dynamic-variables.md#dynamic-variables-using-the-web-sdk) voor meer informatie .

## Dynamisch variabele voorvoegsel met Adobe Analytics-extensie

Dynamisch veranderlijke Voorvoegsel is een gebied onder [!UICONTROL Global Variables] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Breid uit [!UICONTROL Global Variables] accordion, die de [!UICONTROL Dynamic Variable Prefix] veld.

Dit veld bevat `D=` standaard. U kunt de waarde wijzigen als u een ander prefix voor een dynamische variabele wilt gebruiken. U kunt elke gewenste waarde gebruiken, mits deze overeenkomt met de tekencodering op uw site.

## s.dynamicVariablePrefix in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.dynamicVariablePrefix` variabele is een tekenreeks die een reeks tekens kan bevatten. Als deze variabele niet is gedefinieerd, gebruikt AppMeasurement de tekenreeks `D=` standaard.

```js
// An example that changes the dynamic variable prefix
s.dynamicVariablePrefix="..";

// This eVar uses the above customized dynamic variable prefix to set eVar to page URL
s.eVar1="..g";
```
