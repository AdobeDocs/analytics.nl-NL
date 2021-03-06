---
title: Wat is de currencyCode-variabele en hoe gebruik ik deze?
description: Voor eCommerce-sites stelt de valuta in waarin de pagina handelt.
feature: Variables
exl-id: 3332c366-c472-4778-96c8-ef0aa756cca8
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# currencyCode

Voor plaatsen die handel gebruiken, is de opbrengst en de munt een belangrijk deel van Analytics. Veel sites, vooral sites die meerdere landen beslaan, gebruiken verschillende valuta&#39;s. Gebruik de `currencyCode` variabele om ervoor te zorgen dat de opbrengstattributen aan de correcte munt.

Indien `currencyCode` niet gedefinieerd is, monetaire waarden gedefinieerd als [`products`](../page-vars/products.md) variabele - en valutagebeurtenissen worden behandeld alsof ze dezelfde zijn als de valuta van de rapportsuite . Zie [Algemene accountinstellingen](/help/admin/admin/general-acct-settings-admin.md) in de handleiding voor Admin-gebruikers om de valuta van de rapportsuite te bekijken.

Indien `currencyCode` is gedefinieerd en overeenkomt met de valuta van de rapportsuite. Er wordt geen valutaomrekening toegepast.

Indien `currencyCode` is gedefinieerd en verschilt van de valuta van de rapportsuite, past Adobe een valutaomrekening toe op basis van de wisselkoers van de huidige dag. Adobe partners met [XE](https://xe.com) om de valuta elke dag om te zetten. Alle waarden die in gegevensverzamelingsservers worden opgeslagen, worden uiteindelijk opgeslagen in de valuta van de rapportsuite.

>[!WARNING]
>
>Indien `currencyCode` bevat een ongeldige waarde. De hele hit wordt genegeerd, waardoor gegevens verloren gaan. Zorg ervoor dat deze variabele correct is gedefinieerd als u deze in uw implementatie gebruikt.

Deze variabele blijft niet bestaan tussen treffers. Zorg ervoor dat deze variabele op elke pagina wordt bepaald die opbrengst of muntgebeurtenissen impliceert.

## Valutacode die de Web SDK gebruikt

Valutacode is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `commerce.order.currencyCode`.

## Valutacode die de extensie Adobe Analytics gebruikt

Valutacode is een veld onder de [!UICONTROL General] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Breid uit [!UICONTROL General] accordion, die de [!UICONTROL Currency Code] veld.

U kunt een vooraf ingestelde valutacode of een aangepaste valutacode gebruiken. Als u een aangepaste valutacode gebruikt, moet u controleren of de code geldig is.

## Valutacode in Adobe Experience Platform Mobile SDK

Valutacode wordt doorgegeven aan de Adobe Experience Platform Mobile SDK&#39;s via contextgegevensvariabelen in de Adobe Analytics-extensie.

1. De valutacode instellen in een contextgegevensvariabele tijdens een van de `trackState` of `trackAction`.
1. Maak een verwerkingsregel in de Adobe Analytics-beheerconsole voor de rapportsuite. Stel de regel in om de variabele Valutacode te overschrijven.
1. Geef de valutacode door aan de `products` variabele in uw vraag aan `trackState` of `trackAction`.

U kunt een vooraf ingestelde valutacode of een aangepaste valutacode gebruiken. Als u een aangepaste valutacode gebruikt, moet u controleren of de code geldig is.

## s.currencyCode in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.currencyCode` variable is a string, containing a 3 letter uppercase code representing the currency on the page.

```js
s.currencyCode = "USD";
```

De volgende valutacodes zijn geldig:

| Valutacode | Valuta |
| --- | --- |
| `AED` | Verenigde Arabische Emiraten Dirhams |
| `AFA` | Afghanistan Afghanistan |
| `ALL` | Albani?? Leke |
| `AMD` | Armeni?? Drams |
| `ANG` | Nederlandse Atilles Guilders |
| `AOA` | Angola Kwanza |
| `ARS` | Argentina Pesos |
| `AUD` | Australische dollars |
| `AWG` | Aruba Guilders |
| `AZM` | Azerbeidzjaanse machten |
| `BAM` | Bosni?? en Herzegovina Converteerbare Marka |
| `BBD` | Barbados Dollars |
| `BDT` | Bangladesh Taka |
| `BGN` | Bulgarije Leva |
| `BHD` | Bahrain Dinars |
| `BIF` | Burundi Francs |
| `BMD` | Bermuda Dollars |
| `BND` | Brunei Dollars |
| `BOB` | Bolivia Bolivianos |
| `BRL` | Brazili?? Reais |
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
| `CSD` | Servi?? Dinars |
| `CUP` | Cuba Pesos |
| `CVE` | Kaapverdi?? Escudos |
| `CYP` | Cyprus-grenzen |
| `CZK` | Tsjechi?? Koruny |
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
| `HRK` | Kroati?? Kuna |
| `HTG` | Haiti Gourdes |
| `HUF` | Hongarije Forint |
| `IDR` | Indonesi?? Rupiahs |
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
| `KGS` | Kirgizi?? |
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
| `LYD` | Libi?? Dinars |
| `MAD` | Marokko Dirhams |
| `MDL` | Moldavi?? Lei |
| `MGA` | Madagaskar Ariary |
| `MKD` | Macedoni?? |
| `MMK` | Myanmar Kyats |
| `MNT` | Mongoli?? Tugriks |
| `MOP` | Macau Patacas |
| `MRO` | Mauritani?? Ouguiyas |
| `MTL` | Malta Liri |
| `MUR` | Mauritius Rupes |
| `MVR` | Maldives Rufiyaa |
| `MWK` | Malawi Kwachas |
| `MXN` | Mexico Pesos |
| `MYR` | Maleisi?? Ringgits |
| `MZM` | Mozambique Meticais |
| `NAD` | Namibi?? Dollars |
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
| `ROL` | Roemeni?? Lei |
| `RUR` | Russische roebel |
| `RWF` | Rwanda Francs |
| `SAR` | Saoedi-Arabi?? Riyals |
| `SBD` | Salomonseilanden, dollars |
| `SCR` | Seychellen Rupes |
| `SDD` | Sudan Dinars |
| `SEK` | Zweedse kroon |
| `SGD` | Singapore Dollars |
| `SHP` | Sint-Helena Pounds |
| `SIT` | Sloveni?? Tolars |
| `SKK` | Slowakije Koruny |
| `SLL` | Sierra Leone Leones |
| `SOS` | Somali?? Shillings |
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
| `UAH` | Oekra??ne Hryvnia |
| `UGX` | Oegandese shillingen |
| `USD` | Amerikaanse dollar |
| `UYU` | Uruguay Pesos |
| `UZS` | Oezbekistan |
| `VEB` | Venezuela Bolivares |
| `VND` | Vietnam Dong |
| `VUV` | Vanuatu Vatu |
| `WST` | Samoa Tala |
| `XAF` | Communaut?? Financi??re Afriaine Francs B |
| `XAG` | Zilveren ounces |
| `XAU` | Goud |
| `XCD` | Oost-Caribische dollars |
| `XDR` | Speciale uitgave bij het Internationaal Monetair Fonds |
| `XOF` | Communaut?? Financi??re Afriaine Francs B |
| `XPD` | Palladium Ounces |
| `XPF` | Comptoirs Fran??ais du Pacifique Francs |
| `XPT` | Platinum Ounces |
| `YER` | Jemen Rials |
| `ZAR` | Zuid-Afrika Rand |
| `ZMK` | Zambia Kwacha |
| `ZWD` | Zimbabwe Dollar |
