---
title: Dynamische variabelen
description: Variabelen kopiëren zonder de lengte van de afbeeldingsaanvraag te verhogen.
feature: Appmeasurement Implementation
exl-id: 41aab44d-01fd-45fe-892d-637d69488d98
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Dynamische variabelen

Met dynamische variabelen kunt u waarden van de ene variabele naar de andere kopiëren zonder dat de lengte van de afbeeldingsaanvraag toeneemt. Ze zijn handig wanneer u dezelfde gegevens in meerdere variabelen vastlegt.

In eerdere versies van Analytics was de lengte van de afbeeldingsaanvraag belangrijk om afgebroken gegevens te voorkomen. De verbeteringen aan AppMeasurement staan veel langere reeksen van de beeldverzoekvraag toe, zodat zijn de dynamische variabelen typisch niet nodig.

Dynamische variabelen ondersteunen parameters van queryreeksen of HTTP-headers in een afbeeldingsaanvraag. Zie [&#x200B; parameters van de de vraagvraag van de gegevensinzameling &#x200B;](../../validate/query-parameters.md) voor een volledige lijst van beschikbare parameters aan verwijzing. Zie [&#x200B; Standaard verzoekgebieden &#x200B;](https://en.wikipedia.org/wiki/List_of_HTTP_header_fields#Request_fields) op Wikipedia voor een volledige lijst van beschikbare HTTP- verzoekgebieden aan verwijzing.

Wanneer Adobe een dynamisch veranderlijk voorvoegsel erkent, kopieert het automatisch het vraagkoord of de kopbalwaarde van HTTP in uw rapportreeks. Deze actie vindt plaats vóór enige andere verwerking, met inbegrip van verwerkingsregels en VISTA-regels.

>[!TIP]
>
>Houd rekening met de maximale tekenlimiet bij het kopiëren van variabelen. Als `eVar1` naar `prop1` wordt gekopieerd, kan `prop1` bijvoorbeeld een ingekorte waarde hebben omdat deze een limiet van 100 bytes heeft (terwijl `eVar1` een limiet van 255 bytes heeft).

## Dynamische variabelen die de Web SDK gebruiken

Gebruik gegevenstoewijzing DataStream om gegevens naar veelvoudige variabelen van Analytics van één enkel XDM gebied te verzenden.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op **[!UICONTROL Datastreams]** in de linkertrack.
1. Klik op de gewenste gegevensstroom.
1. Klik op **[!UICONTROL Edit Mapping]** aan de rechterkant.
1. Wijs het gewenste [!UICONTROL Source Field] aan het gewenste [!UICONTROL Target Field] toe. Eén bronveld kan worden toegewezen aan een willekeurig aantal doelvelden.

## Dynamische variabelen met de Adobe Analytics-extensie

U kunt dynamische variabelen in om het even welk afmetingsgebied gebruiken dat een koord goedkeurt. Dimension-items worden doorgaans ingesteld tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek het gewenste dimensie-item.

Plaats het voorvoegsel van de dynamische variabele in het tekstveld, gevolgd door de parameter van de querytekenreeks of de HTTP-header waarnaar u wilt verwijzen. Standaard is het voorvoegsel van de dynamische variabele `D=` .

## Dynamische variabelen in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

Dynamische variabelen zijn tekstreeksen die aan andere variabelen zijn toegewezen. Het standaardvoorvoegsel van de dynamische variabele is `D=` . Dynamische variabelen zijn hoofdlettergevoelig.

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
>Dynamische variabelen worden als tekenreeksen weergegeven tijdens foutopsporing in uw implementatie. Waarden worden via de server gekopieerd door Adobe-gegevensverzamelingsservers.
