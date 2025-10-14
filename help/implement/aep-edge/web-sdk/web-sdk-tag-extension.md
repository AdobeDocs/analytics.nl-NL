---
title: Gegevens naar Adobe Analytics verzenden met de webtagextensie SDK
description: Begin met een schone implementatie van de Gegevensinzameling van Adobe Experience Platform om gegevens naar Adobe Analytics te verzenden gebruikend XDM en de het gebiedsgroep van Adobe Analytics ExperienceEvent.
exl-id: 235b3d68-92dd-4ca4-8889-1e1f2d83f47e
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 0%

---

# Gegevens naar Adobe Analytics verzenden met de webtagextensie SDK

Dit implementatiepad omvat een nieuwe Web SDK-installatie met tags in Adobe Experience Platform Data Collection. Andere implementatiepaden worden op afzonderlijke pagina&#39;s behandeld:

* [&#x200B; de bibliotheek van JavaScript van SDK van het Web &#x200B;](web-sdk-javascript-library.md): Een verse installatie van SDK van het Web die de bibliotheek van JavaScript van SDK van het Web (`alloy.js`) gebruikt. Vergelijkbaar met de Web SDK-aanpak voor het extenderen van tags (deze pagina), behalve dat u de implementatie zelf beheert in plaats van de gebruikersinterface voor tags te gebruiken. Hiervoor is de Adobe Analytics ExperienceEvent-veldgroep vereist, die typische analytische variabelen bevat die in uw XDM-schema moeten worden opgenomen.
* [&#x200B; uitbreiding Analytics aan de uitbreiding van SDK van het Web &#x200B;](analytics-extension-to-web-sdk.md): Neem een vlotte en methodische benadering om zich van de de markeringsuitbreiding van Adobe Analytics aan de de markeringsuitbreiding van SDK van het Web te bewegen. Deze benadering onderdrukt de behoefte om XDM te gebruiken tot uw organisatie klaar is om de diensten van Adobe Experience Platform, zoals Customer Journey Analytics te gebruiken. Gebruik het object `data` in plaats van het object `xdm` om gegevens naar Adobe te verzenden.
* [&#x200B; AppMeasurement aan de bibliotheek van JavaScript van het Web SDK &#x200B;](appmeasurement-to-web-sdk.md): Een vlotte en methodische benadering om aan het Web SDK te migreren, behalve het gebruikt geen markeringen. In plaats daarvan verwijdert u handmatig de Adobe Analytics-bibliotheek voor gegevensverzameling (`AppMeasurement.js`) en vervangt u deze door de SDK JavaScript-bibliotheek van het Web (`alloy.js` ).

## Voordelen en nadelen van dit implementatiepad

Het gebruik van de extensie Web SDK voor het verzenden van gegevens naar Adobe Analytics heeft zowel voor- als nadelen. Let zorgvuldig op elke optie om te bepalen welke benadering het beste is voor uw organisatie.

| Voordelen | Nadelen |
| --- | --- |
| <ul><li>**Meest directe benadering**: Deze implementatieweg is de meest ongecompliceerde en typisch de geadviseerde weg voor nieuwe implementaties van SDK van het Web. Als u geen huidige Adobe Analytics-implementatie hebt om u zorgen over te maken, vult u de toepasselijke Web SDK XDM-velden in.</li><li>**vooraf bepaald schema**: Als uw organisatie geen behoefte aan uw eigen schema heeft, kunt u eenvoudig het schema gebruiken dat op Adobe Analytics wordt gericht. Dit concept geldt ook als u naar Customer Journey Analytics gaat. Het concept &#39;props en &#39;eVars&#39; is niet van toepassing op Customer Journey Analytics, maar u kunt &#39;props&#39; en &#39;eVars&#39; blijven gebruiken als eenvoudige aangepaste afmetingen.</li><li>**beheert markeringen zonder ontwikkelaarsinterventie**: De markeringen staan u toe om uw implementatie te beheren zonder het verzoeken dat de ontwikkelaars codeveranderingen in uw implementatie aanbrengen. Uw ontwikkelaars installeren het lader-script voor tags en u hebt volledige controle over de manier waarop gegevens worden verzameld.</li></ul> | <ul><li>**Vergrendeld in het gebruiken van een specifiek schema**: Wanneer uw organisatie zich aan Customer Journey Analytics beweegt, moet u verkiezen om verder te gebruiken het schema van Adobe Analytics, of aan het schema van uw eigen organisatie (dat een afzonderlijke gegevensreeks zou zijn) te migreren. Als uw organisatie zowel het Adobe Analytics-schema als de migratie naar een aparte gegevensset wil vermijden bij de overgang naar Customer Journey Analytics, raadt Adobe een van de volgende twee methoden aan:<ul><li>Gebruik het object `data` : met het object `data` kunt u gegevens naar Adobe Analytics verzenden zonder dat u zich aan een XDM-schema houdt. Nadat u het schema van uw organisatie hebt gemaakt, kunt u gegevensstroomtoewijzing gebruiken om `data` -objectvelden toe te wijzen aan XDM. Zowel gebruiken de [&#x200B; uitbreiding van Analytics aan de uitbreiding van SDK van het Web &#x200B;](analytics-extension-to-web-sdk.md) en [&#x200B; AppMeasurement aan de bibliotheek van JavaScript van het Web &#x200B;](appmeasurement-to-web-sdk.md) dit `data` voorwerp.</li><li>Adobe Analytics volledig overslaan: als u de Web SDK implementeert, kunt u die gegevens naar een dataset in Adobe Experience Platform verzenden voor gebruik in Customer Journey Analytics. U kunt elk schema gebruiken dat u bevalt. Adobe Analytics is helemaal niet betrokken bij deze workflow en vereist daarom niet de Adobe Analytics ExperienceEvent-veldgroep. Deze methode leidt tot het minste bedrag aan technische schulden, maar laat Adobe Analytics ook volledig buiten beeld.</li></ul></ul> |

>[!IMPORTANT]
>
>Deze implementatiemethode vereist dat u een schema gebruikt dat voor Adobe Analytics is geconfigureerd. Als uw organisatie van plan is in de toekomst uw eigen schema met Customer Journey Analytics te gebruiken, kan het gebruik van het Adobe Analytics-schema leiden tot verwarring bij gegevensbeheerders of architecten. Er zijn verschillende opties om dit probleem op te lossen:
>
>* U kunt het Adobe Analytics-schema in CJA gebruiken. Merk op dat CJA geen concept van steunen of eVars heeft; zij worden behandeld zoals een ander schemagebied. Houd er ook rekening mee dat het gebruik van het Adobe Analytics-schema in CJA het gebruik van andere platformservices, zoals Adobe Journey Optimizer of Real-Time Customer Data Platform, kan bemoeilijken.
>* U kunt het gegevensobject gebruiken, net als een migratieworkflow. Merk op dat het gebruik van het gegevensvoorwerp vereist dat u elk gegevensobjecten gebied aan een XDM schemagebied in kaart brengt.
>* U kunt de Adobe Analytics-implementatie volledig overslaan en gegevens naar Adobe Experience Platform verzenden met uw eigen schema. Deze aanpak is ideaal voor de lange termijn en stelt uw organisatie in staat om Customer Journey Analytics te gaan gebruiken.

## Stappen die nodig zijn voor het implementeren van de Web SDK-tagextensie

Een overzicht op hoog niveau van de uitvoeringstaken:

![&#x200B; hoe te om Adobe Analytics uit te voeren gebruikend het de uitbreidingswerkschema van SDK van het Web, zoals die in deze sectie wordt beschreven.](../../assets/websdk-extension-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Taak</b></th><th style="width:35%"><b>Meer informatie</b></th>
</tr>

<tr>
<td>1</td>
<td>Verzeker u <b> een rapportreeks </b> hebt bepaald.</td>
<td><a href="/help/admin/tools/manage-rs/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b> schema's van de Opstelling </b>. Om gegevensinzameling voor gebruik over toepassingen te standaardiseren die hefboomwerking Adobe Experience Platform, heeft Adobe de open en openbaar gedocumenteerde norm, het Model van de Gegevens van de Ervaring (XDM) gecreeerd.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=nl-NL">Overzicht van de interface Schemas</a></td>
</tr>

<tr>
<td>3</td>
<td><b> creeer een gegevenslaag </b> om het volgen van de gegevens op uw website te beheren.</td>
<td><a href="../../prepare/data-layer.md">Een gegevenslaag maken</a></td>
</tr>

<tr>
<td>4</td>
<td><b> vorm een datastream </b>. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web SDK van Adobe Experience Platform.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=nl-NL">Een gegevensstroom configureren<a></td> 
</tr>

<tr>
<td>5</td> 
<td><b> voeg de dienst van Adobe Analytics </b> aan uw datastream toe. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden en naar welke rapportsuite(s) specifiek.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=nl-NL#analytics">Adobe Analytics-service toevoegen aan een gegevensstroom</a></td>
</tr>

<tr>
<td>6</td>
<td><b> creeer een markeringsbezit </b>. Eigenschappen zijn overkoepelende containers die worden gebruikt om te verwijzen naar tagbeheergegevens.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=nl-NL#for-web">Een eigenschap voor tags maken of configureren voor het web</a></td>
</tr>

<tr>
<td>7</td> 
<td><b> installeer en vorm de uitbreiding van SDK van het Web </b> in uw markeringsbezit. Vorm de uitbreiding van SDK van het Web om gegevens naar de datastream te verzenden die in stap 4 wordt gevormd.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html?lang=nl-NL">Adobe Experience Platform Web SDK-extensie - overzicht</a></td>
</tr>

<tr>
<td>8</td>
<td><b> bevestig, bevestig, en publiceer </b> aan productie. Sluit code in om de eigenschap tag op te nemen in de websitepagina's. Dan gebruik gegevenselementen, regels, etc., om uw implementatie aan te passen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?lang=nl-NL#embed-code"> bed code </a><br/> <a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=nl-NL"> het Publiceren overzicht </a> in</td>
</tr>

</table>
