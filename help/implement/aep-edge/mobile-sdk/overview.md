---
title: Adobe Analytics implementeren met Adobe Experience Platform Mobile SDK
description: Gebruik de extensie Mobile SDK in Adobe Experience Platform Data Collection om gegevens naar Adobe Analytics te verzenden.
exl-id: 516e9a1e-caa7-4f8a-ab8c-6404e9242ccb
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 3%

---

# Adobe Analytics implementeren met Adobe Experience Platform Mobile SDK

De Adobe Experience Platform Mobile SDK helpt Adobe Experience Cloud-oplossingen en -services aan te zwengelen in uw mobiele apps. Het is beschikbaar voor Android™, iOS en verschillende platformonafhankelijke ontwikkelframeworks. De configuratie wordt behandeld door de Inzameling van Gegevens van Adobe Experience Platform.

>[!IMPORTANT]
>
>Een Adobe Analytics-extensie is ook beschikbaar in Adobe Experience Platform Data Collection. Als u deze extensie installeert, profiteert u niet van XDM of de Edge Network.

## Adobe Experience Platform SDK

Een overzicht op hoog niveau van de uitvoeringstaken:

![&#x200B; Adobe Analytics die het de uitbreidingswerkschema van Analytics gebruiken &#x200B;](../../assets/mobilesdk-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Taak</b></th><th style="width:35%"><b>Meer informatie</b></th>
</tr>

<tr>
<td>1</td>
<td>Verzeker u <b> een rapportreeks </b> hebt bepaald.</td>
<td><a href="../../../admin/tools/manage-rs/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b> vorm een datastream </b>. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web SDK van Adobe Experience Platform.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=nl-NL">Een gegevensstroom configureren<a></td> 
</tr>

<td>3</td>
<td><b> voeg de dienst van Adobe Analytics </b> aan uw datastream toe. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=nl-NL#analytics">Adobe Analytics-service toevoegen aan een gegevensstroom</a></td>
</tr>

<tr>
<td>4</td>
<td><b> creeer een mobiel bezit </b>. Een eigenschap is een container die u vult met extensies, regels, gegevenselementen en bibliotheken.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/">Een mobiele eigenschap instellen</a></tr>

<tr>
<td>5</td>
<td><b> installeer de uitbreiding van Adobe Experience Platform Edge Network </b> in het mobiele markeringsbezit en vorm de gegevensstroom in de uitbreiding.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/edge-network/"> Adobe Experience Platform Edge Network </a>
</tr>

<tr>
<td>6</td>
<td><b> code van het Gebruik in uw app </b> om de noodzakelijke uitbreidingen te registreren en uw markeringsconfiguratie te laden.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#set-up-the-configuration">De configuratie instellen</a></td>
</tr>

<tr>
<td>7</td>
<td><b> voert en test functionaliteit </b> uit gebruikend combinatie gegevenselementen van markering, regels, extra uitbreidingen, en SDK API vraag in uw app. Inspecteer, bevestig, en zuivert gegevensinzameling en ervaringen voor uw mobiele toepassing.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#use-the-sample-application"> Gebruik de steekproeftoepassing </a>
</tr>

<tr>
<td>8</td>
<td><b> breidt en bevestigt uw mobiele app implementatie </b> uit alvorens het uit aan productie te duwen.</td>
<td></td> 
</tr>

</table>


## Adobe Analytics-extensie

Een overzicht op hoog niveau van de uitvoeringstaken:

![&#x200B; Adobe Analytics die het de uitbreidingswerkschema van Analytics gebruiken &#x200B;](../../assets/mobilesdk-analytics-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Taak</b></th><th style="width:35%"><b>Meer informatie</b></th>
</tr>

<tr>
<td>1</td>
<td>Verzeker u <b> een rapportreeks </b> hebt bepaald.</td>
<td><a href="../../../admin/tools/manage-rs/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b> installeer de uitbreiding van Adobe Analytics </b> in het mobiele markeringsbezit en vorm de uitbreiding om aan uw rapportreeks te richten.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/adobe-analytics/"> uitbreiding van Adobe Analytics voor mobiel bezit </a>
</tr>

<tr>
<td>3</td>
<td><b> code van het Gebruik in uw app </b> om de noodzakelijke uitbreidingen te registreren en uw markeringsconfiguratie te laden.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#set-up-the-configuration">De configuratie instellen</a></td>
</tr>

<tr>
<td>4</td>
<td><b> voert en test functionaliteit </b> uit gebruikend combinatie gegevenselementen van markering, regels, extra uitbreidingen, en SDK API vraag in uw app. Inspecteer, bevestig, en zuivert gegevensinzameling en ervaringen voor uw mobiele toepassing.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#use-the-sample-application"> Gebruik de steekproeftoepassing </a>
</tr>

<tr>
<td>5</td>
<td><b> breidt en bevestigt uw mobiele app implementatie </b> uit alvorens het uit aan productie te duwen.</td>
<td></td> 
</tr>

</table>

## Aanvullende bronnen

- [&#x200B; documentatie van Markeringen &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=nl-NL#)

- [&#x200B; Mobiele documentatie van SDK &#x200B;](https://developer.adobe.com/client-sdks/documentation/)
