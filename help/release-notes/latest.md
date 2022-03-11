---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 75cf6b9898e4afd1f10d7ee2f08f148219965343
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 5%

---

# Opmerkingen bij de huidige Adobe Analytics-release (februari 2022)

**Laatste update**: 11 maart 2022

Meer informatie over de nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html). De nieuwste zelfhulpdocumentatie, zelfstudies en cursussen over Experience League.

## Nieuwe functies in Adobe Analytics {#aa-features}

| Functie | Beschrijving | [Doeldatum](releases.md) |
| ----------- | ---------- | ------- |
| Modus voor voorvertoning van mobiel scorecard-project | Start een voorvertoning van hoe uw mobiele scorecard eruit zal zien in de app Analytics dashboards, rechtstreeks vanuit de scorecard builder. In de voorvertoningsmodus kunnen gebruikers op dezelfde manier werken met filters en grafieken als in de app, zodat ze een voorvertoning van de ervaring kunnen bekijken voordat ze de scorecard opslaan en delen. Gebruikers kunnen de apparaatkiezer ook in de voorvertoningsmodus gebruiken om te zien hoe hun scorecard er op verschillende apparaten uitziet. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/mobapp/create-scorecard.html?lang=en#preview) | 16 februari 2022 |
| API-projecteindpunt | Analysis Workspace-projecten toevoegen, bewerken of verwijderen met behulp van de API. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/projects/) | 1 feb. 2022 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Adobe Analytics

* Oplossing voor een aantal problemen met [!UICONTROL Server call usage]. (AN-279134, AN-279878, AN-280802, AN-279097, AN-191284, AN-269720)
* Probleem opgelost waarbij Data Warehouse lege CSV-bestanden zou exporteren. (AN-280291)
* Probleem verholpen waarbij de namen van het publiek niet werden gevuld voor recente segmenten. (AN-279715)
* Probleem verholpen met trage rapportagetijden. (AN-280055)
* Correctie van problemen met classificaties waarbij niet alle dimensie-items werden ingedeeld. (AN-280031)

### Extra correcties in Adobe Analytics

AN-268093, AN-273820, AN-274435, AN-274904, AN-275356, AN-275947, AN-276160, AN 276258, AN-276705, AN-277051, AN-277957, AN-278693, AN-278882, AN-279000, AN-2 79046, AN-279362, AN-279460, AN-279488, AN-279554, AN-279572, AN-279663, AN-27 9755, AN-279825, AN-280002, AN-280013, AN-280019, AN-280033, AN-280086, AN-280 232, AN-280264, AN-280288, AN-280342, AN-280347, AN-280360, AN-280370, AN-2807 24, AN-280830, AN-280941, AN-281353, AN-281424, AN-281533

## Belangrijke berichten voor [!DNL Analytics]-beheerders

**Bijgewerkt op 11 maart 2022**

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| 2022 ISO-regioupdates | 11 maart 2021 | Adobe voert op 10 juni 2022 updates voor de ISO-regio uit voor 2022. Verwacht dat er na deze release kleine updates worden weergegeven. |
| De manier wijzigen waarop Analytics omgaat met A4T-gegevens die via Experience Edge zijn verzameld | 25 februari 2022 | Aan **7 maart 2022**, zullen we wijzigen hoe we bepaalde doelgerelateerde gegevens verwerken die via Experience Edge naar Adobe Analytics worden verzonden. Bij het gebruik van de Adobe Experience Platform Web SDK met Analytics en Target werden sommige verpersoonlijkingsgebeurtenissen geteld in [!DNL Adobe Analytics] als [!UICONTROL Page Views]. Dit leidde tot opgeblazen aantallen van de paginamening en extra servervraag. Met de verandering, zal de verpersoonlijkingsvraag zonder de inhoud van Analytics worden genegeerd. Aanroepen van personalisatie met A4T-gegevens zullen de A4T-gegevens opnemen, maar zullen niet worden opgenomen als factureerbare serveraanroepen. Evenmin zal dit van invloed zijn op paginaweergaven of metriek van koppelingsgebeurtenissen. |
| Oudere geplande Report Builder-taken pauzeren | 24 februari 2022 | **15 april 2022** Adobe is van plan alle geplande Report Builder-taken die meer dan twee jaar geleden zijn gemaakt, te pauzeren. Deze pauze is met name van toepassing op alle taken die vóór 31 januari 2020 zijn gemaakt. Er worden geen taken, werkboeken of gegevens verwijderd. Taken die ouder zijn dan twee jaar worden echter onderbroken en er worden geen extra geplande taken verzonden. [Meer informatie](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| Verlopen van de lijst van gewenste personen EOL-extensie voor verouderde integratie van Analytics OAuth/JWT | 14 januari 2022 | Aan **25 mei 2022** de [Analytics 1.3 API, 1.4 SOAP API en Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) De verlenging van de lijst van gewenste personen verloopt. Het werd aangeboden klanten te voorzien die erfenis gebruiken [!DNL Adobe Analytics] OAuth/JWT geloofsbrieven extra tijd om hun cliëntintegratie te migreren aan [Adobe IMS-referenties](https://developer.adobe.com/console). Deze vervaldatum beïnvloedt (maar is niet beperkt tot) [!DNL Adobe Analytics Livestream] en [!DNL Adobe Campaign] klanten die hun vereiste IMS-migratie niet hebben voltooid. Klanten die op dit moment verouderde [!DNL Analytics] OAuth/JWT-referenties via de extensie lijst van gewenste personen en die de migratie naar IMS-referenties op 25 mei 2022 niet hebben voltooid, verliezen de toegang tot Adobe-services. Livestream-klanten kunnen naar deze [instructies](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) over het migreren van hun clienttoepassingen naar IMS-referenties. [!DNL Campaign] klanten kunnen hun Adobe account team bereiken over de upgrade naar de nieuwste versie van [!DNL Campaign]. |
| EOL voor [!DNL Reports & Analytics] | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de technologienormen van Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |
| SFTP-services (Secure File Transfer Protocol) upgraden | 3 maart 2022 | Aan **15 mei 2022**, [!DNL Adobe Analytics] zal de SFTP-services (Secure File Transfer Protocol) upgraden om betere beveiliging voor bestandsoverdrachten te bieden. Door deze wijziging worden sommige SFTP-clientconfiguraties niet meer ondersteund. We voegen ook enkele verbindingsopties toe die beschikbaar zijn op **1 maart 2022**. Dit is alleen van invloed op gegevens die via SFTP naar Adobe Analytics worden verzonden of van worden opgehaald. Dit heeft geen invloed op het FTP-protocol. Om onderbreking van de dienst te vermijden, gelieve ervoor te zorgen dat uw cliënten SFTP (code, hulpmiddelen, de diensten) in overeenstemming met de gedetailleerde veranderingen zijn [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html). |

## AppMeasurement {#appm}

Voor de meest recente updates over AppMeasurement-releases (versie 2.22.4) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics] releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=en)
