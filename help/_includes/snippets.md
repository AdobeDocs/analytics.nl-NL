---
source-git-commit: 33ac467cd73e3099ce0ca03aa41cbd4192eb2384
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 0%

---
# Fragmenten

## Rapporten &amp; Analytics-aankondiging aan het einde van de levensduur {#ra-eol}

>[!IMPORTANT]
>
>Effectief **17 januari 2024**, beëindigde de Adobe rapporten en analyses en de bijbehorende rapporten en functies. Op dat moment werken de rapporten en analyses en alle bijbehorende rapporten en programma&#39;s niet meer. De rapporten, visualisaties en de onderliggende technologie die energierapporten &amp; analyses niet meer voldoen aan de technologienormen van de Adobe. De meeste functies voor rapporten en analyses zijn beschikbaar in Analysis Workspace. Voor informatie over het gebruik van rapporten in Analysis Workspace raadpleegt u [Vooraf samengestelde rapporten gebruiken](/help/analyze/analysis-workspace/reports/use-reports.md).
> 
>Sinds de release van Analysis Workspace in 2015 zijn de functionaliteit en mogelijkheden van Rapporten en Analytics verplaatst naar Analysis Workspace en is een drempel voor pariteit van de workflow bereikt. Deze kennisgeving legt het einde van de levensduur uit.
>
>Meer informatie over rapporten en analyses [Aankondiging einde levensduur](https://www.adobe.com/go/analytics_rnaeol_en).

## Criteria van het filter Gegevenswoordenboek {#dd-filter-criteria}

1. (Optioneel) Selecteer de optie **Filter** pictogram ![Filter gegevenswoordenboek, pictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg)Selecteer vervolgens een van de volgende filteropties om de lijst met componenten te filteren:

| Optie | Functie |
|---------|----------|
| [!UICONTROL **Goedgekeurd**] | Alleen componenten tonen die zijn gemarkeerd als goedgekeurd door een beheerder. |
| [!UICONTROL **Favorieten**] | Alleen componenten tonen die zich in de lijst Favorieten bevinden. Voor informatie over het toevoegen van componenten aan uw lijst van favorieten, zie [Overzicht van componenten](/help/analyze/analysis-workspace/components/analysis-workspace-components.md). |
| [!UICONTROL **Dimensies**] | Alleen componenten weergeven die Dimensionen zijn. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
| [!UICONTROL **Cijfers**] | Alleen componenten weergeven die Metrisch zijn. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
| [!UICONTROL **Segmenten**] | Alleen componenten tonen die Segmenten zijn. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) <!--this is Filters in Customer Journey Analytics--> |
| [!UICONTROL **Datumbereiken**] | Alleen componenten tonen die Datumbereik hebben. (Deze optie is ook beschikbaar in het dialoogvenster [!UICONTROL **Snelle filters**] tabblad wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
| [!UICONTROL **Alles tonen**] | Alle componenten tonen. Deze optie is alleen beschikbaar voor beheerders. |
| [!UICONTROL **Niet goedgekeurd**] | Alleen componenten tonen die nog niet zijn gemarkeerd als goedgekeurd door een beheerder. Als beheerder, is dit nuttig wanneer het identificeren van componenten die uw overzicht en goedkeuring vereisen. Deze optie is alleen beschikbaar voor beheerders. |
| [!UICONTROL **Ontbrekende beschrijving**] | Alleen componenten weergeven die nog geen beschrijving hebben in het veld Beschrijving. Deze optie is alleen beschikbaar voor beheerders. |
| [!UICONTROL **Duplicaten tonen**] | <p>Alleen componenten weergeven die dezelfde naam of dezelfde definitie hebben als een andere component in de geselecteerde rapportsuite. Namen of definities moeten exact overeenkomen om als duplicaten te kunnen worden weergegeven.</p><p>Deze optie is alleen beschikbaar voor beheerders.</p><p>**OPMERKING:** Voor definities, omvat dit componenten u evenals die creeert die door Adobe worden verstrekt. Voor namen, omvat dit momenteel slechts componenten u creeert en niet die verstrekt door Adobe. Het tonen van dubbele namen voor Adobe-verstrekte componenten zal in een toekomstige versie worden toegevoegd.</p> |
| [!UICONTROL **Geen recente gegevens**] | Alleen componenten weergeven die de afgelopen 90 dagen geen gegevens hebben verzameld. Deze optie is alleen beschikbaar voor beheerders. |
| [!UICONTROL **Gemaakt door Adobe**] <!-- I don't see this option--> | Alleen componenten weergeven die zijn gemaakt door Adobe. Componenten die door een beheerder of een andere gebruiker in uw organisatie zijn gemaakt, worden niet weergegeven. |

{style="table-layout:auto"}

## Componenten gegevenswoordenboek {#dd-component-information}

| Optie | Functie |
|---------|----------|
| [!UICONTROL **Goedgekeurd**] | <p>Geeft aan dat de component is gecontroleerd en goedgekeurd door de beheerder.</p><p>Nadat een onderdeel is goedgekeurd, kunnen beheerders goedkeuring verwijderen door de optie **Goedgekeurd** knop.</p> |
| [!UICONTROL **Goedkeuring vereist**] | <p>Geeft aan dat de component nog niet is gereviseerd en goedgekeurd door de beheerder.</p><p>Beheerders zien een optie voor [!UICONTROL **Goedkeuren**]. Als u deze optie selecteert, wordt de component gemarkeerd als &quot;Goedgekeurd&quot; voor gebruikers.</p> |
| [!UICONTROL **Beschrijving**] | Beschrijft de voorgenomen functie van de component. (Deze informatie wordt toegevoegd door de beheerder van Analytics, zoals die in [Componentbeschrijvingen toevoegen](/help/analyze/analysis-workspace/components/add-component-descriptions.md).) |
| [!UICONTROL **Vaak gebruikt met**] | <p>Geeft componenten weer die het meest worden gebruikt met de component die u bekijkt.</p><p>Tot 5 componenten worden getoond over de 5 primaire componententypes: Metrisch, Berekend Metrisch, Dimension, Segment, en de Waaier van de Datum.</p><p>Deze lijst is gebaseerd op gegevens uit de afgelopen 90 dagen. Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Beheerders kunnen de componenten beheren die gebruikers in deze sectie zien door de gewenste componenten te selecteren in het dialoogvenster [!UICONTROL **Altijd opnemen**] en [!UICONTROL **Altijd uitsluiten**] vervolgkeuzelijsten. Voordat u de componenten beheert die gebruikers zien, moet u eerst de opdracht **Alles tonen** om ervoor te zorgen dat u componenten ziet die niet met u worden gedeeld.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p> |
| [!UICONTROL **Vergelijkbaar met**] | <p>Geeft componenten weer met vergelijkbare namen als de component die u bekijkt.</p><p>Tot 5 componenten worden getoond over de 5 primaire componententypes: Metrisch, Berekend Metrisch, Dimension, Segment, en de Waaier van de Datum.</p><p>Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Om het even welke dubbele componenten in uw rapportreeks ook hier tonen. Analysebeheerders moeten alle dubbele componenten identificeren en verwijderen, zoals beschreven in [Gezondheid gegevenswoordenboek controleren](/help/analyze/analysis-workspace/components/data-dictionary/monitor-data-dictionary-health.md).</p><p>Beheerders kunnen de componenten beheren die gebruikers in deze sectie zien door de gewenste componenten te selecteren in het dialoogvenster [!UICONTROL **Altijd opnemen**] en [!UICONTROL **Altijd uitsluiten**] vervolgkeuzelijsten. Voordat u de componenten beheert die gebruikers zien, moet u eerst de opdracht **Alles tonen** om ervoor te zorgen dat u componenten ziet die niet met u worden gedeeld.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p><p>**OPMERKING:** Op dit moment wordt **Vergelijkbaar met** Deze sectie bevat alleen componenten die u maakt en niet de componenten die door Adobe worden geleverd. In een toekomstige release worden componenten toegevoegd die door de Adobe worden geleverd.</p> |
| [!UICONTROL **Tags**] | Hiermee worden alle tags weergegeven die op de component zijn toegepast. Gebruikers met beheerdersrechten kunnen tags toevoegen wanneer ze de component bewerken. |
| [!UICONTROL **Componenttype**] | Maakt een lijst van het type van component het is, hetzij een Dimension, een Metrisch, een Segment, of de Waaier van de Datum. |
| [!UICONTROL **Gemaakt door**] | Geeft de naam weer van de gebruiker die de component heeft gemaakt. |
| [!UICONTROL **Voorvertoning**] | Toont een voorproef van hoe de component in Analysis Workspace kijkt. |
| [!UICONTROL **Datum van laatste wijziging**] | Hiermee geeft u de dag weer waarop de component voor het laatst is gewijzigd. Deze sectie wordt weergegeven wanneer u Segmenten, Berekende metriek en Datumbereiken weergeeft. |

{style="table-layout:auto"}

## Sorteeropties voor componenten {#components-sort-options}

| Optie | Functie |
|---------|----------|
| [!UICONTROL **Aanbevolen**] | Hiermee sorteert u componenten met de componenten die boven aan de lijst worden aanbevolen. Componenten die het vaakst en het laatst door u of anderen in uw organisatie worden gebruikt, worden hoger weergegeven in de lijst. |
| [!UICONTROL **Alfabetisch**] | Hiermee worden componenten alfabetisch gesorteerd. |
| [!UICONTROL **Categorisch**] | Sorteert componenten volgens componenttype (afmetingen, metrisch, segment, datumbereik). |

{style="table-layout:auto"}

## Beperkte tests voor releasefase {#release-limited-testing}

>[!AVAILABILITY]
>
>De functionaliteit die in dit artikel wordt beschreven, bevindt zich in de Beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het evaluatieproces Analytics raadpleegt u [Adobe Analytics-functiereleases](/help/release-notes/releases.md).

## Beperkte testsectie voor releasefase {#release-limited-testing-section}

>[!AVAILABILITY]
>
>De in deze sectie beschreven functionaliteit bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het evaluatieproces Analytics raadpleegt u [Adobe Analytics-functiereleases](/help/release-notes/releases.md).


## Dislaimer plug-in {#plug-in}

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van de Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met het accountteam van de Adobe van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

