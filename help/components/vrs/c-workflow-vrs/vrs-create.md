---
description: Voordat u virtuele rapportsuites gaat maken, moet u rekening houden met een aantal zaken.
keywords: Virtuele rapportsuite
title: Virtuele rapportsuites maken
feature: Grondbeginselen van rapporten en analyses
uuid: 022a6656-808e-4c92-b7ec-4d2a42e84fa8
exl-id: 5ff6ff1a-5b99-41cc-a3a7-928197ec9ef9
translation-type: tm+mt
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 4%

---

# Virtuele rapportsuites maken

Voordat u virtuele rapportsuites gaat maken, moet u rekening houden met een aantal zaken.

* Gebruikers die geen beheerder zijn, kunnen de Virtual Report Suite Manager niet zien.
* Virtuele rapportsuites kunnen niet worden gedeeld. &quot;Delen&quot; wordt uitgevoerd via groepen/machtigingen.
* In de Virtuele Manager van de Reeks van het Rapport, kunt u slechts uw eigen virtuele rapportreeksen zien. U moet op Alles tonen klikken om iedereen te zien.

1. Ga naar **[!UICONTROL Components]** > **[!UICONTROL Virtual Report Suites]**.
1. Klik op **[!UICONTROL Add +]**.

   ![](assets/new_vrs.png)

1. Vul de velden in:

<table id="table_0F85B56480BB46CBA5BE236BBD70156D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> <p>De naam van de virtuele rapportreeks wordt niet geërft van de ouderrapportreeks en zou verschillend moeten zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beschrijving </td> 
   <td colname="col2"> <p>Voeg een goede beschrijving toe ten behoeve van uw zakelijke gebruikers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tags </td> 
   <td colname="col2"> <p>U kunt codes toevoegen om uw rapportsuites te organiseren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Groepen </td> 
   <td colname="col2"> <p>Selecteer de machtigingsgroepen die u toegang tot dit VRS wilt hebben. (U kunt groepsmachtigingen ook beheren vanuit <span class="ignoretag"><span class="uicontrol"> Admin</span> &gt; <span class="uicontrol"> Gebruikersbeheer</span> &gt; <span class="uicontrol"> Groepen</span></span>.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bovenliggende rapportsuite </td> 
   <td colname="col2"> <p>De rapportsuite waarvan deze virtuele rapportsuite de volgende instellingen overneemt. De meeste de dienstniveaus en eigenschappen (bijvoorbeeld, eVar montages, de Regels van de Verwerking, Classificaties, etc.) worden geërft. Als u wijzigingen wilt aanbrengen in deze overgeërfde instellingen op een VRS, moet u de bovenliggende rapportsuite bewerken (<span class="ignoretag"><span class="uicontrol"> Admin</span> &gt; <span class="uicontrol"> Rapportsets</span></span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijdzone </td> 
   <td colname="col2"> <p>Het kiezen van een tijdzone is optioneel. </p> <p>Als u een tijdzone kiest, wordt deze samen met de VRS opgeslagen. Als u niet kiest, wordt de tijdzone van de ouderrapportreeks gebruikt. </p> <p>Als u een VRS bewerkt, wordt de tijdzone die met de VRS is opgeslagen, weergegeven in de vervolgkeuzelijst. Als VRS werd gecreeerd alvorens de steun van de tijdzone werd toegevoegd, wordt de de tijdzone van de ouderrapportreeks getoond in de drop-down selecteur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Segmenten </td> 
   <td colname="col2"> <p>U kunt slechts één segment toevoegen of u kunt <a href="https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-build.html"  > stapelsegmenten</a>. </p> <p> <p>Opmerking:  Wanneer het stapelen van twee segmenten, worden zij aangesloten bij door EN verklaring. Dit kan niet in een OF verklaring worden veranderd. </p> </p> <p>Wanneer u probeert om een segment te schrappen of te wijzigen dat momenteel in een virtuele rapportreeks wordt gebruikt, toont een waarschuwing. </p> </td> 
  </tr> 
 </tbody> 
</table>
