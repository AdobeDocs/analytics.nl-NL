---
description: Waarschuwingen beheren.
title: Overzicht van Waarschuwingsbeheer
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 373a1ecffafdcefe3c7b60954f14c2f3a5ca386d
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---

# Waarschuwingenbeheer

U kunt bestaande waarschuwingen beheren in het venster Waarschuwingen. U kunt verschillende beheertaken uitvoeren voor waarschuwingen, zoals labelen, hernoemen, verwijderen en meer.

De manager van het Alarm is zeer gestructureerd zoals de [ Manager van het Segment ](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html) en [ Berekende Metrische Manager ](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html).

![](assets/alert-manager.png)

## Waarschuwingen maken

Waarschuwingen maken via het Alarmbeheer:

1. Selecteer **[!UICONTROL Components]** > **[!UICONTROL Alerts]** om Alerts Manager in Adobe Analytics te openen.

   ![](assets/alert-manager.png)

1. Selecteer [!UICONTROL **toevoegen**] (of [!UICONTROL **creëren nieuw alarm**] als u geen bestaand alarm hebt).

1. Selecteer het type waarschuwing dat overeenkomt met de waarschuwing die u wilt maken:

   * [!UICONTROL **de gegevensalarm van Analytics**]: Een alarm om u op de hoogte te brengen wanneer de abnormale gebeurtenissen in uw gegevens voorkomen.

     Als u deze optie selecteert, ga met [ voort creeer alarm ](/help/analyze/analysis-workspace/c-intelligent-alerts/alert-builder.md) voor meer details over het creëren van alarm.

   * [!UICONTROL **het gebruiksalarm van de de vraag van de Server**]: Een alarm om u van het risico of het voorkomen van een overschrijding in uw de consumptie en verplichtingsgegevens van de servervraag op de hoogte te brengen.

     Als u deze optie selecteert, ga met [ waarschuwingen van het de vraaggebruik van de Server ](/help/admin/admin/c-server-call-usage/scu-alerts.md) verder.

     >[!NOTE]
     >
     >U moet een beheerder van de Analyse of een gebruiker met de toestemming van het de vraaggebruik van de Server zijn om toegang tot het gebruik van de servervraag te hebben.

## Bestaande waarschuwingen beheren

U kunt verschillende handelingen uitvoeren op bestaande waarschuwingen, zoals labelen, hernoemen, verwijderen enzovoort.

Bestaande waarschuwingen beheren in het Waarschuwingenbeheer:

1. Selecteer **[!UICONTROL Components]** > **[!UICONTROL Alerts]** om Alerts Manager in Adobe Analytics te openen.

   ![](assets/alert-manager.png)

1. Selecteer een of meer waarschuwingen die u wilt beheren.

   ![](assets/alert-manager-tasks.png)

1. Selecteer een van de volgende opties op de actiebalk:

   | Handeling | Functie |
   |---------|----------|
   | [!UICONTROL **Markering**] | Pas een tag toe op een waarschuwing. Hierdoor kunt u waarschuwingen ordenen voor gebruiksgemak. |
   | [!UICONTROL **Schrapping**] | Hiermee verwijdert u de waarschuwing. |
   | [!UICONTROL **anders noemen**] | Wijzigt de naam van de waarschuwing. |
   | [!UICONTROL **goedkeuren**] | Markeer de waarschuwing als Goedgekeurd. |
   | [!UICONTROL **Exemplaar**] | Hiermee maakt u een kopie (kopie) van de waarschuwing. |
   | [!UICONTROL **onbruikbaar maken**] | Hiermee wordt een waarschuwing uitgeschakeld die momenteel is ingeschakeld. |
   | [!UICONTROL **laat toe**] | Hiermee wordt een waarschuwing ingeschakeld die momenteel is uitgeschakeld. |
   | [!UICONTROL **Vernieuwen**] | Hiermee wordt de vervaldatum van de waarschuwing vernieuwd. Hiermee wordt de vervaldatum verlengd tot 1 jaar vanaf de dag waarop u deze optie hebt geselecteerd, ongeacht de oorspronkelijke vervaldatum. |
   | [!UICONTROL **Uitvoer aan CSV**] | Exporteert de waarschuwing naar een CSV-bestand. |

## Een waarschuwing bewerken

Een bestaande waarschuwing bewerken:

1. Selecteer **[!UICONTROL Components]** > **[!UICONTROL Alerts]** om Alerts Manager in Adobe Analytics te openen.

   ![](assets/alert-manager.png)

1. Selecteer de waakzame naam in de [!UICONTROL **Titel en beschrijvings**] kolom.

1. Bewerk de waarschuwing naar wens.

   Hier volgen enkele voorbeelden van wat u kunt doen wanneer u een waarschuwing bewerkt:

   * Waarschuwingen toevoegen aan andere rapportsuites
   * De eigenaar wijzigen
   * Filters bijwerken
   * De vervaldatum bijwerken

1. Bewerk het alarm, dan uitgezocht [!UICONTROL **sparen**].

## Kolommen configureren

U kunt de informatie vormen die voor elke alarm in de manager van het Alarm wordt getoond door de kolommen te vormen die worden getoond.

De zichtbare kolommen configureren in het Alarmbeheer:

1. Selecteer in Adobe Analytics de tab **[!UICONTROL Components]** en selecteer vervolgens **[!UICONTROL Alerts]** .

1. In de Waakzame manager, selecteer **kolommen** pictogram ![ aanpassen kolommen pictogram ](assets/customize-columns-icon.png), dan selecteer de kolommen die u in de manager van het Alarm wilt worden getoond.

   De volgende kolommen zijn beschikbaar:

   | Kolomtitel | Beschrijving |
   |---|---|
   | Titel en beschrijving | Deze waarden worden opgegeven in de Alert Builder. Als u de titel en beschrijving wilt bewerken, selecteert u de titelkoppeling om de waarschuwingsconstructor te openen. |
   | Favorieten | Hiermee geeft u sterpictogrammen weer naast elke waarschuwing, zodat u waarschuwingen als favorieten kunt markeren. <!-- For more information, see [Mark calculated metrics as favorites](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md). --> |
   | Type | Toont of het alarm een de gegevensalarm van de Analyse of een alarm van het de vraaggebruik van de Server is. |
   | Ingeschakeld | Hiermee wordt getoond of de waarschuwing is ingeschakeld of uitgeschakeld. |
   | Rapportsuite | Geeft aan in welke rapportsuite de waarschuwing het laatst is opgeslagen. |
   | Eigenaar | Hiermee wordt aangegeven wie de eigenaar van de waarschuwing is. Als niet-beheerder, kunt u slechts alarm zien u bezit of die met u werden gedeeld. |
   | Tags | Hier ziet u tags die zijn toegepast op de waarschuwing, door u of door personen die de waarschuwing met u hebben gedeeld. |
   | Vervaldatum | Geeft de datum en tijd weer waarop de waarschuwing is ingesteld op verlopen. |
   | Datum gewijzigd | Geeft de datum aan waarop de waarschuwing voor het laatst is gewijzigd. |

   {style="table-layout:auto"}

   <!-- When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul> -->


