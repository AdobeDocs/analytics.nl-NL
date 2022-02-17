---
description: Beschrijft hoe te om doelvalutacodes voor multi-muntsteun te bepalen om te werken.
title: Ondersteuning voor meerdere valuta's
feature: Analytics Basics
exl-id: b67f459c-0636-4eac-af52-51846bb583b5
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 0%

---

# Ondersteuning voor meerdere valuta&#39;s

In dit document wordt beschreven hoe u doelvalutacodes voor ondersteuning in meerdere valuta&#39;s definieert.

Doelvalutacodes worden op drie niveaus gedefinieerd:

## Paginaniveau

U kunt een JavaScript-variabele voor de doelvaluta instellen op paginaniveau. De eigenaar van de site stelt deze variabele in met de toepasselijke drieletterige ISO 4217-valutacode (zoals hieronder in dit document wordt vermeld). Als de [currencyCode](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/currencycode.html) De variabele wordt niet op dit niveau ingesteld, de standaardvaluta is dezelfde als die in de rapportsuite is opgegeven. Als de variabele op paginaniveau met de variabele in de rapportreeks wordt gespecificeerd in conflict is, zal de variabele in de rapportreeks belangrijkheid nemen.


## Niveau van rapportsuite

De **basisvaluta** wordt opgegeven wanneer [maken, rapportsuites](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/new-report-suite/new-report-suite.html). Dit is de standaardinstelling voor valuta en heeft voorrang op valutacodes die op paginaniveau zijn ingesteld. Als een rapportsuite orders bevat die Amerikaanse dollars, Euro en Britse Pounds accepteren en de rapportensuite een standaardvalutacode heeft ingesteld op US Dollars, vertaalt de back-end database alle transacties naar US Dollars.

Marketingrapporten gebruiken de wisselkoers op het moment dat de afbeeldingsaanvraag plaatsvindt om de valutanummers op paginaniveau om te zetten in de standaardwaarden van de rapportsuite. Rapportagesuites gebruiken &quot;US Dollars&quot; als de standaardvaluta.


## Rapportniveau

Gebruikers kunnen de standaard gerapporteerde valuta voor gebruikersaanmelding instellen. Dit is toegankelijk via de **Weergaveopties**  koppeling in een omzettingsrapport. Marketingrapporten gebruiken de wisselkoers op het moment dat het rapport wordt uitgevoerd om rapport-suite valutawaarden om te zetten in op rapporten gebaseerde valutawaarden.

## Ondersteunde valutacodes (ISO 4217)

Analytics biedt momenteel ondersteuning voor de volgende valutatypen voor conversietransacties:


&quot;AFA&quot; Afghanistan Afghanistan (AFA)

AFN Afghanistan Afghanistan (AFN)

&quot;ALL&quot; Albanië Leke (ALL)

&quot;DZD&quot; Algerije Dinars (DZD)

&quot;AOA&quot; Angola Kwanza (AOA)

&quot;ARS&quot; Argentina Pesos (ARS)

&quot;AMD&quot; Armenia Drams (AMD)

&quot;AWG&quot; Aruba Guilders (AWG)

&#39;AUD&#39; Australia Dollars (AUD)

&quot;AZM&quot; Azerbeidzjan Manats (AZM)

&quot;AZN&quot; Azerbeidzjan New Manats (AZN)

&quot;BSD&quot; Bahamas Dollars (BSD)

BHD Bahrain Dinars (BHD)

BDT Bangladesh Taka (BDT)

&quot;BBD&quot; Barbados Dollars (BBD)

&quot;BYR&quot; Belarus Rubles (BYR)

BZD Belize Dollars (BZD)

&quot;BMD&quot; Bermuda Dollars (BMD)

&#39;BTN&#39; Bhutan Ngultrum (BTN)

&quot;BOB&quot; Bolivia Bolivianos (BOB)

&quot;BAM&quot; Bosnië en Herzegovina Converteerbare Marka (BAM)

&quot;BWP&quot; Botswana Pulas (BWP)

&quot;BRL&quot; Brazilië Reais (BRL)

&quot;BND&quot; Brunei Dollars (BND)

&quot;BGN&quot; Bulgarije Leva (BGN)

&quot;BIF&quot; Burundi Francs (BIF)

&quot;KHR&quot; Cambodia Riels (KHR)

&#39;CAD&#39; Canada Dollars (CAD)

&quot;CVE&quot; Kaapverdië Escudos (CVE)

&#39;KYD&#39;-dollars op de Caymaneilanden (KYD)

&quot;CLP&quot; Chili Pesos (CLP)

&#39;CNY&#39; China Yuan Renminbi (CNY)

&quot;COP&quot; Colombia Pesos (COP)

&quot;XOF&quot; Communauté Financière Afriaine Francs BCEAO (XOF)

&quot;XAF&quot; Communauté Financière Afriaine Francs BEAC (XAF)

&quot;KMF&quot; Comoros Francs (KMF)

&quot;XPF&quot; Comptoirs Français du Pacifique Francs (XPF)

&#39;CDF&#39; Congo/Kinshasa Francs (CDF)

&quot;CRC&quot; Costa Rica Colones (CRC)

&quot;HRK&quot; Kroatië Kuna (HRK)

&quot;CUC&quot; Cuba Convertible Pesos (CUC)

CUP Cuba Pesos (CUP)

&quot;CYP&quot; Cyprus Pounds (CYP)

&quot;CZK&quot; Tsjechië Koruny (CZK)

&quot;DKK&quot; Denemarken Kroner (DKK)

&quot;DJF&quot; Djibouti Francs (DJF)

&quot;DOP&quot; Dominicaanse Republiek Pesos (DOP)

&#39;XCD&#39; Oost-Caribische dollars (XCD)

&quot;EGP&quot; Egyptische grenzenaars (EGP)

&quot;SVC&quot; El Salvador Colones (SVC)

&quot;ERN&quot; Eritrea Nakfa (ERN)

&#39;XBT&#39; ERR (XBT)

&quot;EEK&quot; Estland Krooni (EEK)

&quot;ETB&quot; Ethiopia Birr (ETB)

&quot;EUR&quot; (EUR)

&quot;FKP&quot; Falklandeilanden (FKP)

FJD Fiji Dollars (FJD)

&quot;GMD&quot; Gambia Dalasi (GMD)

&quot;GEL&quot; Georgia Lari (GEL)

&quot;GHC&quot; Ghana Cedis (GHC)

&quot;GHS&quot; Ghana Cedis (GHS)

GIP Gibraltar Pounds (GIP)

&#39;XAU&#39; Gold Ounces (XAU)

&#39;GTQ&#39; Guatemala Quetzales (GTQ)

&#39;GGP&#39; Guernsey Pounds (GGP)

&quot;GNF&quot; Guinee-Francs (GNF)

&#39;GYD&#39; Guyana Dollars (GYD)

&#39;HTG&#39; Haïtiaanse geuren (HTG)

&quot;HNL&quot; Honduras Lempiras (HNL)

&quot;HKD&quot; Hongkongse dollars (HKD)

&quot;HUF&quot; Hongarije Forint (HUF)

&quot;ISK&quot; IJslandse kroon (ISK)

&quot;INR&quot; India Rupes (INR)

&quot;IDR&quot; Indonesia Rupiahs (IDR)

&quot;XDR&quot; Speciale trekkingsrechten van het Internationaal Monetair Fonds (XDR)

IRR Iran Rials (IRR)

&#39;IQD&#39; Irak-dinars (IQD)

&#39;IMP&#39; Isle of Man Pounds (IMP)

&#39;ILS&#39; Israel New Shekels (ILS)

&quot;JMD&quot; Jamaica Dollars (JMD)

&#39;JPY&#39; Japan Yen (JPY)

&#39;JEP&#39; Jersey Pounds (JEP)

&#39;JOD&#39; Jordan Dinars (JOD)

&quot;KZT&quot; Kazachstan Tenge (KZT)

KES Kenya Shillings (KES)

&quot;KWD&quot; Koeweitse dinars (KWD)

&quot;KGS&quot; Kirgizstan (KGS)

&quot;LAK&quot; Laos Kips (LAK)

&quot;LVL&quot; Letland Lati (LVL)

&#39;LBP&#39; Libanon-grenzen (LBP)

&quot;LSL&quot; Lesotho Maloti (LSL)

&#39;LRD&#39; Liberia Dollars (LRD)

&quot;LYD&quot; Libië Dinars (LYD)

&quot;LTL&quot; Litouwen Litai (LTL)

&quot;MOP&quot; Macau Patacas (MOP)

&quot;MKD&quot; Macedonië Denars (MKD)

&quot;MGA&quot; Madagaskar Ariary (MGA)

&quot;MWK&quot; Malawi Kwachas (MWK)

&quot;MYR&quot; Maleisië Ringgits (MYR)

&quot;MVR&quot; Maldiven Rufiyaa (MVR)

&quot;MTL&quot; Malta Liri (MTL)

&quot;MRO&quot; Mauritania Ouguiyas (MRO)

&quot;MUR&quot; Mauritius Rupes (MUR)

&#39;MXN&#39; Mexico Pesos (MXN)

&quot;MDL&quot; Moldavië Lei (MDL)

&quot;MNT&quot; Mongolia Tugriks (MNT)

&quot;MAD&quot; Marokko Dirhams (MAD)

&quot;MZN&quot; Mozambique Meticais (MZN)

&quot;MZM&quot; Mozambique Meticais (MZM)

&quot;MMK&quot; Myanmar Kyats (MMK)

&#39;NAD&#39; Namibië Dollars (NAD)

&quot;NPR&quot; Nepal Rupes (NPR)

&quot;ANG&quot; Netherlands Antilles Guilders (ANG)

&quot;NZD&quot; New Zealand Dollars (NZD)

&#39;NIO&#39; Nicaragua Cordobas (NIO)

&#39;NGN&#39; Nigeria Nairas (NGN)

&#39;KPW&#39; Noord-Korea Won (KPW)

NOK Noorwegen Kroner (NOK)

Oman Rials (OMR)

&quot;PKR&quot; Pakistan Rupes (PKR)

&#39;XPD&#39;-palladium Ounces (XPD)

&#39;PAB&#39; Panama Balboas (PAB)

&quot;PGK&quot; Papoea-Nieuw-Guinea Kina (PGK)

&#39;PYG&#39; Paraguay Guarantee (PYG)

&quot;PEN&quot; Peru Nuevos Soles (PEN)

PHP Filipijnen Pesos (PHP)

&#39;XPT&#39; Platinum Ounces (XPT)

&quot;PLN&quot; Polen Zlotych (PLN)

QAR&#39; Qatar Riyals (QAR)

&quot;ROL&quot; Roemenië Lei (ROL)

&quot;RON&quot; Roemenië New Lei (RON)

RUB Rusland Rubles (RUB)

RUR Rusland Rubles (RUR)

RWF Rwanda Francs (RWF)

&quot;SHP&quot; Saint Helena Pounds (SHP)

&#39;WST&#39; Samoa Tala (WST)

&quot;STD&quot; São Tomé en Principe Dobras (STD)

&quot;SAR&quot; Riyals (SAR) uit Saoedi-Arabië

&quot;SPL&quot; Seborga Luigini (SPL)

&quot;RSD&quot; Servië Dinars (RSD)

&quot;CSD&quot; Servië Dinars (CSD)

&quot;SCR&quot; Seychellen Rupes (SCR)

&quot;SLL&quot; Sierra Leone Leones (SLL)

&#39;XAG&#39; Silver Ounces (XAG)

&quot;SGD&quot; Singapore Dollars (SGD)

&quot;SKK&quot; Slovakia Koruny (SKK)

&quot;SIT&quot; Slovenië Tolars (SIT)

&quot;SBD&quot; Salomonseilanden Dollars (SBD)

&quot;SOS&quot; Somalië Shillings (SOS)

&quot;ZAR&quot; Zuid-Afrika Rand (ZAR)

&quot;KRW&quot; Zuid-Korea Won (KRW)

&quot;LKR&quot; Sri Lanka Rupes (LKR)

&#39;SDD&#39; Soedandinars (SDD)

&quot;SDG&quot; Soedangrenzen (SDG)

&#39;SRD&#39; Suriname Dollars (SRD)

&#39;SRG&#39; Suriname Guilders (SRG)

&quot;SZL&quot; Swaziland Emalangeni (SZL)

&quot;SEK&quot; Zweedse kroon (SEK)

CHF Zwitserland Francs (CHF)

&#39;SYP&#39; Syrië Pounds (SYP)

&#39;TWD&#39; Taiwan New Dollars (TWD)

TJS Tadzjikistan Somoni (TJS)

TZS Tanzania Shillings (TZS)

&#39;THB&#39; Thailand Baht (THB)

&#39;TOP&#39; Tonga Pa&#39;anga (BOVENKANT)

&#39;TTD&#39; Trinidad en Tobago Dollars (TTD)

&#39;TND&#39; Tunesische dinars (TND)

&quot;TRY&quot; Turkse lira (TRY)

&quot;TRL&quot; Turkije Liras (TRL)

TMM Turkmenistan Manats (TMM)

TMT Turkmenistan New Manats (TMT)

TVD Tuvalu Dollars (TVD)

&quot;UGX&quot; Oeganda Shillings (UGX)

&quot;UAH&quot; Ukraine Hryvnia (UAH)

&quot;AED&quot; Verenigde Arabische Emiraten Dirhams (AED)

&quot;GBP&quot; Britse Pounds (GBP)

&#39;USD&#39; geselecteerde Amerikaanse dollars (USD)

&#39;UYU&#39; Uruguay Pesos (UYU)

Oezbeekse topontmoetingen in Oezbekistan (UZS)

&quot;VUV&quot; Vanuatu Vatu (VUV)

&quot;VEB&quot; Venezuela Bolivares (VEB)

&quot;VEF&quot; Venezuela Bolivares Fuertes (VEF)

&#39;VND&#39; Vietnam Dong (VND)

&#39;JER&#39;-Jemenrialen (JER)

ZMK Zambia Kwacha (ZMK)

&quot;ZMW&quot; Zambia Kwacha (ZMW)

ZWD Zimbabwe Dollars (ZWD)


## Voorbeeld van AppMeasurement.js

De `currencyCode` kan globaal worden gedefinieerd in het bestand AppMeasurement.js. Als de currencyCode-variabele in dit bestand wordt gedefinieerd, wordt voor alle valutatransacties een uniforme valutacode gebruikt. In het onderstaande voorbeeld wordt Euros opgegeven als de `currencyCode` in de `CONFIG SECTION` van het bestand AppMeasurement.js. Alle aankoopgebeurtenissen worden geïnterpreteerd door rapportage als &quot;Euro&quot; - transacties.

```
/************************** CONFIG SECTION **************************/ 
/* You may add or alter any code config here. */ 
s.account="devnow"
s.currencyCode="EUR"
s.trackInlineStats=true 
s.linkLeaveQueryString=false 
s.linkTrackVars="None" 
s.linkTrackEvents="None" 
***
    
```

## Aanvullende opmerkingen bij de implementatie

* Hoewel valutacodes tussen pagina&#39;s kunnen veranderen, moeten alle conversielijnitems die op een bepaald paginaverzoek zijn gedefinieerd dezelfde valuta gebruiken (bijvoorbeeld, kunt u Euro, British Pounds en US Dollars niet op dezelfde paginaweergave hebben gedefinieerd). Als u geen valutawissel wilt uitvoeren, moet u de waarde van currencyCode leeg laten. Hierdoor worden de verzonden waarden rechtstreeks doorgegeven aan rapporten zonder conversie.

* Als een ongeldige currencyCode wordt ingesteld (een waarde die niet voorkomt in de lijst met ondersteunde valutacodes), wordt de gehele hit uitgesloten en worden voor die transactie geen gegevens verzameld. Voor het instellen `currencyCode` in productie, gebruik een reeks van het testrapport om te verifiëren dat de gegevens worden verzameld en de valutaconversie correct is.

* Valuta&#39;s die geen punt (.) gebruiken omdat het scheidingsteken moet worden gewijzigd om de punt te gebruiken in plaats van het typische scheidingsteken. Zweedse kroon, die bijvoorbeeld een komma (,) gebruikt, moet worden gewijzigd om een punt in plaats van een komma te gebruiken. Analytics gebruikt de komma om waarden te scheiden en de gegevens worden niet correct doorgegeven. De periode geeft de waarde correct door aan rapporten.
