---
description: Overzicht van de functionaliteit voor het gebruik van Adobe Analytics-serveroproepen.
title: Overzicht van serveroproepgebruik
feature: Server Call Usage
exl-id: d3d64f1e-f01b-4b9e-9aee-c14e574fc40b
source-git-commit: dc9cd6bb45af0c992c37ffe20ea22eab67789ec5
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 1%

---

# Overzicht van serveroproepgebruik

## Waarom controle en alarm aan het Gebruik van de Vraag van de Server? {#section_060C29BF1D00444B85892AD1FCF55290}

Het gebruik van de Vraag van de Server van Adobe Analytics richt uw verzoeken om transparantie in zowel browser als mobiele gegevens van het de vraaggebruik van de server. U hebt toegang tot:

* Een dashboard van het Gebruik van de Vraag van de Server dat uw gegevens van het de vraagverbruik van de server volgt en het met uw contractuele grens vergelijkt. (**[!UICONTROL Analytics > Admin > Server Call Usage]**)
* Een het waakzame type van het Gebruik van de Vraag van de Server in Waakzame Bouwer dat u opstellingsalarm laat om overzichten te verhinderen (**[!UICONTROL Analytics > Components >Alerts]**)

De belangrijkste voordelen van het Gebruik van de Vraag van de Server omvatten:

* **Zichtbaarheid** in uw gegevens van het de vraagverbruik en van de verbinding van de server, met inbegrip van mobiel gebruik tegenover uw contractuele het gebruiksgrens van de servervraag.
* **Waarschuwingen** om u op de hoogte te stellen van het risico of het optreden van een overschrijding en om de mogelijkheid van overschrijding voor te bereiden of te beïnvloeden.

Eerder, terwijl u tot maandelijkse gegevens van het de vraagverbruik van de server kon toegang hebben onder  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Billing]** Deze gegevens werden pas 6 dagen nadat de facturering voor die maand was afgesloten, bijgewerkt. Bovendien omvatten de gegevens geen mobiel verbruik. Deze functie vervangt ook de huidige **[!UICONTROL Billing Information]** verslag krachtens  **[!UICONTROL Analytics]** > **[!UICONTROL Reports]** .

## Vereisten {#section_49AE590FFC7C4E8A83C640C4AAA581AA}

* **Machtigingen:** Om tot het Dashboard van het Gebruik van de Vraag van de Server en Alert Builder/Manager toegang te hebben, moet u een Beheerder van Adobe Analytics zijn.
* **Machtigingen:** Beheerders kunnen toegang verlenen aan niet-beheerders: de toestemming wordt geroepen **[!UICONTROL Server Call Usage]**. Zie [Machtiging voor serveroproepgebruik](/help/admin/admin/c-server-call-usage/overage-overview.md#section_FCC58EB635954A32990D4E67B52B4369).

## Belangrijke terminologie {#section_CBA348A039F34563B097CD8890AB358D}

Hier is een korte inleiding op essentiële terminologie voor het Gebruik van de Vraag van de Server:

<table id="table_4E97F85F13344A2C962FA4FA5A51642E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Term </th> 
   <th colname="col2" class="entry"> Definitie </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Serveroproep </p> </td> 
   <td colname="col2"> <p>Een serveraanroep, ook wel een "hit" of een "verzoek om een afbeelding" genoemd, is een instantie waarin gegevens naar Adobe-servers worden verzonden om te worden verwerkt. Het gemeenschappelijkste type van servervraag is een paginamening. Een paginamening komt voor waar een bezoeker een pagina op uw website bekijkt en een servervraag wordt geproduceerd aan Adobe, waar de informatie wordt verzameld, verwerkt, en dan inbegrepen in uw rapportmetriek. </p> <p>Er zijn andere soorten servervraag, met inbegrip van uitgangsverbindingen en dossierdownloads, waar de gegevens naar Adobe worden verzonden om te verwerken, maar zij worden niet geregistreerd als nieuwe paginamening. Zelfs "uitgesloten"paginameningen (die van uw rapporten door een IP adreswaaier worden uitgesloten u, bijvoorbeeld) vormt servervraag omdat zij door Adobe worden ontvangen en verwerkt maar nooit in uw rapporten verschijnen. </p> <p><b>Primaire serveroproep</b>: Aanvragen die rechtstreeks zijn ontvangen van de browsers van de websitebezoeker of de API voor het invoegen van gegevens. Deze groep bevat primaire Hits (paginaweergaven), primaire aangepaste gebeurtenissen, primaire downloadgebeurtenissen en primaire afsluitgebeurtenissen. </p> <p><b>Tweede serveroproep</b>: Kopieën van primaire servervraag die door multi-suite markeringen wordt gecreeerd of door een VISTA regel wordt gekopieerd/wordt bewogen. Als een secundaire servervraag (niet gekopieerd) aan een verschillende rapportreeks door een regel VISTA is bewogen, worden de geaccumuleerde secundaire vraag afgetrokken van de primaire servervraag. </p> <p><b>Mobiele primaire serveroproep </b> </p> <p>Verzoeken die rechtstreeks zijn ontvangen van een van de mobiele SDK's. Inclusief trackAction, trackState, trackApp loopt vast, trackActionFromBackground, trackLocation, trackBeacon, trackPushMessageClickThrough, trackTimedActionBacklog, trackLifetimeValueIncrease.</p> <p><b>Mobiele secundaire serveroproep</b> </p> <p>Kopieën van primaire servervraag die door multi-suite markeringen wordt gecreeerd of door een VISTA regel wordt gekopieerd/wordt bewogen. Als een secundaire servervraag (niet gekopieerd) aan een verschillende rapportreeks door een regel VISTA is bewogen, worden de geaccumuleerde secundaire vraag afgetrokken van de primaire servervraag. </p> <p>Opmerking: Als uw bedrijf contractueel alleen recht heeft op mobiele serveraanroepen (primair of secundair), tellen zowel uw web- als mobiele-specifieke gebruik voor uw specifieke mobiele inzet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Factureringsbedrijf (Factuur-ID) </p> </td> 
   <td colname="col2"> <p>De juridische entiteit die voor servervraag in rekening wordt gebracht. Bijvoorbeeld adobe.com. Elk factureringsbedrijf heeft een Facturerings identiteitskaart die wordt gebruikt om de facturerende klant uniek te identificeren. Een facturerings-id kan aan meerdere Experience Cloud Orgs zijn gekoppeld. er is niet altijd een 1:1-relatie tussen een org en een facturerings-id. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanmeldingsbedrijf </p> </td> 
   <td colname="col2"> <p>Eén factureringsbedrijf kan beschikken over <a href="https://helpx.adobe.com/analytics/kb/multiple-login-companies.html"> meerdere aanmeldbedrijven </a>. Een login bedrijf is een inzameling van rapportsuites die door uw organisatie worden gebruikt. Sommige organisaties hebben veelvoudige login bedrijven die op verschillende delen van de organisatie van toepassing zijn. Dit is vooral nuttig voor grote organisaties die met verschillende bedrijfseenheden te maken hebben waar vele rapportsuites niet op anderen in het bedrijf van toepassing zijn. </p> <p>Vaak gaat het om de regionale dochterondernemingen van een onderneming. Dit voorbeeld toont login bedrijven en hun bijbehorende rapportsuites: </p> 
    <ul id="ul_8C756C7972D04F5E89D6E32BB06D26C3"> 
     <li id="li_EA6257FED7854B6FAA071926D0F8A07C">adobe.global: RS1, RS2, RS3, RS4 </li> 
     <li id="li_3EAFB556849E4CCC9D96D5A3492EC898">adobe.us: RS1, RS2 </li> 
     <li id="li_572FFB3F4BF545BDB13102D82CE5E50C">adobe.in: RS3 </li> 
     <li id="li_B6ACBA35E18A427AA83F76BD38E502D7">adobe.de: RS4 </li> 
    </ul> <p>Opmerking: Gebruikersgegevens voor serveroproepen voor <u>alles</u> de rapportsuites binnen een factureringsbedrijf is voor alle gebruikers zichtbaar met de aangewezen <a href="/help/admin/admin/c-server-call-usage/overage-overview.md#section_FCC58EB635954A32990D4E67B52B4369"> machtiging</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud-organisatie </p> </td> 
   <td colname="col2"> <p>Een organisatie is de entiteit die een beheerder toelaat om groepen en gebruikers te vormen, en om enig teken-binnen in de Experience Cloud te controleren. De organisatie werkt als een login bedrijf dat alle producten en oplossingen van de Experience Cloud overspant. </p> <p>Meestal is een organisatie uw bedrijfsnaam. Een bedrijf kan echter veel organisaties hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verbinding serveroproep </p> </td> 
   <td colname="col2"> <p>Wanneer uw bedrijf een contract met Adobe ondertekent, identificeert het team van de Verkoop van de Adobe met u, de klant, de types (Primair, Secundair, Mobiel Primair, Secundair Mobiel) en het ongeveer aantal servervraag die u in de loop van de contractperiode verwacht te zullen veroorzaken. Dit is uw totale verplichting van de servervraag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruiksperiode </p> </td> 
   <td colname="col2"> <p>Voor het controleren van het gebruik van de servervraag, wordt deze totale verplichting van de servervraag verdeeld in kleinere gebruiksperioden (zoals 3 maanden) om jaar-over-jaar vergelijkingen te vergemakkelijken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Contractperiode </p> </td> 
   <td colname="col2"> <p>Contractperioden kunnen meerdere jaren duren. Laten we zeggen dat uw bedrijf een verplichting voor servergesprekken heeft van 6 miljoen oproepen voor een contractperiode van 3 jaar. Met het oog op het toezicht op het gebruik van servergesprekken kan deze periode van drie jaar worden opgesplitst in kleinere gebruiksperiodes om vergelijkingen over jaar mogelijk te maken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Machtiging voor serveroproepgebruik {#section_FCC58EB635954A32990D4E67B52B4369}

De toestemming van het Gebruik van de Vraag van de Server wordt automatisch verleend aan Admins van Analytics. Gebruikers kunnen het dashboard bekijken en waarschuwingen voor serveroproepen maken. Beheerders kunnen deze machtiging aan niet-beheerders verlenen.

>[!NOTE]
>
>Uw bedrijf kan kiezen welke login bedrijven toegang tot het Gebruik van de Vraag van de Server hebben.

<table id="table_86256AD8B4554F369439A8FDF2F545E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam bevoegdheid </th> 
   <th colname="col3" class="entry"> Toestemming verlenen als u bent aangemeld bij Adobe Analytics (oude aanmelding) </th> 
   <th colname="col4" class="entry"> Machtiging verlenen als u bent aangemeld bij Adobe Experience Cloud </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gebruik van server calls </p> </td> 
   <td colname="col3"> 
    <ol id="ol_13A984328D264488B7045DC7521A5F55"> 
     <li id="li_ACDA518C7D184084AC1DFA7B38C67314">Meld u aan bij Analytics via sc.omniture.com. </li> 
     <li id="li_066D90AB071941C3869EDAFCE981707A">Navigeren naar <span class="ignoretag"> <span class="uicontrol"> Beheer </span>  &gt; <span class="uicontrol"> Alle beheerders </span>  &gt; <span class="uicontrol"> Gebruikersbeheer </span>  &gt; <span class="uicontrol"> Groepen </span>  &gt; <span class="uicontrol"> Alle rapporttoegang bewerken </span>  &gt; <span class="uicontrol"> Analysegereedschappen </span>  &gt; <span class="uicontrol"> Aanpassen </span>  &gt; <span class="uicontrol"> Gebruik van serveroproep </span> </span> </li> 
    </ol> </td> 
   <td colname="col4"> 
    <ol id="ol_518673ED323A4C5993A3B9F4BA09E405"> 
     <li id="li_56FF685A3B454ECEA5F16BB591A60034">Meld u aan bij login.experienceCloud.adobe.com.</li> 
     <li id="li_FA1AE0F19DEF4AB2AA77B22CCA2995F9">Klikken <span class="uicontrol"> Analyse </span>. </li> 
     <li id="li_22A4CBB84B5A451780873BBE67E6E6EF">Navigeren naar <span class="ignoretag"> <span class="uicontrol"> Producten </span>  &gt; <span class="uicontrol"> Productprofiel </span>  &gt; <span class="uicontrol"> Machtigingen </span>  &gt; <span class="uicontrol"> Analysegereedschappen </span>  &gt; <span class="uicontrol"> Gebruik van serveroproep </span> </span> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>