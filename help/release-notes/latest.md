---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 3243780b2bb1f7507dc5815f71c448a8be7f62cd
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 3%

---

# Huidige Adobe Analytics-releaseopmerkingen (mei 2022)

**Laatste update**: 17 mei 2022

## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)

## Nieuwe functies in Adobe Analytics

| Functie | Beschrijving | [Doeldatum](releases.md) |
| ----------- | ---------- | ------- |
| De afmetingen en metriek van de levenscyclus populeren via Experience Edge | Veel gebeurtenissen in de levenscyclus worden nu automatisch toegewezen aan XDM-velden. Gebeurtenissen die niet automatisch worden toegewezen, kunnen naar Adobe worden verzonden via sleutelwaardeparen in vrije vorm. [Meer informatie - binnenkort beschikbaar] | 27 mei 2022 |

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
| **SFTP-upgrade** | 9 mei 2022 | Eerder, hadden wij meegedeeld dat Adobe zijn Secure File Transfer Protocol (SFTP) diensten in mei 2022 zou bevorderen om betere veiligheid voor dossieroverdracht te verstrekken. We hebben deze upgrade uitgesteld tot de zomer van 2022. Wanneer deze wijziging plaatsvindt, worden bepaalde SFTP-clientconfiguraties niet meer ondersteund. Dit is alleen van invloed op gegevens die via SFTP naar Adobe Analytics worden verzonden of van worden opgehaald. Dit heeft geen invloed op het FTP-protocol. Om onderbreking van de dienst te vermijden, gelieve ervoor te zorgen dat uw cliënten SFTP (code, hulpmiddelen, de diensten) in overeenstemming met de gedetailleerde veranderingen zijn [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html). |
| **CDA-machtiging (Cross-Device Analytics)** | 13 april 2022 | Effectief **1 mei 2022**, eventuele nieuwe implementaties van [CDA](/help/components/cda/overview.md) zijn beperkt tot een maximum van drie reeks IDs van het rapport (RSIDs) per klant. |
| **Wijzigen in hoe Adobe Analytics omgaat met A4T-gegevens die via Experience Edge zijn verzameld** | 31 maart 2022 | Op 7 maart 2022 veranderde Analytics hoe het sommige vraag die van de Rand van de Ervaring kwam behandelde die inhoud van het Doel voorgenomen voor Analytics voor het Rapport van het Doel (A4T) omvatten. Vanaf 7 maart worden alle hits met A4T-rapportinhoud gewijzigd, zodat ze niet worden behandeld als gebeurtenissen Paginaweergave of Koppeling. Starten **31 maart 2022** De logica is selectiever, zodat de standaardgebeurtenissen Paginaweergave en Klikken niet worden gewijzigd. Voorwaarts, zijn de enige gebeurtenissen die worden gewijzigd verpersoonlijking-slechts vraag die slechts A4T inhoud heeft. |
| **Bijwerken naar voor bepaalde klanten ondersteunde versleutelingsmethoden voor browsers** | 28 maart 2022 | Adobe biedt twee cipher veiligheidsniveaus aan om aan verschillende klantenbehoeften voor veiligheid op de inzameling van gegevens van eerste partij te voldoen. Aan **23 juni 2022** ondersteuning wordt verwijderd voor bepaalde HTTPS-versleutelingsalgoritmen, ook wel &#39;ciphers&#39; genoemd, voor klanten met hun beveiligingsniveau ingesteld op &#39;High&#39;. Dit betekent dat sommige oudere besturingssystemen geen gegevens meer naar Analytics kunnen verzenden omdat deze geen ondersteuning bieden voor moderne versleutelingsmethoden. Klanten die de standaardinstellingen voor standaardcursorbeveiliging gebruiken, worden niet beïnvloed. Er is al rechtstreeks contact opgenomen met alle klanten die momenteel gebruikmaken van de instelling &quot;Hoog&quot;. Hier vindt u een gedetailleerde lijst van de ciphers die door deze wijziging worden beïnvloed. |
| **Oudere geplande rapporten onderbreken** | 12 april 2022 | Effectief **20 april 2022**, is Adobe voornemens alle geplande rapporten met een aanmaakdatum van meer dan twee jaar (aangemaakt vóór 31 januari 2020) te pauzeren. Er worden geen rapporten of gegevens verwijderd. Alleen rapporten die ouder zijn dan twee jaar worden gepauzeerd en er worden geen aanvullende geplande rapporten verzonden. Meer informatie |
| **2022 ISO-regioupdates** | 11 maart 2021 | Adobe is van plan 2022 ISO-regioupdates uit te voeren op **10 juni 2022**. Verwacht dat er na deze release kleine geo-informatie wordt bijgewerkt. |
| **Oudere geplande Report Builder-taken pauzeren** | 12 april 2022 | Effectief **20 april 2022** Adobe is van plan alle geplande Report Builder-taken die meer dan twee jaar geleden zijn gemaakt, te pauzeren. Deze pauze is met name van toepassing op alle taken die vóór 31 januari 2020 zijn gemaakt. Er worden geen taken, werkboeken of gegevens verwijderd. Taken die ouder zijn dan twee jaar worden echter gepauzeerd en er worden geen extra geplande taken verzonden. Meer informatie |
| **Verlopen van de lijst van gewenste personen EOL-extensie voor verouderde integratie van Analytics OAuth/JWT** | 14 januari 2022 | Aan **25 mei 2022** de [Analytics 1.3 API, 1.4 SOAP API en Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) De extensie lijst van gewenste personen verloopt. Het werd aangeboden klanten te voorzien die erfenis gebruiken [!DNL Adobe Analytics] OAuth/JWT geloofsbrieven extra tijd om hun cliëntintegratie te migreren aan [Adobe IMS-referenties](https://developer.adobe.com/console). Deze vervaldatum beïnvloedt (maar is niet beperkt tot) [!DNL Adobe Analytics Livestream] en [!DNL Adobe Campaign] klanten die hun vereiste IMS-migratie niet hebben voltooid. Klanten die op dit moment verouderde [!DNL Analytics] OAuth/JWT-gebruikersgegevens via de extensie lijst van gewenste personen en die de migratie naar IMS-gegevens op 25 mei 2022 niet hebben voltooid, verliezen de toegang tot Adobe-services. Livestream-klanten kunnen naar deze [instructies](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) over het migreren van hun clienttoepassingen naar IMS-referenties. [!DNL Campaign] klanten kunnen hun Adobe account team bereiken over de upgrade naar de nieuwste versie van [!DNL Campaign]. |
| **EOL voor[!DNL Reports & Analytics]** | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de technologienormen van Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

{style=&quot;table-layout:auto&quot;}

### AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.22.4) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).

