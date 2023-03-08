---
description: Veelgestelde vragen over Adobe Analytics-gegevensbeheer
title: Veelgestelde vragen over gegevensbeheer
feature: Data Governance
exl-id: 57399c1b-cf08-405b-8c1b-9d23e4c38716
source-git-commit: b8640d1387a475e2a9dd082759f0514bd18c1b6e
workflow-type: tm+mt
source-wordcount: '2076'
ht-degree: 48%

---

# Veelgestelde vragen

+++ **Hoe ondersteunt Adobe Analytics toegangs- en verwijderingsaanvragen voor eindgebruikers (geregistreerde personen) die door klanten (datacontrollers) zijn gevalideerd?**

Wanneer verschillende gegevensprivacyregels (GDPR, CCPA) van kracht worden, ondersteunt Adobe Analytics de verwerking van geverifieerde verzoeken die door gegevensverwerkingsverantwoordelijken zijn ingediend bij de Experience Cloud Data Privacy API om een geautomatiseerd proces mogelijk te maken. De Data Privacy-API van Adobe is ontworpen om individuele aanvragen om rechten (bijvoorbeeld toegangs- en verwijderingsrechten) te verwerken voor data van onze klanten die zijn opgeslagen in Adobe Experience Cloud-oplossingen. Het is flexibel en schalen volgens het aantal verzoeken van de gegevenstoegang en schrapt uw bedrijf van de Onderwerpen van Gegevens ontvangt.

Ook, staat Privacy Service API de klant toe om de status op te controleren hoe de gegevens toegang hebben en verzoeken schrappen die worden voldaan. Zie voor meer informatie [Privacy Service-API](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) documentatie.

+++

+++ **Wie is verantwoordelijk voor het ontvangen, accepteren en honoreren Data Privacy-aanvragen van eindgebruikers?**

De gegevenscontroller is als enige verantwoordelijk voor het ontvangen en aanvaarden van verzoeken. De Data Controller valideert de identiteit van de betrokkene en voldoet vervolgens aan het verzoek. Een deel van deze verantwoordelijkheid kan het contacteren van Adobe met de ID&#39;s van de Gegevenssubjecten inhouden die kunnen worden geassocieerd met gegevens die in Adobe Analytics worden opgeslagen.

Als gegevensverwerker, moet Adobe redelijke hulp aan de Controlemechanisme verlenen om geverifieerde verzoeken binnen een aanvaardbare hoeveelheid tijd te verwerken.

+++

+++ **Hoe weten Adobe-klanten (datacontrollers) welke Data Privacy-aanvragen horen bij welke id&#39;s in Adobe Analytics voor Data Privacy-verwerking?**

De verantwoordelijken van Gegevens bepalen hoe te om identiteit voor verzoeken van de Subjects van Gegevens op te lossen. Overweeg het gebruik van de Adobe Data Privacy-tag voor het ophalen van id&#39;s. Uw ontwikkelingsteams besparen tijd door onze ophalen van de Data Privacy ID te gebruiken om gebruikers-id&#39;s (cookie-id&#39;s) vast te leggen. Vervolgens kunnen ze onze API voor gegevensprivacy gebruiken om die gebruikers-id&#39;s naar de relevante oplossingen in de Adobe Experience Cloud for Data Privacy-aanvraagverwerking te sturen. De Data Privacy-API kan een breed scala aan klant-id&#39;s in meerdere Adobe-oplossingen ondersteunen.

Als een betrokkene een verzoek indient samen met een id (aangepaste variabele - prop of eVar), scant Adobe Analytics vervolgens de bewaarde historie van de gegevens die voor de opgegeven id zijn verzameld. Raadpleeg voor meer informatie over het configureren van aangepaste id&#39;s die zijn opgeslagen in Analytics Props of eVars de [Analysedocumentatie over naamruimten](/help/admin/admin/c-data-governance/data-labeling/gdpr-namespaces.md).

+++

+++ **Hoe kan Adobe Analytics Data Governance helpen bij het verwerken van Data Privacy-aanvragen?**

Gegevensbeheer is een nieuw hulpmiddel binnen Adobe Analytics dat gegevenscontrollers de mogelijkheid biedt gegevensbesturingselementen en classificaties toe te passen op hun analysegegevens. Met deze nieuwe tool kunnen Adobe-klanten de verwerking van hun Data Privacy-aanvragen voor datatoegang en dataverwijdering aanpassen. In de Data Governance-console kunnen beheerders de gewenste instellingen definiëren die moeten worden toegepast op diverse datakolommen in Adobe Analytics. Zodra deze labels zijn gedefinieerd, zal Adobe alle downstreamtoegangs- of verwijderingsaanvragen honoreren en verwerken volgens de gewenste labelinstellingen van de klant. Het is de verantwoordelijkheid van de gegevensverwerkingsverantwoordelijke om deze labelinstellingen te beoordelen en samen met hun wettelijke vertegenwoordigers aan te raden.

De Data Governance-tool bevat de volgende datalabels:

* **Labels voor identiteitsgegevens**: Wordt gebruikt om gegevens te classificeren die een individu direct of in combinatie met andere gegevens kunnen identificeren. (Geen, I1, I2)

* **Gevoelige gegevenslabels**: Wordt gebruikt om gegevens in te delen als gegevens die volgens het toepasselijke recht als gevoelig kunnen worden gedefinieerd. (Geen, S1, S2) Merk op dat het gebruik van gevoelige data in Adobe Analytics momenteel algemeen verboden is, behalve voor nauwkeurige geolocatiedata die correct zijn verkregen krachtens de toepasselijke wetgeving, die in sommige rechtsgebieden als gevoelige data kunnen worden beschouwd.

* **Data Privacy Data Labels**: Wordt gebruikt om de velden te definiëren die persoonlijke id&#39;s kunnen bevatten voor gebruik in verzoeken om gegevensprivacy of die moeten worden verwijderd als onderdeel van een verzoek tot verwijdering van gegevensprivacy. Deze labels kunnen in sommige gevallen overlappen met labels voor identiteitsdata en gevoelige data.

Voor meer informatie over labels voor gegevensbeheer raadpleegt u [Data Privacy Labels voor analytische variabelen](/help/admin/admin/c-data-governance/data-labeling/gdpr-labels.md).

+++

+++ **Hoe kan ik bevestigen dat de verzoeken van de Privacy Service behoorlijk werken om gegevens van Adobe Analytics te schrappen?**

De klanten van Analytics zetten typisch sommige reeksen van het testrapport op om functionaliteit te verifiëren alvorens het aan het algemene publiek wordt vrijgegeven. Websites of toepassingen die aan de productie voorafgaan, verzenden gegevens naar deze test/dev/QA-rapportsuites om te evalueren hoe de zaken werken wanneer de code wordt uitgebracht voordat echt verkeer naar de productierapporten wordt verzonden.

Bij een normale configuratie kan de verwerking van een GPDR-aanvraag echter niet eerst op deze testrapportsuites worden getest, voordat aanvragen op de productierapportsuites worden toegepast. Dit komt omdat een verzoek van de Privacy van Gegevens automatisch wordt toegepast op alle rapportreeksen in de organisatie van de Experience Cloud, die vaak alle rapportreeksen voor uw bedrijf is.

Toch zijn er een paar manieren dat u uw verwerking van de Privacy van Gegevens kunt testen alvorens het op al uw rapportseries toe te passen:

* Een optie is om een afzonderlijke Experience Cloud-organisatie in te stellen die alleen testrapportsuites bevat. Gebruik vervolgens deze Experience Cloud-organisatie voor uw Data Privacy-tests en uw normale Experience Cloud-organisatie voor daadwerkelijke Data Privacy-verwerking.

* Een andere optie is om andere naamruimten toe te wijzen aan de id&#39;s in uw testrapportsuites, in tegenstelling tot de naamruimten in uw productierapportsuites. U kunt bijvoorbeeld voor elke naamruimte een voorvoegsel “qa-” opgeven in uw testrapportsuites. Wanneer u Data Privacy-aanvragen verzendt met uitsluitend naamruimten met het qa-voorvoegsel, worden deze aanvragen alleen uitgevoerd op uw testrapportsuites. Later, wanneer u aanvragen verzendt zonder het qa-voorvoegsel, worden ze toegepast op uw productierapportsuites. **Dit is de aanbevolen aanpak, tenzij u de naamruimten bezoekerId, AID, ECID of customVisitorId gebruikt. Deze naamruimten zijn gecodeerd en u kunt geen alternatieve namen voor deze naamruimten opgeven in de suites van het testrapport.**

+++

+++ **Waar kan ik beginnen met Data Privacy-gereedmaking in Adobe Analytics?**

Voor een stapsgewijze begeleiding bij de gereedmaking voor Data Privacy-regels raadpleegt u [ Adobe Analytics Data Privacy-workflow](/help/admin/admin/c-data-governance/an-gdpr-workflow.md).

+++

+++ **Hoe zouden de Controllers van Gegevens over toestemming moeten denken wanneer het op gebruikersbetrokkenheid aankomt?**

GDPR en CCPA zijn goede kansen om uw strategie en praktijken van het toestemmingsbeheer te heroverwegen. Dit omvat het bepalen wanneer de toestemming en het nadenken over het waardevoorstel voor de gebruiker nodig is. Overweeg de waardepropositie voor de privacy van de consument, wat conversie en loyaliteit kan helpen bevorderen. De ruimte voor toestemmingsbeheer (bijv. tools, normen, best practices) evolueert snel en is een gebied om aandacht aan te besteden. Om de impact op de betrokkenheid van gebruikers te minimaliseren, moeten controllers samenwerken met leveranciers in deze ruimte en met hun juridische adviseur om ervoor te zorgen dat ze opkomende wetten en richtlijnen voor toestemming en cookies volgen. Het is een goede strategie om na te denken over ‘ervaringsgerichte privacy’ in de vorm van een merkgerichte, contextueel relevante ervaring waarin de waardepropositie van uw dataverzamelingsactiviteiten worden uiteengezet.

Als Data Controller bent u verantwoordelijk voor het verkrijgen van uitdrukkelijke toestemming van de betrokkenen voordat u gegevens over deze gegevens verzamelt (mogelijk met inbegrip van Adobe Analytics-gegevens) en voor het implementeren van een [opt-out-mechanisme](https://www.adobe.com/privacy/opt-out.html#customeruse) op uw website. Hierdoor kunnen uw gegevenssubjecten afzien van toekomstige Adobe Experience Cloud-gegevensverzameling.

+++

+++ **Hoe zouden de Controllers van Gegevens over gegevensbehoud moeten denken wanneer het over de Privacy van Gegevens komt?**

Persoonsgegevens mogen in het algemeen niet langer worden bewaard dan nodig is om het doel waarvoor zij zijn verzameld te bereiken. Algemene Adobe passen een standaard gegevensbewaaringsplan van 5 maanden toe, tenzij een andere gegevensbewaartermijn contractueel is overeengekomen. Klanten moeten hun beleid voor gegevensbewaring instellen voordat Adobe een verzoek om gegevensprivacy kan verwerken.

Het huidige dataretentiebeleid van elke rapportsuite wordt weergegeven in de nieuwe Data Governance-beheergebruikersinterface. Klanten moeten contact opnemen met hun Adobe-vertegenwoordiger als ze hun beleid voor het bewaren van gegevens moeten aanpassen. Zie [Veelgestelde vragen over Adobe Analytics-gegevensbewaring](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html?lang=en).

+++

+++ **Kan een klant de bewaarperiode voor standaardgegevens verkorten of verlengen?**

Klanten kunnen vragen dat hun gegevens eerder dan 25 maanden worden verwijderd door de klantenservice aan te roepen. Klanten kunnen de gegevensbewaring ook langer dan 25 maanden laten duren door een extensie aan te schaffen. Extensies zijn beschikbaar in stappen van 1 jaar of langer, tot maximaal 8 jaar (in totaal 10 jaar). Voor deze uitbreidingen zijn bijgewerkte contractvoorwaarden en extra kosten vereist.

+++

+++ **Met welke privacyoverwegingen moet een datacontrolleraccount rekening houden wanneer persoonlijke data uit Adobe Analytics worden geëxporteerd?**

Als een klant Adobe Analytics-datafeeds gebruikt om data van Analytics naar zijn of haar bedrijfsdatawarehouse of naar andere systemen buiten Adobe te exporteren, is het de verantwoordelijkheid van de klant (de datacontroller) om ervoor te zorgen dat verwijderingsaanvragen op de data worden toegepast. Dit geldt ook voor on-premise implementaties van de Data Workbench van de Adobe, waar een lopende de gegevensvoer van Adobe Analytics de gegevens van de Data Workbench bevolkt. Adobe kan tools bieden voor het zoeken naar en verwijderen van de records uit bepaalde soorten datafeeds, zoals data die worden gebruikt voor Data Workbench, maar het is nog steeds de verantwoordelijkheid van de klant (datacontroller) om ervoor te zorgen dat de data worden verwijderd in overeenstemming met hun eigen, interne beleid voor dataretentie en dataverwijdering.

Houd ook rekening met gevallen waarin werknemers Adobe Analytics-rapporten met persoonlijke gegevens hebben gedownload. Deze rapporten moeten mogelijk worden bijgewerkt of verwijderd als er een verzoek tot verwijdering in verband met gegevensprivacy is ontvangen met een id die in het rapport voorkomt. De klanten zouden met de juridische adviseur van hun eigen bedrijf moeten werken om bewaartermijnen, en privacy en veiligheidseisen te bepalen die op deze types van documenten zouden moeten worden toegepast.

+++

+++ **Sommige data die we niet hadden moeten verzamelen, zijn per ongeluk naar Adobe Analytics verzonden. Kunnen we de API voor gegevensprivacy gebruiken om deze gegevens op te schonen?**

De [API voor Privacy Service van gegevens](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) is verstrekt om u te helpen verzoeken van de Privacy van Gegevens vervullen, die tijdgevoelig zijn. Het gebruik van deze API voor andere doeleinden wordt niet ondersteund door Adobe en kan een nadelige invloed hebben op de snelheid waarmee Adobe door de gebruiker geïnitieerde Data Privacy-aanvragen met hoge prioriteit voor andere Adobe-klanten kan afhandelen.

We vragen u de Data Privacy-API niet te gebruiken voor andere doeleinden, zoals het wissen van data die per ongeluk zijn verzonden tussen grote groepen bezoekers. Bedenk ook dat voor bezoekers die een treffer hebben verwijderd (bijgewerkt of geanonimiseerd) als gevolg van een Data Privacy-verwijderingsaanvraag, de statusgegevens worden hersteld. De volgende keer dat de bezoeker uw website bezoekt, wordt deze een nieuwe bezoeker. Alle eVar-attributie wordt opnieuw gestart, evenals informatie als aantal bezoeken, referrers, bezochte eerste pagina, enz. Dit bijeffect is ongewenst in situaties waarin u datavelden wilt wissen, en legt de nadruk op één reden waarom de Data Privacy-API niet geschikt is voor dit gebruik.

Neem contact op met uw accountmanager (CSM) om samen met het consultingteam van onze engineering-architect verder te controleren en zich in te spannen voor het verwijderen van eventuele PII- of dataproblemen.

+++

+++ **Ons juridisch team heeft vastgesteld dat de waarden die we al jaren in een variabele verzamelen, niet meer in overeenstemming zijn met ons bijgewerkte privacybeleid. Kunnen we de Data Privacy-API gebruiken om alle waarden uit deze variabele te verwijderen?**

De [API voor Privacy Service van gegevens](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) is verstrekt om u te helpen verzoeken van de Privacy van Gegevens vervullen, die tijdgevoelig zijn. Het gebruik van deze API voor andere doeleinden wordt niet ondersteund door Adobe en kan een nadelige invloed hebben op de snelheid waarmee Adobe door de gebruiker geïnitieerde Data Privacy-aanvragen met hoge prioriteit voor andere Adobe-klanten kan afhandelen. We vragen u de Data Privacy-API niet te gebruiken voor andere doeleinden, zoals het wissen van data die per ongeluk zijn verzonden tussen grote groepen bezoekers.

Bedenk ook dat voor bezoekers die een treffer hebben verwijderd (bijgewerkt of geanonimiseerd) als gevolg van een Data Privacy-verwijderingsaanvraag, de statusgegevens worden hersteld. De volgende keer dat de bezoeker uw website bezoekt, wordt deze een nieuwe bezoeker. Alle eVar-attributie wordt opnieuw gestart, evenals informatie als aantal bezoeken, referrers, bezochte eerste pagina, enz. Dit bijeffect is ongewenst in situaties waarin u datavelden wilt wissen, en legt de nadruk op één reden waarom de Data Privacy-API niet geschikt is voor dit gebruik.

Neem contact op met uw accountmanager (CSM) om samen te werken met ons consultatieteam van de Engineering Architect om verdere revisie uit te voeren en de moeite te leveren om eventuele problemen met PII&#39;s of gegevens te verwijderen.

+++

Aanvullende Data Privacy-bronnen:

* [Algemene voorwaarden GDPR](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_commonterms.pdf)
* Experience Cloud Data Privacy [Care Package](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_carepackage.pdf)
* Experiential Privacy [Blogpost](https://theblog.adobe.com/experiential-privacy-an-investment-opportunity-for-the-experience-business/)
