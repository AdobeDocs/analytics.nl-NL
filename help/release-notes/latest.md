---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 2998ab3ecb83e14be38333a2836f863667babfee
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 3%

---

# Huidige Adobe Analytics-releaseopmerkingen (september 2023)

**Laatste update**: 13 september 2023

De opmerkingen in de release van september betreffen de releaseperiode van 13 september 2023 tot 3 oktober 2023. Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Classificaties in API 2.0** | Biedt Adobe Analytics API 2.0-methoden voor het opslaan, verwijderen, ophalen, importeren en exporteren van indelingssetgegevens. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/) | N.v.t. | 13 september 2023 |
| **Ondersteuning voor nieuwe `correlationID` veld voor A4T-classificaties** | De `_experience.decisioning.propositions.scopeDetails.correlationID` Het veld is nu beschikbaar in het Adobe Analytics-bronverbindingsschema. We voegen deze id toe voor het eenvoudig samenvoegen van classificatiegegevens voor Adobe Target-activiteiten en ervaringsgebeurtenissen. | N.v.t. | 13 september 2023 |
| **Verbeteringen voor Data Warehouse** | Wanneer het creëren van een verzoek van de Data Warehouse, kunt u een wolkenrekening nu vormen om als rapportbestemming te gebruiken. De volgende typen cloudaccounts zijn beschikbaar voor het verzenden van gegevens:<ul><li>Amazon S3</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li><li>E-mail (deze optie was voorheen beschikbaar)</li></ul>FTP, SFTP, Azure Blob, en S3 zijn nog beschikbaar als rapportbestemmingen, maar worden niet meer geadviseerd.<p>De gebruikerservaring bij het maken en beheren van verzoeken om Data Warehouse is ook verbeterd. Zie voor meer informatie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md) en [Aanvragen voor Data Warehouse beheren](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-requests-manage.html). | 13 september 2023 | 4 oktober 2023 |
| **Nieuwe kolommen beschikbaar bij het beheren van componenten** | De volgende nieuwe kolommen zijn nu beschikbaar wanneer het beheren van componenten:<ul><li>Gebruikt in<p>Deze kolom is beschikbaar in het dialoogvenster [Het berekende manager van metriek](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md) en de [Segmentbeheer](/help/components/segmentation/segmentation-workflow/seg-manage.md).</p></li><li>Laatst gebruikt<p>Deze kolom is beschikbaar in het dialoogvenster [Het berekende manager van metriek](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md)de [Segmentbeheer](/help/components/segmentation/segmentation-workflow/seg-manage.md)en de [Waarschuwingenbeheer](/help/components/c-alerts/alert-manager.md).</p></li></ul><p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd. U kunt het gegevenswoordenboek samen met deze informatie gebruiken om u te helpen bij het volgen van en beter begrijpen hoe de componenten in uw organisatie worden gebruikt.</p> | 20 september 2023 | 4 oktober 2023 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Probleem verholpen waardoor classificatiegegevens niet konden worden weergegeven in Workspace. (AN-326827)

## Andere oplossingen

AN-314882; AN-315591; AN-318165; AN-318559; AN-319031; AN-319244; AN-321657; AN 321759; AN-323099; AN-323596; AN-323640; AN-324442; AN-324921; AN-324953; AN-3 24977; AN-324979; AN-325124; AN-325395; AN-325433; AN-325535; AN-325693; AN-32 5720; AN-325835; AN-325880; AN-325957; AN-325984; AN-326054; AN-326065; AN-326 136; AN-326155; AN-326162; AN-326235; AN-326317; AN-326344; AN-32637; AN-3263 59; AN-326433; AN-326438; AN-326440; AN-326461; AN-326464; AN-326523; AN-3265 3; AN-326606; AN-326635; AN-326642; AN-326652; AN-326678; AN-326769; AN-32677; AN-326830; AN-326938; AN-326949; AN-327081; AN-327082; AN-327085; AN-327103; AN 327198; AN-327225; AN-327275; AN-327358; AN-327423; AN-327561; AN-327755; AN-3 27896; AN-327922; AN-328128; AN-328300; AN-328428; AN-328518; AN-32854

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| N.v.t. | N.v.t. | N.v.t. |

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

Voor de meest recente updates over releases van AppMeasurementen (versie 2.24.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
