---
description: Leer over hoe te om de Manager van de Activiteit van de Rapportering te gebruiken om capaciteitskwesties tijdens piekrapporteringstijden te diagnostiseren en te bevestigen.
title: Rapportageverzoeken annuleren in de Manager van de Activiteit van de Rapportering
feature: Admin Tools
source-git-commit: 4c4c38329b203b16d24ffc95f2a4580e7ca0ba0a
workflow-type: tm+mt
source-wordcount: '1333'
ht-degree: 0%

---

# Rapportageverzoeken annuleren in de Manager van de Activiteit van de Rapportering

{{release-limited-testing}}

De [!UICONTROL Reporting Activity Manager] kunnen beheerders rapportageaanvragen snel diagnosticeren en annuleren om problemen met de rapportagecapaciteit tijdens piekrapportagetijden op te lossen.

Overweeg het volgende wanneer het annuleren van rapporteringsverzoeken:

* U kunt specifieke verzoeken annuleren, alle verzoeken van een specifieke gebruiker annuleren of alle verzoeken met betrekking tot een specifiek project annuleren.

* Wanneer u verzoeken annuleert, kunt u ook verkiezen om verdere verzoeken voor een bepaalde tijdspanne te beperken.

* U kunt een aanvraag niet annuleren als de [!UICONTROL **Gebruiker**] de kolom van een verzoek toont zoals [!UICONTROL **Niet herkend**]. Wanneer dit voorkomt, betekent het dat de gebruiker in een login bedrijf is waar u geen administratieve toestemmingen hebt.

Voor meer informatie over het Melden van de Manager van de Activiteit, met inbegrip van zeer belangrijke voordelen en toestemmingsvereisten, zie [Overzicht van Activity Manager rapporteren](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md).

## Specifieke verzoeken annuleren

U kunt individuele verzoeken annuleren die een grote hoeveelheid rapporteringscapaciteit verbruiken.

1. Ga in Adobe Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Selecteer de rapportsuite waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Zie voor meer informatie over de gegevens die op deze pagina beschikbaar zijn [Rapportactiviteiten weergeven in de rapportagManager](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Selecteer de [!UICONTROL **Verzoeken**] selecteert u een of meer aanvragen.

   <!-- add screenshot -->

1. Selecteren [!UICONTROL **Aanvragen annuleren**].

   De [!UICONTROL **Annuleren _x_ verzoeken om rapportage**] wordt weergegeven.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Optioneel) Toekomstige verzoeken voor een bepaalde periode beperken:

   1. Schakel de optie in om [!UICONTROL **Verdere verzoeken beperken**]

      ![Verdere verzoeken beperken](assets/restrict-subsequent-requests.png)

   1. Kies een van de volgende opties:

      | Optie | -functie |
      |---------|----------|
      | [!UICONTROL **Gebruiker en project**] | De gebruikers verbonden aan de geselecteerde verzoeken zullen tijdelijk worden beperkt van het runnen van rapporteringsverzoeken voor de bijbehorende projecten. |
      | [!UICONTROL **Gebruiker**] | De gebruikers verbonden aan de geselecteerde verzoeken zullen tijdelijk worden beperkt van het maken van om het even welke rapporteringsverzoeken. |
      | [!UICONTROL **Project**] | De projecten verbonden aan de geselecteerde verzoeken zullen tijdelijk van alle rapporteringsverzoeken worden beperkt. |
      | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!-- double-check this --><p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

      {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Doorgaan met annulering**].

   In Analysis Workspace wordt een melding weergegeven waarin gebruikers worden geïnformeerd dat het verzoek is geannuleerd. Ga voor meer informatie over hoe dit in Analysis Workspace wordt weergegeven naar [Ervaring wanneer de gebruikers tot een geannuleerd rapport toegang hebben](#experience-when-users-access-a-cancelled-report).

## Aanvragen door gebruiker annuleren

U kunt alle aanvragen annuleren die aan een of meer gebruikers zijn gekoppeld.

1. Ga in Adobe Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Selecteer de rapportsuite waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Zie voor meer informatie over de gegevens die op deze pagina beschikbaar zijn [Rapportactiviteiten weergeven in de rapportagManager](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Selecteer de [!UICONTROL **Gebruikers**] selecteert u een of meer gebruikers.

   <!-- add screenshot -->

1. Selecteren [!UICONTROL **Aanvragen annuleren**].

   De [!UICONTROL **Annuleren _x_ rapporteert verzoeken van x gebruikers**] wordt weergegeven.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Optioneel) Toekomstige verzoeken voor een bepaalde periode beperken:

   1. Schakel de optie in om [!UICONTROL **Verdere verzoeken beperken**].

      ![Verdere verzoeken van gebruikers beperken](assets/restrict-subsequent-requests-user.png)

   1. Kies een van de volgende opties:

      | Optie | -functie |
      |---------|----------|
      | [!UICONTROL **Gebruiker en project**] | Geselecteerde gebruikers kunnen tijdelijk geen rapportageaanvragen voor de bijbehorende projecten indienen. |
      | [!UICONTROL **Gebruiker**] | Geselecteerde gebruikers kunnen tijdelijk geen rapportageaanvragen indienen. |
      | [!UICONTROL **Project**] | Projecten die aan de geselecteerde gebruikers zijn gekoppeld, worden beperkt tot alle rapportageaanvragen die door gebruikers worden ingediend. |
      | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!--double-check this--> <p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

      {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Doorgaan met annulering**].

   In Analysis Workspace wordt een melding weergegeven waarin gebruikers worden geïnformeerd dat het verzoek is geannuleerd. Ga voor meer informatie over hoe dit in Analysis Workspace wordt weergegeven naar [Ervaring wanneer de gebruikers tot een geannuleerd rapport toegang hebben](#experience-when-users-access-a-cancelled-report).

## Aanvragen door project annuleren

U kunt alle verzoeken annuleren die aan één of meerdere projecten worden geassocieerd.

1. Ga in Adobe Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Selecteer de rapportsuite waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Zie voor meer informatie over de gegevens die op deze pagina beschikbaar zijn [Rapportactiviteiten weergeven in de rapportagManager](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Selecteer de [!UICONTROL **Projecten**] selecteert u vervolgens een of meer projecten.

   <!-- add screenshot -->

1. Selecteren [!UICONTROL **Aanvragen annuleren**].

   De [!UICONTROL **Annuleren _x_ rapporteert verzoeken van x projecten**] wordt weergegeven.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Optioneel) Toekomstige verzoeken voor een bepaalde periode beperken:

   1. Schakel de optie in om [!UICONTROL **Verdere verzoeken beperken**].

      ![Verdere verzoeken beperken per project](assets/restrict-subsequent-requests-project.png)

   1. Kies een van de volgende opties:

      | Optie | -functie |
      |---------|----------|
      | [!UICONTROL **Gebruiker en project**] | Geselecteerde projecten worden tijdelijk beperkt van alle rapportageaanvragen die door de betrokken gebruikers worden ingediend. |
      | [!UICONTROL **Gebruiker**] | De gebruikers verbonden aan de geselecteerde projecten zullen worden beperkt van het indienen van om het even welke rapporteringsverzoeken. |
      | [!UICONTROL **Project**] | De geselecteerde projecten zullen tijdelijk van om het even welke rapporteringsverzoeken worden beperkt die door om het even welke gebruiker worden gemaakt. |
      | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!--double-check this--> <p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

      {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Doorgaan met annulering**].

   In Analysis Workspace wordt een melding weergegeven waarin gebruikers worden geïnformeerd dat het verzoek is geannuleerd. Ga voor meer informatie over hoe dit in Analysis Workspace wordt weergegeven naar [Ervaring wanneer de gebruikers tot een geannuleerd rapport toegang hebben](#experience-when-users-access-a-cancelled-report).

## Aanvragen door toepassing annuleren

U kunt alle aanvragen annuleren die aan een of meer toepassingen zijn gekoppeld. Wanneer u aanvragen die aan een toepassing zijn gekoppeld, annuleert, kunt u de aan die toepassing gekoppelde verzoeken gedurende een bepaalde periode verder beperken.

Toepassingen zijn onder andere:

* ANALYSIS WORKSPACE UI
* Werkruimte geplande projecten
* Report Builder
* Builder-gebruikersinterface: Segment, Berekende afmetingen, Annotaties, Soorten publiek, enzovoort.
* API-aanroepen van 1.4 of 2.0 API
* Intelligente waarschuwingen
* Delen met koppelingen van anderen
* Een andere toepassing die de Analyse meldend motor vraagt

Aanvragen door toepassing annuleren:

1. Ga in Adobe Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Selecteer de verbinding waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Zie voor meer informatie over de gegevens die op deze pagina beschikbaar zijn [Rapportactiviteiten weergeven in de rapportagManager](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Selecteer de [!UICONTROL **Toepassingen**] selecteert u een of meer toepassingen.

   <!-- add screenshot -->

1. Selecteren [!UICONTROL **Aanvragen annuleren**].

   De [!UICONTROL **Annuleren _x_ rapporteert verzoeken van x projecten**] wordt weergegeven.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Optioneel) Toekomstige verzoeken voor een bepaalde periode beperken:

   1. Schakel de optie in om [!UICONTROL **Verdere verzoeken beperken**]

      ![Verdere aanvragen beperken door toepassing](assets/restrict-subsequent-requests-application.png)

   1. Kies een van de volgende opties:

      | Optie | -functie |
      |---------|----------|
      | [!UICONTROL **Gebruiker en project**] | De geselecteerde toepassingen zullen tijdelijk van om het even welke rapporteringsverzoeken worden beperkt die door de bijbehorende gebruikers en de projecten worden gemaakt.<p>Dit is de minst beperkende optie.</p> |
      | [!UICONTROL **Gebruiker**] | Gebruikers die bij de geselecteerde toepassingen horen, kunnen geen rapportageaanvragen indienen. |
      | [!UICONTROL **Project**] | De projecten verbonden aan de geselecteerde toepassingen zullen van om het even welke rapporteringsverzoeken worden beperkt die door om het even welke gebruiker worden gemaakt. |
      | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!--double-check this--> <p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

      {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Doorgaan met annulering**].

   Er wordt een melding weergegeven in de toepassing (bijvoorbeeld in Analysis Workspace) om gebruikers te laten weten dat het verzoek is geannuleerd. Ga voor meer informatie over hoe dit in Analysis Workspace wordt weergegeven naar [Ervaring wanneer de gebruikers tot een geannuleerd rapport toegang hebben](#experience-when-users-access-a-cancelled-report).

## Ervaring wanneer de gebruikers tot een geannuleerd rapport toegang hebben

In Analysis Workspace zien gebruikers de volgende berichten wanneer ze proberen toegang te krijgen tot een rapport of visualisatie die wordt beïnvloed door een annulering:

### Bericht over het project

Wanneer de gebruikers proberen om tot een project toegang te hebben dat door een annulering wordt beïnvloed, zien zij een bericht die hen informeren dat het rapport tijdelijk beperkt is:

![Bericht van annulering van project](assets/workspace-canceled-report.png)

### Bericht over de visualisatie

Wanneer gebruikers proberen om tot een visualisatie toegang te hebben die door een annulering wordt beïnvloed, zien zij een bericht die hen informeren dat de gegevensverwerking voor het rapport tijdelijk beperkt is:

![Bericht van visualisatie-opheffing](assets/workspace-cancelled-visualization.png)