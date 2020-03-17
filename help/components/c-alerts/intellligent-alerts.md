---
description: Het nieuwe systeem voor intelligente waarschuwingen biedt meer gedetailleerde controle over waarschuwingen en integreert de detectie van anomalieën met het waarschuwingssysteem.
title: Intelligente waarschuwingen
uuid: ac8c9710-d245-46e9-b906-32d3bb0013c0
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Intelligente waarschuwingen

Het nieuwe systeem voor intelligente waarschuwingen biedt meer gedetailleerde controle over waarschuwingen en integreert de detectie van anomalieën met het waarschuwingssysteem.

## Overzicht {#section_6AC8CA81DEA94E99B0F192B60D0FDF03}

>[!IMPORTANT]
>
>Intelligente waarschuwingen zijn alleen beschikbaar voor klanten van Adobe [!DNL Analytics] Premiere en Adobe [!DNL Analytics] Ultimate.

De nieuwe Waarschuwingsbouwer en de Manager van de Waarschuwing vervangen de bestaande waakzame functionaliteit in Adobe [!DNL Analytics]. Met intelligente waarschuwingen kunt u

* Berichten opstellen op basis van anomalieën (90%, 95%, 99%, 99,75% en 99,9% drempelwaarden; % wijziging; boven/onder).
* Een voorvertoning weergeven van hoe vaak een waarschuwing wordt geactiveerd.
* Verzend alarm door e-mail of SMS met verbindingen naar auto-geproduceerde projecten van de Werkruimte van de Analyse.
* Maak &#39;gestapelde&#39; waarschuwingen die meerdere meetgegevens vastleggen in één waarschuwing.

Onderdelen van het nieuwe waarschuwingssysteem zijn: Alert Builder, Alert Manager, Alert Voorproef, en betere in-context toegang tot het creëren van alarm. De oude gebruikersinterface van het waarschuwingssysteem is niet meer beschikbaar, maar de waarschuwingen worden gemigreerd. Sommige oude waarschuwingsfuncties [zijn niet meer beschikbaar](https://marketing.adobe.com/resources/help/en_US/sc/user/deprecated_alerts.html).

Er zijn vier manieren om naar de Waarschuwingsbouwer te gaan:

* Door de volgende kortere weg in de Werkruimte van de Analyse te gebruiken:

   `ctrl (or cmd) + shift + a`
* Door rechtstreeks naar de waarschuwingsBuilder te gaan:  **[!UICONTROL Workspace]** > **[!UICONTROL Components]** > **[!UICONTROL New Alert]** .
* Door een of meer vrije regelitems voor tabellen te selecteren, klikt u met de rechtermuisknop en selecteert u deze **[!UICONTROL Create Alert from Selection]**. Hiermee wordt de waarschuwingsBuilder geopend en wordt de builder vooraf gevuld met de juiste maateenheden en filters die uit de tabel zijn toegepast. U kunt de waarschuwing vervolgens bewerken, indien nodig.

   ![](assets/create-alert-from-selection.png)

* Ga vanuit een [!UICONTROL Reports & Analytics] rapport naar **[!UICONTROL More]** > **[!UICONTROL Add Alert]** . Dit zal nieuwe Bouwer van de Waarschuwing openen en zal de bouwer met de aangewezen metriek en de filters pre-bevolken die van het rapport worden toegepast. U kunt de waarschuwing vervolgens bewerken, indien nodig.

   ![](assets/add-alert.png)

## Veelgestelde vragen: Hoe waarschuwingen worden berekend en geactiveerd {#section_1F3B1DAF21784306953B49AAD4C3DCAB}

De procentuele drempels zijn standaardafwijkingen. 95% = 2 standaardafwijkingen en 99% = 3 standaardafwijkingen. Afhankelijk van de tijdsgranulariteit die u kiest, worden [verschillende modellen](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) gebruikt om te berekenen hoe ver (hoeveel standaardafwijkingen) elk gegevenspunt van de norm is. Als u een lagere drempel instelt (bijvoorbeeld 90%), krijgt u meer anomalieën dan wanneer u een hogere drempel instelt (99%). 99,75% &amp; 99,99% drempels werden ingevoerd specifiek voor de uurgranulariteit zodat het niet zoveel anomalieën zou veroorzaken.

<table id="table_B3AA85E1DE3543DCA34966A52E3CE4AB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>V: Hoe ver gaat de anomaliedetectie van de waarschuwing om anomalieën in de gegevens vast te stellen?</b> </p> </td> 
   <td colname="col2"> <p>De duur van de training is afhankelijk van de geselecteerde korreligheid. Zie Statistische technieken die worden gebruikt in <a href="/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md">Anomaly Detection</a> voor meer informatie. Hier volgt een overzicht: </p> 
    <ul id="ul_4F8C2A41F06C498DBF5E7AE5DE803773"> 
     <li id="li_E246091A3F1E484C8444AF4052FCA784">Maandelijks = 15 maanden + zelfde marge vorig jaar </li> 
     <li id="li_CC014FB38AE1492B9647E990C29BFB3C">Wekelijks = 15 weken + zelfde marge vorig jaar </li> 
     <li id="li_2517EE2097534324BE9C1B54CD181A62">Dagelijks = 35 dagen + zelfde waaier vorig jaar </li> 
     <li id="li_710BC8B009354542AA4962A59A646099">Uur = 336 uur </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Als ik alleen op een dip in gedrag of slechts een piek in gedrag wil worden geattendeerd, kan ik de anomalie gebruiken of moet ik absolute waarde gebruiken?</b> </p> </td> 
   <td colname="col2"> <p>Het gebruiken van absolute waarde zou alarm op dips evenals pieken nog teweegbrengen. U kunt waarschuwingen niet isoleren voor alleen dips of pieken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Kan ik alarm vormen om slechts tijdens bepaalde uren van de dag (zoals kantooruren vs. niet-bedrijfsuren) teweeg te brengen? </b> </p> </td> 
   <td colname="col2"> <p>Op dit moment, nee. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Kan ik een tabel krijgen van de "verwachte waarden" die de stippellijn vormen, of een soort output van wat die waarden zijn? </b> </p> </td> 
   <td colname="col2"> <p>Niet in Werkruimte, maar u kunt in de Bouwer van het Rapport (zie deze video over <a href="https://www.youtube.com/watch?v=-a-8W6GQZnU"  > Anomaly Detection in de Bouwer van het Rapport </a>). </p> <p>Houd in mening dat de Bouwer van het Rapport minder geavanceerde anomalieopsporingsmethodes gebruikt. Het gebruikt een vaste trainingsperiode van 30 dagen, een vaste periode van 95% en is vergelijkbaar met het opsporen van anomalieën in <a href="https://marketing.adobe.com/resources/help/en_US/reference/anomaly.html"  > rapporten en analyses <span class="uicontrol"></span> </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

