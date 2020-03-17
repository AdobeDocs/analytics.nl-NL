---
description: 'null'
subtopic: Alerts
title: Waarschuwingen
topic: Reports and analytics
uuid: e1333a9b-eba0-45b7-b7e6-46e06190db64
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Waarschuwingen

## Waarschuwingen {#concept_8AB25AF6FB52478DB98C1BA4577A2E16}

Met Intelligente waarschuwingen kunt u, als het nieuwe waarschuwingssysteem voor alle Adobe Analytics-componenten, waarschuwingen maken en beheren, compleet met een voorvertoning van waarschuwingen en een bijdrage van de regel. U kunt

* Berichten opstellen op basis van anomalieën (90%, 95% of 99% drempelwaarden); % wijziging; boven/onder).
* Een voorvertoning weergeven van hoe vaak een waarschuwing wordt geactiveerd.
* Verzend alarm door e-mail of SMS met verbindingen naar auto-geproduceerde projecten van de Werkruimte van de Analyse.
* Maak &#39;gestapelde&#39; waarschuwingen die meerdere meetgegevens vastleggen in één waarschuwing.

U kunt dit nieuwe waarschuwingssysteem openen vanuit **[!UICONTROL More]** > **[!UICONTROL Alerts]** in elk rapport in Rapporten en Analyse.

Voor meer informatie, ga naar de documentatie van de Werkruimte van de Analyse over [Intelligente Alarm](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/intellligent_alerts.html).

## Een waarschuwing toevoegen {#task_51187E8BF19544DDA9EF2057E6F11D35}

Stappen waarin wordt beschreven hoe u een waarschuwing kunt toevoegen in Adobe Analytics.

<!-- 

t_add_an_alert.xml

 -->

Navigeer naar de nieuwe waarschuwingsfunctie in het menu **[!UICONTROL Analytics]** > **[!UICONTROL Components]** . U kunt het echter wel openen vanuit rapporten en analyses:

1. Open in Rapporten en Analytics het rapport waarin u een waarschuwing wilt instellen.
1. Klik op **[!UICONTROL More]** > **[!UICONTROL Add Alert]**.
1. Hiermee gaat u naar de [nieuwe waarschuwingsBuilder](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/alert-builder.html).

## Bestaande waarschuwingen weergeven of bewerken {#task_2ADF2A05EB784B8BBAFE293AC8243C46}

Taakcontext

1. Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Alerts]**. Hiermee gaat u naar het nieuwe [waarschuwingsbeheer](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/alert-manager.html).

## Migratie van verouderde waarschuwingen {#concept_7E8179F5EF6E4913B0CE5CF4FF186911}

Verschillende functies van bestaande waarschuwingen voor Analytics worden niet opgenomen in de nieuwe waarschuwingsmanager, die in het najaar van 2016 wordt uitgebracht (als onderdeel van de Analyse Workspace). In de volgende tabel vindt u een overzicht van de vervangen waarschuwingsfuncties en enkele waarschuwingsfuncties die in een ander formulier naar de nieuwe Waarschuwingsmanager worden gemigreerd.

<!-- 

deprecated_alerts.xml

 -->

<table id="table_9307013B16AC4AC7BFC6F4C440FCFDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Oudere waarschuwingsfunctie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Vervangen of gemigreerd? </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Totalen (alle items) </p> </td> 
   <td colname="col2"> <p>Maak waarschuwingen voor alle items van een dimensierapport. </p> </td> 
   <td colname="col3"> <p>In sommige gevallen, of u een alarm over alle punten van een afmetingsrapport creeert of of u opstelling de alarm over enkel samengevoegde metrisch door zich (niet toegepast op een afmeting), komt het zelfde resultaat voor. Stel bijvoorbeeld dat u een waarschuwing Alle items maandelijks maakt op de metrische waarde "Opbrengst". U krijgt hetzelfde resultaat als alleen het inkomstenrapport wordt uitgevoerd en een maandelijkse waarschuwing wordt ingesteld. </p> <p>In deze situatie, zal de erfenisTotals (Alle Punten) alarm niet meer beschikbaar zijn en aan laatstgenoemde, eenvoudigere versie gemigreerd. </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Top 1000 van items </p> <p> </p> </td> 
   <td colname="col2"> <p>Maak waarschuwingen voor de bovenste 1000 items in een rapport. </p> </td> 
   <td colname="col3"> <p>Niet meer beschikbaar in het nieuwe waarschuwingsbeheer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Unieke bezoekerswaarschuwingen op basis van tijd (dagelijks, wekelijks, maandelijks, enz.) Unieke bezoekers) </p> <p> </p> </td> 
   <td colname="col2"> <p>Maak waarschuwingen voor unieke bezoekersrapporten per uur, dag, week en maand. </p> </td> 
   <td colname="col3"> <p>In het nieuwe waarschuwingsbeheer worden bepaalde op tijd gebaseerde waarschuwingen voor Unieke bezoekers niet meer ondersteund. Wanneer u bijvoorbeeld eerder een wekelijkse waarschuwing voor Daily Unique Visitors kunt instellen, kunt u een dagelijkse, wekelijkse, enz. instellen. waarschuwing over de metrische gegevens van de Unieke Bezoekers. (De Werkruimte van de Analyse steunt unieke bezoekers metrisch, maar niet Dagelijks/Wekelijks/Maandelijks/etc. Unieke cijfers voor bezoekers.) </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoeken </p> </td> 
   <td colname="col2"> <p>Maak waarschuwingen voor een dimensierapport waarop een zoekopdracht is toegepast. Alleen van toepassing op "totalen" ("Alle items") of "Top 1000 items". </p> <p> </p> </td> 
   <td colname="col3"> <p>Niet meer beschikbaar in het nieuwe waarschuwingsbeheer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Specifieke rapporten voor rapporten en analyses </p> </td> 
   <td colname="col2"> <p>Creeer alarm voor verscheidene rapporten die in Rapporten &amp; Analytics bestaan en niet aan een rapport van de Werkruimte van de Analyse beantwoorden, zoals 
     <ul id="ul_9A690970A5AE4ED39E664DF23EF3164F"> 
      <li id="li_E2F44EDBA1D945CEBAC4802ED714E7A1">JavaScript </li> 
      <li id="li_B847C6A988854F76824F099681705EC9">Lengte pad </li> 
      <li id="li_4AF656460BC748E8802FAF258D01842F">Bots </li> 
      <li id="li_A300D2803B244774839BEC23D3EB533A">Tijdzones </li> 
      <li id="li_7A0B4CF92F4D47238B7B329EEC213322">Domeinen op hoofdniveau </li> 
     </ul> </p> <p> </p> </td> 
   <td colname="col3"> <p>Niet meer beschikbaar in het nieuwe waarschuwingsbeheer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Waarschuwingen met een ASI-sleuf als rapportsuite </p> </td> 
   <td colname="col2"> <p>U kunt geen ASI-sleuven meer <a href="https://marketing.adobe.com/resources/help/en_US/reference/ASI_slots_admin.html"  > maken of bewerken </a> en deze zijn niet beschikbaar voor gebruik in de analysewerkruimte. Daarom worden zij niet ondersteund door de nieuwe waarschuwingen. </p> <p> </p> </td> 
   <td colname="col3"> <p>Niet beschikbaar in het nieuwe waarschuwingsbeheer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Waarschuwingen die gebruikmaken van participatiemetingen </p> </td> 
   <td colname="col2"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/reference/metrics_participation.html"  > De metriek van de participatie </a> is beschikbaar in Rapporten &amp; Analytics, maar is momenteel niet beschikbaar in het nieuwe alarminstallatiesysteem in de Werkruimte van de Analyse. </p> <p> </p> </td> 
   <td colname="col3"> <p>Niet beschikbaar in het nieuwe waarschuwingsbeheer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Maandelijkse waarschuwingen voor aangepaste kalenderrapporten </p> </td> 
   <td colname="col2"> <p>Dit is alleen van toepassing op klanten met waarschuwingen die zijn ingesteld voor rapportsuites met <a href="https://marketing.adobe.com/resources/help/en_US/arb/custom_calendar.html"  > aangepaste begindatums voor de maand </a> (nationale detailhandel/NRF en aangepaste kalendertypen). </p> <p>Het heeft geen invloed op waarschuwingen over Gregoriaanse of Gewijzigde Gregoriaanse kalenderrapportsuites. Eerder werden deze waarschuwingen verzonden op de eerste dag van de Gregoriaanse maand (bijvoorbeeld 1 januari, 1 februari enz.). Dit werkt niet met het nieuwe onderdeel Anomaly Detection van waarschuwingen, dat bij het opsporen van anomalieën rekening houdt met gegevens van vorige maanden. In de toekomst, zullen wij steun aan ons het plannen systeem voor douanecalendars toevoegen zodat zowel Alarm als Geplande Projecten kunnen worden gepland om op de eerste dag van de maand van de douanekalender in plaats van enkel de eerste dag van de Gregoriaanse maand te verzenden. </p> <p> </p> </td> 
   <td colname="col3"> <p>Nog niet beschikbaar in het nieuwe waarschuwingsbeheer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Waarschuwingen die sinds september 2015 niet zijn gestart. </p> </td> 
   <td colname="col2"> <p>Er zijn verschillende redenen waarom waarschuwingen sinds september 2015 niet zouden zijn uitgevoerd, zoals: </p> 
    <ul id="ul_15812938A2454537AF6ADDB039DE16BC"> 
     <li id="li_D079A819CEE04F609AF18C09EEE83F0D">U hebt op "Uitschakelen" geklikt in het waarschuwingsbericht. </li> 
     <li id="li_E23D01FA0B1341AD8BC1DDD16FB1366F">De waarschuwing bevat fouten en wordt nooit met succes voltooid. </li> 
    </ul> <p> </p> </td> 
   <td colname="col3"> Deze waarschuwingen worden niet naar het nieuwe systeem gemigreerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Waarschuwingen die zijn gemarkeerd als "uitgeschakeld" </td> 
   <td colname="col2"> Er is momenteel geen manier om alarm in het nieuwe gebruikersinterface onbruikbaar te maken/opnieuw toe te laten, hoewel er plannen zijn om deze functionaliteit toe te voegen. <p> </p> </td> 
   <td colname="col3"> Deze waarschuwingen worden niet naar het nieuwe systeem gemigreerd. </td> 
  </tr> 
 </tbody> 
</table>

