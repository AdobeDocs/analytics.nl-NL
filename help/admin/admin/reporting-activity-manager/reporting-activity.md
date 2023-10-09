---
description: Leer over hoe te om de Manager van de Activiteit van de Rapportering te gebruiken om capaciteitskwesties tijdens piekrapporteringstijden te diagnostiseren en te bevestigen.
title: Activity Manager rapporteren
feature: Admin Tools
mini-toc-levels: 3
exl-id: f638c6a9-1c2c-4936-a787-281269f95afc
source-git-commit: 0e03379550808e5be3e86f0f9ddbbedd026d4910
workflow-type: tm+mt
source-wordcount: '1564'
ht-degree: 1%

---

# Rapportactiviteiten weergeven in de rapportagManager

{{release-limited-testing}}

De [!UICONTROL Reporting Activity Manager] stelt beheerders in staat om problemen met de rapportcapaciteit tijdens piekrapportagetijden snel te diagnosticeren en op te lossen.

Voor meer informatie over het Melden van de Manager van de Activiteit, met inbegrip van zeer belangrijke voordelen en toestemmingsvereisten, zie [Overzicht van Activity Manager rapporteren](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md).

## Rapportactiviteiten voor alle rapportsuites weergeven {#view-all-report-suites}

1. Ga in Adobe Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

   Een lijst van uw toegelaten reeksen van het basisrapport wordt getoond.

   ![rapportwachtrij](/help/admin/admin/assets/reporting-activity1.png)

1. (Optioneel) U kunt de lijst met rapportsuites opzoeken of filteren:

   * Gebruik het onderzoeksgebied aan onderzoek naar een specifieke rapportreeks. Typ de naam of id van de rapportsuite en de lijst met updates van rapportsuites terwijl u typt.

   * Selecteer de [!UICONTROL **Filter**] pictogram ![Filterpictogram](assets/filter-icon.png) om de lijst met filteropties uit te vouwen. U kunt filteren op [!UICONTROL **Favorieten**] of [!UICONTROL **Status**].

     Als u een rapportsuite als favoriet wilt markeren, selecteert u het sterpictogram links van de naam van de rapportsuite.

<!-- (does this option still exist?) 1. (Optional) Select **[!UICONTROL Refresh]** at the top-right to refresh the data. -->

1. De gebruiksinformatie van de mening over elke rapportreeks. U kunt een kolomkop selecteren om de tabel op die kolom te sorteren.

   De volgende kolommen zijn beschikbaar:

   | UI-element | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Report Suite]** | De set met basisrapporten waarvan u de rapportactiviteiten controleert. |
   | **[!UICONTROL Virtual report suites]** | Toont alle virtuele rapportsuites die in deze reeks van het basisrapport van toepassing zijn. De virtuele rapportsuites voegen ingewikkeldheid aan rapporteringsverzoeken toe toe toe te schrijven aan extra niveaus van toegepaste filtratie en segmentatie. Alle verzoeken die uit de virtuele rapportreeksen komen worden gecombineerd en neer aan de reeks van het basisrapport.<p>Bijvoorbeeld, als u 10 verzoeken hebt die uit 5 VRSs komen, is dat 50 verzoeken bij de het rapportreeks van het basisniveau. Op deze manier kun je snel de capaciteit raken. |
   | **[!UICONTROL Capacity utilization]** | Het percentage van de rapporteringscapaciteit van de rapportreeks die, in echt - tijd wordt gebruikt. <p>**Opmerking** Zelfs een gebruikscapaciteit van 100% betekent niet noodzakelijk dat u begint rapporteringsverzoeken te annuleren. De gebruikscapaciteit van 100% kan gezond zijn als de gemiddelde wachttijd redelijk is. De 100% gebruikscapaciteit zou op een probleem kunnen wijzen als het aantal in de rij gevormde verzoeken ook groeit.</p> |
   | **[!UICONTROL Queued requests]** | Het aantal verzoeken dat moet worden verwerkt. <!-- ??? --> |
   | **[!UICONTROL Queue wait time]** | De gemiddelde wachttijd op elk verzoek om te verwerken. <!-- ???? --> |
   | **[!UICONTROL Status]** | De mogelijke statussen zijn: <ul><li>[!UICONTROL **Actief**] (blauw): de rapporten zijn in werking gesteld op de rapportreeks en het wordt gecontroleerd op activiteit.</li><li>[!UICONTROL **Inactief**] (grijs): er zijn nooit rapporten uitgevoerd over de rapportsuite. Deze status wordt alleen weergegeven wanneer de rapportsuites voor het eerst worden gemaakt.</li></ul> |

   {style="table-layout:auto"}

## Rapportactiviteiten weergeven voor één rapportsuite

1. Selecteer in Adobe Analytics [!UICONTROL **Beheerder**] > [!UICONTROL **Activity Manager rapporteren**].

1. Selecteer de gekoppelde titel van de rapportsuite waarvan u de details wilt weergeven.

   De gegevens van de rapportactiviteit worden getoond voor de rapportreeks die u selecteerde.

   <!-- Need to update this screenshot: ![report suite](assets/indiv-report-ste.png) -->

1. Gebruik de beschikbare grafieken en de lijst om rapporteringsactiviteit in de rapportreeks te begrijpen.

   * [Grafieken weergeven](#view-graphs)

   * [Tabel weergeven](#view-data-in-the-table)

### Grafieken weergeven

De volgende grafieken zijn beschikbaar om u te helpen de activiteit begrijpen die in de rapportreeks gebeurt. Als grafieken niet zichtbaar zijn, selecteert u de optie [!UICONTROL **Grafieken tonen**] knop.

#### Gebruiksgrafiek {#utilization}

De grafiek van het Gebruik toont hoe het rapporteringsgebruik voor de geselecteerde rapportreeks over de laatste 2 uren.

* Op de x-as wordt de capaciteit van het rapportgebruik gedurende de laatste 2 uur weergegeven.
* Op de y-as wordt het percentage van de rapportgebruikscapaciteit per minuut weergegeven.
* U kunt de muisaanwijzer boven het diagram houden om bepaalde punten in de tijd te bekijken waar het percentage van de gebruikscapaciteit het hoogst was gedurende die minuut.

  ![gebruikslijn](assets/utilization-graph.png)

#### Afzonderlijke gebruikersgrafiek

In de grafiek Afzonderlijke gebruikers wordt de rapportactiviteit voor de geselecteerde rapportsuite gedurende de laatste twee uur weergegeven.

* Op de x-as ziet u een tijdframe van 2 uur.
* Op de y-as ziet u het aantal gebruikers dat rapportageverzoeken per minuut heeft ingediend.
* U kunt de muisaanwijzer boven het diagram houden om op bepaalde tijdstippen te zien waar het maximumaantal gebruikers het hoogst was gedurende die minuut.

  ![Afzonderlijke gebruikersgrafiek](assets/distinct-users-graph.png)

<!--

#### Requests graph

The Requests graph shows the number of processed and completed requests for the selected report suite over the last 2 hours. 

* The x-axis shows a 2-hour time frame.
* The y-axis shows the number of processed requests (in purple) and completed requests (in green), by minute.
* You can hover over the chart to view points in time where the maximum number of requests was highest for that minute.

   ![Distinct Users graph](assets/requests-graph.png)

#### Queueing graph

The Queueing graph shows the average queue wait time (in seconds) for reporting requests for the selected report suite over the last 2 hours. 

* The x-axis shows a 2-hour time frame.
* The y-axis shows the average wait time (in seconds).
* You can hover over the chart to view points in time where the maximum average wait time was highest for that minute.

   ![Distinct Users graph](assets/queueing-graph.png)

-->

### Tabel weergeven {#view-table}

U kunt ervoor kiezen om gegevens weer te geven door een van de volgende tabbladen boven aan de gegevenstabel te kiezen: [!UICONTROL **Verzoek**], [!UICONTROL **Gebruiker**], [!UICONTROL **Project**], of [!UICONTROL **Toepassing**].

>[!TIP]
>
>U kunt [!UICONTROL **Grafieken verbergen**] alleen de tabel weergeven.

![tabbladen](assets/indiv-report-ste-table-tabs.png)

#### Gegevens op verzoek weergeven

Wanneer u [!UICONTROL **Verzoek**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Aanvraag-id**] | Kan voor het oplossen van problemendoeleinden worden gebruikt. |
| [!UICONTROL **Tijdsduur**] | Hoe lang de aanvraag is uitgevoerd. |
| [!UICONTROL **Begintijd**] | Wanneer de aanvraag is begonnen met de verwerking (op basis van de lokale tijd van de beheerder). |
| [!UICONTROL **Wacht op tijd**] | Hoe lang het verzoek heeft gewacht alvorens wordt verwerkt. In het algemeen bij &quot;0&quot; wanneer er voldoende capaciteit is. |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door de [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende afmetingen, Annotaties, Soorten publiek, enzovoort.</li><li>API-aanroepen van 1.4 of 2.0 API</li><li>Intelligente waarschuwingen</li></ul> |
| [!UICONTROL **Gebruiker**] | De gebruiker die de aanvraag heeft gestart. Als de waarde van deze kolom [!UICONTROL **Niet herkend**], betekent dit dat de gebruiker zich in een login bedrijf bevindt waar u geen administratieve toestemmingen hebt. |
| [!UICONTROL **Project**] | Opgeslagen projectnamen voor Workspace, API-rapport-id&#39;s, enz. (Metagegevens kunnen per toepassing verschillen.) |
| [!UICONTROL **Status**] | Statusindicatoren: <ul><li>**Wordt uitgevoerd**: Verzoek wordt momenteel verwerkt.</li><li>**In behandeling**: De aanvraag is in afwachting van verwerking.</li></ul> |
| [!UICONTROL **Complexiteit**] | Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken. Mogelijke waarden zijn: <ul><li>[!UICONTROL **Laag**]</li><li>[!UICONTROL **Normaal**]</li><li>[!UICONTROL **Hoog**]</li></ul>Deze waarde wordt beïnvloed door de waarden in de volgende kolommen:<ul><li>[!UICONTROL **Maandgrenzen**]</li><li>[!UICONTROL **Kolommen**]</li><li>[!UICONTROL **Segmenten**]</li></ul> |
| [!UICONTROL **Maandgrenzen**] | Het aantal maanden dat in een verzoek is opgenomen. Dit vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Kolommen**] | Het aantal metriek en onderverdelingen in het verzoek. Dit vergroot de complexiteit van het verzoek. |
| [!UICONTROL **Segmenten**] | Het aantal segmenten dat op de aanvraag wordt toegepast. Dit vergroot de complexiteit van het verzoek. |

{style="table-layout:auto"}

#### Gegevens weergeven per gebruiker

Wanneer u [!UICONTROL **Gebruiker**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Gebruiker**] | De gebruiker die de aanvraag heeft gestart. Als de waarde van deze kolom [!UICONTROL **Niet herkend**], betekent dit dat de gebruiker zich in een login bedrijf bevindt waar u geen administratieve toestemmingen hebt. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal aanvragen dat door de gebruiker wordt geïnitieerd. |
| [!UICONTROL **Aantal projecten**] | Het aantal projecten verbonden aan de gebruiker. <!-- ??? --> |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door de [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende afmetingen, Annotaties, Soorten publiek, enzovoort.</li><li>API-aanroepen van 1.4 of 2.0 API</li><li>Intelligente waarschuwingen</li></ul> |
| [!UICONTROL **Gemiddelde complexiteit**] | De gemiddelde ingewikkeldheid van verzoeken die door de gebruiker in werking worden gesteld. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p><ul><li>[!UICONTROL **Gem. maandgrenzen**]</li><li>[!UICONTROL **Gem. kolommen**]</li><li>[!UICONTROL **Gem-segmenten**]</li></ul> |
| [!UICONTROL **Gem. maandgrenzen**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Dit vergroot de gemiddelde complexiteit van het verzoek. |
| [!UICONTROL **Gem. kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Dit vergroot de gemiddelde complexiteit. |
| [!UICONTROL **Gem-segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Dit vergroot de gemiddelde complexiteit. |

{style="table-layout:auto"}

#### Gegevens weergeven per project

Wanneer u [!UICONTROL **Project**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Project**] | Het project waar de vragen werden geïnitieerd. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal verzoeken verbonden aan het project. |
| [!UICONTROL **Aantal gebruikers**] | Het aantal gebruikers dat aan het project is gekoppeld. <!-- ??? --> |
| [!UICONTROL **Toepassing**] | De toepassingen die worden ondersteund door de [!UICONTROL Reporting Activity Manager] zijn: <ul><li>ANALYSIS WORKSPACE UI</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende afmetingen, Annotaties, Soorten publiek, enzovoort.</li><li>API-aanroepen van 1.4 of 2.0 API</li><li>Intelligente waarschuwingen</li></ul> |
| [!UICONTROL **Gemiddelde complexiteit**] | De gemiddelde complexiteit van aanvragen die in het project zijn opgenomen. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p><ul><li>[!UICONTROL **Gem. maandgrenzen**]</li><li>[!UICONTROL **Gem. kolommen**]</li><li>[!UICONTROL **Gem-segmenten**]</li></ul> |
| [!UICONTROL **Gem. maandgrenzen**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Dit vergroot de gemiddelde complexiteit van het verzoek. |
| [!UICONTROL **Gem. kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Dit vergroot de gemiddelde complexiteit. |
| [!UICONTROL **Gem-segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Dit vergroot de gemiddelde complexiteit. |

{style="table-layout:auto"}

#### Gegevens weergeven per toepassing

Wanneer u [!UICONTROL **Toepassing**] de volgende kolommen zijn beschikbaar in de tabel:

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL **Toepassing**] | De toepassing waar de query&#39;s zijn gestart. |
| [!UICONTROL **Aantal verzoeken**] | Het aantal aanvragen dat aan de toepassing is gekoppeld. |
| [!UICONTROL **Aantal gebruikers**] | Het aantal gebruikers dat aan de toepassing is gekoppeld. <!--???--> |
| [!UICONTROL **Aantal projecten**] | Het aantal projecten verbonden aan de toepassing. <!--???--> |
| [!UICONTROL **Gemiddelde complexiteit**] | De gemiddelde ingewikkeldheid van verzoeken verbonden aan de toepassing. <p>Niet alle verzoeken vereisen de zelfde hoeveelheid tijd om te verwerken. De complexiteit van aanvragen kan u helpen een algemeen idee te geven van de tijd die nodig is om de aanvraag te verwerken.</p><p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:</p>De waarde in deze kolom is gebaseerd op een score die wordt bepaald door de waarden in de volgende kolommen:<ul><li>[!UICONTROL **Gem. maandgrenzen**]</li><li>[!UICONTROL **Gem. kolommen**]</li><li>[!UICONTROL **Gem-segmenten**]</li></ul> |
| [!UICONTROL **Gem. maandgrenzen**] | Het gemiddelde aantal maanden dat in de verzoeken is opgenomen. Dit vergroot de gemiddelde complexiteit van het verzoek. |
| [!UICONTROL **Gem. kolommen**] | Het gemiddelde aantal metriek en onderverdelingen in de inbegrepen verzoeken. Dit vergroot de gemiddelde complexiteit. |
| [!UICONTROL **Gem-segmenten**] | Het gemiddelde aantal segmenten dat wordt toegepast op de opgenomen aanvragen. Dit vergroot de gemiddelde complexiteit. |

{style="table-layout:auto"}

<!--

### Filter

You can filter the table by Application (see list in the table below), by User, and by Project.

![filter](/help/admin/admin/assets/filter.png)

### Summary Numbers {#summary}

![filter](/help/admin/admin/assets/summary_numbers.png)

The Summary Numbers show the following information:

| Summary Number | Description |
| --- | --- |
| [!UICONTROL **Users**] | The number of users that are currently sending reporting requests to this report suite. |
| [!UICONTROL **Projects**] | Workspace projects, Report Builder workbooks, etc.  | 
| [!UICONTROL **Queries**] | The number of queries currently running. |
| [!UICONTROL **Average Wait Time**] | The average wait time for all running queries.  |
| [!UICONTROL **Usage Capacity**] | The current usage capacity for this report suite. |

{style="table-layout:auto"}

-->


