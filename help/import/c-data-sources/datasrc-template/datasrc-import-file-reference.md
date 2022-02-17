---
description: Informatie over het malplaatje van de Gegevensbron .txt.
subtopic: Data sources
title: Referentie van bestand importeren
topic-fix: Developer and implementation
feature: Data Sources
exl-id: 7966b156-04bf-4d39-a720-ab47a665d1e2
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 2%

---

# Referentie van bestand importeren

Informatie over het malplaatje van de Gegevensbron .txt.

Gebruik de Tovenaar van Gegevensbronnen om een het invoeren malplaatje te produceren. Het de invoerdossier van Gegevensbronnen omvat de volgende gegevens:

* Een hekje (#) geeft die rij aan als een opmerking.
* Desgewenst kunt u aanvullende opmerkingen aan het bestand toevoegen.
* Een opmerking die de titel van het sjabloonbestand weergeeft.
* Een opmerking die de namen opsomt van de externe metrische waarden en gegevensdimensies die zijn opgegeven in het dialoogvenster [!UICONTROL Data Source Activation Wizard].

Kolomkoppen worden gebruikt om de gegevens in elke kolom van het gegevensbronbestand te identificeren. Er zijn drie typen kolomkoppen:

**Datum**: (Vereist) Een tijdstempel voor elke gegevensrij in het bestand, in de notatie `m/d/yyyy`.

**Variabelen**: De namen van de rapportagevariabelen die zijn toegewezen aan de gegevensafmetingen van de gegevensbron.

**Gebeurtenissen**: De namen van de gebeurtenissen die zijn toegewezen aan de gegevens van de gegevensbron.

Gebruik het malplaatje van de Gegevensbron om een Gegevensbrondossier tot stand te brengen dat gegevens bevat die u wilt uploaden. Houd rekening met het volgende wanneer u een gegevensbronbestand maakt:

* In feite bevat elke rij in het gegevensbronbestand één gegevensrecord, waarin elke record bestaat uit een reeks tabgescheiden velden. De kolomkoppen in de gegevensbronsjabloon bepalen de volgorde van deze velden. Bijvoorbeeld:

   ```
     #Sample data file for mycorp_report_suite 
     #Imported data for ad impressions applied to Event 6
     Date     Tracking Code      Event 6 
     1/1/2009     NYT8453A      8754
     1/1/2009     WSJ4453B      9492
     1/1/2009     BHG44563      10553
     1/2/2009     NYT8453A      6452
     1/2/2009     WSJ4453B      7237
     1/2/2009     BHG44563      9031
   ```

* Als u veelvoudige gegevensdossiers uploadt, laden de Gegevensbronnen hen in alfabetische orde. Bestanden die chronologisch moeten worden verwerkt, moeten een zodanige naam krijgen dat hun alfabetische volgorde overeenkomt met hun chronologische volgorde. Bijvoorbeeld:

   ```
   log_2009-01-01_13:00.txt
   log_2009-01-01_13:15.txt
   log_2009-01-01_13:30.txt
   ```

* Om de verwerking van uw Gegevensbrondossier te versnellen, adviseert Adobe samenvoegend gebeurtenis (metrische) gegevens in één enkele rij per datum.

   Als uw gegevensbronbestand bijvoorbeeld een hyperlink en een afbeelding naar gebeurtenis 6 bevat, maakt u één gegevensrij die het totale aantal indrukken en indrukken voor elke dag bevat. U hoeft dus geen gegevensrijitem te maken voor elke advertentie die op een bepaalde dag is opgetreden.
* Als u gegevens moet uploaden vanaf datums vóór de aanmaakdatum van de rapportsuite, neemt u contact op met uw accountmanager om de oudste datum te wijzigen waarvoor u rapporten kunt uitvoeren.

**.FIN-bestand**

Wanneer u klaar bent met het invullen van het gegevensbronbestand, kunt u het naar Analytics FTP. Er is echter een extra bestand nodig om uw gegevens te kunnen verwerken. U moet een leeg tekstbestand met dezelfde naam als het gegevensbestand uploaden, maar met een [!DNL .fin] extensie.

Als u bijvoorbeeld een gegevensbestand (met tabs als scheidingsteken) uploadt, genaamd [!DNL myproductdata.txt], moet u ook een leeg tekstbestand uploaden met de naam [!DNL myproductdata.fin]. Zonder de [!DNL .fin] bestand, gegevens worden nooit verwerkt.
