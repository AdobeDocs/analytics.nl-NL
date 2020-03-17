---
description: Beschikbaar in de Werkruimte van de Analyse en de Bouwer van het Segment.
title: Bezoekers met Experience Cloud ID
uuid: 47ebd3d6-a921-4e51-ac7a-b8d5fb9565e0
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Bezoekers met Experience Cloud ID

Beschikbaar in de Werkruimte van de Analyse en de Bouwer van het Segment.

Hier wordt het aantal bezoekers met een Experience Cloud-id weergegeven. U kunt zien welke pagina&#39;s de Identity Service hebben geïmplementeerd en u kunt begrijpen hoeveel bezoekers u kunt delen met andere Experience Cloud-oplossingen. U kunt deze metrische waarde ook gebruiken in segmenten die worden gedeeld met de Experience Cloud.

>[!IMPORTANT]
>
>Voor dit metrisch om te verschijnen, moet u de Dienst [hebben van de](https://marketing.adobe.com/resources/help/en_US/mcvid/) Identiteit die voor de rapportreeks loopt.

## Fouten opsporen in de installatie van uw Experience Cloud ID {#section_679E62142A3E46548FF8FBDA46568005}

De [!UICONTROL Visitors with Experience Cloud ID] metrische waarde is nuttig metrisch in de Analytics van Adobe bedoeld om u te helpen uw [!UICONTROL Identity Service]opstelling vinden en zuiveren. Metrisch is een telling van het aantal bezoekers in een rapportreeks die een identiteitskaart van de Wolk van de Ervaring van de Dienst van de Identiteit is toegewezen. Deze maatstaf kan zeer nuttig zijn bij het vaststellen waarom bepaalde Experience Cloud-integraties mogelijk niet zoveel bezoekers delen als verwacht, of bij het identificeren van gebieden van uw site die mogelijk nog geen MCID hebben geïmplementeerd.

Om bezoekers met metrische identiteitskaart van de Wolk van de Ervaring te gebruiken, sleep het eenvoudig binnen aan om het even welk rapport zoals dit [!UICONTROL Pages] rapport:

![](assets/metric-mcvid1.png)

In dit voorbeeld heeft elke pagina hetzelfde aantal Unieke bezoekers als bezoekers met een Experience Cloud-id. Het totale aantal unieke bezoekers is echter groter dan het totale aantal bezoekers met Experience Cloud ID. Als u de pagina&#39;s wilt zoeken die de MCID niet voor alle bezoekers instellen, [maakt u een berekende metrische waarde](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/cm_build_metrics.html) met deze definitie:

![](assets/metric-mcvid2.png)

Door berekende metrisch aan het rapport toe te voegen, kunt u het rapport van Pagina&#39;s sorteren zodat de pagina&#39;s met het hoogste aantal bezoekers zonder MCID worden bedekt:

![](assets/metric-mcvid3.png)

Nu kunt u snel zien dat de pagina&#39;s &quot;Productoverzicht&quot; niet correct zijn geïmplementeerd met de identiteitsservice en zo snel mogelijk moeten worden bijgewerkt. Een gelijkaardig rapport kan rond om het even welk type van afmeting zoals browser type, plaatssectie, of inhoudstypes worden geconstrueerd.

Nadat u pagina&#39;s hebt geïdentificeerd die bezoekers zonder MCID hebben, zou u dat naar uw implementatieteam moeten kunnen terugnemen zodat zij die pagina&#39;s kunnen herstellen.

In sommige gevallen zult u merken dat een klein aantal MCID&#39;s niet is ingesteld voor sommige bezoekers, ook al is de MCID-service op de pagina geïmplementeerd. In die gevallen is dit zeer waarschijnlijk toe te schrijven aan een veelvoorkomende verkeerde configuratie van de configuratie Analytics JavaScript of DTM waarin de functie AppMeasurement wordt aangeroepen voordat een rapportsuite wordt aangeboden. Om dit te vermijden, zorg ervoor u kernAppMeasurement code [correct](https://marketing.adobe.com/resources/help/en_US/sc/implement/dtm/t_appmeasurement-code.html) opneemt.

Houd er rekening mee dat segmenten die zijn gebaseerd op de pagina &quot;Productieresoluties&quot; (zoals hierboven is weergegeven) die u deelt met de Experience Cloud waarschijnlijk een zeer lage match-rate hebben met andere Experience Cloud-oplossingen. Om de dekking MCID voor om het even welk segment te controleren, kunt u een rapport als dit construeren:

![](assets/metric-mcvid4.png)

In deze tabel, waarin het aantal unieke bezoekers voor de bezoekers met een Experience Cloud-id wordt vergeleken, is het gemakkelijk te zien dat &quot;Segment 1&quot; geen 100% MCID-dekking heeft, terwijl &quot;Segment 2&quot; dat wel doet. Dit betekent dat als ik Segment 1 zou delen met de Experience Cloud, slechts 2.186 van de in totaal 3.859 bezoekers in aanmerking zouden komen voor delen.
