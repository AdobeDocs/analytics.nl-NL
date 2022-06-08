---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 8666c32ffe907ad486778fa382404807459be03c
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 2%

---

# Huidige Adobe Analytics-releaseopmerkingen (mei 2022)

**Laatste update**: 8 juni 2022

## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)

## Nieuwe functies in Adobe Analytics

| Functie | Beschrijving | [Doeldatum](releases.md) |
| ----------- | ---------- | ------- |
| De afmetingen en metriek van de levenscyclus populeren via Experience Edge | Gegevens over de mobiele levenscyclus die via Experience Edge worden verzonden, worden nu weergegeven in Analytics-rapportage. Raadpleeg de documentatie voor meer informatie over de gegevens over de levenscyclus die via Experience Edge worden verzameld en over de manier waarop deze overeenkomen met de bestaande levenscyclusrapportage. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) | 27 mei 2022 |

{style=&quot;table-layout:auto&quot;}

### Oplossingen in Adobe Analytics

(Oplossingen voor meerdere klanten)

N.v.t.

### Extra correcties in Adobe Analytics

(Oplossingen voor individuele klanten)

AN-274429; AN-279640; AN-280918; AN-280945; AN-282884; AN-283565; AN-284785; AN-284814; AN-284854; AN-284989; AN-285244; AN-285253; AN-285432; AN-285528; AN-285535; AN-285710; AN-286255; AN-286340; AN-286434; AN-286454; AN-286630; AN-286716; AN-286854; AN-286911

### Belangrijke kennisgevingen voor Adobe Analytics-beheerders

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| Geplande rapporten onderbreken in rapporten en analyses | 8 juni 2022 | Op 21 april 2022 hebben we aangekondigd dat verschillende specifieke kenmerken van de geplande rapporten zullen worden vervangen ter voorbereiding van de eerder aangekondigde [einde van levensduur voor rapporten en analyses](https://express.adobe.com/page/6WnF8JK6IRDhf/). Deze functies omvatten de mogelijkheid om nieuwe rapporten en nieuwe gegevensextracten te plannen.<p>In reactie op verzoeken van klanten die een extensie willen aanvragen en om de overgang van Reports and Analytics te vergemakkelijken, hebben we besloten de toegang tot deze functies te verlengen tot **31 jan. 2023**. Houd er rekening mee dat de vervaltijden voor zowel rapporten als gegevensextracten beperkt blijven tot negen maanden. aan het einde van deze periode wordt de levering van rapporten en gegevensuittreksels gepauzeerd , tenzij het schema opnieuw wordt geactiveerd . <p>Deze functies zijn verouderd op 31 januari 2023. Hiervoor moet u de geplande rapportage migreren naar een van de andere mechanismen waarover u in Adobe Analytics beschikt. Neem voor aanvullende vragen of ondersteuning contact op met de klantenservice van Adobe. |
| Geplande taken pauzeren in Report Builder | 8 juni 2022 | Op 21 april 2022 hebben we wijzigingen doorgevoerd in de geplande taken in Report Builder als onderdeel van onze inspanningen om de prestaties en prestaties te optimaliseren. Deze wijzigingen omvatten het verwijderen van de mogelijkheid om geplande leveringen &#39;end na x occurrences&#39; te laten beëindigen. In antwoord op verschillende verzoeken van klanten die meer tijd zoeken om alternatieven te onderzoeken en te implementeren, hebben we besloten deze optie op beperkte wijze te herstellen tot **31 jan. 2023**.<p>U kunt Report Builder-taken per uur blijven plannen en deze na maximaal 99 exemplaren laten beëindigen. De terugdraaiing geldt alleen voor uurwerk. het &quot; einde na x &quot; komt niet voor alle andere leveringsintervallen ( dagelijks , wekelijks , maandelijks en jaarlijks ) . Deze optie wordt afgekeurd op 31 januari 2023. Neem voor meer vragen of ondersteuning contact op met de klantenservice van Adobe. |
| **SFTP-upgrade** | 9 mei 2022 | Eerder, hadden wij meegedeeld dat Adobe zijn Secure File Transfer Protocol (SFTP) diensten in mei 2022 zou bevorderen om betere veiligheid voor dossieroverdracht te verstrekken. We hebben deze upgrade uitgesteld naar de **zomer 2022**. Wanneer deze wijziging plaatsvindt, worden bepaalde SFTP-clientconfiguraties niet meer ondersteund. Dit is alleen van invloed op gegevens die via SFTP naar Adobe Analytics worden verzonden of van worden opgehaald. Dit heeft geen invloed op het FTP-protocol. Om onderbreking van de dienst te vermijden, gelieve ervoor te zorgen dat uw cliënten SFTP (code, hulpmiddelen, de diensten) in overeenstemming met de gedetailleerde veranderingen zijn [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html). |
| **Bijwerken naar voor bepaalde klanten ondersteunde versleutelingsmethoden voor browsers** | 28 maart 2022 | Adobe biedt twee cipher veiligheidsniveaus aan om aan verschillende klantenbehoeften voor veiligheid op de inzameling van gegevens van eerste partij te voldoen. Aan **23 juni 2022** ondersteuning wordt verwijderd voor bepaalde HTTPS-versleutelingsalgoritmen, ook wel &#39;ciphers&#39; genoemd, voor klanten met hun beveiligingsniveau ingesteld op &#39;High&#39;. Dit betekent dat sommige oudere besturingssystemen geen gegevens meer naar Analytics kunnen verzenden omdat deze geen ondersteuning bieden voor moderne versleutelingsmethoden. Klanten die de standaardinstellingen voor standaardcursorbeveiliging gebruiken, worden niet beïnvloed. Er is al rechtstreeks contact opgenomen met alle klanten die momenteel gebruikmaken van de instelling &quot;Hoog&quot;. Hier vindt u een gedetailleerde lijst van de ciphers die door deze wijziging worden beïnvloed. |
| **2022 ISO-regioupdates** | 11 maart 2021 | Adobe is van plan 2022 ISO-regioupdates uit te voeren op **10 juni 2022**. Verwacht dat er na deze release kleine geo-informatie wordt bijgewerkt. |
| **EOL voor[!DNL Reports & Analytics]** | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de technologienormen van Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

{style=&quot;table-layout:auto&quot;}

### AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.22.4) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).

