---
description: Beschrijft de marketing efficiency die door de integratie wordt bereikt.
title: Lyris Data Connector voor Adobe Analytics
uuid: db213865-1296-4a93-a0a2-781c026b2be5
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Lyris Data Connector voor Adobe Analytics{#lyris-data-connector-for-adobe-analytics}

Beschrijft de marketing efficiency die door de integratie wordt bereikt.

De e-mailintegratie van Adobe® Data Connectors™ combineert gedragsinformatie van Adobe Analytics met de e-mailmarketing van Lyris om succesmeting en doelpubliek opnieuw te definiëren met meer relevante berichten.

Het leveren van relevante e-mailberichten aan deze marktsegmenten kan in volledig nieuwe opbrengstkansen resulteren, die tot verhoogde omzetting en opbrengst onder nieuwe en bestaande e-mailcampagnes leiden. Het leveren van relevante e-mailberichten op basis van producten die tijdens een bezoek zijn bekeken of producten die in een verlaten winkelwagentje zijn achtergelaten, heeft bijvoorbeeld een dramatische invloed op de inkomsten, met minimale gevolgen voor de kosten, omdat dit alleen maar leidt tot het benutten van bezoekers die uw site al krijgt.

Deze verhoging van de marketingefficiëntie is een van de belangrijkste voordelen van de integratie van Adobe Analytics met Lyris. Bovendien worden de e-mailgegevens door deze integratie zo vaak als u wilt automatisch gesynchroniseerd met de gegevens van Adobe Analytics voor closed-loop rapportage.

## Belangrijke voordelen en functies{#key-benefits-and-features}

Hierin worden de belangrijkste voordelen beschreven van de integratie van Lyris en Adobe Marketing Reports en Analytics.

De integratie van Lyris en Adobe Analytics biedt de volgende belangrijke voordelen:

* Consolideer e-mailmarketing en analysegegevens in één rapportinterface
* E-mailcampagnes optimaliseren door conversie en bijdrage aan inkomsten en succes van de site
* Hermarkt voor belangrijke bezoekers en marktsegmenten op basis van dynamische marketingsegmenten

### Dynamische marketingsegmenten

De e-mailintegratie steunt dynamische marketing segmenten om u te helpen uw zaken drijven. Deze integratie kenmerkt de volgende marketing segmenten, uit de doos:

* **Profiel** voor afschrijving van winkelwagentje: Bezoekers helpen zich om te zetten in klanten door middel van speciaal voor hen die aarzelen om winkelwagentjes te maken ontworpen, fijnafgestemde campagnes
* **Aankoopprofielen**: Herhalingsbestellingen en gemiddelde orderwaarde verhogen via campagnes die zijn bedoeld voor aankooppatronen van bezoekers
* **Gedragsprofiel** van product-/inhoudsweergave: Bereik potentiële klanten door marketing segmenten die op productmeningen en inhoud toegang profiling worden gebaseerd
* De klanten kunnen ook **douane re-marketing segmenten** tot stand brengen en plannen specifiek voor de behoeften van hun gebruikers.

## Integratievereisten{#integration-prerequisites}

Beschrijft de eerste vereisten voor een geslaagde integratie.

Voordat u deze integratie activeert, moet u de volgende items controleren op uw implementatie van Adobe Analytics en uw e-mailsoftware.

Dit zorgt ervoor dat de juiste beste praktijken en voorwaarden aanwezig zijn voordat de activering plaatsvindt, wat zal resulteren in een optimale en succesvolle integratie.

### Vereisten voor Adobe Analytics {#section-ddb9d4f3b283438ea33788f47f35e69a}

* **rapportsuite specifiek**: Houd er rekening mee dat deze integratie specifiek is voor rapporten. Zorg ervoor dat u de gewenste rapportsuite hebt geselecteerd voordat u de integratie activeert
* **Beschikbare en geconfigureerde analytische variabelen**: Voor deze integratie zijn aangepaste gebeurtenissen en aangepaste eVars en eventueel aanvullende gebeurtenissen en extra eVars vereist.

* **Geautoriseerde vertegenwoordiger**: Houd er rekening mee dat het inschakelen van deze integratie ertoe kan leiden dat uw bedrijf kosten aanrekent in overeenstemming met uw serviceovereenkomst met Adobe, Inc. of uw serviceovereenkomst met een van de vertrouwde partners van Adobe, al naargelang het geval. Door deze integratie te activeren, vertegenwoordigt u hierbij dat u een gemachtigde vertegenwoordiger van uw bedrijf bent; en als zodanig stemt uw bedrijf ermee in de eventuele kosten te betalen die in de hierboven beschreven serviceovereenkomst zijn vermeld.
* **Adobe Analytics-gegevenspakhuis**: Voor deze integratie moet Adobe Analytics-gegevenspakhuis zijn ingeschakeld om opnieuw op de markt gebrachte segmenten te genereren. Neem contact op met Adobe voor meer informatie als u het gegevensentrepot niet hebt ingeschakeld.
* **Ontvanger-id**: De integratie vereist dat wij een &quot;Bezoeker ID&quot;binnen een variabele van de Analyse (eVar) vangen en opslaan. De bezoeker-id (vaak de &quot;Ontvanger-id&quot; genoemd) is een gecodeerde of numerieke weergave van een e-mailadres van het Lyris-systeem. Deze &quot;Ontvanger-id&quot; is gekoppeld aan het gedrag van een downstreambezoeker op de site (winkels, aankopen, enz.) die weer in het Lyris-systeem wordt opgenomen en voor hermarketingdoeleinden kan worden gebruikt. Als deel van het opstellingsproces, moet u eVar voor dit doel identificeren wanneer ertoe aangezet door de Tovenaar.
* **Externe tracering**: Als u momenteel niet de beste praktijken van het toelaten van externe het volgen voor elke e-mailcampagne volgt u verzendt, moet u dit doen om een succesvolle integratie te verzekeren. Zie de sectie Lyris hieronder voor meer informatie
* **Privacy-compatibiliteit**: Als u de functie voor het bijhouden van de identiteit van de ontvanger of de bezoeker inschakelt, worden hiermee persoonlijke identificeerbare gegevens van uw sitebezoekers mogelijk bijgehouden. Dit heeft gevolgen voor de privacy en vereist de implementatie van de juiste procedures door uw organisatie, zoals kennisgeving aan en toestemming van uw sitebezoekers.

### Vereisten voor Lyris EmailLabs {#section-84abae9401224a3699fed861f715ebde}

* **Geldige Lyris-account**: Als u deze integratie van de gegevensconnector wilt gebruiken, hebt u een geldig Lyris-account nodig.
* **Accountinformatie**: Tijdens deze integratie-installatie hebt u de volgende informatie over uw Lyris-account nodig:

   * *Lyris API-sleutel*: Gebruikt voor gegevenspopulatie
   * *Parameters* queryreeks: Deze worden toegevoegd in de bestemmingspagina URL voor Bericht ID en Ontvangersidentiteitskaart (Bezoeker ID).
   * *Lyris Server/URL*: De serverwaarde die u gebruikt in het Lyris-systeem
   * *Site-ID* van Lyris: Dit is de unieke waarde voor uw exemplaar van Lyris HQ, ook wel &quot;Customer ID&quot; genoemd. U vindt deze informatie onder &quot;Klantgegevens&quot; in het gedeelte &quot;Account Home&quot; van e-maillabs.

## Adobe Analytics-variabelen voor Lyris configureren{#configure-adobe-analytics-variables-for-lyris}

Beschrijft eVars en Gebeurtenissen die voor elke implementatie van de rapportreeks moeten worden gereserveerd.

Deze integratie vereist minstens twee eVars die voor elke implementatie van de rapportreeks worden gereserveerd. Naast deze eVars kunnen enkele gebeurtenissen worden gereserveerd, afhankelijk van de Lyris-gegevens die u in Analytics wilt zien. Deze gebeurtenissen en gebeurtenissen worden in de onderstaande tabel beschreven:

<table id="table_43E32344E9E54FED8491F28047249329"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type variabele </th> 
   <th colname="col2" class="entry"> Naam variabele </th> 
   <th colname="col3" class="entry"> Hoe de variabele wordt gebruikt </th> 
   <th colname="col4" class="entry"> Instellingen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Bericht-id </td> 
   <td colname="col3"> De identificatie van de campagne voor afzonderlijke e-mailberichten vastleggen </td> 
   <td colname="col4"> <p>Status: Ingeschakeld </p> <p>Toewijzing: Recentste </p> <p>Verlopen na: "Bedrijfsbesluit" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> E-mailontvanger-id </td> 
   <td colname="col3"> Om de anonieme identificatie voor uw klant te vangen die de e-mailcampagne klikte </td> 
   <td colname="col4"> <p>Status: Ingeschakeld </p> <p>Toewijzing: Recentste </p> <p>Verlopen na: "Bedrijfsbesluit" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Lyris - Verzonden e-mails </td> 
   <td colname="col3"> Nee opslaan. van e-mails verzonden door Lyris </td> 
   <td colname="col4">Type: Numeriek <p>Deelname: Ingeschakeld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Lyris - E-mails geopend </td> 
   <td colname="col3"> Nee opslaan. van e-mails die zijn geopend </td> 
   <td colname="col4">Type: Numeriek <p>Deelname: Ingeschakeld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Lyris - Unieke e-mails geopend </td> 
   <td colname="col3"> Nee opslaan. van unieke e-mails die zijn geopend </td> 
   <td colname="col4">Type: Numeriek <p>Deelname: Ingeschakeld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Lyris - E-mail klikcontroles </td> 
   <td colname="col3"> Nee opslaan. van keer dat er op een e-mail is geklikt </td> 
   <td colname="col4">Type: Numeriek <p>Deelname: Ingeschakeld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Lyris - E-mailgrenzen </td> 
   <td colname="col3"> Het nummer opslaan. van e-mails die zijn teruggestuurd </td> 
   <td colname="col4">Type: Numeriek <p>Deelname: Ingeschakeld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenis </td> 
   <td colname="col2"> Lyris - E-mailabonnementen opzeggen </td> 
   <td colname="col3"> Het nummer opslaan. van e-mailabonnementen die zijn uitgeschakeld </td> 
   <td colname="col4">Type: Numeriek <p>Deelname: Ingeschakeld </p> </td> 
  </tr> 
 </tbody> 
</table>
