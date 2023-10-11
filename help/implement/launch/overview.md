---
title: Adobe Analytics implementeren met de extensie Analytics
description: Leer hoe u Adobe Analytics implementeert met tags en de extensie Analytics
feature: Launch Implementation
exl-id: 52990731-8a68-4779-ad42-6ec94b0aabd1
source-git-commit: 8cb2fd426e9fef247d79de4c138ea814dd691ed3
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 3%

---

# Adobe Analytics implementeren met de extensie Analytics

Tijdens de levensduur van Adobe Analytics heeft Adobe verschillende methoden aangeboden om code op uw site te implementeren voor gegevensverzameling. De Adobe raadt u momenteel aan de tags in Adobe Experience Platform te gebruiken.

Tags in Adobe Experience Platform zijn een oplossing voor tagbeheer waarmee u naast andere coderingsvereisten ook analytische code kunt implementeren. Adobe biedt integratie met andere oplossingen en producten aan, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.

Alle klanten met een actief Adobe Experience Cloud-contract kunnen tags gebruiken. Als u niet zeker bent als u toegang hebt, contacteer één van de het systeembeheerders van het Experience Cloud van uw organisatie.

Een overzicht op hoog niveau van de uitvoeringstaken:



![Adobe Analytics implementeren met behulp van de analyseextensieworkflow, zoals beschreven in deze sectie.](../assets/analytics-extension-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Taak</b></th><th style="width:35%"><b>Meer informatie</b></th>
</tr>

<tr>
<td> 1</td>
<td>Zorg ervoor dat u <b>een rapportsuite gedefinieerd</b>.</td>
<td><a href="../../admin/admin/c-manage-report-suites/report-suites-admin.md">Rapportsuitebeheer</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Een gegevenslaag maken</b> om het bijhouden van de gegevens op uw website te beheren.</td>
<td>
<a href="../prepare/data-layer.md">Een datalaag maken</a>
</td>
</tr>

<tr>
<td>3</td>
<td><b><b>Een tag-eigenschap maken</b>. Eigenschappen zijn overkoepelende containers die worden gebruikt om te verwijzen naar tagbeheergegevens.</td>
<td><a ref="../launch/create-analytics-property.md">Een Adobe Analytics-tageigenschap maken</a></td>
</tr>

<tr>
<td>4</td><td><b>De extensie Analytics installeren</b> in de eigenschap tag. Configureer de extensie Analytics om gegevens naar Adobe Analytics te verzenden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html?lang=en">Overzicht Adobe Analytics-extensie</a></td>
</tr>

<tr>
<td>5</td>
<td><b>Distribueren naar een ontwikkelomgeving</b>. Zorg voor een omgeving waarin u de ontwikkeling van tags kunt doorlopen.</td>
<td><a href="./deploy-dev.md">Implementeer een analytische implementatie in een ontwikkelomgeving</td>
</tr>

<tr>
<td>6</td> 
<td><b>Valideren en publiceren naar productie</b>. Sluit code in om de eigenschap tag op te nemen in de websitepagina's. Dan gebruik gegevenselementen, regels, etc., om uw implementatie aan te passen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?lang=en#embed-code">Code insluiten</a><br/><a href="./validate-publish-prod.md">Een ontwikkelimplementatie valideren en publiceren naar productie</a></td>
</tr>

</table>

## Aanvullende bronnen

Tags kunnen zeer aangepast worden. Meer informatie over hoe u optimaal kunt profiteren van Adobe Analytics door de juiste gegevens op te nemen in uw implementatie.

- [Documentatie over tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html#): Leer hoe de interface werkt en welke extensies beschikbaar zijn.

- [Uitvoeringsvariabelen](../vars/overview.md): Bepaal welke variabelen u naar de servers van de gegevensinzameling wilt verzenden.
