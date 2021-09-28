---
title: Media afspelen tijd besteed, deelvenster
description: Het deelvenster Media Playback Time Spent in Analysis Workspace gebruiken en interpreteren.
feature: Panels
role: User, Admin
exl-id: null
source-git-commit: 74ef44c4afba6d2dffb2b10fa473baee3be16a23
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 0%

---

# Media afspelen tijd besteed, deelvenster

Klanten van Media Analytics kunnen de afspeeltijd analyseren die ze hebben doorgebracht om te begrijpen waar de piekgelijktijdige uitvoering plaatsvond of waar drop-offs kostbare inzichten hebben opgeleverd in de kwaliteit van de betrokkenheid van content en viewers, en om hulp te bieden bij het oplossen van problemen of het plannen van volumes of schaal.

In Analysis Workspace is Afspeeltijd de tijd die nodig is om de mediastream(s) op een bepaald tijdstip weer te geven en omvat pauze, buffer en begintijd.

Met het deelvenster Tijd voor afspelen van media kunt u het afspelen in de loop van de tijd analyseren, waarbij u details kunt vinden over de piekconsistentie en de mogelijkheid om af te breken en te vergelijken. Navigeer naar een rapportsuite met Media Analytics-componenten ingeschakeld om het deelvenster Afspeeltijd van media te openen. Klik vervolgens op het deelvensterpictogram helemaal links en sleep het deelvenster naar uw Analysis Workspace-project.

Dit deelvenster bevat ook nieuwe functies in de kalender waarmee u minder dan 24 uur kunt selecteren en weergeven. U kunt dat voor het hele deelvenster doen, of u kunt segmenten maken met opeenvolgende tijdsperioden, zodat u de doorloop in/uitloop in de programma&#39;s of programmaonderdelen kunt bijhouden. Nadat u ten minste twee van deze datumsegmenten hebt geplaatst, ziet u een optie voor een keuzerondje voor Datumsequentie-weergave die de lijnen bedekt met een gemeenschappelijke beginpunt voor de x-as of deze op volgorde weergeeft met hun specifieke beginpunt voor de x-as.

## Deelvensterinvoer {#Input}

U kunt het deelvenster Tijd voor afspelen van media configureren met de volgende invoerinstellingen:

| Instelling | Beschrijving |
|---|---|
| Datumbereik van deelvenster | Het standaarddatumbereik van het deelvenster is Vandaag. U kunt de presentatie bewerken om een enkele dag of maanden tegelijk weer te geven.<br>Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Granulariteit | De standaardwaarde voor granulariteit is Minute.<br>Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken. |
| Samenvattingsnummers deelvenster | Er is een samenvattingsnummer beschikbaar om datum- of tijdgegevens voor de afspeeltijd te zien. Bij Maximaal worden details voor de piekfrequentie weergegeven. Bij Minimum worden details voor de dal weergegeven. De som verhoogt de totale playbacktijd die voor de selectie wordt doorgebracht. De paneelstandaard toont slechts Maximum, maar u kunt het veranderen om Minimum, Som, of om het even welke combinatie drie te tonen.<br>Als u onderverdelingen gebruikt, wordt een samenvattingsaantal getoond voor elk. |
| Uitsplitsing naar serie | U kunt desgewenst de visualisatie opsplitsen in segmenten, dimensies, dimensiepunten of datumbereiken.<p>- U kunt maximaal 10 regels tegelijk weergeven. Uitsplitsingen zijn beperkt tot één niveau.</p><p>- Wanneer u een dimensie sleept, worden de bovenste dimensie-items automatisch geselecteerd op basis van het geselecteerde datumbereik van het deelvenster.</p>- Als u datumbereiken wilt vergelijken, sleept u twee of meer datumbereiken naar het filter voor reeksindeling. |
| Tijdnotatie | U kunt de playbacktijd bekijken die in of Uren:Minutes:Seconden (gebrek) wordt doorgebracht of in Minuten (die in gehele aantallen, naar boven afgerond om .5 wordt getoond). |
| Weergave datumvolgorde | Als u ten minste twee segmenten van het datumbereik als reeksonderverdelingen hebt geplaatst, ziet u de optie om een overlay (standaard) of een sequentiële overlay te selecteren. Met overlay worden de lijnen weergegeven met een gemeenschappelijke beginpunt op de x-as, zodat deze parallel lopen, terwijl bij sequentieel de lijnen met hun specifieke beginpunt op de x-as worden weergegeven. Als de gegevenslijnen omhoog (bijvoorbeeld, eind segment 1 bij 8:44 pm en segment 2 begint bij 8:45 pm), dan zullen de lijnen in opeenvolging tonen. |

### Standaardweergave

![Standaardweergave](assets/mpts_default_view.png)

## Deelvensteruitvoer {#Output}

In het deelvenster Afspeeltijd van media worden een regeldiagram en samenvattingsnummers geretourneerd met gegevens over de maximale, minimale en/of totale afspeeltijd. Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren.

U kunt het deelvenster op elk gewenst moment bewerken en opnieuw samenstellen door op het bewerkingspotlood in de rechterbovenhoek te klikken.

Als u reeksindeling hebt geselecteerd, worden een regel in het lijndiagram en een samenvattingsnummer voor elke regel weergegeven:

![media playback tijd bestede output](assets/mpts_outputs1.png)

### Gegevensbron

De enige metrische waarde die in dit deelvenster kan worden gebruikt, is Afspeeltijd.

| Metrisch | Beschrijving |
|---|---|
| Afspeeltijd besteed | Totaal aantal uren:minutes:seconden (of minuten) van inhoud die tijdens de geselecteerde granulariteit worden weergegeven, inclusief pauze, buffer en begintijd. |

## Veelgestelde vragen {#FAQ}

| Vraag | Antwoord |
|---|---|
| Waar is de tabel voor vrije vorm? Hoe kan ik de gegevensbron zien? | <p></p><p>De tabel Freeform is niet beschikbaar in deze weergave. U kunt de gegevensbron downloaden door met de rechtermuisknop op het lijndiagram te klikken en het CSV-bestand te downloaden.</p> |
| <p>Waarom veranderde mijn granulariteit?</p> | <p>Deze visualisatie is beperkt tot 1440 rijen gegevens (bijvoorbeeld 24 uur bij granulariteit op minaniveau). Als een datumbereik en de combinatie van granulariteit meer dan 1440 rijen opleveren, wordt de granulariteit automatisch bijgewerkt om het volledige datumbereik te kunnen gebruiken.</p><p></p><p>Wanneer u van een groter datumbereik overschakelt op een kleiner datumbereik, wordt de granulariteit bijgewerkt naar het laagste detailniveau dat is toegestaan nadat het datumbereik is gewijzigd. Als u een hogere granulariteit wilt weergeven, bewerkt u het deelvenster en maakt u het opnieuw.</p> |
| <p></p><p>Hoe vergelijk ik videonamen, segmenten, inhoudstypen, enzovoort?</p> | <p>Om deze in één enkele visualisatie te vergelijken, sleep segmenten, dimensies, of specifieke afmetingspunten in de filter van de reeksafbraak.</p><p></p><p>De weergave is beperkt tot 10 uitsplitsingen. Als u meer dan 10 wilt weergeven, moet u meerdere deelvensters gebruiken.</p> |
| Hoe vergelijk ik datumbereiken? | Om datumwaaiers in één enkele visualisatie te vergelijken, gebruik de reeksonderverdelingen door 2 of meer datumwaaiers te slepen. Deze datumbereiken overschrijven het datumbereik van het deelvenster. |
| Hoe kan ik het visualisatietype wijzigen? | <p></p><p>In dit deelvenster kunt u alleen de lijnen voor de tijdreeks visualiseren.</p> |
| Kan ik anomaliedetectie uitvoeren? | <p></p><p>Nee. Anomaly-detectie is niet beschikbaar voor dit deelvenster.</p> |
