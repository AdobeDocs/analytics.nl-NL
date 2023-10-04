---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 5785629376b8ae528535629a77a29dcdd2ca80b8
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 1%

---

# Opmerkingen bij de huidige Adobe Analytics-release (oktober 2023)

**Laatste update**: 4 oktober 2023

De opmerkingen in de release van oktober hebben betrekking op de releaseperiode van 4 oktober 2023 tot 25 oktober 2023. Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Nieuwe kolommen beschikbaar bij het beheren van componenten** | De volgende nieuwe kolommen zijn nu beschikbaar wanneer het beheren van componenten:<ul><li>Gebruikt in<p>Deze kolom is beschikbaar in het dialoogvenster [Het berekende manager van metriek](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md) en de [Segmentbeheer](/help/components/segmentation/segmentation-workflow/seg-manage.md).</p></li><li>Laatst gebruikt<p>Deze kolom is beschikbaar in het dialoogvenster [Het berekende manager van metriek](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md)de [Segmentbeheer](/help/components/segmentation/segmentation-workflow/seg-manage.md)en de [Waarschuwingenbeheer](/help/components/c-alerts/alert-manager.md).</p></li></ul><p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd. U kunt het gegevenswoordenboek samen met deze informatie gebruiken om u te helpen bij het volgen van en beter begrijpen hoe de componenten in uw organisatie worden gebruikt.</p> | 20 september 2023 | 4 oktober 2023 |
| **Verbeteringen voor Activity Manager rapporteren** | De manager van de Activiteit van de Rapportering laat u de rapporteringscapaciteit voor elke rapportreeks in uw organisatie zien.  Het biedt beheerders gedetailleerde zichtbaarheid bij het melden van het verbruik om capaciteitsproblemen tijdens piekrapportagetijden eenvoudig te kunnen vaststellen en verhelpen. Hieronder vindt u een aantal verbeteringen die nu beschikbaar zijn in Rapportagentenbeheer: <ul><li>Verdere verzoeken beperken: naast het annuleren van huidige aanvragen kunnen beheerders nu verzoeken voor een bepaalde periode beperken. De beheerders kunnen verzoeken door Verzoek, Project, en Gebruiker beperken.</li><li>Naast de metriek van het Gebruik en van de Capaciteit, omvat de Manager van de Activiteit van de Rapportering nu meer gegevens over het melden van activiteit: de kolom van de Complexiteit, de kolom van de Gebruiker, en de kolom van de Verbinding.</li><li>Alle annuleringen en beperkingen die in de manager van de Activiteit van de Rapportering worden aangebracht zijn nu zichtbaar in het Logboek van de Controle. Beheerders kunnen het auditlogboek gebruiken om te bekijken wat momenteel is geannuleerd. Annuleringen kunnen niet worden teruggedraaid in de Manager van de Activiteit van de Rapportering of in het Logboek van de Controle.</li></ul>Meer informatie (binnenkort beschikbaar) | 17 oktober 2023 | 23 oktober 2023 |
| **Verbeteringen voor Data Warehouse** | Wanneer het creëren van een verzoek van de Data Warehouse, kunt u een wolkenrekening nu vormen om als rapportbestemming te gebruiken. De volgende typen cloudaccounts zijn beschikbaar voor het verzenden van gegevens:<ul><li>Amazon S3</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li><li>E-mail (deze optie was voorheen beschikbaar)</li></ul>FTP, SFTP, Azure Blob, en S3 zijn nog beschikbaar als rapportbestemmingen, maar worden niet meer geadviseerd.<p>De gebruikerservaring bij het maken en beheren van verzoeken om Data Warehouse is ook verbeterd. Zie voor meer informatie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md) en [Aanvragen voor Data Warehouse beheren](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-requests-manage.html). | 12 september 2023 | 25 oktober 2023 |
| **Adobe Analytics-projecten en alle inbegrepen onderdelen migreren naar Customer Journey Analytics** | U kunt nu uw Adobe Analytics-projecten migreren naar Customer Journey Analytics. Dit proces vereenvoudigt de overgang van Adobe Analytics naar Customer Journey Analytics. Wanneer u projecten naar Customer Journey Analytics migreert, worden de activa in kaart gebracht van een het rapportreeks van Adobe Analytics aan een de gegevensmening van de Customer Journey Analytics. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration.html) | 11 oktober 2023 | 25 oktober 2023 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Problemen verholpen waarbij A4T-rapporten niet werden weergegeven in de interface Doel/Analyse. (AN-329375, AN-329745, AN-330026)

AN-313983; AN-324189; AN-325095; AN-325677; AN-325886; AN-326068; AN-326360; AN 326458; AN-327290; AN-327315; AN-327353; AN-327505; AN-327589; AN-327609; AN-3 27922; AN-328110; AN-328222; AN-328261; AN-328496; AN-328577; AN-328629; AN-32 8736; AN-328888; AN-328899; AN-328902; AN-328921; AN-328958; AN-329208; AN-329 329336; AN-329357; AN-329335; AN-329336; AN-329357; AN-329385; AN-3293 329501; AN-329504; AN-329505; AN-329504; AN-329505; AN-329515; AN-32952 4; AN-329526; AN-329534; AN-329539; AN-329541; AN-329543; AN-329545; AN-32956; AN-329570; AN-329623; AN-329624; AN-329636; AN-329646; AN-329647; AN-32968; AN 329701; AN-329737; AN-329741; AN-329751; AN-329812; AN-329813; AN-329821; AN-3 29824; AN-329833; AN-329848; AN-329852; AN-329861; AN-329863; AN-329874 9882; AN-329911; AN-329917; AN-329942; AN-329954; AN-329968; AN-329971; AN-329 982; AN-330044; AN-330052; AN-330131; AN-330132; AN-330230; AN-330352; AN-3303 330541; AN-330599

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Volledige IP obfuscatie voor de Invloed van de Rand van de Ervaring van de Adobe** | 27 september 2023 | IP-verduistering voor hits van Experience Edge wordt later in oktober 2023 bijgewerkt. In april, voegde de Rand van de Ervaring de capaciteit toe om IP adressen te verduisteren. Op dat ogenblik, steunde Adobe Analytics slechts gedeeltelijke obfuscatie van IPs, wegens de manier de processen van de Analyse van de Ervaring Edge. Wanneer klanten volledige verwarring kozen voor Experience Edge, ontvingen Analytics slechts gedeeltelijk verduisterde IP&#39;s. Wanneer deze verandering wordt uitgevoerd, zal Analytics volledig verduisterde IP ontvangen. |
| **Adobe Analytics LiveStream - API&#39;s voor Analytics 2.0** | 27 september 2023 | Klanten hebben nu toegang tot de [Eindpuntgids voor Adobe Analytics Livestream](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/) onder de Adobe Analytics 2.0 API&#39;s in plaats daarvan op de vorige locatie, met de 1.4 API&#39;s. Merk op dat de klanten die de geloofsbrieven van Adobe I/O JWT gebruiken aan Adobe I/O server-aan-Server geloofsbrieven tegen 1 Januari, 2025 moeten migreren. (Zie de gegevens onder EOL-berichten hieronder.) |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar Adobe I/O OAuth Server-to-Server-gebruikersgegevens migreren door **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementatiehandleiding voor nieuwe en oude toepassingen met OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[De nieuwe OAuth Server-to-Server-referenties gebruiken](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL voor[!DNL Reports & Analytics]** | 7 maart 2023 | Effectief **31 december 2023**, is de Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] niet langer aan de technologienormen van de Adobe voldoen. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit.<p>Op 31 december 2023 zullen we veel van de bijbehorende functies Rapporten en Analytics beëindigen, waaronder, maar niet beperkt tot: Geplande rapporten, Gegevensextracten en DL-rapporten. Na 31 december 2023 worden alle geplande rapporten niet meer verzonden. In **April 2023**, werden alle rapporten die volgens de planning na 31 december 2023 zouden verlopen, automatisch bijgewerkt en op 31 december 2023 zouden vervallen. Bovendien kun je toekomstige rapporten niet langer plannen na 31 december 2023. |
| **EOL van [!UICONTROL Publishing Lists] functie** | 29 september 2022 | In het kader van de regeling exportgerichte bedrijven voor rapporten en analyses: [!UICONTROL Publishing Lists] zijn bedoeld om het einde van de levensduur van **december 2023**. U kunt geen nieuwe of bestaande [!UICONTROL Publishing Lists] naar verzenden of plannen [!UICONTROL Analysis Workspace] projecten. |
| **EOL voor Data Workbench** | 14 september 2022 | Adobe wil Data Workbench aan het einde van de levensduur effectief maken **31 december 2023**. Zie [Aankondiging einde levensduur Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html) voor meer informatie. Neem contact op met de accountmanager van de Adobe van uw organisatie voor vragen. |

{style="table-layout:auto"}

## AppMeasurement

Voor de meest recente updates over releases van AppMeasurementen (versie 2.25.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
