---
title: Aanpassing rapporteren in Adobe Analytics
description: Leer hoe u rapporten kunt aanpassen in Adobe Analytics
feature: Third-party Integration
exl-id: 8ea6ec3a-cfc6-4c14-966b-d245949451c7
source-git-commit: 6de20d2fbbab6ded6c92f0c6f3536671f4b2ae46
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 0%

---

# Rapporten aanpassen

Op platforms van derden, zoals Google Analytics, zijn verschillende aanpassingsopties beschikbaar. Met deze aanpassingen kan een gebruiker dashboards, aangepaste rapporten, opgeslagen rapporten en aangepaste waarschuwingen maken. Omdat Analysis Workspace gebruikers in staat stelt rapporten op te stellen op basis van een leeg canvas, worden de meeste aanpassingen rechtstreeks in het gereedschap ingebouwd.

Deze pagina gaat ervan uit dat de gebruiker een basiskennis heeft van het gebruik van [!UICONTROL Analysis Workspace]. Zie [Een basisrapport maken in Analysis Workspace voor gebruikers van Google Analytics](reports/create-report.md) als u het gereedschap nog niet kent in Adobe Analytics.

## Dashboards

De [!UICONTROL Analysis Workspace] architectuur wordt gebouwd gelijkaardig aan het concept dashboardwidgets. Projecten in [!UICONTROL Analysis Workspace] zijn ongeveer gelijk aan dashboards in Google Analytics. Visualisaties in [!UICONTROL Analysis Workspace] Dit is bij benadering het equivalent van widgets in Google Analytics.

### Inhoud toevoegen aan een project

1. Klik op de knop [!UICONTROL Visualizations] aan de linkerkant en sleep de gewenste visualisatie naar de werkruimte.
2. Klik op de knop [!UICONTROL Components] aan de linkerkant en sleep de gewenste afmetingen en afmetingen naar de visualisatie om deze te vullen met gegevens.
3. Sleep de randen van de visualisatie om het formaat te wijzigen en sleep de titel van de visualisatie om het te verplaatsen.

Alle Google Analytics-widgets zijn beschikbaar in [!UICONTROL Analysis Workspace]:

* De **Metrische widget** is ongeveer gelijk aan de [!UICONTROL Summary Number] visualisatie.
* De **Tijdlijnwidget** is ongeveer gelijk aan de [!UICONTROL Line] visualisatie.
* De **Geomap-widget** is ongeveer gelijk aan de [!UICONTROL Map] visualisatie.
* De **Tabelwidget** is ongeveer gelijk aan de [!UICONTROL Freeform Table] visualisatie.
* De **Schijfwidget** is ongeveer gelijk aan de [!UICONTROL Donut] visualisatie.
* De **Widget Bar** is ongeveer gelijk aan de [!UICONTROL Bar] visualisatie.

[!UICONTROL Analysis Workspace] bevat veel meer visualisatieopties om gegevens te presenteren op een manier die het beste aansluit bij uw rapportagebehoeften. Zie [Visualisaties in Analysis Workspace](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) in de Analyze Handleiding voor meer informatie.

### Projecten delen

Als u klaar bent met het toevoegen van inhoud aan een project, kunt u deze delen.

* Ga naar **[!UICONTROL Share > Share Project]**. Ontvangers zijn andere gebruikers in uw organisatie die een Adobe Analytics-account hebben.
* Ga naar **[!UICONTROL Share > Get Project Link]**. Hiervoor moet u zich binnen uw organisatie nog aanmelden bij Adobe Analytics.

### Projecten exporteren

Naast PDF [!UICONTROL Analysis Workspace] biedt een CSV-export aan.

1. Klikken *[!UICONTROL Share]* > *[!UICONTROL Send File Now]*, waarmee een modaal venster wordt geopend.
2. Geef het bestandstype en de ontvangers op.
3. Klik op [!UICONTROL Send Now].

## Aangepaste rapporten

Wanneer u een aangepast rapport maakt in Google Analytics, lijken de vereiste velden op de workflow voor het maken van een visualisatie in de werkruimte. De definities Dimension, Metriek en Filter zijn op verschillende platforms vergelijkbaar. In Analysis Workspace worden afmetingen en metriek niet uit een lijst geselecteerd, maar naar een vrije-vormtabel gesleept.

### Berekende metriek in douanerapporten

Aangepaste rapporten zijn een van de weinige gebieden in Google Analytics die het gebruik van berekende maatstaven toestaan. Omdat Analysis Workspace als een canvas werkt, werken berekende metriek retroactief en in elke context.

Een berekende metrische waarde maken:

1. Klik op de knop **+** pictogram bij de metrische lijst om het [!UICONTROL Calculated Metric Builder].
2. Geef de berekende metrische waarde een naam en geef een indeling op.
3. Sleep metrische componenten naar het definitiegebied en gebruik de vervolgkeuzelijsten tussen elke component om een operator aan te wijzen.
4. Zodra berekende metrisch de gewenste formule bevat, klik sparen om terug naar uw werkruimte te gaan.
5. Sleep de nieuw gedefinieerde berekende metrische waarde naar de werkruimte.

   Meer informatie over [Berekende cijfers](/help/components/c-calcmetrics/cm-overview.md) in de gebruikershandleiding van Componenten.

## Aangepaste waarschuwingen

Alarm is beschikbaar op beide platforms. Gebruik in Adobe Analytics het navigatiemenu voor de koptekst en ga naar *[!UICONTROL Components]* > *[!UICONTROL Alerts]*. Zie [Intelligente waarschuwingen](/help/components/c-alerts/intellligent-alerts.md) in de gebruikershandleiding van Componenten voor meer informatie.
