---
description: Met het deelvenster Activiteitenkaarten kunt u de instellingen en eigenschappen voor alle typen overlayvisualisaties wijzigen.
title: Instellingen Activiteitenkaart configureren
topic: Activity map
uuid: 42a0309e-3efc-4506-989b-09b6fe419423
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Instellingen Activiteitenkaart configureren

Met het deelvenster Activiteitenkaarten kunt u de instellingen en eigenschappen voor alle typen overlayvisualisaties wijzigen.

Open het deelvenster Instellingen activiteitenkaart dat u wilt openen door op het tandwielpictogram op de werkbalk Activiteitenkaart te klikken.

In het deelvenster Instellingen wordt andere inhoud weergegeven op basis van de geselecteerde toepassingsmodus. Het tabblad Overige bevat algemene instellingen.

| Standaard | **[!UICONTROL Gradient]** of **[!UICONTROL Bubble]** overlays |
|---|---|
| Live | **[!UICONTROL Gainers & Losers]**, **[!UICONTROL Gradient]**, **[!UICONTROL Bubble]** overlays |
| Overige | De selectie van de Reeks van het rapport en de Selectie van de Taal |

## Instellingen voor overlay in de standaardmodus {#section_24DB95376E1A448494ECF3F57743FC19}

![](assets/settings_standard.png)

<table id="table_0244107DE6D142F2A1DA4882E0ED9826"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> Instellingen </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Labelbedekkingen met</span> </td> 
   <td colname="col3"> 
    <ul id="ul_13AD02789F2D4904A35215A8FA230F3E"> 
     <li id="li_8DB71636D2074C69B0D94D3FB0CAFE28"> <b>Geen label</b>: alleen van toepassing op de verloopbedekking. In dit geval geeft de kleur van de overlay een betekenis voor de rangschikking van de koppeling </li> 
     <li id="li_39C98D7EA9514C1D8731B9D21C0E73A6"> <b>Waarde</b>: het onbewerkte metrische totaal voor die koppeling </li> 
     <li id="li_A5F583E45BCD4F2399398F9DCC7FE382"> <b>Percentage</b>: percentage van metrisch voor deze verbinding op totale metrisch voor de pagina. </li> 
     <li id="li_E4BF7D3B863E4B6C8E737CF29ADA9D67"> <b>Rang</b>: rang van deze koppeling voor alle koppelingen die zich op de weergegeven pagina bevinden </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Tekengrootte label</span> </td> 
   <td colname="col3"> Hiermee kunt u de tekengrootte van het bedekkingslabel met een schuifregelaar vergroten/verkleinen voor betere leesbaarheid. </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Weergave</span> </td> 
   <td colname="col3">Selecteer <span class="uicontrol"> Boven</span>, <span class="uicontrol"> Onder</span>of <span class="uicontrol"> Alle koppelingen</span> om weer te geven in de bedekking. Als u Boven of Onder selecteert, moet u ook het aantal koppelingen selecteren dat u wilt weergeven. </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Bedekkingen verbergen voor koppelingen die geen treffers hebben ontvangen.</span> </td> 
   <td colname="col3"> Met dit selectievakje kunt u bedekkingen verbergen voor koppelingen die geen treffers hebben ontvangen om de interface overzichtelijker te maken. </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Verloopkleur/Bubble-kleur</span> </td> 
   <td colname="col3">Selecteer een van de kleuren om overlaykoppelingsmarkeringen voor <span class="uicontrol"> Verloop</span> - of <span class="uicontrol"> Bubblebedekking</span> weer te geven. </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Kleurverloop op basis van</span> </td> 
   <td colname="col3"> 
    <ul id="ul_1B5C2A44A9EB465D8B8E9AD91AF79D69"> 
     <li id="li_C983CB68B90B492BB0774254292B5961"> <span class="uicontrol"> Hoogste 30 classificaties</span>: De kleurintensiteit wordt genormaliseerd voor de bovenste 30 waarden. </li> 
     <li id="li_1E83431C8C734AB0BC82B5A66AED1189"> <span class="uicontrol"> Absolute metrische waarde</span>: De kleurintensiteit is een functie van de absolute metrische waarde. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Transparantie verloop</span> </td> 
   <td colname="col3">Selecteer het transparantieniveau voor de verloopbedekkingen. <p>Deze instelling heeft geen invloed op de Bubble-overlays. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Instellingen voor overlays in de live modus {#section_D30F6E62FB5D404090B588F396A460AF}

![](assets/settings_live.png)

| Instellingen | Beschrijving |
|---|---|
| **[!UICONTROL Display Top]** | Selecteer het aantal koppelingen dat u wilt weergeven (of alle koppelingen) en het **[!UICONTROL Gainers]** of **[!UICONTROL Losers]** (of beide) dat u wilt weergeven als overlays. |
| **[!UICONTROL Exclude bottom (%)]** | Schakel deze optie in om te voorkomen dat er koppelingen zijn naar Gainers-Losers met dunne gegevens. Filter het onderste percentage van koppelingswijzigingen uit om alleen de koppelingen weer te geven met voldoende gegevens om relevante winsten of verliezen weer te geven. Het percentage wordt berekend op basis van het aantal koppelingen op die pagina. Als u bijvoorbeeld de onderste 10% van een lijst met 200 koppelingen verwijdert, worden de laatste 20 koppelingen verwijderd. |
| **[!UICONTROL Auto Update Data]** | Hiermee kunt u bepalen of de analysegegevens die in de interface worden weergegeven, automatisch moeten worden bijgewerkt wanneer een nieuwe periode wordt berekend of niet. |
| **[!UICONTROL Auto Update Period]** | Als deze optie is ingeschakeld, wordt de webpagina vernieuwd met elke nieuwe gegevensophaling, zodat de koppelingen op de pagina nauwer kunnen worden gesynchroniseerd met de verzamelde gegevens. |

## Overige instellingen {#section_697A12F099494D699A4BF498598178C5}

![](assets/settings_other.png)

<table id="table_0F560236F8844FA0928CBB9C50D5ABEF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> Rapportsuite </td> 
   <td colname="col2"> <p>De lijst met rapportsuites die voor u toegankelijk zijn, is niet meer beperkt tot de rapportsuites die zijn gedefinieerd in de webpaginatag. U kunt de geselecteerde rapportsuite (die overeenkomt met een van de tags op de pagina) nu vervangen door een andere rapportsuite. Deze nieuwe rapportsuite hoeft niet te worden gekoppeld aan een tag op de pagina. Als u de geselecteerde rapportsuite wijzigt in Instellingen activiteitenkaart, worden alle betrokken analyserapporten vernieuwd door het proces <span class="uicontrol"> Opslaan</span> . </p> <p> <p>Belangrijk: Virtuele rapportsets zijn alleen in de standaardmodus niet compatibel met de live modus. Als u in de live modus voor een standaard rapportsuite werkt, maar in dit dialoogvenster een virtuele rapportsuite selecteert, wordt de standaardmodus weergegeven wanneer u hier op <span class="uicontrol"> OK</span> klikt. </p> </p> <p>Bovendien zal de controle van de Kalender opnieuw worden geïnitialiseerd om het de kalendertype van de rapportreeks (Gregorian, kleinhandel, douane..) aan te passen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Taal </td> 
   <td colname="col2"> De selectie komt overeen met de talen die worden aangeboden voor Adobe Analytics. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Info </td> 
   <td colname="col2"> Geeft de naam en het versienummer van de toepassing aan. </td> 
  </tr> 
 </tbody> 
</table>

