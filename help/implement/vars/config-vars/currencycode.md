---
title: Wat is de currencyCode-variabele en hoe gebruik ik deze?
description: Voor eCommerce-sites stelt de valuta in waarin de pagina handelt.
translation-type: tm+mt
source-git-commit: 4d0d5ca99049e48fcf1f248f78ecef94534b6815
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---


# currencyCode

Voor plaatsen die handel gebruiken, is de opbrengst en de munt een belangrijk deel van Analytics. Veel sites, vooral sites die meerdere landen beslaan, gebruiken verschillende valuta&#39;s. Gebruik de `currencyCode` variabele om opbrengstattributen aan de correcte munt te verzekeren.

Als `currencyCode` niet wordt bepaald, worden de monetaire waarden die [`products`](../page-vars/products.md) veranderlijke en valutagebeurtenissen worden bepaald behandeld alsof zij het zelfde als de munt van de rapportreeks zijn. Zie [Algemene accountinstellingen](/help/admin/admin/general-acct-settings-admin.md) in de gebruikershandleiding voor Admin om de valuta van de rapportsuite te bekijken.

Als `currencyCode` wordt bepaald en de munt van de rapportreeks aanpast, wordt geen muntomzetting toegepast.

Als `currencyCode` is gedefinieerd en anders is dan de valuta van de rapportsuite, past Adobe een valutaomrekening toe op basis van de wisselkoers van de huidige dag. Adobe werkt met [XE](https://xe.com) samen om valuta elke dag om te zetten. Alle waarden die in gegevensverzamelingsservers worden opgeslagen, worden uiteindelijk opgeslagen in de valuta van de rapportsuite.

>[!IMPORTANT]
>
>Als `currencyCode` een ongeldige waarde bevat, wordt de volledige slag verworpen veroorzakend gegevensverlies. Zorg ervoor dat deze variabele correct is gedefinieerd als u deze in uw implementatie gebruikt.

Deze variabele blijft niet bestaan tussen treffers. Zorg ervoor dat deze variabele op elke pagina wordt bepaald die opbrengst of muntgebeurtenissen impliceert.

## Valutacode in Adobe Experience Platform Launch

Valutacode is een veld onder de accordion [!UICONTROL General] bij het configureren van de Adobe Analytics-extensie.

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL General] uit, zodat het veld [!UICONTROL Currency Code] zichtbaar wordt.

U kunt een vooraf ingestelde valutacode of een aangepaste valutacode gebruiken. Als u een aangepaste valutacode gebruikt, moet u controleren of de code geldig is.

## Valutacode in Adobe Experience Platform Mobile SDK

Valutacode wordt doorgegeven aan de Adobe Experience Platform Mobile SDK&#39;s via contextgegevensvariabelen in de Adobe Analytics-extensie.

1. Stel de valutacode in een contextgegevensvariabele in tijdens `trackState` of `trackAction`.
2. Maak een verwerkingsregel in de Adobe Analytics-beheerconsole voor de rapportsuite. Stel de regel in om de variabele Valutacode te overschrijven.
3. Geef de valutacode aan de `products` variabele in uw vraag aan `trackState` of `trackAction` door.

U kunt een vooraf ingestelde valutacode of een aangepaste valutacode gebruiken. Als u een aangepaste valutacode gebruikt, moet u controleren of de code geldig is.

## s.currencyCode in AppMeasurement en Launch, aangepaste code-editor

De variabele `s.currencyCode` is een tekenreeks die een code van drie letters bevat die de valuta op de pagina vertegenwoordigt.

```js
s.currencyCode = "USD";
```

De volgende valutacodes zijn geldig:

| Valutacode | Valuta |
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
| `CZK` | Tsjechië Koruny |
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
| `MKD` | Macedonië |
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
