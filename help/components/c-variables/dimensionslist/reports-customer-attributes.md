---
description: Een veelgestelde vragen over analysemogelijkheden voor klantkenmerken en hoe het rapport Klantkenmerken moet worden uitgevoerd.
solution: Experience Cloud,Analytics
title: Klantkenmerken
uuid: 94721265-ba23-45d5-8807-76f81b0b8a30
translation-type: tm+mt
source-git-commit: ''

---


# Klantkenmerken

Een veelgestelde vragen over analysemogelijkheden voor klantkenmerken en hoe het rapport Klantkenmerken moet worden uitgevoerd.

**[!UICONTROL Reports]** **[!UICONTROL > Visitor Profile]** > **[!UICONTROL Customer Attributes]**

Als u gegevens van ondernemingsklanten in een gegevensbestand van het het relatiebeheer van de klant (CRM) vangt, kunt u de gegevens in een gegevensbron van de klantenattributen in de Wolk van de Ervaring uploaden. Nadat de gegevens zijn geüpload, kunt u het rapport Klantkenmerken in Rapporten &amp; Analytics uitvoeren.

* [Kenmerken van de klant en rapporteringsmetriek in Analytics](/help/components/c-variables/dimensionslist/reports-customer-attributes.md#section_EF343662146B460A882D3DF772ADD86D)
* [Veelgestelde vragen - Klantkenmerken in analyse](/help/components/c-variables/dimensionslist/reports-customer-attributes.md#section_E29641D1F3D649C1AC9EA5231921F038)

Raadpleeg [Klantkenmerken](https://marketing.adobe.com/resources/help/en_US/mcloud/attributes.html) in de Help van Experience Cloud voor meer informatie over het uploaden van klantkenmerkgegevens.

## Kenmerken van de klant en rapporteringsmetriek in Analytics {#section_EF343662146B460A882D3DF772ADD86D}

Nadat u klantenattributen uploadt en het schema (in de Wolk van de Ervaring) bevestigt, leidt het systeem metriek die op de vriendschappelijke namen (als *`age`* of *`gender`*) wordt gebaseerd die u aan de attributenkoorden en gehelen in kaart brengt. Deze metriek wordt weergegeven in rapporten van **[!UICONTROL Visitor Profile]** > **[!UICONTROL Customer Attributes]** .

Bijvoorbeeld:

**[!UICONTROL Visitor Profile]** > **[!UICONTROL Customer Attributes]** > **[!UICONTROL Age]**

![](assets/report_age.png)

**Voorbeeld: leeftijdsmetriek**

Als u een tekenreeks opgeeft als *`age`*, maakt het systeem de volgende metriek en afmetingen:

* Leeftijdsdimensie: Laat u een rapport in werking stellen dat op de attributen van de Leeftijd wordt gebaseerd.
* Metrische leeftijd: Metrisch kunt u aan een rapport, zoals een Uniek rapport van Bezoekers toevoegen.
* Aantal metrische leeftijdscijfers: Hiermee kunt u begrijpen, bijvoorbeeld, of bezoekers een *`age`* waarde op een formulier hebben opgegeven.

Omdat de metriek sommen in een rapportlijst zijn, zou u berekende metrisch [moeten](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/) creëren die u de gemiddelde leeftijd vertelt. De formule voor deze metrische waarde is `Age / Count of Age`.

## Veelgestelde vragen - Klantkenmerken in analyse {#section_E29641D1F3D649C1AC9EA5231921F038}

<table id="table_88631069013B408EBB0A810657662B36"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Waarom is het beter om de identiteitsservice te gebruiken om de klant-id in te stellen in plaats van de klant-id in een prop of eVar te vullen? </p> </td> 
   <td colname="col2"> <p>Het gebruik van de identiteitsservice biedt een aantal voordelen: </p> 
    <ul id="ul_5D3659604D43419F9CA5920B4F93728E"> 
     <li id="li_BA2EF0715C5A47EFAFA7191CFAD088A4">Als u de klant-id niet instelt bij Identiteitsservice, zijn de klantgegevens alleen beschikbaar voor Adobe Analytics. Als u de klantenverslagen voor in real time het richten wilt gebruiken, moet u de Dienst van de Identiteit gebruiken. </li> 
     <li id="li_228358684E474A298E39578D427BF932">Als u de identiteitsservice gebruikt om de klant-id in te stellen, neemt het synchroniseren van id's met de Experience Cloud minder tijd in beslag. Als u de klant-id in een prop of eVar plaatst, worden de klant-id's naar de Experience Cloud verzonden via back-end serversynchronisatie die in batches plaatsvindt. De identiteitsservice synchroniseert de klant-id direct met de Experience Cloud. </li> 
     <li id="li_BCF28219E4014FCF9F747C3D8D270526"> Als u de Identity Service gebruikt in plaats van een prop of eVar, wordt die prop of eVar vrijgemaakt voor andere toepassingen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Als ik al een klant-id opslaat in een prop of eVar, waarom zou ik deze nieuwe functionaliteit gebruiken in plaats van mijn prop of eVar te classificeren met de attributen van CRM? </p> </td> 
   <td colname="col2"> <p>Props en eVars zijn onderworpen aan Uniques Exceeded beperkingen. Met deze functionaliteit kunt u kenmerkgegevens voor een onbeperkt aantal klant-id's invoeren. Bovendien beperkt de prop/eVar-benadering de CRM-informatie tot Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoe worden mijn CRM-kenmerken weergegeven in Adobe Analytics? </p> </td> 
   <td colname="col2"> <p>De attributen van CRM zullen in de Werkruimte van de Analyse, Rapporten &amp; Analyse, Ad hoc Analyse, rapporteringsAPI, en de Bouwer van het Rapport manifest zijn. Tekstkenmerken worden weergegeven als rapporten/afmetingen. Numerieke kenmerken worden weergegeven als afmetingen en metriek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zijn de CRM-gegevens beschikbaar in Data Warehouse en in Data Feeds? </p> </td> 
   <td colname="col2"> <p>De CRM-gegevens zijn momenteel niet beschikbaar in Data Warehouse of Analytics Data Feed. </p> </td> 
  </tr> 
 </tbody> 
</table>

