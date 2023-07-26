---
title: Adobe Analytics implementeren met de Adobe Experience Platform Edge Network Server-API
description: Gebruik de Adobe Experience Platform Edge Network Server-API om gegevens naar Adobe Analytics te verzenden.
exl-id: 1ede95b7-4f17-4d69-aba6-62b253b6693a
feature: Implementation Basics
source-git-commit: 5a57f4d2d73f16a72fbe8b198b1609a8bffc38b6
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 2%

---

# Adobe Analytics implementeren met de Adobe Experience Platform Edge Network Server-API

U gebruikt typisch de Server API van het Netwerk van de Rand van het Experience Platform om gegevens van apparaten zoals apparaten IoT, reeks-hoogste dozen, Desktoptoepassingen te verzamelen. Stuur die gegevens vervolgens naar het Edge-netwerk en naar services zoals Adobe Analytics.

Overweeg ook de Edge Network Server-API wanneer u wilt dat vertrouwelijke gegevens veilig worden verzameld en geverifieerd in het netwerk. Zie [Verificatie](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/authentication.html?lang=en) voor meer informatie .

Een overzicht op hoog niveau van de uitvoeringstaken:

![Adobe Analytics die de uitbreidingsworkflow voor Analytics gebruikt](../../assets/edge-network-server-api.png)

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
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en">Overzicht van de interface Schemas</a> en <a href="https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en">Overzicht van de gebruikersinterface voor gegevensbestanden</a></td>
</tr>

<tr>
<td>3</td>
<td><b>Een gegevensstroom configureren</b>. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het gebruiken van API's van het Netwerk van Adobe Experience Platform Edge API.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=en">Een gegevensstroom configureren<a></td> 
</tr>

<tr>
<td>4</td>
<td><b>Gegevensverzameling implementeren en testen</b> met de API's voor het verzamelen van gegevens voor Single-event en Batch-gebeurtenissen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=en">Gegevensverzameling voor één gebeurtenis</a><br/><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/non-interactive-data-collection.html?lang=en">Batch-gebeurtenisgegevensverzameling</a>
</tr>

<td>5</td>
<td><b>Een Adobe Analytics-service toevoegen</b> naar uw gegevensstroom. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/interacting-other-adobe-solutions/interacting-adobe-analytics.html?lang=ens">Interactie met Adobe Analytics</a></td>
</tr>


</table>

Zie [Edge Network Server API-documentatie](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html)en een voorbeeld [integratie met Adobe Analytics](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/interacting-other-adobe-solutions/interacting-adobe-analytics.html) voor meer informatie .

