---
description: Berekende en Geavanceerde Berekende (of Afgeleide) Metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.
keywords: Berekende metriek;Afgeleide Metriek;Geavanceerde Berekende Metriek
title: Berekende en Geavanceerde berekende (Afgeleide) Metriek
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 1dc0325f1a8b4fc1888895ee18570effb34e6208
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 6%

---

# Berekende en Geavanceerde berekende (Afgeleide) metriek

Berekende en Geavanceerde berekende (of Afgeleide) metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.

Met onze gereedschappen voor berekende meetwaarden kunt u op zeer flexibele wijze metriek bouwen, beheren en beheren. Met deze services kunt u als marketers, productmanagers en analisten vragen stellen over de gegevens zonder dat u uw [!DNL Analytics] uitvoering. De aangepaste maatstaven die beschikbaar zijn in elke [!DNL Analytics] pakket is:

* Adobe [!DNL Analytics] Stichting: Berekend
* [Adobe Analytics selecteren](https://www.adobe.com/nl/data-analytics-cloud/analytics/select.html): Berekend + Geavanceerd berekend
* [Adobe Analytics Prime](https://www.adobe.com/nl/data-analytics-cloud/analytics/prime.html): Berekend + Geavanceerd berekend
* [Adobe Analytics Ultimate](https://www.adobe.com/nl/data-analytics-cloud/analytics/ultimate.html): Berekend + Geavanceerd berekend

Hier is een vergelijking van Berekende metriek en Geavanceerde Berekende metriekmogelijkheden:

| Builder-opties | Berekende standaarden | Geavanceerde berekende (Afgeleide) metriek |
|---|---|---|
| [Indelingstypen (decimaal, tijd, percentage, valuta)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) | Ja | Ja |
| [Wijzigingen in het kenmerk (standaard, lineair, deelname, enz.)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | Ja | Ja |
| [Metrische typen (standaard, totaal)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | Ja | Ja |
| Basisoperatoren (toevoegen, verwijderen, vermenigvuldigen, verdelen) | Ja | Ja |
| [Segmenten toepassen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md) | Nee | Ja |
| [Basisfuncties (aantal, abs-waarde, gemiddelde, enz.)](/help/components/c-calcmetrics/cm-reference/cm-functions.md) | Nee | Ja |
| [Geavanceerde functies (regressie, indien/toen, t-score, enz.)](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md) | Nee | Ja |

## Mogelijkheden {#section_A0A5C275B68A4D628950BBB0B1EE631F}

U kunt

* Metrisch maken over [!UICONTROL Analysis Workspace], [!UICONTROL Reports & Analytics], [!UICONTROL Report Builder], [!UICONTROL Anomaly Detection], en [!UICONTROL Contribution Analysis].
* Creeer gesegmenteerde metriek die bij rapportruntime worden afgeleid, zonder het moeten de implementatie veranderen. Deze kunnen historisch worden bekeken omdat ze zijn gebaseerd op segmenten.

  >[!VIDEO](https://video.tv.adobe.com/v/25407/?quality=12&learn=on)

* De metriek van het aandeel over rapportsuites. Dit betekent dat alle pas gecreëerde metriek op alle rapportsuites in het zelfde login bedrijf van toepassing is.
* (Alleen geavanceerde berekende metriek) Segment op metriek. U kunt bijvoorbeeld een metrische waarde maken voor &quot;Nieuwe bezoekers&quot;, met een aantal personen voor wie dit de eerste sessie is.

* (Alleen geavanceerde berekende gegevens) Neem statistische functies op om uw gegevens beter te kunnen beschrijven. Bijvoorbeeld, kunt u het aantal punten in een rapport tellen of in het aantal standaardafwijkingen voor elk punt toevoegen.

  >[!VIDEO](https://video.tv.adobe.com/v/25409/?quality=12&learn=on)

## Beperkingen {#section_CB878B02451541D68A68B508D4DBD19A}

Sommige [!DNL Analytics] Met functies kunt u wel gebeurtenissen gebruiken, maar niet berekende meetwaarden:

* [!UICONTROL Funnels] in [!UICONTROL Reports & Analytics]
* [!UICONTROL Fallout] in [!UICONTROL Analysis Workspace]
* [!UICONTROL Cohort Analysis] in Analysis Workspace
* [!UICONTROL Data Warehouse]
* [!UICONTROL Segments]
* [!UICONTROL Real-Time] rapporten
* [!UICONTROL Current Data] rapporten
* [!DNL Analytics] for [!DNL Target]

## Tools {#section_D65E9C067E9C45E1A50DD30F50561BB2}

Hier volgt een kort overzicht van het [!UICONTROL Calculated metrics] gereedschappen:

<table id="table_520AFE97DB514958ABE23FD3C9CE0ABD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Gereedschap </th> 
   <th colname="col2" class="entry"> Mogelijkheden </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md"  > Berekende metrische bouwer</a> </td> 
   <td colname="col2"> 
    <ul id="ul_E6F02AB9DF204C2F9A0AC92A31594B3E"> 
     <li id="li_A4A6E716374243A190C539A3F4A41C0C">Creeer berekende en geavanceerde berekende metriek gebruikend geavanceerde toewijzingsmodellen. </li> 
     <li id="li_C8C97BA4E227463E98077ABA5818FFC6">Voeg segmenten inline toe aan metrische formules. </li> 
     <li id="li_8503D9E06A3C46569B5CDB4B90F72446">Vergelijk segmenten in het zelfde rapport. Vergelijk bijvoorbeeld lokale bezoekers met internationale bezoekers. </li> 
     <li id="li_4B528FDE1F96400DBA0D3276408FF919">Gebruik statistische functies. </li> 
     <li id="li_C1162B1EA6784B8189A8A87E2B0DA79A">Geef gedetailleerde metrische beschrijvingen op (toon wat het doet, waar het wordt gebruikt, waar het NIET wordt gebruikt). </li> 
     <li id="li_DEA13F5E8BF94AF1B311C467FE6E2A74">Kopieer definities naar nieuwe metriek. </li> 
     <li id="li_8C21F55015D44910904202D2BF74221C">Een inline metrische voorvertoning weergeven. </li> 
     <li id="li_3704F66C321C477F9D4F52E068C231BD">Metrische polariteit instellen die aangeeft of het goed of slecht is als een bepaalde aangepaste gebeurtenis (metrisch) wordt verhoogd. </li> 
     <li id="li_9D45319FA965476FB1C90DE8AA72BBD7">Metrische codes. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md"  > Berekende standaard-beheer</a> </td> 
   <td colname="col2"> 
    <ul id="ul_E4D20D5DD3904CC6A85785B5BD4C1B1E"> 
     <li id="li_E0B216BA1478406EB6212263DF71D85B">Deel metriek met anderen. </li> 
     <li id="li_96EB16FAF3454211AAEF78EA5B08927F">Metriek goedkeuren en krullen. </li> 
     <li id="li_3ADBD2428EAC4B0AA61222D87C3AF2B7">Organiseer uw gegevens (tag) zodat mensen ze kunnen vinden. </li> 
     <li id="li_726F3C3390744E49BA63606FE196880E">Metrische gegevens verwijderen. </li> 
     <li id="li_F306BA4FA8AF4A6E987BA62634659A2F">Naam metriek wijzigen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrische kiezer </td> 
   <td colname="col2"> <p>Vervangt de <span class="uicontrol"> Metrisch tonen</span> popup in <span class="uicontrol"> Rapporten en analyses</span>. </p> <p>Het laat u naar het rapport zoeken en metriek toevoegen/toepassen. U kunt ook de <a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-finding.md"  > sorteren</a> volgorde (opties zijn: alfabetisch, aanbevolen, vaak gebruikt, onlangs gebruikt.) Bovendien kunt u op de Reeksen van het Rapport filtreren om slechts metriek te tonen die in een specifieke rapportreeks wordt gecreeerd. </p> <p>Klik op het pictogram Metriek voor toegang tot deze metrische kiezer <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg" width="15px" id="image_2C6F20B4E634486B95BACD4CA47EF991" /> links van een rapport. Zo ziet de metrische kiezer eruit: </p> <p><img src="assets/metrics_rail.png" width="200px" id="image_379523E9AFEC4CF08D20C42C740AA358" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/README.md"  > API voor berekende cijfers</a> </td> 
   <td colname="col2"> <p>Deel van de Adobe Analytics 2.0 API-set. </p> </td> 
  </tr> 
 </tbody> 
</table>
