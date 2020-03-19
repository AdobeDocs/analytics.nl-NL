---
title: referentie
description: Overschrijf de automatisch verzamelde verwijzer voor een klap.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# referentie

De `referrer` variabele negeert de automatisch verzamelde verwijzer in rapporten. Deze variabele is handig in situaties waarin de referentie verloren kan gaan, bijvoorbeeld tijdens omleidingen of het tijdelijk doorsturen van de bezoeker naar een betalingsverwerker. Met deze variabele kunt u de afmetingen &#39;Referrer&#39; en &#39;Refering Domain&#39; vullen.

## Referrer in Adobe Experience Platform Launch

U kunt de verwijzer instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Referrer] sectie.

U kunt de verwijzing instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.reference in AppMeturement en de redacteur van de douanecode van de Lancering

De `s.referrer` variabele is een tekenreeks die de URL van de vorige pagina bevat. Deze variabele kan maximaal 255 bytes opslaan; waarden die groter zijn dan 255 bytes, worden afgekapt. AppMeturement plaatst automatisch deze variabele aan `document.referrer`; U hoeft deze variabele niet in te stellen, tenzij u de automatisch verzamelde waarde wilt overschrijven.

```js
s.referrer = "https://example.com";
```

Stel deze variabele niet in op niet-URL-waarden.

## Voorbeeld

Veel organisaties werken met implementaties rond omleidingen. U kunt het [`Util.getQueryParam()`](../functions/util-getqueryparam.md) hulpprogramma gebruiken om een verwijzing op te halen via de URL als uw site daar ruimte voor biedt. Zorg ervoor dat u URL codeert om het even welke waarden inbegrepen in het vraagkoord.

```js
// Example if the URL is https://example.com?r=https%3A%2F%2Fexample.org
s.referrer = s.Util.getQueryParam("r");
```
