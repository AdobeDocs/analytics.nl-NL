---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 533c323b8be651eca14a88641aa4a82705305297
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 3%

---

# Opmerkingen bij de huidige Adobe Analytics-release (maart 2022)

**Laatst bijgewerkt: 28 maart 2022**

* Voor opmerkingen bij de release van februari 2022 gaat u [hier](/help/release-notes/2022.md).
* Meer informatie over de nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html). De nieuwste zelfhulpdocumentatie, zelfstudies en cursussen over Experience League.

## Nieuwe functies in Adobe Analytics {#aa-features}

| Functie | Beschrijving | [Doeldatum](releases.md) |
| ----------- | ---------- | ------- |
| Annotaties in werkruimte | Met annotaties in Workspace kunt u op effectieve wijze contextuele gegevensnuances en inzichten aan uw organisatie meedelen. [Meer informatie](/help/analyze/analysis-workspace/components/annotations/overview.md) | De geleidelijke uitrol start op 23 maart 2022. Algemene beschikbaarheid: 11 april 2022 |
| Adobe Analytics-bestemmingspagina-updates | Updates van de landingspagina van de gezamenlijke werkruimte/Rapporten &amp; Analytics die de bruikbaarheid en het gemak van navigatie verbetert. [Meer informatie](/help/analyze/landing.md) | 1 april 2022 |
| [!UICONTROL Next item] of [!UICONTROL Previous item] Deelvenster Werkruimte | De [!UICONTROL Next or Previous item] kunt u zoeken naar items die een dimensie-item van uw keuze volgen of er vooraf aan gaan. Gebruik deze optie bijvoorbeeld als u de volgende of vorige pagina&#39;s naar een specifieke productpagina, een marketingkanaal of zelfs naar een apparaattype wilt bekijken. Dit deelvenster gaat verder dan oudere rapporten (verouderde rapporten), omdat u hiermee elke dimensie kunt bekijken en geen nieuwe implementatie nodig hebt om inzichten op te halen. | 1 april 2022 |
| [!UICONTROL Page Summary] Deelvenster Werkruimte | De [!UICONTROL Page Summary] biedt een diepgaande analyse van de pagina die u kiest. Het biedt dezelfde details als oudere rapporten en analyses [!UICONTROL Page Summary] verslag, nog veel meer. | 1 april 2022 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Adobe Analytics

* Probleem verholpen waarbij een fout is opgetreden bij het openen van Activity Map. (AN-267177)
* Probleem verholpen met onsuccesvolle overdracht van gebruikerselementen. (AN-279813)
* Problemen verholpen met het deelvenster A4T-werkruimte. (AN-281594; AN-282418)
* Probleem verholpen waarbij sommige gebruikers geen toegang hadden tot Adobe Analytics. (AN-282776)
* Oplossing voor problemen met enkele nieuw gemaakte rapportsuites die geen gegevens verzamelden. (AN-283114, AN-283311)
* Correctie van problemen met verkeerd verzonden e-mails met gegevensfeeds. (AN-280255; AN-282051)


### Extra correcties in Adobe Analytics

AN-256929; AN-270937; AN-272158; AN-275130; AN-277830; AN-278635; AN-279066; AN-279683; AN-279899; AN-280504; AN-280617; AN-280663; AN-281423; AN-281523; AN-281608; AN-281671; AN-281963; AN-282027; AN-282218; AN-282593; AN-282605; AN-282632; AN-282654; AN-282694; AN-282744; AN-282756; AN-282804; AN-282838; AN-282862; AN-282903; AN-282937; AN-282892; AN-283315; AN-283338; AN-283388; AN-283417; AN-283474; AN-283511; AN-283691, AN-283895; AN-283943; AN-283957; AN-284030; AN-284100; AN-284142; AN-284162

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| Bijwerken naar voor bepaalde klanten ondersteunde versleutelingsmethoden voor browsers | 28 maart 2022 | Adobe biedt twee cipher veiligheidsniveaus aan om aan verschillende klantenbehoeften voor veiligheid op de inzameling van gegevens van eerste partij te voldoen. Aan **23 juni 2022** wij zullen steun voor bepaalde encryptiealgoritmen HTTPS, die als ciphers worden bekend, voor klanten met hun veiligheidsniveau verwijderen dat aan &quot;Hoog&quot;wordt geplaatst. Dit betekent dat sommige oudere besturingssystemen geen gegevens meer naar Analytics kunnen verzenden omdat deze geen ondersteuning bieden voor moderne versleutelingsmethoden. Klanten die de standaardinstellingen voor standaardcursorbeveiliging gebruiken, worden niet beïnvloed. Er is al rechtstreeks contact opgenomen met alle klanten die momenteel gebruikmaken van de instelling &quot;Hoog&quot;. Een gedetailleerde lijst van de ciphers die door deze verandering worden beïnvloed is te vinden [hier](/help/technotes/rdc/encryption-algos.md). |
| Oudere geplande rapporten onderbreken | 11 maart 2022 | Effectief **15 april 2022**, is Adobe voornemens alle geplande rapporten met een aanmaakdatum van meer dan twee jaar (aangemaakt vóór 31 januari 2020) te pauzeren. Er worden geen rapporten of gegevens verwijderd. Alleen rapporten die ouder zijn dan twee jaar worden gepauzeerd en er worden geen aanvullende geplande rapporten verzonden. [Meer informatie](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| 2022 ISO-regioupdates | 11 maart 2021 | Adobe voert 2022 ISO-regioupdates uit op **10 juni 2022**. Verwacht dat er na deze release kleine updates worden weergegeven. |
| De manier wijzigen waarop Analytics omgaat met A4T-gegevens die via Experience Edge zijn verzameld | 25 februari 2022 | Aan **7 maart 2022**, hebben we de manier gewijzigd waarop we bepaalde doelgerelateerde gegevens die via Experience Edge naar Adobe Analytics zijn verzonden, verwerken. Bij het gebruik van de Adobe Experience Platform Web SDK met Analytics en Target werden sommige verpersoonlijkingsgebeurtenissen geteld in [!DNL Adobe Analytics] als [!UICONTROL Page Views]. Dit leidde tot opgeblazen aantallen van de paginamening en extra servervraag. Met de verandering, worden de verpersoonlijkingsvraag zonder de inhoud van Analytics genegeerd. Aanroepen van personalisatie met A4T-gegevens zullen de A4T-gegevens opnemen, maar zullen niet worden opgenomen als factureerbare serveraanroepen. Evenmin zal dit van invloed zijn op paginaweergaven of metriek van koppelingsgebeurtenissen. |
| Oudere geplande Report Builder-taken pauzeren | 24 februari 2022 | **15 april 2022** Adobe is van plan alle geplande Report Builder-taken die meer dan twee jaar geleden zijn gemaakt, te pauzeren. Deze pauze is met name van toepassing op alle taken die vóór 31 januari 2020 zijn gemaakt. Er worden geen taken, werkboeken of gegevens verwijderd. Taken die ouder zijn dan twee jaar worden echter onderbroken en er worden geen extra geplande taken verzonden. [Meer informatie](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| Verlopen van de lijst van gewenste personen EOL-extensie voor verouderde integratie van Analytics OAuth/JWT | 14 januari 2022 | Aan **25 mei 2022** de [Analytics 1.3 API, 1.4 SOAP API en Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) De verlenging van de lijst van gewenste personen verloopt. Het werd aangeboden klanten te voorzien die erfenis gebruiken [!DNL Adobe Analytics] OAuth/JWT geloofsbrieven extra tijd om hun cliëntintegratie te migreren aan [Adobe IMS-referenties](https://developer.adobe.com/console). Deze vervaldatum beïnvloedt (maar is niet beperkt tot) [!DNL Adobe Analytics Livestream] en [!DNL Adobe Campaign] klanten die hun vereiste IMS-migratie niet hebben voltooid. Klanten die op dit moment verouderde [!DNL Analytics] OAuth/JWT-referenties via de extensie lijst van gewenste personen en die de migratie naar IMS-referenties op 25 mei 2022 niet hebben voltooid, verliezen de toegang tot Adobe-services. Livestream-klanten kunnen naar deze [instructies](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) over het migreren van hun clienttoepassingen naar IMS-referenties. [!DNL Campaign] klanten kunnen hun Adobe account team bereiken over de upgrade naar de nieuwste versie van [!DNL Campaign]. |
| SFTP-services (Secure File Transfer Protocol) upgraden | 3 maart 2022 | Aan **15 mei 2022**, [!DNL Adobe Analytics] zal de SFTP-services (Secure File Transfer Protocol) upgraden om betere beveiliging voor bestandsoverdrachten te bieden. Door deze wijziging worden sommige SFTP-clientconfiguraties niet meer ondersteund. We voegen ook enkele verbindingsopties toe die beschikbaar zijn op **1 maart 2022**. Dit is alleen van invloed op gegevens die via SFTP naar Adobe Analytics worden verzonden of van worden opgehaald. Dit heeft geen invloed op het FTP-protocol. Om onderbreking van de dienst te vermijden, gelieve ervoor te zorgen dat uw cliënten SFTP (code, hulpmiddelen, de diensten) in overeenstemming met de gedetailleerde veranderingen zijn [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html). |
| EOL voor [!DNL Reports & Analytics] | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de technologienormen van Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement {#appm}

Voor de meest recente updates over AppMeasurement-releases (versie 2.22.4) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics] releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=en)
