---
description: U kunt het leveringsschema voor rapporten aanpassen. U kunt de levering op een bepaald ogenblik tegenhouden, of het aantal tijden specificeren u een rapport wilt verzenden. De nieuwe programma's gebruiken de datumwaaier die in het rapport wordt bepaald. Als u bijvoorbeeld een rapport maakt voor de laatste 90 dagen en het dagelijks laat uitvoeren, ontvangt u elke dag een rapport voor de laatste 90 dagen. Als u een rapport met een statische datumwaaier van de kalender creeert, zult u het zelfde rapport zien telkens als het wordt verzonden.
title: Planningsbeheer
topic: Ad hoc analysis
uuid: 82a054ef-109d-414d-a6e1-e09ee57c163f
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Planningsbeheer

U kunt het leveringsschema voor rapporten aanpassen. U kunt de levering op een bepaald ogenblik tegenhouden, of het aantal tijden specificeren u een rapport wilt verzenden. De nieuwe programma&#39;s gebruiken de datumwaaier die in het rapport wordt bepaald. Als u bijvoorbeeld een rapport maakt voor de laatste 90 dagen en het dagelijks laat uitvoeren, ontvangt u elke dag een rapport voor de laatste 90 dagen. Als u een rapport met een statische datumwaaier van de kalender creeert, zult u het zelfde rapport zien telkens als het wordt verzonden.

## Planningsbeheer {#concept_A1CDE14B72A54DD6AE17B816092CAB8B}

U kunt het leveringsschema voor rapporten aanpassen. U kunt de levering op een bepaald ogenblik tegenhouden, of het aantal tijden specificeren u een rapport wilt verzenden. De nieuwe programma&#39;s gebruiken de datumwaaier die in het rapport wordt bepaald. Als u bijvoorbeeld een rapport maakt voor de laatste 90 dagen en het dagelijks laat uitvoeren, ontvangt u elke dag een rapport voor de laatste 90 dagen. Als u een rapport met een statische datumwaaier van de kalender creeert, zult u het zelfde rapport zien telkens als het wordt verzonden.

>[!NOTE] Wanneer een gebruikersaccount is uitgeschakeld, worden alle geplande rapportleveringen die door die gebruiker zijn gemaakt, opgeschort.

Om ervoor te zorgen dat de lijnpunten in een verdeling in bewaarde en geplande rapporten blijvend zijn, gebruik de **[!UICONTROL Edit Items]** eigenschap in de Bouwer [van de](/help/analyze/ad-hoc-analysis/c-tablebuilder.md) Lijst om vaste afmetingslijsten in onderverdelingen tot stand te brengen.

>[!IMPORTANT]
>
>Met Ad hoc-analyse kunt u snel rapporten definiëren en plannen voor specifieke, tijdige en ad-hocrapportagebehoeften. Het is niet ontworpen voor de volledige uitvoer van gegevens met een massaal aantal of rijen, kolommen, metrische evaluaties, of uitgebreide onderverdelingen die gegevensextracten gebruiken.
>
>Praktische beperkingen voor geplande rapportage in ad hoc analyse zijn gebaseerd op dit beginsel: Als uw rapport niet binnen tien minuten bouwt (de onderbreking voor ad hoc Analyse), dan is uw rapport zeer waarschijnlijk te complex.
>
>Het waarschijnlijkst heeft uw rapport teveel metriek, teveel afsplitsingen van afmetingselementen, teveel rijen of kolommen, of andere extremen die het te lang een proces van de rapportgeneratie voor Ad hoc Analyse maken. Dit type rapport moet worden uitgevoerd in Data Warehouse, een Adobe Analytics-functie die is ontwikkeld voor volledige gegevensextractie die offline wordt uitgevoerd, en het genereren van rapporten die vele uren of dagen in beslag kan nemen.
>
>Bijvoorbeeld, kan Ad hoc Analyse 50.000 rijen van gegevens behandelen, maar het breken van dat de gegevens voor tien browser types betekent 50.000 keer 10, een exponentiële verhoging die voor een ad hoc rapporteringshulpmiddel kan te complex zijn. De extra uitsplitsingen verhogen opnieuw exponentieel de rijen van gegevens. Het bepalen van het daadwerkelijke aantal of de rijen, de kolommen, en de onderverdelingen om voor Ad hoc de rapportering van de Analyse te beperken kan niet in stark termijnen worden bepaald maar is een combinatie van al deze factoren.

## Een rapport voor levering plannen {#task_7A3165C8C5C349718FE3B2B0C727ACFD}

Stappen die beschrijven hoe te om een rapport voor levering te plannen.

<!-- 

t_schedule_delivery.xml

 -->

1. Klik **[!UICONTROL Tools]** en klik vervolgens op **[!UICONTROL Schedule Manager]**.
1. Klik op de [!UICONTROL Schedule Manager]knop **[!UICONTROL New.]**

## Leveringsopties - Definities {#reference_CA49AC560258471AAE959BCA243F170C}

Definities voor de instellingen voor leveringsopties.

<!-- 

r_delivery_options.xml

 -->

U kunt de gegevens die worden weergegeven in het geselecteerde rapport, verzenden naar de indeling die u selecteert. U kunt het één keer verzenden of een leveringsschema instellen en de gewenste bestandsindeling opgeven. U kunt een digitale handtekening maken en verzenden om de ontvanger van het bestand te verzekeren dat het bestand authentiek is. U kunt het bestand naar een e-mailadres verzenden of uploaden naar een FTP-server.

<table id="table_C18A0F1C9E214EB585A29801BA2400F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Veld </p> </th> 
   <th colname="col2" class="entry"> <p>Definitie </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Naam </p> </td> 
   <td colname="col2"> <p> De configureerbare naam van dit rapport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID </p> </td> 
   <td colname="col2"> <p>Vertelt u rapportID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Bestandsindeling </p> </td> 
   <td colname="col2"> 
    <ul id="ul_711C2D9B216C48359F7B42521D927872"> 
     <li id="li_36E8DEFDA1B84890A4204A6DFF4E0267">Excel: Hiermee wordt uw rapport uitgevoerd in een spreadsheet, inclusief alle afbeeldingen. Bewerkbaar in Microsoft Excel. </li> 
     <li id="li_C918FA3AE8194BD2B59E554DAC7CBBE2">CSV: Hiermee wordt uw rapport uitgevoerd in door komma's gescheiden waarden. Bewerkbaar in een eenvoudige teksteditor (zoals Kladblok) of een spreadsheet-editor (zoals Excel). Bevat geen afbeeldingen. </li> 
     <li id="li_B7C8C098C5264B349C21077A0DEFE059">PDF: Hiermee wordt uw rapport uitgevoerd in Portable Document Format. Niet-bewerkbaar en weergavebaar in Adobe Acrobat of Adobe Reader. </li> 
     <li id="li_B1183DB25DE34B689FBD0E5B44691F49">HTML: Hiermee wordt uw rapport uitgevoerd in een bijlage bij de Hypertext Markup Language. Deze indeling bestaat voor de meeste websites. Niet bewerkbaar, tenzij u bekend bent met HTML-code. </li> 
     <li id="li_5ED5F1862AB1490A9FF5695FF9F52C5E">Woord: Hiermee wordt uw rapport uitgevoerd in Rich Text Format, inclusief alle afbeeldingen. Bewerkbaar in Microsoft Word of WordPad. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Geavanceerd </p> </td> 
   <td colname="col2"> <p> Zie <a href="/help/analyze/ad-hoc-analysis/c-schedule.md"   > Geavanceerde indelingsinstellingen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bestandsbestemming </p> </td> 
   <td colname="col2"> <p>E-mail: Instellingen voor verzending via e-mail. </p> <p>FTP: Instellingen voor uploaden naar een FTP-server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportbereik en leveringsschema </p> </td> 
   <td colname="col2"> <p>Specificeert wanneer om het rapport te leveren. De nieuwe programma's gebruiken de datumwaaier die in het rapport wordt bepaald. Als u bijvoorbeeld een rapport maakt voor de laatste 90 dagen en het dagelijks laat uitvoeren, ontvangt u elke dag een rapport voor de laatste 90 dagen. Als u een rapport met een statische datumwaaier van de kalender creeert, zult u het zelfde rapport zien telkens als het wordt verzonden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Geavanceerde indelingsinstellingen - Definities {#reference_F99B65BF7C9746638D8147EED147015B}

Definities voor de instellingen bij Geavanceerde opmaakinstellingen.

<!-- 

r_advanced_format_settings_dsc.xml

 -->

<table id="table_CD0888E8390745F4B83DF6AC69CB0854"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Veld </p> </th> 
   <th colname="col2" class="entry"> <p>Definitie </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Bestandsnaam </p> </td> 
   <td colname="col2"> <p>Een door de gebruiker gedefinieerde bestandsnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Id toevoegen aan bestandsnaam </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de rapport-id automatisch aan de bestandsnaam toegevoegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Datum toevoegen aan bestandsnaam </p> </td> 
   <td colname="col2"> <p> Hiermee voegt u automatisch de datum van het rapport toe aan de bestandsnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Taal </p> </td> 
   <td colname="col2"> <p> Hiermee kunt u een taal voor het rapport selecteren. U kunt het rapport in om het even welke volgende talen verzenden ongeacht de taal die u gebruikt </p> 
    <ul id="ul_BD3D331B0D6146F79A6D254136E43920"> 
     <li id="li_0EE6A371B1BB4627BD3F64BD0EF07E44">Engels </li> 
     <li id="li_5EF76261928543FDB36D99E4C89DE994">Spaans </li> 
     <li id="li_FABF47E8CD64486BA1567E02460422C5">Vereenvoudigd Chinees </li> 
     <li id="li_8A6BC2DE92DB47DA9397B8931D8DCC6E">Traditioneel Chinees </li> 
     <li id="li_EDA24D700BE040E8B839B82E31DABC28">Frans </li> 
     <li id="li_A8D41DCCC91542BB8D0A522EC99575E8">Duits </li> 
     <li id="li_E9F73C93C94A46B78BCE85A7261CEDD4">Japans </li> 
     <li id="li_699B97050AA54D818659C191F4594E4E">Portugees </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Codering </p> </td> 
   <td colname="col2"> <p>Hiermee wordt een coderingstype opgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Rapport verzenden als gecomprimeerd bestand </p> </td> 
   <td colname="col2"> <p> Hiermee wordt het bestand gecomprimeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Digitale handtekeningbestand verzenden </p> </td> 
   <td colname="col2"> <p>Hiermee maakt u een digitale handtekening die u met de e-mail wilt verzenden. </p> </td> 
  </tr> 
 </tbody> 
</table>

