---
description: Veelgestelde vragen over Advertising Analytics.
title: Veelgestelde vragen voor reclameanalyses
feature: Advertising Analytics
exl-id: 664a5641-1c79-439f-a9fb-2ff134574412
source-git-commit: 6bedfb9b1333a442bf17cf71dad1e0883b97fd45
workflow-type: tm+mt
source-wordcount: '1294'
ht-degree: 0%

---

# Veelgestelde vragen

## Toegang/rechten {#access}

+++ Moet ik een klant van Adobe Advertising Cloud of Adobe Advertising Cloud (AMO) zijn om toegang te krijgen tot deze functionaliteit?

Nee, deze functionaliteit is beschikbaar voor klanten die geen advertenties in de cloud of in een andere omgeving aanbieden.

AMO-klanten kunnen gebruikmaken van de bestaande integratie tussen Analytics en AMO; ze kunnen Ad Analytics niet gebruiken.

+++

+++ Welke Adobe Analytics SKU&#39;s geven u het recht om Advertising Analytics te gebruiken?

Advertising Analytics is beschikbaar voor Adobe Analytics

* [&#x200B; Uitgezocht &#x200B;](https://www.adobe.com/nl/data-analytics-cloud/analytics/select.html)

* [&#x200B; Prime &#x200B;](https://www.adobe.com/nl/data-analytics-cloud/analytics/prime.html)

* [&#x200B; Ultimate &#x200B;](https://www.adobe.com/nl/data-analytics-cloud/analytics/ultimate.html)

+++

+++ Moet ik extra betalen om Advertising Analytics te gebruiken?

Nee, buiten de juiste SKU-provisioning maakt Advertising Analytics geen extra kosten.

+++

+++ Telt Advertising Analytics op mijn gebruik van de servervraag

Nee, Advertising Analytics gebruikt een speciaal gegevensbrontype dat geen kosten veroorzaakt voor serveraanroepen.

+++

+++ Als ik al gebruik van Advertising Cloud/AMO, kan ik dan nog steeds de Advertising Analytics-functionaliteit gebruiken?

Elk compatibel account voor zoekmachines wordt doorgegeven aan Advertising Analytics en wordt weergegeven als alleen-lezen. Alle bewerkingen of updates moeten worden verwerkt in de cloud/AMO voor advertenties.

+++

+++ Ik bezit de juiste SKU, maar ik heb geen toegang tot Advertising Analytics, waarom is dat?

Advertising Analytics is alleen beschikbaar voor Adobe Analytics-beheerders; beheerders kunnen echter toegang verlenen aan niet-beheerders. Neem contact op met uw beheerder voor toegangsrechten.

+++

## Advertising Analytics gebruiken {#using}

+++ Welke rekeningen van zoekprogramma&#39;s zijn opgenomen in Advertising Analytics?

Motoraccounts zijn onder andere Google Ads en Microsoft Advertising.

+++

+++ Waar ga ik naar Advertising Analytics?

Nadat u zich hebt aangemeld bij Adobe Analytics, navigeert u naar de map [!UICONTROL Admin] . Selecteer vervolgens [!UICONTROL Advertising Analytics] om uw zoekprogrammaaccounts toe te voegen.

+++

+++ Hoe worden de gegevens verzameld en doorgegeven aan Analytics?

Advertising Analytics gebruikt een aantal aangepaste API&#39;s om gegevens van zoekprogramma&#39;s via de Adobe Advertising Cloud door te geven aan Analytics.

+++

+++ Welke zoekgegevens krijg ik met deze integratie?

U krijgt

* Impressies
* Klikken
* Kosten
* Kwaliteitsscore
* Gemiddelde positie rechtstreeks vanuit de zoekmachines, en
* Instanties van AMO-id (klik op Instanties).

+++

+++ Kan ik mijn Advertising Analytics-gegevens onderbreken door andere Analytics-gegevens (metriek/afmetingen)?

Nee, de onbewerkte zoekgegevens worden opgenomen als een onafhankelijke gegevensset. Nochtans, is er een versie van Instanties van de klikgegevens die door andere gegevens van Analytics kunnen worden verdeeld.

+++ Wat is de definitie van de verschillende statusindicatoren voor mijn accounts (in behandeling, actief, gepauzeerd, enz.)? Elk van deze statusindicatoren identificeert de levenscyclusfase van elk onderzoek motorrekening.

* [!UICONTROL Pending]
* [!UICONTROL Paused] betekent dat de account eerder is ingesteld, maar dat deze niet actief is.
* [!UICONTROL Active] betekent dat de account volledig is ingesteld en zoekgegevens aantrekt.

+++

+++ Ik probeer mijn Advertising Analytics-accounts toe te wijzen aan een specifieke rapportsuite, maar deze is niet beschikbaar in het modaal rapportenpakket. Waarom?

Alvorens u een rapportreeks aan een rekening van Advertising Analytics kunt toewijzen, moet de gewenste rapportreeks [&#x200B; worden voorzien voor Advertising Analytics die &#x200B;](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md) rapporteert
Dit gebeurt via een aparte beheerpagina die u kunt vinden op: Beheer > Rapportagesuites > `[select report suite]` > Instellingen bewerken > Advertising Analytics-configuratie.

+++

+++ Is het mogelijk om een virtuele rapportsuite aan een Advertising Analytics-account toe te wijzen?

Met virtuele rapportsets worden geen gegevens verzameld, zodat u een Advertising Analytics-account niet rechtstreeks kunt toewijzen aan een Virtual Report-suite. U kunt de Advertising Analytics-account echter toewijzen aan de bovenliggende rapportsuite van de Virtual Report Suite waarin u gegevens wilt zien. De metriek van de Motor van het Onderzoek (klik/kosten/impressies) kunnen niet in de Virtuele rapportreeks verschijnen tenzij u een &quot;of&quot;voorwaarde in uw segmentlogica opneemt die op AMO ID (of zijn classificatie) wordt gebaseerd. Voorbeeld: het toevoegen van &quot;alle treffers waar AMO ID bestaat&quot; zou de metriek van de onderzoeksmotor in het segment omvatten.

+++

+++ Zijn de metriek van Advertising Analytics rapporteerbaar in het *Marketing Kanalen* rapport?

Nr, zijn zij niet inbegrepen in het rapport van de Kanalen van de Marketing.

+++

+++ Wanneer worden de zoekgegevens naar Analytics gehaald?

De zoekgegevens worden uit de zoekmachines gehaald rond 6AM (06:00) in de tijdzone van uw datacenter Analytics. Dit is wanneer de gegevens van AMO worden verzameld en in de rapportreeks opgenomen. Het wordt dan omgezet in de tijdzone van de rapportreeks als deel van het opnemen van de gegevens in Analytics.

+++

+++ Wat kan *worden gevangen vóór de klik*? Zien we indrukken, kosten, gemiddelde positie, enzovoort? zelfs zonder klik ?

De AMO-id legt de maatstaven van de zoekmachine vast: Impressies, Kosten, Klikken, Gemiddelde positie en Gemiddelde kwaliteitsscore. Als er geen kliks zijn, maar er indrukken zijn, dan zullen de beeld/positie/kwaliteitsscore gegevens nog naar Analytics worden verzonden. Doorgaans zijn er ook geen kosten verbonden als er niet wordt geklikt.

+++

+++ Op welk niveau worden deze gegevens vastgelegd? *Bezoeker? Hit?*

De metriek van de motor van het Onderzoek wordt gevangen op het raakniveau en met AMO identiteitskaart (en zijn classificaties) verbonden. Dit zijn gegevens op overzichtsniveau die geen verband houden met bezoeken/bezoekers. Als zodanig kunnen de metriek van de zoekmachine slechts in segmenten worden gebruikt die bereik op raakniveau zijn en op AMO-id (of zijn classificaties) gebaseerd zijn.

De AMO-id wordt ook vastgelegd op de bestemmingspagina in de hit voor die pagina (die de id verbindt met het bezoek/de bezoeker) en zal verderop in de stroom blijven staan om krediet te krijgen voor andere analytische gegevens (totdat deze verlopen of door een nieuwe AMO-id wordt overschreven). Net als alle andere eVar is het volledig in de gegevensset opgenomen.

+++

+++ Vanggen wij slechts google.com of *landversies* (als google.co.uk, google.it, google.fr, of google.de) eveneens?

De classificatie van het Platform van de Advertentie vangt deze waarden: &quot;Adwords van Google&quot;, en &quot;Bing Adds&quot;. De beste praktijk is om de landcode op te nemen in de naamgeving van campagnes. Vervolgens kunt u naar beneden of naar een segment filteren (bijvoorbeeld als alle campagnes beginnen met landcode_ en u vervolgens een segment maakt waarin Campagnes (AMO ID) beginnen met &quot;UK_&quot;, zodat u alleen gegevens voor het Verenigd Koninkrijk krijgt).

+++

+++ De metrische &quot;Kosten AMO&quot;is de kosten die voor elk sleutelwoord/elke advertentie worden betaald zoals die door het onderzoeksmotor worden gemeld. Zijn dit nettokosten of brutokosten?

&quot;AMO-kosten&quot; zijn alleen de kosten die aan de zoekmachines worden betaald. Hieronder vallen geen kosten voor het optimaliseren van de zoekopdracht of het beheerplatform.

+++

+++ Zijn er plannen om andere reclame kanalen zoals *Vertoning* of *Sociale* te omvatten?

Nee, op dit moment hebben we geen plannen voor deze andere kanalen op de routekaart.

+++


## Automatisch versus handmatig bijhouden {#section_7437C4698A6D482EB7ED94A948390119}

+++ Wanneer vestiging mijn rekening van Advertising, verklaart het dat *Auto het Volgen* tot onbedoelde gevolgen kan leiden. Welke gevolgen kunnen zich voordoen?

In de modus Automatisch wordt geprobeerd URL-parameters toe te voegen aan het einde van de volgende sjablonen/doel-URL&#39;s in de juiste indeling. Het is echter uw verantwoordelijkheid om ervoor te zorgen dat de toegevoegde URL-parameters correct blijven op de laatste bestemmingspagina. In de modus Automatisch kunnen sleutelwoorden worden ingevoegd in de bestemmings-URL en het is mogelijk dat uw webserver geen trefwoorden met speciale tekens ondersteunt.

+++

+++ Als ik eerst Handmatig of Automatisch bijhouden heb ingesteld, kan ik dan later overschakelen op de andere modus voor bijhouden? Wat zijn de gevolgen?

Ja kunt u overschakelen naar een andere modus voor bijhouden, maar u moet de oude logica voor bijhouden verwijderen voordat u de overstap maakt. Dit kan in wat onderbreking van het volgen op de dag resulteren de schakelaar wordt gemaakt (vooral als zich van hand aan automatisch beweegt). Daarom adviseren wij niet te schakelen tenzij absoluut noodzakelijk.

* Overschakelen van Handmatig naar Automatisch: verwijder de handmatige toevoegingen aan de trackingsjablonen en schakel vervolgens de schakeloptie in de gebruikersinterface van Advertising Analytics van handmatig naar Automatisch in en sla de instelling op. Het kan enkele uren duren voordat het systeem de automatische trackingcodes heeft ingevuld.

* Overschakelen van Automatisch naar Handmatig: Werk de schakeloptie van handmatig naar automatisch bij in de Advertising Analytics-instellingsinterface en implementeer de handmatige volgcodes zo snel mogelijk. Als u tijdens de implementatie van de handmatige volgcodes de automatische volgcodes in de sjablonen voor zoekprogramma&#39;s ziet, verwijdert u deze.

+++
