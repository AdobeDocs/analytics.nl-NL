---
title: Bot verwijderen in Adobe Analytics
description: Bommen verwijderen in Adobe Analytics
feature: Bot Removal
role: Admin
exl-id: 6d4b1925-4496-4017-85f8-82bda9e92ff3
source-git-commit: de9d2039411a7f8539f8e7b4eb840f03c964f489
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Bot verwijderen in Adobe Analytics

Adobe Analytics biedt meerdere opties om beide verkeer uit de rapportage te verwijderen:

## Bot-regels gebruiken

Filtermethoden voor zowel standaard als aangepaste bot worden ondersteund in **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Bot Rules]** :

| Type regel | Beschrijving |
|--- |--- |
| Standaardregels voor IAB-bot | Het selecteren van **[!UICONTROL Enable IAB Bot Filtering Rules]** gebruikt [ IAB ](https://www.iab.com/) (Internationale Lijst van het Bureau van Advertising) Internationale Spinnen &amp; Bots om beide verkeer te verwijderen. De meeste klanten selecteren deze optie op een minimum. |
| Aangepaste botregels | U kunt de regels van de douanebot bepalen en toevoegen die op gebruikersagenten, IP adressen, of IP waaiers worden gebaseerd. |

Voor meer detail, zie [ beide regels ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) begrijpen en vormen.

## Een combinatie van Adobe Tools gebruiken

Bovendien biedt Adobe, aangezien bots snel aan het morferen zijn, verschillende andere krachtige functies die, wanneer ze op de juiste manier en op regelmatige basis worden gecombineerd, kunnen helpen om deze vijanden van gegevenskwaliteit te verwijderen. Deze functies zijn: Experience Cloud ID-service, segmentatie, Data Warehouse, klantkenmerken en virtuele rapportsuites. Hier volgt een overzicht van hoe u deze gereedschappen kunt gebruiken.

### Stap 1: Geef de Experience Cloud-id van uw bezoekers door in een nieuwe gedeclareerde id

Om te beginnen, creeer een nieuwe verklaarde identiteitskaart in de [ Dienst van de Kern van Mensen ](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html). Geef identiteitskaart van Experience Cloud van uw bezoeker in deze nieuwe verklaarde identiteitskaart over, die snel en gemakkelijk met [ markeringen in Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html) kan worden gedaan. Gebruik de naam ECID voor de gedeclareerde id.

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-cust-attr-setup.png)

Hieronder wordt beschreven hoe deze id kan worden vastgelegd via het gegevenselement. Zorg ervoor dat u uw Experience Cloud OrgID correct in het gegevenselement vult.

```return Visitor.getInstance("REPLACE_WITH_YOUR_ECORG_ID@AdobeOrg").getExperienceCloudVisitorID();```

Zodra dit Element van Gegevens opstelling is, volg [ deze instructies ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html) om gedeclareerde IDs in het ECID Hulpmiddel door te geven gebruikend markeringen in Adobe Experience Platform.

### Stap 2: segmentatie gebruiken om vlekken te identificeren

Nu u ECID van uw bezoeker in gedeclareerde identiteitskaart hebt overgegaan, kunt u [ segmentatie in Analysis Workspace ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/t-freeform-project-segment.html) gebruiken om bezoekers te identificeren die als bots handelen. Bots worden vaak gedefinieerd door hun gedrag: enkele toegangsbezoeken, ongebruikelijke gebruikersagenten, onbekende apparaat-/browserinformatie, geen referentie, nieuwe bezoekers, ongebruikelijke landingspagina&#39;s, enz. Gebruik de bevoegdheden van Workspace boor-downs en segmentatie om de bots te identificeren die het filtreren IAB en uw regels van de rapportsuite allebei hebben omzeild. Hier ziet u bijvoorbeeld een schermafbeelding van een segment dat u kunt gebruiken:

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-filter-seg1.png)

### Stap 3: Alle [!DNL Experience Cloud IDs] uit het segment exporteren via Data Warehouse

Nu u de vlekken gebruikend segmenten hebt geïdentificeerd, is de volgende stap Data Warehouse te gebruiken om alle Experience Cloud IDs te halen verbonden aan dit segment. Dit het schermschot toont hoe u opstelling uw [ Data Warehouse ](/help/export/data-warehouse/data-warehouse.md) verzoek zou moeten:

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-dwh-3.png)

Gebruik de Experience Cloud Visitor-id als dimensie en pas het segment &#39;Bots&#39; toe.

### Stap 4: geef deze lijst terug aan Adobe als attribuut van de Klant

Als het Data Warehouse-rapport eenmaal is ontvangen, hebt u een lijst met ECID&#39;s die moeten worden gefilterd op basis van historische gegevens. Kopieer en plak deze ECID&#39;s in een leeg CSV-bestand met slechts twee kolommen, ECID en Bot-vlag.

* **ECID**: Zorg ervoor dat deze kolomkopbal de naam aanpast u aan nieuwe verklaarde identiteitskaart hierboven gaf.
* **Vlag van de Bot**: Voeg &quot;Vlag van de Bot&quot;als dimensie van het het attributenschema van de Klant toe.

Gebruik dit .CSV dossier als uw dossier van de de attributeninvoer van de Klant, dan onderteken uw rapportreeks(s) aan de attributen van de Klant zoals die in dit [ blogpost ](https://blog.adobe.com/en/publish/2016/10/20/link-digital-behavior-customers) worden beschreven.

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-csv-4.png)

### Stap 5: Creeer een segment dat hefboomwerkingen de nieuwe attributen van de Klant

Als uw gegevensset eenmaal is verwerkt en geïntegreerd in Analysis Workspace, maakt u nog een segment dat gebruikmaakt van de nieuwe maat van het kenmerk &quot;Bot Flag&quot; voor klanten en een [!UICONTROL Exclude] -container:

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-filter-seg2.png)

### Stap 6: Gebruik dit segment als het filter van de virtuele rapportsuite

Tot slot creeer a [ Virtuele rapportreeks ](/help/components/vrs/vrs-about.md) die dit segment gebruikt om de geïdentificeerde bots uit te filteren:

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-vrs.png)

Deze nieuwe gesegmenteerde virtuele rapportsuite zal nu leiden tot een schonere gegevensset, waarbij de geïdentificeerde &#39;bots&#39; zijn verwijderd.

### Stap 7: Herhaal stap 2, 3 en 4 regelmatig

Stel ten minste een maandelijkse herinnering in om nieuwe vlekken te identificeren en te filteren, misschien vóór een regelmatig geplande analyse.

>[!MORELIKETHIS]
>
>* [ Betere Bot die (Deel 1) blokkeert: De Grondbeginselen ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/better-bot-blocking-part-1-the-basics/ba-p/715839)
>* [ Betere Bot die (Deel 2) blokkeert: Het identificeren van Bots en het Leveraging CIDR.](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/better-bot-blocking-part-2-identifying-bots-and-leveraging-cidr/ba-p/722132)
>* [ Betere Bot die (Deel 3) blokkeert: De Hit Gouverneur ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/better-bot-blocking-part-3-the-hit-governor/ba-p/727051)

