---
title: Deelvenster voor attributie
description: Het toewijzingspaneel in Analysis Workspace gebruiken en interpreteren.
feature: Attribution
role: User, Admin
exl-id: 96ce3cb9-7753-4ec0-b551-e70a1508e3b7
source-git-commit: 09124e3a176dab1e61ae54738abfd33e5be7082c
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Deelvenster voor attributie

Het [!UICONTROL Attribution] paneel is een gemakkelijke manier om een analyse te bouwen die diverse attributiemodellen vergelijkt. Het is een eigenschap in [Attribution IQ](../attribution/overview.md) die u een specifieke werkruimte geeft om attributiemodellen te gebruiken en te vergelijken.

>[!VIDEO](https://video.tv.adobe.com/v/23139/?quality=12)

## Een deelvenster met kenmerken maken

1. Klik op het deelvensterpictogram aan de linkerkant.
1. Sleep het [!UICONTROL Attribution] paneel in uw Project van Analysis Workspace.

   ![Nieuw deelvenster voor kenmerken](assets/Attribution_Panel_1.png)

1. Voeg metrisch toe dat u om het even welke afmeting aan attributen wilt kenmerken en toevoegen tegen. Voorbeelden zijn Marketingkanalen of aangepaste afmetingen, zoals interne promoties.

   ![Dimensie en metrisch selecteren](assets/attribution_panel2.png)

1. Selecteer [attributiemodellen en terugkijkvenster](../attribution/models.md) u wilt vergelijken.

1. Het deelvenster Kenmerken retourneert een uitgebreide set gegevens en visualisaties die de kenmerk voor de geselecteerde dimensie en de metrische waarde met elkaar vergelijken.

   ![Attributievisualisaties](assets/attr_panel_vizs.png)

## Attributievisualisaties

* **Totaal metrisch**: Het totale aantal omzettingen dat zich tijdens het rapporttijdvenster voordeed. Dit zijn de omzettingen die over de afmeting worden toegeschreven u selecteerde.
* **Vergelijkingsbalk** voor kenmerken: Vergelijkt visueel de toegeschreven omzettingen over elk van de afmetingspunten van uw geselecteerde afmeting. Elke staafkleur vertegenwoordigt een afzonderlijk attributiemodel.
* **Vergelijkingstabel** kenmerk: Hiermee worden dezelfde gegevens weergegeven als het staafdiagram, dat als een tabel wordt weergegeven. Wanneer u verschillende kolommen of rijen in deze tabel selecteert, worden het staafdiagram en diverse andere visualisaties in het deelvenster gefilterd. Deze lijst doet gelijkaardig aan een andere Lijst Freeform in Werkruimte - toestaand u om componenten zoals metriek, segmenten, of onderverdelingen toe te voegen.
* **Overlap diagram**: Een tekening van Venn die de hoogste drie afmetingspunten toont en hoe vaak zij gezamenlijk aan een omzetting deelnemen. De grootte van de ballonoverlapping geeft bijvoorbeeld aan hoe vaak conversies hebben plaatsgevonden wanneer een bezoeker aan beide dimensie-items werd blootgesteld. Als u andere rijen in de aangrenzende tabel Freeform selecteert, wordt de visualisatie bijgewerkt met uw selectie.
* **Prestatiegegevens**: Hiermee kunt u maximaal drie kenmerkingsmodellen visueel vergelijken met behulp van een spreidingsgrafiek.
* **Trended Performance**: Standaard wordt de trend van de conversieprestaties weergegeven op basis van het toewijzingsmodel voor de eerste dimensie in de aangrenzende tabel Freeform. U kunt verschillende afmetingsrijen in de lijst van Freeform selecteren om de trend voor de geselecteerde afmetingen (zoals Totale Ontvangsten voor elk attributiemodel voor Sociale Campagnes en Betaald Onderzoek) te tonen. Afwisselend, kunt u cellen in de kolommen voor om het even welke metrische en attributietype combinaties in de lijst van de Vrije vorm selecteren om de trended prestaties door afmetingswaarde voor de gespecificeerde attributiemodellen (zoals Totale Inkomsten door het Kanaal van de Marketing die laatste Aanraking en Eerste Toekenning gebruiken) te zien.
* **Stroom**: Hiermee kunt u zien welke kanalen het meest worden gebruikt en in welke volgorde de bezoeker op reis is.
