---
description: Veldbeschrijvingen voor Algemene accountinstellingen van rapportsuite in Admin.
title: Algemene accountinstellingen
feature: Admin Tools
uuid: c1ab5c34-2c41-4d12-a706-0e760dff8a95
exl-id: f49babb2-8e26-4cc6-b264-b4d7be93f130
source-git-commit: af3bdcf3eedecc6b670e51dcb2f6980e75982077
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Algemene accountinstellingen

Veldbeschrijvingen voor de algemene accountinstellingen van een rapportsuite in Admin.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL General Account Settings]**

Deze montages bevatten het uitgeven opties voor de functionaliteit van de basisrapportreeks, zoals naam en tijdzone.

Hier volgt een video over het configureren van algemene accountinstellingen:

>[!VIDEO](https://video.tv.adobe.com/v/332330/?quality=12)

| Optie | Beschrijving |
|--- |--- |
| Titel site | Identificeert uw site. Geef elke rapportsuite een unieke titel voor de site. |
| Basis-URL | Geeft de hoofdwebsite van de rapportsuite aan. De basis-URL heeft geen invloed op het filteren van referenties. Gebruiken [interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md) in plaats daarvan. |
| Tijdzone | Bepaalt de datum en de tijd verbonden aan uw rapportgegevens.  Het veranderen van de tijdzone voor een levende rapportreeks leidt of tot een spiek of hiaat in rapportgegevens. Om de impact tot een minimum te beperken, raadt Adobe aan de tijdzones tijdens niet-piekuren te wijzigen om te voorkomen dat gegevens worden schuingetrokken.  Als u bijvoorbeeld de tijdzone van de rapportsuite wijzigt van Central naar Pacific om 15.00 uur, wordt de huidige tijd van de rapportsuite ingesteld op 13.00 uur. Omdat het melden reeds gegevens voor 1:00 uur heeft verzameld, tonen de rapporten een verkeerspiek tussen 1:00pm en 3:00pm.  Alternatief, als u de tijdzone van de rapportreeks van Centraal in Oost om 15:00pm verandert, wordt de huidige tijd van de rapportreeks 4:00pm. Rapporten geven geen gegevens weer tussen 15.00 en 16.00 uur op de dag van de tijdwijziging. |
| Standaardpagina | Als uw [!UICONTROL Most Popular Pages] rapport bevat URL&#39;s in plaats van paginanamen. Deze instelling voorkomt dat meerdere URL&#39;s dezelfde pagina vertegenwoordigen. De URL&#39;s `https://example.com` en `https://example.com/index.html` zijn doorgaans dezelfde pagina. U kunt standaardbestandsnamen verwijderen, zodat deze twee URL&#39;s beide worden weergegeven als `https://example.com`.  Als deze optie niet wordt opgegeven, worden de volgende bestandsnamen verwijderd uit de URL&#39;s: index.htm, index.html, index.cgi, index.asp, default.htm, default.cgi, default.asp, home.htm, home.html, home.cgi en home.asp.  Als u het verwijderen van bestandsnamen wilt uitschakelen, voert u een waarde in die nooit voorkomt in de URL&#39;s. |
| Vervang het laatste octet van IP adressen met 0 | Wanneer toegelaten, vervangt het laatste octet van IP adressen met nul. Dit gebeurt voordat geo-gerelateerde rapporten worden ingevuld en kan daarom van invloed zijn op de nauwkeurigheid van deze rapporten. |
| IP Obfuscatie | Zet IP adressen in niet-herkenbare koorden, hoofdzakelijk verwijderend hen uit de gegevensopslag van Adobe. Wanneer IP de Verduistering wordt toegelaten, worden de originele IP adressen permanent verloren. <br> **Opmerking**: De IP adressen worden overal in Analytics, met inbegrip van Data Warehouse verduisterd. Nochtans, wordt IP die in Doel plaatst gecontroleerd afzonderlijk, zodat heeft dit het plaatsen geen effect op Doel.<br> Als IP de verduistering wordt toegelaten, al nodig verwerking met inbegrip van IP het filtreren/uitsluiting, zowel worden de regels als de raadplegingen van de Geosegmentatie gedaan alvorens het IP adres wordt verduisterd. U hoeft niets te wijzigen wanneer u IP-verduistering inschakelt.<ul><li>Controleren **Uitgeschakeld** laat het IP adres in de gegevens.</li><li>Controleren **Obfuscate IP-adres** wijzigt het IP in twee dubbelepunten gevolgd door een hashwaarde (bijvoorbeeld `::1932023538`).</li><li>Controleren **IP-adres verwijderen** vervangt het IP adres met `::X.X.X.X` in de gegevens, na geo-lookup.</li></ul>**Opmerking**: voor deze instelling zijn mogelijk wijzigingen in de aangepaste instellingen vereist [bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) of [IP-uitsluitingen](/help/admin/admin/exclude-ip.md). |
| Opslag van transactie-id | Hiermee kunt u [Transactie-id](/help/import/data-sources/transactionid.md) gegevensbronnen. |
| Data Warehouse inschakelen | Hiermee schakelt u de gebruikersinterface van de Data Warehouse in via Analytics > Tools > Data Warehouse. |
| Zip-optie | Hier kunt u de postcode opgeven in plaats van wat onze IP-opzoekopdracht van de geo oplevert. |
| Ondersteuning voor multibyte-tekens | Bij multibyte-tekenondersteuning worden tekens in de rapportsuite opgeslagen met UTF-8. Na ontvangst zet het systeem gegevens van de tekenset van uw webpagina om in de tekenset UTF-8, zodat u elke taal in uw marketingrapporten kunt gebruiken. Neem contact op met uw Adobe-accountteam of de klantenservice om de multibyte-tekenondersteuning voor een bestaande rapportsuite te wijzigen. |
| geactiveerd | Geeft aan of deze rapportsuite is geactiveerd of niet. |
| Basisvaluta | Hiermee kunt u de basis opgeven [valuta](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/currencycode.html) voor dit rapportpakket. |
| Organisatie-id | De id die is gekoppeld aan uw Experience Cloud-bedrijf dat u hebt ingericht. Deze id is een alfanumerieke tekenreeks van 24 tekens, gevolgd door (en moet bevatten) @AdobeOrg. |