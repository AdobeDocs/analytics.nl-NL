---
title: addProductEvar
description: Voegt merchandising Vars aan de productvariabele toe.
feature: Variables
exl-id: 6be94a15-78c9-4cbc-8b33-4a16f1b73b96
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# Adobe-plug-in: addProductEvar

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `addProductEvar` Met de plug-in kunt u eenvoudig een Adobe Analytics-eVar voor het verhandelen van producten toevoegen die productsyntaxis gebruikt voor de productvariabele zonder dat u zich zorgen hoeft te maken of de bestaande inhoud van de productvariabele wordt gewijzigd/verplaatst/verwijderd. Adobe raadt u aan deze plug-in te gebruiken als u eenvoudig handelsversies van productsyntaxis wilt toevoegen aan de [`products`](../page-vars/products.md) variabele. U hoeft de `addProductEvar` insteekmodule als u geen elektronische handelsversies met productsyntaxis gebruikt.

>[!NOTE]
>
>Deze plug-in vervangt eVars die al in een product voorkomen niet. Er worden alleen waarden toegevoegd die u instelt met deze insteekmodule. Wees voorzichtig bij het toevoegen van eVars die al voor dat product bestaan.

## Plug-in installeren met tags in Adobe Experience Platform

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer en publiceer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: AddProductEvar initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Installeer de plug-in met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adobe doen met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: addProductEvar v2.0 */
function addProductEvar(en,ev,ap){var e=en,f=ev,d=ap;if("-v"===e)return{plugin:"addProductEvar",version:"2.0"};a:{if("undefined"!==typeof window.s_c_il){var b=0;for(var c;b<window.s_c_il.length;b++)if(c=window.s_c_il[b],c._c&&"s_c"===c._c){b=c;break a}}b=void 0}if("undefined"!==typeof b&&(b.contextData.addProductEvar="2.0","string"===typeof e&&"string"===typeof f&&""!==f))if(d=d||!1,b.products){c=b.products.split(",");var g=c.length;d=d?0:g-1;for(var a;d<g;d++)a=c[d].split(";"),a[5]&&-1<a[5].toLowerCase().indexOf("evar")?a[5]=a[5]+"|"+e+"="+f:a[5]?a[5]=e+"="+f:a[5]||(a[4]||(a[4]=""),a[3]||(a[3]=""),a[2]||(a[2]=""),a[1]||(a[1]=""),a[5]=e+"="+f),c[d]=a.join(";");b.products=c.join(",")}else b.products=";;;;;"+e+"="+f};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `addProductEvar` de plug-in gebruikt de volgende argumenten:

* **`en`** (vereist, tekenreeks): De eVar die moet worden toegevoegd aan de laatste vermelding die momenteel in de productvariabele is opgenomen. Als de productvariabele leeg is, maakt de plug-in een &quot;leeg&quot; product-item met de waarde eVar aan het einde van de vermelding.
* **`ev`** (vereist, tekenreeks): De waarde die aan de eVar is toegewezen.
* **`ap`** (optioneel, Booleaans): Als de productvariabele momenteel meer dan één productitem bevat, voegt een waarde waar (of 1) de eVar toe aan **alles** de productgegevens.  De standaardwaarde is false (of 0), waardoor de eVar alleen wordt toegevoegd aan de eigenschap **last** de vermelding in de productvariabele.

De `addProductEvar` retourneert niets. In plaats daarvan worden de eVar (en de waarde van de eVar) toegevoegd die zijn opgegeven in het dialoogvenster `en` en `ev` voor de `products` variabele.

## Voorbeelden

```js
// Set a merchandising eVar to blue on the last product. The output for the products variable is ";product1;3;300,;product2;2;122,;product3;1;25;;eVar1=blue"
s.products=";product1;3;300,;product2;2;122,;product3;1;25";
addProductEvar("eVar1", "blue");

// Set a merchandising eVar to blue on all products. The output for the products variable is ";product1;3;300;;eVar1=blue,;product2;2;122;;eVar1=blue,;product3;1;25;;eVar1=blue"
s.products=";product1;3;300,;product2;2;122,;product3;1;25";
addProductEvar("eVar1", "blue", true);

// Set multiple merchandising eVars to the last product in the string. The output for the products variable is ";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue,;product2;2;122,;product3;1;25;;eVar23=medium|eVar24=women|eVar1=red"
s.products=";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue,;product2;2;122,;product3;1;25";
addProductEvar("eVar23", "medium");
addProductEvar("eVar24", "women");
addProductEvar("eVar1", "red");

// Set multiple merchandising eVars to all products in the string. The output for the products variable is ";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue|eVar23=medium|eVar24=women|eVar1=red,;product2;2;122;;eVar23=medium|eVar24=women|eVar1=red,;product3;1;25;;eVar23=medium|eVar24=women|eVar1=red"
s.products=";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue,;product2;2;122,;product3;1;25";
addProductEvar("eVar23", "medium", true);
addProductEvar("eVar24", "women", true);
addProductEvar("eVar1", "red", true);

// If the products variable is not set, the plug-in creates an empty product string correctly delimited to the merchandising eVar. The output for the products variable is ";;;;;eVar1=blue"
addProductEvar("eVar1", "blue");
```

## Versiehistorie

### 2.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 1.0 (7 oktober 2019)

* Eerste release.
