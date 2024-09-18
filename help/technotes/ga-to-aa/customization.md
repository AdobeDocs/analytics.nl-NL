---
title: Aanpassing rapporteren in Adobe Analytics
description: Leer hoe u rapporten kunt aanpassen in Adobe Analytics
feature: Third-party Integration
exl-id: 8ea6ec3a-cfc6-4c14-966b-d245949451c7
source-git-commit: 815e50e30fa6a0bce1bf78f33843070f96f52de8
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 0%

---

# Rapporten aanpassen

Op platforms van derden, zoals Googles Analytics, zijn verschillende aanpassingsopties beschikbaar. Met deze aanpassingen kan een gebruiker dashboards, aangepaste rapporten, opgeslagen rapporten en aangepaste waarschuwingen maken. Omdat Analysis Workspace gebruikers in staat stelt rapporten op te stellen op basis van een leeg canvas, worden de meeste aanpassingen rechtstreeks in het gereedschap ingebouwd.

Deze pagina gaat ervan uit dat de gebruiker bekend is met het gebruik van [!UICONTROL Analysis Workspace] . Zie [ een basisrapport in Analysis Workspace voor Googles Analytics gebruikers ](reports/create-report.md) tot stand brengen als u nog niet vertrouwd met het hulpmiddel in Adobe Analytics bent.

## Dashboards

De [!UICONTROL Analysis Workspace] -architectuur is gebaseerd op het concept van dashboardwidgets. Projecten in [!UICONTROL Analysis Workspace] komen ongeveer overeen met dashboards in Googles Analytics. Visualisaties in [!UICONTROL Analysis Workspace] zijn ongeveer gelijk aan widgets in Googles Analytics.

### Inhoud toevoegen aan een project

1. Klik op het pictogram [!UICONTROL Visualizations] aan de linkerkant en sleep de gewenste visualisatie naar de werkruimte.
2. Klik op het pictogram [!UICONTROL Components] aan de linkerkant en sleep de gewenste afmetingen en afmetingen naar de visualisatie om deze te vullen met gegevens.
3. Sleep de randen van de visualisatie om het formaat te wijzigen en sleep de titel van de visualisatie om het te verplaatsen.

Alle Googles Analytics-widgets zijn beschikbaar in [!UICONTROL Analysis Workspace] :

* De **Metrische widget** is ongeveer gelijk aan [!UICONTROL Summary Number] visualisatie.
* De **widget van de Chronologie** is ongeveer gelijk aan [!UICONTROL Line] visualisatie.
* De **widget Geomap** is ongeveer gelijk aan [!UICONTROL Map] visualisatie.
* De **widget van de Lijst** is ongeveer gelijk aan [!UICONTROL Freeform Table] visualisatie.
* De **Schijfwidget** is ongeveer gelijk aan [!UICONTROL Donut] visualisatie.
* De **Bar widget** is ongeveer gelijk aan [!UICONTROL Bar] visualisatie.

[!UICONTROL Analysis Workspace] bevat veel meer visualisatieopties om gegevens weer te geven op een manier die het beste aansluit bij uw rapportagebehoeften. Zie [ Visualisaties in Analysis Workspace ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) in de Analyze Gids van de Gebruiker voor meer informatie.

### Projecten delen

Als u klaar bent met het toevoegen van inhoud aan een project, kunt u deze delen.

* Ga naar **[!UICONTROL Share > Share Project]** als u het project wilt delen met uw collega&#39;s. Ontvangers zijn andere gebruikers in uw organisatie die een Adobe Analytics-account hebben.
* Ga naar **[!UICONTROL Share > Get Project Link]** als u uw project wilt delen via een koppeling. Hiervoor moet u zich binnen uw organisatie nog aanmelden bij Adobe Analytics.

### Projecten exporteren

Naast PDF biedt [!UICONTROL Analysis Workspace] een CSV-export.

1. Klik op *[!UICONTROL Share]* > *[!UICONTROL Send File Now]* om een modaal venster te openen.
2. Geef het bestandstype en de ontvangers op.
3. Klik op [!UICONTROL Send Now].

## Aangepaste rapporten

Wanneer u een aangepast rapport maakt in Googles Analytics, lijken de vereiste velden op de workflow voor het maken van een visualisatie in de werkruimte. De Dimensionen, de Metriek, en de definities van de Filter zijn gelijkaardig tussen platforms. In Analysis Workspace worden afmetingen en metriek niet uit een lijst geselecteerd, maar naar een vrije-vormtabel gesleept.

### Berekende cijfers in aangepaste rapporten

De rapporten van de douane zijn één van de weinige gebieden in Googles Analytics die het gebruik van berekende metriek toestaat. Omdat Analysis Workspace als een canvas werkt, werken berekende metriek retroactief en in elke context.

Een berekende metrische waarde maken:

1. Klik op het pictogram **+** bij de metrische lijst om de lijst [!UICONTROL Calculated Metric Builder] te openen.
2. Geef de berekende metrische waarde een naam en geef een indeling op.
3. Sleep metrische componenten naar het definitiegebied en gebruik de vervolgkeuzelijsten tussen elke component om een operator aan te wijzen.
4. Zodra berekende metrisch de gewenste formule bevat, klik sparen om terug naar uw werkruimte te gaan.
5. Sleep de nieuw gedefinieerde berekende metrische waarde naar de werkruimte.

   Leer meer over [ Berekende Metriek ](/help/components/c-calcmetrics/cm-overview.md) in de de gebruikersgids van Componenten.

## Aangepaste waarschuwingen

Alarm is beschikbaar op beide platforms. Gebruik in Adobe Analytics het navigatiemenu voor de koptekst en ga naar *[!UICONTROL Components]* > *[!UICONTROL Alerts]* . Zie [ overzicht van Alarm ](/help/components/c-alerts/intellligent-alerts.md) in de Gids van de Gebruiker van Componenten voor meer informatie.
