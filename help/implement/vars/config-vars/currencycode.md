---
title: Wat is de currencyCode-variabele en hoe gebruik ik deze?
description: Voor eCommerce-sites stelt de valuta in waarin de pagina handelt.
feature: Appmeasurement Implementation
exl-id: 3332c366-c472-4778-96c8-ef0aa756cca8
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# currencyCode

Voor plaatsen die handel gebruiken, is de opbrengst en de munt een belangrijk deel van Analytics. Veel sites, vooral sites die meerdere landen beslaan, gebruiken verschillende valuta&#39;s. Gebruik de variabele `currencyCode` om ervoor te zorgen dat de opbrengstattributen aan de correcte munt.

Bij valutaomrekening wordt bij elke druk de volgende logica gebruikt. Deze stappen zijn op opbrengstwaarden van toepassing plaatsen de [`products`](../page-vars/products.md) variabele en alle gebeurtenissen die als &quot;Valuta&quot;in [ de gebeurtenissen van het Succes ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) onder de reeksinstellingen van het Rapport worden vermeld.

* Als `currencyCode` niet is gedefinieerd, gaat Adobe ervan uit dat alle valutawaarden de valuta van de rapportsuite zijn. Zie {de Montages van de Rekening van 0} Algemeen ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) in de reeksinstellingen van het Rapport om de munt van de rapportreeks te zien.[
* Als `currencyCode` is gedefinieerd en overeenkomt met de valuta van de rapportsuite, wordt geen valutaomrekening toegepast.
* Als `currencyCode` is gedefinieerd en afwijkt van de valuta van de rapportsuite, past Adobe een valutaomrekening toe op basis van de wisselkoers van de huidige dag. De partners van Adobe met [ XE ](https://xe.com) om munt om te zetten elke dag. Alle waarden die in de rapportsuite zijn opgeslagen, bevinden zich in de valuta van de rapportsuite.
* Als `currencyCode` aan een ongeldige waarde wordt geplaatst, **wordt de volledige slag verworpen veroorzakend gegevensverlies.** Zorg ervoor dat deze variabele correct is gedefinieerd wanneer deze wordt gebruikt.

Deze variabele blijft niet behouden in verschillende treffers. Zorg ervoor dat deze variabele op elke pagina wordt bepaald die opbrengst of muntgebeurtenissen impliceert die niet de standaardmunt van de rapportreeks aanpassen.

>[!NOTE]
>
>Valutacodes kunnen tussen pagina&#39;s veranderen, maar voor alle valutacijfers bij één enkele hit moet dezelfde valuta worden gebruikt.

Een periode **moet** als muntseparator voor alle valuta worden gebruikt wanneer het uitvoeren van deze variabele. Zweedse kroon, die doorgaans een kommagescheidingsteken weergeeft, moet bijvoorbeeld worden gewijzigd om een punt in de `products` -variabele en alle valutagebeurtenissen te gebruiken. Adobe geeft bij rapportage het juiste valutascheidingsteken weer.

## Valutacode die het Web SDK gebruikt

Valutacode wordt toegewezen aan de volgende variabelen:

* [ voorwerp XDM ](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.commerce.order.currencyCode`
* [ voorwerp van Gegevens ](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.currencyCode` of `data.__adobe.analytics.cc`

## Valutacode die de extensie Adobe Analytics gebruikt

Valutacode is een veld onder de accordion [!UICONTROL General] bij het configureren van de Adobe Analytics-extensie.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Vouw de accordeon [!UICONTROL General] uit, zodat het veld [!UICONTROL Currency Code] zichtbaar wordt.

U kunt een vooraf ingestelde valutacode of een aangepaste valutacode gebruiken. Als u een aangepaste valutacode gebruikt, moet u controleren of de code geldig is.

## Valutacode in Adobe Experience Platform Mobile SDK

Valutacode wordt doorgegeven aan de Adobe Experience Platform Mobile SDK&#39;s via contextgegevensvariabelen in de Adobe Analytics-extensie.

1. Stel de valutacode in een contextgegevensvariabele tijdens `trackState` of `trackAction` in.
1. Maak een verwerkingsregel in Adobe Analytics Admin Tools voor de rapportsuite. Stel de regel in om de variabele Valutacode te overschrijven.
1. Geef de valutacode door aan de variabele `products` in de aanroep van `trackState` of `trackAction` .

U kunt een vooraf ingestelde valutacode of een aangepaste valutacode gebruiken. Als u een aangepaste valutacode gebruikt, moet u controleren of de code geldig is.

## s.currencyCode in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.currencyCode` variabele is een tekenreeks die een 3-letterige hoofdlettercode bevat die de valuta op de pagina vertegenwoordigt. Waarden zijn hoofdlettergevoelig.

```js
s.currencyCode = "USD";
```

De volgende valutacodes zijn geldig:

| Valuta | Label |
| --- | --- |
| `AED` | Verenigde Arabische Emiraten Dirhams |
| `AFA` | Afghanistan Afghanistan |
| `ALL` | Albanië Leke |
| `AMD` | Armenië Drams |
| `ANG` | Nederlandse Atilles Guilders |
| `AOA` | Angola Kwanza |
| `ARS` | Argentina Pesos |
| `AUD` | Australische dollars |
| `AWG` | Aruba Guilders |
| `AZM` | Azerbeidzjaanse machten |
| `BAM` | Bosnië en Herzegovina Converteerbare Marka |
| `BBD` | Barbados Dollars |
| `BDT` | Bangladesh Taka |
| `BGN` | Bulgarije Leva |
| `BHD` | Bahrain Dinars |
| `BIF` | Burundi Francs |
| `BMD` | Bermuda Dollars |
| `BND` | Brunei Dollars |
| `BOB` | Bolivia Bolivianos |
| `BRL` | Brazilië Reais |
| `BSD` | Bahamas Dollars |
| `BTN` | Bhutan Ngultrum |
| `BWP` | Botswana Pulas |
| `BYR` | Belarus Rubles |
| `BZD` | Belize Dollars |
| `CAD` | Canada Dollars |
| `CDF` | Congo/Kinshasa Francs |
| `CHF` | Zwitserse franken |
| `CLP` | Chili Pesos |
| `CNY` | China Yuan Renminbi |
| `COP` | Colombia Pesos |
| `CRC` | Costa Rica Colones |
| `CSD` | Servië Dinars |
| `CUP` | Cuba Pesos |
| `CVE` | Kaapverdië Escudos |
| `CYP` | Cyprus-grenzen |
| `CZK` | Tsjechische Republiek Koruny |
| `DJF` | Djibouti Francs |
| `DKK` | Denemarken Kroner |
| `DOP` | Dominicaanse Republiek Pesos |
| `DZD` | Algerije Dinars |
| `EEK` | Estland Krooni |
| `EGP` | Egyptische grenzen |
| `ERN` | Eritrea Nakfa |
| `ETB` | Ethiopia Birr |
| `EUR` | Euro |
| `FJD` | Fiji Dollars |
| `FKP` | Falklandeilanden |
| `GBP` | Verenigd Koninkrijk |
| `GEL` | Georgia Lari |
| `GGP` | Guernsey Pounds |
| `GHC` | Ghana Cedis |
| `GIP` | Gibraltar Pounds |
| `GMD` | Gambia Dalasi |
| `GNF` | Guinee Francs |
| `GTQ` | Guatemala Quetzales |
| `GYD` | Guyana Dollars |
| `HKD` | Hongkongse dollars |
| `HNL` | Honduras Lempiras |
| `HRK` | Kroatië Kuna |
| `HTG` | Haiti Gourdes |
| `HUF` | Hongarije Forint |
| `IDR` | Indonesië Rupiahs |
| `ILS` | Israel New Shekels |
| `IMP` | Isle of Man Pounds |
| `INR` | Indiase roepies |
| `IQD` | Irak-dinars |
| `IRR` | Iran Rials |
| `ISK` | IJslandse kroon |
| `JEP` | Jersey Pounds |
| `JMD` | Jamaica Dollars |
| `JOD` | Jordan Dinars |
| `JPY` | Japan Yen |
| `KES` | Kenya Shillings |
| `KGS` | Kirgizië |
| `KHR` | Cambodja Riels |
| `KMF` | Comoros Francs |
| `KPW` | Noord-Korea Won |
| `KRW` | Zuid-Korea Won |
| `KWD` | Koeweitse dinars |
| `KYD` | Dollars op de Caymaneilanden |
| `KZT` | Kazachstan Tenge |
| `LAK` | Laos Kips |
| `LBP` | Libanon-grenzen |
| `LKR` | Sri Lanka Rupes |
| `LRD` | Liberia Dollars |
| `LSL` | Lesotho Maloti |
| `LTL` | Litouwen Litai |
| `LVL` | Letland Lati |
| `LYD` | Libië Dinars |
| `MAD` | Marokko Dirhams |
| `MDL` | Moldavië Lei |
| `MGA` | Madagaskar Ariary |
| `MKD` | Denken Macedonië |
| `MMK` | Myanmar Kyats |
| `MNT` | Mongolië Tugriks |
| `MOP` | Macau Patacas |
| `MRO` | Mauritanië Ouguiyas |
| `MTL` | Malta Liri |
| `MUR` | Mauritius Rupes |
| `MVR` | Maldives Rufiyaa |
| `MWK` | Malawi Kwachas |
| `MXN` | Mexico Pesos |
| `MYR` | Maleisië Ringgits |
| `MZM` | Mozambique Meticais |
| `NAD` | Namibië Dollars |
| `NGN` | Nigeria Nairas |
| `NIO` | Nicaragua Gold Cordobas |
| `NOK` | Noorwegen Kroner |
| `NPR` | Nepal Rupes |
| `NZD` | Nieuw-Zeelandse dollars |
| `OMR` | Oman Rials |
| `PAB` | Panama Balboas |
| `PEN` | Peru Nuevos Soles |
| `PGK` | Papoea-Nieuw-Guinea Kina |
| `PHP` | Filipijnen Pesos |
| `PKR` | Pakistan Rupes |
| `PLN` | Polen Zlotych |
| `PYG` | Paraguay Gari |
| `QAR` | Qatar Riyals |
| `ROL` | Roemenië Lei |
| `RUR` | Russische roebel |
| `RWF` | Rwanda Francs |
| `SAR` | Saoedi-Arabië Riyals |
| `SBD` | Salomonseilanden, dollars |
| `SCR` | Seychellen Rupes |
| `SDD` | Sudan Dinars |
| `SEK` | Zweedse kroon |
| `SGD` | Singapore Dollars |
| `SHP` | Sint-Helena Pounds |
| `SIT` | Slovenië Tolars |
| `SKK` | Slowakije Koruny |
| `SLL` | Sierra Leone Leones |
| `SOS` | Somalië Shillings |
| `SPL` | Seborga Luigini |
| `SRD` | Suriname Dollars |
| `SRG` | Suriname Guilders |
| `STD` | Sao Tome en Principe Dobras |
| `SVC` | El Salvador Colones |
| `SYP` | Syrische grenzen |
| `SZL` | Swaziland Emalangeni |
| `THB` | Thailand Baht |
| `TJS` | Tadzjikistan Somoni |
| `TMM` | Turkmenistan Manats |
| `TND` | Tunesische dinars |
| `TOP` | Tonga Pa&#39;anga |
| `TRL` | Turkije Liras |
| `TTD` | Trinidad en Tobago Dollars |
| `TVD` | Tuvalu Dollars |
| `TWD` | Taiwan Nieuwe dollars |
| `TZS` | Tanzania Shillings |
| `UAH` | Oekraïne Hryvnia |
| `UGX` | Oegandese shillingen |
| `USD` | Amerikaanse dollar |
| `UYU` | Uruguay Pesos |
| `UZS` | Oezbekistan |
| `VEB` | Venezuela Bolivares |
| `VND` | Vietnam Dong |
| `VUV` | Vanuatu Vatu |
| `WST` | Samoa Tala |
| `XAF` | Communauté Financière Afriaine Francs B |
| `XAG` | Zilveren ounces |
| `XAU` | Goud |
| `XCD` | Oost-Caribische dollars |
| `XDR` | Speciale uitgave bij het Internationaal Monetair Fonds |
| `XOF` | Communauté Financière Afriaine Francs B |
| `XPD` | Palladium Ounces |
| `XPF` | Comptoirs Français du Pacifique Francs |
| `XPT` | Platinum Ounces |
| `YER` | Jemen Rials |
| `ZAR` | Zuid-Afrika Rand |
| `ZMK` | Zambia Kwacha |
| `ZWD` | Zimbabwe Dollar |
