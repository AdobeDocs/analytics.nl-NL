---
title: Media afspelen tijd besteed, deelvenster
description: Het deelvenster Media Playback Time Spent in Analysis Workspace gebruiken en interpreteren.
feature: Panels
role: User, Admin
exl-id: 9268baf7-b50b-4c09-a722-7bfcd4172f15
source-git-commit: 4633225cc35658a7de39a40cd77df00137a54461
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Media afspelen tijd besteed, deelvenster

In Analysis Workspace is Afspeeltijd de hoeveelheid tijd die is besteed aan het bekijken van uw mediastreams op een bepaald tijdstip. Het omvat pauze, buffer, en tijd om te beginnen.

Met het deelvenster Tijd voor afspelen van media kunt u het afspelen in de loop van de tijd analyseren, waarbij u details kunt vinden over de piekfrequentie en de mogelijkheid om af te breken en te vergelijken.

Klanten die de invoegtoepassing voor de verzameling van streaming media hebben aangeschaft, kunnen de afspeeltijd analyseren om waardevolle inzichten in de kwaliteit van de inhoud en de betrokkenheid van de viewer te krijgen en om hulp te bieden bij het oplossen van problemen of het plannen van volumes of schaal.

Met de tijd die u hebt besteed voor afspelen kunt u het volgende begrijpen:

* Waar de piekconcentratie optrad

* Locatie van vervolgkeuzelijst

Hieronder volgt een video-overzicht van dit deelvenster:

>[!VIDEO](https://video.tv.adobe.com/v/338699)

## Het deelvenster Afspeeltijd van media gebruiken

1. Ga naar een rapportsuite met ingeschakelde streamingmedia-componenten.
1. Selecteer het deelvensterpictogram helemaal links en sleep het deelvenster naar uw Analysis Workspace-project.
1. Ga verder met de volgende secties om het deelvenster Afspeeltijd van media aan te passen

   * [Deelvensterinvoer](#panel-inputs)
   * [Deelvensteruitvoer](#panel-output)

## Deelvensterinvoer {#Input}

U kunt het deelvenster Tijd voor afspelen van media configureren met de volgende invoerinstellingen:

| Instelling | Beschrijving |
|---|---|
| Datumbereik van deelvenster | Het standaarddatumbereik van het deelvenster is Vandaag. U kunt de presentatie bewerken om een enkele dag of maanden tegelijk weer te geven.<br>Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Granulariteit | De standaardwaarde voor granulariteit is Minute.<br>Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Samenvattingsnummers deelvenster | Er is een samenvattingsnummer beschikbaar om datum- of tijdgegevens voor de afspeeltijd te zien. Bij Maximaal worden details voor de piekfrequentie weergegeven. Bij Minimum worden details voor de dal weergegeven. De som verhoogt de totale playbacktijd die voor de selectie wordt doorgebracht. De paneelstandaard toont slechts Maximum, maar u kunt het veranderen om Minimum, Som, of om het even welke combinatie drie te tonen.<br>Als u onderverdelingen gebruikt, wordt een samenvattingsaantal getoond voor elk. |
| Uitsplitsing naar serie | U kunt desgewenst de visualisatie opsplitsen in segmenten, dimensies, dimensiepunten of datumbereiken.<p>- U kunt maximaal 10 regels tegelijk weergeven. Uitsplitsingen zijn beperkt tot één niveau.</p><p>- Wanneer u een dimensie sleept, worden de bovenste dimensie-items automatisch geselecteerd op basis van het geselecteerde datumbereik van het deelvenster.</p>- Als u datumbereiken wilt vergelijken, sleept u twee of meer datumbereiken naar het filter voor reeksindeling. |
| Tijdnotatie | U kunt de afspeeltijd in een van beide bekijken `Hours:Minutes:Seconds` (standaardwaarde) of in `Minutes` (wordt in gehele getallen weergegeven, naar boven afgerond op 0,5). |
| Weergave datumvolgorde | Als u minstens twee segmenten van het datumbereik als reeksonderverdelingen hebt geplaatst, zult u de optie zien om of bedekking (gebrek) of opeenvolgend te selecteren. Met overlay worden de lijnen weergegeven met een gemeenschappelijke beginpunt op de x-as, zodat deze parallel lopen, terwijl bij sequentieel de lijnen met hun specifieke beginpunt op de x-as worden weergegeven. Als de gegevenslijnen omhoog (bijvoorbeeld, eind segment 1 bij 8:44 pm en segment 2 begint bij 8:45 pm), dan zullen de lijnen in opeenvolging tonen. |

## Standaardweergave

![Standaardweergave](assets/mpts_default_view.png)

## Deelvensteruitvoer {#Output}

In het deelvenster Afspeeltijd van media worden een regeldiagram en samenvattingsnummers geretourneerd met gegevens over de maximale, minimale en/of totale afspeeltijd. Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren.

U kunt het deelvenster op elk gewenst moment bewerken en opnieuw samenstellen door op het bewerkingspotlood in de rechterbovenhoek te klikken.

Als u reeksindeling hebt geselecteerd, worden een regel in het lijndiagram en een samenvattingsnummer voor elke regel weergegeven:

![media playback tijd bestede output](assets/mpts_outputs1.png)

### Data Source

De enige metrische waarde die in dit deelvenster kan worden gebruikt, is Afspeeltijd.

| Metrisch | Beschrijving |
|---|---|
| Afspeeltijd besteed | Totaal `hours:minutes:seconds` (of `minutes`) van inhoud die wordt weergegeven tijdens de geselecteerde granulariteit, zoals pauzeren, buffer en begintijd. |

## Veelgestelde vragen

| Vraag | Antwoord |
|---|---|
| Waar is de tabel voor vrije vorm? Hoe kan ik de gegevensbron zien? | De tabel Freeform is niet beschikbaar in deze weergave. U kunt de gegevensbron downloaden door met de rechtermuisknop op het lijndiagram te klikken en het CSV-bestand te downloaden. |
| Waarom veranderde mijn granulariteit? | Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. <p>Wanneer u van een groter datumbereik overschakelt op een kleiner datumbereik, wordt de granulariteit bijgewerkt naar het laagste detailniveau dat is toegestaan nadat het datumbereik is gewijzigd. Als u een hogere granulariteit wilt weergeven, bewerkt u het deelvenster en maakt u het opnieuw.</p> |
| Hoe vergelijk ik videonamen, segmenten, inhoudstypen, enzovoort? | Om deze in één enkele visualisatie te vergelijken, sleep segmenten, dimensies, of specifieke afmetingspunten in de filter van de reeksafsplitsing.De mening is beperkt tot 10 onderbrekingen. Als u meer dan 10 wilt weergeven, moet u meerdere deelvensters gebruiken. |
| Hoe vergelijk ik datumbereiken? | Om datumwaaiers in één enkele visualisatie te vergelijken, gebruik de reeksonderverdelingen door 2 of meer datumwaaiers te slepen. Deze datumbereiken overschrijven het datumbereik van het deelvenster. |
| Hoe kan ik het visualisatietype wijzigen? | In dit deelvenster kunt u alleen de lijnen voor de tijdreeks visualiseren. |
| Kan ik anomaliedetectie uitvoeren? | Nee. Anomaly-detectie is niet beschikbaar voor dit deelvenster. |
