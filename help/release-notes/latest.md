---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: c083c9d62d71dfd2d8a6360f24d8cc40f18f427d
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 2%

---

# Opmerkingen bij de huidige Adobe Analytics-release (juni 2022)

**Laatste update**: 16 juni 2022

## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)

## Nieuwe functies in Adobe Analytics

| Functie | Beschrijving | [Doeldatum](releases.md) |
| ----------- | ---------- | ------- |
| **Nieuwe interface voor stroomvisualisatie** | Biedt extra functionaliteit voor onze stroomvisualisatie om deze krachtiger en beter in staat te maken. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/flow/create-flow.html?lang=en) | Uitrol start op 15 juni 2022; GA uiterlijk 27 juni 2022 |
| **Annotaties delen op mobiele scorecards** | U kunt annotaties weergeven die zijn gemaakt in Workspace, in Mobiele Scorecards. Hierdoor kunt u contextuele gegevensnuances en inzichten over uw organisatie en campagnes rechtstreeks delen binnen Mobile Scorecard-projecten, die kunnen worden weergegeven in de mobiele app Analytics dashboards. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/annotations/mobile-annotations.html?lang=en) | 15 juni 2022 |
| **Ondersteuning voor productsyntaxisversie van Merchandising Variables met Edge Collection** | U kunt nu de variabelen voor het wijzigen van de handel instellen met behulp van het equivalent van de productsyntaxis door de relevante XDM-velden in te stellen. Zie [productvariabele](../implement/vars/page-vars/products.md) voor meer informatie de syntaxis van SDK van het Web met `products` variabele, en [Variabeletoewijzing analyseren in Adobe Experience Edge](../implement/aep-edge/variable-mapping.md) voor een volledige lijst van beschikbare variabelen. | 15 juni 2022 |
| **De afmetingen en metriek van de levenscyclus populeren via Experience Edge** | Gegevens over de mobiele levenscyclus die via Experience Edge worden verzonden, worden nu weergegeven in Analytics-rapportage. Zie de documentatie voor meer informatie over welke XDM-velden zijn toegewezen aan bestaande rapportage over de mobiele levenscyclus. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) | 27 mei 2022 |
| **Verwerkingsregels voor mobiele services die beschikbaar zijn in de verwerkingsregels voor Analytics** | De einddatum van de Adobe Mobile Services is 31 december 2022. Bestaande verwerkingsregels die zijn gemaakt of gegenereerd door Adobe Mobile Services, migreren automatisch naar Adobe Analytics-verwerkingsregels waar u deze kunt bewerken en beheren. Ze kunnen wel worden weergegeven, maar kunnen niet meer worden bewerkt in Mobiele services totdat het product op zonsondergang staat. Neem voor aanvullende vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](https://experienceleague.adobe.com/docs/mobile-services/using/eol.html?lang=en) | 15 juni 2022 |
| **Classificatiesets - fase 1** | Deze gefaseerde release van een nieuwe gebruikerservaring voor classificaties verbetert de zichtbaarheid van classificatiegegevens die eigendom zijn van klanten aanzienlijk. Zie [Classificatiesets](../components/classifications/sets/overview.md) voor meer informatie . | Beperkte tests starten 15 juni 2022, algemene beschikbaarheid geschat begin 2023 |

{style=&quot;table-layout:auto&quot;}

### Oplossingen in Adobe Analytics

AN-251686; AN-283542; AN-286572; AN-286945; AN-286784; AN-286944; AN-287012; AN-287319; AN-287333; AN-287348; AN-287429; AN-288238; AN-288281; AN-288660; AN-288769; AN-288798; AN-288871; AN-288872; AN-288941; AN-288951; AN-288952; AN-288956; AN-289062; AN-289340; AN-289346; AN-289488; AN-289562; AN-289580; AN-289861; AN-289892;

### Belangrijke kennisgevingen voor Adobe Analytics-beheerders

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Geplande rapporten onderbreken in rapporten en analyses** | 8 juni 2022 | Op 21 april 2022 hebben we aangekondigd dat verschillende functies die specifiek zijn voor geplande rapporten, zullen worden vervangen ter voorbereiding op het eerder aangekondigde einde van de levensduur van Reports &amp; Analytics. Deze functies omvatten de mogelijkheid om nieuwe rapporten en nieuwe gegevensextracten te plannen.<p>In reactie op verzoeken van klanten die een extensie willen aanvragen en om de overgang van Reports and Analytics te vergemakkelijken, hebben we besloten de toegang tot deze functies te verlengen tot **31 jan. 2023**. Houd er rekening mee dat de vervaltijden voor zowel rapporten als gegevensextracten beperkt blijven tot negen maanden. aan het einde van deze periode wordt de levering van rapporten en gegevensuittreksels gepauzeerd , tenzij het schema opnieuw wordt geactiveerd .<p>Om nog maar eens te herhalen: deze functies zijn verouderd op 31 januari 2023. Voor deze datum moet u de geplande rapportage migreren naar een van de andere methoden die beschikbaar zijn in Adobe Analytics. Neem voor aanvullende vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Geplande taken pauzeren in Report Builder** | 8 juni 2022 | Op 21 april 2022 hebben we wijzigingen doorgevoerd in de geplande taken in Report Builder als onderdeel van onze inspanningen om de prestaties en prestaties te optimaliseren. Deze wijzigingen omvatten het verwijderen van de mogelijkheid om geplande leveringen &#39;end na x occurrences&#39; te laten beëindigen. In antwoord op verschillende verzoeken van klanten die meer tijd zoeken om alternatieven te onderzoeken en te implementeren, hebben we besloten deze optie op beperkte wijze te herstellen tot **31 jan. 2023**.<p>U kunt Report Builder-taken per uur blijven plannen en deze na maximaal 99 exemplaren laten beëindigen. De terugdraaiing geldt alleen voor uurwerk. het &quot; einde na x &quot; komt niet voor alle andere leveringsintervallen ( dagelijks , wekelijks , maandelijks en jaarlijks ) . Deze optie wordt afgekeurd op 31 januari 2023. Neem voor meer vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| **SFTP-upgrade** | 9 mei 2022 | Eerder, hadden wij meegedeeld dat Adobe zijn Secure File Transfer Protocol (SFTP) diensten in mei 2022 zou bevorderen om betere veiligheid voor dossieroverdracht te verstrekken. We hebben deze upgrade uitgesteld naar de **zomer 2022**. Wanneer deze wijziging plaatsvindt, worden bepaalde SFTP-clientconfiguraties niet meer ondersteund. Dit is alleen van invloed op gegevens die via SFTP naar Adobe Analytics worden verzonden of van worden opgehaald. Dit heeft geen invloed op het FTP-protocol. Om onderbreking van de dienst te vermijden, gelieve ervoor te zorgen dat uw cliënten SFTP (code, hulpmiddelen, de diensten) in overeenstemming met de gedetailleerde veranderingen zijn [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html). |
| **Bijwerken naar voor bepaalde klanten ondersteunde versleutelingsmethoden voor browsers** | 28 maart 2022 | Adobe biedt twee cipher veiligheidsniveaus aan om aan verschillende klantenbehoeften voor veiligheid op de inzameling van gegevens van eerste partij te voldoen. Aan **23 juni 2022** ondersteuning wordt verwijderd voor bepaalde HTTPS-versleutelingsalgoritmen, ook wel &#39;ciphers&#39; genoemd, voor klanten met hun beveiligingsniveau ingesteld op &#39;High&#39;. Dit betekent dat sommige oudere besturingssystemen geen gegevens meer naar Analytics kunnen verzenden omdat deze geen ondersteuning bieden voor moderne versleutelingsmethoden. Klanten die de standaardinstellingen voor standaardcursorbeveiliging gebruiken, worden niet beïnvloed. Er is al rechtstreeks contact opgenomen met alle klanten die momenteel gebruikmaken van de instelling &quot;Hoog&quot;. Een gedetailleerde lijst van de cifers waarop dit betrekking heeft |
| **2022 ISO-regioupdates** | 11 maart 2021 | Adobe heeft 2022 ISO-regioupdates uitgevoerd op **10 juni 2022**. Verwacht dat er na deze release kleine geo-informatie wordt bijgewerkt. |
| **EOL voor[!DNL Reports & Analytics]** | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de technologienormen van Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

{style=&quot;table-layout:auto&quot;}

### AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.22.4) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).

