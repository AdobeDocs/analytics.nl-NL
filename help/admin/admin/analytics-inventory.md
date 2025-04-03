---
description: De analytische inventaris gebruiken
title: Analytische inventarisatie
feature: Admin Tools
role: Admin
hide: true
hidefromtoc: true
exl-id: 9fc985c8-93d7-4838-9342-72a6268ef96f
source-git-commit: fceb28b7af480e6d87abf09c26f45a7afb2d3270
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 2%

---

# Analysevoorraad {#analytics-inventory}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory"
>title="Analysevoorraad"
>abstract="Deze pagina biedt een uitgebreid overzicht van uw Adobe Analytics-omgeving, inclusief het aantal projecten en onderdelen, rapportreeksen, gebruikers en nog veel meer. Deze informatie is met name van belang wanneer u voorbereidingen treft voor de upgrade naar Customer Journey Analytics."

<!-- markdownlint-enable MD034 -->

De Analysevoorraad biedt een uitgebreid overzicht van uw Adobe Analytics-omgeving, inclusief het aantal projecten en componenten, rapportsuites, gebruikers en nog veel meer. Deze informatie is met name van belang wanneer u voorbereidingen treft voor de upgrade naar Customer Journey Analytics.

Het doel van deze toepassing is om u te helpen de volgende vragen beantwoorden:

* Voor uw organisatie, welke activa (zoals rapportsuites, segmenten, gebruikers, werkruimteprojecten, gegevensvoer, etc.) moet u bevorderen en welke activa kunt u achterlaten?

* Nadat u hebt bepaald welk element moet worden gemigreerd:

   * Moet u vóór deze upgrade wat activa opruimen?

   * Moet u wat activaconsolidatie doen als onderdeel van het proces?

   * Wat moet de upgradevolgorde zijn voor uw activa?

   * Welke groep rapportsuites moet u als eerste upgraden? laatst?

## Machtigingen

De Inventaris van de Analyse is beschikbaar aan gebruikers met de voorrechten van Admin van het Product van Adobe Analytics in [ Adobe Admin Console ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/admin-roles-in-analytics).

## Access Analytics Inventory

1. Klik op **[!UICONTROL Analytics Inventory]** in het menu **[!UICONTROL Admin]** . Of ga naar **[!UICONTROL All admin]** > **[!UICONTROL Analytics Inventory]** .

![ Analytics-Inventory-menu ](assets/an-inventory-menu.png)

1. Het hoofdscherm toont een uitgebreid overzicht van uw Adobe Analytics-omgeving:

   ![ Hoofd inventarisscherm ](assets/an_inventory.png)

>[!IMPORTANT]
>
>   In deze eerste versie ziet u overzichtsnummers voor Workspace-projecten, Segmenten, Berekende metriek, Geavanceerde (Media Analytics) gegevens en Gebruikers. Momenteel zijn alleen rapportsuites mogelijk.


## Onderdelen {#components}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-components"
>title="Onderdelen"
>abstract="Deze sectie toont het aantal projecten, segmenten, en berekende metriek die in uw milieu van Adobe Analytics bestaan. Projecten en onderdelen kunnen naar Customer Journey Analytics worden gemigreerd."

<!-- markdownlint-enable MD034 -->

In deze aanvankelijke versie, kunt u samenvattingsinventarisaantallen voor de projecten van Workspace, Segmenten, en Berekende metrisch zien. Met de volgende releases kunt u deze componenten analyseren.

## Gegevensconfiguratie en -verzameling {#data-config}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-data-config"
>title="Gegevensconfiguratie en -verzameling"
>abstract="In deze sectie ziet u het aantal rapportsuite in uw Adobe Analytics-omgeving en uw toegang tot Streaming Media. "

<!-- markdownlint-enable MD034 -->

### Rapportsuites analyseren

1. Als u rapportsuites wilt analyseren en wilt beslissen welke u wilt migreren, navigeert u naar **[!UICONTROL Data configuration and collection]** > **[!UICONTROL Report suites]** en klikt u op **[!UICONTROL Analyze]**.

   ![Lijst van rapportsuites](assets/an_inv_rs.png)

   | Element | Beschrijving |
   | --- | --- |
   | Naam | De naam van de rapportsuite |
   | ID | De rapportsuite-id (rsid). Hiermee geeft u een unieke id op die alleen alfanumerieke tekens mag bevatten. Deze id kan na het maken niet meer worden gewijzigd. Adobe stelt het vereiste ID-voorvoegsel in en kan dit ook niet wijzigen. |
   | Voorvallen (afgelopen 90 dagen) |  |
   | Metrics | Hoe |
   | Dimensies |  |
   | Analyse voor doel (A4T) ingeschakeld |  |
   | Marketingkanalen ingeschakeld |  |
   | Source Connector ingeschakeld | Om te volgen |
   | Kalender Type | Raadpleeg Aangepaste agenda&#39;s voor meer informatie [](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/custom-calendar#) |

1. Let op:..

### Exporteren naar CSV

1. Als u de lijst met rapportsuites wilt exporteren naar een CSV-bestand, klikt u op **[!UICONTROL Export to CSV]** .

1. Het .csv-bestand wordt weergegeven in de map Downloads.

1. Open en sla deze op met een spreadsheettoepassing op uw apparaat.


## Gebruikersbeheer {#user-management}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-user-management"
>title="Gebruikersbeheer"
>abstract="In deze sectie wordt het aantal gebruikers in uw Adobe Analytics-omgeving weergegeven."

<!-- markdownlint-enable MD034 -->

Gebruikersbeheer is beschikbaar in een latere versie van het Analytics-overzicht.