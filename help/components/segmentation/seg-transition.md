---
description: Begrijp hoe te om erfenissegmenten te beheren.
title: Veelgestelde vragen over verouderde segmenten
feature: Segmentation
exl-id: 316e2a2e-55d3-4c23-9985-9a6d90390e86
source-git-commit: c44bffa45ab8ed29ea28b91b2b3dc51811ab25fe
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 0%

---

# Oudere segmenten

Dit artikel beantwoordt vaak gestelde vragen over beste praktijken voor het beheren van erfenissegmenten. Oudere segmenten zijn segmenten die vóór 2014 zijn gemaakt.

## Oudere segmenten beheren {#legacy}

+++ **wat met mijn bestaande segmenten gebeurde?**

Uw bestaande segmenten werken nog steeds zoals voorheen. Om het even welke rapporten die deze toegepaste segmenten hebben blijven correct werken.

De meeste vroegere vooraf bepaalde en reekssegmenten worden gemigreerd over als segmentmalplaatjes in de bouwer van het Segment. Segmentsjablonen worden gebruikt om snel aangepaste segmenten te maken met een veel voorkomend publiek. De malplaatjes van het segment kunnen niet rechtstreeks op een rapport worden toegepast, maar zij kunnen gemakkelijk aan een douanesegment worden bewaard.

De malplaatjes van het segment zijn duidelijk met een speciaal pictogram ![ AdobeLogoSmall ](/help/assets/icons/AdobeLogoSmall.svg) in de bouwer van het Segment.



+++

+++ **wat gebeurde met geplande rapporten die toegepaste segmenten hebben?**

De geplande rapporten blijven behoorlijk met de segmenten lopen die u bepaalde.

Wanneer u een segment schrapt, blijven de geplande rapporten en de dashboards die dit segment hebben toegepast normaal werken, d.w.z. het segment of dashboard blijft het geschrapte segment gebruiken.

Geplande rapporten worden niet bijgewerkt wanneer u een segment met dezelfde naam bewerkt. Hier is een voorbeeld: Stel dat u twee segmenten met dezelfde naam in verschillende rapportsuites hebt:

![](assets/duplicate_seg_names.png)

U hebt een visualisatie die verwijzingen het segment voor de **[!UICONTROL mainprod]** rapportreeks. Dan schrapt u dat segment omdat het een duplicaat is. De visualisatie wordt verder uitgevoerd en verwijst naar de definitie van het verwijderde segment. Als u de segmentdefinitie voor het maindev-segment wijzigt en Catalina Island en Tijuana, Mexico opneemt, verandert het segment dat wordt toegepast op de visualisatie niet en gebruikt het de oude definitie. Als u de nieuwe definitie wilt gebruiken, werkt u de visualisatie bij en verwijst u naar de nieuwe definitie. Als u onzeker bent of een visualisatie, een project of een gepland rapport een geschrapt segment gebruikt, verander de naam van het resterende segment om te tonen of de visualisatie het resterende segment gebruikt.

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

Deze segmenten worden gemigreerd over als segmentmalplaatjes in de bouwer van het Segment. Bestaande rapporten waarop deze segmenten zijn toegepast, werken nog steeds correct.

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

**Admin** segmenten worden gemigreerd in de nieuwe segmentinterface en verschijnen omhoog als segmenten die met iedereen worden gedeeld.

De eigenaar van deze segmenten wordt ingesteld op de beheerder met de oudste account van de gebruikers van de beheerder. Alle beheerders kunnen deze segmenten echter verwijderen, bewerken en delen.

De interface van het segmentbeheer in Admin Console waar Admins creeerde en deze globale segmenten beheerde niet meer beschikbaar is. Beheerders moeten nu de nieuwe segmentbuilder gebruiken om segmenten te maken en deze te delen met de juiste groepen of personen of met iedereen.

Bestaande segmenten die logica gebruiken die is gewijzigd zoals beschreven in dit document, blijven correct werken, hoewel de segmenten moeten worden bijgewerkt voordat ze opnieuw kunnen worden opgeslagen. Als u bijvoorbeeld een bestaand segment hebt waarin **[!UICONTROL US States]** **[!UICONTROL contains]** `New York` voorkomt, blijft dat segment correct werken. De volgende keer dat u het segment bewerkt, moet u het segment bijwerken om het opgesomde type te gebruiken met een voorwaarde **[!UICONTROL equals]** .

+++

+++ **wat zou ik met dubbele segmenten moeten doen die de zelfde naam maar verschillende definities hebben?**
Nu de segmenten in veelvoudige rapportreeksen werken, zou u kunnen vinden dat u veelvoudige segmenten met de zelfde naam hebt. U moet:

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

Aan de hand van de volgende tips kunt u veelvoorkomende afmetingen migreren:

* Geo-city/region/country - zoek naar en selecteer specifieke steden, regio&#39;s of landen in plaats van een gedeeltelijke match.
* Browsers - gebruik de dimensie Browsertypen om alle browsers in een type op te halen, bijvoorbeeld Google Chrome
* Besturingssystemen - gebruik de afmetingen voor besturingssysteemtypen om alle besturingssystemen van een type op te halen, bijvoorbeeld Microsoft Windows.
* Zie &quot;Nieuwe afmetingen en hernoemde afmetingen&quot; (zie hieronder).

## Nieuwe en hernoemde afmetingen {#renamed}

De volgende lijst bevat een lijst van afmetingen die in de bouwer van het Segment anders werden genoemd.

| Nieuwe Dimension-naam | Vorige naam | Notities |
|--- |--- |--- |
| Typen besturingssystemen | Nieuw | Toegevoegd in voorjaar 2015. |
| Browserbreedte - Emmerd | Browserbreedte | Deze dimensie is compatibel met alle interfaces en wordt gesplitst in een opgesomde lijst met bereiken in plaats van specifieke gehele getallen. Als u specifieke waarden moet segmenteren, gebruikt u de granulaire versie van deze dimensie in een Data Warehouse-segment. |
| Browserhoogte - Emmerd | Browserhoogte | Deze dimensie is compatibel met alle interfaces en wordt gesplitst in een opgesomde lijst met bereiken in plaats van specifieke gehele getallen. Als u specifieke waarden moet segmenteren, gebruikt u de granulaire versie van deze dimensie in een Data Warehouse-segment. |
| Browserbreedte - korrelig | Browserbreedte | De naam van deze dimensie is gewijzigd en is nu alleen compatibel met Data Warehouse. Wanneer het bepalen van segmenten die met alle interfaces compatibel zijn, gebruik het opgesomde type, Browser Breedte - Embleekt. |
| Browserhoogte - korrelig | Browserhoogte | De naam van deze dimensie is gewijzigd en is nu alleen compatibel met Data Warehouse. Wanneer het bepalen van segmenten die met alle interfaces compatibel zijn, gebruik het opgesomde type, Browser Hoogte - Embleet. |
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

Op tekenreeks gebaseerde afmetingen met een bekende set waarden zijn gewijzigd in opsommingstypen. Wanneer u een segment maakt met deze afmetingen, wordt de lijst vooraf gevuld met alle bekende waarden en wordt alleen **[!UICONTROL equals]** ondersteund. Met deze reeks waarden kunt u snel de exacte waarden segmenteren die u zoekt, zonder dat u onbedoelde waarden hoeft te selecteren wanneer u minder restrictieve overeenkomsten gebruikt.

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

Op gehele getallen gebaseerde afmetingen (zoals de breedte van de browser) met een bekende set waarden worden gesplitst in opsommingsbereiken, zodat u snel segmenten voor een bepaald bereik kunt definiëren. Deze opsommingslijsten worden toegevoegd met &quot; - Emmerd&quot;na de afmetingsnaam. Het volgende scherm toont hoe deze afmetingen gebruikend de vorige en nieuwe segmentbouwerinterfaces worden gesegmenteerd:

![](assets/seg_browser_dimension.png)

De operatoren kleiner dan, groter dan en vergelijkbaar zijn nu alleen compatibel met Data Warehouse-segmenten. Segmenten die compatibel moeten zijn met alle rapporteringsinterfaces, moeten de &quot;Emmerde&quot; versie van de metrische waarde gebruiken met de operator **[!UICONTROL equals]** .
