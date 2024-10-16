---
title: Wat is de Hub van de Report Builder in Adobe Analytics
description: Beschrijft de componenten van de Hub van de Report Builder
role: User
feature: Report Builder
type: Documentation
solution: Analytics
source-git-commit: eedabc6295f9b918e1e00b93993680e676c216c3
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# Report Builder Hub

Gebruik de hub van de Report Builder om, gegevensblokken tot stand te brengen bij te werken te schrappen en te beheren.

Het knooppunt Report Builder bevat de knoppen Maken en Beheren, de lijst OPDRACHTEN en de deelvensters SNEL BEWERKEN.

<img src="./assets/hub51.png" alt="Report Builder Hub"/>


## Knoppen Maken, Beheren en Schema

Met de knoppen Maken, Beheren en Schema kunt u nieuwe gegevensblokken maken, bestaande gegevensblokken beheren of gegevensblokken plannen.

## Deelvenster OPDRACHTEN

Gebruik het deelvenster OPDRACHTEN voor toegang tot opdrachten die compatibel zijn met de geselecteerde cellen of een vorige handeling.

### Opdrachten

| Weergegeven opdrachten | Beschikbaar als... | Doel |
|------|------------------|--------|
| Gegevensblok maken | Één of meerdere cellen wordt geselecteerd in het werkboek. | Wordt gebruikt om een gegevensblok te maken |
| Gegevensblok bewerken | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Wordt gebruikt om een gegevensblok te bewerken |
| Gegevensblok vernieuwen | De selectie bevat ten minste één gegevensblok. De opdracht vernieuwt alleen de gegevensblokken in de selectie. | Wordt gebruikt om een of meer gegevensblokken te vernieuwen |
| Alle gegevensblokken vernieuwen | Het werkboek bevat één of meerdere gegevensblokken. | Gebruikt om ALLE gegevensblokken in het werkboek te verfrissen |
| Werkmap verzenden |   | Verzend een werkboek op een programma. |
| Gegevensblok kopiëren | De geselecteerde cel of het geselecteerde celbereik maakt deel uit van een of meer gegevensblokken. | Wordt gebruikt om een gegevensblok te kopiëren |
| Gegevensblok verwijderen | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Wordt gebruikt om een gegevensblok te verwijderen |

## Deelvenster SNEL BEWERKEN

Wanneer u een of meer gegevensblokken in een spreadsheet selecteert, wordt het deelvenster SNEL BEWERKEN weergegeven met de Report Builder. U kunt het deelvenster SNEL BEWERKEN gebruiken om parameters in één gegevensblok te wijzigen of om parameters in meerdere gegevensblokken tegelijk te wijzigen.

![ Snel geeft paneel in Report Builder uit ](./assets/hub2.png)

De wijzigingen die u hebt aangebracht met de secties Snel bewerken zijn van toepassing op alle geselecteerde gegevensblokken.

### Reeksen rapporteren

Gegevensblokken trekken gegevens uit een geselecteerde rapportsuite. Als de veelvoudige gegevensblokken in een aantekenvel worden geselecteerd en zij trekken geen gegevens van de zelfde rapportreeks, **toont de 1} verbinding van de Suites van het Rapport *Veelvoud*.**

Wanneer u de rapportsuite wijzigt, nemen alle gegevensblokken in de selectie de nieuwe rapportsuite aan. Componenten in het gegevensblok komen overeen met de nieuwe rapportsuite op basis van bijvoorbeeld id ( ```evars``` ). Als een component niet in een gegevensblok wordt gevonden, wordt een waarschuwingsbericht getoond en de component wordt verwijderd uit het gegevensblok.

Om de rapportreeks te veranderen, selecteer een nieuwe rapportreeks van het drop-down menu.

![ de Hub die van de Report Builder het drop-down menu van de rapportreeks toont.](./assets/image16.png)

### Datumbereik

**[!UICONTROL Date range]** geeft het datumbereik voor de geselecteerde gegevensblokken weer. Als de veelvoudige gegevensblokken met veelvoudige datumwaaiers worden geselecteerd, **[!UICONTROL Date range]** verbindingsvertoningen *Veelvoud*.

### Filters

De **verbindingen van Filters** toont een summiere lijst van de filters die door de geselecteerde gegevensblokken worden gebruikt. Als de veelvoudige gegevensblokken met veelvoudige toegepaste filters worden geselecteerd, de **verbindingsvertoningen van Filters *Veelvoud*.**
