---
title: Workbooks plannen met Report Builder
description: Leer hoe u de planningsfunctie in Report Builder kunt gebruiken.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 40e1feb0-64bc-40e6-83cb-4a1ea7e2d0cc
source-git-commit: 8b6d8a4efec59b693a69984880d8f374ae0cfabc
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Workbooks plannen door ze via e-mail te delen

>[!NOTE]
>
>Naast het plannen van werkboeken voor het delen door e-mail, zoals die in deze sectie wordt beschreven, kunt u werkboeken plannen om naar wolkenbestemmingen worden uitgevoerd, zoals die in [&#x200B; worden beschreven werkboeken van het Programma voor de uitvoer naar wolkenbestemmingen &#x200B;](/help/analyze/report-builder/report-builder-export.md).

Nadat u uw werkboek en voltooide uw analyse bewaarde, kunt u uw werkboek met anderen op uw team gemakkelijk delen gebruikend de het plannen eigenschap. De eigenschap van het Programma staat u toe om een programma tot stand te brengen dat automatisch de gegevens in het werkboek vernieuwt en het dossier van het werkboek van Excel .xlsx als gehechtheid aan uw gespecificeerd publiek op een specifieke datum en een tijd e-mailt. Als u een schema instelt, krijgen ontvangers automatisch regelmatig updates. U kunt de planningseigenschap ook gebruiken om het werkboek eens uit te sturen zonder automatische updates te plannen.

U kunt veelvoudige programma&#39;s voor één enkel werkboek tot stand brengen. Bijvoorbeeld, kunt u een werkboek naar uw team op een dagelijkse basis verzenden en u kunt het werkboek naar uw manager eens per week verzenden door twee verschillende programma&#39;s te creëren.

De eigenschap van het Programma staat u ook aan de bescherming van het opstellingswachtwoord voor een werkboek toe en geeft eerder geplande werkboeken uit.


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; werkboeken van het Programma &#x200B;](https://video.tv.adobe.com/v/3413079?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Een werkboek plannen

Een werkboek plannen:

1. Selecteer **[!UICONTROL Schedule]** in de hub van Report Builder om een programma tot stand te brengen zodat u een dossier van werkboekExcel (.xlsx) aan een individu of een groep kunt automatisch verdelen.

   ![&#x200B; selecteer de knoop van het Programma om een programma tot stand te brengen.](./assets/schedule.png){zoomable="yes"}

1. Selecteer **[!UICONTROL Schedule Workbook]** of ![&#x200B; voeg &#x200B;](/help/assets/icons/Add.svg) toe om een nieuw gepland werkboek tot stand te brengen.

   ![&#x200B; het venster van de werkboeken van het Programma.](./assets/schedule-workbook.png){zoomable="yes"}

   De het plannen ruit toont sommige vooraf bepaalde informatie over het werkboek zoals de werkboeknaam en de laatste datum dat het werkboek werd gewijzigd.

### Bestand

In de sectie **[!UICONTROL File]** geeft u details over het bestandstype, de naam en een wachtwoord op om het bestand te beveiligen.

![&#x200B; het plannen ruit.](./assets/schedule-pane.png){zoomable="yes"}

1. Gebruik ![&#x200B; TableSelect &#x200B;](/help/assets/icons/TableSelect.svg) om het huidige werkboek te selecteren, als niet reeds geselecteerd.

1. (Optioneel) Voer een **[!UICONTROL File name]** in.

   De naam van het werkboekdossier blijft aan de naam van het werkboek in gebreke maar u kunt de dossiernaam veranderen als u wilt.

1. Selecteer een **[!UICONTROL File type]** .

   * **[!UICONTROL Excel]**
   * **[!UICONTROL PDF]**
   * **[!UICONTROL CSV]**

   Wanneer u **[!UICONTROL CSV]** selecteert, houd er rekening mee dat het geplande werkboek als postgehechtheid wordt verzonden. Sommige e-mailbeheerders van bedrijven kunnen e-mailberichten blokkeren met ZIP-bijlagen. U ziet een waarschuwing op basis hiervan.

1. (Optioneel) Selecteer **[!UICONTROL Append time-stamp to file name]** .

   U kunt een timestamp aan het dossier toevoegen - noem om de datum te identificeren het werkboek werd bijgewerkt. Een timestamp is nuttig om te zien welke versie van een werkboek op een specifieke datum werd verzonden. Als deze optie is geselecteerd, kunt u kiezen tussen:

   * **[!UICONTROL ISO Date format]** . Dit betekent dat `YYYY-MM-DD` aan de bestandsnaam wordt toegevoegd.
   * **[!UICONTROL ISO Date format + time stamp]** . Dit betekent dat `YYYY-MM-DD_HH-MM-SS` aan de bestandsnaam wordt toegevoegd.

<!-- Does no longer seem to be an option? 
1. (Optional) Select **.zip compression** to compress the file and set up password protection on the file.

    When you make this selection, you're prompted to enter a password to open the file. This is helpful if you have concerns about data security and you want to password protect the workbook. Protecting the file with a password requires you to select **.zip compression**. The password must be at least 8 characters and contain a number and a special character.

    ![Enter a password in the Password protect the workbook field.](./assets/zip-compression.png){zoomable="yes"}{width="55%"}
-->

1. Voer een wachtwoord in **[!UICONTROL Password protect the workbook]** in. Voor een geldig wachtwoord zijn ten minste 8 tekens nodig, een getal en een speciaal teken. Selecteer ![&#x200B; VisibilityOff &#x200B;](/help/assets/icons/VisibilityOff.svg) om het wachtwoord en ![&#x200B; Zichtbaarheid &#x200B;](/help/assets/icons/Visibility.svg) te tonen om het wachtwoord (gebrek) te verbergen.


### E-mail

In de sectie **[!UICONTROL Email]** geeft u de ontvangers, het onderwerp en de beschrijving van de e-mail op.

![&#x200B; e-mailmontages van het Programma &#x200B;](assets/schedule-email.png){zoomable="yes"}

1. Ga **Ontvangers** in. U kunt de naam invoeren van een persoon die in uw organisatie wordt herkend. U kunt ook een e-mailadres invoeren van een persoon die zich buiten uw organisatie bevindt.

1. Ga het **Onderwerp** van e-mail en een beschrijving voor uw ontvangers in. Het onderwerp blijft aan de naam van het werkboekdossier in gebreke maar u kunt het onderwerp wijzigen indien nodig. U kunt details in de beschrijvingssectie toevoegen.

1. U kunt desgewenst een beschrijving invoeren in het tekstgebied **[!UICONTROL Description]** .


### Schema

In de **[!UICONTROL Schedule]** sectie, kunt u het programma bepalen om de e-mails met het werkboek naar uw ontvangers te verzenden.

![&#x200B; definitie van het Programma &#x200B;](assets/schedule-enable.png){zoomable="yes"}

1. Selecteer **[!UICONTROL Show scheduling options]** om een schema te definiëren.

1. Voer een begindatum in in **[!UICONTROL Starting on]** . Alternatief, selecteer ![&#x200B; Kalender &#x200B;](/help/assets/icons/Calendar.svg) om een begindatum van de kalender te kiezen.

1. Voer een einddatum in in **[!UICONTROL Ending on]** . Alternatief, selecteer ![&#x200B; Kalender &#x200B;](/help/assets/icons/Calendar.svg) om een einddatum van de kalender te kiezen.

1. Selecteer een **[!UICONTROL Frequency]** . Afhankelijk van de geselecteerde frequentie, hebt u extra opties. Zie onderstaande tabel.

   | Frequentie | Opties |
   |---|---|
   | **[!UICONTROL Send hourly]** | Voer een waarde in voor **[!UICONTROL Send every number of hours]** . |
   | **[!UICONTROL Send daily]** | Selecteer een **[!UICONTROL Daily frequency]**: **[!UICONTROL Send every day]**, **[!UICONTROL Send every weekday]** of **[!UICONTROL Custom frequency]** .<br/> Als u **[!UICONTROL Custom frequency]** selecteert, ga een waarde voor **[!UICONTROL Send every number of days]** in. |
   | **[!UICONTROL Send weekly]** | Voer een waarde in voor **[!UICONTROL Send every number of weeks]** . Selecteer een **[!UICONTROL Day of week]** . |
   | **[!UICONTROL Send monthly by day of the week]** | Selecteer een **[!UICONTROL Day of week]** en een **[!UICONTROL Week of month]** . |
   | **[!UICONTROL Send monthly by day of the month]** | Selecteer een waarde in **[!UICONTROL Send on this day of the month]** . |
   | **[!UICONTROL Send yearly by day of the month]** | Selecteer een **[!UICONTROL Day of week]** , selecteer een **[!UICONTROL Week of month]** en selecteer een **[!UICONTROL Monthly of year]** . |
   | **[!UICONTROL Send yearly by specific date]** | Selecteer een **[!UICONTROL Month of year]** en selecteer een waarde in **[!UICONTROL Send on this day of the month]** . |

### Verzenden

Om het werkboek te verzenden:

* Als u geen schema gebruikend **[!UICONTROL Show scheduling options]** hebt bepaald, uitgezocht **[!UICONTROL Send now]** om het werkboek per e-mail onmiddellijk te verzenden.
* Als u een programma gebruikend **[!UICONTROL Show scheduling options]** hebt bepaald, uitgezocht **[!UICONTROL Send on schedule]** om het werkboek door e-mail te verzenden gebruikend het programma u bepaalde.

In beide gevallen ziet u een bevestigingstoets onder aan de Report Builder-hub.

Als u het verzenden van het werkboek wilt annuleren, selecteert u **[!UICONTROL Cancel]** .

## Geplande werkboeken beheren

Voor informatie over het beheren van werkboeken die reeds gepland zijn, zie [&#x200B; geplande werkboeken beheren &#x200B;](/help/analyze/report-builder/manage-reportbuilder.md).




<!--

## Schedule a workbook

Use the Schedule button in the Report Builder hub to quickly create a schedule so that you can automatically distribute a workbook Excel file (.xlsx) to an individual or a group.

1. Click the Schedule button in the Report Builder hub.

    ![Click the Schedule button to create a schedule.](./assets/schedule-button.png){width="55%"}

1. Click Schedule Workbook or the plus button in the upper-left to create a new scheduled workbook.

    ![The Schedule workbooks window.](./assets/schedule-workbook.png){width="55%"}

    The scheduling pane displays some pre-defined information about the workbook such as the workbook name and the last date that the workbook was modified.

    ![The scheduling pane.](./assets/schedule-pane.png){width="55%"}

1. (Optional) Enter a file name.

    The workbook file name defaults to the name of the workbook but you can change this if you want. If you\'re sending the same workbook to multiple audiences and you want to name it something a little bit more friendly for a certain audience, you can change the name.

1. (Optional) Select **Append time-stamp to file name**.

    You can append a timestamp to the file name to identify the date the workbook was updated. This is helpful to quickly see which version of a workbook was sent on a specific date. The **Filename preview** shows how the workbook file name will appear in the email when the workbook is distributed. The time-stamp format is YYYY-MM-DD.

1. (Optional) Select **.zip compression** to compress the file and set up password protection on the file.

    When you make this selection, you're prompted to enter a password to open the file. This is helpful if you have concerns about data security and you want to password protect the workbook. Protecting the file with a password requires you to select **.zip compression**. The password must be at least 8 characters and contain a number and a special character.

    ![Enter a password in the Password protect the workbook field.](./assets/zip-compression.png){width="55%"}

1. Enter **Recipients**. You can enter the name of a person that is recognized in your organization, or you can enter an email address of a person inside or outside of your organization.

1. Enter the **Subject** of the email and a description for your recipients. The subject defaults to the workbook file name but you can modify the subject if needed. You can add details in the description section.

    ![Enter a subject in the Subject field.](./assets/recipients-subject.png){width="55%"}

1. Set up the scheduling options to set the date and time that you want the workbook emailed to your recipients.

    Choose the start and end date and time frames. This can be today's date or a date in the future.

    Choose the **Frequency** from the drop-down menu. You can set the frequency to be hourly, daily, weekly, monthly, or yearly on a specific day. For example, you can set up a schedule to send the workbook on the first Sunday night of the month so that your recipients will have the email in their inbox first thing on Monday morning.

    ![Select the frequency to schedule your report.](./assets/frequency.png){width="55%"}

1. After you set the schedule, click **Send on schedule**.

    ![Click Send on schedule.](./assets/send-on-schedule.png){width="55%"}

    You see a confirmation toast at the bottom of the Report Builder hub and the scheduled workbook is listed under the Workbooks tab.

    ![Confirmation toast](./assets/confirmation-toast.png){width="55%"}

## Schedule a converted workbook {#converted}

1. Schedule a [converted](/help/analyze/report-builder/convert-workbooks.md) legacy workbook.

   A pop up appears, asking if you want to use the scheduling metada from the legacy workbook to create a new scheduled task. 

1. If you select **[!UICONTROL Use]**, Report Builder automatically fills in the legacy scheduling information. 

1. Ensure that this information is correct and schedule. 

1. If you want to send the workbook on a different schedule, schedule a completely fresh scheduled task. 


## Send the workbook one-time only

You can also send out the workbook only once.

1. Un-check **Show scheduling options** 

    ![Click Un-check Show scheduling options to send out a workbook one time.](./assets/send-now.png){width="40%"}

1. Click **Send Now**.

## Manage scheduled workbooks

For information about managing workbooks that are already scheduled, see [Manage scheduled workbooks](/help/analyze/report-builder/manage-schedules-reportbuilder.md).

-->