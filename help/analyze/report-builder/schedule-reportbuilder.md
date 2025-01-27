---
title: Hoe te om werkboeken te plannen gebruikend Report Builder in Adobe Analytics
description: Leer hoe u de planningsfunctie in Report Builder gebruikt
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 40e1feb0-64bc-40e6-83cb-4a1ea7e2d0cc
source-git-commit: cf1b64479690cf5bdfdc8d9ba08879d0e0886611
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 0%

---

# Workbooks plannen

Nadat u uw werkboek en voltooide uw analyse bewaarde, kunt u uw werkboek met anderen op uw team gemakkelijk delen gebruikend de het plannen eigenschap. De eigenschap van het Programma staat u toe om een programma tot stand te brengen dat automatisch de gegevens in het werkboek vernieuwt en het dossier van het werkboek van Excel .xlsx als gehechtheid aan uw gespecificeerd publiek op een specifieke datum en een tijd e-mailt. Als u een schema instelt, krijgen ontvangers automatisch regelmatig updates. U kunt de planningseigenschap ook gebruiken om het werkboek eens uit te sturen zonder automatische updates te plannen.

U kunt veelvoudige programma&#39;s voor één enkel werkboek tot stand brengen. Bijvoorbeeld, kunt u een werkboek naar uw team op een dagelijkse basis verzenden en u kunt het werkboek naar uw manager eens per week verzenden door twee verschillende programma&#39;s te creëren.

De eigenschap van het Programma staat u ook aan de bescherming van het opstellingswachtwoord voor een werkboek toe en geeft eerder geplande werkboeken uit.

>[!VIDEO](https://video.tv.adobe.com/v/3413079/?quality=12&learn=on)

## Een werkboek plannen

Gebruik de knoop van het Programma in de hub van de Report Builder om snel een programma tot stand te brengen zodat u een dossier van werkboekExcel (.xlsx) aan een individu of een groep kunt automatisch verdelen.

1. Klik de knoop van het Programma in de hub van de Report Builder.

   ![ klik de knoop van het Programma om een programma tot stand te brengen.](./assets/schedule-button.png){width="55%"}

1. Klik het Werkboek van het Programma of de plus knoop in upper-left om een nieuw gepland werkboek tot stand te brengen.

   ![ het venster van de werkboeken van het Programma.](./assets/schedule-workbook.png){width="55%"}

   De het plannen ruit toont sommige vooraf bepaalde informatie over het werkboek zoals de werkboeknaam en de laatste datum dat het werkboek werd gewijzigd.

   ![ het plannen ruit.](./assets/schedule-pane.png){width="55%"}

1. (Optioneel) Voer een bestandsnaam in.

   De naam van het werkboekdossier blijft aan de naam van het werkboek in gebreke maar u kunt dit veranderen als u wilt. Als u hetzelfde werkboek naar meerdere soorten publiek stuurt en u het een wat vriendelijker naam wilt geven voor een bepaald publiek, kunt u de naam wijzigen.

1. (Optioneel) Selecteer **Tijdstempel toevoegen aan bestandsnaam** .

   U kunt een timestamp aan het dossier toevoegen - noem om de datum te identificeren het werkboek werd bijgewerkt. Dit is nuttig om snel te zien welke versie van een werkboek op een specifieke datum werd verzonden. De **filename voorproef** toont hoe de naam van het werkboekdossier in e-mail zal verschijnen wanneer het werkboek wordt verdeeld. De tijdstempelnotatie is YYYY-MM-DD.

1. (Optioneel) Selecteer **.zip-compressie** om het bestand te comprimeren en wachtwoordbeveiliging voor het bestand in te stellen.

   Wanneer u deze selectie maakt, wordt u gevraagd een wachtwoord in te voeren om het bestand te openen. Dit is nuttig als u zich zorgen maakt over gegevensveiligheid en u wachtwoord het werkboek wilt beschermen. Als u het bestand met een wachtwoord wilt beveiligen, moet u **.zip compression** selecteren. Het wachtwoord moet ten minste 8 tekens hebben en een getal en een speciaal teken bevatten.

   ![ ga een wachtwoord op het Wachtwoord in beschermt het werkboekgebied.](./assets/zip-compression.png){width="55%"}

1. Ga **Ontvangers** in. U kunt de naam invoeren van een persoon die in uw organisatie wordt herkend, of u kunt een e-mailadres invoeren van een persoon binnen of buiten uw organisatie.

1. Ga het **Onderwerp** van e-mail en een beschrijving voor uw ontvangers in. Het onderwerp blijft aan de naam van het werkboekdossier in gebreke maar u kunt het onderwerp wijzigen indien nodig. U kunt details in de beschrijvingssectie toevoegen.

   ![ ga een onderwerp op het Onderwerp in.](./assets/recipients-subject.png){width="55%"}

1. Opstelling de het plannen opties om de datum en de tijd te plaatsen die u het werkboek aan uw ontvangers wilt e-mailden.

   Kies de begin- en einddatum- en tijdframes. Dit kan de datum van vandaag of een datum in de toekomst zijn.

   Kies de **Frequentie** van het drop-down menu. U kunt de frequentie instellen op uurbasis, dagelijks, wekelijks, maandelijks of jaarlijks op een bepaalde dag. Bijvoorbeeld, kunt u opstelling een programma om het werkboek op de eerste Zondagnacht van de maand te verzenden zodat uw ontvangers de e-mail in hun inbox eerste ding op maandagochtend zullen hebben.

   ![ selecteer de frequentie om uw rapport te plannen.](./assets/frequency.png){width="55%"}

1. Nadat u het programma plaatst, verzendt de klik **op programma**.

   ![ klik verzenden op programma.](./assets/send-on-schedule.png){width="55%"}

   U zult een bevestigingstoast bij de bodem van de hub van de Report Builder zien en het geplande werkboek is vermeld onder het lusje van Werkboeken.

   ![ Bevestiging toast ](./assets/confirmation-toast.png){width="55%"}

## Een omgezet werkboek plannen {#converted}

1. Plan a [ omgezet ](/help/analyze/report-builder/convert-workbooks.md) erfeniswerkboek.

   Een pop - op verschijnt, vragend of wilt u het plannen metada van het erfeniswerkboek gebruiken om een nieuwe geplande taak tot stand te brengen.

1. Als u **[!UICONTROL Use]** selecteert, vult de Report Builder automatisch de oude planningsinformatie in.

1. Zorg ervoor dat deze informatie correct en volgens plan is.

1. Als u het werkboek op een verschillend programma wilt verzenden, programma een volledig nieuwe geplande taak.


## Het werkboek slechts éénmaal verzenden

U kunt het werkboek ook slechts eenmaal verzenden.

1. Un-controle **tonen het plannen opties**

   ![ klik niet-controle tonen het plannen opties om een werkboek één keer uit te zenden.](./assets/send-now.png){width="40%"}

1. Klik **verzenden nu**.

## Geplande werkboeken weergeven en bewerken {#view-edit}

U kunt alle geplande werkboeken weergeven en beheren op één locatie onder het tabblad Werkboeken.

1. In de sectie van het Programma van de hub van de Report Builder, klik de Werkboeken tabel. Gebruik deze weergave om een lijst met alle geplande werkboeken weer te geven.

1. Selecteer een werkboek. Verscheidene hulpmiddelen worden getoond die u toestaan om het werkboek uit te geven, de planningstaak uit te geven, de planningstaak te pauzeren en opnieuw te beginnen, een gepland taakrapport te downloaden, of de planningstaak te schrappen.

   ![ Screenshot die de werkboekplanningspictogrammen tonen.](./assets/schedule-icons.png){width="20%"}

* (Facultatief) klik het potloodpictogram om de werkboekplanningstaak uit te geven.

* (Optioneel) Klik op het klokpictogram om een geschiedenis van elke geplande taak weer te geven.

* (Optioneel) Klik op het pauzepictogram om de taak van het distributieprogramma te onderbreken en opnieuw te starten. Dit is nuttig als u het werkboek moet wijzigen alvorens het werkboek wordt verzonden. Klik nogmaals op het pauzepictogram als u de distributie opnieuw wilt starten.

* (Facultatief) klik het downloadpictogram om een exemplaar van de werkboekprogrammataak te downloaden.

* (Optioneel) Klik op de prullenbak om de geplande taak te verwijderen.

  ![ Schermafbeelding die de lijst met planningstaken toont.](./assets/selected-workbook.png){width="40%"}

## De status van geplande taken controleren {#status}

In de geschiedenisweergave kunt u de status van elke geplande taak controleren. Er is een afzonderlijke rij die de statusverandering voor elke geplande taak documenteert. In het hieronder getoonde voorbeeld, werd het *Nieuwe Uur Programma* in werking gesteld op 5 Januari, bij 3:04pm. Om 15:05 uur is het bestand vernieuwd en verzonden naar ontvangers. Het volgende werkboek, *Onjuiste werkboek*, ontmoette een fout tijdens verfrist proces. Als een werkboek niet kon verzenden, helpt het geschiedenislusje u problemen oplossen door te tonen waar in het proces de fout voorkwam. In dit geval, is het waarschijnlijk toe te schrijven aan één of andere fout van het gegevensblok, misschien een ontbrekende component, die het werkboek van met succes het verfrissen hield.

Een groen vinkje wijst erop dat het werkboek met succes werd verzonden. Een uitroepteken in een rode driehoek geeft aan dat er een fout is opgetreden.

U kunt kiezen welke kolommen u wilt weergeven op het tabblad Historie door op het pictogram voor kolominstellingen rechts van de zoekbalk te klikken.

![ klik het kolompictogram om specifieke kolommen te tonen of te verbergen.](./assets/history.png){width="55%"}

U kunt onderaan de geschiedenis filtreren om slechts dat van één enkele geplande werkboeken te zien door naar het werkboeklusje te gaan, het werkboek te selecteren en het geschiedenispictogram te klikken.

U kunt de geschiedenis van een specifiek werkboek van het lusje van Werkboeken ook bekijken. Voor het lusje van Werkboeken, selecteer het werkboek en klik dan het geschiedenispictogram.

![ het pictogram van de de geschiedenisgeschiedenis van werkboeken ](./assets/history2.png){width="55%"}

Het werkboekfilter zal dan bij de bovenkant van de geschiedenis verschijnen. Klik op de x naast het filter om de geschiedenis van alle geplande taken opnieuw weer te geven.

![ de werkboekfilter.](./assets/history3.png){width="55%"}
