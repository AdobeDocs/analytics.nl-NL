---
title: AMO EF-ID
description: De EF-id van Adobe Media Optimizer, die wordt gebruikt in Adobe Advertising-integraties.
feature: Dimensions
source-git-commit: 408d8db0d1e3c8301a066fe54d611ec7b8e3418a
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# AMO EF-ID

De **[!UICONTROL AMO EF ID]** is een id voor een advertentie-klik die wordt gebruikt in Adobe Advertising-integratie. Het is een unieke token die Adobe Advertising gebruikt om activiteiten te koppelen aan een online klik of belichting op bezoekersniveau. De afmeting wordt automatisch gecreeerd wanneer het toelaten van [&#x200B; Analytics voor de integratie van Advertising &#x200B;](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview).

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt de waarden ervan op meerdere manieren:

* Voor klik-door verkeer, wordt het gegeven verzameld van de `ef_id` parameter van het vraagkoord in de [&#x200B; Pagina URL &#x200B;](page-url.md), gewoonlijk op de pagina waardoor het ad-gedreven verkeer de plaats ingaat.
* Doorklikken kan ook worden vastgelegd wanneer de URL geen volgcodes bevat, maar de Adobe Advertising JavaScript detecteert een klik in de voorafgaande twee minuten.
* Voor gesteund mening-door verkeer, vult Adobe Advertising waarden op het achterste eind gebruikend een supplementaire identiteitskaart (`SDID`).

>[!NOTE]
>
>EF-id&#39;s zijn hoofdlettergevoelig. Als uw implementatie URL-tracking in kleine letters dwingt, herkent Adobe Advertising de EF-id niet.

## Dimension-objecten

Dimension-items bevatten id&#39;s voor toevoegen en klikken die zijn gegenereerd door ondersteunde advertentienetwerken. De tekenreeksindeling is afhankelijk van het netwerk en het kanaal dat de tekenreeks heeft gegenereerd.

### Zoeken in Google Adds

```text
{gclid}:G:{s}
```

* **`gclid`**: De Google klik-id (GCLID).
* **`s`**: Het netwerktype (`"s"` voor onderzoek).

### Microsoft Advertising-zoekadvertenties

```text
{msclkid}:G:{s}
```

* **`msclkid`**: De Microsoft klik-id (MSCLKID).
* **`s`**: Het netwerktype (`"s"` voor onderzoek).

### Advertenties en zoekadvertenties weergeven op andere zoekmachines

```text
{amovid}:{ts}:{channel}
```

* **`amovid`**: De Adobe Advertising-bezoeker-id, ook wel de surfer-id genoemd.
* **`ts`**: De tijdstempel die door Adobe Advertising wordt gegenereerd.
* **`channel`**: Het kanaaltype dat verantwoordelijk is voor de klik of belichting:
   * **`d`**: Een klik op een DSP-advertentie (klik-via tonen).
   * **`i`**: Een indruk op een DSP-advertentie (display view-through).
   * **`s`**: Een klik op een zoekadvertentie (doorzoekklik).

### Voorbeelden

```text
CjwKCAiAkbbMBhB2EiwANbxtbb9L573Dys0rjTDqcMo3x7tv2yEfh1RGb8exG9N892NoMqAzMBEGmhoCWxwQAvD_BwE:G:s
06207ca63ae6f4fa832197585547393c:20260301111101:i
WcmibgAAAHJK1RyY:1551968087687:d
```
