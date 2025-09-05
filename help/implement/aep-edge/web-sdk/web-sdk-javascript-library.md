---
title: Gegevens naar Adobe Analytics verzenden met de Web SDK JavaScript-bibliotheek
description: Start met een schone SDK-implementatie voor het web om gegevens naar Adobe Analytics te verzenden met de JavaScript-bibliotheek.
exl-id: 593b63ac-e411-4f88-af7e-78f026269ec0
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 0%

---

# Gegevens naar Adobe Analytics verzenden met de Web SDK JavaScript-bibliotheek

Dit implementatiepad omvat een nieuwe Web SDK-installatie met behulp van de Web SDK JavaScript-bibliotheek. Andere implementatiepaden worden op afzonderlijke pagina&#39;s behandeld:

* [ de markeringsuitbreiding van SDK van het Web ](web-sdk-tag-extension.md): Een nieuwe installatie van SDK van het Web die de de markeringsuitbreiding van SDK van het Web gebruikt. Vergelijkbaar met de Web SDK JavaScript-bibliotheekaanpak (deze pagina), behalve dat u de implementatie beheert met tags in Adobe Experience Platform Data Collection. Hiervoor is de Adobe Analytics ExperienceEvent-veldgroep vereist, die typische analytische variabelen bevat die in uw XDM-schema moeten worden opgenomen.
* [ uitbreiding Analytics aan de uitbreiding van SDK van het Web ](analytics-extension-to-web-sdk.md): Neem een vlotte en methodische benadering om zich van de de markeringsuitbreiding van Adobe Analytics aan de de markeringsuitbreiding van SDK van het Web te bewegen. Deze benadering onderdrukt de behoefte om XDM te gebruiken tot uw organisatie klaar is om de diensten van Adobe Experience Platform, zoals Customer Journey Analytics te gebruiken. Gebruik het object `data` in plaats van het object `xdm` om gegevens naar Adobe te verzenden.
* [ AppMeasurement aan de bibliotheek van JavaScript van het Web SDK ](appmeasurement-to-web-sdk.md): Een vlotte en methodische benadering om aan het Web SDK te migreren, behalve het gebruikt geen markeringen. In plaats daarvan, kunt u de bibliotheek van de de gegevensinzameling van Adobe Analytics (`AppMeasurement.js`) manueel verwijderen en het vervangen met de bibliotheek van JavaScript van het Web (`alloy.js`).

## Voordelen en nadelen van dit implementatiepad

Het gebruik van de Web SDK JavaScript-bibliotheek voor het verzenden van gegevens naar Adobe Analytics heeft zowel voor- als nadelen. Let zorgvuldig op elke optie om te bepalen welke benadering het beste is voor uw organisatie.

| Voordelen | Nadelen |
| --- | --- |
| <ul><li>**Directe benadering**: Deze implementatieweg is helderder dan benaderingen die bestaande implementaties van Adobe Analytics bewegen. Als u geen huidige Adobe Analytics-implementatie hebt om u zorgen over te maken, vult u de toepasselijke Web SDK XDM-velden in.</li><li>**vooraf bepaald schema**: Als uw organisatie geen behoefte aan uw eigen schema heeft, kunt u eenvoudig het schema gebruiken dat op Adobe Analytics wordt gericht. Dit concept geldt ook als u naar Customer Journey Analytics gaat. Het concept &#39;props en &#39;eVars&#39; is niet van toepassing op Customer Journey Analytics, maar u kunt &#39;props&#39; en &#39;eVars&#39; blijven gebruiken als eenvoudige aangepaste afmetingen.</li></ul> | <ul><li>**de veranderingen van de Implementatie vereisen ontwikkelaarinterventie**: Als u veranderingen in uw implementatie van SDK van het Web wilt aanbrengen, moet u met uw ontwikkelingsteam werken om de code op uw plaats uit te geven. De benadering die de [ de markeringsuitbreiding van SDK van het Web ](web-sdk-tag-extension.md) gebruikt vermijdt dit nadeel.</li><li>**Vergrendeld in het gebruiken van een specifiek schema**: Wanneer uw organisatie zich aan Customer Journey Analytics beweegt, moet u verkiezen om verder te gebruiken het schema van Adobe Analytics, of aan het schema van uw eigen organisatie (dat een afzonderlijke gegevensreeks zou zijn) te migreren. Als uw organisatie zowel het Adobe Analytics-schema als de migratie naar een aparte gegevensset wil vermijden bij de overgang naar Customer Journey Analytics, raadt Adobe een van de volgende twee methoden aan:</li><ul><li>Gebruik het object `data` : met het object `data` kunt u gegevens naar Adobe Analytics verzenden zonder dat u zich aan een XDM-schema houdt. Nadat u het schema van uw organisatie hebt gemaakt, kunt u gegevensstroomtoewijzing gebruiken om `data` -objectvelden toe te wijzen aan XDM. Zowel gebruiken de [ uitbreiding van Analytics aan de uitbreiding van SDK van het Web ](analytics-extension-to-web-sdk.md) en [ AppMeasurement aan de bibliotheek van JavaScript van het Web ](appmeasurement-to-web-sdk.md) dit `data` voorwerp.</li><li>Adobe Analytics volledig overslaan: als u de Web SDK implementeert, kunt u die gegevens naar een dataset in Adobe Experience Platform verzenden voor gebruik in Customer Journey Analytics. U kunt elk schema gebruiken dat u bevalt. Adobe Analytics is helemaal niet betrokken bij deze workflow en vereist daarom niet de Adobe Analytics ExperienceEvent-veldgroep. Deze methode leidt tot het minste bedrag aan technische schulden, maar laat Adobe Analytics ook volledig buiten beeld.</li></ul></ul> |

>[!IMPORTANT]
>
>Deze implementatiemethode vereist dat u een schema gebruikt dat voor Adobe Analytics is geconfigureerd. Als uw organisatie van plan is in de toekomst uw eigen schema met Customer Journey Analytics te gebruiken, kan het gebruik van het Adobe Analytics-schema leiden tot verwarring bij gegevensbeheerders of architecten. Er zijn verschillende opties om dit probleem op te lossen:
>
>* U kunt het Adobe Analytics-schema in CJA gebruiken. Merk op dat CJA geen concept van steunen of eVars heeft; zij worden behandeld zoals een ander schemagebied. Houd er ook rekening mee dat het gebruik van het Adobe Analytics-schema in CJA het gebruik van andere platformservices, zoals Adobe Journey Optimizer of Real-Time Customer Data Platform, kan bemoeilijken.
>* U kunt het gegevensobject gebruiken, net als een migratieworkflow. Merk op dat het gebruik van het gegevensvoorwerp vereist dat u elk gegevensobjecten gebied aan een XDM schemagebied in kaart brengt.
>* U kunt de Adobe Analytics-implementatie volledig overslaan en gegevens naar Adobe Experience Platform verzenden met uw eigen schema. Deze aanpak is ideaal voor de lange termijn en stelt uw organisatie in staat om Customer Journey Analytics te gaan gebruiken.

## Stappen vereist voor implementatie van de Web SDK JavaScript-bibliotheek

Een overzicht op hoog niveau van de uitvoeringstaken:

![ hoe te om Adobe Analytics uit te voeren gebruikend het werkschema van SDK van het Web, zoals die in deze sectie wordt beschreven.](../../assets/websdk-annotated.png)

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
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html">Overzicht van de interface Schemas</a></td>
</tr>

<tr>
<td>3</td>
<td><b> creeer een gegevenslaag </b> om het volgen van de gegevens op uw website te beheren.</td>
<td><a href="../../prepare/data-layer.md">Een gegevenslaag maken</a></td>
</tr>

<tr>
<td> 4</td>
<td><b> installeer de prebuilt standalone versie </b>. U kunt de bibliotheek (<code>alloy.js</code>) op CDN direct op uw pagina van verwijzingen voorzien of het downloaden en ontvangen op uw eigen infrastructuur. U kunt ook het NPM-pakket gebruiken.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/install/library.html"> Installerend de prebuilt standalone versie </a> en <a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/install/npm.html"> Gebruikend het pakket NPM </a></td>
</tr>

<tr>
<td>5</td>
<td><b> vorm een datastream </b>. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web SDK van Adobe Experience Platform.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html">Een gegevensstroom configureren<a></td> 
</tr>

<td>6</td>
<td><b> voeg de dienst van Adobe Analytics </b> aan uw datastream toe. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden en naar welke rapportsuite(s) specifiek.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html#analytics">Adobe Analytics-service toevoegen aan een gegevensstroom</a></td>
</tr>

<tr>
<td>7</td>
<td><b> vorm SDK van het Web </b>. Zorg ervoor dat de bibliotheek die u in stap 4 hebt geïnstalleerd, correct is geconfigureerd met de gegevensstroom-id (voorheen bekend als edge configuration id (<code>datastreamId</code>), organisatie-id (<code>orgId</code> ) en andere beschikbare opties. Zorgen voor juiste toewijzing van variabelen. </td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/commands/configure/overview.html"> vorm het Web SDK </a><br/> <a href="../xdm-var-mapping.md"> XDM objecten veranderlijke afbeelding </a></td>
</tr>

<tr>
<td>8</td>
<td><b> voert bevelen </b> en/of <b> spoorgebeurtenissen </b> uit. Nadat de basiscode op uw webpagina is geïmplementeerd, kunt u beginnen met het uitvoeren van opdrachten en het volgen van gebeurtenissen met de SDK.
</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/commands/sendevent/overview.html">Gebeurtenissen verzenden</a></td>
</tr>

<tr>
<td>9</td><td><b> breidt en bevestigt uw implementatie </b> uit alvorens het uit aan productie te duwen.</td><td></td> 
</tr>
</table>
