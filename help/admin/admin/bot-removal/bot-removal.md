---
title: Bot verwijderen in Adobe Analytics
description: 3 manieren om vlekken te verwijderen in Adobe Analytics
exl-id: 6d4b1925-4496-4017-85f8-82bda9e92ff3
translation-type: tm+mt
source-git-commit: b78e8303277b08a4c693283e45416f2e104268b7
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 2%

---

# Bot verwijderen in Adobe Analytics

In Adobe Analytics hebt u meerdere opties om beide verkeer uit de rapportage te verwijderen:

## Bot-regels gebruiken

Zowel de standaard als de douanetriefiltermethoden worden gesteund in **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Bot Rules]**:

| Type regel | Beschrijving |
|--- |--- |
| Standaardregels voor IAB-bot | Als u **[!UICONTROL Enable IAB Bot Filtering Rules]** selecteert, wordt de lijst met internationale spinnen en boten van [IAB&#39;s](https://www.iab.com/) (International Advertising Bureau&#39;s) gebruikt om beide typen verkeer te verwijderen. De meeste klanten selecteren deze optie op een minimum. |
| Aangepaste botregels | U kunt de regels van de douanebot bepalen en toevoegen die op gebruikersagenten, IP adressen of IP waaiers worden gebaseerd. |

Zie [Overzicht van beide regels](/help/admin/admin/bot-removal/bot-rules.md) voor meer informatie.

## Gebruik de [!UICONTROL websiteBot] plug-in om lettertypen te identificeren

Met de insteekmodule websiteBot kunt u dynamisch bepalen of bezoekers van een bureaublad bots zijn. U kunt deze gegevens gebruiken om grotere nauwkeurigheid in alle types van rapportering te drijven, die u een betere manier geeft om wettig plaatsverkeer te meten.

Deze plug-in voert twee controles uit:

* Eerst, bepaalt het of het apparaat een Desktop of een mobiel apparaat gebruikend de navigator.UserAgent variabele is. Mobiele apparaten worden genegeerd.
* Als het een desktopapparaat is, wordt er een gebeurtenislistener toegevoegd voor muisbewegingen.

Zie [Adobe Analytics Implementation Guide](https://experienceleague.adobe.com/docs/analytics/implementation/vars/plugins/websitebot.html) voor meer informatie.

## Een combinatie van Adobe-gereedschappen gebruiken

Bovendien biedt Adobe, aangezien bots snel morferen, verschillende andere krachtige functies die, wanneer ze op een juiste manier en op regelmatige basis worden gecombineerd, kunnen helpen om deze vijanden van gegevenskwaliteit te verwijderen. Deze functies zijn: De Dienst van identiteitskaart van Experience Cloud, Segmentatie, Data Warehouse, de Attributen van de Klant, en Virtuele Reeksen van het Rapport. Hier volgt een overzicht van hoe u deze gereedschappen kunt gebruiken.

### Stap 1: Geef de Experience Cloud-id van uw bezoekers door in een nieuwe gedeclareerde id

Om te beginnen, zult u een nieuwe verklaarde identiteitskaart in [de Dienst van de Kern van Mensen](https://docs.adobe.com/content/help/nl-NL/core-services/interface/audiences/audience-library.html) willen tot stand brengen. U moet de Experience Cloud-id van uw bezoeker doorgeven in deze nieuwe gedeclareerde id, die u snel en eenvoudig kunt gebruiken met [Adobe Experience Platform Launch](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html). Gebruik de naam ECID voor de gedeclareerde id.

![](assets/bot-cust-attr-setup.png)

Hieronder wordt beschreven hoe deze id kan worden vastgelegd via het gegevenselement. Ben zeker om uw Experience Cloud OrgID in het Element van Gegevens correct te bevolken.

```return Visitor.getInstance("REPLACE_WITH_YOUR_ECORG_ID@AdobeOrg").getExperienceCloudVisitorID();```

Nadat dit gegevenselement is ingesteld, volgt u [deze instructies](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) om gedeclareerde id&#39;s door te geven aan het ECID-gereedschap in Launch.

### Stap 2: Segmentatie gebruiken om vlekken te identificeren

Nu de ECID van uw bezoeker in een verklaarde identiteitskaart wordt overgegaan, kunt u [segmentatie in Analysis Workspace](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/t-freeform-project-segment.html) gebruiken om bezoekers te identificeren die als bots handelen. Bots worden vaak gedefinieerd door hun gedrag: één toegangsbezoek, ongebruikelijke gebruikersagenten, onbekende apparaat/browser informatie, geen referentie, nieuwe bezoekers, ongebruikelijke landingspagina&#39;s, enz. Gebruik de bevoegdheden van de boor-downs van de Werkruimte en segmentatie om de bots te identificeren die het filtreren IAB en uw de boomregels van de rapportsuite hebben omzeild. Hier ziet u bijvoorbeeld een schermafbeelding van een segment dat u kunt gebruiken:

![](assets/bot-filter-seg1.png)

### Stap 3: Alle [!DNL Experience Cloud IDs] uit het segment exporteren via Data Warehouse

Nu u de bots gebruikend segmenten hebt geïdentificeerd, is de volgende stap hefboomwerking Data Warehouse om alle Experience Cloud IDs te halen verbonden aan dit segment. Dit is hoe u opstelling uw [verzoek Data Warehouse](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html) zou moeten:

![](assets/bot-dwh-3.png)

Vergeet niet Experience Cloud Visitor-id te gebruiken als uw dimensie en het Bots-segment toe te passen.

### Stap 4: Geef deze lijst terug naar Adobe als Attribuut van de Klant

Zodra het rapport van de Data Warehouse aankomt, zult u een lijst van ECIDs hebben die van historische gegevens moeten worden gefiltreerd. Kopieer en plak deze ECID&#39;s in een leeg CSV-bestand met slechts twee kolommen, ECID en Bot-vlag.

* **ECID**: Zorg ervoor dat deze kolomkop overeenkomt met de naam die u aan de bovenstaande nieuwe gedeclareerde id hebt gegeven.
* **Bodemvlag**: Voeg dit als het schemadimensie van het Attribuut van de Klant toe.

Gebruik dit .CSV-bestand als het importbestand voor klantkenmerken en abonneer vervolgens uw rapportsuite(s) op het kenmerk Klant zoals beschreven in dit [blogbericht](https://theblog.adobe.com/link-digital-behavior-customers).

![](assets/bot-csv-4.png)

### Stap 5: Creeer een segment dat hefboomwerkingen de nieuwe Attributen van de Klant

Als uw gegevensset eenmaal is verwerkt en geïntegreerd in Analysis Workspace, maakt u nog een segment dat gebruikmaakt van de nieuwe attribuutdimensie van de klant &quot;Bot Flag&quot; en een [!UICONTROL Exclude]-container:

![](assets/bot-filter-seg2.png)

### Stap 6: Dit segment gebruiken als het filter Virtuele rapportsuite

Tot slot zou u een [Virtuele Reeks van het Rapport](/help/components/vrs/vrs-about.md) moeten creëren die dit segment gebruikt om de geïdentificeerde bots uit te filtreren:

![](assets/bot-vrs.png)

Deze nieuwe, gesegmenteerde virtuele rapportsuite zal nu resulteren in een aanzienlijk schonere gegevensset, waarbij de geïdentificeerde bots volledig zijn verwijderd.

### Stap 7: Herhaal stap 2, 3 en 4 regelmatig

Stel ten minste een maandelijkse herinnering in om nieuwe vlekken te identificeren en te filteren, wellicht voorafgaand aan de regelmatig geplande analyse.
