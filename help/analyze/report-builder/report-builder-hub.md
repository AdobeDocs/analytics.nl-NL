---
title: Wat is de Report Builder Hub in Adobe Analytics
description: Beschrijft de componenten van de Hub van Report Builder
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: e18381ea-b7d4-4d7a-9ded-23b2d06fa204
source-git-commit: d3d74042f6c282db490483393f4b58cddd6b1525
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 1%

---

# Report Builder Hub

Met de Report Builder-hub kunt u gegevensblokken maken, bijwerken, verwijderen en beheren.

De Report Builder-hub bevat de knoppen Maken, Beheren en Planning, het deelvenster OPDRACHTEN en het deelvenster SNEL BEWERKEN.

<img src="./assets/hub51.png" alt="Report Builder Hub"/>


## Knoppen Maken, Beheren en Schema

Met de knoppen Maken, Beheren en Schema kunt u nieuwe gegevensblokken maken, bestaande gegevensblokken beheren of gegevensblokken plannen.

## Deelvenster OPDRACHTEN

Gebruik het deelvenster OPDRACHTEN voor toegang tot opdrachten die compatibel zijn met de geselecteerde cellen of een vorige handeling.

### Opdrachten

| Weergegeven opdrachten | Beschikbaar als... | Doel |
|------|------------------|--------|
| Gegevensblok bewerken | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Wordt gebruikt om een gegevensblok te bewerken |
| Gegevensblok vernieuwen | De selectie bevat ten minste één gegevensblok. Met deze opdracht vernieuwt u alleen de gegevensblokken in de selectie. | Wordt gebruikt om een of meer gegevensblokken te vernieuwen |
| Alle gegevensblokken vernieuwen | Het werkboek bevat één of meerdere gegevensblokken. | Gebruikt om ALLE gegevensblokken in het werkboek te verfrissen |
| Werkmap verzenden |   | Verzend een werkboek op een programma. |
| Gegevensblok kopiëren | De geselecteerde cel of het geselecteerde celbereik maakt deel uit van een of meer gegevensblokken. | Wordt gebruikt om een gegevensblok te kopiëren |
| Gegevensblok knippen |   | Wordt gebruikt om een gegevensblok te knippen |
| Gegevensblok verwijderen | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Wordt gebruikt om een gegevensblok te verwijderen |

## Deelvenster SNEL BEWERKEN

Wanneer u een of meer gegevensblokken in een spreadsheet selecteert, geeft Report Builder het deelvenster SNEL BEWERKEN weer. U kunt het deelvenster SNEL BEWERKEN gebruiken om parameters in één gegevensblok te wijzigen of om parameters in meerdere gegevensblokken tegelijk te wijzigen.

![&#x200B; Snel geeft paneel in Report Builder uit &#x200B;](./assets/hub2.png)

De wijzigingen die u hebt aangebracht met de secties Snel bewerken zijn van toepassing op alle geselecteerde gegevensblokken.

### Reeksen rapporteren

Gegevensblokken trekken gegevens uit een geselecteerde rapportsuite. Als de veelvoudige gegevensblokken in een aantekenvel worden geselecteerd en zij trekken geen gegevens van de zelfde rapportreeks, **toont de 1&rbrace; verbinding van de Suites van het Rapport** Veelvoud *.*

Wanneer u de rapportsuite wijzigt, nemen alle gegevensblokken in de selectie de nieuwe rapportsuite aan. Componenten in het gegevensblok komen overeen met de nieuwe rapportsuite op basis van bijvoorbeeld id ( ```evars``` ). Als een component niet in een gegevensblok wordt gevonden, wordt een waarschuwingsbericht getoond en de component wordt verwijderd uit het gegevensblok.

Om de rapportreeks te veranderen, selecteer een nieuwe rapportreeks van het drop-down menu.

![&#x200B; de Hub van Report Builder die het drop-down menu van de rapportreeks toont.](./assets/image16.png)

### Datumbereik

**[!UICONTROL Date range]** geeft het datumbereik voor de geselecteerde gegevensblokken weer. Als de veelvoudige gegevensblokken met veelvoudige datumwaaiers worden geselecteerd, **[!UICONTROL Date range]** verbindingsvertoningen *Veelvoud*. [Meer informatie](/help/analyze/report-builder/select-date-range.md)

### Segmenten

De **verbinding van Segmenten** toont een summiere lijst van de segmenten die door de geselecteerde gegevensblokken worden gebruikt. Als de veelvoudige gegevensblokken met veelvoudige toegepaste segmenten worden geselecteerd, de **verbindingsvertoningen van segmenten** Veelvoudig *.* [Meer informatie](/help/analyze/report-builder/work-with-segments.md)
