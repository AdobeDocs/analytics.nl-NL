---
title: referrer
description: Overschrijf de automatisch verzamelde verwijzer voor een klap.
feature: Variables
exl-id: 09a76de9-0689-424a-aead-3fdff1709fd9
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# referentie

De `referrer` de variabele treedt automatisch verzamelde verwijzer in rapporten met voeten. Deze variabele is handig in situaties waarin de referentie verloren kan gaan, bijvoorbeeld tijdens omleidingen of het tijdelijk doorsturen van de bezoeker naar een betalingsverwerker. Met deze variabele kunt u de afmetingen &#39;Referrer&#39; en &#39;Refering Domain&#39; vullen.

## Referrer die SDK van het Web gebruikt

Referrer is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `web.webReferrer.URL`.

## Referrer die de extensie Adobe Analytics gebruikt

U kunt de verwijzer instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions]klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Referrer] sectie.

U kunt de verwijzing instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.reference in AppMeasurement en de de coderedacteur van de de uitbreiding van de Analyse van de douanecode

De `s.referrer` variabele is een tekenreeks die de URL van de vorige pagina bevat. Deze variabele kan maximaal 255 bytes opslaan; waarden die groter zijn dan 255 bytes, worden afgekapt. AppMeasurement stelt deze variabele automatisch in op `document.referrer`; U hoeft deze variabele niet in te stellen, tenzij u de automatisch verzamelde waarde wilt overschrijven.

```js
s.referrer = "https://example.com";
```

Als u de `digitalData` [gegevenslaag](../../prepare/data-layer.md):

```js
s.referrer = digitalData.page.pageInfo.referringURL;
```

>[!CAUTION]
>
>Stel deze variabele niet in op niet-URL-waarden. Verwijder het URL-protocol niet.

## Voorbeeld

Veel organisaties werken met implementaties rond omleidingen. U kunt de [`Util.getQueryParam()`](../functions/util-getqueryparam.md) gebruiken om de referentie via de URL op te halen als uw site dit toestaat. Zorg ervoor dat u URL codeert om het even welke waarden inbegrepen in het vraagkoord.

```js
// Example if the URL is https://example.com?r=https%3A%2F%2Fexample.org
s.referrer = s.Util.getQueryParam("r");
```
