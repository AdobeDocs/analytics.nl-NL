---
description: Gegevensbronnen bieden twee extra manieren om gebeurtenissen te integreren die offline bij uw online gegevens optreden.
subtopic: Data sources
title: Transactie- en klantintegratie
topic-fix: Developer and implementation
feature: Data Sources
exl-id: d4e4388b-6449-4fef-a94d-01b3a52c2190
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 2%

---

# Transactie- en klantintegratie

Gegevensbronnen bieden twee extra manieren om gebeurtenissen te integreren die offline aan uw online gegevens voorkomen.

* [Opname van transactie-id inschakelen](/help/import/c-data-sources/datasrc-integrating-offline-data.md#section_30D6D47AEC0F4A36B87EBFE4C858F20C)
* [Transactieintegratie](/help/import/c-data-sources/datasrc-integrating-offline-data.md#section_B3F281CEFF9B47E9A07F9851D61D415D)
* [Klantenintegratie](/help/import/c-data-sources/datasrc-integrating-offline-data.md#section_9F4AAD710D2543BDA834090A98115FBF)

Deze integratie associeert off-line gegevens met een specifieke online transactie of met een online bezoeker.

## Opname van transactie-id inschakelen {#section_30D6D47AEC0F4A36B87EBFE4C858F20C}

De transactie-id kan worden in-/uitgeschakeld vanuit de gebruikersinterface, zonder betrokkenheid van ClientCare:

Ga naar **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL General Account Settings]**.

<!-- 

<p>When contacting Customer Care, be prepared to provide the following information: </p> 
<ul id="ul_C425C7A074484650AFCCF0425E8E3F47"> 
 <li id="li_7640C0C4DF0C49749A3C37E5461DC22F">Report Suite ID of the data source for which you need transaction ID recording enabled. <p>In Data Sources, the report suite ID is the first part of the login appended by a random number that identifies the specific data source that was set up. For example, <code> RSID-drmossdev5 Login-drmossdev5_0001343430</code>. </p> </li> 
 <li id="li_4FB0E3EC7BE94A2DBEE9063365A71C9C">The Transaction ID expiration window (described in <a href="/help/import/c-data-sources/datasrc-tid-visitor-profile.md"  > Transaction ID and Visitor Profiles</a>). By default this is 90 days, but it can be extended to up to 2 years. </li> 
</ul>

 -->

Als u wilt zien of Opname van transactie-id is ingeschakeld, navigeert u naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Data sources]**.

![](assets/transaction-ID-recording-active.png)

De [!UICONTROL Manage] geeft de status van Transactie ID-opname weer.

## Klantenintegratie {#section_9F4AAD710D2543BDA834090A98115FBF}

Klant-id&#39;s worden gebruikt om de offlineactiviteit van een klant op te geven en aan online activiteiten te koppelen. Deze dienen te worden gebruikt wanneer:

* Een klant-id wordt ingevuld in het gedeelte *`visitorID`* variabele.
* Er is geen aangewezen punt waar de klantenactiviteit zich off-line beweegt, zoals een voorloodsvoorlegging of een aankoop.

Om dit type van gegevensbron te vormen, zie [Bezoeker-id](/help/import/c-data-sources/c-datasrc-types/datasrc-visitorid.md)

## Transactieintegratie {#section_B3F281CEFF9B47E9A07F9851D61D415D}

Transactie-id&#39;s worden gebruikt om de status van een bezoeker op een bepaald tijdstip vast te leggen. Deze zouden moeten worden gebruikt wanneer er een punt in tijd is wanneer de klanten typisch hun ervaring van online aan off-line bewegen, zoals:

* Verzendt een lood voor een verkoper om de klant te contacteren.
* Maakt een online aankoop, die later in opslag zou kunnen zijn teruggekeerd.
* Hiermee koopt u een product waarvoor ze later mogelijk om ondersteuning vragen.

De klant is vaak anoniem wanneer hij of zij online naar offline gaat.

Gebeurtenissen van transactie-id zijn niet opgenomen in statistieken voor deelname aan het bezoek (die worden weergegeven in marketingrapporten). De reden hiervoor is dat de transactie-id-gegevens niet aan een bezoek zijn gekoppeld (omdat de offline gebeurtenis gewoonlijk geen deel uitmaakt van de online gebeurtenis), maar aan de bezoeker zijn gekoppeld.

Zie [Transactie-id](/help/import/c-data-sources/c-datasrc-types/datasrc-transactionid.md).
