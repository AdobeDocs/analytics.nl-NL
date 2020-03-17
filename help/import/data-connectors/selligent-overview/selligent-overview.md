---
description: 'null'
title: Slimme gegevensconnector voor Adobe Analytics
uuid: e16c3ca6-b131-44b1-a36c-e39697677a96
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Slimme gegevensconnector voor Adobe Analytics{#selligent-data-connector-for-adobe-analytics}

Deze integratie omvat de volgende belangrijke voordelen:

* Consolideer e-mailmarketing en analysegegevens in één rapportinterface.
* Optimaliseer e-mailcampagnes door conversie en bijdrage aan inkomsten en succes van de site.
* Hermarkt voor belangrijke bezoekers en marktsegmenten op basis van dynamische marketingsegmenten.

## Dynamische marketingsegmenten {#section-a2216f3339304636bd5417249bd635a4}

Deze e-mailintegratie ondersteunt dynamische marketingsegmenten om uw bedrijf te stimuleren. Deze integratie kenmerkt de volgende marketing segmenten, uit de doos:

| Segment | Beschrijving |
|---|---|
| **Afstotingsprofiel voor illustraties** | Help bezoekers om te zetten in klanten via fijnafgestemde campagnes die speciaal zijn ontworpen voor mensen die aarzelen om winkelwagentjes te maken. |
| **Aankoopprofiel** | Herhalingsbestellingen en gemiddelde orderwaarde verhogen via campagnes die zijn bedoeld voor aankooppatronen van bezoekers. |
| **Gedragsprofiel van product-/inhoudsweergave** | Bereik potentiële klanten door marketing segmenten die op productmeningen en inhoud toegang profiling worden gebaseerd. |
| **Aangepaste remarketing-segmenten** | De klanten kunnen douane ook tot stand brengen en plannen hermarketing segmenten specifiek voor de behoeften van hun gebruikers. |

## Voordat u deze integratie activeert{#before-you-activate-this-integration}

Voordat u deze integratie activeert, moet u de volgende items controleren op uw implementatie van Adobe Analytics en uw e-mailsoftware.

Dit zorgt ervoor dat de juiste beste praktijken en voorwaarden aanwezig zijn voordat de activering plaatsvindt. Dit zal resulteren in een optimale en succesvolle integratie.

## Vereisten voor Adobe Analytics{#prerequisites-for-adobe-analytics}

Hier worden de vereiste acties weergegeven die moeten worden uitgevoerd in Adobe Analytics voordat u de integratie kunt implementeren.

| Vereiste | Notities |
|---|---|
| Rapportsuite selecteren | Houd er rekening mee dat deze integratie specifiek is voor rapporten. Zorg ervoor dat u de gewenste rapportsuite hebt geselecteerd voordat u de integratie activeert. |
| Analysevariabelen configureren | Voor deze integratie zijn aangepaste gebeurtenissen en aangepaste eVars en eventueel aanvullende gebeurtenissen en extra eVars vereist. Zie Analytische variabelen configureren voor Selectief. |
| Geautoriseerde vertegenwoordiger | Houd er rekening mee dat het inschakelen van deze integratie ertoe kan leiden dat uw bedrijf kosten aanrekent in overeenstemming met uw serviceovereenkomst met Adobe, Inc. of uw serviceovereenkomst met een van de vertrouwde partners van Adobe, al naargelang het geval. Door deze integratie te activeren, vertegenwoordigt u hierbij dat u een gemachtigde vertegenwoordiger van uw bedrijf bent; en als zodanig stemt uw bedrijf ermee in de eventuele kosten te betalen die in de hierboven beschreven serviceovereenkomst zijn vermeld. |
| Adobe Data Warehouse™ inschakelen | Deze integratie vereist het Pakhuis van Gegevens worden toegelaten om remarketing segmenten te produceren. Als u het Adobe Data Warehouse niet hebt ingeschakeld, neemt u contact op met Adobe voor meer informatie. |
| Ontvanger-id | De integratie vereist dat wij een &quot;Bezoeker ID&quot;binnen een variabele van de Analyse (eVar) vangen en opslaan. De bezoekersidentiteitskaart (die vaak als &quot;Ontvangersidentiteitskaart&quot;wordt bedoeld) is een gecodeerde of numerieke vertegenwoordiging van een e-mailadres van het Te kiezen systeem. Deze &quot;Ontvanger-id&quot; is gekoppeld aan het gedrag van een downstreambezoeker op de site (winkels, aankopen, enz.) die weer in het systeem van Selligent wordt opgenomen en voor hermarketingdoeleinden kan worden gebruikt. Als deel van het opstellingsproces, moet u eVar voor dit doel identificeren wanneer ertoe aangezet door de Tovenaar. |
| Extern bijhouden | Als u momenteel niet de beste praktijken van het toelaten van externe het volgen voor elke e-mailcampagne volgt u verzendt, moet u dit doen om een succesvolle integratie te verzekeren. Zie de sectie Selecteren hieronder voor meer informatie. |
| Privacynaleving | Als u de functie voor het bijhouden van de identiteit van de ontvanger of de bezoeker inschakelt, worden hiermee persoonlijke identificeerbare gegevens van uw sitebezoekers mogelijk bijgehouden. Dit heeft gevolgen voor de persoonlijke levenssfeer en vereist de implementatie van de juiste procedures door uw organisatie, zoals kennisgeving aan en toestemming van uw sitebezoekers. |

## Analysevariabelen configureren voor kiezen{#configure-analytics-variables-for-selligent}

Deze integratie vereist 2 eVars die voor elke implementatie van de rapportreeks worden gereserveerd.

Naast deze eVars kunnen enkele gebeurtenissen worden gereserveerd, afhankelijk van de gegevens van Selligent, die u in Analytics wilt zien. Deze gebeurtenissen en gebeurtenissen worden als volgt beschreven:

<table id="table_2FFB865DBD80412F90DA8E224B12FB62"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type variabele </th> 
   <th colname="col2" class="entry"> Naam variabele </th> 
   <th colname="col3" class="entry"> Hoe wordt het gebruikt </th> 
   <th colname="col4" class="entry"> Instellingen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Bericht-id </td> 
   <td colname="col3"> Om de individuele identificatie van de e-mailberichtcampagne te vangen. </td> 
   <td colname="col4"> <p><b>Status</b>: Ingeschakeld </p> <p><b>Toewijzing</b>: Recentste </p> <p><b>Verlopen na</b>: "Bedrijfsbesluit" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eV ar </td> 
   <td colname="col2"> Ontvanger-id </td> 
   <td colname="col3"> Om de anonieme identificatie voor uw klant te vangen die de e-mailcampagne klikte. </td> 
   <td colname="col4"> <p><b>Status</b>: Ingeschakeld </p> <p><b>Toewijzing</b>: Recentste </p> <p><b>Verlopen na</b>: "Bedrijfsbesluit" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Verzonden </td> 
   <td colname="col3"> Om het aantal e-mails op te slaan dat door Selligent is verzonden. </td> 
   <td colname="col4"> <p><b>Type</b>: Numeriek </p> <p><b>Deelname</b>: Ingeschakeld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Geleverd </td> 
   <td colname="col3"> Het aantal geleverde e-mails opslaan. </td> 
   <td colname="col4"> <p><b>Type</b>: Numeriek </p> <p><b>Deelname</b>: Ingeschakeld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Weergaven </td> 
   <td colname="col3"> Om het aantal unieke e-mails op te slaan dat is weergegeven. </td> 
   <td colname="col4"> <p><b>Type</b>: Numeriek </p> <p><b>Deelname</b>: Ingeschakeld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Klikken </td> 
   <td colname="col3"> Om het aantal keren op te slaan dat op een e-mail is geklikt. </td> 
   <td colname="col4"> <p><b>Type</b>: Numeriek </p> <p><b>Deelname</b>: Ingeschakeld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Afgekeerd </td> 
   <td colname="col3"> Het aantal teruggestuurde e-mails opslaan. </td> 
   <td colname="col4"> <p><b>Type</b>: Numeriek </p> <p><b>Deelname</b>: Ingeschakeld </p> </td> 
  </tr> 
 </tbody> 
</table>

## Vereisten voor selectie{#prerequisites-for-selligent}

Hiermee geeft u de vereiste informatie weer die u van uw account met de optie Selectief wilt ontvangen voordat u de integratie kunt implementeren.

**Geldige, betrouwbare account**

Als u deze integratie met gegevensconnectors wilt gebruiken, hebt u een geldig, slim account nodig.

**Accountinformatie**

Tijdens deze integratie-instelling hebt u de volgende informatie nodig over uw account met de optie &#39;SELECT&#39;:

* **URL** van Adobe-service:

   De URL kan worden afgeleid van de URL die wordt gebruikt om u aan te melden bij de oplossing voor het selecteren van marketing. Vervang het deel &quot;/simweb/login.aspx&quot; van de URL door &quot;/automation/omniture.asmx&quot;

   Bijvoorbeeld: `http://<client-specific install url>/automation/omniture.asmx`

* **Parameters queryreeks:** Deze worden toegevoegd in de bestemmingspagina URL voor Bericht ID en Ontvangersidentiteitskaart (Bezoeker ID). Dit zijn altijd MID en RID voor respectievelijk Bericht-ID en Ontvanger-ID.

* **Integratietoken** Start het hulpprogramma Manager vanuit Simweb en ga naar **[!UICONTROL Configuration]** > **[!UICONTROL System Settings]** > **[!UICONTROL General]** tab > **[!UICONTROL System]**. Onder **[!UICONTROL Security]**, kunt u het teken van de Integratie vinden.

   ![](assets/selligent-integration_token.png)
