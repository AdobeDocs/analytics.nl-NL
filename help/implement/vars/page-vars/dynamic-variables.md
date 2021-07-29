---
title: Dynamische variabelen
description: Variabelen kopiëren zonder de lengte van de afbeeldingsaanvraag te verhogen.
exl-id: 41aab44d-01fd-45fe-892d-637d69488d98
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---

# Dynamische variabelen

Met dynamische variabelen kunt u waarden van de ene variabele naar de andere kopiëren zonder dat de lengte van de afbeeldingsaanvraag toeneemt. Ze zijn handig wanneer u dezelfde gegevens in meerdere variabelen vastlegt.

In eerdere versies van Analytics was de lengte van de afbeeldingsaanvraag belangrijk om afgebroken gegevens te voorkomen. De verbeteringen aan AppMeasurement staan veel langere reeksen van de beeldverzoekvraag toe, zodat zijn de dynamische variabelen typisch niet nodig.

Dynamische variabelen ondersteunen parameters van queryreeksen of HTTP-headers in een afbeeldingsaanvraag. Zie [de vraagparameters van de gegevensinzameling](../../validate/query-parameters.md) voor een volledige lijst van beschikbare parameters aan verwijzing. Zie [Standaardaanvraagvelden](https://en.wikipedia.org/wiki/List_of_HTTP_header_fields#Request_fields) op Wikipedia voor een volledige lijst met beschikbare HTTP-aanvraagvelden waarnaar moet worden verwezen.

Wanneer Adobe een dynamisch veranderlijke prefix erkent, kopieert het automatisch het vraagkoord of de kopbalwaarde van HTTP in uw rapportreeks. Deze actie vindt plaats vóór enige andere verwerking, met inbegrip van verwerkingsregels en VISTA-regels.

>[!TIP]
>
>Houd rekening met de maximale tekenlimiet bij het kopiëren van variabelen. Als bijvoorbeeld `eVar1` naar `prop1` wordt gekopieerd, kan `prop1` een ingekorte waarde hebben omdat deze een limiet van 100 bytes heeft (terwijl `eVar1` een limiet van 255 bytes heeft).

## Dynamische variabelen met tags in Adobe Experience Platform

U kunt dynamische variabelen in om het even welk afmetingsgebied gebruiken dat een koord goedkeurt. Dimension-items worden doorgaans ingesteld tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek het gewenste dimensie-item.

Plaats het voorvoegsel van de dynamische variabele in het tekstveld, gevolgd door de parameter van de querytekenreeks of de HTTP-header waarnaar u wilt verwijzen. Standaard is het voorvoegsel van de dynamische variabele `D=`.

## Dynamische variabelen in AppMeasurement en aangepaste code-editor

Dynamische variabelen zijn tekstreeksen die aan andere variabelen zijn toegewezen. Het standaard dynamische veranderlijke prefix is `D=`. Dynamische variabelen zijn hoofdlettergevoelig.

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
>Dynamische variabelen worden als tekenreeksen weergegeven tijdens foutopsporing in uw implementatie. De waarden zijn gekopieerde server-kant door de servers van de Adobe gegevensinzameling.
