---
title: Adobe Analytics implementeren met de Adobe Experience Platform Web SDK
description: Gebruik de uitbreiding van SDK van het Web in de Inzameling van Gegevens van Adobe Experience Platform om gegevens naar Adobe Analytics te verzenden.
source-git-commit: 97bff355a5d9bb737d510221b63ba1321aaf5812
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 5%

---

# Adobe Analytics implementeren met de Adobe Experience Platform Web SDK

U kunt de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html) om gegevens naar Adobe Analytics te verzenden. Deze implementatiemethode werkt door de [Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) in een indeling die wordt gebruikt door Analytics.

U kunt gegevens naar de Rand van de Ervaring direct verzenden gebruikend het Web SDK, of door de uitbreiding van SDK van het Web in Markeringen.

## Web SDK

Een overzicht op hoog niveau van de uitvoeringstaken:

![Adobe Analytics implementeren met Web SDK-workflow](../../assets/websdk-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Taak</b></th><th style="width:35%"><b>Meer informatie</b></th>
</tr>

<tr>
<td>1</td>
<td>Zorg ervoor dat u <b>een rapportsuite gedefinieerd</b>.</td>
<td><a href="../../../admin/admin/c-manage-report-suites/report-suites-admin.md">Rapportsuitebeheer</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Installatieschema's en gegevenssets</b>. Om gegevensinzameling voor gebruik over toepassingen te standaardiseren die hefboomwerking Adobe Experience Platform, heeft Adobe de open en openbaar gedocumenteerde norm, het Model van de Gegevens van de Ervaring (XDM) gecreeerd.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en">Overzicht van schema's</a> en <a href="https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en">Overzicht van de gebruikersinterface voor gegevensbestanden</a></td>
</tr>

<tr>
<td>3</td>
<td><b>Een gegevenslaag maken</b> om het bijhouden van de gegevens op uw website te beheren.</td>
<td><a href="../../prepare/data-layer.md">Een datalaag maken</a></td>
</tr>

<tr>
<td> 4</td>
<td><b>De vooraf gebouwde zelfstandige versie installeren</b>. U kunt verwijzen naar de bibliotheek (<code>alloy.js</code>) rechtstreeks op de CDN op de pagina of download en host deze op uw eigen infrastructuur. U kunt ook het NPM-pakket gebruiken.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-2%3A-installing-the-prebuilt-standalone-version">De vooraf gebouwde zelfstandige versie installeren</a> en <a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-3%3A-using-the-npm-package">Het NPM-pakket gebruiken</a></td>
</tr>

<tr>
<td>5</td>
<td><b>Een gegevensstroom configureren</b>. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web SDK van Adobe Experience Platform.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en">Een gegevensstroom configureren<a></td> 
</tr>

<td>6</td>
<td><b>Een Adobe Analytics-service toevoegen</b> naar uw gegevensstroom. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics">Adobe Analytics-service toevoegen aan een gegevensstroom</a></td>
</tr>

<tr>
<td>7</td>
<td><b>De SDK van het web configureren</b>. Zorg ervoor dat de bibliotheek die u in stap 4 hebt geïnstalleerd, correct is geconfigureerd met de gegevensstroom-id (voorheen bekend als edge configuration id (<code>edgeConfigId</code>), organisatie-id (<code>orgId</code>) en andere beschikbare opties.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=en">De SDK van het web configureren</a></td>
</tr>

<tr>
<td>8</td>
<td><b>Opdrachten uitvoeren</b> en/of <b>gebeurtenissen track</b>. Nadat de basiscode op uw webpagina is geïmplementeerd, kunt u beginnen met het uitvoeren van opdrachten en het volgen van gebeurtenissen met de SDK.
</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/executing-commands.html?lang=en">Opdrachten uitvoeren</a> en <a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=en">Gebeurtenissen bijhouden</a></td>
</tr>

<tr>
<td>9</td><td><b>Uw implementatie uitbreiden en valideren</b> voordat het naar de productie wordt verplaatst.</td><td></td> 
</tr>
</table>


## Web SDK-extensie

Een overzicht op hoog niveau van de uitvoeringstaken:

![Adobe Analytics implementeren met de webSDK-uitbreidingsworkflow](../../assets/websdk-extension-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Taak</b></th><th style="width:35%"><b>Meer informatie</b></th>
</tr>

<tr>
<td>1</td>
<td>Zorg ervoor dat u <b>een rapportsuite gedefinieerd</b>.</td>
<td><a href="../../../admin/admin/c-manage-report-suites/report-suites-admin.md">Rapportsuitebeheer</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Installatieschema's en gegevenssets</b>. Om gegevensinzameling voor gebruik over toepassingen te standaardiseren die hefboomwerking Adobe Experience Platform, heeft Adobe de open en openbaar gedocumenteerde norm, het Model van de Gegevens van de Ervaring (XDM) gecreeerd.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en">Overzicht van schema's</a> en <a href="https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en">Overzicht van de gebruikersinterface voor gegevensbestanden</a></td>
</tr>

<tr>
<td>3</td>
<td><b>Een gegevenslaag maken</b> om het bijhouden van de gegevens op uw website te beheren.</td>
<td><a href="../../prepare/data-layer.md">Een datalaag maken</a></td>
</tr>

<tr>
<td>4</td>
<td><b>Een gegevensstroom configureren</b>. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web SDK van Adobe Experience Platform.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en">Een gegevensstroom configureren<a></td> 
</tr>

<tr>
<td>5</td> 
<td><b>Een Adobe Analytics-service toevoegen</b> naar uw gegevensstroom. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics">Adobe Analytics-service toevoegen aan een gegevensstroom</a></td>
</tr>

<tr>
<td>6</td>
<td><b>Een tag-eigenschap maken</b>. Eigenschappen zijn overkoepelende containers die worden gebruikt om te verwijzen naar tagbeheergegevens.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en#for-web">Een eigenschap voor tags maken of configureren voor het web</a></td>
</tr>

<tr>
<td>7</td> 
<td><b>De Web SDK-extensie installeren en configureren</b> in uw eigenschap tag. Vorm de uitbreiding van SDK van het Web om gegevens naar de datastream te verzenden die in stap 4 wordt gevormd.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html?lang=en">Overzicht van Adobe Experience Platform Web SDK-extensie</a></td>
</tr>

<tr>
<td>8</td>
<td><b>Interfereren, valideren en publiceren</b> aan de productie. Voeg de eigenschap tag toe aan uw website. Dan gebruik gegevenselementen, regels, etc., om uw implementatie aan te passen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=en">Overzicht van publicatie</a></td>
</tr>

</table>


## Aanvullende bronnen

Tags kunnen in hoge mate worden aangepast. Meer informatie over hoe u optimaal kunt profiteren van Adobe Analytics door de juiste gegevens op te nemen in uw implementatie.

- [Documentatie over tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html#): Leer hoe de interface werkt en welke extensies beschikbaar zijn.

- [Adobe Experience Platform Web SDK-documentatie](https://experienceleague.adobe.com/docs/web-sdk.html?lang=en)
