---
title: Boot verwijderen in Adobe Analytics
description: 3 manieren om vlekken te verwijderen in Adobe Analytics
translation-type: tm+mt
source-git-commit: e1cbdf87140b915dccbb8f64694797bb903d8ab8

---


# Boot verwijderen in Adobe Analytics

In Adobe Analytics hebt u meerdere opties om beide verkeer uit de rapportage te verwijderen:

## Bot-regels gebruiken

De filtermethoden Standaard en Aangepast bot worden ondersteund in **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** **[!UICONTROL Bot Rules]**:

| Type regel | Beschrijving |
|--- |--- |
| Standaardregels voor IAB-bot | Bij het selecteren **[!UICONTROL Enable IAB Bot Filtering Rules]** wordt gebruik gemaakt van de International Spiders &amp; Bots List van het [IAB](https://www.iab.com/) (International Advertising Bureau) om beide verkeer te verwijderen. De meeste klanten selecteren deze optie op een minimum. |
| Aangepaste botregels | U kunt de regels van de douanebot bepalen en toevoegen die op gebruikersagenten, IP adressen of IP waaiers worden gebaseerd. |

Zie Overzicht [van de](/help/admin/admin/bot-removal/bot-rules.md)basisregels voor meer informatie.

## Een combinatie van Adobe-gereedschappen gebruiken

Bovendien biedt Adobe, aangezien de bots snel overslaan, verschillende andere krachtige functies die, wanneer behoorlijk en op regelmatige basis worden gecombineerd, kunnen helpen om deze vijanden van gegevenskwaliteit te verwijderen. Deze functies zijn: Ervaar de Cloud-id-service, segmentatie, Data Warehouse, klantkenmerken en virtuele rapportsuite. Hier volgt een overzicht van hoe u deze gereedschappen kunt gebruiken.

### Stap 1: Geef de Cloud-id voor beleving van bezoekers door aan een nieuwe gedeclareerde id

Om te beginnen, zult u een nieuwe verklaarde identiteitskaart in de Dienst [van de Kern van](https://docs.adobe.com/content/help/en/core-services/interface/audiences/audience-library.html)Mensen willen tot stand brengen. U moet de Experience Cloud-id van uw bezoeker doorgeven aan deze nieuwe gedeclareerde id, die snel en eenvoudig kan worden uitgevoerd met [Adobe Experience Platform Launch](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html). Gebruik de naam ECID voor de gedeclareerde id.

![](assets/bot-cust-attr-setup.png)

Hieronder wordt beschreven hoe deze id kan worden vastgelegd via het gegevenselement. Zorg ervoor dat u uw Experience Cloud OrgID correct hebt ingevuld in het Data Element.

```return Visitor.getInstance("REPLACE_WITH_YOUR_ECORG_ID@AdobeOrg").getExperienceCloudVisitorID();```

Nadat dit gegevenselement is ingesteld, volgt u [deze instructies](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) om gedeclareerde id&#39;s door te geven aan het gereedschap ECID in Launch.

### Stap 2: Segmentatie gebruiken om vlekken te identificeren

Nu de ECID van uw bezoeker in een verklaarde identiteitskaart wordt overgegaan, kunt u [segmentatie in de Werkruimte](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/t-freeform-project-segment.html) van de Analyse gebruiken om bezoekers te identificeren die als bots handelen. Bots worden vaak gedefinieerd door hun gedrag: één toegangsbezoek, ongebruikelijke gebruikersagenten, onbekende apparaat/browser informatie, geen referentie, nieuwe bezoekers, ongebruikelijke landingspagina&#39;s, enz. Gebruik de bevoegdheden van de boor-downs van de Werkruimte en segmentatie om de bots te identificeren die het filtreren IAB en uw de boomregels van de rapportsuite hebben omzeild. Hier ziet u bijvoorbeeld een schermafbeelding van een segment dat u kunt gebruiken:

![](assets/bot-filter-seg1.png)

### Stap 3: Alles exporteren [!DNL Experience Cloud IDs] uit het segment via Data Warehouse

Nu u de bots hebt geïdentificeerd gebruikend segmenten, is de volgende stap het Warehouse van Gegevens te gebruiken om alle de Wolk IDs van de Ervaring te halen verbonden aan dit segment. Dit is hoe u opstelling uw verzoek van het [Pakhuis](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html) van Gegevens zou moeten:

![](assets/bot-dwh-3.png)

Vergeet niet de Experience Cloud Visitor-id te gebruiken als uw dimensie en het Bots-segment toe te passen.

### Stap 4: Deze lijst als kenmerk Klanten doorgeven aan Adobe

Zodra het rapport van het Pakhuis van Gegevens aankomt, zult u een lijst van ECIDs hebben die van historische gegevens moeten worden gefiltreerd. Kopieer en plak deze ECID&#39;s in een leeg CSV-bestand met slechts twee kolommen, ECID en Bot-vlag.

* **ECID**: Zorg ervoor dat deze kolomkop overeenkomt met de naam die u aan de bovenstaande nieuwe gedeclareerde id hebt gegeven.
* **Bodemvlag**: Voeg dit als het schemadimensie van het Attribuut van de Klant toe.

Gebruik dit .CSV-bestand als het importbestand voor klantkenmerken en abonneer vervolgens uw rapportsuite(s) op het kenmerk Klant zoals beschreven in dit [blogbericht](https://theblog.adobe.com/link-digital-behavior-customers).

![](assets/bot-csv-4.png)

### Stap 5: Creeer een segment dat hefboomwerkingen de nieuwe Attributen van de Klant

Zodra uw gegevensreeks is verwerkt en in de Werkruimte van de Analyse geïntegreerd, creeer één meer segment dat hefboomwerkingen uw nieuwe de attributendimensie van de klant &quot;van de Vlag&quot;en een [!UICONTROL Exclude] container:

![](assets/bot-filter-seg2.png)

### Stap 6: Dit segment gebruiken als het filter Virtuele rapportsuite

Tot slot zou u een [Virtuele Reeks](/help/components/vrs/vrs-about.md) van het Rapport moeten creëren die dit segment gebruikt om de geïdentificeerde vlekken uit te filteren:

![](assets/bot-vrs.png)

Deze nieuwe, gesegmenteerde virtuele rapportsuite zal nu resulteren in een aanzienlijk schonere gegevensset, waarbij de geïdentificeerde bots volledig zijn verwijderd.

### Stap 7: Herhaal stap 2, 3 en 4 regelmatig

Stel ten minste een maandelijkse herinnering in om nieuwe vlekken te identificeren en te filteren, wellicht voorafgaand aan de regelmatig geplande analyse.
