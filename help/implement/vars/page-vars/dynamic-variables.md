---
title: Dynamische variabelen
description: Variabelen kopiëren zonder de lengte van de afbeeldingsaanvraag te verhogen.
translation-type: tm+mt
source-git-commit: 751d19227d74d66f3ce57888132514cf8bd6f7fc

---


# Dynamische variabelen

Met dynamische variabelen kunt u waarden van de ene variabele naar de andere kopiëren zonder dat de lengte van de afbeeldingsaanvraag toeneemt. Ze zijn handig wanneer u dezelfde gegevens in meerdere variabelen vastlegt.

In eerdere versies van Analytics was de lengte van de afbeeldingsaanvraag belangrijk om afgebroken gegevens te voorkomen. De verbeteringen aan AppMeasurement staan veel langere reeksen van de beeldverzoekvraag toe, zodat zijn de dynamische variabelen typisch niet nodig.

Dynamische variabelen ondersteunen parameters van queryreeksen of HTTP-headers in een afbeeldingsaanvraag. Zie de vraagparameters [van de](../../validate/query-parameters.md) gegevensinzameling voor een volledige lijst van beschikbare parameters aan verwijzing. Zie [Standaardaanvraagvelden](https://en.wikipedia.org/wiki/List_of_HTTP_header_fields#Request_fields) op Wikipedia voor een volledige lijst met beschikbare HTTP-aanvraagvelden waarnaar moet worden verwezen.

Wanneer Adobe een dynamisch veranderlijk voorvoegsel herkent, kopieert het automatisch het vraagkoord of de kopbalwaarde van HTTP in uw rapportreeks. Deze actie vindt plaats vóór enige andere verwerking, met inbegrip van verwerkingsregels en VISTA-regels.

> [!TIP] Houd rekening met de maximale tekenlimiet bij het kopiëren van variabelen. Bijvoorbeeld, als het kopiëren `eVar1` aan `prop1`, `prop1` kan een afgekapte waarde hebben aangezien het een grens 100 byte heeft (terwijl `eVar1` een grens van 255 byte heeft).

## Dynamische variabelen in Adobe Experience Platform Launch

U kunt dynamische variabelen in om het even welk afmetingsgebied gebruiken dat een koord goedkeurt. Dimensiewaarden worden doorgaans ingesteld tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de gewenste waarde voor de dimensie.

Plaats het voorvoegsel van de dynamische variabele in het tekstveld, gevolgd door de parameter van de querytekenreeks of de HTTP-header waarnaar u wilt verwijzen. Standaard is het voorvoegsel van de dynamische variabele `D=`.

## Dynamische variabelen in de aangepaste code-editor van AppMeasurement en Launch

Dynamische variabelen zijn tekstreeksen die aan andere variabelen zijn toegewezen. Het standaardvoorvoegsel van de dynamische variabele is `D=`. Dynamische variabelen zijn hoofdlettergevoelig.

```js
// Copy eVar1 into eVar2. The query string parameter of eVar1 is v1.
s.eVar1 = "Example value";
s.eVar2 = "D=v1";

// Take the user agent string found in the image request HTTP header and place it in eVar1.
s.eVar1 = "D=User-Agent";

// Copy the page URL and place it in eVar1. The query string parameter of page URL is g.
s.eVar1 = "D=g";
```

> [!NOTE] Dynamische variabelen worden als tekenreeksen weergegeven tijdens foutopsporing in uw implementatie. Waarden worden via de server gekopieerd door Adobe-servers voor gegevensverzameling.
