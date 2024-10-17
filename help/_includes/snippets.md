---
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '1214'
ht-degree: 0%

---
# Fragmenten

## Oudere Report Builder {#legacy-arb}

>[!IMPORTANT]
>
>Een nieuwe en gestroomlijnde [ Report Builder ](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/report-buider-overview) werd vrijgegeven op 16 oktober, 2024. Deze functie wordt ondersteund in Mac-, Windows- en webbrowsers.
>Deze verouderde invoegtoepassing voor Reporten Builder werkt nog steeds. U kunt [ uw erfeniswerkboeken ](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/convert-workbooks) in de nieuwe Report Builder omzetten.

## Rapporten &amp; Analytics-aankondiging aan het einde van de levensduur {#ra-eol}

>[!IMPORTANT]
>
>Effectieve **Januari 17, 2024**, beëindigde de Adobe Rapporten &amp; Analytics en zijn begeleidende rapporten en eigenschappen. Op dat moment werken de rapporten en analyses en alle bijbehorende rapporten en programma&#39;s niet meer. De rapporten, visualisaties en de onderliggende technologie die energierapporten &amp; analyses niet meer voldoen aan de technologienormen van de Adobe. De meeste functies voor rapporten en analyses zijn beschikbaar in Analysis Workspace. Voor informatie over het gebruiken van rapporten in Analysis Workspace, zie [ Gebruik pre-gebouwde rapporten ](/help/analyze/analysis-workspace/reports/use-reports.md).
> 
>Sinds de release van Analysis Workspace in 2015 zijn de functionaliteit en mogelijkheden van Rapporten en Analytics verplaatst naar Analysis Workspace en is een drempel voor pariteit van de workflow bereikt. Deze kennisgeving legt het einde van de levensduur uit.
>
>Lees meer over de Rapporten &amp; de aankondiging van het Eind van Analytics [ ](https://www.adobe.com/go/analytics_rnaeol_en).

## Criteria van het filter Gegevenswoordenboek {#dd-filter-criteria}

1. (Facultatief) selecteer het **pictogram van de Filter ![ van het Woordenboek van de Filter van de Filter ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg), dan om het even welke volgende filteropties om de lijst van componenten te filtreren:**

| Optie | Functie |
|---------|----------|
| [!UICONTROL **Goedgekeurd**] | Alleen componenten tonen die zijn gemarkeerd als goedgekeurd door een beheerder. |
| [!UICONTROL **Favorieten**] | Alleen componenten tonen die zich in de lijst Favorieten bevinden. Voor informatie over het toevoegen van componenten aan uw lijst van favorieten, zie [ Overzicht van Componenten ](/help/analyze/analysis-workspace/components/analysis-workspace-components.md). |
| [!UICONTROL **Dimensies**] | Alleen componenten weergeven die Dimensionen zijn. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) |
| [!UICONTROL **Cijfers**] | Alleen componenten weergeven die Metrisch zijn. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) |
| [!UICONTROL **Segmenten**] | Alleen componenten tonen die Segmenten zijn. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) <!--this is Filters in Customer Journey Analytics--> |
| [!UICONTROL **waaiers van de Datum**] | Alleen componenten tonen die Datumbereik hebben. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) |
| [!UICONTROL **toon allen**] | Alle componenten tonen. Deze optie is alleen beschikbaar voor beheerders. |
| [!UICONTROL **Niet goedgekeurd**] | Alleen componenten tonen die nog niet zijn gemarkeerd als goedgekeurd door een beheerder. Als beheerder, is dit nuttig wanneer het identificeren van componenten die uw overzicht en goedkeuring vereisen. Deze optie is alleen beschikbaar voor beheerders. |
| [!UICONTROL **Ontbrekende Beschrijving**] | Alleen componenten weergeven die nog geen beschrijving hebben in het veld Beschrijving. Deze optie is alleen beschikbaar voor beheerders. |
| [!UICONTROL **toon duplicaten**] | <p>Alleen componenten weergeven die dezelfde naam of dezelfde definitie hebben als een andere component in de geselecteerde rapportsuite. Namen of definities moeten exact overeenkomen om als duplicaten te kunnen worden weergegeven.</p><p>Deze optie is alleen beschikbaar voor beheerders.</p><p>**NOTA:** voor definities, omvat dit componenten u evenals die creeert die door Adobe worden verstrekt. Voor namen, omvat dit momenteel slechts componenten u creeert en niet die verstrekt door Adobe. Het tonen van dubbele namen voor Adobe-verstrekte componenten zal in een toekomstige versie worden toegevoegd.</p> |
| [!UICONTROL **Geen recente gegevens**] | Alleen componenten weergeven die de afgelopen 90 dagen geen gegevens hebben verzameld. Deze optie is alleen beschikbaar voor beheerders. |
| [!UICONTROL **die door Adobe**] wordt gecreeerd <!-- I don't see this option--> | Alleen componenten weergeven die zijn gemaakt door Adobe. Componenten die door een beheerder of een andere gebruiker in uw organisatie zijn gemaakt, worden niet weergegeven. |

{style="table-layout:auto"}

## Componenten gegevenswoordenboek {#dd-component-information}

| Optie | Functie |
|---------|----------|
| [!UICONTROL **Goedgekeurd**] | <p>Geeft aan dat de component is gecontroleerd en goedgekeurd door de beheerder.</p><p>Nadat een component wordt goedgekeurd, kunnen de beheerders goedkeuring verwijderen door de **Goedgekeurde** knoop te selecteren.</p> |
| [!UICONTROL **nodig Goedkeuring**] | <p>Geeft aan dat de component nog niet is gereviseerd en goedgekeurd door de beheerder.</p><p>De beheerders zien een optie [!UICONTROL **goedkeuren**]. Als u deze optie selecteert, wordt de component gemarkeerd als &quot;Goedgekeurd&quot; voor gebruikers.</p> |
| [!UICONTROL **Beschrijving**] | Beschrijft de voorgenomen functie van de component. (Deze informatie wordt toegevoegd door de beheerder van Analytics, zoals die in [ wordt beschreven voeg componentenbeschrijvingen ](/help/analyze/analysis-workspace/components/add-component-descriptions.md) toe.) |
| [!UICONTROL **vaak gebruikt met**] | <p>Geeft componenten weer die het meest worden gebruikt met de component die u bekijkt.</p><p>Tot 5 componenten worden getoond over de 5 primaire componententypes: Metrisch, Berekend Metrisch, Dimension, Segment, en de Waaier van de Datum.</p><p>Deze lijst is gebaseerd op gegevens uit de afgelopen 90 dagen. Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>De beheerders kunnen tot de componenten leiden die de gebruikers in deze sectie zien door de gewenste componenten in [!UICONTROL **te selecteren omvatten**] altijd en [!UICONTROL **sluit**] drop-down gebieden altijd uit. Alvorens u de componenten beheert die de gebruikers zien, pas eerst **toe tonen alle** filter om ervoor te zorgen u om het even welke componenten ziet die niet met u worden gedeeld.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p> |
| [!UICONTROL **Gelijkaardig aan**] | <p>Geeft componenten weer met vergelijkbare namen als de component die u bekijkt.</p><p>Tot 5 componenten worden getoond over de 5 primaire componententypes: Metrisch, Berekend Metrisch, Dimension, Segment, en de Waaier van de Datum.</p><p>Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Om het even welke dubbele componenten in uw rapportreeks ook hier tonen. De beheerders van Analytics zouden alle dubbele componenten moeten identificeren en verwijderen, zoals die in [ wordt beschreven de gezondheid van het Woordenboek van Gegevens van de Monitor ](/help/analyze/analysis-workspace/components/data-dictionary/monitor-data-dictionary-health.md).</p><p>De beheerders kunnen tot de componenten leiden die de gebruikers in deze sectie zien door de gewenste componenten in [!UICONTROL **te selecteren omvatten**] altijd en [!UICONTROL **sluit**] drop-down gebieden altijd uit. Alvorens u de componenten beheert die de gebruikers zien, pas eerst **toe tonen alle** filter om ervoor te zorgen u om het even welke componenten ziet die niet met u worden gedeeld.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p><p>**NOTA:** momenteel, **Gelijkaardig aan** sectie omvat slechts componenten u creeert en niet die verstrekt door Adobe. In een toekomstige release worden componenten toegevoegd die door de Adobe worden geleverd.</p> |
| [!UICONTROL **Markeringen**] | Hiermee worden alle tags weergegeven die op de component zijn toegepast. Gebruikers met beheerdersrechten kunnen tags toevoegen wanneer ze de component bewerken. |
| [!UICONTROL **Type van Component**] | Maakt een lijst van het type van component het is, hetzij een Dimension, een Metrisch, een Segment, of de Waaier van de Datum. |
| [!UICONTROL **die door**] wordt gecreeerd | Geeft de naam weer van de gebruiker die de component heeft gemaakt. |
| [!UICONTROL **Voorproef**] | Toont een voorproef van hoe de component in Analysis Workspace kijkt. |
| [!UICONTROL **Datum laatst gewijzigd**] | Hiermee geeft u de dag weer waarop de component voor het laatst is gewijzigd. Deze sectie wordt weergegeven wanneer u Segmenten, Berekende metriek en Datumbereiken weergeeft. |

{style="table-layout:auto"}

## Sorteeropties voor componenten {#components-sort-options}

| Optie | Functie |
|---------|----------|
| [!UICONTROL **geadviseerd**] | Hiermee sorteert u componenten met de componenten die boven aan de lijst worden aanbevolen. Componenten die het vaakst en het laatst door u of anderen in uw organisatie worden gebruikt, worden hoger weergegeven in de lijst. |
| [!UICONTROL **alfabetisch**] | Hiermee worden componenten alfabetisch gesorteerd. |
| [!UICONTROL **Categorisch**] | Sorteert componenten volgens componenttype (afmetingen, metrisch, segment, datumbereik). |

{style="table-layout:auto"}

## Beperkte tests voor releasefase {#release-limited-testing}

>[!AVAILABILITY]
>
>De functionaliteit die in dit artikel wordt beschreven, bevindt zich in de Beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het de versieproces van de Analyse, zie [ de eigenschapversies van Adobe Analytics ](/help/release-notes/releases.md).

## Beperkte testsectie voor releasefase {#release-limited-testing-section}

>[!AVAILABILITY]
>
>De in deze sectie beschreven functionaliteit bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het de versieproces van de Analyse, zie [ de eigenschapversies van Adobe Analytics ](/help/release-notes/releases.md).


## Dislaimer plug-in {#plug-in}

>[!IMPORTANT]
>
>Deze insteekmodule wordt door Adobe Consulting geleverd als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van de Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met het accountteam van de Adobe van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.


## Alleen beschikbaar voor bestaande klanten {#available-existing-customers}

>[!AVAILABILITY]
>
>De in deze sectie beschreven functionaliteit is alleen beschikbaar voor bestaande klanten die al een licentie voor de functionaliteit hebben. De functionaliteit wordt niet meer aangeboden als een extra toevoeging aan bestaande of nieuwe klanten.
>
