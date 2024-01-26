---
title: Dynamische variabelen
description: Variabelen kopiëren zonder de lengte van de afbeeldingsaanvraag te verhogen.
feature: Variables
exl-id: 41aab44d-01fd-45fe-892d-637d69488d98
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Dynamische variabelen

Met dynamische variabelen kunt u waarden van de ene variabele naar de andere kopiëren zonder dat de lengte van de afbeeldingsaanvraag toeneemt. Ze zijn handig wanneer u dezelfde gegevens in meerdere variabelen vastlegt.

In eerdere versies van Analytics was de lengte van de afbeeldingsaanvraag belangrijk om afgebroken gegevens te voorkomen. De verbeteringen aan AppMeasurement staan veel langere reeksen van de beeldvraag van de beeldvraag toe, zodat zijn de dynamische variabelen typisch niet nodig.

Dynamische variabelen ondersteunen parameters van queryreeksen of HTTP-headers in een afbeeldingsaanvraag. Zie [queryparameters voor gegevensverzameling](../../validate/query-parameters.md) voor een volledige lijst van beschikbare parameters waarnaar moet worden verwezen. Zie [Standaardaanvraagvelden](https://en.wikipedia.org/wiki/List_of_HTTP_header_fields#Request_fields) op Wikipedia voor een volledige lijst van beschikbare HTTP- verzoekgebieden aan verwijzing.

Wanneer de Adobe een dynamisch veranderlijke prefix erkent, kopieert het automatisch het vraagkoord of de kopbalwaarde van HTTP in uw rapportreeks. Deze actie vindt plaats vóór enige andere verwerking, met inbegrip van verwerkingsregels en VISTA-regels.

>[!TIP]
>
>Houd rekening met de maximale tekenlimiet bij het kopiëren van variabelen. Bijvoorbeeld bij kopiëren `eVar1` tot `prop1`, `prop1` kan een ingekorte waarde hebben omdat deze een limiet van 100 bytes heeft (terwijl `eVar1` heeft een limiet van 255 bytes).

## Dynamische variabelen met de SDK van het Web

Gebruik gegevenstoewijzing DataStream om gegevens naar veelvoudige variabelen van Analytics van één enkel XDM gebied te verzenden.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klikken **[!UICONTROL Datastreams]** in het linkerspoor.
1. Klik op de gewenste gegevensstroom.
1. Klikken **[!UICONTROL Edit Mapping]** rechts.
1. Wijs de gewenste afbeelding toe [!UICONTROL Source Field] naar wens [!UICONTROL Target Field]. Eén bronveld kan worden toegewezen aan een willekeurig aantal doelvelden.

## Dynamische variabelen met de Adobe Analytics-extensie

U kunt dynamische variabelen in om het even welk afmetingsgebied gebruiken dat een koord goedkeurt. De punten van het Dimension worden typisch geplaatst terwijl het vormen van de uitbreiding van de Analyse (globale variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek het gewenste dimensie-item.

Plaats het voorvoegsel van de dynamische variabele in het tekstveld, gevolgd door de parameter van de querytekenreeks of de HTTP-header waarnaar u wilt verwijzen. Standaard is het voorvoegsel van de dynamische variabele `D=`.

## Dynamische variabelen in AppMeasurement en de de uitbreidingsredacteur van de douanecode van de Analyse

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

>[!NOTE]
>
>Dynamische variabelen worden als tekenreeksen weergegeven tijdens foutopsporing in uw implementatie. De waarden worden gekopieerd server-kant door de servers van de de gegevensinzameling van de Adobe.
