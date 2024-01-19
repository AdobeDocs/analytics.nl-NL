---
description: Het systeem van de Intelligente Alarm staat voor meer korrelige controle over alarm toe en integreert anomalieopsporing met het waakzame systeem.
title: Intelligente waarschuwingen
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: a979fc8787fa96f8fa8317996ac66341a6f54354
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 6%

---

# Intelligente waarschuwingen

Het systeem van de Intelligente Alarm staat voor meer korrelige controle over alarm toe en integreert anomalieopsporing met het waakzame systeem.

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/25446/?quality=12)

## Overzicht {#section_6AC8CA81DEA94E99B0F192B60D0FDF03}

>[!IMPORTANT]
>
>Intelligente waarschuwingen zijn beschikbaar voor Adobe [!DNL Analytics] Eerste en Adobe [!DNL Analytics] Alleen ultieme klanten.

Met intelligente waarschuwingen kunt u

* Berichten opbouwen op basis van anomalieën (90%, 95%, 99%, 99,75% en 99,9% drempelwaarden; procentuele verandering; boven/onder).
* Een voorvertoning bekijken van het aantal keren dat een melding is geactiveerd.
* Een melding sturen via e-mail of sms, met koppelingen naar automatisch gegenereerde Analysis Workspace-projecten.
* &#39;Gestapelde&#39; meldingen maken waarbij meerdere metrics zijn opgenomen in één waarschuwing.

De componenten van het waakzame systeem omvatten: De Bouwer van de alarm, Manager van de Alarm, Voorproef van de Alarm, en betere in-context toegang tot het creëren van alarm. De oude gebruikersinterface van het waarschuwingssysteem is niet meer beschikbaar, maar de waarschuwingen worden gemigreerd. Enkele oude waarschuwingsfuncties [zijn niet meer beschikbaar](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/alerts.html).

Er zijn drie manieren om naar de Waarschuwingsbouwer te gaan:

* Met de volgende sneltoets in Analysis Workspace:

  `ctrl (or cmd) + shift + a`
* Door rechtstreeks naar de waarschuwingsBuilder te gaan:  **[!UICONTROL Workspace]** > **[!UICONTROL Components]** > **[!UICONTROL New Alert]** .
* Door een of meer vrije regelitems voor tabellen te selecteren, klikt u met de rechtermuisknop en selecteert u **[!UICONTROL Create Alert from Selection]**. Hiermee wordt de waarschuwingsBuilder geopend en wordt de builder vooraf gevuld met de juiste maateenheden en filters die uit de tabel zijn toegepast. U kunt de waarschuwing vervolgens bewerken, indien nodig.

  ![](assets/create-alert-from-selection.png)


## Veelgestelde vragen: Hoe waarschuwingen worden berekend en geactiveerd {#trigger}

De procentuele drempels zijn standaardafwijkingen. 95% = 2 standaardafwijkingen en 99% = 3 standaardafwijkingen. Afhankelijk van de tijdsgranulariteit die u kiest, [verschillende modellen](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) worden gebruikt om te berekenen hoe ver weg (hoeveel standaardafwijkingen) elk gegevenspunt van de norm is. Als u een lagere drempel instelt (bijvoorbeeld 90%), krijgt u meer anomalieën dan wanneer u een hogere drempel instelt (99%). 99,75% &amp; 99,99% drempels werden ingevoerd specifiek voor de uurgranulariteit zodat het niet zoveel anomalieën zou veroorzaken.

<table id="table_B3AA85E1DE3543DCA34966A52E3CE4AB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Q: Hoe ver gaat de anomalieopsporing van de alarm om gegevensanomalieën te bepalen?</b> </p> </td> 
   <td colname="col2"> <p>De trainingsperiode is afhankelijk van de geselecteerde korreligheid. Zie Statistische technieken gebruikt in <a href="/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md">Anomaly Detection</a> voor meer details. Hier volgt een overzicht: </p> 
    <ul id="ul_4F8C2A41F06C498DBF5E7AE5DE803773"> 
     <li id="li_E246091A3F1E484C8444AF4052FCA784">Maandelijks = 15 maanden + zelfde marge vorig jaar </li> 
     <li id="li_CC014FB38AE1492B9647E990C29BFB3C">Wekelijks = 15 weken + zelfde marge vorig jaar </li> 
     <li id="li_2517EE2097534324BE9C1B54CD181A62">Dagelijks = 35 dagen + zelfde waaier vorig jaar </li> 
     <li id="li_710BC8B009354542AA4962A59A646099">Uur = 336 uur </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Als ik slechts aan een dip in gedrag of slechts een piek in gedrag wil worden gealarmeerd, kan ik de anomalieeigenschap gebruiken of moet ik absolute waarde gebruiken?</b> </p> </td> 
   <td colname="col2"> <p>Het gebruiken van absolute waarde zou alarm op dips evenals pieken nog teweegbrengen. U kunt waarschuwingen niet isoleren voor alleen dips of alleen pieken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Kan ik alarm vormen om slechts tijdens bepaalde uren van de dag (zoals kantooruren vs. niet-bedrijfsuren) teweeg te brengen? </b> </p> </td> 
   <td colname="col2"> <p>Op dit moment, nee. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Kan ik een lijst krijgen van de "verwachte waarden"die uit de stippellijn bestaan, of één of andere soort output van wat die waarden zijn? </b> </p> </td> 
   <td colname="col2"> <p>Niet in Workspace, maar in Report Builder (zie deze video op <a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/exporting/report-builder/anomaly-detection-in-report-builder.html"  > Anomaly Detection in Report Builder </a>). </p> <p>Houd er rekening mee dat Report Builder minder geavanceerde afwijkingsdetectiemethoden gebruikt. Het gebruikt een vaste opleidingsperiode van 30 dagen, vaste 95% interval. </p> </td> 
  </tr> 
 </tbody> 
</table>
