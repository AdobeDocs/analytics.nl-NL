---
title: dynamicVariablePrefix
description: Hiermee kunt u de tekenreeks aanpassen die dynamische variabelen identificeert.
exl-id: fe208723-0cf2-4899-be7a-8f23c6501c11
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# dynamicVariablePrefix

Dynamische variabelen zijn een kortstondig concept waarmee u waarden van de ene variabele naar de andere kunt kopiëren. Deze zijn nuttig voor lange variabelewaarden, omdat ze de URL-lengte van een afbeeldingsaanvraag verkorten. Zie [Dynamische variabelen](../page-vars/dynamic-variables.md) voor meer informatie over dit concept.

Dynamische variabelen gebruiken standaard het voorvoegsel `D=`. Met de variabele `dynamicVariablePrefix` kunt u de tekenreeks aanpassen die dynamische variabelen identificeert. Het is hoofdlettergevoelig.

## Dynamisch voorvoegsel van variabele met tags in Adobe Experience Platform

Dynamisch veranderlijk Voorvoegsel is een gebied onder [!UICONTROL Global Variables] accordion wanneer het vormen van de uitbreiding van Adobe Analytics.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Global Variables] uit, zodat het veld [!UICONTROL Dynamic Variable Prefix] zichtbaar wordt.

Dit veld bevat standaard `D=`. U kunt de waarde wijzigen als u een ander prefix voor een dynamische variabele wilt gebruiken. U kunt elke gewenste waarde gebruiken, mits deze overeenkomt met de tekencodering op uw site.

## s.dynamicVariablePrefix in AppMeasurement en de aangepaste code-editor

De variabele `s.dynamicVariablePrefix` is een tekenreeks die een reeks tekens kan bevatten. Als deze variabele niet wordt bepaald, gebruikt AppMeasurement het koord `D=` door gebrek.

```js
// An example that changes the dynamic variable prefix
s.dynamicVariablePrefix="..";

// This eVar uses the above customized dynamic variable prefix to set eVar to page URL
s.eVar1="..g";
```
