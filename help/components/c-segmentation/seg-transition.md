---
description: 'null'
keywords: segmentation;segments
title: Veelgestelde vragen
topic: Segments
uuid: f49dc829-1d53-4183-9add-1aeaa5219d89
translation-type: tm+mt
source-git-commit: ''

---


# Veelgestelde vragen

Beantwoord frequente vragen over segmentatiefuncties, toegang, machtigingen, beste praktijken en het beheren van verouderde segmenten.

## Functies {#section_BD58629D1A9346BF879E229FA6BEC7A2}

* Segmentering in analysewerkruimte:

   * U kunt segmenten [](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/segment-comparison.html)vergelijken.
   * Gebruik [segmenten als afmetingen](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/segments_as_dimensions.html) in een vergelijking.
   * Gebruik segmenten in [uitvalanalyse](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/graphics/compare-segments-fallout.html).

* U kunt veelvoudige segmenten [toepassen op een rapport of een project](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md).
* De segmenten zijn universeel aan alle rapportseries.
* De [Segment Builder](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md) vereenvoudigt het maken van segmenten.
* Met [Segmentbeheer](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md) kunt u [workflows](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md) instellen met functies voor het delen van segmenten, codering, verificatie en goedkeuring.

* U kunt segmenten [](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md) labelen om ze later te ordenen en te doorzoeken in plaats van mappen te gebruiken. Eerder hebt u mappen (in [!DNL Ad Hoc Analysis]) gebruikt om uw segmenten te ordenen.

* U kunt [Opeenvolgende Segmenten](/help/components/c-segmentation/c-segmentation-workflow/seg-sequential-build.md) buiten Ad hoc Analyse tot stand brengen.
* De naam van de container Paginaweergave is gewijzigd in de container Actief om aan te geven dat in deze container alle typen gegevens worden gesegmenteerd, en niet alleen de paginaweergaven. De aanroepen voor het bijhouden van koppelingen en trackhandelingen van de mobiele SDK&#39;s worden bijvoorbeeld allemaal opgenomen of uitgesloten in de aanraakcontainer. Merk op dat er geen verandering in de manier was deze container werkt - het werd eenvoudig anders genoemd.

Zie het artikel [Improving Segmentation in Adobe Analytics](https://blogs.adobe.com/digitalmarketing/analytics/improving-segmentation-adobe-analytics/) op het Digital Marketing Blog voor meer informatie.

## Toegang tot de segmentatiehulpmiddelen {#section_088AD0E4E21943DFA8CF7206AEC485DD}

**Hoe kan ik de Segment Builder bereiken?**

U kunt tot de Bouwer van het Segment toegang hebben door:

* Een bestaand rapport weergeven en klikken op het pictogram Segmenten ![](assets/segment_icon.png) in de linkernavigatie. In het segment dat wordt weergegeven, klikt u op **[!UICONTROL Add]** of

* Klik boven aan Segmentbeheer op **[!UICONTROL + Add]**.  ![](assets/add_button.png)

   of

* Klik op een bestaande segmenttitel in Segmentbeheer om het segment te bewerken in Segmentbouwer.

**Hoe kan ik Segmentbeheer openen?**

Toegang tot Segmentbeheer via:

* Ga naar **[!UICONTROL Analytics]** **[!UICONTROL Components]** > in de bovenste navigatie. Klik vervolgens **[!UICONTROL Segments]** of

* Een bestaand rapport weergeven en klikken op het pictogram Segmenten ![](assets/segment_icon.png) in de linkernavigatie. Klik vervolgens **[!UICONTROL Manage]** of

* Druk op de schuine streep &#39;/&#39; in de interface en zoek naar segmentmanager.

**Waar ging het verouderde segment neerzetten?**

De segmentdrop-down in Rapporten &amp; Analytics is vervangen door een veel meer eigenschaprijke [interface van de Bouwer](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md) van het Segment die u toestaat om &quot;universele&quot;segmenten tot stand te brengen bruikbaar over rapportreeksen en over de oplossingen van de Analytics van Adobe. Als u een lijst met bestaande segmenten wilt weergeven, klikt u op het pictogram Segmenten ![](assets/segment_icon.png)

in de linkernavigatie en de vertoningen van de segmentspoorstaaf.

**Waar ging de verouderde rapportsuite?**

De vervolgkeuzelijst met rapportsuite is verplaatst naast de datumkiezer in de rechterbovenhoek van elk rapport of dashboard.

![](assets/report_suite_selector.png)

## Machtigingen {#section_648DFA3A882146C485A84ED014EEC707}

**Welke rechten en voorrechten moet ik gebruiken, creëren, en segmenten beheren?**

Standaard kunnen alle gebruikers persoonlijke segmenten maken en bewerken. Nochtans, kunnen de Beheerders beslissen wie [toestemmingen zou moeten hebben om segmenten](https://marketing.adobe.com/resources/help/en_US/reference/groups.html) tot stand te brengen en hen aan specifieke groepen kunnen toewijzen. Deze segmenten kunnen rechtstreeks met andere gebruikers van Analytics worden gedeeld.

Beheerders kunnen elk segment bewerken en segmenten delen met groepen en met iedereen in de organisatie. [Meer...](/help/components/c-segmentation/seg-reference/seg-rights.md)

**Kan ik alle segmenten in mijn bedrijf zien?**

Ja, Admins kan alle segmenten binnen de [!DNL Analysis Workspace] [!DNL Reports & Analytics] en gebruikersinterfaces zien.

De ad hoc Analysesegmenten en de vertoningssegmenten van de Bouwer van het Rapport die u bezit en segmenten die met u worden gedeeld.

**Kan ik alle segmenten Analytics in de Manager van het Segment beheren?**

Ja, kunnen alle segmenten in de Manager van het Segment in de Werkruimte van de Analyse, Rapporten &amp; Analytics en Ad hoc Analyse worden beheerd. Segmentbeheer geeft segmenten weer die zichtbaar zijn voor de eigenaar (gebruiker die het segment heeft gemaakt), gedeelde gebruikers en beheerders. De segmentkiezer geeft segmenten weer die eigendom zijn van en gedeeld worden met de gebruiker.

Admins kunnen alle segmenten binnen de Werkruimte van de Analyse en [!DNL Reports & Analytics] gebruikersinterfaces zien.

De ad hoc Analyse en van de Bouwer van het Rapport tonen slechts segmenten die door u of segmenten worden gebouwd die specifiek met u zijn gedeeld.

**Waarom kan ik dit segment niet verwijderen?**

Als het segment is [gepubliceerd naar de Experience Cloud](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md), kunt u het niet verwijderen of bewerken. U kunt de gekopieerde versie echter wel kopiëren en bewerken.

## Aanbevolen werkwijzen {#section_E2C3A1B4B4274D1B86CAA9C0359D049C}

**Wat zou ik met dubbele segmenten moeten doen die de zelfde naam hebben maar verschillende definities kunnen hebben?**
Nu de segmenten in veelvoudige rapportreeksen werken, zou u kunnen vinden dat u veelvoudige segmenten met de zelfde naam hebt. We raden u aan

* Naam wijzigen van segmenten met dezelfde naam, maar met andere definities, of
* Segmenten verwijderen die niet meer nodig zijn.

**Wat raadt Adobe aan voor het opschonen van segmenten?**

* Label alle segmenten met verouderde tag.
* Bekijk de segmenten die u hebt.
* Voeg deze waar van toepassing toe aan de segmentbibliotheek.
* Goedkeuren van canonieke segmenten.
* Segmenten labelen volgens de [aanbevolen procedures](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md).

## Oudere segmenten beheren {#section_76CF47142D1A4FB6A0718AD9073049FE}

**Wat gebeurde er met mijn bestaande segmenten?**

Uw bestaande segmenten blijven werken zoals voorheen. Om het even welke rapporten die deze toegepaste segmenten hebben zullen blijven correct werken. [Meer...](/help/components/c-segmentation/seg-transition.md)

De meeste vroegere vooraf bepaalde en reekssegmenten zullen over als segmentmalplaatjes in de Bouwer van het Segment worden gemigreerd. Segmentsjablonen worden gebruikt om snel aangepaste segmenten te maken met een veel voorkomend publiek. De malplaatjes van het segment kunnen niet rechtstreeks op een rapport worden toegepast, maar zij kunnen gemakkelijk aan een douanesegment worden bewaard.

Segmentsjablonen worden gemarkeerd met een speciaal pictogram in Segment Builder:

![](assets/seg_templates.png)

**Wat gebeurde er met mijn bestaande segmentmappen?**

In plaats van mappen voor ad hoc analyse gebruikt Segmentbeheer tags. De mapnamen worden automatisch omgezet in tags en deze tags worden toegepast op de respectievelijke segmenten.

**Wat gebeurde met geplande rapporten die toegepaste segmenten hebben?**

De geplande rapporten blijven behoorlijk met de segmenten lopen die u bepaalde.

Wanneer u een segment schrapt, blijven de geplande rapporten en de dashboards die dit segment hebben toegepast normaal werken, d.w.z. het segment of dashboard blijft het geschrapte segment gebruiken.

Geplande rapporten worden niet bijgewerkt wanneer u een segment met dezelfde naam bewerkt. Hier volgt een voorbeeld: Stel dat u twee segmenten met dezelfde naam in verschillende rapportsuites hebt:

![](assets/duplicate_seg_names.png)

U hebt een referentie die naar het segment voor de belangrijkste rapportreeks verwijst. Dan schrapt u dat segment omdat het een duplicaat is. De bladwijzer blijft lopen, verwijzend naar de definitie van het geschrapte segment. Als u de segmentdefinitie voor het maindev-segment wijzigt en Catalina Island en Tijuana Mexico opneemt, verandert het segment dat op de bladwijzer is toegepast niet. De oude definitie wordt gebruikt. Als u dit wilt corrigeren, werkt u de bladwijzer bij en verwijst u naar de nieuwe definitie. Als u niet zeker bent of een referentie, dashboard of gepland rapport een geschrapt segment gebruikt, kon u de naam van het resterende segment veranderen zodat is het duidelijker of de referentie het resterende segment gebruikt.

**Wat gebeurt er met de segmenten van Data Warehouse?**

Alle bestaande segmenten van Data Warehouse werken nog in Data Warehouse. De meeste segmenten van het Pakhuis van Gegevens zullen ook in andere componenten zoals de Werkruimte van de Analyse, Ad hoc Analyse en Rapporten &amp; Analytics werken.

U kunt een nieuwe segmenten van het Pakhuis van Gegevens in de segmentbouwer/de manager tot stand brengen of uitgeven. Het mechanisme van de Verenigbaarheid van het Product in de Bouwer van het Segment bepaalt automatisch of een segment met het Pakhuis van Gegevens compatibel is.

**Wat gebeurt er met de Segmenten van Favorieten (ad hoc Analyse)?**

Deze ad hoc segmenten van de Analyse worden getoond als regelmatige segmenten in de Analytics van Adobe.

Zij zouden niet met de eigenschap van Favorieten in de Manager van het Segment moeten worden verward die u segmenten als favorieten laat merken.

**Wat gebeurt er met vooraf geconfigureerde segmenten?**

* **Bezoeken van één pagina**
* **Bezoeken van mobiele apparaten**
* **Bezoeken van Natuurlijk zoeken**
* **Bezoeken van Betaalde zoekopdracht**
* **Bezoeken met cookie van bezoeker-id**

Deze segmenten zullen over als segmentmalplaatjes in de Bouwer van het Segment worden gemigreerd.

Bestaande rapporten waarop deze segmenten zijn toegepast, blijven correct werken.

**Wat gebeurt er met de segmenten Experience Cloud (Suite):**

* Niet-aankoopcentrales
* Aankopers
* Eerste bezoeken
* Bezoeken van sociale sites
* Bezoeken van meer dan 10 minuten*
* Bezoeken met 5+ vorige bezoeken*
* Bezoeken van Facebook*

De meeste van deze segmenten (met uitzondering van de segmenten die met een asterisk * zijn gemarkeerd) worden als segmentsjablonen gemigreerd naar de segmentbuilder. Bovendien zijn verscheidene nieuwe segmentmalplaatjes toegevoegd.

Bestaande rapporten waarop deze segmenten zijn toegepast, blijven correct werken.

**Wat gebeurt er met Admin-segmenten (ook wel &quot;algemene&quot; segmenten genoemd)?**

**De segmenten Admin** zullen in de nieuwe segmentinterface worden gemigreerd en zullen verschijnen als segmenten die met iedereen worden gedeeld.

De eigenaar van deze segmenten wordt ingesteld op de beheerder met de oudste account in de lijst met beheergebruikers van het aanmeldingsbedrijf. Alle beheerders kunnen deze segmenten echter verwijderen, bewerken en delen.

De interface voor segmentbeheer in de beheerconsole, waar Admins deze algemene segmenten heeft gemaakt en beheerd, is niet meer beschikbaar. Beheerders moeten nu de nieuwe segmentbuilder gebruiken om segmenten te maken en deze te delen met de juiste groepen of personen of met iedereen.

<!-- 

seg_definition.xml

 -->

Bestaande segmenten die logica gebruiken die is gewijzigd zoals beschreven in dit document, blijven correct werken, hoewel ze moeten worden bijgewerkt voordat ze opnieuw kunnen worden opgeslagen. Bijvoorbeeld, als u een bestaand segment hebt waar de Staten van de VS &quot;New York&quot;bevatten, blijft het correct werken, hoewel de volgende keer u het segment uitgeeft zult u het moeten bijwerken om het opgesomde type met een gelijke voorwaarde te gebruiken.

**Migratietips**

Aan de hand van de volgende tips kunt u veel voorkomende afmetingen migreren:

* Geo-city/region/country - zoek naar en selecteer specifieke steden, regio&#39;s of landen in plaats van een gedeeltelijke match.
* Browsers - gebruik de dimensie Browsertypen om alle browsers in een type op te halen, bijvoorbeeld Google Chrome
* Besturingssystemen - gebruik de afmetingen voor besturingssysteemtypen om alle besturingssystemen in een type op te halen, bijvoorbeeld Microsoft Windows.

* [Nieuwe en hernoemde afmetingen](/help/components/c-segmentation/seg-transition.md#section_73CF121B64A24DEF8E6499F3167BF742)
* [Wijzigingen in Bevat](/help/components/c-segmentation/seg-transition.md#section_1A9EDEE5CBC44B5AA6262560052ABE77)
* [Wijzigingen in Kleiner dan en Groter dan](/help/components/c-segmentation/seg-transition.md#section_84A8AAD0344148AD9F9211D3EB271903)

## Nieuwe en hernoemde afmetingen {#section_73CF121B64A24DEF8E6499F3167BF742}

De volgende lijst bevat een lijst van afmetingen die in de Bouwer van het Segment anders werden genoemd.

<table id="table_1A8C1940FD0446FA8414C6A7DE66E44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nieuwe naam dimensie </th> 
   <th colname="col2" class="entry"> Vorige naam </th> 
   <th colname="col3" class="entry"> Notities </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Typen besturingssystemen </td> 
   <td colname="col2"> Nieuw </td> 
   <td colname="col3"> Toegevoegd in het voorjaar van 2015. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browserbreedte - Emmerd </td> 
   <td colname="col2"> Browserbreedte </td> 
   <td colname="col3"> Deze dimensie is compatibel met alle interfaces en wordt gesplitst in een opgesomde lijst met bereiken in plaats van specifieke gehele getallen. Als u specifieke waarden moet segmenteren, gebruik de korrelversie van deze dimensie in een segment van het gegevenspakhuis. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browserhoogte - Emmerd </td> 
   <td colname="col2"> Browserhoogte </td> 
   <td colname="col3"> Deze dimensie is compatibel met alle interfaces en wordt gesplitst in een opgesomde lijst met bereiken in plaats van specifieke gehele getallen. Als u specifieke waarden moet segmenteren, gebruik de korrelversie van deze dimensie in een segment van het gegevenspakhuis. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browserbreedte - korrelig </td> 
   <td colname="col2"> Browserbreedte </td> 
   <td colname="col3"> <p>Dit werd anders genoemd en is nu compatibel met slechts gegevenspakhuis. Wanneer het bepalen van segmenten die met alle interfaces compatibel zijn, gebruik het opgesomde type, Browser Breedte - Embleekt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browserhoogte - korrelig </td> 
   <td colname="col2"> Browserhoogte </td> 
   <td colname="col3"> <p>Dit werd anders genoemd en is nu compatibel met slechts gegevenspakhuis. Wanneer het bepalen van segmenten die met alle interfaces compatibel zijn, gebruik het opgesomde type, Browser Hoogte - Embleet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Cookie-ondersteuning </td> 
   <td colname="col2"> Cookies </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kleurdiepte </td> 
   <td colname="col2"> Kleurdiepte monitor </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> - </td> 
   <td colname="col2"> "App - *" </td> 
   <td colname="col3"> de "App -"-voorvoegsels zijn verwijderd uit een aantal typen dimensies. Aangezien gegevens van mobiele apps doorgaans worden vastgelegd in een rapportsuite die geen webgegevens bevat, waren deze voorvoegsels niet nodig. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Oorspronkelijke invoerpagina </td> 
   <td colname="col2"> Oorspronkelijke invoerpagina </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Java ingeschakeld </td> 
   <td colname="col2"> Java </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maximale URL browser voor mobiel </td> 
   <td colname="col2"> URL-lengte mobiele browser </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Decoratie van mobiele e-mail </td> 
   <td colname="col2"> Ondersteuning voor e-mail voor mobiele decoratie </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobiel apparaat </td> 
   <td colname="col2"> Naam van mobiel apparaat </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maximale bladwijzerlengte voor mobiel </td> 
   <td colname="col2"> Maximale URL bladwijzer voor mobiel </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maximale e-maillengte voor mobiele apparaten </td> 
   <td colname="col2"> Max. URL-lengte mobiele post </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobiel besturingssysteem (afgekeurd) </td> 
   <td colname="col2"> Mobiel besturingssysteem </td> 
   <td colname="col3"> Gebruik de dimensie van het besturingssysteem en pas in plaats daarvan bezoeken toe vanuit segmenten voor mobiele apparaten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobiel pushbericht om te spreken </td> 
   <td colname="col2"> Mobiele PTT </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beoordelingsweergaven </td> 
   <td colname="col2"> Totaal aantal beoordelingsweergaven </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Antwoorden enquête </td> 
   <td colname="col2"> Totaal aantal enquêtereacties </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Diepte bezoeken </td> 
   <td colname="col2"> Lengte pad </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Postcode </td> 
   <td colname="col2"> Postcode </td> 
   <td colname="col3"> - </td> 
  </tr> 
 </tbody> 
</table>

## Veranderingen in op koord-Gebaseerde Dimensies die Bekende Waarden hebben {#section_1A9EDEE5CBC44B5AA6262560052ABE77}

Op tekenreeks gebaseerde afmetingen met een bekende set waarden zijn gewijzigd in opsommingstypen. Wanneer u een segment maakt met deze afmetingen, wordt de lijst vooraf gevuld met alle bekende waarden en wordt alleen de operator ondersteund voor gelijkheid gebruikt. Zo kunt u snel de exacte waarden segmenteren die u zoekt, zonder dat u onbedoelde waarden hoeft te selecteren wanneer u minder restrictieve overeenkomsten gebruikt.

De volgende afmetingen zijn gewijzigd in opsommingslijsten:

| mobiele fabrikant | mobiele e-maillengte | kleurdiepte |
|---|---|---|
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

## Veranderingen in op geheel-gebaseerde afmetingen die Bekende Waarden hebben {#section_84A8AAD0344148AD9F9211D3EB271903}

Op gehele getallen gebaseerde afmetingen (zoals de breedte van de browser) met een bekende set waarden zijn opgedeeld in opsommingsbereiken, zodat u snel segmenten voor een bepaald bereik kunt definiëren. Deze opsommingslijsten worden toegevoegd met &quot; - Emmerd&quot;na de afmetingsnaam. Het volgende scherm toont aan hoe deze afmetingen gebruikend de vorige en nieuwe segmentbouwerinterfaces worden gesegmenteerd:

![](assets/seg_browser_dimension.png)

De operatoren kleiner dan, groter dan en vergelijkbaar zijn nu alleen compatibel met de segmenten Data Warehouse. Segmenten die compatibel moeten zijn met alle rapporteringsinterfaces, moeten de &quot;Emmerde&quot; versie van de metrische methode gebruiken met de gelijknamige operator.
