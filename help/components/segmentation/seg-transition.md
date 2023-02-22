---
description: Veelgestelde vragen over het beheer van oudere segmenten.
title: Veelgestelde vragen over verouderde segmenten
feature: Segmentation
exl-id: 316e2a2e-55d3-4c23-9985-9a6d90390e86
source-git-commit: 83542d77b26e5fdf7545e4deced35da84263848b
workflow-type: tm+mt
source-wordcount: '1446'
ht-degree: 1%

---

# Veelgestelde vragen over verouderde segmenten

Beantwoord frequente vragen over beste praktijken voor het beheren van erfenissegmenten - segmenten die vóór 2014 werden gecreeerd.

## Oudere segmenten beheren {#legacy}

+++ **Wat gebeurde er met mijn bestaande segmenten?**

Uw bestaande segmenten blijven werken zoals voorheen. Om het even welke rapporten die deze toegepaste segmenten hebben zullen blijven correct werken. [Meer...](/help/components/segmentation/seg-transition.md)

De meeste vroegere vooraf bepaalde en reekssegmenten zullen over als segmentmalplaatjes in de Bouwer van het Segment worden gemigreerd. Segmentsjablonen worden gebruikt om snel aangepaste segmenten te maken met een veel voorkomend publiek. De malplaatjes van het segment kunnen niet rechtstreeks op een rapport worden toegepast, maar zij kunnen gemakkelijk aan een douanesegment worden bewaard.

Segmentsjablonen worden gemarkeerd met een speciaal pictogram in Segment Builder:

![](assets/seg_templates.png)

+++

+++ **Wat gebeurde met geplande rapporten die toegepaste segmenten hebben?**

De geplande rapporten blijven behoorlijk met de segmenten lopen die u bepaalde.

Wanneer u een segment schrapt, blijven de geplande rapporten en de dashboards die dit segment hebben toegepast normaal werken, d.w.z. het segment of dashboard blijft het geschrapte segment gebruiken.

Geplande rapporten worden niet bijgewerkt wanneer u een segment met dezelfde naam bewerkt. Hier volgt een voorbeeld: Stel dat u twee segmenten met dezelfde naam in verschillende rapportsuites hebt:

![](assets/duplicate_seg_names.png)

U hebt een referentie die naar het segment voor de belangrijkste rapportreeks verwijst. Dan schrapt u dat segment omdat het een duplicaat is. De bladwijzer blijft lopen, verwijzend naar de definitie van het geschrapte segment. Als u de segmentdefinitie voor het maindev-segment wijzigt en Catalina Island en Tijuana Mexico opneemt, verandert het segment dat op de bladwijzer is toegepast niet. De oude definitie wordt gebruikt. Als u dit wilt corrigeren, werkt u de bladwijzer bij en verwijst u naar de nieuwe definitie. Als u niet zeker bent of een referentie, dashboard of gepland rapport een geschrapt segment gebruikt, kon u de naam van het resterende segment veranderen zodat is het duidelijker of de referentie het resterende segment gebruikt.

+++

+++ **Wat gebeurde er met de segmenten van de Data Warehouse?**

Alle bestaande segmenten van de Data Warehouse werken nog steeds in de Data Warehouse. De meeste segmenten van Data Warehouse werken ook in andere componenten, zoals Analysis Workspace en Reports &amp; Analytics.

U kunt een nieuwe segmenten van de Data Warehouse in de de segmentbouwer/manager tot stand brengen of uitgeven. Het mechanisme van de Verenigbaarheid van het Product in de Bouwer van het Segment bepaalt automatisch of een segment met Data Warehouse compatibel is.

+++

+++ **Wat gebeurde met pre-gevormde Segmenten?**

* **Bezoeken van één pagina**
* **Bezoeken van mobiele apparaten**
* **Bezoeken van Natuurlijk zoeken**
* **Bezoeken van Betaalde zoekopdracht**
* **Bezoeken met cookie van bezoeker-id**

Deze segmenten zullen over als segmentmalplaatjes in de Bouwer van het Segment worden gemigreerd. Bestaande rapporten waarop deze segmenten zijn toegepast, blijven correct werken.

+++

+++ **Wat is er met de segmenten Experience Cloud (Suite) gebeurd:**

* Niet-aankoopcentrales
* Aankopers
* Eerste bezoeken
* Bezoeken van sociale sites
* Bezoeken van meer dan 10 minuten*
* Bezoeken met 5+ vorige bezoeken*
* Bezoeken van Facebook*

De meeste van deze segmenten (behalve de segmenten gemarkeerd met een asterisk *) werden gemigreerd over als segmentsjablonen in de segmentbuilder. Bovendien zijn verscheidene nieuwe segmentmalplaatjes toegevoegd.

Bestaande rapporten waarop deze segmenten zijn toegepast, werken nog steeds correct.

+++

+++ **Wat gebeurde er met Admin-segmenten (ook wel &quot;algemene&quot; segmenten genoemd)?**

**Beheer** De segmenten zullen in de nieuwe segmentinterface worden gemigreerd en zullen verschijnen als segmenten die met iedereen worden gedeeld.

De eigenaar van deze segmenten wordt ingesteld op de beheerder met de oudste account in de lijst met beheergebruikers van het aanmeldingsbedrijf. Alle beheerders kunnen deze segmenten echter verwijderen, bewerken en delen.

De interface van het segmentbeheer in de Admin Console waar Admins creeerde en deze globale segmenten beheerde niet meer beschikbaar is. Beheerders moeten nu de nieuwe segmentbuilder gebruiken om segmenten te maken en deze te delen met de juiste groepen of personen of met iedereen.

Bestaande segmenten die logica gebruiken die is gewijzigd zoals beschreven in dit document, blijven correct werken, hoewel ze moeten worden bijgewerkt voordat ze opnieuw kunnen worden opgeslagen. Bijvoorbeeld, als u een bestaand segment hebt waar de Staten van de VS &quot;New York&quot;bevatten, blijft het correct werken, hoewel de volgende keer u het segment uitgeeft zult u het moeten bijwerken om het opgesomde type met een gelijke voorwaarde te gebruiken.

+++

+++ **Wat zou ik met dubbele segmenten moeten doen die de zelfde naam hebben maar verschillende definities kunnen hebben?**
Nu de segmenten in veelvoudige rapportreeksen werken, zou u kunnen vinden dat u veelvoudige segmenten met de zelfde naam hebt. We raden u aan

* Naam wijzigen van segmenten met dezelfde naam, maar met andere definities, of
* Segmenten verwijderen die niet meer nodig zijn.

+++

+++ **Wat adviseert Adobe met betrekking tot het schoonmaken van segmenten?**

* Label alle segmenten met verouderde tag.
* Bekijk de segmenten die u hebt.
* Voeg deze waar van toepassing toe aan de segmentbibliotheek.
* Goedkeuren van canonieke segmenten.
* Segmenten labelen volgens [best practices](/help/components/segmentation/segmentation-workflow/seg-workflow.md).

+++

### Migratietips

Aan de hand van de volgende tips kunt u veel voorkomende afmetingen migreren:

* Geo-city/region/country - zoek naar en selecteer specifieke steden, regio&#39;s of landen in plaats van een gedeeltelijke match.
* Browsers - gebruik de dimensie Browsertypen om alle browsers in een type op te halen, bijvoorbeeld Google Chrome
* Besturingssystemen - gebruik de afmetingen voor besturingssysteemtypen om alle besturingssystemen in een type op te halen, bijvoorbeeld Microsoft Windows.
* Zie &quot;Nieuwe en hernoemde Dimension&quot; (zie hieronder).

## Nieuwe en hernoemde Dimension {#renamed}

De volgende lijst bevat een lijst van afmetingen die in de Bouwer van het Segment anders werden genoemd.

| Nieuwe naam Dimension | Vorige naam | Notities |
|--- |--- |--- |
| Typen besturingssystemen | Nieuw | Toegevoegd in het voorjaar van 2015. |
| Browserbreedte - Emmerd | Browserbreedte | Deze dimensie is compatibel met alle interfaces en wordt gesplitst in een opgesomde lijst met bereiken in plaats van specifieke gehele getallen. Als u specifieke waarden moet segmenteren, gebruik de korrelversie van deze dimensie in een segment van het gegevenspakhuis. |
| Browserhoogte - Emmerd | Browserhoogte | Deze dimensie is compatibel met alle interfaces en wordt gesplitst in een opgesomde lijst met bereiken in plaats van specifieke gehele getallen. Als u specifieke waarden moet segmenteren, gebruik de korrelversie van deze dimensie in een segment van het gegevenspakhuis. |
| Browserbreedte - korrelig | Browserbreedte | Dit werd anders genoemd en is nu compatibel met slechts gegevenspakhuis. Wanneer het bepalen van segmenten die met alle interfaces compatibel zijn, gebruik het opgesomde type, Browser Breedte - Embleekt. |
| Browserhoogte - korrelig | Browserhoogte | Dit werd anders genoemd en is nu compatibel met slechts gegevenspakhuis. Wanneer het bepalen van segmenten die met alle interfaces compatibel zijn, gebruik het opgesomde type, Browser Hoogte - Embleet. |
| Cookie-ondersteuning | Cookies | - |
| Kleurdiepte | Kleurdiepte monitor | - |
| - | &quot;App - *&quot; | de &quot;App -&quot;-voorvoegsels zijn verwijderd uit een aantal typen dimensies. Aangezien gegevens van mobiele apps doorgaans worden vastgelegd in een rapportsuite die geen webgegevens bevat, waren deze voorvoegsels niet nodig. |
| Oorspronkelijke invoerpagina | Oorspronkelijke invoerpagina | - |
| Java ingeschakeld | Java | - |
| Maximale URL browser voor mobiel | URL-lengte mobiele browser | - |
| Decoratie van mobiele e-mail | Ondersteuning voor e-mail voor mobiele decoratie | - |
| Mobiel apparaat | Naam van mobiel apparaat | - |
| Maximale bladwijzerlengte voor mobiel | Maximale URL bladwijzer voor mobiel | - |
| Maximale e-maillengte voor mobiele apparaten | Max. URL-lengte mobiele post | - |
| Mobiel besturingssysteem (afgekeurd) | Mobiel besturingssysteem | Gebruik de dimensie van het besturingssysteem en pas in plaats daarvan bezoeken toe vanuit segmenten voor mobiele apparaten. |
| Mobiel pushbericht om te spreken | Mobiele PTT | - |
| Beoordelingsweergaven | Totaal aantal beoordelingsweergaven | - |
| Antwoorden enquête | Totaal aantal enquêtereacties | - |
| Diepte bezoeken | Padlengte | - |
| Postcode | Postcode | - |

{style=&quot;table-layout:auto&quot;}

## Veranderingen in op koord-Gebaseerde Dimension die Bekende Waarden hebben {#string-based-dims}

Op tekenreeks gebaseerde afmetingen met een bekende set waarden zijn gewijzigd in opsommingstypen. Wanneer u een segment maakt met deze afmetingen, wordt de lijst vooraf gevuld met alle bekende waarden en wordt alleen de operator ondersteund voor gelijkheid gebruikt. Zo kunt u snel de exacte waarden segmenteren die u zoekt, zonder dat u onbedoelde waarden hoeft te selecteren wanneer u minder restrictieve overeenkomsten gebruikt.

De volgende afmetingen zijn gewijzigd in opsommingslijsten:

| Naam Dimension | Naam Dimension | Naam Dimension |
| --- | --- | --- |
| mobiele fabrikant | mobiele e-maillengte | kleurdiepte |
| grootte mobiel scherm | nummer mobiel apparaat | monitorresolutie |
| hoogte mobiel scherm | mobiele druk om te praten | insteekmodule |
| ondersteuning voor mobiele cookies | versiering van mobiele post | besturingssysteem |
| ondersteuning voor mobiele afbeeldingen | mobiele informatiediensten | verwijzingstype |
| mobiele kleurdiepte | type mobiel apparaat | zoekmachine |
| ondersteuning voor mobiele audio | browsertype | state |
| ondersteuning voor mobiele video | browser | geo |
| mobiele drm | verbindingstype | geo |
| mobiele netprotocollen | mobiele provider | geo |
| mobiele apparaten | koekje | geo dma |
| mobiele java vm | klantentrouw | permanente cookie |
| lengte van mobiele bladwijzer | java ingeschakeld | betaalde zoekopdracht |
| mobiele URL-lengte | taal |  |

## Wijzigingen in Dimension op basis van gehele getallen met bekende waarden {#integer-based-dims}

Op gehele getallen gebaseerde afmetingen (zoals de breedte van de browser) met een bekende set waarden zijn opgedeeld in opsommingsbereiken, zodat u snel segmenten voor een bepaald bereik kunt definiëren. Deze opsommingslijsten worden toegevoegd met &quot; - Emmerd&quot;na de afmetingsnaam. Het volgende scherm toont hoe deze afmetingen gebruikend de vorige en nieuwe segmentbouwerinterfaces worden gesegmenteerd:

![](assets/seg_browser_dimension.png)

De operatoren kleiner dan, groter dan en vergelijkbaar zijn nu alleen compatibel met segmenten van de Data Warehouse. Segmenten die compatibel moeten zijn met alle rapporteringsinterfaces, moeten de &quot;Emmerde&quot; versie van de metrische methode gebruiken met de gelijknamige operator.
