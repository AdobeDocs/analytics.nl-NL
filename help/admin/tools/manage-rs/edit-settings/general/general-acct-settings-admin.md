---
description: Veldbeschrijvingen voor Algemene accountinstellingen van rapportsuite in Admin.
title: Algemene accountinstellingen
feature: Admin Tools
uuid: c1ab5c34-2c41-4d12-a706-0e760dff8a95
exl-id: f49babb2-8e26-4cc6-b264-b4d7be93f130
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Algemene accountinstellingen

Veldbeschrijvingen voor de algemene accountinstellingen van een rapportsuite in Admin.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL General Account Settings]**

Deze montages bevatten het uitgeven opties voor de functionaliteit van de basisrapportreeks, zoals naam en tijdzone.


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; het Vormen algemene rekeningsmontages &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/administration/manage-report-suites/configuring-general-account-settings){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

| Optie | Beschrijving |
|--- |--- |
| Titel site | Identificeert uw site. Geef elke rapportsuite een unieke titel voor de site. |
| Basis-URL | Geeft de hoofdwebsite van de rapportsuite aan. De basis-URL heeft geen invloed op het filteren van referenties. Gebruik [&#x200B; interne filters URL &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) in plaats daarvan. |
| Tijdzone | Bepaalt de datum en de tijd verbonden aan uw rapportgegevens.  Het veranderen van de tijdzone voor een levende rapportreeks leidt of tot een spiek of hiaat in rapportgegevens. Om de impact tot een minimum te beperken, raadt Adobe aan de tijdzones tijdens niet-piekuren te wijzigen om te voorkomen dat gegevens worden schuingetrokken.  Bijvoorbeeld, als u de tijdzone van de rapportreeks van Centraal in Stille Oceaan 3 :00pm verandert, wordt de huidige tijd van de rapportreeks 1 :00pm. Omdat het melden reeds gegevens voor het 1 :00 uur heeft verzameld, tonen de rapporten een verkeerspiek tussen 1 :00pm en 3 :00pm.  Alternatief, als u de tijdzone van de rapportreeks van Centraal in Oost bij 3 :00pm verandert, wordt de huidige tijd van de rapportreeks 4 :00pm. De vertoningen van rapporten geen gegevens tussen 3 :00pm en 4 :00pm op de dag van de tijdverandering. |
| Standaardpagina | Als uw [!UICONTROL Most Popular Pages] -rapport URL&#39;s bevat in plaats van paginanamen, voorkomt deze instelling dat meerdere URL&#39;s dezelfde pagina vertegenwoordigen. De URL&#39;s `https://example.com` en `https://example.com/index.html` zijn bijvoorbeeld doorgaans dezelfde pagina. U kunt standaardbestandsnamen verwijderen, zodat deze twee URL&#39;s beide worden weergegeven als `https://example.com` .  Als deze optie niet wordt opgegeven, worden de volgende bestandsnamen verwijderd uit de URL&#39;s: index.htm, index.html, index.cgi, index.asp, default.htm, default.cgi, default.asp, home.htm, home.html, home.cgi en home.asp.  Als u het verwijderen van bestandsnamen wilt uitschakelen, voert u een waarde in die nooit voorkomt in de URL&#39;s. |
| Vervang het laatste octet van IP adressen met 0 | Wanneer toegelaten, vervangt het laatste octet van IP adressen met nul. Dit gebeurt voordat geo-gerelateerde rapporten worden ingevuld en kan daarom van invloed zijn op de nauwkeurigheid van deze rapporten. |
| IP Obfuscatie | Zet IP adressen in niet-herkenbare koorden, hoofdzakelijk verwijderend hen uit de gegevensopslag van Adobe. Wanneer IP de Verduistering wordt toegelaten, worden de originele IP adressen permanent verloren. <br> **Nota**: De IP adressen zijn overal in Analytics, met inbegrip van Data Warehouse verduisterd. Nochtans, wordt IP die in Doel plaatst gecontroleerd afzonderlijk, zodat heeft dit het plaatsen geen effect op Doel.<br> Als IP de bemoeienis wordt toegelaten, al nodig verwerking met inbegrip van IP het filtreren/uitsluiting, zowel worden de regels als de raadplegingen van de Geosegmentatie gedaan alvorens het IP adres wordt verduisterd. U hoeft niets te wijzigen wanneer u IP-verduistering inschakelt.<ul><li>Het controleren **Gehandicapten** verlaat het IP adres in de gegevens.</li><li>Het controleren **verduisteren IP adres** verandert IP in twee dubbelepunten die door een gehakte waarde (b.v., `::1932023538`) worden gevolgd.</li><li>Het controleren **verwijdert IP adres** vervangt het IP adres met `::X.X.X.X` in de gegevens, na geo-raadpleging.</li></ul>**Nota**: Dit het plaatsen zou veranderingen in douane [&#x200B; bot regels &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md) of [&#x200B; IP uitsluitingen &#x200B;](/help/admin/tools/exclude-ip.md) kunnen vereisen.<br> **Nota**: De gegevens die gebruikend het Web SDK worden verzameld kunnen IP die obfuscatie hebben bij Edge Network door [&#x200B; worden toegepast de configuratie van de gegevensstroom &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#@advanced-options). Als IP de verduistering op Edge Network wordt toegepast, is het reeds verduisterd wanneer het Analytics bereikt. Deze verduistering beïnvloedt zowel regels als geo lookups. |
| Opslag van transactie-id | Laat u toe om [&#x200B; gegevensbronnen van identiteitskaart van de Transactie &#x200B;](/help/import/data-sources/transactionid.md) te gebruiken. |
| Data Warehouse inschakelen | Schakelt de gebruikersinterface van Data Warehouse in via Analytics > Tools > Data Warehouse. |
| Zip-optie | Hier kunt u de postcode opgeven in plaats van wat onze IP-opzoekopdracht van de geo oplevert. |
| Ondersteuning voor multibyte-tekens | Bij multibyte-tekenondersteuning worden tekens in de rapportsuite opgeslagen met UTF-8. Na ontvangst zet het systeem gegevens van de tekenset van uw webpagina om in de tekenset UTF-8, zodat u elke taal in uw marketingrapporten kunt gebruiken. Neem contact op met uw Adobe-accountteam of de klantenservice om de multibyte-tekenondersteuning voor een bestaande rapportsuite te wijzigen. |
| geactiveerd | Geeft aan of deze rapportsuite is geactiveerd of niet. |
| Basisvaluta | Laat u de basis [&#x200B; munt &#x200B;](/help/implement/vars/config-vars/currencycode.md) voor deze rapportreeks specificeren. |
| Organisatie-id | De id die aan uw Experience Cloud-bedrijf is gekoppeld. Deze id is een alfanumerieke tekenreeks van 24 tekens, gevolgd door (en moet bevatten) @AdobeOrg. |
