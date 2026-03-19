---
title: AMO-id
description: De Adobe Media Optimizer-id die wordt gebruikt in Adobe Advertising-integratie.
feature: Dimensions
source-git-commit: 408d8db0d1e3c8301a066fe54d611ec7b8e3418a
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 1%

---

# AMO-id

**[!UICONTROL AMO ID]** is een verzameling samengevoegde id&#39;s die worden gebruikt in Adobe Advertising-integratie. Waarden die in deze dimensie zijn opgeslagen, worden automatisch ingedeeld in afzonderlijke, meer leesbare classificatiedimensies voor gebruik in analytische rapportage. De afmeting wordt automatisch gecreeerd wanneer het toelaten van [ Analytics voor de integratie van Advertising ](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview).

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt de waarden ervan op meerdere manieren:

* Voor klik-door verkeer, wordt het gegeven verzameld van de `s_kwcid` parameter van het vraagkoord in de [ Pagina URL ](page-url.md), gewoonlijk op de pagina waardoor het ad-gedreven verkeer de plaats ingaat.
* Doorklikken kan ook worden vastgelegd wanneer de URL geen volgcodes bevat, maar de Adobe Advertising JavaScript detecteert een klik in de voorafgaande twee minuten.
* Voor gesteund mening-door verkeer, vult Adobe Advertising waarden op het achterste eind gebruikend een supplementaire identiteitskaart (`SDID`).

## Dimension-objecten

Dimension-items bevatten AMO-id&#39;s, ook wel `s_kwcid` -waarden genoemd. De exacte indeling hangt af van het feit of het verkeer afkomstig is van DSP of van Search, Social en Commerce. AMO-id&#39;s zijn korter dan EF-id&#39;s en worden voornamelijk gebruikt voor classificaties en inname van Adobe Advertising-metriek in Analytics.

### DSP

```text
AC!{ad key}!{placement key}
```

* **`AC`** - Geeft het weergavekanaal aan.
* **`ad key`**: door Adobe Advertising gegenereerde alfanumerieke id voor de advertentie.
* **`placement key`**: door Adobe Advertising gegenereerde alfanumerieke id voor de plaatsing.

Voorbeeld:

```text
AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7
```

### Zoeken, sociale media en Commerce-advertenties

AMO-id&#39;s voor zoeken, sociale media en Commerce beginnen met `AL` , gevolgd door de gebruikers-id van de adverteerder, de id van de advertentienetwerkaccount en netwerkspecifieke id&#39;s. Tot de id&#39;s van gedeelde en netwerkaccounts behoren:

* **`3`**: Google Ads
* **`10`**: Microsoft Advertising
* **`45`**: Meta
* **`86`**: Yahoo! Netwerk weergeven
* **`87`**: Naver
* **`88`**: Baidu
* **`90`**: Yandex
* **`94`**: Yahoo! Japan Adds
* **`105`**: Yahoo Native (afgekeurd)
* **`106`**: Pinterest (afgekeurd)

#### Google Adds

Google Ads gebruikt twee verwante indelingen. Nieuwere accounts kunnen campagne-id en ad-groep-id bevatten, die campagne- en ad-group-rapportage voor Performance Max en concepten/experimentatiecampagnes ondersteunt.

```text
AL!{user}!3!{creative}!{matchtype}!{placement}!{network}!{product partition}!{keyword}[!{campaign id}!{ad group id}]
```

* **`creative`**: Google voegt creatieve id toe.
* **`matchtype`**: Trefwoordmatch-type (`e` voor exact, `p` voor woordgroep, `b` voor breed).
* **`placement`**: domein waarop op de advertentie is geklikt.
* **`network`**: Netwerk waarop de klik plaatsvond (`g` voor Google onderzoek, `s` voor een onderzoekspartner, `d` voor vertoning).
* **`product partition`**: Product group ID for product ads.
* **`keyword`**: Trefwoord triggeren op zoeksites of trefwoord dat het beste overeenkomt met de gewenste zoekopdracht op inhoudssites.
* **`campaign id`**: Google Ads-campagne-id, indien aanwezig.
* **`ad group id`**: Google Ads en groep-id, indien aanwezig.

Voor dynamische zoekopdrachten wordt het trefwoordveld gevuld met het automatische doel.

Voorbeeld:

```text
AL!1234!3!569345525675!e!!g!!adobe express!15557590691!136734402131
```

#### Microsoft Advertising

```text
AL!{user}!10!{ad id}!!!!{keyword/order item id}!!{campaign id}!{ad group id}
```

* **`ad id`**: Creatieve id van Microsoft Advertising.
* **`keyword/order item id`**: Microsoft Advertising-trefwoordid.
* **`campaign id`**: Microsoft Advertising-campagne-id.
* **`ad group id`**: Microsoft Advertising en groep-id.

Voor sommige niet-gemigreerde accounts kunnen nog steeds oudere Microsoft-indelingen bestaan.

Voorbeeld:

```text
AL!1234!10!79577297926903!!!!79577437127536!!291647087!1273234845019564
```

#### Baidu

```text
AL!{user}!88!{creative}!{placement}!{keyword id}
```

* **`creative`**: Baidu creative ID.
* **`placement`**: website waarop op de advertentie is geklikt.
* **`keyword id`**: Basis-trefwoordid.

#### Yahoo! Japan Adds

```text
AL!{user}!94!{creative}!{matchtype}!{network}!{keyword}
```

* **`creative`**: Yahoo! Japan voegt creatieve id toe.
* **`matchtype`**: Trefwoordmatch-type (`be` exact, `bp` uitdrukking, `bb` breed).
* **`network`**: Netwerk waarop de klik heeft plaatsgevonden (`n` native, `s` zoekopdracht).
* **`keyword`**: trefwoord triggeren.

#### Yandex

```text
AL!{user}!90!{ad id}!{source type}!!!{phrase id}
```

* **`ad id`**: Yandex creative ID.
* **`source type`**: Sitetype waarop de advertentie is weergegeven (`b` zoeken, `c` context/inhoud, `ct` categorie).
* **`phrase id`**: Yandex-trefwoord-id.

## Classificaties

Wanneer het toelaten van [ Analytics voor de integratie van Advertising ](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview), worden de volgende classificaties automatisch gecreeerd. De classificatiewaarden worden automatisch door de integratie gehandhaafd.

| Classificatie | Beschrijving | DSP | Onderzoek, <br> Sociale, &amp; <br> Commerce |
| --- | --- | :---: | :---: |
| **[!UICONTROL Account]** | De accountnaam. | &amp;check; | &amp;check; |
| **[!UICONTROL Ad Display URL]** | De URL die wordt weergegeven in de advertentie. | | &amp;check; |
| **[!UICONTROL Ad Description]** | De beschrijving van de advertentie (DSP) of advertentie (Zoeken, Sociaal en Commerce). | &amp;check; | &amp;check; |
| **[!UICONTROL Ad Destination URL]** | De doel-URL voor de advertentie. | | &amp;check; |
| **[!UICONTROL Ad Group]** | De naam van de advertentiegroep. | | &amp;check; |
| **[!UICONTROL Ad Platform]** | De naam van de advertentie-DSP of zoekmachine. | &amp;check; | &amp;check; |
| **[!UICONTROL Ad Title]** | Het advertentietype (DSP) of advertentietype (Zoeken, Sociaal en Commerce). | &amp;check; | &amp;check; |
| **[!UICONTROL Ad Type]** | Het advertentietype, zoals `text` , `video` , `display` of `native` . | &amp;check; | &amp;check; |
| **[!UICONTROL AdCloud Attribute 1]** -<br>**[!UICONTROL AdCloud Attribute 5]** | Classificaties van plaatsaanduidingen zijn gereserveerd voor toekomstige aangepaste kenmerken. Momenteel niet in gebruik. | | |
| **[!UICONTROL Campaign]** | De naam van de campagne. | &amp;check; | &amp;check; |
| **[!UICONTROL Creative Experience Name]** | Naam van de creatieve ervaring verbonden aan de advertentie interactie, die een groep creatieve variaties vertegenwoordigt die in het testen of verpersoonlijken worden gebruikt. | &amp;check; | |
| **[!UICONTROL Creative Branch Name]** | Naam van de vertakking binnen een creatieve ervaring die een specifieke variatie of weg in het creatieve experiment vertegenwoordigt. | &amp;check; | |
| **[!UICONTROL Creative Branch ID]** | Unieke id die aan een creatieve vertakking wordt toegewezen binnen een creatieve ervaring. | &amp;check; | |
| **[!UICONTROL Creative Name]** | Naam van het specifieke en creatieve middel dat aan de gebruiker werd betekend. | &amp;check; | |
| **[!UICONTROL Creative Variant Name]** | Naam van de specifieke variant van een creatief object dat wordt gebruikt binnen een creatieve ervaring of vertakking. | &amp;check; | |
| **[!UICONTROL Keyword]** | Het trefwoord. | | &amp;check; |
| **[!UICONTROL Keyword Match Type]** | Het trefwoord en het overeenkomende type. | | &amp;check; |
| **[!UICONTROL Landing Type]** | Hiermee wordt aangegeven of het item van de openingspagina een doorkijkeffect of een doorklikeffect heeft. | &amp;check; | &amp;check; |
| **[!UICONTROL Match Type]** | Het type zoekovereenkomst. | | &amp;check; |
| **[!UICONTROL Network]** | RTB (DSP) of de naam van het advertentienetwerk (Search, Social, &amp; Commerce). | &amp;check; | &amp;check; |
| **[!UICONTROL Optimization]** | De pakketnaam (DSP) of de portfolionaam (Zoeken, Sociaal en Commerce). | &amp;check; | &amp;check; |
| **[!UICONTROL Placement]** | De plaatsingsnaam. | &amp;check; | |
| **[!UICONTROL Product Target]** | Het productdoel voor een advertentie voor een productaanbieding. | | &amp;check; |
