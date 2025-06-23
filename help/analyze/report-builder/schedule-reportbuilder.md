---
title: Workbooks plannen met Report Builder in Adobe Analytics
description: Meer informatie over het gebruik van de planningsfunctie in Report Builder
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 40e1feb0-64bc-40e6-83cb-4a1ea7e2d0cc
source-git-commit: 9ece9f6fcebdf308b6218aa50ab78af4f75ee8e7
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---

# Workbooks plannen door ze via e-mail te delen

>[!NOTE]
>
>Naast het plannen van werkboeken voor het delen door e-mail, zoals die in deze sectie wordt beschreven, kunt u werkboeken plannen om naar wolkenbestemmingen worden uitgevoerd, zoals die in [ worden beschreven werkboeken van het Programma voor de uitvoer naar wolkenbestemmingen ](/help/analyze/report-builder/report-builder-export.md).

Nadat u uw werkboek en voltooide uw analyse bewaarde, kunt u uw werkboek met anderen op uw team gemakkelijk delen gebruikend de het plannen eigenschap. De eigenschap van het Programma staat u toe om een programma tot stand te brengen dat automatisch de gegevens in het werkboek vernieuwt en het dossier van het werkboek van Excel .xlsx als gehechtheid aan uw gespecificeerd publiek op een specifieke datum en een tijd e-mailt. Als u een schema instelt, krijgen ontvangers automatisch regelmatig updates. U kunt de planningseigenschap ook gebruiken om het werkboek eens uit te sturen zonder automatische updates te plannen.

U kunt veelvoudige programma&#39;s voor één enkel werkboek tot stand brengen. Bijvoorbeeld, kunt u een werkboek naar uw team op een dagelijkse basis verzenden en u kunt het werkboek naar uw manager eens per week verzenden door twee verschillende programma&#39;s te creëren.

De eigenschap van het Programma staat u ook aan de bescherming van het opstellingswachtwoord voor een werkboek toe en geeft eerder geplande werkboeken uit.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ werkboeken van het Programma ](https://video.tv.adobe.com/v/3413079?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Een werkboek plannen

Gebruik de knoop van het Programma in de hub van Report Builder om snel een programma tot stand te brengen zodat u een dossier van werkboekExcel (.xlsx) aan een individu of een groep kunt automatisch verdelen.

1. Klik op de knop Planning in de Report Builder-hub.

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

   U ziet een bevestigingstoets bij de bodem van de hub van Report Builder en het geplande werkboek is vermeld onder het lusje van Werkboeken.

   ![ Bevestiging toast ](./assets/confirmation-toast.png){width="55%"}

## Een omgezet werkboek plannen {#converted}

1. Plan a [ omgezet ](/help/analyze/report-builder/convert-workbooks.md) erfeniswerkboek.

   Een pop - op verschijnt, vragend of wilt u het plannen metada van het erfeniswerkboek gebruiken om een nieuwe geplande taak tot stand te brengen.

1. Als u **[!UICONTROL Use]** selecteert, vult Report Builder automatisch de oudere planningsgegevens in.

1. Zorg ervoor dat deze informatie correct en volgens plan is.

1. Als u het werkboek op een verschillend programma wilt verzenden, programma een volledig nieuwe geplande taak.


## Het werkboek slechts éénmaal verzenden

U kunt het werkboek ook slechts eenmaal verzenden.

1. Un-controle **tonen het plannen opties**

   ![ klik niet-controle tonen het plannen opties om een werkboek één keer uit te zenden.](./assets/send-now.png){width="40%"}

1. Klik **verzenden nu**.

## Geplande werkboeken beheren

Voor informatie over het beheren van werkboeken die reeds gepland zijn, zie [ geplande werkboeken beheren ](/help/analyze/report-builder/manage-schedules-reportbuilder.md).
