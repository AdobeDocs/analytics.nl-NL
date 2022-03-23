---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: f3b62096b481bda29946ccb091771157dce41d9d
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 4%

---

# Current Adobe Analytics release notes (March 2022)

**Laatst bijgewerkt: 23 maart 2022**

>[!IMPORTANT]
>
>De volgende inhoud bevat pre-releasegegevens en kan worden gewijzigd.

* Voor opmerkingen bij de release van februari 2022 gaat u [hier](/help/release-notes/2022.md).
* Meer informatie over de nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html). De nieuwste zelfhulpdocumentatie, zelfstudies en cursussen over Experience League.

## Nieuwe functies in Adobe Analytics {#aa-features}

| Functie | Beschrijving | [Doeldatum](releases.md) |
| ----------- | ---------- | ------- |
| Annotaties in werkruimte | Met annotaties in Workspace kunt u op effectieve wijze contextuele gegevensnuances en inzichten aan uw organisatie meedelen. [Meer informatie](/help/analyze/analysis-workspace/components/annotations/overview.md) | Geleidelijke uitrol start op 23 maart 2022 |
| Adobe Analytics-bestemmingspagina-updates | Updates van de landingspagina van de gezamenlijke werkruimte/Rapporten &amp; Analytics die de bruikbaarheid en het gemak van navigatie verbetert. [Meer informatie](/help/analyze/landing.md) | April 1, 2022 |
| [!UICONTROL Next item] of [!UICONTROL Previous item] Deelvenster Werkruimte | The [!UICONTROL Next or Previous item] panel allows you to explore items that follow or precede a dimension item of your choice. Gebruik deze optie bijvoorbeeld als u de volgende of vorige pagina&#39;s naar een specifieke productpagina, een marketingkanaal of zelfs naar een apparaattype wilt bekijken. Dit deelvenster gaat verder dan oudere rapporten (verouderde rapporten), omdat u hiermee elke dimensie kunt bekijken en geen nieuwe implementatie nodig hebt om inzichten op te halen. | 1 april 2022 |
| [!UICONTROL Page Summary] Workspace panel | The [!UICONTROL Page Summary] panel provides a deep-dive analysis for a page of your choosing. Het biedt dezelfde details als oudere rapporten en analyses [!UICONTROL Page Summary] verslag, nog veel meer. | 1 april 2022 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Adobe Analytics

* Probleem verholpen waarbij een fout is opgetreden bij het openen van Activity Map. (AN-267177)
* Fixed an issue with unsuccessful user asset transfers. (AN-279813)
* Problemen verholpen met het deelvenster A4T-werkruimte. (AN-281594; AN-282418)
* Probleem verholpen waarbij sommige gebruikers geen toegang hadden tot Adobe Analytics. (AN-282776)
* Fixed issues with some newly created report suites not collecting data. (AN-283114, AN-283311)
* Oplossing voor problemen waarbij Win11 niet kon worden gedetecteerd met de dimensie Besturingssysteem. (AN-275569, AN-275727; AN-280335)
* Correctie van problemen met verkeerd verzonden e-mails met gegevensfeeds. (AN-280255; AN-282051)


### Extra correcties in Adobe Analytics

AN-256929; AN-270937; AN-272158; AN-275130; AN-277830; AN-278635; AN-279066; AN-279683; AN-279899; AN-280504; AN-280617; AN-280663; AN-281423; AN-281523; AN-281608; AN-281671; AN-281963; AN-282027; AN-282218; AN-282593; AN-282605; AN-282632; AN-282654; AN-282694; AN-282744; AN-282756; AN-282804; AN-282838; AN-282862; AN-282903; AN-282937; AN-282892; AN-283315; AN-283338; AN-283388; AN-283417; AN-283474; AN-283511; AN-283691, AN-283895; AN-283943; AN-283957; AN-284030; AN-284100; AN-284142; AN-284162

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| Oudere geplande rapporten onderbreken | 11 maart 2022 | Effectief **15 april 2022**, is Adobe voornemens alle geplande rapporten met een aanmaakdatum van meer dan twee jaar (aangemaakt vóór 31 januari 2020) te pauzeren. No reports or data will be deleted. Alleen rapporten die ouder zijn dan twee jaar worden gepauzeerd en er worden geen aanvullende geplande rapporten verzonden. [Meer informatie](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| 2022 ISO region updates | March 11, 2021 | Adobe voert 2022 ISO-regioupdates uit op **10 juni 2022**. Verwacht dat er na deze release kleine updates worden weergegeven. |
| De manier wijzigen waarop Analytics omgaat met A4T-gegevens die via Experience Edge zijn verzameld | 25 februari 2022 | Aan **7 maart 2022**, hebben we de manier gewijzigd waarop we bepaalde doelgerelateerde gegevens die via Experience Edge naar Adobe Analytics zijn verzonden, verwerken. Bij het gebruik van de Adobe Experience Platform Web SDK met Analytics en Target werden sommige verpersoonlijkingsgebeurtenissen geteld in [!DNL Adobe Analytics] als [!UICONTROL Page Views]. Dit leidde tot opgeblazen aantallen van de paginamening en extra servervraag. Met de verandering, worden de verpersoonlijkingsvraag zonder de inhoud van Analytics genegeerd. Personalization-aanroepen met A4T-gegevens registreren de A4T-gegevens, maar worden niet opgenomen als factureerbare serveraanroepen. Ze hebben evenmin invloed op de paginaweergaven of de metriek van de koppelingsgebeurtenis. |
| Oudere geplande Report Builder-taken pauzeren | February 24, 2022 | **15 april 2022** Adobe is van plan alle geplande Report Builder-taken die meer dan twee jaar geleden zijn gemaakt, te pauzeren. Deze pauze is met name van toepassing op alle taken die vóór 31 januari 2020 zijn gemaakt. No tasks, workbooks or data will be deleted. However, tasks identified as older than two years will be paused, and no additional scheduled tasks will be sent. [Meer informatie](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| Verlopen van de lijst van gewenste personen EOL-extensie voor verouderde integratie van Analytics OAuth/JWT | 14 januari 2022 | Aan **25 mei 2022** de [Analytics 1.3 API, 1.4 SOAP API en Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) De verlenging van de lijst van gewenste personen verloopt. It was offered to provide customers using legacy [!DNL Adobe Analytics] OAuth/JWT credentials additional time to migrate their client integrations to [Adobe IMS credentials](https://developer.adobe.com/console). Deze vervaldatum beïnvloedt (maar is niet beperkt tot) [!DNL Adobe Analytics Livestream] en [!DNL Adobe Campaign] klanten die hun vereiste IMS-migratie niet hebben voltooid. Klanten die op dit moment verouderde [!DNL Analytics] OAuth/JWT-referenties via de extensie lijst van gewenste personen en die de migratie naar IMS-referenties op 25 mei 2022 niet hebben voltooid, verliezen de toegang tot Adobe-services. Livestream-klanten kunnen naar deze [instructies](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) over het migreren van hun clienttoepassingen naar IMS-referenties. [!DNL Campaign] klanten kunnen hun Adobe account team bereiken over de upgrade naar de nieuwste versie van [!DNL Campaign]. |
| SFTP-services (Secure File Transfer Protocol) upgraden | 3 maart 2022 | Aan **15 mei 2022**, [!DNL Adobe Analytics] zal de SFTP-services (Secure File Transfer Protocol) upgraden om betere beveiliging voor bestandsoverdrachten te bieden. Door deze wijziging worden sommige SFTP-clientconfiguraties niet meer ondersteund. We voegen ook enkele verbindingsopties toe die beschikbaar zijn op **1 maart 2022**. This impacts only data sent to or retrieved from Adobe Analytics using SFTP. Dit heeft geen invloed op het FTP-protocol. Om onderbreking van de dienst te vermijden, gelieve ervoor te zorgen dat uw cliënten SFTP (code, hulpmiddelen, de diensten) in overeenstemming met de gedetailleerde veranderingen zijn [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html). |
| EOL for [!DNL Reports & Analytics] | 4 januari 2022 | Effective **December 31, 2023**, Adobe intends to discontinue [!DNL Reports & Analytics] and its accompanying reports and features. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de technologienormen van Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

## AppMeasurement {#appm}

For the latest updates on AppMeasurement releases (Version 2.22.4), please refer to [AppMeasurement for JavaScript release notes](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics] releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=en)
