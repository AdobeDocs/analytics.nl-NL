---
description: Toont gemiddeld hoe ver binnen een bezoek elke waarde in brand werd gestoken. Deze metrische waarde is nuttig om te bepalen hoe ver binnen een bezoek uw publiek een bepaalde pagina of pro-waarde bereikt. De gemiddelde Diepte van de Pagina is beschikbaar op om het even welke variabele met toegelaten kleven.
title: Gemiddelde diepte pagina
topic: Metrics
uuid: 4d8a3a3c-c698-4210-8dd8-a02a1638483c
translation-type: tm+mt
source-git-commit: ''

---


# Gemiddelde diepte pagina

Toont gemiddeld hoe ver binnen een bezoek elke waarde in brand werd gestoken. Deze metrische waarde is nuttig om te bepalen hoe ver binnen een bezoek uw publiek een bepaalde pagina of pro-waarde bereikt. De gemiddelde Diepte van de Pagina is beschikbaar op om het even welke variabele met toegelaten kleven.

Als een bezoek bijvoorbeeld het volgende pad bevat: Pagina A > Pagina B > Pagina C > Pagina D > Pagina E > Pagina F, de diepte is een index van de positie van de pagina. &quot;Pagina A&quot; heeft bijvoorbeeld een diepte van 0 en &quot;Pagina F&quot;. heeft een diepte van vijf. Het gemiddelde is gebaseerd op een combinatie van alle bezoeken. Een paginadiepte met een waarde van minder dan één (bijvoorbeeld 0,9) is de gemiddelde waarde van alle pagina&#39;s die vóór de desbetreffende pagina zijn bezocht.

[!UICONTROL Page Depth] helpt u te begrijpen waar een bepaalde pagina typisch in een gebruikerspad valt, ongeacht vorige of volgende pagina&#39;s in dit pad. Hierdoor krijgt u meer inzicht in de manier waarop de pagina past in het totaalbeeld van de gebruikerservaring op uw site. Dit inzicht kan het best worden gezien in een [!UICONTROL Pages] verslag.

<table id="table_E92B185A487C40E28C70EA30EDF73A40"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Gebruiksmiddelen </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Verkeer </td> 
   <td colname="col2"> <p>De berekening van pagina-gebeurtenissen en weergegeven pagina's gedeeld door bezoeken, waarbij het gemiddelde aantal klikken op een pagina wordt weergegeven. Houd rekening met hetzelfde pad voor bezoeken: </p> <p>A &gt; B &gt; B &gt; C &gt; D &gt; B </p> <p>Het klikaantal wordt berekend voor elke pagina en paginagebeurtenis, met inbegrip van herlaadt wanneer de optie van de Instanties van de Herhaling van de Telling wordt toegelaten (dit is door gebrek in Ad hoc analyse, en altijd in de Rapporten van de Marketing en Analyse). Tijdens dit bezoek ontvangt pagina A het kliknummer 0. Voor pagina B zijn de kliknummers 1, 2 en 5. De berekening voor het gemiddelde zou [(1+2+5) / 3] zijn voor een gemiddelde paginadiepte van 2,67 voor pagina B. </p> <p>Als de optie "Aantal herhalingsinstanties" is uitgeschakeld, ontvangt pagina B de waarden 1 en 4. De tweede wordt niet geteld. De berekening zou [(1+4) / 2 = 2,5] zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Conversie </td> 
   <td colname="col2"> N.v.t. </td> 
  </tr> 
 </tbody> 
</table>

>[!MORELIKETHIS]
>
>* [Rapport Paginadiepte](/help/components/c-variables/dimensionslist/reports-page-depth.md)

