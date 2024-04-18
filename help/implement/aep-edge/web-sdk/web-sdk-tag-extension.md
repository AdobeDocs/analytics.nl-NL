---
title: Gegevens naar Adobe Analytics verzenden met de Web SDK-tagextensie
description: Begin met een schone implementatie van de Gegevensinzameling van Adobe Experience Platform om gegevens naar Adobe Analytics te verzenden gebruikend XDM en de het gebiedsgroep van Adobe Analytics ExperienceEvent.
exl-id: 235b3d68-92dd-4ca4-8889-1e1f2d83f47e
source-git-commit: 316ca1074de36db0d7c9545691e7c6d72a2ed2c4
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 0%

---

# Gegevens naar Adobe Analytics verzenden met de Web SDK-tagextensie

Dit implementatiepad omvat een nieuwe Web SDK-installatie met tags in Adobe Experience Platform Data Collection. Andere implementatiepaden worden op afzonderlijke pagina&#39;s behandeld:

* [Web SDK JavaScript-bibliotheek](web-sdk-javascript-library.md): Een nieuwe Web SDK-installatie met de Web SDK JavaScript-bibliotheek (`alloy.js`). Gelijkaardig aan de de marktextensiebenadering van SDK van het Web (deze pagina), behalve beheert u de implementatie zelf in plaats van het gebruiken van de markeringen UI. Hiervoor is de Adobe Analytics ExperienceEvent-veldgroep vereist, die typische analytische variabelen bevat die in uw XDM-schema moeten worden opgenomen.
* [De uitbreiding van de Analyse aan de uitbreiding van SDK van het Web](analytics-extension-to-web-sdk.md): Kies een vloeiende en methodische aanpak om van de Adobe Analytics-tagextensie over te schakelen op de Web SDK-tagextensie. Deze benadering onderdrukt de behoefte om XDM te gebruiken tot uw organisatie klaar is om de diensten van Adobe Experience Platform, zoals Customer Journey Analytics te gebruiken. Gebruik de `data` object in plaats van het `xdm` -object om gegevens naar de Adobe te verzenden.
* [AppMeasurement naar Web SDK JavaScript-bibliotheek](appmeasurement-to-web-sdk.md): Een vloeiende en methodische aanpak voor het migreren naar de SDK van het Web, behalve dat er geen tags worden gebruikt. In plaats daarvan verwijdert u handmatig de Adobe Analytics-bibliotheek voor gegevensverzameling (`AppMeasurement.js`) en deze vervangen door de Web SDK JavaScript-bibliotheek (`alloy.js`).

## Voordelen en nadelen van dit implementatiepad

Het gebruiken van de uitbreiding van SDK van het Web om gegevens naar Adobe Analytics te verzenden heeft zowel voordelen als nadelen. Let zorgvuldig op elke optie om te bepalen welke benadering het beste is voor uw organisatie.

| Voordelen | Nadelen |
| --- | --- |
| <ul><li>**Meest directe benadering**: Dit implementatiepad is het meest ongecompliceerde en doorgaans het aanbevolen pad voor nieuwe Web SDK-implementaties. Als u geen huidige implementatie van Adobe Analytics om zich over ongerust te maken hebt, bevolk de toepasselijke gebieden van SDK van het Web XDM.</li><li>**Vooraf gedefinieerd schema**: Als uw organisatie geen behoefte aan uw eigen schema heeft, kunt u eenvoudig het schema gebruiken dat aan Adobe Analytics wordt gericht. Dit concept is zelfs van toepassing als u naar Customer Journey Analytics gaat. Het concept &#39;props&#39; en &#39;eVars&#39; zijn niet van toepassing op Customer Journey Analytics, maar u kunt &#39;props&#39; en &#39;eVars&#39; blijven gebruiken als eenvoudige aangepaste afmetingen.</li><li>**Tags beheren zonder tussenkomst van de ontwikkelaar**: Met labels kunt u uw implementatie beheren zonder dat ontwikkelaars hoeven aan te vragen dat ze code wijzigen in uw implementatie. Uw ontwikkelaars installeren het lader-script voor tags en u hebt volledige controle over de manier waarop gegevens worden verzameld.</li></ul> | <ul><li>**Vergrendeld in een specifiek schema**: Wanneer uw organisatie naar Customer Journey Analytics gaat, moet u het Adobe Analytics-schema blijven gebruiken of naar het schema van uw eigen organisatie migreren (wat een aparte gegevensset zou zijn). Als uw organisatie zowel het Adobe Analytics-schema als de migratie naar een aparte gegevensset bij de overgang naar de Customer Journey Analytics wil vermijden, raadt Adobe een van de volgende twee methoden aan:<ul><li>Gebruik de `data` object: Het `data` kunt u gegevens naar Adobe Analytics verzenden zonder aan een XDM-schema te voldoen. Zodra het schema van uw organisatie wordt gecreeerd, kunt u gegevenstoewijzing aan kaart gebruiken `data` objectvelden naar XDM. Beide [De uitbreiding van de Analyse aan de uitbreiding van SDK van het Web](analytics-extension-to-web-sdk.md) en [AppMeasurement naar Web SDK JavaScript-bibliotheek](appmeasurement-to-web-sdk.md) gebruiken `data` object.</li><li>Adobe Analytics volledig overslaan: als u de SDK van het Web implementeert, kunt u die gegevens naar een dataset in Adobe Experience Platform verzenden voor gebruik in Customer Journey Analytics. U kunt elk schema gebruiken dat u bevalt. Adobe Analytics is helemaal niet betrokken bij deze workflow en vereist daarom niet de Adobe Analytics ExperienceEvent-veldgroep. Deze methode leidt tot het minste bedrag aan technische schulden, maar laat Adobe Analytics ook volledig buiten beeld.</li></ul></ul> |

>[!IMPORTANT]
>
>Deze implementatiemethode vereist dat u een schema gebruikt dat voor Adobe Analytics is geconfigureerd. Als uw organisatie van plan is om uw eigen schema met Customer Journey Analytics in de toekomst te gebruiken, kan het gebruik van het schema van Adobe Analytics tot verwarring voor gegevensbeheerders of architecten leiden. Er zijn verschillende opties om dit probleem op te lossen:
>
>* U kunt het Adobe Analytics-schema in CJA gebruiken. Merk op dat CJA geen concept van steunen of eVars heeft; zij worden behandeld zoals een ander schemagebied. Houd er ook rekening mee dat het gebruik van het Adobe Analytics-schema in CJA het gebruik van andere platformservices, zoals Adobe Journey Optimizer of Real-time Customer Data Platform, kan bemoeilijken.
>* U kunt het gegevensobject gebruiken, net als een migratieworkflow. Merk op dat het gebruik van het gegevensvoorwerp vereist dat u elk gegevensobjecten gebied aan een XDM schemagebied in kaart brengt.
>* U kunt de Adobe Analytics-implementatie volledig overslaan en gegevens naar Adobe Experience Platform verzenden met uw eigen schema. Deze benadering is ideaal op lange termijn, en staat uw organisatie toe om Customer Journey Analytics te beginnen gebruiken.

## Stappen vereist om de de marktextensie van SDK van het Web uit te voeren

Een overzicht op hoog niveau van de uitvoeringstaken:

![Hoe te om Adobe Analytics uit te voeren gebruikend de uitbreidingswerkschema van SDK van het Web, zoals die in deze sectie wordt beschreven.](../../assets/websdk-extension-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Taak</b></th><th style="width:35%"><b>Meer informatie</b></th>
</tr>

<tr>
<td>1</td>
<td>Zorg ervoor dat u <b>een rapportsuite gedefinieerd</b>.</td>
<td><a href="/help/admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Installatieschema's</b>. Om gegevensinzameling voor gebruik over toepassingen te standaardiseren die hefboomwerking Adobe Experience Platform, heeft de Adobe de open en openbaar gedocumenteerde norm, het Model van de Gegevens van de Ervaring (XDM) gecreeerd.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html">Overzicht van de interface Schemas</a></td>
</tr>

<tr>
<td>3</td>
<td><b>Een gegevenslaag maken</b> om het bijhouden van de gegevens op uw website te beheren.</td>
<td><a href="../../prepare/data-layer.md">Een gegevenslaag maken</a></td>
</tr>

<tr>
<td>4</td>
<td><b>Een gegevensstroom configureren</b>. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web SDK van Adobe Experience Platform.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html">Een gegevensstroom configureren<a></td> 
</tr>

<tr>
<td>5</td> 
<td><b>Een Adobe Analytics-service toevoegen</b> naar uw gegevensstroom. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden en naar welke rapportsuite(s) specifiek.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html#analytics">Adobe Analytics-service toevoegen aan een gegevensstroom</a></td>
</tr>

<tr>
<td>6</td>
<td><b>Een tag-eigenschap maken</b>. Eigenschappen zijn overkoepelende containers die worden gebruikt om te verwijzen naar tagbeheergegevens.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-web">Een eigenschap voor tags maken of configureren voor het web</a></td>
</tr>

<tr>
<td>7</td> 
<td><b>De Web SDK-extensie installeren en configureren</b> in uw eigenschap tag. Vorm de uitbreiding van SDK van het Web om gegevens naar de datastream te verzenden die in stap 4 wordt gevormd.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html">Overzicht van Adobe Experience Platform Web SDK-extensie</a></td>
</tr>

<tr>
<td>8</td>
<td><b>Interfereren, valideren en publiceren</b> aan de productie. Sluit code in om de eigenschap tag op te nemen in de websitepagina's. Dan gebruik gegevenselementen, regels, etc., om uw implementatie aan te passen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html#embed-code">Code insluiten</a><br/><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html">Overzicht van publicatie</a></td>
</tr>

</table>
