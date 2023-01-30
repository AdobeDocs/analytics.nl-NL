---
description: Veelgestelde vragen over Adobe Analytics-gegevensbeheer
title: Veelgestelde vragen over gegevensbeheer
feature: Data Governance
exl-id: 57399c1b-cf08-405b-8c1b-9d23e4c38716
source-git-commit: 82c69131fcc5a22795e44ed97246240aec31f4d9
workflow-type: tm+mt
source-wordcount: '1867'
ht-degree: 81%

---

# Veelgestelde vragen

+++ **Hoe ondersteunt Adobe Analytics toegangs- en verwijderingsaanvragen voor eindgebruikers (geregistreerde personen) die door klanten (datacontrollers) zijn gevalideerd?**

Wanneer verschillende gegevensprivacyregels (GDPR, CCPA) van kracht worden, ondersteunt Adobe Analytics de verwerking van geverifieerde verzoeken die door gegevensverwerkingsverantwoordelijken zijn ingediend bij de Experience Cloud Data Privacy API om een geautomatiseerd proces mogelijk te maken. De Data Privacy-API van Adobe is ontworpen om individuele aanvragen om rechten (bijvoorbeeld toegangs- en verwijderingsrechten) te verwerken voor data van onze klanten die zijn opgeslagen in Adobe Experience Cloud-oplossingen. Dit is flexibel en er wordt geschaald op basis van het aantal datatoegangs- en verwijderingsaanvragen dat uw bedrijf van geregistreerde personen ontvangt.

De Privacy Service-API biedt de klant ook de mogelijkheid om de status te controleren van de manier waarop de verzoeken om gegevenstoegang en -verwijdering worden uitgevoerd. Zie voor meer informatie [Privacy Service-API](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) documentatie.

+++

+++ **Wie is verantwoordelijk voor het ontvangen, accepteren en honoreren Data Privacy-aanvragen van eindgebruikers?**

De gegevenscontroller (d.w.z. de Adobe-klant) is als enige verantwoordelijk voor het verstrekken van persoonsgegevens aan betrokkenen in antwoord op een verzoek om individuele rechten op grond van gegevensbescherming. De datacontroller is eveneens als enige verantwoordelijk voor het ontvangen van aanvragen en het accepteren van de aanvraag - het valideren van de identiteit van de geregistreerde persoon en vervolgens het honoreren van de aanvraag, waaronder mogelijk contact opnemen met Adobe over id&#39;s van geregistreerde personen die mogelijk zijn gekoppeld aan data die in Adobe Analytics zijn opgeslagen.

Als dataverwerker moet Adobe de controller redelijke hulp bieden om geverifieerde aanvragen binnen een aanvaardbare tijd te verwerken.

+++

+++ **Hoe weten Adobe-klanten (datacontrollers) welke Data Privacy-aanvragen horen bij welke id&#39;s in Adobe Analytics voor Data Privacy-verwerking?**

De gegevenscontrollers bepalen hoe de identiteit van de betrokkenen kan worden opgelost. Overweeg het gebruik van de Adobe Data Privacy-tag voor het ophalen van id&#39;s. Uw ontwikkelingsteams besparen tijd door onze Data Privacy-tag voor het ophalen van id&#39;s te gebruiken om gebruikers-id&#39;s (cookie-id&#39;s) vast te leggen en deze gebruikers-id&#39;s via de Data Privacy-API te verzenden naar de relevante oplossingen in de Adobe Experience Cloud voor Data Privacy-aanvraagverwerking. De Data Privacy-API kan een breed scala aan klant-id&#39;s in meerdere Adobe-oplossingen ondersteunen.

Als een geregistreerde persoon aanvraag verzendt samen met een id (aangepaste variabele - prop of eVar), scant Adobe Analytics vervolgens de gehele bewaarde geschiedenis van de data die voor de betreffende id zijn verzameld. Raadpleeg voor meer informatie over het configureren van aangepaste id&#39;s die zijn opgeslagen in Analytics Props of eVars de [Analysedocumentatie over naamruimten](/help/admin/c-data-governance/data-labeling/gdpr-namespaces.md).

+++

+++ **Hoe kan Adobe Analytics Data Governance helpen bij het verwerken van Data Privacy-aanvragen?**

Data Governance is een nieuwe tool in Adobe Analytics waardoor datacontrollers databesturingselementen en classificaties kunnen toepassen op hun Analytics-data. Met deze nieuwe tool kunnen Adobe-klanten de verwerking van hun Data Privacy-aanvragen voor datatoegang en dataverwijdering aanpassen. In de Data Governance-console kunnen beheerders de gewenste instellingen definiëren die moeten worden toegepast op diverse datakolommen in Adobe Analytics. Zodra deze labels zijn gedefinieerd, zal Adobe alle downstreamtoegangs- of verwijderingsaanvragen honoreren en verwerken volgens de gewenste labelinstellingen van de klant. Het is de verantwoordelijkheid van de datacontroller om deze labelinstellingen te controleren en te bespreken met hun wettelijke vertegenwoordigers. Adobe Analytics moedigt klanten aan om de gegevenslabel correct in te stellen vóór de datum waarop de GDPR van kracht wordt, namelijk 25 mei 2018, zodat de voltooiing van het verzoek met behulp van de Data Privacy API kan worden aangepast.

De Data Governance-tool bevat de volgende datalabels:

* Labels voor identiteitsdata:  wordt gebruikt om data te classificeren die een individu direct of in combinatie met andere data kunnen identificeren. (Geen, I1, I2)

* Labels voor gevoelige data:  wordt gebruikt om data te classificeren als data die volgens het toepasselijke recht als gevoelig kunnen worden gedefinieerd. (Geen, S1, S2) Merk op dat het gebruik van gevoelige data in Adobe Analytics momenteel algemeen verboden is, behalve voor nauwkeurige geolocatiedata die correct zijn verkregen krachtens de toepasselijke wetgeving, die in sommige rechtsgebieden als gevoelige data kunnen worden beschouwd.

* Data Privacy-datalabels:  wordt gebruikt om de velden te definiëren die persoonlijke id&#39;s kunnen bevatten voor gebruik in Data Privacy-aanvragen, of die moeten worden verwijderd als onderdeel van een Data Privacy-verwijderingsaanvraag. Deze labels kunnen in sommige gevallen overlappen met labels voor identiteitsdata en gevoelige data.

Voor meer informatie over labels voor gegevensbeheer raadpleegt u [Data Privacy Labels voor analytische variabelen](/help/admin/c-data-governance/data-labeling/gdpr-labels.md).

+++

+++ **Waar kan ik beginnen met Data Privacy-gereedmaking in Adobe Analytics?**

Voor een stapsgewijze begeleiding bij de gereedmaking voor Data Privacy-regels raadpleegt u [ Adobe Analytics Data Privacy-workflow](/help/admin/c-data-governance/an-gdpr-workflow.md).

+++

+++ **Hoe moeten datacontrollers denken over toestemming in verband met gebruikersbetrokkenheid?**

GDPR en CCPA zijn goede gelegenheden om opnieuw na te denken over uw strategie en praktijk voor toestemmingsbeheer, inclusief de bepaling wanneer toestemming nodig is, en de overweging van de waardepropositie voor de gebruiker. Overweeg de waardepropositie voor de privacy van de consument, wat conversie en loyaliteit kan helpen bevorderen.  De ruimte voor toestemmingsbeheer (bijv. tools, normen, best practices) evolueert snel en is een gebied om aandacht aan te besteden. Om de impact op de gebruikersbetrokkenheid tot een minimum te beperken moeten controllers samenwerken met leveranciers op dit gebied en hun adviseurs, en de nieuwe EU-wetgeving en -richtlijnen voor toestemming en cookies volgen. Het is een goede strategie om na te denken over ‘ervaringsgerichte privacy’ in de vorm van een merkgerichte, contextueel relevante ervaring waarin de waardepropositie van uw dataverzamelingsactiviteiten worden uiteengezet.

U, als de gegevensbeheerder, bent verantwoordelijk voor het verkrijgen van uitdrukkelijke toestemming van de betrokkenen voordat u gegevens over hen verzamelt (mogelijk met inbegrip van Adobe Analytics-gegevens) en voor het implementeren van een [opt-out-mechanisme](https://www.adobe.com/privacy/opt-out.html#customeruse) op uw website. Hierdoor kunnen geregistreerde personen zich afmelden voor toekomstige dataverzameling in Adobe Experience Cloud.

+++

+++ **Hoe moeten datacontrollers denken over dataretentie in verband met Data Privacy?**

In het algemeen bepaalt Data Privacy dat persoonlijke data doorgaans niet langer mogen worden bewaard dan nodig is voor het doel waarvoor ze zijn verzameld.  Zoals Adobe in februari in zijn klantencommunicatie heeft uiteengezet, zullen we voor de meeste klanten een 25-maandenplan voor dataretentie aanhouden, tenzij er andere regelingen zijn getroffen (die aan de klant moeten worden gemeld en door de klant moeten worden goedgekeurd). Klanten moeten hun dataretentiebeleid instellen voordat Adobe een Data Privacy-aanvraag kan verwerken.

In Adobe Analytics moeten klanten hun dataretentie instellen om hun Data Privacy-aanvragen te kunnen verwerken. Het huidige dataretentiebeleid van elke rapportsuite wordt weergegeven in de nieuwe Data Governance-beheergebruikersinterface. Klanten moeten contact opnemen met hun Adobe-vertegenwoordiger als ze hun dataretentiebeleid willen aanpassen. Zie [Veelgestelde vragen over Adobe Analytics-gegevensbewaring](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html?lang=en).

+++

+++ **Kan een klant de standaardperiode voor dataretentie verkorten of verlengen?**

Klanten kunnen verzoeken om hun data eerder dan 25 maanden te laten verwijderen door contact op te nemen met de klantenservice. Klanten kunnen de dataretentie verlengen tot meer dan 25 maanden door een uitbreiding aan te schaffen. Uitbreidingen zijn beschikbaar in stappen van 1 (één) extra jaar, tot maximaal 8 (acht) extra jaren (in totaal 10 jaar). Voor deze verlengingen zijn mogelijk wijzigingen in de contractvoorwaarden en extra kosten vereist.

+++

+++ **Met welke privacyoverwegingen moet een datacontrolleraccount rekening houden wanneer persoonlijke data uit Adobe Analytics worden geëxporteerd?**

Als een klant Adobe Analytics-datafeeds gebruikt om data van Analytics naar zijn of haar bedrijfsdatawarehouse of naar andere systemen buiten Adobe te exporteren, is het de verantwoordelijkheid van de klant (de datacontroller) om ervoor te zorgen dat verwijderingsaanvragen op de data worden toegepast. Dit geldt ook voor on-premise implementaties van de Data Workbench van de Adobe, waar een lopende de gegevensvoer van Adobe Analytics de gegevens van de Data Workbench bevolkt. Adobe kan tools bieden voor het zoeken naar en verwijderen van de records uit bepaalde soorten datafeeds, zoals data die worden gebruikt voor Data Workbench, maar het is nog steeds de verantwoordelijkheid van de klant (datacontroller) om ervoor te zorgen dat de data worden verwijderd in overeenstemming met hun eigen, interne beleid voor dataretentie en dataverwijdering.

Houd ook rekening met gevallen waarin medewerkers Adobe Analytics-rapporten hebben gedownload die persoonlijke data bevatten. Deze rapporten moeten mogelijk worden bijgewerkt of verwijderd als er een Data Privacy-gerelateerde aanvraag voor verwijdering is ontvangen die een id betreft die in het rapport zou kunnen staan. Klanten kunnen het best samenwerken met de juridische adviseur van uw bedrijf om retentieperioden vast te stellen en de privacy- en beveiligingsvereisten te bepalen die op deze soorten documenten moeten worden toegepast.

+++

+++ **Sommige data die we niet hadden moeten verzamelen, zijn per ongeluk naar Adobe Analytics verzonden. Kunnen we de Data Privacy-API gebruiken om deze data op te schonen?**

De [API voor Privacy Service van gegevens](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) is verstrekt om u te helpen verzoeken van de Privacy van Gegevens vervullen, die tijdgevoelig zijn. Het gebruik van deze API voor andere doeleinden wordt niet ondersteund door Adobe en kan een nadelige invloed hebben op de snelheid waarmee Adobe door de gebruiker geïnitieerde Data Privacy-aanvragen met hoge prioriteit voor andere Adobe-klanten kan afhandelen. We vragen u de Data Privacy-API niet te gebruiken voor andere doeleinden, zoals het wissen van data die per ongeluk zijn verzonden tussen grote groepen bezoekers. Bedenk ook dat voor bezoekers die een treffer hebben verwijderd (bijgewerkt of geanonimiseerd) als gevolg van een Data Privacy-verwijderingsaanvraag, de statusgegevens worden hersteld. De volgende keer dat de bezoeker uw website bezoekt, wordt deze een nieuwe bezoeker. Alle eVar-attributie wordt opnieuw gestart, evenals informatie als aantal bezoeken, referrers, bezochte eerste pagina, enz. Dit bijeffect is ongewenst in situaties waarin u datavelden wilt wissen, en legt de nadruk op één reden waarom de Data Privacy-API niet geschikt is voor dit gebruik.

Neem contact op met uw accountmanager (CSM) om samen met het consultingteam van onze engineering-architect verder te controleren en zich in te spannen voor het verwijderen van eventuele PII- of dataproblemen.

+++

+++ **Ons juridisch team heeft vastgesteld dat waarden die we al jaren verzamelen in een variabele, niet meer voldoen aan ons bijgewerkte privacybeleid. Kunnen we de Data Privacy-API gebruiken om alle waarden uit deze variabele te verwijderen?**

De [API voor Privacy Service van gegevens](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) is verstrekt om u te helpen verzoeken van de Privacy van Gegevens vervullen, die tijdgevoelig zijn. Het gebruik van deze API voor andere doeleinden wordt niet ondersteund door Adobe en kan een nadelige invloed hebben op de snelheid waarmee Adobe door de gebruiker geïnitieerde Data Privacy-aanvragen met hoge prioriteit voor andere Adobe-klanten kan afhandelen. We vragen u de Data Privacy-API niet te gebruiken voor andere doeleinden, zoals het wissen van data die per ongeluk zijn verzonden tussen grote groepen bezoekers.

Bedenk ook dat voor bezoekers die een treffer hebben verwijderd (bijgewerkt of geanonimiseerd) als gevolg van een Data Privacy-verwijderingsaanvraag, de statusgegevens worden hersteld. De volgende keer dat de bezoeker uw website bezoekt, wordt deze een nieuwe bezoeker. Alle eVar-attributie wordt opnieuw gestart, evenals informatie als aantal bezoeken, referrers, bezochte eerste pagina, enz. Dit bijeffect is ongewenst in situaties waarin u datavelden wilt wissen, en legt de nadruk op één reden waarom de Data Privacy-API niet geschikt is voor dit gebruik.

Neem contact op met uw accountmanager (CSM) om samen te werken met ons consultatieteam van de Engineering Architect om verdere revisie uit te voeren en de moeite te leveren om eventuele problemen met PII&#39;s of gegevens te verwijderen.

+++


Aanvullende Data Privacy-bronnen:

* [Algemene voorwaarden GDPR](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_commonterms.pdf)
* Experience Cloud Data Privacy [Care Package](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_carepackage.pdf)
* Experiential Privacy [Blogpost](https://theblog.adobe.com/experiential-privacy-an-investment-opportunity-for-the-experience-business/)
