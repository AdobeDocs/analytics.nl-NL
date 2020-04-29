---
description: Berekende en Geavanceerde Berekende (of Afgeleide) Metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.
keywords: Calculated Metrics;Derived Metrics;Advanced Calculated Metrics
title: Berekende en Geavanceerde berekende (Afgeleide) Metriek
uuid: 2553c115-b15a-4109-8de2-733dbc1eeb9e
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Berekende en Geavanceerde berekende (Afgeleide) Metriek

Berekende en Geavanceerde Berekende (of Afgeleide) Metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.

>[!IMPORTANT]
>
>In juli 2018 heeft Adobe [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html)geïntroduceerd, die de manier waarop toewijzingsmodellen in berekende metriek worden geëvalueerd, heeft herzien. In het kader van deze wijziging zijn berekende maatstaven die een niet-standaard toewijzingsmodel gebruiken, gemigreerd naar nieuwe, verbeterde toewijzingsmodellen:
>
>* De toewijzingsmodellen &quot;Marketing Channel Last Touch&quot; en &quot;Marketing Channel First Touch&quot; zijn gemigreerd naar de nieuwe toewijzingsmodellen &quot;Last Touch&quot; en &quot;First Touch&quot; (Opmerking: De &quot;Kanalen van de Marketing&quot;is niet afgekeurd - slechts de twee toewijzingsmodellen die in berekende metriek verschijnen zijn geweest).
>* Bovendien hebben we de manier gecorrigeerd waarop de lineaire toewijzing wordt berekend. Voor klanten die berekende metriek met &quot;Lineaire&quot;toewijzingsmodellen gebruiken, kunnen de rapporten lichtjes veranderen om het nieuwe, gecorrigeerde attributiemodel te weerspiegelen. Deze verandering in berekende metriek wordt weerspiegeld in [!UICONTROL Analysis Workspace], [!UICONTROL Reports & Analytics], de Rapporterende API, de Bouwer van het Rapport, en Ad hoc Analyse. Zie [Hoe lineaire toewijzing werkt per 19 juli 2018 voor meer informatie](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_EDBB2E14A6C248C5A79C0913C02D7CA1).


Met onze gereedschappen voor berekende meetwaarden kunt u op zeer flexibele wijze metriek bouwen, beheren en beheren. Met deze services kunt u als marketers, productmanagers en analisten vragen stellen over de gegevens zonder dat u uw [!DNL Analytics] implementatie hoeft te wijzigen. De beschikbare aangepaste meetgegevens in elk [!DNL Analytics] pakket zijn:

* Adobe [!DNL Analytics] Foundation: Berekend
* [Selecteer](https://www.adobe.com/data-analytics-cloud/analytics/select.html)Adobe Analytics: Berekend + Geavanceerd berekend
* [Primaire](https://www.adobe.com/data-analytics-cloud/analytics/prime.html)Adobe Analytics: Berekend + Geavanceerd berekend
* [Adobe Analytics Ultimate](https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html): Berekend + Geavanceerd berekend

Hier volgt een vergelijking van de mogelijkheden Berekende meetwaarden en Geavanceerde berekende meetwaarden:

| Builder-opties | Berekende statistieken | Geavanceerde berekende (Afgeleide) Metriek |
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

* Maak metriek voor [!UICONTROL Analysis Workspace], [!UICONTROL Reports & Analytics], [!UICONTROL Ad Hoc Analysis], [!UICONTROL Report Builder], [!UICONTROL Anomaly Detection]en [!UICONTROL Contribution Analysis].
* Creeer gesegmenteerde metriek die bij rapportruntime worden afgeleid, [zonder het moeten de implementatie](https://youtu.be/CuQTm9RaUpY)veranderen. Deze kunnen historisch worden bekeken omdat ze zijn gebaseerd op segmenten.
* De metriek van het aandeel over rapportsuites. Dit betekent dat alle pas gecreëerde metriek op alle rapportsuites in het zelfde login bedrijf van toepassing is.
* (Alleen Geavanceerde berekende cijfers) Segment op maateenheden. U kunt bijvoorbeeld een metrische waarde maken voor &quot;Nieuwe bezoekers&quot;, met een aantal personen voor wie dit de eerste sessie is.
* (Alleen geavanceerde berekende statistieken) Neem statistische functies op om uw gegevens beter te kunnen beschrijven. Bijvoorbeeld, kunt u het aantal punten in een rapport tellen of in het aantal standaardafwijkingen voor elk punt toevoegen.
* Gebruik metriek die in [!UICONTROL Ad Hoc Analysis] de andere [!DNL Analytics] hulpmiddelen worden gecreeerd en vice versa.

   >[!NOTE]
   >
   >U kunt metriek in Ad hoc Analyse blijven creëren. Zijn berekende metrische bouwergebruikersinterface is nu gelijkaardig aan de nieuwe metrische bouwer.

## Beperkingen {#section_CB878B02451541D68A68B508D4DBD19A}

Met sommige [!DNL Analytics] functies kunt u wel gebeurtenissen gebruiken, maar geen berekende meetwaarden:

* [!UICONTROL Funnels] in [!UICONTROL Reports & Analytics]
* [!UICONTROL Fallout] in [!UICONTROL Analysis Workspace]
* [!UICONTROL Cohort Analysis] in analysewerkruimte
* [!UICONTROL Data Warehouse]
* [!UICONTROL Segments]
* [!UICONTROL Real-Time] rapporten
* [!UICONTROL Current Data] rapporten
* [!DNL Analytics] for [!DNL Target]

## Gereedschappen {#section_D65E9C067E9C45E1A50DD30F50561BB2}

Hier volgt een kort overzicht van de [!UICONTROL Calculated Metrics] gereedschappen:

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
   <td colname="col1"><a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md"  > Berekend metrisch beheer</a> </td> 
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
   <td colname="col2"> <p>Hiermee vervangt u het pop-upvenster Metriek <span class="uicontrol"> tonen in</span> Rapporten en Analyse <span class="uicontrol"></span>. </p> <p>Het laat u naar het rapport zoeken en metriek toevoegen/toepassen. U kunt ook de <a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-finding.md"  > sorteervolgorde</a> wijzigen (opties zijn: alfabetisch, aanbevolen, vaak gebruikt, onlangs gebruikt.) Bovendien kunt u op de Reeksen van het Rapport filtreren om slechts metriek te tonen die in een specifieke rapportreeks wordt gecreeerd. </p> <p>Klik op het pictogram Metrisch links van een rapport om deze metrische kiezer te openen. <img placement="inline"  src="assets/metrics_icon.png" width="30px" id="image_2C6F20B4E634486B95BACD4CA47EF991" /> Zo ziet de metrische kiezer eruit: </p> <p><img src="assets/metrics_rail.png" width="200px" id="image_379523E9AFEC4CF08D20C42C740AA358" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/README.md"  > API voor berekende cijfers</a> </td> 
   <td colname="col2"> <p>Deel van de Adobe Analytics 2.0 API-set. </p> </td> 
  </tr> 
 </tbody> 
</table>

