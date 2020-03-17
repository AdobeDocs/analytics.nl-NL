---
title: Aanpassing rapporteren in Adobe Analytics
description: Leer hoe u rapporten kunt aanpassen in Adobe Analytics
translation-type: tm+mt
source-git-commit: 757cea821bae49fabe819a65b921797070d328fc

---


# Rapporten aanpassen

Op externe platforms, zoals Google Analytics, zijn verschillende aanpassingsopties beschikbaar. Met deze aanpassingen kan een gebruiker dashboards, aangepaste rapporten, opgeslagen rapporten en aangepaste waarschuwingen maken. Omdat de Werkruimte van de Analyse gebruikers toestaat om rapporten van een leeg canvas te bouwen, worden de meeste aanpassingen direct gebouwd in het hulpmiddel.

Deze pagina veronderstelt de gebruiker een basiskennis van het gebruiken van de Werkruimte van de Analyse heeft. Zie Een basisrapport [maken in de Analyse Workspace voor Google Analytics-gebruikers](reports/create-report.md) als u nog niet bekend bent met het hulpprogramma in Adobe Analytics.

## Dashboards

De architectuur van de Werkruimte van de analyse wordt gebouwd gelijkaardig aan het concept dashboardwidgets. Projecten in de analysewerkruimte zijn ongeveer gelijk aan dashboards in Google Analytics. Visualisaties in de analysewerkruimte zijn ongeveer equivalent aan widgets in Google Analytics.

### Inhoud toevoegen aan een project

1. Klik op het pictogram Visualisaties aan de linkerkant en sleep de gewenste visualisatie naar de werkruimte.
2. Klik op het pictogram Componenten aan de linkerkant en sleep de gewenste afmetingen en afmetingen naar de visualisatie om deze te vullen met gegevens.
3. Sleep de randen van de visualisatie om het formaat te wijzigen en sleep de titel van de visualisatie om het te verplaatsen.

Alle Google Analytics-widgets zijn beschikbaar in de analysewerkruimte:

* De **metrische widget** is ongeveer gelijk aan de visualisatie Samenvattingsnummer.
* De **tijdlijnwidget** is ongeveer gelijk aan de lijnvisualisatie.
* De **Geomap-widget** is ongeveer gelijk aan de Kaartweergave.
* De **tabelwidget** is ongeveer gelijk aan de visualisatie van de tabel voor vrije vorm.
* De **schijfwidget** is ongeveer gelijk aan de Donut-visualisatie.
* De **Bar-widget** is ongeveer gelijk aan de Bar-visualisatie.

De analysewerkruimte bevat veel meer visualisatieopties om gegevens te presenteren op een manier die het beste aansluit bij uw rapportagebehoeften. Zie [Visualisaties in de Werkruimte](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) van de Analyse in de Gids van de Gebruiker van de Analyse voor meer informatie.

### Projecten delen

Als u klaar bent met het toevoegen van inhoud aan een project, kunt u deze delen.

* Als u het project met uw collega&#39;s wilt delen, gaat u naar Delen > Project delen. Ontvangers zijn andere gebruikers in uw organisatie die Adobe Analytics-accounts hebben.
* Als u uw project wilt delen via een koppeling, gaat u naar Delen > Projectkoppeling ophalen. Hiervoor moet u zich binnen uw organisatie nog aanmelden bij Adobe Analytics.

### Projecten exporteren

Naast PDF biedt de analysewerkruimte een CSV-export.

1. Klik op *[!UICONTROL Share]* > *[!UICONTROL Send File Now]*, waarmee u een modaal venster opent.
2. Geef het bestandstype en de ontvangers op.
3. Klik op [!UICONTROL Send Now].

## Aangepaste rapporten

Wanneer u een aangepast rapport maakt in Google Analytics, lijken de vereiste velden op de workflow voor het maken van een visualisatie in de werkruimte. Dimensies, metriek en filterdefinities zijn vergelijkbaar tussen platforms. In de Werkruimte van de Analyse, in plaats van het selecteren van afmetingen en metriek van een lijst, worden de afmetingen en de metriek gesleept op een vrije vormlijst.

### Berekende metriek in douanerapporten

Aangepaste rapporten zijn een van de weinige gebieden in Google Analytics die het gebruik van berekende metriek toestaat. Omdat de Werkruimte van de Analyse als canvas werkt, werken de berekende metriek retroactief en in om het even welke context.

Een berekende metrische waarde maken:

1. Klik op het pictogram **+** bij de metrische lijst om de Berekende metrische bouwer te openen.
2. Geef de berekende metrische waarde een naam en geef een indeling op.
3. Sleep metrische componenten naar het definitiegebied en gebruik de dropdowns tussen elke component om een exploitant aan te wijzen.
4. Zodra berekende metrisch de gewenste formule bevat, klik sparen om terug naar uw werkruimte te gaan.
5. Sleep de nieuw gedefinieerde berekende metrische waarde naar de werkruimte.

   Meer informatie over [berekende meetgegevens](/help/components/c-variables/c-metrics/calculated-metric.md) vindt u in de gebruikershandleiding voor componenten.

## Aangepaste waarschuwingen

Alarm is beschikbaar op beide platforms. Gebruik in Adobe Analytics het navigatiemenu voor de koptekst en ga naar *[!UICONTROL Components]* > *[!UICONTROL Alerts]*. Zie [Intelligente waarschuwingen](/help/components/c-alerts/intellligent-alerts.md) in de Gebruikershandleiding van Componenten voor meer informatie.
