---
description: Meer informatie over de veldbeschrijvingen voor Verzoeken beheren in Report Builder.
title: Hoe te om verzoeken in Report Builder te beheren
uuid: 01b21d0e-c870-4df8-95b9-f4aef1f4d16b
feature: Report Builder
role: User, Admin
exl-id: fd8c0145-4c7e-4f07-aa63-656a8a20724c
source-git-commit: 12d048b42c6a61e03dbbe73acb9d34df3e37693c
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# Verzoeken beheren - definities

Bekijk details van een verzoekstatus en gebruik de gebiedsbeschrijvingen om verzoeken in Report Builder te beheren.

## Overzicht {#section_75C288C945FA4781A4EDF806711A5660}

[!UICONTROL Request Manager] verstrekt een gedetailleerde mening van de status van alle verzoeken u voor alle bladen of enkel één blad van het actieve werkboek bouwde. U kunt ook een aanvraag toevoegen, bewerken, vernieuwen en verwijderen. Deze functies worden meestal gekoppeld aan de [!UICONTROL Request Wizard] en [!UICONTROL Request Manager] wanneer u met de rechtermuisknop op een beschikbare cel in het Excel-werkblad klikt dat eerdere aanvragen bevat.

De [!UICONTROL Request Manager] wordt weergegeven wanneer u op **[!UICONTROL Manage]** ![](assets/edit_request.gif) klikt op de werkbalk Report Builder.

>[!NOTE]
>
>Adobe Report Builder dwingt aanvraagafhankelijkheden alleen af binnen hetzelfde werkblad, niet tussen werkbladen. Het beperken tot gebiedsdelen binnen één enkel aantekeningsblad verzekert uitvoeringstijdelijkheid.

## Definities {#section_FD29D8614DE74F32A0027FA130F40304}

<table id="table_0880204181074BDBBA37E3DF2972A672"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Veld </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Alle bladen </p> </td> 
   <td colname="col2"> <p>De verzoeken van vertoningen van alle bladen van het actieve werkboek. Schakel deze optie uit als u aanvragen van specifieke bladen wilt weergeven. Als u deze optie uitzet, moet u op een lusje van het Blad bij de bodem van uw rapport van Excel klikken om de verzoeken te tonen verbonden aan dat blad in de <span class="wintitle"> Manager van het Verzoek </span>. Het etiket naast checkbox wijst op welk blad van het werkboek momenteel de nadruk heeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Werkblad </p> </td> 
   <td colname="col2"> <p>Toont de naam van de bladen in het werkboek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportsuite </p> </td> 
   <td colname="col2"> <p>Toont de naam van de rapportreeks. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datumbereik </p> </td> 
   <td colname="col2"> <p>Toont de gespecificeerde datumwaaier van het rapport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Granulariteit </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u de granulariteit van de aanvraag op. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Laatste uitvoering </p> </td> 
   <td colname="col2"> <p>Geeft de datum aan waarop het verzoek voor het laatst is verwerkt door de Report Builder. Een diagnostisch bericht wordt ook getoond in deze lijst in de <span class="wintitle"> laatste looppas </span> kolom, indien van toepassing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toevoegen </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u het dialoogvenster Wizard Verzoek weer. Zie <a href="/help/analyze/legacy-report-builder/data-requests/t-create-a-data-request.md"   > Een gegevensaanvraag maken </a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bewerken </p> </td> 
   <td colname="col2"> <p> (Of Meerdere bewerken) Hiermee bewerkt u een geselecteerde aanvraag. Het systeem toont de <span class="wintitle"> Tovenaar van het Verzoek </span> dialoog. Zie <a href="/help/analyze/legacy-report-builder/manage-requests/t-edit-multiple-requests.md"   > Meerdere verzoeken bewerken </a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verwijderen </p> </td> 
   <td colname="col2"> <p>Verwijdert aanvragen. U kunt meerdere geselecteerde aanvragen verwijderen. U kunt een verzoek in de lijst ook schrappen door het verzoek te selecteren en Schrapping op uw toetsenbord te drukken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Alles selecteren </p> </td> 
   <td colname="col2"> <p>Selecteer alle aanvragen. De <span class="wintitle"> Manager van het Verzoek </span> toont het aantal verzoeken u bij de bodem van de verzoeklijst hebt geselecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uit cel </p> </td> 
   <td colname="col2"> <p>Hiermee worden gegevens voor een aanvraag opgehaald uit het werkblad. Als een verzoek wordt geassocieerd met de momenteel geselecteerde cel in het actieve aantekenvel, wordt het bijbehorende verzoek in de lijst geselecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Vernieuwen </p> </td> 
   <td colname="col2"> <p>Hiermee vernieuwt u één aanvraag of een selectie aanvragen. (Zie <a href="/help/analyze/legacy-report-builder/manage-requests/t-refresh-a-request.md"   > Een aanvraag vernieuwen </a> .) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lijst vernieuwen </p> </td> 
   <td colname="col2"> <p>Hiermee vernieuwt u alle weergegeven aanvragen. Wanneer u alle verzoeken vernieuwt, is de tijd om de informatie van de server aan uw rapport bij te werken direct evenredig aan de ingewikkeldheid van de verzoeken in het rapport. Voor zeer grote rapporten, kan het verfrissen van alle verzoeken verscheidene notulen vereisen. Daarom kunt u de meest dringende verzoeken afzonderlijk bijwerken en <span class="wintitle"> Alles vernieuwen </span> selecteren op een ander, minder tijd-cruciaal moment. </p> <p> <p>Nota: Het wordt geadviseerd dat u resultaten vaak in <span class="wintitle"> Manager van het Verzoek </span> controleert als u een aantekenvel verfrist die veelvoudige verzoeken bevat. Als er een fout optreedt bij een aanvraag, kunt u met het foutbericht in de diagnostische kolom de bron van de fout bepalen. Terwijl in de meeste gevallen een foutenmelding wordt getoond wanneer een verzoek ontbreekt, merk op dat af en toe geen foutenmelding wordt geproduceerd. Het kan zijn dat bij een vernieuwingsbewerking de gegevens niet worden bijgewerkt in een cel die een verwijzing bevat, of dat bij een update de gegevens uit de cel worden verwijderd. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>
