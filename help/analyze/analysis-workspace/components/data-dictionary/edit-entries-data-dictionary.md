---
description: Met het gegevenswoordenboek in Analysis Workspace kunnen gebruikers de verschillende componenten in Analysis Workspace, waaronder het beoogde gebruik, die zijn goedgekeurd, duplicaten zijn, catalogiseren en bijhouden, enzovoort.
title: Items in het gegevenswoordenboek bewerken
feature: Components
role: Admin
exl-id: 4f15cad2-596e-41c3-89aa-4456d8e94fa0
source-git-commit: 1e1f90f1ba290365b8ae9c8914e38f9c2f339b3f
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---

# Onderdeelitems bewerken in het gegevenswoordenboek

Analysebeheerders kunnen componentitems in het gegevenswoordenboek voor een bepaalde rapportsuite bewerken. Alle aangebrachte wijzigingen zijn zichtbaar voor alle gebruikers van de rapportsuite.

Een component in het gegevenswoordenboek bewerken:

1. Ga naar het Analysis Workspace-project dat de component bevat die u wilt bewerken.

1. Selecteer het **pictogram van het Woordenboek van Gegevens** in het linkerspoor van Analysis Workspace. (Alternatieve manieren om tot het Woordenboek van Gegevens toegang te hebben worden beschreven in &quot;toegang tot het Woordenboek van Gegevens&quot;in [ het Overzicht van het Woordenboek van Gegevens ](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md).)

   Het venster Gegevenswoordenboek wordt weergegeven.

   ![ Admin van het Woordenboek van Gegevens mening ](assets/data-dictionary-admin.png)

1. Controleer of de juiste rapportsuite is geselecteerd in de keuzelijst. Standaard wordt de rapportsuite weergegeven waarin u zich al bevindt.

1. (Optioneel) Typ in het zoekveld de naam van de component die u wilt bewerken.

   Het type component kan door zowel kleur als pictogram worden geïdentificeerd. **Dimensionen** ![ het pictogram van het Dimension ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg) is oranje, **Segmenten** ![ het pictogram van het Segment ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) is blauw, **waaiers van de Datum** ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) 10} het waaierpictogram van de Datum is paars, en **Metriek** ![ is het Stematische pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg) groen. ![ Het pictogram van de Adobe wijst op of een berekend metrisch malplaatje of een segmentmalplaatje, en het pictogram van de calculator ![ Calculator ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg) op berekende metrisch die door een beheerder Analytics in uw organisatie werd gecreeerd.

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

1. (Facultatief) selecteer het **pictogram van de Soort ![ de componenten van de Soort pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SortOrderDown_18_N.svg), dan om het even welke volgende filteropties om de lijst van componenten te sorteren:**

   {{components-sort-options}}

1. Selecteer in de lijst met componenten de component die u wilt bewerken.

1. Selecteer **uitgeven** pictogram ![ Woordenboek van Gegevens geeft pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) naast de componentennaam uit.

1. Bewerk de volgende informatie over de component:

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

1. Klik **sparen** pictogram ![ Woordenboek van Gegevens sparen pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SaveFloppy_18_N.svg) om uw veranderingen te bewaren.
