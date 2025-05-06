---
title: Adobe Analytics implementeren met de Adobe Experience Platform Edge Network API
description: Gebruik de Adobe Experience Platform Edge Network API om gegevens naar Adobe Analytics te verzenden.
exl-id: 1ede95b7-4f17-4d69-aba6-62b253b6693a
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 8e701a3da6f04ccf2d7ac3abd10c6df86feb00a7
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 1%

---

# Adobe Analytics implementeren met de Adobe Experience Platform Edge Network API

U gebruikt doorgaans de Experience Platform Edge Network API om gegevens te verzamelen op de server in plaats van op de client en om gegevens te verzamelen van apparaten zoals IoT-apparaten, set-top boxes en bureaubladtoepassingen. Vervolgens verzendt u die gegevens naar het Edge-netwerk en naar services zoals Adobe Analytics.

Overweeg ook de Edge Network API wanneer u wilt dat vertrouwelijke gegevens veilig worden verzameld en geverifieerd via het netwerk. Zie [ Authentificatie ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/authentication.html) voor meer informatie.

Een overzicht op hoog niveau van de uitvoeringstaken:

![ Adobe Analytics die het de uitbreidingswerkschema van Analytics gebruiken ](../../assets/edge-network-server-api-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Taak</b></th><th style="width:35%"><b>Meer informatie</b></th>
</tr>

<tr>
<td>1</td>
<td>Verzeker u <b> een rapportreeks </b> hebt bepaald.</td>
<td><a href="../../../admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b> schema's van de Opstelling </b>. Om gegevensinzameling voor gebruik over toepassingen te standaardiseren die hefboomwerking Adobe Experience Platform, heeft Adobe de open en openbaar gedocumenteerde norm, het Model van de Gegevens van de Ervaring (XDM) gecreeerd.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html">Overzicht van de interface Schemas</a></td>
</tr>

<tr>
<td>3</td>
<td><b> vorm een datastream </b>. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het gebruiken van API's van Adobe Experience Platform Edge Network API.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html">Een gegevensstroom configureren<a></td> 
</tr>

<tr>
<td>4</td>
<td><b> voert en test gegevensinzameling </b> uit gebruikend de Enige gebeurtenisgegevens en de inzameling APIs van de gebeurtenisgegevens van de Partij.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html"> Single-event gegevensinzameling </a><br/> <a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/non-interactive-data-collection.html"> de inzameling van de gebeurtenisgegevens van de Partij </a>
</tr>

<td>5</td>
<td><b> voeg de dienst van Adobe Analytics </b> aan uw datastream toe. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/interacting-other-adobe-solutions/interacting-adobe-analytics.html">Interactie met Adobe Analytics</a></td>
</tr>


</table>

Zie [ Edge Network API documentatie ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html) voor meer informatie.

