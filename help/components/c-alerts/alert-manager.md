---
description: Waarschuwingen beheren.
title: Overzicht van Waarschuwingsbeheer
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 49324ef7fd45adeef2c31167d0444a7e67041d6d
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Waarschuwingenbeheer

De manager van het Alarm is zeer gestructureerd zoals de [ Manager van het Segment ](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html) en [ Berekende Metrische Manager ](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html).

![](assets/alert-manager.png)

## Toegang krijgen tot de Waarschuwingenmanager

1. In Adobe Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **Alarm**].

## Beschikbare handelingen in het venster Waarschuwingen

In het Alarmbeheer kunt u:

* Klik op **[!UICONTROL + Add]** om de waarschuwingsfunctie van Builder te openen.
* Tagwaarschuwingen. Zo kunt u ze ordenen voor gebruiksgemak.
* Waarschuwingen verwijderen.
* Namen van waarschuwingen wijzigen.
* Waarschuwingen goedkeuren.
* Waarschuwingen kopiëren.
* Waarschuwingen in-/uitschakelen.
* **vernieuw** een waakzame vervaldatum. Wanneer een of meer waarschuwingen zijn geselecteerd, kunnen deze worden vernieuwd door op **[!UICONTROL Renew]** te klikken. Hierdoor worden de vervaldatums verlengd tot 1 jaar vanaf de dag waarop op **[!UICONTROL Renew]** is geklikt, ongeacht de oorspronkelijke vervaldatum.
* Exporteer een waarschuwing naar een CSV-bestand.
* Bewerk waarschuwingen door te dubbelklikken op de titel van de waarschuwing.
* Zoeken naar waarschuwingen.
* Voeg waarschuwingen toe aan andere rapportsuites.
* Geef de eigenaar van een waarschuwing op of wijzig deze.
* Andere filters toevoegen.
* Bepaal een waakzame **vervaldatum**.

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


