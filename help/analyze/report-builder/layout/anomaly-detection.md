---
description: De opsporing van het anomaly gebruikt statistische modellering om onverwachte tendensen in uw gegevens automatisch te vinden. Het model analyseert metriek en bepaalt een ondergrens, bovengrens, en verwachte waaier van waarden. Wanneer een onverwachte punt of daling voorkomt, alarmeert het systeem u in het rapport.
title: Anomaly Detection
topic: Report builder
uuid: 02da21b4-3394-471b-97b5-aa1bddf1f445
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Anomaly Detection{#anomaly-detection}

De opsporing van het anomaly gebruikt statistische modellering om onverwachte tendensen in uw gegevens automatisch te vinden. Het model analyseert metriek en bepaalt een ondergrens, bovengrens, en verwachte waaier van waarden. Wanneer een onverwachte punt of daling voorkomt, alarmeert het systeem u in het rapport.

Voorbeelden van anomalieën die u kunt onderzoeken zijn:

* Drastische afname in gemiddelde orderwaarde
* Pieken in orders met lage inkomsten
* Spikes of druppels in proefregistraties
* Druppels in weergaven van openingspagina&#39;s
* Spaties in videobuffergebeurtenissen
* Spikes in lage videobitsnelheden

>[!NOTE] Anomaly-detectie is alleen beschikbaar wanneer u de granulariteit Dag selecteert.

<p class="head"> <b>Metrische gegevens voor anomalge detectie</b> </p>

Bij Anomalige detectie worden nieuwe metrische waarden toegevoegd voor elke metrische waarde die u selecteert, waaronder:

<table id="table_BF75FC874634498DB6632C12CBD8D533"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Ondergrens </td> 
   <td colname="col2"> <p>Lager niveau van het voorspelde interval. Waarden onder dit niveau worden als abnormaal beschouwd. </p> <p>Vertegenwoordigt een 95% vertrouwen dat de waarden boven dit niveau zullen zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verwacht </td> 
   <td colname="col2"> <p>De voorspelde waarde op basis van de gegevensanalyse. Deze waarde is ook het middelpunt tussen de boven- en ondergrens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bovenste binding </td> 
   <td colname="col2"> <p>Bovenste niveau van het voorspellingsinterval. Waarden boven dit niveau worden als abnormaal beschouwd. </p> <p>Vertegenwoordigt een 95% vertrouwen dat de waarden onder dit niveau zullen zijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

De bouwer van het rapport past deze waarden op geselecteerde metriek toe. Als u bijvoorbeeld een metrische weergave van paginaweergaven selecteert en afwijkende detectie toepast, wordt een *`Page Views Lower Bound`* metrische waarde gebruikt.

**Hoe Anomaly Detection wordt berekend**

Bij anomaliedetectie wordt een trainingsperiode gebruikt om gegevens over het voorspellingsinterval per dag te berekenen, te leren en te rapporteren. De opleidingsperiode is de historische periode waarin wordt vastgesteld wat normaal is ten opzichte van anomalieën, en past wat wordt geleerd toe op de verslagperiode. In marketingrapporten zijn er trainingsperiodes van 30, 60 en 90 beschikbaar. In rapportbuilder zijn 30 dagen beschikbaar.

De opleidingsperiode hoeft niet hetzelfde te zijn als de geselecteerde rapportageperiode. Een rapportgrafiek geeft de datumbereikperiode weer die u in de kalender hebt opgegeven.

Om de gegevens te berekenen wordt het dagelijkse totaal voor elke metrische waarde vergeleken met de trainingsperiode met elk van de volgende algoritmen:

* Holt Winters Multiplicative (Drievoudige Exponential Smoothing)
* Holt Winters Additive (Triple Exponential Smoothing)
* Houts Trend Corrected (Double Exponential Smoothing)

Elk algoritme wordt toegepast om het algoritme met de kleinste Som van Vierkante Fouten (SSE) te bepalen. De gemiddelde Absolute Percent Error (MAPE) en de huidige Standaardfout worden vervolgens berekend om ervoor te zorgen dat het model statistisch geldig is.

Deze algoritmen kunnen worden uitgebreid om voorspellingen van metriek in toekomstige periodes te verstrekken.

Omdat de trainingsperiode afhankelijk is van het begin van de rapportageperiode, kunnen er verschillen optreden in de gegevens die op dezelfde datum worden gerapporteerd als onderdeel van twee verschillende tijdsperiodes.

Bijvoorbeeld, als u een rapport voor 1-14 Januari in werking stelt, en dan een rapport voor 7-21 Januari in werking stelt, zou u verschillende voorspellingsgegevens voor zelfde metrisch tussen 7-14 Januari in de twee verschillende rapporten kunnen zien. Dit is het gevolg van het verschil in opleidingsperioden.

| Rapportbereik | Opleidingsperiode |
|--- |--- |
| 1-14 januari | 27 november - 31 december |
| 7-21 januari | 4 december - 6 januari |
