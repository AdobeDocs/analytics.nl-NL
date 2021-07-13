---
description: Een deelvenster is een verzameling tabellen en visualisaties
title: Overzicht van deelvensters
feature: Deelvensters
role: User, Admin
exl-id: dd1a3c40-8b5b-47dd-86d9-da766575ee46
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 1%

---

# Overzicht van deelvensters

A [!UICONTROL panel] is een inzameling van lijsten en visualisaties. U hebt toegang tot deelvensters via het pictogram linksboven in Workspace of via een [leeg deelvenster](blank-panel.md). Deelvensters zijn handig wanneer u uw projecten wilt ordenen op basis van een tijdsperiode, een rapport of een analyse. De volgende deelvenstertypen zijn beschikbaar in Analysis Workspace:

| Vensternaam | Beschrijving |
| --- | --- |
| [Leeg deelvenster](blank-panel.md) | Kies uit de beschikbare deelvensters en visualisaties om uw analyse te starten. |
| [Deelvenster Snelle inzichten](quickinsight.md) | Snel een vrije-vormlijst en een bijbehorende visualisatie bouwen om inzichten sneller te analyseren en te ontdekken. |
| [Analyses voor venster Doel](a4t-panel.md) | Doelactiviteiten en ervaringen in Analysis Workspace analyseren. |
| [Deelvenster voor attributie](attribution.md) | Vergelijk en visualiseer snel om het even welk aantal attributiemodellen gebruikend om het even welke afmeting en omzettingsmetrisch. |
| [Deelvenster Vrije vorm](freeform-panel.md) | Voer onbeperkte vergelijkingen en onderverdelingen uit, dan voeg visualisaties toe om een rijk gegevensverhaal te vertellen. |
| [Deelvenster voor gelijktijdige mediaviewers](media-concurrent-viewers.md) | Analyseer gelijktijdige viewers in de loop van de tijd met details over de piekconsistentie en de mogelijkheid om af te breken en te vergelijken. |
| [Deelvenster Segmentvergelijking](c-segment-comparison/segment-comparison.md) | Vergelijk snel twee segmenten in alle gegevenspunten om automatisch relevante verschillen te vinden. |

![](assets/panel-overview.png)

[!UICONTROL Quick Insights],  [!UICONTROL Blank] en  [!UICONTROL Freeform] deelvensters zijn ideale plaatsen om uw analyse te starten, terwijl  [!UICONTROL Analytics for Target],  [!UICONTROL Attribution IQ],  [!UICONTROL Media Concurrent Viewers] en zich aan geavanceerdere analyses  [!UICONTROL Segment Comparison] lenen. Een `"+"` knoop is beschikbaar in projecten zodat kunt u lege panelen op elk ogenblik toevoegen.

Het standaardstartvenster is het [!UICONTROL Freeform]-deelvenster, maar u kunt ook het [lege deelvenster](/help/analyze/analysis-workspace/c-panels/blank-panel.md) als standaard instellen.

## Rapportsuite {#report-suite}

Tabellen en visualisaties in een deelvenster leiden gegevens af van de [!UICONTROL report suite] die rechtsboven in het deelvenster is geselecteerd. Het rapportpakket bepaalt ook welke componenten in de linkerspoorstaaf beschikbaar zijn. Binnen een project, kunt u één of [vele rapportreeksen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html) afhankelijk van uw gevallen van het analysegebruik gebruiken. Als u één rapportsuite op alle deelvensters in een project wilt toepassen, **klikt u met de rechtermuisknop op de koptekst van het deelvenster > Rapportsuite toepassen op alle deelvensters**.

De lijst van rapportreeksen wordt gesorteerd op relevantie, die Adobe bepaalt gebaseerd op hoe onlangs en vaak de reeks door de huidige gebruiker is gebruikt, en hoe vaak de reeks binnen de organisatie wordt gebruikt.

![](assets/panel-report-suite.png)

## Kalender {#calendar}

De paneelkalender bepaalt het rapporteringswaaier voor lijsten en visualisaties binnen een paneel.

Opmerking: Als een (paarse) datumbereikcomponent wordt gebruikt binnen een tabel, visualisatie of dropzone van een deelvenster, wordt de paneelkalender hierdoor overschreven.

![](assets/panel-calendar.png)

## Dropzone {#dropzone}

Met de dropzone van het deelvenster kunt u segment- en vervolgkeuzefilters toepassen op alle tabellen en visualisaties in een deelvenster. U kunt een of meerdere filters toepassen op een deelvenster. U kunt de titel boven elk filter wijzigen door op het bewerkingspenlood te klikken. U kunt ook met de rechtermuisknop klikken om het filter helemaal te verwijderen.

### Segmentfilters

Sleep een segment van de linkerspoorstaaf naar de neerzetzone van het deelvenster om het deelvenster te filteren.

![](assets/segment-filter.png)

### Ad-hocsegmentfilters

Niet-segmentcomponenten kunnen ook rechtstreeks naar de dropzone worden gesleept om ad-hocsegmenten te maken, waardoor u tijd en moeite bespaart om naar de Segment Builder te gaan. Segmenten die op deze manier worden gemaakt, worden automatisch gedefinieerd als raaksegmenten. Deze definitie kan worden gewijzigd door op het informatiepictogram (i) naast het segment te klikken, vervolgens op het pictogram voor het bewerken van de vorm van een potlood te klikken en dit te bewerken in de Segment Builder.

Ad-hocsegmenten zijn lokaal voor het project en verschijnen niet in uw linkerspoor tenzij u ze openbaar maakt.

![](assets/adhoc-segment-filter.png)

### Vervolgkeuzefilters {#dropdown-filter}

Naast segmentfilters kunt u met vervolgkeuzefilters op een gecontroleerde manier met de gegevens werken. U kunt bijvoorbeeld een vervolgkeuzefilter toevoegen voor mobiele apparaattypen, zodat u het deelvenster kunt segmenteren op tablet, mobiele telefoon of bureaublad.

U kunt vervolgkeuzefilters gebruiken om een groot aantal projecten ook in één project te consolideren. Bijvoorbeeld, als u vele versies van het zelfde project met verschillende toegepaste segmenten van het Land hebt, kunt u alle versies in één enkel project consolideren en een drop-down filter van het Land toevoegen.

![](assets/dropdown-filter-intro.png)

Vervolgkeuzefilters maken:

1. Als u een vervolgkeuzefilter wilt maken met [!UICONTROL Dimension items], zoals waarden binnen de [!UICONTROL Marketing Channel]-dimensie, klikt u op het pictogram met de pijl naar rechts naast de afmeting in de linkertrack. Hiermee worden alle beschikbare items zichtbaar. Selecteer een of meer componentitems in de linkertrack en zet ze **neer in de dropzone van het deelvenster terwijl u Shift ingedrukt houdt.** Hierdoor worden de componenten omgezet in een vervolgkeuzefilter in plaats van in één segment.
1. Als u een vervolgkeuzefilter wilt maken met een andere component, zoals metriek, segmenten of datumbereiken, selecteert u een van de componenttypen in de linkerrails en zet u de vervolgkeuzelijst neer in de dropzone van het deelvenster terwijl u Shift ingedrukt houdt **.**
1. Selecteer een van de opties in het vervolgkeuzemenu om de gegevens in het deelvenster te wijzigen. U kunt er ook voor kiezen om geen van de deelvenstergegevens te filteren door **[!UICONTROL No filter]** te selecteren.

![](assets/create-dropdown.png)

[Bekijk de ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-panels-to-organize-your-analysis-workspace-projects.html) video voor meer informatie over het toevoegen van vervolgkeuzefilters aan uw project.

## Klikken met rechtermuisknop {#right-click}

Aanvullende functionaliteit voor een deelvenster is beschikbaar door met de rechtermuisknop op de koptekst van het deelvenster te klikken.

![](assets/right-click-menu.png)

De volgende instellingen zijn beschikbaar:

| Instelling | Beschrijving |
| --- | --- |
| Gekopieerd deelvenster/visualisatie invoegen | Hiermee kunt u een gekopieerd deelvenster of een visualisatie plakken (&quot;invoegen&quot;) naar een andere locatie in het project of naar een geheel ander project. |
| Deelvenster kopiëren | Hiermee kunt u met de rechtermuisknop klikken en een deelvenster kopiëren, zodat u het kunt invoegen op een andere locatie in het project of in een geheel ander project. |
| Rapportsuite toepassen op alle deelvensters | Hiermee kunt u de rapportsuite van het actieve deelvenster toepassen op alle deelvensters in het project. |
| Deelvenster dupliceren | Hiermee maakt u een exacte kopie van het huidige deelvenster, dat u vervolgens kunt wijzigen. |
| Alle deelvensters samenvouwen/uitvouwen | Hiermee vouwt u alle projectdeelvensters samen en breidt u deze uit. |
| Alle visualisaties in deelvenster samenvouwen/uitvouwen | Hiermee vouwt u alle visualisaties in het huidige deelvenster samen en breidt u deze uit. |
| Beschrijving bewerken | Voeg (of bewerk) een tekstbeschrijving voor het paneel toe. |
| Deelvensterkoppeling ophalen | Hiermee kunt u iemand doorsturen naar een specifiek deelvenster binnen een project. Wanneer op de koppeling wordt geklikt, moet de ontvanger zich aanmelden voordat deze wordt omgeleid naar het exacte deelvenster dat is gekoppeld aan. |
