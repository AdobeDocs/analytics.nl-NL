---
description: Met het gegevenswoordenboek in Analysis Workspace kunnen gebruikers de verschillende componenten in Analysis Workspace, waaronder het beoogde gebruik, die zijn goedgekeurd, duplicaten zijn, catalogiseren en bijhouden, enzovoort.
title: Het gegevenswoordenboek weergeven
feature: Components
role: User, Admin
exl-id: 68f68ea4-f0a6-4937-bf8f-aecfa28572bb
source-git-commit: 74ef4e73b6ed1e2a4ad498e2314af704acb6d8cb
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 0%

---

# Componentinformatie weergeven in gegevenswoordenboek

In het gegevenswoordenboek kunt u informatie weergeven over een component, zoals de componentbeschrijving, vergelijkbare componenten, andere componenten waarmee een component vaak wordt gebruikt en meer.

Informatie over een component weergeven in het gegevenswoordenboek:

1. Ga naar het Analysis Workspace-project dat de component bevat die u wilt bekijken.

1. Selecteer het [!UICONTROL **pictogram van het Woordenboek van Gegevens**] in het linkerspoor van Analysis Workspace. (Alternatieve manieren om tot het Woordenboek van Gegevens toegang te hebben worden beschreven in [ toegang tot het gegevenswoordenboek ](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md#access-the-data-dictionary).)

   Het venster Gegevenswoordenboek wordt weergegeven.

   ![ gegeven-dictionary.png ](assets/data-dictionary.png)

   <!--double-check this screenshot. I mocked the admin view up a bit to get rid of the Dictionary health tab.-->

1. Controleer of de rapportsuite die de component bevat die u wilt weergeven, is geselecteerd in de vervolgkeuzelijst. Standaard wordt de rapportsuite weergegeven waarin u zich al bevindt.

1. (Optioneel) Typ in het zoekveld de naam van de component die u wilt weergeven.

   Het type component kan door zowel kleur als pictogram worden geïdentificeerd. **het pictogram van Afmetingen ![ Dimension ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg) is oranje,** Segmenten **![ het pictogram van het Segment ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) is blauw,** de waaiers van de Datum **![&#128279;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) het de waaierpictogram van de Datum is paars, en** Metriek **![ Metrisch pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg) is groen.** Het pictogram van Adobe wijst op of een berekend metrisch malplaatje of een segmentmalplaatje, en het pictogram van de calculator ![ Calculator ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg) op berekende metrisch die door een beheerder van de Analyse in uw organisatie werd gecreeerd.

1. (Facultatief) selecteer het **pictogram van de Filter ![ van het Woordenboek van de Filter van de Filter ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg), dan om het even welke volgende filteropties om de lijst van componenten te filtreren:**

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **Goedgekeurd**] | Alleen componenten tonen die zijn gemarkeerd als goedgekeurd door een beheerder. |
   | [!UICONTROL **Favorieten**] | Alleen componenten tonen die zich in de lijst Favorieten bevinden. Voor informatie over het toevoegen van componenten aan uw lijst van favorieten, zie [ Overzicht van Componenten ](/help/analyze/analysis-workspace/components/analysis-workspace-components.md). |
   | [!UICONTROL **Dimensies**] | Alleen componenten weergeven die afmetingen hebben. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) |
   | [!UICONTROL **Cijfers**] | Alleen componenten weergeven die Metrisch zijn. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) |
   | [!UICONTROL **Segmenten**] | Alleen componenten tonen die Segmenten zijn. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) |
   | [!UICONTROL **waaiers van de Datum**] | Alleen componenten tonen die Datumbereik hebben. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) |
   | [!UICONTROL **toon allen**] | Alle componenten tonen. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Niet goedgekeurd**] | Alleen componenten tonen die nog niet zijn gemarkeerd als goedgekeurd door een beheerder. Als beheerder, is dit nuttig wanneer het identificeren van componenten die uw overzicht en goedkeuring vereisen. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Ontbrekende Beschrijving**] | Alleen componenten weergeven die nog geen beschrijving hebben in het veld Beschrijving. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **toon duplicaten**] | <p>Alleen componenten weergeven die dezelfde naam of dezelfde definitie hebben als een andere component in de geselecteerde rapportsuite. Namen of definities moeten exact overeenkomen om als duplicaten te kunnen worden weergegeven.</p><p>Deze optie is alleen beschikbaar voor beheerders.</p><p>**NOTA:** voor definities, omvat dit componenten u evenals die creeert die door Adobe worden verstrekt. Voor namen omvat dit momenteel alleen componenten die u maakt en niet de componenten die door Adobe worden geleverd. In een toekomstige release worden dubbele namen voor door Adobe geleverde componenten weergegeven.</p> |
   | [!UICONTROL **Geen recente gegevens**] | Alleen componenten weergeven die de afgelopen 90 dagen geen gegevens hebben verzameld. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **die door Adobe**] wordt gecreeerd <!-- I don't see this option--> | Alleen componenten weergeven die door Adobe zijn gemaakt. Componenten die door een beheerder of een andere gebruiker in uw organisatie zijn gemaakt, worden niet weergegeven. |

   {style="table-layout:auto"}

1. (Facultatief) selecteer het **pictogram van de Soort ![ de componenten van de Soort pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SortOrderDown_18_N.svg), dan om het even welke volgende filteropties om de lijst van componenten te sorteren:**

   {{components-sort-options}}

1. Selecteer in de lijst met componenten de component die u wilt weergeven.

   De volgende informatie over de component wordt weergegeven:

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **Goedgekeurd**] | <p>Geeft aan dat de component is gecontroleerd en goedgekeurd door de beheerder.</p><p>Nadat een component wordt goedgekeurd, kunnen de beheerders goedkeuring verwijderen door de **Goedgekeurde** knoop te selecteren.</p> |
   | [!UICONTROL **nodig Goedkeuring**] | <p>Geeft aan dat de component nog niet is gereviseerd en goedgekeurd door de beheerder.</p><p>De beheerders zien een optie [!UICONTROL **goedkeuren**]. Als u deze optie selecteert, wordt de component gemarkeerd als &quot;Goedgekeurd&quot; voor gebruikers.</p> |
   | [!UICONTROL **Beschrijving**] | Beschrijft de voorgenomen functie van de component. (Deze informatie wordt toegevoegd door de beheerder van Analytics, zoals die in [ wordt beschreven voeg componentenbeschrijvingen ](/help/analyze/analysis-workspace/components/add-component-descriptions.md) toe.) |
   | [!UICONTROL **vaak gebruikt met**] | <p>Geeft componenten weer die het meest worden gebruikt met de component die u bekijkt.</p><p>Er worden maximaal vijf componenten weergegeven voor de vijf primaire componenttypen: Metrisch, Berekend metrisch, Dimension, Segment en Datumbereik.</p><p>Deze lijst is gebaseerd op gegevens uit de afgelopen 90 dagen. Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>De beheerders kunnen tot de componenten leiden die de gebruikers in deze sectie zien door de gewenste componenten in [!UICONTROL **te selecteren omvatten**] altijd en [!UICONTROL **sluit**] drop-down gebieden altijd uit. Alvorens u de componenten beheert die de gebruikers zien, pas eerst **toe tonen alle** filter om ervoor te zorgen u om het even welke componenten ziet die niet met u worden gedeeld.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p> |
   | [!UICONTROL **Gelijkaardig aan**] | <p>Geeft componenten weer met vergelijkbare namen als de component die u bekijkt.</p><p>Er worden maximaal vijf componenten weergegeven voor de vijf primaire componenttypen: Metrisch, Berekend metrisch, Dimension, Segment en Datumbereik.</p><p>Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Om het even welke dubbele componenten in uw rapportreeks ook hier tonen. De beheerders van Analytics zouden alle dubbele componenten moeten identificeren en verwijderen, zoals die in [ wordt beschreven de gezondheid van het Woordenboek van Gegevens van de Monitor ](/help/analyze/analysis-workspace/components/data-dictionary/monitor-data-dictionary-health.md).</p><p>De beheerders kunnen tot de componenten leiden die de gebruikers in deze sectie zien door de gewenste componenten in [!UICONTROL **te selecteren omvatten**] altijd en [!UICONTROL **sluit**] drop-down gebieden altijd uit. Alvorens u de componenten beheert die de gebruikers zien, pas eerst **toe tonen alle** filter om ervoor te zorgen u om het even welke componenten ziet die niet met u worden gedeeld.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p><p>**NOTA:** momenteel, **Gelijkaardig aan** sectie omvat slechts componenten u creeert en niet die verstrekt door Adobe. Door Adobe verschafte onderdelen worden in een toekomstige release toegevoegd.</p> |
   | [!UICONTROL **Markeringen**] | Hiermee worden alle tags weergegeven die op de component zijn toegepast. Gebruikers met beheerdersrechten kunnen tags toevoegen wanneer ze de component bewerken. |
   | [!UICONTROL **Type van Component**] | Hiermee wordt het type component weergegeven dat het is, ongeacht of het een Dimension, Metrisch, Segment of Datumbereik betreft. |
   | [!UICONTROL **die door**] wordt gecreeerd | Geeft de naam weer van de gebruiker die de component heeft gemaakt. |
   | [!UICONTROL **Voorproef**] | Toont een voorproef van hoe de component in Analysis Workspace kijkt. |
   | [!UICONTROL **Datum laatst gewijzigd**] | Hiermee geeft u de dag weer waarop de component voor het laatst is gewijzigd. Deze sectie wordt weergegeven wanneer u Segmenten, Berekende metriek en Datumbereiken weergeeft. |

   {style="table-layout:auto"}

1. (Optioneel) Sleep een component van het gegevenswoordenboek naar Analysis Workspace.
