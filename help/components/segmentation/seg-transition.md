---
description: Veelgestelde vragen over het beheer van oudere segmenten.
title: Veelgestelde vragen over oudere segmenten
feature: Segmentation
exl-id: 316e2a2e-55d3-4c23-9985-9a6d90390e86
source-git-commit: 80e4a3ba4a5985563fcf02acf06997b4592261e4
workflow-type: tm+mt
source-wordcount: '1441'
ht-degree: 0%

---

# Veelgestelde vragen over oudere segmenten

Dit artikel beantwoordt vaak gestelde vragen over beste praktijken voor het beheren van erfenissegmenten (segmenten die vóór 2014 werden gecreeerd).

## Oudere segmenten beheren {#legacy}

+++ **wat met mijn bestaande segmenten gebeurde?**

Uw bestaande segmenten blijven werken zoals voorheen. Om het even welke rapporten die deze toegepaste segmenten hebben zullen blijven correct werken.

De meeste vroegere vooraf bepaalde en reekssegmenten zullen over als segmentmalplaatjes in de bouwer van het Segment worden gemigreerd. Segmentsjablonen worden gebruikt om snel aangepaste segmenten te maken met een veel voorkomend publiek. De malplaatjes van het segment kunnen niet rechtstreeks op een rapport worden toegepast, maar zij kunnen gemakkelijk aan een douanesegment worden bewaard.

Segmentsjablonen worden gemarkeerd met een speciaal pictogram in Segment Builder:

![](assets/seg_templates.png)

+++

+++ **wat gebeurde met geplande rapporten die toegepaste segmenten hebben?**

De geplande rapporten blijven behoorlijk met de segmenten lopen die u bepaalde.

Wanneer u een segment schrapt, blijven de geplande rapporten en de dashboards die dit segment hebben toegepast normaal werken, d.w.z. het segment of dashboard blijft het geschrapte segment gebruiken.

Geplande rapporten worden niet bijgewerkt wanneer u een segment met dezelfde naam bewerkt. Hier is een voorbeeld: Stel dat u twee segmenten met dezelfde naam in verschillende rapportsuites hebt:

![](assets/duplicate_seg_names.png)

U hebt een referentie die naar het segment voor de belangrijkste rapportreeks verwijst. Dan schrapt u dat segment omdat het een duplicaat is. De bladwijzer zal blijven lopen, verwijzend naar de definitie van het geschrapte segment. Als u de segmentdefinitie voor het maindev-segment wijzigt en Catalina Island en Tijuana Mexico opneemt, verandert het segment dat op de bladwijzer is toegepast niet. De oude definitie wordt gebruikt. Als u dit wilt corrigeren, werkt u de bladwijzer bij en verwijst u naar de nieuwe definitie. Als u niet zeker bent of een referentie, dashboard of gepland rapport een geschrapt segment gebruikt, kon u de naam van het resterende segment veranderen zodat is het duidelijker of de referentie het resterende segment gebruikt.

+++

+++ **wat gebeurde met de segmenten van Data Warehouse?**

Alle bestaande Data Warehouse-segmenten werken nog steeds in Data Warehouse. De meeste Data Warehouse-segmenten werken ook in andere componenten, zoals Analysis Workspace.

U kunt nieuwe Data Warehouse-segmenten maken of bewerken in de gesegmenteerde builder/manager. Het mechanisme van de Verenigbaarheid van het Product in de bouwer van het Segment bepaalt automatisch of een segment met Data Warehouse compatibel is.

+++

+++ **wat met pre-gevormde Segmenten gebeurde?**

* **Enige Bezoeken van de Pagina**
* **bezoeken van Mobiele Apparaten**
* **bezoeken van Natuurlijk Onderzoek**
* **bezoeken van Betaald Onderzoek**
* **bezoeken met de Koekje van identiteitskaart van de Bezoeker**

Deze segmenten worden als segmentsjablonen gemigreerd naar de Segmentbuilder. Bestaande rapporten waarop deze segmenten zijn toegepast, blijven correct werken.

+++

+++ **wat met de segmenten van Experience Cloud (Suite) gebeurde:**

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

+++ **wat gebeurde met segmenten Admin (die ook als &quot;Globale&quot;segmenten worden bekend)?**

**Admin** segmenten zullen in de nieuwe segmentinterface worden gemigreerd en zullen verschijnen als segmenten die met iedereen worden gedeeld.

De eigenaar van deze segmenten wordt ingesteld op de beheerder met de oudste account in de lijst met beheergebruikers van het aanmeldingsbedrijf. Alle beheerders kunnen deze segmenten echter verwijderen, bewerken en delen.

De interface van het segmentbeheer in Admin Console waar Admins creeerde en deze globale segmenten beheerde niet meer beschikbaar is. Beheerders moeten nu de nieuwe segmentbuilder gebruiken om segmenten te maken en deze te delen met de juiste groepen of personen of met iedereen.

Bestaande segmenten die logica gebruiken die is gewijzigd zoals beschreven in dit document, blijven correct werken, hoewel ze moeten worden bijgewerkt voordat ze opnieuw kunnen worden opgeslagen. Bijvoorbeeld, als u een bestaand segment hebt waar de Staten van de VS &quot;New York&quot;bevatten, blijft het correct werken, hoewel de volgende keer u het segment uitgeeft zult u het moeten bijwerken om het opgesomde type met een gelijke voorwaarde te gebruiken.

+++

+++ **wat zou ik met dubbele segmenten moeten doen die de zelfde naam maar verschillende definities hebben?**
Nu de segmenten in veelvoudige rapportreeksen werken, zou u kunnen vinden dat u veelvoudige segmenten met de zelfde naam hebt. We raden u aan

* Naam wijzigen van segmenten met dezelfde naam, maar met andere definities, of
* Segmenten verwijderen die niet meer nodig zijn.

+++

+++ **wat adviseert Adobe met betrekking tot het schoonmaken van segmenten?**

* Label alle segmenten met verouderde tag.
* Bekijk de segmenten die u hebt.
* Voeg deze waar van toepassing toe aan de segmentbibliotheek.
* Goedkeuren van canonieke segmenten.
* De segmenten van de markering volgens [ beste praktijken ](/help/components/segmentation/segmentation-workflow/seg-workflow.md).

+++

### Migratietips

Aan de hand van de volgende tips kunt u veel voorkomende afmetingen migreren:

* Geo-city/region/country - zoek naar en selecteer specifieke steden, regio&#39;s of landen in plaats van een gedeeltelijke match.
* Browsers - gebruik de dimensie Browsertypen om alle browsers in een type op te halen, bijvoorbeeld Google Chrome
* Besturingssystemen - gebruik de afmetingen voor besturingssysteemtypen om alle besturingssystemen in een type op te halen, bijvoorbeeld Microsoft Windows.
* Zie &quot;Nieuwe afmetingen en hernoemde afmetingen&quot; (zie hieronder).

## Nieuwe en hernoemde afmetingen {#renamed}

De volgende lijst bevat een lijst van afmetingen die in de bouwer van het Segment anders werden genoemd.

| Nieuwe Dimension-naam | Vorige naam | Notities |
|--- |--- |--- |
| Typen besturingssystemen | Nieuw | Toegevoegd in voorjaar 2015. |
| Browserbreedte - Emmerd | Browserbreedte | Deze dimensie is compatibel met alle interfaces en wordt gesplitst in een opgesomde lijst met bereiken in plaats van specifieke gehele getallen. Als u specifieke waarden moet segmenteren, gebruik de korrelversie van deze dimensie in een segment van het gegevenspakhuis. |
| Browserhoogte - Emmerd | Browserhoogte | Deze dimensie is compatibel met alle interfaces en wordt gesplitst in een opgesomde lijst met bereiken in plaats van specifieke gehele getallen. Als u specifieke waarden moet segmenteren, gebruik de korrelversie van deze dimensie in een segment van het gegevenspakhuis. |
| Browserbreedte - korrelig | Browserbreedte | Dit werd anders genoemd en is nu compatibel met slechts gegevenspakhuis. Wanneer het bepalen van segmenten die met alle interfaces compatibel zijn, gebruik het opgesomde type, Browser Breedte - Embleekt. |
| Browserhoogte - korrelig | Browserhoogte | Dit werd anders genoemd en is nu compatibel met slechts gegevenspakhuis. Wanneer het bepalen van segmenten die met alle interfaces compatibel zijn, gebruik het opgesomde type, Browser Hoogte - Embleet. |
| Cookie-ondersteuning | Cookies | - |
| Kleurdiepte | Kleurdiepte monitor | - |
| - | &quot;App - *&quot; | de &quot;App -&quot;-voorvoegsels zijn verwijderd uit een aantal typen dimensies. Aangezien gegevens van mobiele apps doorgaans worden vastgelegd in een rapportsuite die geen webgegevens bevat, waren deze voorvoegsels niet nodig. |
| Origineel van invoerpagina | Oorspronkelijke invoerpagina | - |
| Java ingeschakeld | Java | - |
| Maximale URL browser voor mobiel | URL-lengte mobiele browser | - |
| Decoratie van mobiele e-mail | Ondersteuning voor e-mail voor mobiele decoratie | - |
| Mobiel apparaat | Naam van mobiel apparaat | - |
| Maximale bladwijzerlengte voor mobiel | Maximale URL bladwijzer voor mobiele apparaten | - |
| Maximale e-maillengte voor mobiele apparaten | Max. URL-lengte mobiele post | - |
| Mobiel besturingssysteem (afgekeurd) | Mobiel besturingssysteem | Gebruik de dimensie van het besturingssysteem en pas in plaats daarvan bezoeken toe vanuit segmenten voor mobiele apparaten. |
| Mobiel pushbericht om te spreken | Mobiele PTT | - |
| Beoordelingsweergaven | Totaal aantal beoordelingsweergaven | - |
| Antwoorden enquête | Totaal aantal enquêtereacties | - |
| Diepte bezoeken | Lengte pad | - |
| Postcode | Postcode | - |

{style="table-layout:auto"}

## Wijzigingen in op een tekenreeks gebaseerde afmetingen met bekende waarden {#string-based-dims}

Op tekenreeks gebaseerde afmetingen met een bekende set waarden zijn gewijzigd in opsommingstypen. Wanneer u een segment maakt met deze afmetingen, wordt de lijst vooraf gevuld met alle bekende waarden en wordt alleen de operator ondersteund voor gelijkheid gebruikt. Zo kunt u snel de exacte waarden segmenteren die u zoekt zonder onbedoelde waarden te selecteren bij het gebruik van minder restrictieve overeenkomsten.

De volgende afmetingen zijn gewijzigd in opsommingslijsten:

| Dimension-naam | Dimension-naam | Dimension-naam |
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

## Wijzigingen in op gehele getallen gebaseerde afmetingen met bekende waarden {#integer-based-dims}

Op gehele getallen gebaseerde afmetingen (zoals de breedte van de browser) met een bekende set waarden zijn opgedeeld in opsommingsbereiken, zodat u snel segmenten voor een bepaald bereik kunt definiëren. Deze opsommingslijsten worden toegevoegd met &quot; - Emmerd&quot;na de afmetingsnaam. Het volgende scherm toont hoe deze afmetingen gebruikend de vorige en nieuwe segmentbouwerinterfaces worden gesegmenteerd:

![](assets/seg_browser_dimension.png)

De operatoren kleiner dan, groter dan en vergelijkbaar zijn nu alleen compatibel met Data Warehouse-segmenten. Segmenten die compatibel moeten zijn met alle rapporteringsinterfaces, moeten de &quot;Emmerde&quot; versie van de metrische methode gebruiken met de gelijknamige operator.
