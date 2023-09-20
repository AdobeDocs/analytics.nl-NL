---
description: Waarschuwingen beheren.
title: Overzicht van Waarschuwingsbeheer
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 637f498c8abee0f3c83780bccd0447f2e3a804e3
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Waarschuwingenbeheer

De Alarm Manager is zeer gestructureerd zoals [Segmentbeheer](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html) en de [Berekend metrisch beheer](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html).

![](assets/alert-manager.png)

## Toegang krijgen tot de Waarschuwingenmanager

1. Selecteer in Adobe Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Waarschuwingen**].

## Beschikbare handelingen in het venster Waarschuwingen

In het Alarmbeheer kunt u:

* Open de waarschuwingsBuilder door op **[!UICONTROL + Add]**.
* Tagwaarschuwingen. Zo kunt u ze ordenen voor gebruiksgemak.
* Waarschuwingen verwijderen.
* Namen van waarschuwingen wijzigen.
* Waarschuwingen goedkeuren.
* Waarschuwingen kopiëren.
* Waarschuwingen in-/uitschakelen.
* **Vernieuwen** een vervaldatum van een signalering. Wanneer een of meer waarschuwingen zijn geselecteerd, kunnen deze worden vernieuwd door op **[!UICONTROL Renew]**.Hierdoor worden de vervaldatums van de dieren verlengd tot één jaar vanaf de dag **[!UICONTROL Renew]** is aangeklikt, ongeacht de oorspronkelijke vervaldatum.
* Exporteer een waarschuwing naar een CSV-bestand.
* Bewerk waarschuwingen door te dubbelklikken op de titel van de waarschuwing.
* Zoeken naar waarschuwingen.
* Voeg waarschuwingen toe aan andere rapportsuites.
* Geef de eigenaar van een waarschuwing op of wijzig deze.
* Andere filters toevoegen.
* Een waarschuwing definiëren **vervaldatum**.

## Kolommen configureren

U kunt de informatie vormen die voor elke alarm in de manager van het Alarm wordt getoond door de kolommen te vormen die worden getoond.

De zichtbare kolommen configureren in het Alarmbeheer:

1. Selecteer in Adobe Analytics de optie **[!UICONTROL Components]** tab, dan selecteren **[!UICONTROL Alerts]**.

1. Selecteer in Waarschuwingsbeheer de optie **Kolommen aanpassen** pictogram ![Het pictogram Kolommen aanpassen](assets/customize-columns-icon.png)Selecteer vervolgens de kolommen die u wilt weergeven in het venster Waarschuwingen.

   De volgende kolommen zijn beschikbaar:

   | Kolomtitel | Beschrijving |
   |---|---|
   | Favorieten | Hiermee geeft u sterpictogrammen weer naast elke waarschuwing, zodat u waarschuwingen als favorieten kunt markeren. <!-- For more information, see [Mark calculated metrics as favorites](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md). --> |
   | Titel en beschrijving | Deze waarden worden opgegeven in de Alert Builder. Als u de titel en beschrijving wilt bewerken, selecteert u de titelkoppeling om de waarschuwingsconstructor te openen. |
   | Rapportsuite | Geeft aan in welke rapportsuite de waarschuwing het laatst is opgeslagen. |
   | Eigenaar | Hiermee wordt aangegeven wie de eigenaar van de waarschuwing is. Als niet-beheerder, kunt u slechts alarm zien u bezit of die met u werden gedeeld. |
   | Tags | Hier ziet u tags die zijn toegepast op de waarschuwing, door u of door personen die de waarschuwing met u hebben gedeeld. |
   | Gedeeld met | Hiermee geeft u personen of groepen (alleen beheerder) of Alle personen (alleen beheerder) weer waarmee u de waarschuwing hebt gedeeld. |
   | Datum gewijzigd | Geeft de datum aan waarop de waarschuwing voor het laatst is gewijzigd. |
   | Laatst gebruikt | **Opmerking:** Deze functionaliteit bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het proces van de release van de Customer Journey Analytics raadpleegt u [Release van de Customer Journey Analytics-functie](/help/release-notes/releases.md).<p>Geeft de datum weer waarop de waarschuwing voor het laatst is gebruikt.</p> <p>Deze informatie kan u helpen bepalen of een alarm voor gebruikers in uw organisatie waardevol is, of het zou moeten worden geschrapt.</p><p>Deze informatie omvat geen gebruik van API, Report Builder, of Data Warehouse.</p> |

   {style="table-layout:auto"}
