---
description: Veelgestelde vragen over Adobe Analytics-gegevensbeheer
title: Veelgestelde vragen over gegevensbeheer
feature: Data Governance
role: Admin
exl-id: 57399c1b-cf08-405b-8c1b-9d23e4c38716
source-git-commit: 2d5348a4a6377313f5aab229214d97a02c826939
workflow-type: tm+mt
source-wordcount: '2040'
ht-degree: 38%

---

# Veelgestelde vragen over Adobe Analytics-privacy

+++ **Hoe ondersteunt Adobe Analytics toegangs- en verwijderingsaanvragen voor eindgebruikers (geregistreerde personen) die door klanten (datacontrollers) zijn gevalideerd?**

Wanneer verschillende gegevensprivacyregels (GDPR, CCPA) van kracht worden, ondersteunt Adobe Analytics de verwerking van geverifieerde verzoeken die door gegevensverwerkingsverantwoordelijken zijn ingediend bij de Experience Cloud Data Privacy API, zodat een geautomatiseerd proces mogelijk wordt. De Data Privacy-API van Adobe is ontworpen om individuele aanvragen om rechten (bijvoorbeeld toegangs- en verwijderingsrechten) te verwerken voor data van onze klanten die zijn opgeslagen in Adobe Experience Cloud-oplossingen. Het is flexibel en schalen volgens het aantal verzoeken van de gegevenstoegang en schrapt uw bedrijf van de Onderwerpen van Gegevens ontvangt.

De Privacy Service API biedt de klant ook de mogelijkheid om de status te controleren van de manier waarop de gegevens worden benaderd en aanvragen te verwijderen die worden uitgevoerd. Voor meer details zie [&#x200B; Privacy Service API &#x200B;](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) documentatie.

+++

+++ **Wie is verantwoordelijk voor het ontvangen, accepteren en honoreren Data Privacy-aanvragen van eindgebruikers?**

De gegevenscontroller is als enige verantwoordelijk voor het ontvangen en aanvaarden van verzoeken. De Data Controller valideert de identiteit van de betrokkene en voldoet vervolgens aan het verzoek. Een deel van deze verantwoordelijkheid kan bestaan uit contact opnemen met Adobe met de id&#39;s van de gegevenssubjecten die kunnen worden gekoppeld aan in Adobe Analytics opgeslagen gegevens.

Als gegevensverwerker moet Adobe de Controller redelijke hulp bieden om geverifieerde verzoeken binnen een aanvaardbare tijd te verwerken.

+++

+++ **Hoe weten Adobe-klanten (datacontrollers) welke Data Privacy-aanvragen horen bij welke id&#39;s in Adobe Analytics voor Data Privacy-verwerking?**

De verantwoordelijken van Gegevens bepalen hoe te om identiteit voor verzoeken van de Subjects van Gegevens op te lossen. U kunt overwegen om de Retrieval-tag voor Adobe-gegevensprivacygegevens in te voeren. Uw ontwikkelingsteams besparen tijd door onze ophaaltag voor de Data Privacy ID te gebruiken om gebruikers-id&#39;s (cookie-id&#39;s) vast te leggen. Vervolgens kunnen ze onze API voor gegevensprivacy gebruiken om die gebruikers-id&#39;s naar de relevante oplossingen in de Adobe Experience Cloud for Data Privacy-aanvraagverwerking te sturen. De Data Privacy API kan een groot aantal klant-id&#39;s voor meerdere Adobe-oplossingen ondersteunen.

Als een betrokkene een verzoek indient samen met een id (aangepaste variabele - prop of eVar), scant Adobe Analytics vervolgens de bewaarde geschiedenis van de gegevens die voor de gegeven id zijn verzameld. Voor meer details over hoe te om douane IDs te vormen die in de steunen van Analytics of eVars wordt opgeslagen, gelieve te verwijzen naar de [&#x200B; documentatie van Analytics over namespaces &#x200B;](/help/admin/tools/privacy-labeling/namespaces.md).

+++

+++ **Hoe kan Adobe Analytics Data Governance helpen bij het verwerken van Data Privacy-aanvragen?**

Gegevensbeheer is een nieuw hulpmiddel binnen Adobe Analytics dat gegevenscontrollers de mogelijkheid biedt gegevensbesturingselementen en classificaties toe te passen op hun analysegegevens. Met deze nieuwe tool kunnen Adobe-klanten de verwerking van hun Data Privacy-aanvragen voor datatoegang en dataverwijdering aanpassen. In de Data Governance-console kunnen beheerders de gewenste instellingen definiëren die moeten worden toegepast op diverse datakolommen in Adobe Analytics. Zodra deze labels zijn gedefinieerd, zal Adobe alle downstreamtoegangs- of verwijderingsaanvragen honoreren en verwerken volgens de gewenste labelinstellingen van de klant. Het is de verantwoordelijkheid van de gegevensverwerkingsverantwoordelijke om deze labelinstellingen te beoordelen en samen met hun wettelijke vertegenwoordigers aan te raden.

De Data Governance-tool bevat de volgende datalabels:

* **Etiketten van Gegevens van de Identiteit**: Gebruikt om gegevens te classificeren die een individu of direct of in combinatie met andere gegevens kunnen identificeren. (Geen, I1, I2)

* **Gevoelige Etiketten van Gegevens**: Gebruikt om gegevens als gegevens te classificeren die als gevoelig onder toepasselijk recht kunnen worden bepaald. (Geen, S1, S2) Merk op dat het gebruik van gevoelige data in Adobe Analytics momenteel algemeen verboden is, behalve voor nauwkeurige geolocatiedata die correct zijn verkregen krachtens de toepasselijke wetgeving, die in sommige rechtsgebieden als gevoelige data kunnen worden beschouwd.

* **de Etiketten van de Gegevens van de Privacy van Gegevens van Gegevens**: Gebruikt om de gebieden te bepalen die persoonlijke herkenningstekens voor gebruik in de verzoeken van de Privacy van Gegevens kunnen bevatten of die als deel van een het schrappingsverzoek van de Privacy van Gegevens zouden moeten worden verwijderd. Deze labels kunnen in sommige gevallen overlappen met labels voor identiteitsdata en gevoelige data.

Voor meer informatie over de etiketten van het Beleid van Gegevens, zie {de Etiketten van de Privacy van 0} Gegevens voor de Variabelen van Analytics [.](/help/admin/tools/privacy-labeling/labels.md)

+++

+++ **Hoe kan ik bevestigen dat de verzoeken van Privacy Service behoorlijk werken om gegevens van Adobe Analytics te schrappen?**

De klanten van Analytics zetten typisch sommige reeksen van het testrapport op om functionaliteit te verifiëren alvorens het aan het algemene publiek wordt vrijgegeven. Websites of toepassingen die aan de productie voorafgaan, verzenden gegevens naar deze test/dev/QA-rapportsuites om te evalueren hoe de zaken werken wanneer de code wordt uitgebracht voordat echt verkeer naar de productierapporten wordt verzonden.

Bij een normale configuratie kan de verwerking van een GPDR-aanvraag echter niet eerst op deze testrapportsuites worden getest, voordat aanvragen op de productierapportsuites worden toegepast. Dit komt omdat een verzoek van de Privacy van Gegevens automatisch wordt toegepast op alle rapportreeksen in de organisatie van Experience Cloud, die vaak alle rapportreeksen voor uw bedrijf is.

Toch zijn er een paar manieren dat u uw verwerking van de Privacy van Gegevens kunt testen alvorens het op al uw rapportseries toe te passen:

* Een optie is om een afzonderlijke Experience Cloud-organisatie in te stellen die alleen testrapportsuites bevat. Gebruik vervolgens deze Experience Cloud-organisatie voor uw Data Privacy-tests en uw normale Experience Cloud-organisatie voor daadwerkelijke Data Privacy-verwerking.

* Een andere optie is verschillende naamruimten toe te wijzen aan de id&#39;s in uw testreeks van het testrapport, in tegenstelling tot de naamruimten in uw productierapporten. U kunt bijvoorbeeld voor elke naamruimte een voorvoegsel “qa-” opgeven in uw testrapportsuites. Wanneer u Data Privacy-aanvragen verzendt met uitsluitend naamruimten met het qa-voorvoegsel, worden deze aanvragen alleen uitgevoerd op uw testrapportsuites. Later, wanneer u aanvragen verzendt zonder het qa-voorvoegsel, worden ze toegepast op uw productierapportsuites. **dit is de geadviseerde benadering, tenzij u `visitorId`, STEUN, ECID of `customVisitorId` namespaces gebruikt. Deze namespaces zijn hard - gecodeerd en u kunt geen afwisselende namen voor hen in uw reeksen van het testrapport specificeren.**

+++

+++ **Waar kan ik beginnen met Data Privacy-gereedmaking in Adobe Analytics?**

Voor een geleidelijke analyse om klaar voor de regels van de Privacy van Gegevens te worden, zie [&#x200B; het Werkschema van de Privacy van Gegevens van Adobe Analytics &#x200B;](privacy-workflow.md).

+++

+++ **hoe zouden de Controllers van Gegevens over toestemming moeten denken wanneer het over gebruikersbetrokkenheid komt?**

GDPR en CCPA zijn goede kansen om uw strategie en praktijken van het toestemmingsbeheer te heroverwegen. Dit omvat het bepalen wanneer de toestemming en het nadenken over het waardevoorstel voor de gebruiker nodig is. Overweeg het waardevoorstel voor de privacy van de consument, wat conversie en loyaliteit kan helpen bevorderen. De ruimte voor toestemmingsbeheer (bijv. tools, normen, best practices) evolueert snel en is een gebied om aandacht aan te besteden. Om de impact op de betrokkenheid van gebruikers te minimaliseren, moeten controllers samenwerken met leveranciers in deze ruimte en met hun juridische adviseur om ervoor te zorgen dat ze opkomende wetten en richtlijnen voor toestemming en cookies volgen. Het is een goede strategie om na te denken over ‘ervaringsgerichte privacy’ in de vorm van een merkgerichte, contextueel relevante ervaring waarin de waardepropositie van uw dataverzamelingsactiviteiten worden uiteengezet.

U, als het Controlemechanisme van Gegevens, bent verantwoordelijk voor het verkrijgen van expliciete toestemming van uw Subjects van Gegevens alvorens u gegevens over hen (misschien met inbegrip van de gegevens van Adobe Analytics) verzamelt en voor het uitvoeren van een [&#x200B; opt-out mechanisme &#x200B;](https://www.adobe.com/privacy/opt-out.html#customeruse) op uw website. Hierdoor kunnen uw gegevenssubjecten afzien van toekomstige Adobe Experience Cloud-gegevensverzameling.

+++

+++ **hoe zouden de Controllers van Gegevens over gegevensbehoud moeten denken wanneer het over de Privacy van Gegevens komt?**

Persoonsgegevens mogen in het algemeen niet langer worden bewaard dan nodig is om het doel waarvoor zij zijn verzameld te bereiken. Algemene voorwaarden van Adobe passen een standaard 25-maands gegevensbewaaringsplan toe, tenzij contractueel een andere bewaartermijn is overeengekomen. Klanten moeten hun beleid voor het bewaren van gegevens instellen voordat Adobe een verzoek om privacy van gegevens kan verwerken.

Het huidige dataretentiebeleid van elke rapportsuite wordt weergegeven in de nieuwe Data Governance-beheergebruikersinterface. Klanten moeten contact opnemen met hun Adobe-vertegenwoordiger als ze hun beleid voor het bewaren van gegevens moeten aanpassen. Gelieve te verwijzen naar [&#x200B; Veelgestelde vragen van het Behoud van Gegevens van Adobe Analytics &#x200B;](/help/technotes/data-retention.md).

+++

+++ **kan een klant de periode van het standaardgegevensbehoud verminderen of uitbreiden?**

Klanten kunnen vragen dat hun gegevens eerder dan 25 maanden worden verwijderd door de klantenservice aan te roepen. Klanten kunnen de gegevensbewaring ook langer dan 25 maanden laten duren door een extensie aan te schaffen. Extensies zijn beschikbaar in stappen van 1 jaar of langer, tot maximaal 8 jaar (in totaal 10 jaar). Voor deze uitbreidingen zijn bijgewerkte contractvoorwaarden en extra kosten vereist.

+++

+++ **welke privacyoverwegingen een rekening van het Controlemechanisme van Gegevens zouden moeten voor wanneer de persoonlijke gegevens uit Adobe Analytics worden uitgevoerd?**

Als een klant Adobe Analytics-datafeeds gebruikt om data van Analytics naar zijn of haar bedrijfsdatawarehouse of naar andere systemen buiten Adobe te exporteren, is het de verantwoordelijkheid van de klant (de datacontroller) om ervoor te zorgen dat verwijderingsaanvragen op de data worden toegepast. Dit geldt ook voor on-premise implementaties van Adobe Data Workbench, waar een doorlopende Adobe Analytics-gegevenstoevoer de Data Workbench-gegevens vult. Adobe kan tools bieden voor het zoeken naar en verwijderen van de records uit bepaalde soorten datafeeds, zoals data die worden gebruikt voor Data Workbench, maar het is nog steeds de verantwoordelijkheid van de klant (datacontroller) om ervoor te zorgen dat de data worden verwijderd in overeenstemming met hun eigen, interne beleid voor dataretentie en dataverwijdering.

Houd ook rekening met gevallen waarin werknemers Adobe Analytics-rapporten met persoonlijke gegevens hebben gedownload. Deze rapporten moeten mogelijk worden bijgewerkt of verwijderd als er een verzoek tot verwijdering in verband met gegevensprivacy is ontvangen met een id die in het rapport voorkomt. De klanten zouden met de juridische adviseur van hun eigen bedrijf moeten werken om bewaartermijnen, en privacy en veiligheidseisen te bepalen die op deze types van documenten zouden moeten worden toegepast.

+++

+++ **sommige gegevens die wij niet moesten verzamelen werden per ongeluk verzonden naar Adobe Analytics. Kunnen wij de API van de Privacy van Gegevens gebruiken om deze gegevens op te schonen?**

De [&#x200B; Gegevens Privacy Service API &#x200B;](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) is verstrekt om u te helpen de verzoeken van de Privacy van Gegevens vervullen, die tijdgevoelig zijn. Het gebruik van deze API voor andere doeleinden wordt niet ondersteund door Adobe en kan van invloed zijn op de mogelijkheid van Adobe om tijdig verzoeken om gegevensprivacy die door de gebruiker zijn geïnitieerd voor andere Adobe-klanten in te dienen met hoge prioriteit.

We vragen u de API voor gegevensprivacy niet te gebruiken voor andere doeleinden, zoals het wissen van gegevens die per ongeluk zijn verzonden door grote groepen bezoekers. Bedenk ook dat voor bezoekers die een treffer hebben verwijderd (bijgewerkt of geanonimiseerd) als gevolg van een Data Privacy-verwijderingsaanvraag, de statusgegevens worden hersteld. De volgende keer dat de bezoeker uw website bezoekt, wordt deze een nieuwe bezoeker. Alle eVar-attributie wordt opnieuw gestart, evenals informatie als aantal bezoeken, referrers, bezochte eerste pagina, enz. Dit bijeffect is ongewenst in situaties waarin u datavelden wilt wissen, en legt de nadruk op één reden waarom de Data Privacy-API niet geschikt is voor dit gebruik.

Neem contact op met uw Adobe-accountteam om samen te werken met ons consultingteam van Engineering Architect voor verdere evaluatie en om alles in het werk te stellen om eventuele problemen met PII&#39;s of gegevens te verwijderen.

+++

+++ **Ons juridisch team heeft bepaald dat de waarden die wij in een variabele al jaren verzamelen niet meer aan ons bijgewerkte privacybeleid voldoen. Kunnen we de Data Privacy-API gebruiken om alle waarden uit deze variabele te verwijderen?**

De [&#x200B; Gegevens Privacy Service API &#x200B;](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) is verstrekt om u te helpen de verzoeken van de Privacy van Gegevens vervullen, die tijdgevoelig zijn. Het gebruik van deze API voor andere doeleinden wordt niet ondersteund door Adobe en kan een nadelige invloed hebben op de snelheid waarmee Adobe door de gebruiker geïnitieerde Data Privacy-aanvragen met hoge prioriteit voor andere Adobe-klanten kan afhandelen. We vragen u de Data Privacy-API niet te gebruiken voor andere doeleinden, zoals het wissen van data die per ongeluk zijn verzonden tussen grote groepen bezoekers.

Bedenk ook dat voor bezoekers die een treffer hebben verwijderd (bijgewerkt of geanonimiseerd) als gevolg van een Data Privacy-verwijderingsaanvraag, de statusgegevens worden hersteld. De volgende keer dat de bezoeker uw website bezoekt, wordt deze een nieuwe bezoeker. Alle eVar-attributie wordt opnieuw gestart, evenals informatie als aantal bezoeken, referrers, bezochte eerste pagina, enz. Dit bijeffect is ongewenst in situaties waarin u datavelden wilt wissen, en legt de nadruk op één reden waarom de Data Privacy-API niet geschikt is voor dit gebruik.

Neem contact op met uw Adobe-accountteam om samen te werken met ons consultingteam van de Engineering Architect voor verdere controle en om alles in het werk te stellen om eventuele problemen met PII&#39;s of gegevens te verwijderen.

+++

Aanvullende Data Privacy-bronnen:

* [Algemene voorwaarden GDPR](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_commonterms.pdf)
* Experience Cloud Data Privacy [Care Package](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_carepackage.pdf)
* Experiential Privacy [Blogpost](https://theblog.adobe.com/experiential-privacy-an-investment-opportunity-for-the-experience-business/)
