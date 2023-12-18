---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: d3d4547238bdaedf8a9c8ac9c4a29e9237bbc3d8
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 1%

---

# Opmerkingen bij de huidige Adobe Analytics-release (oktober/november 2023)

**Laatste update**: 13 december 2023

Deze opmerkingen hebben betrekking op de releaseperiode van 23 oktober 2023 tot eind november 2023. Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Verbeteringen voor Activity Manager rapporteren** | De manager van de Activiteit van de Rapportering laat u de rapporteringscapaciteit voor elke rapportreeks in uw organisatie zien.  Het biedt beheerders gedetailleerde zichtbaarheid bij het melden van het verbruik om capaciteitsproblemen tijdens piekrapportagetijden eenvoudig te kunnen vaststellen en verhelpen. Hieronder vindt u een aantal verbeteringen die nu beschikbaar zijn in Rapportagentenbeheer: <ul><li>Verdere verzoeken beperken: naast het annuleren van huidige aanvragen kunnen beheerders nu verzoeken voor een bepaalde periode beperken. De beheerders kunnen verzoeken door Verzoek, Project, en Gebruiker beperken.</li><li>Naast de metriek van het Gebruik en van de Capaciteit, omvat de Manager van de Activiteit van de Rapportering nu meer gegevens over het melden van activiteit: de kolom van de Complexiteit, de kolom van de Gebruiker, en de kolom van de Verbinding.</li><li>Alle annuleringen en beperkingen die in de manager van de Activiteit van de Rapportering worden aangebracht zijn nu zichtbaar in het Logboek van de Controle. Beheerders kunnen het auditlogboek gebruiken om te bekijken wat momenteel is geannuleerd. Annuleringen kunnen niet worden teruggedraaid in de Manager van de Activiteit van de Rapportering of in het Logboek van de Controle.</li></ul><p>Zie voor meer informatie [Overzicht van Activity Manager rapporteren](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md)</p> | woensdag 17 oktober 2023 | woensdag 24 oktober 2023 |
| **Verbeteringen voor Data Warehouse** | Wanneer het creëren van een verzoek van de Data Warehouse, kunt u een wolkenrekening nu vormen om als rapportbestemming te gebruiken. De volgende typen cloudaccounts zijn beschikbaar voor het verzenden van gegevens:<ul><li>Amazon S3</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li><li>E-mail (deze optie was voorheen beschikbaar)</li></ul>FTP, SFTP, Azure Blob, en S3 zijn nog beschikbaar als rapportbestemmingen, maar worden niet meer geadviseerd.<p>De gebruikerservaring bij het maken en beheren van verzoeken om Data Warehouse is ook verbeterd. Zie voor meer informatie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md) en [Aanvragen voor Data Warehouse beheren](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-requests-manage.html). | woensdag 12 september 2023 | 15 december 2023 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Deze wijzigingen in Analytics Processing and Reporting Engine worden geïmplementeerd in de laatste week van oktober: we verhelpen een probleem waarbij de labels voor pagina- of koppelingsafmetingen onjuist werden weergegeven als `Unknown`. Voordat de correctie wordt uitgevoerd, wordt `Unknown` labels worden mogelijk onjuist weergegeven wanneer bij een treffer geen paginanaam of koppelingsnaam is doorgegeven. Standaard worden [!UICONTROL Page URL] en [!UICONTROL Link URL], respectievelijk. Deze afmetingen werden gevormd om geval ongevoelig te zijn. Met deze correctie zijn de volgende rapporten juist. Maar voor rapporten over historische gegevens kunnen sommige rapportresultaten nog steeds onjuist worden gelabeld als `Unknown`. (AN-328030)

### Andere oplossingen

AN-315676; AN-323398; AN-326209; AN-328178; AN-328261; AN-328395; AN-328671; AN 329282; AN-329330; AN-329355; AN-329506; AN-329516; AN-329738; AN-329769; AN-3 29771; AN-329816; AN-329877; AN-329928; AN-329957; AN-329962; AN-329966; AN-33 0023; AN-330081; AN-330083; AN-330105; AN-330138; AN-330140; AN-330165; AN-30 241; AN-330359; AN-330366; AN-330427; AN-330438; AN-330442; AN-330534; AN-306 16; AN-330654; AN-330783; AN-330879; AN-330881; AN-330883; AN-33087; AN-33088 330955; AN-330979; AN-331031; AN-331053; AN-331068; AN-331071; AN-331074; AN-331075; AN-331076; AN-331078; AN-331085; AN-331093; AN-331167; AN-331171; AN 331181; AN-331196; AN-331226; AN-331258; AN-331260; AN-331279; AN-331286; AN-3 31290; AN-331365; AN-331375; AN-331376; AN-331454; AN-331519; AN-331570; AN-33 1590; AN-331593; AN-331603; AN-331751; AN-331816; AN-331897; AN-331900; AN-331 906; AN-331926; AN-331929; AN-332031; AN-332067; AN-332101; AN-33214; AN-3321 332277; AN-332361; AN-332370; AN-332277; AN-332361; AN-332370; AN-33238 6

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Volledige IP obfuscatie voor de Invloed van de Rand van de Ervaring van de Adobe** | donderdag 27 september 2023 | IP-verduistering voor hits van Experience Edge wordt later in oktober 2023 bijgewerkt. In april 2023, voegde de Rand van de Ervaring de capaciteit toe om IP adressen te verduisteren. Op dat ogenblik, steunde Adobe Analytics slechts gedeeltelijke obfuscatie van IPs, wegens de manier de processen van de Analyse van de Ervaring Edge. Wanneer klanten volledige verwarring kozen voor Experience Edge, ontvingen Analytics slechts gedeeltelijk verduisterde IP&#39;s. Wanneer deze verandering wordt uitgevoerd, zal Analytics volledig verduisterde IP ontvangen. |
| **Adobe Analytics LiveStream - API&#39;s voor Analytics 2.0** | donderdag 27 september 2023 | Klanten hebben nu toegang tot de [Eindpuntgids voor Adobe Analytics Livestream](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/) onder de Adobe Analytics 2.0 API&#39;s in plaats daarvan op de vorige locatie, met de 1.4 API&#39;s. Merk op dat de klanten die de geloofsbrieven van Adobe I/O JWT gebruiken aan Adobe I/O server-aan-Server geloofsbrieven tegen 1 Januari, 2025 moeten migreren. (Zie de gegevens onder EOL-berichten hieronder.) |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **EOL voor[!DNL Reports & Analytics]** | 13 december 2023 | Effectief **17 januari 2024**, is de Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] niet langer aan de technologienormen van de Adobe voldoen. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit.<p>Op 31 december 2023 zullen we veel van de bijbehorende functies Rapporten en Analytics beëindigen, waaronder, maar niet beperkt tot: Geplande rapporten, Gegevensextracten en DL-rapporten. Na 31 december 2023 worden alle geplande rapporten niet meer verzonden. In **April 2023**, werden alle rapporten die volgens de planning na 31 december 2023 zouden verlopen, automatisch bijgewerkt en op 31 december 2023 zouden vervallen. Bovendien kun je toekomstige rapporten niet langer plannen na 31 december 2023. |
| **EOL van [!UICONTROL Publishing Lists] functie** | 13 december 2023 | In het kader van de regeling exportgerichte bedrijven voor rapporten en analyses: [!UICONTROL Publishing Lists] zijn bedoeld om het einde van de levensduur te bereiken **17 januari 2024**. U kunt geen nieuwe of bestaande [!UICONTROL Publishing Lists] naar verzenden of plannen [!UICONTROL Analysis Workspace] projecten. |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | vrijdag 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar Adobe I/O OAuth Server-to-Server-gebruikersgegevens migreren door **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementatiehandleiding voor nieuwe en oude toepassingen met OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[De nieuwe OAuth Server-to-Server-referenties gebruiken](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL voor Data Workbench** | donderdag 14 september 2022 | Adobe wil Data Workbench aan het einde van de levensduur effectief maken **31 december 2023**. Zie [Aankondiging einde levensduur Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html) voor meer informatie. Neem contact op met de accountmanager van de Adobe van uw organisatie voor vragen. |

{style="table-layout:auto"}

## AppMeasurement

Voor de meest recente updates over releases van AppMeasurementen (versie 2.25.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
