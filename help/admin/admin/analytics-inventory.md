---
description: De analytische inventaris gebruiken
title: Analytische inventarisatie
feature: Admin Tools
role: Admin
hide: true
hidefromtoc: true
exl-id: 9fc985c8-93d7-4838-9342-72a6268ef96f
source-git-commit: f9bbb764ab34310e575a308110f84270ee9d665a
workflow-type: tm+mt
source-wordcount: '1014'
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

Het doel van Analytics-inventarisatie is om u te helpen de volgende vragen te beantwoorden:

* Voor uw organisatie, welke activa (zoals rapportsuites, segmenten, gebruikers, werkruimteprojecten, gegevensvoer, etc.) moet u migreren en welke activa kunt u achterlaten?

* Nadat u hebt bepaald welk element moet worden gemigreerd:

   * Wilt u de middelen opschonen voordat u de upgrade uitvoert?

   * Moet u een of andere consolidatie van bedrijfsmiddelen uitvoeren als onderdeel van het proces?

   * Wat zou de verbeteringsopeenvolging voor uw activa moeten zijn?

   * Welke rapportsuites moet u eerst of het laatst bevorderen?

## Machtigingen

De Inventaris van de Analyse is beschikbaar aan gebruikers met de voorrechten van Admin van het Product van Adobe Analytics in [ Adobe Admin Console ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/admin-roles-in-analytics).

## Access Analytics Inventory

1. Klik op **[!UICONTROL Analytics Inventory]** in het menu **[!UICONTROL Admin]** . Of ga naar **[!UICONTROL All admin]** > **[!UICONTROL Analytics Inventory]** .

![ Analytics-Inventory-menu ](assets/an-inventory-menu.png)

1. Het hoofdscherm toont een uitgebreid overzicht van uw Adobe Analytics-omgeving:

   ![ Hoofd inventarisscherm ](assets/an_inventory.png)

   Dit scherm toont met name:

   * Het totale aantal Analysis Workspace- en Mobile Scorecard-projecten dat onder deze organisatie actief is, voor alle gebruikers.
   * Het totale aantal segmenten en berekende metriek die onder deze organisatie, over alle gebruikers actief zijn.
   * Het totale aantal basisrapportsuites dat is gedefinieerd. Virtuele rapportsuites zijn niet inbegrepen.
   * Als de functie Media Analytics actief is en als dat het geval is, in welke modus.
   * Het totale aantal gebruikers dat is gedefinieerd in deze organisatie.


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

* Welke rapportsuites hebben de meeste treffers in de afgelopen 90 dagen ontvangen?
* Welke rapportsuites hebben de afgelopen 90 dagen geen treffers ontvangen?
* Welke rapportsuites hebben het grootste aantal bepaalde dimensie?
* Welke rapportsuites hebben het grootste aantal bepaalde metriek?

De antwoorden op deze vragen zullen u een goed idee geven van welke verslagen de beste kandidaten voor migratie zijn.

>[!NOTE]
>
>Deze tabel wordt langzaam gevuld, één celwaarde tegelijk.


1. Als u rapportsuites wilt analyseren, navigeert u naar **[!UICONTROL Data configuration and collection]** > **[!UICONTROL Report suites]** en klikt u op **[!UICONTROL Analyze]** .

   ![ Lijst van rapportsuites ](assets/an_inv_rs.png)

   | Element | Beschrijving |
   | --- | --- |
   | Naam | De naam van de rapportsuite |
   | ID | De rapportsuite-id (rsid). Hiermee geeft u een unieke id op die alleen alfanumerieke tekens mag bevatten. Deze id kan na het maken niet meer worden gewijzigd. Adobe stelt het vereiste ID-voorvoegsel in en kan dit ook niet wijzigen. |
   | Voorvallen (afgelopen 90 dagen) | De metrische waarde &#39;Voorkomt&#39; toont het aantal treffers waar een bepaalde dimensie is ingesteld of geduurd. Hoeveel treffers heeft deze rapportsuite in de afgelopen 90 dagen ontvangen? |
   | Metrics | Hoeveel metriek worden bepaald in deze rapportreeks? |
   | Dimensies | Hoeveel dimensies worden gedefinieerd in dit rapportpakket? |
   | Analyse voor doel (A4T) ingeschakeld | Is deze rapportreeks toegelaten voor [ Analytics voor Doel ](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t)? |
   | Marketingkanalen ingeschakeld | Is deze rapportreeks toegelaten voor [ de Kanalen van de Marketing ](https://experienceleague.adobe.com/en/docs/analytics/components/marketing-channels/c-getting-started-mchannel)? |
   | Source Connector ingeschakeld | [ In ontwikkeling ] wordt deze rapportreeks toegelaten voor de [ Schakelaar van Adobe Analytics Source voor rapportreeksgegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/analytics) in Adobe Experience Platform? Met andere woorden, kan dit rapportenpakket naar Customer Journey Analytics worden gemigreerd via de Analytics Source Connector? |
   | Type agenda | Voor meer informatie, verwijs naar [ Douane Kalenders ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/custom-calendar#) |

#### Afmetingen analyseren

Dit scherm verstrekt een gedetailleerde mening van alle dimensies die voor een specifieke rapportreeks worden bepaald. In deze weergave kunt u de volgende vragen beantwoorden:

* Welke afmetingen zijn ingeschakeld voor deze rapportsuite?
* Wat zijn de top tien afmetingspunten voor de laatste 90 dagen voor deze afmeting?

1. Klik op de koppeling **[!UICONTROL Dimensions]** op de pagina Rapportsuite.

   | Element | Beschrijving |
   | --- | --- |
   | Naam | De naam van de dimensie |
   | ID | De dimensie-id. |
   | Type | Het type dimensie. Mogelijke waarden zijn onder andere Omzetten, Verkeer, Navigatie, Verkeersbronnen, Klanten, Datum of Adobe-productspecifieke afmetingen, zoals AEM, Publiek, Adobe Campaign, Mobiele app, enz. |
   | Beschrijving | Niet alle dimensies hebben beschrijvingen. |

1. Bepaal welke dimensies handig zijn om te migreren naar CJA.


#### Metrische gegevens analyseren

Dit scherm verstrekt een gedetailleerde die mening van alle metriek voor een specifieke rapportreeks wordt bepaald. In deze weergave kunt u de volgende vragen beantwoorden:

* Welke metriek worden toegelaten voor deze rapportreeks?
* Wat zijn de top tien van metriek de afgelopen 90 dagen?

1. Klik op de koppeling **[!UICONTROL Metrics]** op de pagina Rapportsuite.


   | Element | Beschrijving |
   | --- | --- |
   | Naam | De naam van metrisch |
   | ID | De metrische id. |
   | Type | Het type metrisch. Mogelijke waarden zijn onder andere Omzetten, Verkeer, Navigatie, Verkeersbronnen, Klanten, Datum of Adobe-productspecifieke afmetingen, zoals AEM, Publiek, Adobe Campaign, Mobiele app, enz. |
   | Beschrijving | Niet alle dimensies hebben beschrijvingen. |

1. Bepaal welke maatstaven handig zijn voor migratie naar CJA.

#### Exporteren naar CSV

1. Klik op **[!UICONTROL Export to CSV]** als u de lijst met rapportsuites, afmetingen of metriek wilt exporteren naar een CSV-bestand.

1. Het .csv-bestand wordt weergegeven in de map Downloads.

1. Open en sla deze op met een spreadsheettoepassing op uw apparaat.

#### Filteren, zoeken, ordenen en navigeren

* U kunt de tabel doorzoeken.
* Klik in de linkertrack op het pictogram Filter om te filteren op &quot;Type&quot;. Of klik op **[!UICONTROL Hide Filter]** .
* U kunt alle kolommen in oplopende of aflopende volgorde rangschikken (alleen enkele kolomvolgorde).
* U kunt op items in de broodkruimel klikken om naar een ander scherm te navigeren.

## Gebruikersbeheer {#user-management}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-user-management"
>title="Gebruikersbeheer"
>abstract="In deze sectie wordt het aantal gebruikers in uw Adobe Analytics-omgeving weergegeven."

<!-- markdownlint-enable MD034 -->

Gebruikersbeheer is beschikbaar in een latere versie van het Analytics-overzicht.