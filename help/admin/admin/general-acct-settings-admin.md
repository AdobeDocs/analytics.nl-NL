---
description: Veldbeschrijvingen voor Algemene accountinstellingen van rapportsuite in Admin.
title: Algemene accountinstellingen
feature: Admin Tools
uuid: c1ab5c34-2c41-4d12-a706-0e760dff8a95
exl-id: f49babb2-8e26-4cc6-b264-b4d7be93f130
source-git-commit: f52623f4885063d080c95ef275808a3d051895e5
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# Algemene accountinstellingen

Veldbeschrijvingen voor de algemene accountinstellingen van een rapportsuite in Admin.

**[!UICONTROL Analytics]** >  **[!UICONTROL Admin]** >  **[!UICONTROL Report Suites]** >  **[!UICONTROL Edit Settings]** >  **[!UICONTROL General]** >  **[!UICONTROL General Account Settings]**

Deze montages bevatten het uitgeven opties voor de functionaliteit van de basisrapportreeks, zoals naam en tijdzone.

Hier volgt een video over het configureren van algemene accountinstellingen:

>[!VIDEO](https://video.tv.adobe.com/v/332330/?quality=12)

| Optie | Beschrijving |
|--- |--- |
| Titel site | Identificeert uw site. Geef elke rapportsuite een unieke titel voor de site. |
| Basis-URL | Geeft de hoofdwebsite van de rapportsuite aan. De basis-URL heeft geen invloed op het filteren van referenties. Gebruik in plaats hiervan [interne URL-filters](/help/admin/admin/internal-url-filter-admin.md). |
| Tijdzone | Bepaalt de datum en de tijd verbonden aan uw rapportgegevens.  Het veranderen van de tijdzone voor een levende rapportreeks leidt of tot een spiek of hiaat in rapportgegevens. Om de impact tot een minimum te beperken, raadt Adobe aan de tijdzones tijdens niet-piekuren te wijzigen om te voorkomen dat gegevens worden schuingetrokken.  Als u bijvoorbeeld de tijdzone van de rapportsuite wijzigt van Central naar Pacific om 15.00 uur, wordt de huidige tijd van de rapportsuite ingesteld op 13.00 uur. Omdat het melden reeds gegevens voor 1:00 uur heeft verzameld, tonen de rapporten een verkeerspiek tussen 1:00pm en 3:00pm.  Alternatief, als u de tijdzone van de rapportreeks van Centraal in Oost om 15:00pm verandert, wordt de huidige tijd van de rapportreeks 4:00pm. Rapporten geven geen gegevens weer tussen 15.00 en 16.00 uur op de dag van de tijdwijziging. |
| Standaardpagina | Als uw [!UICONTROL Most Popular Pages] rapport URLs eerder dan paginanamen bevat, verhindert dit het plaatsen veelvoudige URLs om de zelfde pagina te vertegenwoordigen. De URL&#39;s `https://example.com` en `https://example.com/index.html` zijn bijvoorbeeld doorgaans dezelfde pagina. U kunt standaardbestandsnamen verwijderen, zodat deze twee URL&#39;s beide worden weergegeven als `https://example.com`.  Indien leeg gelaten, worden de volgende bestandsnamen verwijderd uit de URL&#39;s:  index.htm, index.html, index.cgi, index.asp, default.htm, default.html, default.cgi, default.asp, home.htm, home.html, home.cgi en home.asp.  Als u het verwijderen van bestandsnamen wilt uitschakelen, voert u een waarde in die nooit voorkomt in de URL&#39;s. |
| Vervang het laatste octet van IP adressen met 0 | Het laatste octet verwijderen wordt gedaan alvorens om het even welke verwerking op de klap, met inbegrip van v????r IP filtreren/uitsluiting, alvorens beide regels te controleren, v????r Geosegmentation raadplegingen, enz. wordt gedaan. Als dusdanig, wordt het laatste octet vervangen met 0, en IP de uitsluitingsregels zouden moeten worden bijgewerkt om IP adressen met nul op het eind aan te passen. Overeenkomende * moet overeenkomen met 0. Bijvoorbeeld, wordt het IP adres 11.22.33.44 veranderd in 11.22.33.0. Geosegmentatiegegevens zullen niet zo precies zijn als wanneer het volledige IP adres wordt gebruikt. Meer in het bijzonder zal de nauwkeurigheid van de stad meer worden be??nvloed dan de nauwkeurigheid van het land of de regio. Zowel worden de regels van Bot als de regels van VISTA be??nvloed omdat het volledige IP adres niet aan hen beschikbaar is. Bovendien worden om het even welke verwerkingsregels die IP gebaseerd zijn, met inbegrip van de regels van het marketingkanaal en de regels van de rapportreeksverwerking, be??nvloed door dit het plaatsen. <br> **Opmerking**: Deze instelling wordt standaard ingeschakeld voor alle nieuwe rapportsuites die na januari 2019 in het London Data Center worden gemaakt, maar alleen als de instellingen voor die rapportsuites worden gekopieerd uit een sjabloon dat in de Admin Console wordt vermeld. De reeksen van het rapport waarvan de montages van andere rapportreeksen worden gedupliceerd zullen alle montages van de geselecteerde rapportreeks erven. |
| IP Obfuscatie | Zet IP adressen in niet-herkenbare koorden, hoofdzakelijk verwijderend hen uit de gegevensopslag van Adobe. Wanneer IP de Verduistering wordt toegelaten, worden de originele IP adressen permanent verloren. <br> **Opmerking**: De IP adressen worden overal in Analytics, met inbegrip van Data Warehouse verduisterd. Nochtans, wordt IP die in Doel plaatst gecontroleerd afzonderlijk, zodat heeft dit het plaatsen geen effect op Doel.<br> Als IP de verduistering wordt toegelaten, al nodig verwerking met inbegrip van IP het filtreren/uitsluiting, zowel worden de regels als de raadplegingen van de Geosegmentatie gedaan alvorens het IP adres wordt verduisterd. U hoeft niets te wijzigen wanneer u IP-verduistering inschakelt.<ul><li>Als u **Uitgeschakeld** inschakelt, blijft het IP-adres in de gegevens staan.</li><li>Als u **IP-adres verduisteren** inschakelt, verandert de IP in twee dubbele punten, gevolgd door een gehashte waarde (bijvoorbeeld `::1932023538`).</li><li>Als u **IP-adres verwijderen** inschakelt, wordt het IP-adres vervangen door `::X.X.X.X` in de gegevens, na geo-lookup.</li></ul>**Opmerking**: Deze instelling kan wijzigingen in aangepaste  [zowel ](/help/admin/admin/bot-removal/bot-rules.md) linialen als  [IP-uitsluitingen](/help/admin/admin/exclude-ip.md) vereisen. |
| Opslag van transactie-id | Hiermee kunt u [Transactie-id](/help/import/c-data-sources/c-datasrc-types/datasrc-transactionid.md) gegevensbronnen gebruiken. |
| Data Warehouse inschakelen | Hiermee schakelt u de gebruikersinterface van de Data Warehouse in via Analytics > Tools > Data Warehouse. |
| Zip-optie | Hier kunt u de postcode opgeven in plaats van wat onze IP-opzoekopdracht van de geo oplevert. |
| Ondersteuning voor multibyte-tekens | Bij multibyte-tekenondersteuning worden tekens in de rapportsuite opgeslagen met UTF-8. Na ontvangst zet het systeem gegevens van de tekenset van uw webpagina om in de tekenset UTF-8, zodat u elke taal in uw marketingrapporten kunt gebruiken. Neem contact op met uw accountmanager of de klantenservice om de multibyte-tekenondersteuning voor een bestaande rapportsuite te wijzigen. |
| Geactiveerd | Geeft aan of deze rapportsuite is geactiveerd of niet. |
| Basisvaluta | Hier kunt u de basis [currency](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/currencycode.html?lang=en) voor deze rapportsuite opgeven. |
| Organisatie-id | De id die is gekoppeld aan uw Experience Cloud-bedrijf dat u hebt ingericht. Deze id is een alfanumerieke tekenreeks van 24 tekens, gevolgd door (en moet bevatten) @AdobeOrg. |