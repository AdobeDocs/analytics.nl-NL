---
description: Overzicht van de functionaliteit voor het gebruik van Adobe Analytics-serveroproepen.
title: Overzicht van serveroproepgebruik
feature: Server Call Usage
exl-id: d3d64f1e-f01b-4b9e-9aee-c14e574fc40b
role: Admin
source-git-commit: 58e1d3025b455de7fa07037b3b0659330c8324c7
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 1%

---

# Gebruik van serveroproepen

Met het gebruik van Adobe Analytics-serveroproepen worden uw verzoeken om transparantie verwerkt in de gebruikersgegevens van zowel de browser als de mobiele server. U hebt hiermee toegang tot:

* Een dashboard van het het gebruiksdashboard van de servervraag dat uw gegevens van het servervraagverbruik volgt en het met uw contractuele grens vergelijkt. (In Adobe Analytics selecteert u > [!UICONTROL **Beheerder**] > [!UICONTROL **Gebruik van serveroproepen**])
* Een waarschuwingstype voor het gebruik van een serveraanroep in de waarschuwingsbuilder waarmee u waarschuwingen kunt instellen om overgangen te voorkomen (selecteer in Adobe Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Waarschuwingen**])

De belangrijkste voordelen van servervraaggebruik omvatten:

* **Zichtbaarheid** in uw gegevens van het de vraagverbruik en van de verbinding van de server, met inbegrip van mobiel gebruik tegenover uw contractuele het gebruiksgrens van de servervraag.
* **Waarschuwingen** om u op de hoogte te stellen van het risico of het optreden van een overschrijding en om de mogelijkheid van overschrijding voor te bereiden of te beïnvloeden.

## Vereisten {#section_49AE590FFC7C4E8A83C640C4AAA581AA}

* **Rechten:** Als u toegang wilt tot het gebruiksdashboard voor de serveraanroep en de builder of waakzame manager, moet u een Adobe Analytics-beheerder zijn.
* **Rechten:** Beheerders kunnen toegang verlenen aan niet-beheerders: de machtiging wordt aangeroepen **[!UICONTROL Server call usage]**. Zie [Machtiging voor oproepgebruik van server](#server-call-usage-permission).

## Belangrijke terminologie {#terminology}

De volgende termijnen zijn belangrijk in het begrip van het gebruik van de servervraag:

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
   <td colname="col2"> <p>Een serveraanroep, ook wel een "hit" of een "verzoek om een afbeelding" genoemd, is een instantie waarin gegevens naar Adobe servers worden verzonden om te worden verwerkt. Het gemeenschappelijkste type van servervraag is een paginamening. Een paginamening komt voor waar een bezoeker een pagina op uw website bekijkt en een servervraag wordt geproduceerd aan Adobe, waar de informatie wordt verzameld, verwerkt, en dan inbegrepen in uw rapportmetriek. </p> <p>Er zijn andere soorten servervraag, met inbegrip van uitgangsverbindingen en dossierdownloads, waar de gegevens naar Adobe worden verzonden om te verwerken, maar zij worden niet geregistreerd als nieuwe paginamening. Zelfs "uitgesloten"paginameningen (die van uw rapporten door een IP adreswaaier worden uitgesloten u, bijvoorbeeld) vormt servervraag omdat zij door Adobe worden ontvangen en verwerkt maar nooit in uw rapporten verschijnen. </p> <p><b>Primaire serveroproep</b>: Verzoeken die rechtstreeks zijn ontvangen van browsers van websitebezoekers of de API voor het invoegen van gegevens. Deze groep bevat primaire Hits (paginaweergaven), primaire aangepaste gebeurtenissen, primaire downloadgebeurtenissen en primaire afsluitgebeurtenissen. </p> <p><b>Tweede serveroproep</b>: Kopieën van primaire serveraanroepen die zijn gemaakt met tags van meerdere suite of die zijn gekopieerd/verplaatst door een VISTA-regel. Als een secundaire servervraag (niet gekopieerd) aan een verschillende rapportreeks door een regel VISTA is bewogen, worden de geaccumuleerde secundaire vraag afgetrokken van de primaire servervraag. </p> <p><b>Mobiele primaire serveroproep </b> </p> <p>Verzoeken die rechtstreeks zijn ontvangen van een van de mobiele SDK's. Inclusief trackAction, trackState, trackApp loopt vast, trackActionFromBackground, trackLocation, trackBeacon, trackPushMessageClickThrough, trackTimedActionBacklog, trackLifetimeValueIncrease.</p> <p><b>Mobiele secundaire serveroproep</b> </p> <p>Kopieën van primaire servervraag die door multi-suite markeringen wordt gecreeerd of door een VISTA regel wordt gekopieerd/wordt bewogen. Als een secundaire servervraag (niet gekopieerd) aan een verschillende rapportreeks door een regel VISTA is bewogen, worden de geaccumuleerde secundaire vraag afgetrokken van de primaire servervraag. </p> <p>Opmerking: als uw bedrijf contractueel alleen recht heeft op mobiele serveraanroepen (primair of secundair), tellen zowel uw web- als mobiele-specifieke gebruik mee voor uw specifieke mobiele inzet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Factureringsbedrijf (Factuur-ID) </p> </td> 
   <td colname="col2"> <p>De juridische entiteit die voor servervraag in rekening wordt gebracht. Bijvoorbeeld adobe.com. Elk factureringsbedrijf heeft een Facturerings identiteitskaart die wordt gebruikt om de facturerende klant uniek te identificeren. Een facturerings-id kan aan meerdere Experience Cloud-Orgs worden gekoppeld; er is niet altijd een 1:1-relatie tussen een org en een facturerings-id. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanmeldingsbedrijf </p> </td> 
   <td colname="col2"> <p>Eén factureringsbedrijf kan <a href="https://helpx.adobe.com/analytics/kb/multiple-login-companies.html"> meerdere aanmeldbedrijven </a>. Een login bedrijf is een inzameling van rapportsuites die door uw organisatie worden gebruikt. Sommige organisaties hebben veelvoudige login bedrijven die op verschillende delen van de organisatie van toepassing zijn. Dit is vooral nuttig voor grote organisaties die met verschillende bedrijfseenheden te maken hebben waar vele rapportsuites niet op anderen in het bedrijf van toepassing zijn. </p> <p>Vaak gaat het om de regionale dochterondernemingen van een onderneming. Dit voorbeeld toont login bedrijven en hun bijbehorende rapportsuites: </p> 
    <ul id="ul_8C756C7972D04F5E89D6E32BB06D26C3"> 
     <li id="li_EA6257FED7854B6FAA071926D0F8A07C">adobe.worldwide: RS1, RS2, RS3, RS4 </li> 
     <li id="li_3EAFB556849E4CCC9D96D5A3492EC898">adobe.us: RS1, RS2 </li> 
     <li id="li_572FFB3F4BF545BDB13102D82CE5E50C">adobe.in: RS3 </li> 
     <li id="li_B6ACBA35E18A427AA83F76BD38E502D7">adobe.de: RS4 </li> 
    </ul> <p>Opmerking: gegevens van serveroproepgebruik voor <u>alles</u> de rapportsuites binnen een factureringsbedrijf is voor alle gebruikers zichtbaar met de aangewezen <a href="/help/admin/admin/c-server-call-usage/overage-overview.md#section_FCC58EB635954A32990D4E67B52B4369"> machtiging</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Organisatie van Experiencen Cloud </p> </td> 
   <td colname="col2"> <p>Een organisatie is de entiteit die een beheerder toelaat om groepen en gebruikers te vormen, en om enig teken-binnen in het Experience Cloud te controleren. De organisatie werkt als een login bedrijf dat alle producten en oplossingen van de Experience Cloud overspant. </p> <p>Meestal is een organisatie uw bedrijfsnaam. Een bedrijf kan echter veel organisaties hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verbinding met serveroproep </p> </td> 
   <td colname="col2"> <p>Wanneer uw bedrijf een contract met Adobe ondertekent, identificeert het team van de Verkoop van de Adobe met u, de klant, de types (Primair, Secundair, Mobiel Primair, Secundair Mobiel) en het geschatte aantal servervraag die u verwacht te zullen veroorzaken over de loop van de contractperiode. Dit is uw totale verplichting van de servervraag. </p> </td> 
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

## Machtiging voor oproepgebruik van server {#permission}

De toestemming van het het vraaggebruik van de Server wordt automatisch verleend aan Admins van Analytics. Gebruikers kunnen het dashboard bekijken en waarschuwingen voor serveroproepen maken. Beheerders kunnen deze machtiging aan niet-beheerders verlenen.

>[!NOTE]
>
>Uw bedrijf kan kiezen welke login bedrijven toegang tot het vraaggebruik van de Server hebben.

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
   <td colname="col1"> <p>Gebruik van serveroproepen </p> </td> 
   <td colname="col3"> 
    <ol id="ol_13A984328D264488B7045DC7521A5F55"> 
     <li id="li_ACDA518C7D184084AC1DFA7B38C67314">Meld u aan bij Analytics via sc.omniture.com. </li> 
     <li id="li_066D90AB071941C3869EDAFCE981707A">Navigeren naar <span class="ignoretag"> <span class="uicontrol"> Beheerder </span>  &gt; <span class="uicontrol"> Alle beheerders </span>  &gt; <span class="uicontrol"> Gebruikersbeheer </span>  &gt; <span class="uicontrol"> Groepen </span>  &gt; <span class="uicontrol"> Alle rapporttoegang bewerken </span>  &gt; <span class="uicontrol"> Analysegereedschappen </span>  &gt; <span class="uicontrol"> Aanpassen </span>  &gt; <span class="uicontrol"> serveroproepgebruik </span> </span> </li> 
    </ol> </td> 
   <td colname="col4"> 
    <ol id="ol_518673ED323A4C5993A3B9F4BA09E405"> 
     <li id="li_56FF685A3B454ECEA5F16BB591A60034">Log in bij login.experiencecloud.adobe.com.</li> 
     <li id="li_FA1AE0F19DEF4AB2AA77B22CCA2995F9">Klikken <span class="uicontrol"> Analyse </span>. </li> 
     <li id="li_22A4CBB84B5A451780873BBE67E6E6EF">Navigeren naar <span class="ignoretag"> <span class="uicontrol"> Producten </span>  &gt; <span class="uicontrol"> Productprofiel </span>  &gt; <span class="uicontrol"> Machtigingen </span>  &gt; <span class="uicontrol"> Analysegereedschappen </span>  &gt; <span class="uicontrol"> serveroproepgebruik </span> </span> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>
