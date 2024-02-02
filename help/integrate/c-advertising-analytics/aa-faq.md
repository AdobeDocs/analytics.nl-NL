---
description: Veelgestelde vragen over Advertising Analytics.
title: Veelgestelde vragen voor reclameanalyses
feature: Advertising Analytics
exl-id: 664a5641-1c79-439f-a9fb-2ff134574412
source-git-commit: 591b82e271cc7474e9b413015804d4fe37d9050c
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 0%

---

# Veelgestelde vragen

## Toegang/rechten {#access}

+++ Moet ik Adobe Advertising Cloud of Adobe Advertising Cloud (AMO) klant zijn om toegang te krijgen tot deze functionaliteit?

Nee, deze functionaliteit is beschikbaar voor niet-Advertising Cloud- en niet-AMO-klanten. </p> <p>AMO-klanten kunnen gebruikmaken van de bestaande integratie tussen Analytics en AMO; ze kunnen Ad Analytics niet gebruiken.

+++

+++ Welke Adobe Analytics SKU&#39;s geven u het recht om Advertising Analytics te gebruiken?

Advertising Analytics is beschikbaar voor Adobe Analytics

* [Selecteren](https://www.adobe.com/nl/data-analytics-cloud/analytics/select.html)

* [Eerste](https://www.adobe.com/nl/data-analytics-cloud/analytics/prime.html)

* [Ultieme](https://www.adobe.com/nl/data-analytics-cloud/analytics/ultimate.html)

+++

+++ Moet ik extra betalen om Advertising Analytics te gebruiken?

Nee, buiten de juiste SKU-provisioning maakt Advertising Analytics geen extra kosten.

+++

+++ Telt Advertising Analytics op mijn gebruik van de servervraag

Nee, Advertising Analytics gebruikt een speciaal gegevensbrontype dat geen kosten veroorzaakt voor serveraanroepen.

+++

+++ Als ik Advertising Cloud/AMO al gebruik, kan ik dan nog steeds de Advertising Analytics-functionaliteit gebruiken?

Elk compatibel account voor zoekmachines wordt doorgegeven aan Advertising Analytics en wordt weergegeven als alleen-lezen. Alle bewerkingen of updates moeten worden verwerkt in Advertising Cloud/AMO.

+++

+++ Ik bezit de juiste SKU, maar ik heb geen toegang tot Advertising Analytics, waarom is dat?

Advertising Analytics is alleen beschikbaar voor Adobe Analytics-beheerders; beheerders kunnen echter toegang verlenen aan niet-beheerders. Neem contact op met uw beheerder voor toegangsrechten.

+++

## Advertising Analytics gebruiken {#using}

+++ Welke rekeningen van zoekprogramma&#39;s zijn opgenomen in Advertising Analytics?

Motoraccounts bevatten Google AdWords en Microsoft Bing.

+++

+++ Waar ga ik naar Advertising Analytics?

Na het aanmelden bij Adobe Analytics navigeert u naar de [!UICONTROL Admin]. Selecteer vervolgens [!UICONTROL Advertising Analytics] om je zoekprogrammaaccounts toe te voegen.

+++

+++ Hoe worden de gegevens verzameld en doorgegeven aan Analytics?

Advertising Analytics gebruikt een reeks aangepaste API&#39;s om gegevens van zoekmachines via de Adobe Advertising Cloud door te geven aan Analytics.

+++

+++ Welke zoekgegevens krijg ik met deze integratie?

U krijgt

* Impressies
* Klikken
* Kosten
* Kwaliteitsscore
* Gemiddelde positie rechtstreeks vanuit de zoekmachines, en
* Instanties van AMO-id (klik op Instanties).

+++

+++ Kan ik mijn Advertising Analytics-gegevens onderbreken door andere Analytics-gegevens (metriek/afmetingen)?

Nee, de onbewerkte zoekgegevens worden opgenomen als een onafhankelijke gegevensset. Nochtans, is er een versie van Instanties van de klikgegevens die door andere gegevens van Analytics kunnen worden verdeeld.

+++ Wat is de definitie van de verschillende statusindicatoren voor mijn accounts (in behandeling, actief, gepauzeerd, enz.)? Elk van deze statusindicatoren identificeert de levenscyclusfase van elk onderzoek motorrekening.

* [!UICONTROL Pending]
* [!UICONTROL Paused] betekent dat de rekening eerder is ingesteld, maar niet is geactiveerd.
* [!UICONTROL Active] betekent dat de rekening volledig is opgezet en aan zoekgegevens voldoet.

+++

+++ Ik probeer mijn Advertising Analytics-accounts toe te wijzen aan een specifieke rapportsuite, maar deze is niet beschikbaar in het modaal rapportenpakket. Waarom?

Voordat u een rapportsuite aan een Advertising Analytics-account kunt toewijzen, moet de gewenste rapportsuite [voorzien voor Advertising Analytics-rapportage](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md)
Dit gebeurt via een aparte beheerpagina die u kunt vinden op: Beheer > Rapportageopties > [rapportsuite selecteren] > Instellingen bewerken > Advertising Analytics-configuratie.

+++

+++ Is het mogelijk om een virtuele rapportsuite aan een Advertising Analytics-account toe te wijzen?

Met virtuele rapportsets worden geen gegevens verzameld, zodat u een Advertising Analytics-account niet rechtstreeks kunt toewijzen aan een Virtual Report-suite. U kunt de Advertising Analytics-account echter toewijzen aan de bovenliggende rapportsuite van de Virtual Report Suite waarin u gegevens wilt zien. De metriek van de Motor van het Onderzoek (klik/kosten/impressies) kunnen niet in de Virtuele rapportreeks verschijnen tenzij u een &quot;of&quot;voorwaarde in uw segmentlogica opneemt die op AMO ID (of zijn classificatie) wordt gebaseerd. Voorbeeld: het toevoegen van &quot;alle treffers waar AMO ID bestaat&quot; zou de metriek van de onderzoeksmotor in het segment omvatten.

+++

+++ Zijn Advertising Analytics-meetgegevens die in de <b>Marketingkanalen</b> rapporteren?

Nr, zijn zij niet inbegrepen in het rapport van de Kanalen van de Marketing.

+++

+++ Wanneer worden de zoekgegevens naar Analytics gehaald?

De zoekgegevens worden uit de zoekmachines gehaald rond 6AM (06:00) in de tijdzone van uw datacenter Analytics. Dit is wanneer de gegevens van AMO worden verzameld en in de rapportreeks opgenomen. Het wordt dan omgezet in de tijdzone van de rapportreeks als deel van het opnemen van de gegevens in Analytics.

+++

+++ Wat kan er gebeuren? <b>vastgelegd voor klik</b>? Zien we indrukken, kosten, gemiddelde positie, enzovoort? zelfs zonder klik ? </p> </td>

De AMO-id legt de maatstaven van de zoekmachine vast: Impressies, Kosten, Klikken, Gemiddelde positie en Gemiddelde kwaliteitsscore. Als er geen kliks zijn, maar er indrukken zijn, dan zullen de beeld/positie/kwaliteitsscore gegevens nog naar Analytics worden verzonden. Doorgaans zijn er ook geen kosten verbonden als er niet wordt geklikt.

+++

+++ Op welk niveau worden deze gegevens vastgelegd? <b>Bezoeker? Hit?</b>

De metriek van de motor van het Onderzoek wordt gevangen op het raakniveau en met AMO identiteitskaart (en zijn classificaties) verbonden. Dit zijn gegevens op overzichtsniveau die geen verband houden met bezoeken/bezoekers. Als zodanig kunnen de metriek van de zoekmachine slechts in segmenten worden gebruikt die bereik op raakniveau zijn en op AMO-id (of zijn classificaties) gebaseerd zijn.

De AMO-id wordt ook vastgelegd op de bestemmingspagina in de hit voor die pagina (die de id verbindt met het bezoek/de bezoeker) en zal verderop in de stroom blijven staan om krediet te krijgen voor andere analytische gegevens (totdat deze verlopen of door een nieuwe AMO-id wordt overschreven). Net als elke andere eVar wordt het volledig in de gegevensset opgenomen.

+++

+++ Wordt alleen google.com vastgelegd of <b>landversies</b> (zoals google.co.uk, google.it, google.fr, of google.de) eveneens?

De classificatie van het Platform van de Advertentie vangt deze waarden: &quot;Adwords van Google&quot;, en &quot;Bing Adds&quot;. De beste praktijk is om de landcode op te nemen in de naamgeving van campagnes. Vervolgens kunt u naar beneden of naar een segment filteren (bijvoorbeeld als alle campagnes beginnen met landcode_ en u vervolgens een segment maakt waarin Campagnes (AMO ID) beginnen met &quot;UK_&quot;, zodat u alleen gegevens voor het Verenigd Koninkrijk krijgt).

+++

+++ De metrische &quot;Kosten AMO&quot;is de kosten die voor elk sleutelwoord/elke advertentie worden betaald zoals die door het onderzoeksmotor worden gemeld. Zijn dit nettokosten of brutokosten?

&quot;AMO-kosten&quot; zijn alleen de kosten die aan de zoekmachines worden betaald. Hieronder vallen geen kosten voor het optimaliseren van de zoekopdracht of het beheerplatform.

+++

+++ Zijn er plannen om andere reclamekanalen op te nemen, zoals <b>Weergave</b> of <b>Sociaal</b>?

Nee, op dit moment hebben we geen plannen voor deze andere kanalen op de routekaart.

+++


## Automatisch versus handmatig bijhouden {#section_7437C4698A6D482EB7ED94A948390119}

<table id="table_9738FF8459574ED2937A860A665BE739"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Q: Bij het instellen van mijn advertentieaccount staat het volgende:<b> Automatisch bijhouden</b> kan leiden tot onbedoelde gevolgen. Welke gevolgen kunnen zich voordoen? </p> </td> 
   <td colname="col2"> <p>A: 
     <ul id="ul_59EFF4A2ECE947EBBDB6A9FF6D072FE0"> 
      <li id="li_8731E4B7D6ED4F0996B3630A35D5BAC4">In de modus Automatisch wordt geprobeerd URL-parameters toe te voegen aan het einde van de volgende sjablonen/doel-URL's in de juiste indeling. <b>Het is echter uw verantwoordelijkheid om ervoor te zorgen dat de toegevoegde URL-parameters correct blijven op de laatste bestemmingspagina. </b> </li> 
      <li id="li_1202FE1FC88342378A60E8FE65E5426B">In de modus Automatisch kunnen sleutelwoorden worden ingevoegd in de bestemmings-URL en het is mogelijk dat uw webserver geen trefwoorden met speciale tekens ondersteunt. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Als ik eerst handmatig of automatisch bijhouden heb ingesteld, <b>kan ik schakelen</b> op de andere volgmodus later? Wat zijn de gevolgen? </p> </td> 
   <td colname="col2"> <p>A: Ja u kunt schakelen, maar u zult de oude volgende logica moeten verwijderen alvorens de schakelaar te maken. Dit kan in wat onderbreking van het volgen op de dag resulteren de schakelaar wordt gemaakt (vooral als zich van hand aan automatisch beweegt). Daarom wordt aanbevolen niet over te schakelen, tenzij dit absoluut noodzakelijk is. </p> 
    <ul id="ul_3F3CADD1C97B4947A13837CEE63A599D"> 
     <li id="li_CB9265951FD040388AEAB9EAD790A36E"><b>Overschakelen van Handmatig naar Automatisch</b>: Verwijder de handmatige toevoegingen aan de volgsjablonen en schakel de schakeloptie in de gebruikersinterface van Advertising Analytics van handmatig naar Automatisch in en sla de instelling op. Het kan tot x uur duren voordat het systeem de automatische trackingcodes heeft ingevuld. </li> 
     <li id="li_2B6ED1342E2D443B8AF26D03532AB8E4"><b>Schakelen van Automatisch naar Handmatig</b>: Werk de schakeloptie van handmatig naar automatisch bij in de Advertising Analytics-instellingsinterface en implementeer de handmatige volgcodes zo snel mogelijk. Als u tijdens de implementatie van de handmatige volgcodes de automatische volgcodes in de sjablonen voor zoekprogramma's ziet, verwijdert u deze. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
