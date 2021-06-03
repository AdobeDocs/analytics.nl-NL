---
title: Overzicht van classificaties
description: Pas de groepering van dimensie-items aan.
exl-id: 0d2c77ea-610f-48e0-b6a2-6e91794783b1
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# Overzicht van classificaties

Een classificatie is een manier om de veranderlijke gegevens van Analytics te categoriseren, dan tonend de gegevens op verschillende manieren wanneer u rapporten produceert.

Video-overzicht van [Analytics Classifications](https://video.tv.adobe.com/v/16853/).

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > *`<Traffic or Conversion>`*

Wanneer het classificeren, vestigt u een verband tussen de variabele en de meta-gegevens met betrekking tot die variabele. Classificaties worden het vaakst gebruikt in campagnes. Gegevens die zijn verzameld met behulp van variabelen (eVars, props en events) kunnen worden opgerold door metagegevens toe te passen op de waarden die in de variabelen zijn verzameld.

![Stapinfo](assets/sub_class_create.png)

Zodra geclassificeerd, kan om het even welk rapport dat u het gebruiken van de zeer belangrijke variabele kunt produceren ook worden geproduceerd gebruikend de bijbehorende attributen. U kunt bijvoorbeeld [!UICONTROL Product IDs] indelen met aanvullende productkenmerken, zoals productnaam, kleur, grootte, beschrijving en SKU. Het uitbreiden van rapportage- en analysegegevens met aanvullende kenmerken biedt diepere en complexere rapportagemogelijkheden.

Nadat u de classificaties hebt gemaakt, kunt u de nieuwe gegevenskenmerken in Adobe Analytics gebruiken.

## Voorbeeld van trackingcodes

Veronderstel dat in plaats van het bekijken van campagnes enkel door het volgen code, u campagneresultaten door de Motor van het Onderzoek, het Sleutelwoord, en het Kanaal van de Campagne wilt zien. In plaats van conversievariabelen voor elk van deze variabelen te wijden, kunt u drie classificaties van de campagnevariabele maken om de Motor van het Onderzoek, het Sleutelwoord, en het Kanaal van de Campagne te vertegenwoordigen. Met deze strategie kunt u de gebeurtenissen voor het succes van de site weergeven voor alle vier de variabelen, zonder extra tags.

De rapportage en de analyse omvatten vooraf bepaalde classificaties voor de volgende codevariabele, die op classificatie-gebaseerde rapporten genoemd Creative Elementen en Campagnes aanbiedt. U moet classificaties voor alle andere omzettings en verkeersvariabelen manueel vormen.

Zie [Verkeersclassificaties](/help/admin/admin/c-traffic-variables/traffic-classifications.md) en [Conversieclassificaties](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-classifications.html).

In de volgende tabel worden de verschillende typen classificaties beschreven die beschikbaar zijn, en de typen variabelen die deze ondersteunen. Controleer de informatie in [Algemene bestandsstructuur](/help/components/classifications/importer/c-saint-data-files.md) voordat u gegevensbestanden uploadt.

<table id="table_279728C28D9C40EE832ACC9F211B5F17"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>TYPE </p> </th> 
   <th colname="col2" class="entry"> <p>BESCHIKBAARHEID </p> </th> 
   <th colname="col3" class="entry"> <p>BESCHRIJVING </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> Tekst</span> </p> </td> 
   <td colname="col2"> <p>Conversie- en verkeersvariabelen </p> </td> 
   <td colname="col3"> <p>Tekstclassificaties definiëren een categorie waarmee u variabele gegevens kunt groeperen voor rapportagedoeleinden. </p> <p>Als u bijvoorbeeld overhemden verkoopt, kunt u de hemdverkopen (conversies) indelen op kleur, grootte en stijl, zodat u rapporten kunt genereren waarin de hemdverkopen worden weergegeven die door deze categorieën worden georganiseerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> Tekst met datumnotatie</span> </p> <p>Opmerking:  In 10 mei 2018, de uitgave van het Onderhoud van Analytics, begon Adobe de functionaliteit van datum-toegelaten classificaties te beperken. Deze classificatietypen zijn verwijderd uit de interfaces Admin en Classification Importer. U kunt geen nieuwe klasseringen voor datums toevoegen. Bestaande classificaties kunnen nog steeds worden beheerd (geüpload naar, verwijderd) via de standaardclassificatieworkflow en blijven beschikbaar in de rapportage. </p> </td> 
   <td colname="col2"> <p>Conversievariabelen </p> </td> 
   <td colname="col3"> <p>Met een tekstclassificatie voor datums kunt u datumbereiken toewijzen aan een tekstclassificatie. Dit wordt typisch gebruikt met campagneclassificaties zodat u uit de grafiekmening van Gantt in <span class="wintitle"> het rapport van Campagnes</span> kunt voordeel halen. </p> <p>U kunt de daadwerkelijke campagnecedata in het gegevensbestand opnemen dat de classificatiegegevens bevolkt. </p> <p>Rapporten &amp; Analytics verzamelt de codes voor het bijhouden van de campagne, zelfs als de einddatum van de campagne al voorbij is, maar de campagnegegevens die na de einddatum van de campagne worden verzameld, zijn niet gekoppeld aan de campagne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> Numeriek</span> <p>Opmerking:  In de versie Analytics Maintenance van 10 mei 2018, begon Adobe de functionaliteit van numerieke classificaties te beperken. Deze classificatietypen zijn verwijderd uit de interfaces Admin en Classification Importer. Er kunnen geen nieuwe numerieke classificaties worden toegevoegd. Bestaande classificaties kunnen nog steeds worden beheerd (geüpload naar, verwijderd) via de standaardclassificatieworkflow en blijven beschikbaar in de rapportage. </p> </p> </td> 
   <td colname="col2"> <p>Conversievariabelen </p> </td> 
   <td colname="col3"> <p>Met numerieke classificaties kunt u vaste numerieke waarden toepassen op Conversie</span>-rapporten. <span class="wintitle"> Deze classificaties worden als metriek weergegeven in rapporten. </span></p> <p>Wanneer u overweegt of u een <span class="wintitle"> Numerieke </span>-classificatie wilt toevoegen, moet de numerieke waarde vast zijn en ongewijzigd blijven. </p> </td> 
  </tr> 
 </tbody> 
</table>
