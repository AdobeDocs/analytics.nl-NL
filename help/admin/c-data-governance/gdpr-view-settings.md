---
description: Het dialoogvenster Data Governance in Admin Tools biedt een overzicht van welke rapportsuites zijn geconfigureerd voor data-governance, of ze zijn toegewezen aan een Experience Cloud-organisatie, en of er een dataretentiebeleid voor deze rapportsuite bestaat.
title: Data Governance-instellingen voor een rapportsuite weergeven/beheren
feature: Data Governance
exl-id: 87b0be42-1098-4e72-8eb8-0c1bb56791f8
source-git-commit: f6199620033af9c8e304bd0f537d4e0b052ed64d
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 100%

---

# Data Governance-instellingen voor een rapportsuite weergeven/beheren

Het dialoogvenster Data Governance in Admin Tools biedt een overzicht van welke rapportsuites zijn geconfigureerd voor data-governance, of ze zijn toegewezen aan een Experience Cloud-organisatie, en of er een dataretentiebeleid voor deze rapportsuite bestaat.

1. Meld u aan bij Adobe Experience Cloud.
1. Ga naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Data Governance]**.

   U ziet rapportsuites die deel van uw aanmeldingsbedrijf uitmaken:

   ![](assets/privacy_setup_an.png)

<table id="table_448292730FF0475E9DCB731882F9A29B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Instelling </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Rapportsuites </p> </td> 
   <td colname="col2"> <p>De eerste rij vermeldt de friendly name van de rapportsuite. De tweede rij bevat de interne naam van de rapportsuite. Als u labels voor een rapportsuite mag instellen, is de eerste rij een klikbare koppeling die u naar de labelpagina brengt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Organisatietoewijzing </p> </td> 
   <td colname="col2"> 
    <ul id="ul_EF8F613B0C5E42D19DB60BD0C89C114B"> 
     <li id="li_B35EE88555F547EFBF55ADE9D0C9EC3B"><b>Toegewezen</b>: Deze rapportsuite is al toegewezen aan dezelfde Experience Cloud-organisatie als het aanmeldingsbedrijf voor Analytics waarbij u bent aangemeld. Alleen rapportsuites met deze instelling kunnen worden gelabeld. </li>
     <li id="li_FF825A65D089487BBF5FCB0D74D41CD7"><b>Toegewezen aan een andere organisatie</b>: Deze rapportsuite is al aan een andere Experience Cloud-organisatie toegewezen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dataretentiebeleid </p> </td> 
   <td colname="col2"> <p>Voor de Analytics Data Privacy-implementatie hebt u een dataretentiebeleid nodig. </p> <p>Met deze instelling wordt het volgende getoond: </p> 
    <ul> 
     <li>of er een dataretentiebeleid is voor deze rapportsuite, en </li> 
     <li>hoe lang de data door Adobe worden bewaard voordat ze worden verwijderd. De standaard dataretentieperiode is 25 maanden. </li> 
    </ul> <p>Opmerking:  Adobe Analytics kan u niet helpen bij het verwerken van aanvragen bij de Data Privacy-API, dat wil zeggen, het verwerken van toegangs- of verwijderingsaanvragen die u van uw eindgebruikers ontvangt, als de dataretentieperiode niet is ingesteld. Neem contact op met de Customer Success Manager om de periode voor dataretentie in te stellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Groepen </p> </td> 
   <td colname="col2"> <p>Groeperingsfunctionaliteit is momenteel niet geïmplementeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Linkerzijbalk </p> </td> 
   <td colname="col2"> <p>Klik op het trechterpictogram om de zijbalk te openen of te sluiten. </p> <p>In de sectie Organisatietoewijzing wordt het aantal rapportsuites weergegeven dat in elk van de beschreven categorieën valt. </p> <p>In de sectie Dataretentiebeleid wordt elk uniek dataretentiebeleid weergegeven dat momenteel geldt voor uw organisatie, en het aantal rapportsuites dat aan dit retentiebeleid is toegewezen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Exporteren naar CSV </p> </td> 
   <td colname="col2"> <p>Als u het selectievakje naast een of meer rapportsuites selecteert, wordt de optie <span class="uicontrol">Exporteren naar CSV</span> weergegeven. Met deze optie kunt u een CSV-bestand downloaden met alle huidige labeldefinities voor alle variabelen voor alle geselecteerde rapportsuites. </p> <p>We adviseren dat uw juridische team uw labelkeuzes controleert, en deze optie maakt die controle mogelijk. U kunt het CSV-bestand met het team delen, zodat ze de controle niet hoeven uit te voeren terwijl ze zijn aangemeld bij de Data Governance-gebruikersinterface. </p> <p><img placement="break"  src="assets/export_csv.png" width="300px" id="image_5FE821B2D07B402D8E0F6FE53D6FC52E" /> </p> </td> 
  </tr> 
 </tbody> 
</table>
