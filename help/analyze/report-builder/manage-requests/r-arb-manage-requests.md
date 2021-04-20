---
description: Veldbeschrijvingen voor Verzoeken beheren in Report Builder.
title: Aanvragen beheren - definities
uuid: 01b21d0e-c870-4df8-95b9-f4aef1f4d16b
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 2%

---


# Aanvragen beheren - definities

Veldbeschrijvingen voor Verzoeken beheren in Report Builder.

## Overzicht {#section_75C288C945FA4781A4EDF806711A5660}

[!UICONTROL Request Manager] verstrekt een gedetailleerde mening van het statuut van alle verzoeken u voor alle bladen of enkel één blad van het actieve werkboek hebt gebouwd. U kunt een verzoek (functies die typisch met [!UICONTROL Request Wizard] en [!UICONTROL Request Manager] worden geassocieerd) ook toevoegen, uitgeven, verfrissen en schrappen door op een beschikbare cel in de spreadsheet van Excel met de rechtermuisknop te klikken die vorige verzoeken bevat.

De [!UICONTROL Request Manager] wordt weergegeven wanneer u op **[!UICONTROL Manage]** ( ![](assets/edit_request.gif) op de werkbalk Report Builder klikt.

>[!NOTE]
>
>Adobe Report Builder dwingt aanvraagafhankelijkheden alleen af binnen hetzelfde werkblad, niet tussen werkbladen. Het beperken tot gebiedsdelen binnen één enkel aantekenvel verzekert tijdigheid van uitvoering.

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
   <td colname="col2"> <p>De verzoeken van vertoningen van alle bladen van het actieve werkboek. Schakel deze optie uit als u aanvragen van specifieke bladen wilt weergeven. Als u deze optie uitzet, moet u op een lusje van het Blad bij de bodem van uw rapport van Excel klikken om de verzoeken te tonen verbonden aan dat blad in <span class="wintitle"> de Manager van het Verzoek </span>. Het etiket naast checkbox wijst op welk blad van het werkboek momenteel de nadruk heeft. </p> </td> 
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
   <td colname="col2"> <p>Geeft de datum aan waarop het verzoek voor het laatst is verwerkt door Report Builder. In deze tabel wordt ook een diagnostisch bericht weergegeven in de kolom <span class="wintitle"> Laatste uitvoering</span>, indien van toepassing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toevoegen </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u het dialoogvenster Wizard Verzoek weer. Zie <a href="/help/analyze/report-builder/data-requests/t-create-a-data-request.md"   > Een gegevensverzoek maken</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bewerken </p> </td> 
   <td colname="col2"> <p> (Of Meerdere bewerken) Hiermee bewerkt u een geselecteerde aanvraag. Het systeem toont het <span class="wintitle"> Dialoogvenster van de Tovenaar van het Verzoek</span>. Zie <a href="/help/analyze/report-builder/manage-requests/t-edit-multiple-requests.md"   > Meerdere verzoeken bewerken</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verwijderen </p> </td> 
   <td colname="col2"> <p>Verwijdert aanvragen. U kunt meerdere geselecteerde aanvragen verwijderen. U kunt een verzoek in de lijst ook schrappen door het verzoek te selecteren en Schrapping op uw toetsenbord te drukken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Alles selecteren </p> </td> 
   <td colname="col2"> <p>Selecteer alle aanvragen. <span class="wintitle"> de Manager van het Verzoek</span> toont het aantal verzoeken u bij de bodem van de verzoeklijst hebt geselecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uit cel </p> </td> 
   <td colname="col2"> <p>Hiermee worden gegevens voor een aanvraag opgehaald uit het werkblad. Als een verzoek wordt geassocieerd met de momenteel geselecteerde cel in het actieve aantekenvel, wordt het bijbehorende verzoek in de lijst geselecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Vernieuwen </p> </td> 
   <td colname="col2"> <p>Hiermee vernieuwt u één aanvraag of een selectie aanvragen. (Zie <a href="/help/analyze/report-builder/manage-requests/t-refresh-a-request.md"   > Een verzoek vernieuwen</a>.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lijst vernieuwen </p> </td> 
   <td colname="col2"> <p>Hiermee vernieuwt u alle weergegeven aanvragen. Wanneer u alle verzoeken vernieuwt, is de tijd om de informatie van de server aan uw rapport bij te werken direct evenredig aan de ingewikkeldheid van de verzoeken in het rapport. Voor zeer grote rapporten, kan het verfrissen van alle verzoeken verscheidene notulen vereisen. Om deze reden, kunt u de meest dringende verzoeken willen individueel bijwerken, en <span class="wintitle"> selecteert allen </span> op een ander, minder tijd-cruciaal ogenblik verfrissen. </p> <p> <p>Opmerking: Het wordt geadviseerd dat u resultaten vaak in <span class="wintitle"> de Manager van het Verzoek </span> controleert als u een aantekenvel verfrist die veelvoudige verzoeken bevat. Als een aanvraagfout optreedt, kunt u met het foutbericht in de diagnostische kolom de bron van de fout bepalen. Terwijl in de meeste gevallen een foutenmelding wordt getoond wanneer een verzoek ontbreekt, merk op dat af en toe geen foutenmelding wordt geproduceerd. Het kan zijn dat bij een vernieuwingsbewerking de gegevens niet worden bijgewerkt in een cel die een verwijzing bevat, of dat bij een update de gegevens uit de cel worden verwijderd. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

