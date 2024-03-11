---
title: Adobe Analytics implementeren met de Adobe Experience Platform Edge Network Server-API
description: Gebruik de Adobe Experience Platform Edge Network Server-API om gegevens naar Adobe Analytics te verzenden.
exl-id: 1ede95b7-4f17-4d69-aba6-62b253b6693a
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 2e5171842794d7acc7bb67048b734f47a438cf1c
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# Adobe Analytics implementeren met de Adobe Experience Platform Edge Network Server-API

U gebruikt typisch de Server API van het Netwerk van de Rand van het Experience Platform om gegevens server-kant eerder dan cliënt-kant te verzamelen en wanneer het verzamelen van gegevens van apparaten zoals apparaten IoT, reeks-top dozen, Desktoptoepassingen. Vervolgens verzendt u die gegevens naar het Edge-netwerk en naar services zoals Adobe Analytics.

Overweeg ook de Edge Network Server-API wanneer u wilt dat vertrouwelijke gegevens veilig worden verzameld en geverifieerd in het netwerk. Zie [Verificatie](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/authentication.html) voor meer informatie .

Een overzicht op hoog niveau van de uitvoeringstaken:

![Adobe Analytics die de uitbreidingsworkflow voor Analytics gebruikt](../../assets/edge-network-server-api-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Taak</b></th><th style="width:35%"><b>Meer informatie</b></th>
</tr>

<tr>
<td>1</td>
<td>Zorg ervoor dat u <b>een rapportsuite gedefinieerd</b>.</td>
<td><a href="../../../admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Installatieschema's</b>. Om gegevensinzameling voor gebruik over toepassingen te standaardiseren die hefboomwerking Adobe Experience Platform, heeft de Adobe de open en openbaar gedocumenteerde norm, het Model van de Gegevens van de Ervaring (XDM) gecreeerd.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html">Overzicht van de interface Schemas</a></td>
</tr>

<tr>
<td>3</td>
<td><b>Een gegevensstroom configureren</b>. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het gebruiken van API's van het Netwerk van Adobe Experience Platform Edge API.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html">Een gegevensstroom configureren<a></td> 
</tr>

<tr>
<td>4</td>
<td><b>Gegevensverzameling implementeren en testen</b> met de API's voor het verzamelen van gegevens voor Single-event en Batch-gebeurtenissen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html">Gegevensverzameling voor één gebeurtenis</a><br/><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/non-interactive-data-collection.html">Batch-gebeurtenisgegevensverzameling</a>
</tr>

<td>5</td>
<td><b>Een Adobe Analytics-service toevoegen</b> naar uw gegevensstroom. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/interacting-other-adobe-solutions/interacting-adobe-analytics.html">Interactie met Adobe Analytics</a></td>
</tr>


</table>

Zie [Edge Network Server API-documentatie](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html)en een voorbeeld [integratie met Adobe Analytics](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/interacting-other-adobe-solutions/interacting-adobe-analytics.html) voor meer informatie .

