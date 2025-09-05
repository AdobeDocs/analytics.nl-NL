---
title: Adobe Analytics implementeren met de extensie Analytics
description: Leer hoe u Adobe Analytics implementeert met tags en de extensie Analytics
feature: Tags
exl-id: 52990731-8a68-4779-ad42-6ec94b0aabd1
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 3%

---

# Adobe Analytics implementeren met de extensie Analytics

Tijdens de levensduur van Adobe Analytics heeft Adobe verschillende methoden aangeboden om code op uw site te implementeren voor gegevensverzameling. Adobe momenteel geadviseerde methode is door [ Markeringen ](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html) in Adobe Experience Platform.

Tags in Adobe Experience Platform zijn een oplossing voor tagbeheer waarmee u naast andere coderingsvereisten ook analytische code kunt implementeren. Adobe biedt integratie met andere oplossingen en producten, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.

Alle klanten met een actief Adobe Experience Cloud-contract kunnen tags gebruiken. Neem contact op met een van de Experience Cloud-systeembeheerders van uw organisatie als u niet zeker weet of u toegang hebt.

Een overzicht op hoog niveau van de uitvoeringstaken:



![ hoe te om Adobe Analytics uit te voeren gebruikend het de uitbreidingswerkschema van Analytics, zoals die in deze sectie wordt beschreven.](../assets/analytics-extension-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Taak</b></th><th style="width:35%"><b>Meer informatie</b></th>
</tr>

<tr>
<td> 1</td>
<td>Verzeker u <b> een rapportreeks </b> hebt bepaald.</td>
<td><a href="../../admin/tools/manage-rs/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b> creeer een gegevenslaag </b> om het volgen van de gegevens op uw website te beheren.</td>
<td>
<a href="../prepare/data-layer.md">Een datalaag maken</a>
</td>
</tr>

<tr>
<td>3</td>
<td><b><b> creeer een markeringsbezit </b>. Eigenschappen zijn overkoepelende containers die worden gebruikt om te verwijzen naar tagbeheergegevens.</td>
<td><a href="../launch/create-analytics-property.md">Een Adobe Analytics-tageigenschap maken</a></td>
</tr>

<tr>
<td>4</td><td><b> installeer de uitbreiding van de Analyse </b> in het markeringsbezit. Configureer de extensie Analytics om gegevens naar Adobe Analytics te verzenden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html">Overzicht Adobe Analytics-extensie</a></td>
</tr>

<tr>
<td>5</td>
<td><b> stelt aan een ontwikkelomgeving </b> op. Zorg voor een omgeving waarin u de ontwikkeling van tags kunt doorlopen.</td>
<td><a href="./deploy-dev.md">Implementeer een analytische implementatie in een ontwikkelomgeving</td>
</tr>

<tr>
<td>6</td> 
<td><b> bevestigt en publiceert aan productie </b>. Sluit code in om de eigenschap tag op te nemen in de websitepagina's. Dan gebruik gegevenselementen, regels, etc., om uw implementatie aan te passen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html#embed-code"> bed code </a><br/> in <a href="./validate-publish-prod.md"> bevestigt een ontwikkelingsimplementatie en publiceert aan productie </a></td>
</tr>

</table>

## Aanvullende bronnen

Tags kunnen zeer aangepast worden. Meer informatie over hoe u optimaal kunt profiteren van Adobe Analytics door de juiste gegevens op te nemen in uw implementatie.

- [ de documentatie van Markeringen ](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html#): Leer hoe de interface werkt en welke uitbreidingen beschikbaar zijn.

- [ de variabelen van de Implementatie ](../vars/overview.md): Bepaal welke variabelen u naar de servers van de gegevensinzameling wilt verzenden.
