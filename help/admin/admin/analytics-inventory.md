---
description: De analytische inventaris gebruiken
title: Analytische inventarisatie
feature: Admin Tools
role: Admin
hide: true
hidefromtoc: true
exl-id: 9fc985c8-93d7-4838-9342-72a6268ef96f
source-git-commit: 1e52aecdbb26dce0875b2df685ed2fa860eaba85
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 1%

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

   * Wilt u de middelen opschonen voordat u de upgrade uitvoert?

   * Moet u een of andere consolidatie van bedrijfsmiddelen uitvoeren als onderdeel van het proces?

   * Wat zou de verbeteringsopeenvolging voor uw activa moeten zijn?

   * Welke groep rapportsuites zou u eerst bevorderen? laatst?

## Machtigingen

De Inventaris van de Analyse is beschikbaar aan gebruikers met de voorrechten van Admin van het Product van Adobe Analytics in [ Adobe Admin Console ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/admin-roles-in-analytics).

## Access Analytics Inventory

1. Klik op **[!UICONTROL Analytics Inventory]** in het menu **[!UICONTROL Admin]** . Of ga naar **[!UICONTROL All admin]** > **[!UICONTROL Analytics Inventory]** .

![ Analytics-Inventory-menu ](assets/an-inventory-menu.png)

1. Het hoofdscherm toont een uitgebreid overzicht van uw Adobe Analytics-omgeving:

   ![ Hoofd inventarisscherm ](assets/an_inventory.png)

   Specifiek, dit schermoppervlakken

   * Het totale aantal Analysis Workspace- en Mobile Scorecard-projecten dat onder deze organisatie actief is voor alle gebruikers.
   * Het totale aantal segmenten en berekende metriek die onder deze organisatie over alle gebruikers actief zijn.
   * Het totale aantal basisrapportsuites dat is gedefinieerd (virtuele rapportsuites worden niet opgenomen).
   * Als de functie Media Analytics actief is en als dat het geval is, in welke modus.
   * Het totale aantal gebruikers dat in die organisatie is gedefinieerd.


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

### Reeksen rapporteren

In de weergave met de rapportsuites worden alle in een organisatie gedefinieerde rapportsuites weergegeven. U kunt de volgende vragen beantwoorden:

* Welke rapportsuites hebben de afgelopen 90 dagen het zwaarst getroffen?
* Welke rapportsuites hebben de afgelopen 90 dagen geen treffer ontvangen?
* Welke rapportsuites hebben het grootste aantal bepaalde dimensie?
* Welke rapportsuites hebben het grootste aantal bepaalde metriek?

De antwoorden op deze vragen zullen u een goed idee geven van welke verslagen de beste kandidaten voor migratie zijn.

1. Als u rapportsuites wilt analyseren, navigeert u naar **[!UICONTROL Data configuration and collection]** > **[!UICONTROL Report suites]** en klikt u op **[!UICONTROL Analyze]** .

   ![ Lijst van rapportsuites ](assets/an_inv_rs.png)

   | Element | Beschrijving |
   | --- | --- |
   | Naam | De naam van de rapportsuite |
   | ID | De rapportsuite-id (rsid). Hiermee geeft u een unieke id op die alleen alfanumerieke tekens mag bevatten. Deze id kan na het maken niet meer worden gewijzigd. Adobe stelt het vereiste ID-voorvoegsel in en kan dit ook niet wijzigen. |
   | Voorvallen (afgelopen 90 dagen) | Hoeveel treffers heeft deze rapportsuite in de afgelopen 90 dagen ontvangen? |
   | Metrics | Hoeveel metriek worden bepaald in deze rapportreeks? |
   | Dimensies | Hoeveel dimensies worden gedefinieerd in dit rapportpakket? |
   | Analyse voor doel (A4T) ingeschakeld | Is deze rapportreeks wordt toegelaten voor [ Analytics voor Doel ](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t)? |
   | Marketingkanalen ingeschakeld | Is deze rapportreeks wordt toegelaten voor [ de Kanalen van de Marketing ](https://experienceleague.adobe.com/en/docs/analytics/components/marketing-channels/c-getting-started-mchannel)? |
   | Source Connector ingeschakeld | [ In ontwikkeling ] wordt deze rapportreeks toegelaten voor de [ Schakelaar van Adobe Analytics Source voor rapportreeksgegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/analytics) in Adobe Experience Platform? Met andere woorden, kan dit rapportenpakket naar Customer Journey Analytics worden gemigreerd via de Analytics Source Connector? |
   | Type agenda | Voor meer informatie, verwijs naar [ Douane Kalenders ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/custom-calendar#) |

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