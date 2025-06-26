---
description: Met het gegevenswoordenboek in Analysis Workspace kunnen gebruikers de verschillende componenten in Analysis Workspace catalogiseren en bijhouden, inclusief het beoogde gebruik, dat is goedgekeurd, duplicaten zijn enzovoort.
title: Items in het gegevenswoordenboek bewerken
feature: Components
role: Admin
exl-id: 4f15cad2-596e-41c3-89aa-4456d8e94fa0
source-git-commit: 8f7c6a0d1477b599b05aeb7b74c4ee96531d294d
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%

---

# Onderdeelitems bewerken in het gegevenswoordenboek

Analysebeheerders kunnen componentitems in het gegevenswoordenboek voor een bepaalde rapportsuite bewerken. Alle aangebrachte wijzigingen zijn zichtbaar voor alle gebruikers van de rapportsuite.

Een component in het gegevenswoordenboek bewerken:

1. Ga naar het Analysis Workspace-project dat de component bevat die u wilt bewerken.

1. Selecteer het **pictogram van het Woordenboek van Gegevens** in het linkerspoor van Analysis Workspace. (Alternatieve manieren om tot het Woordenboek van Gegevens toegang te hebben worden beschreven in [ toegang tot het Woordenboek van Gegevens ](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md#access-the-data-dictionary).)

   Het venster Gegevenswoordenboek wordt weergegeven.

   ![ Admin van het Woordenboek van Gegevens mening ](assets/data-dictionary-admin.png)

1. Controleer of de juiste rapportsuite is geselecteerd in de keuzelijst. Standaard wordt de rapportsuite weergegeven waarin u zich al bevindt.

1. (Optioneel) Typ in het zoekveld de naam van de component die u wilt bewerken.

   Het type component kan door zowel kleur als pictogram worden geïdentificeerd. **het pictogram van Afmetingen ![ Dimension ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg) is oranje,** Segmenten **![ het pictogram van het Segment ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) is blauw,** de waaiers van de Datum **](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) het de waaierpictogram van de Datum is paars, en** Metriek **![ Metrisch pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg) is groen.**![ Het pictogram van Adobe wijst op of een berekend metrisch malplaatje of een segmentmalplaatje, en het pictogram van de calculator ![ Calculator ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg) op berekende metrisch die door een beheerder van de Analyse in uw organisatie werd gecreeerd.

1. (Facultatief) selecteer het **pictogram van de Filter ![ van het Woordenboek van de Filter van de Filter ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg), dan om het even welke volgende filteropties om de lijst van componenten te filtreren:**

   | Optie | Functie |
   |---------|----------|
   | **[!UICONTROL Approved]** | Alleen componenten die zijn gemarkeerd als goedgekeurd door een beheerder. |
   | **[!UICONTROL Favorites]** | Alleen componenten in de lijst Favorieten. Voor informatie over het toevoegen van componenten aan uw lijst van favorieten, zie [ Overzicht van Componenten ](/help/analyze/analysis-workspace/components/analysis-workspace-components.md). |
   | **[!UICONTROL Dimensions]** | Alleen componenten die afmetingen hebben. (Deze optie is ook beschikbaar op het tabblad **[!UICONTROL Quick filters]** wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
   | **[!UICONTROL Metrics]** | Alleen componenten die Metrisch zijn. (Deze optie is ook beschikbaar op het tabblad **[!UICONTROL Quick filters]** wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
   | **[!UICONTROL Segments]** | Alleen componenten die Segmenten zijn. (Deze optie is ook beschikbaar op het tabblad **[!UICONTROL Quick filters]** wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
   | **[!UICONTROL Date ranges]** | Alleen componenten die Datumbereiken zijn. (Deze optie is ook beschikbaar op het tabblad **[!UICONTROL Quick filters]** wanneer u voor het eerst toegang krijgt tot het gegevenswoordenboek.) |
   | **[!UICONTROL Show all]** | Alle componenten. Deze optie is alleen beschikbaar voor beheerders. |
   | **[!UICONTROL Unapproved]** | Alleen componenten die nog niet zijn gemarkeerd als goedgekeurd door een beheerder. Als beheerder, is dit nuttig wanneer het identificeren van componenten die uw overzicht en goedkeuring vereisen. Deze optie is alleen beschikbaar voor beheerders. |
   | **[!UICONTROL Missing Description]** | Alleen componenten die nog geen beschrijving hebben in het veld Beschrijving. Deze optie is alleen beschikbaar voor beheerders. |
   | **[!UICONTROL Show duplicates]** | <p>Alleen componenten met dezelfde naam of dezelfde definitie als een andere component in de geselecteerde rapportsuite. Namen of definities moeten exact overeenkomen om als duplicaten te kunnen worden weergegeven.</p><p>Deze optie is alleen beschikbaar voor beheerders.</p><p>**NOTA:** voor definities, omvat dit componenten u evenals die creeert die door Adobe worden verstrekt. Voor namen omvat dit momenteel alleen componenten die u maakt en niet de componenten die door Adobe worden geleverd. In een toekomstige release worden dubbele namen voor door Adobe geleverde componenten weergegeven.</p> |
   | **[!UICONTROL No recent data]** | Alleen componenten die de afgelopen 90 dagen geen gegevens hebben verzameld. Deze optie is alleen beschikbaar voor beheerders. |
   | **[!UICONTROL Created by Adobe]** <!-- I don't see this option--> | Alleen componenten weergeven die door Adobe zijn gemaakt.  Bijvoorbeeld Adobe Target. Componenten die door een beheerder of een andere gebruiker in uw organisatie zijn gemaakt, worden niet weergegeven. |

   {style="table-layout:auto"}

1. (Facultatief) selecteer het **pictogram van de Soort ![ de componenten van de Soort pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SortOrderDown_18_N.svg), dan om het even welke volgende filteropties om de lijst van componenten te sorteren:**

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **geadviseerd**] | Hiermee sorteert u componenten met de componenten die boven aan de lijst worden aanbevolen. Componenten die het vaakst en het laatst door u of anderen in uw organisatie worden gebruikt, worden hoger weergegeven in de lijst. |
   | [!UICONTROL **alfabetisch**] | Hiermee worden componenten alfabetisch gesorteerd. |
   | [!UICONTROL **Categorisch**] | Sorteert componenten volgens componenttype (afmetingen, metrisch, segment, datumbereik). |

   {style="table-layout:auto"}

1. Selecteer in de lijst met componenten de component die u wilt bewerken.

1. Selecteer **uitgeven** pictogram ![ Woordenboek van Gegevens geeft pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) naast de componentennaam uit.

1. Bewerk de volgende informatie over de component:

   | Optie | Functie |
   |---------|----------|
   | **[!UICONTROL Approved]** | <p>Geeft aan dat de component is gecontroleerd en goedgekeurd door de beheerder.</p><p>Nadat een component wordt goedgekeurd, kunnen de beheerders goedkeuring verwijderen door de **Goedgekeurde** knoop te selecteren.</p> |
   | **[!UICONTROL Approval needed]** | <p>Geeft aan dat de component nog niet is gereviseerd en goedgekeurd door de beheerder.</p><p>Beheerders zien een optie voor **[!UICONTROL Approve]** . Als u deze optie selecteert, wordt de component gemarkeerd als &quot;Goedgekeurd&quot; voor gebruikers.</p> |
   | **[!UICONTROL Description]** | Beschrijft de voorgenomen functie van de component. (Deze informatie wordt toegevoegd door de beheerder van Analytics, zoals die in [ wordt beschreven voeg componentenbeschrijvingen ](/help/analyze/analysis-workspace/components/add-component-descriptions.md) toe.) |
   | **[!UICONTROL Frequently used with]** | <p>Geeft componenten weer die het meest worden gebruikt met de component die u bekijkt.</p><p>Er worden maximaal vijf componenten weergegeven voor de vijf primaire componenttypen: Metrisch, Berekend metrisch, Dimension, Segment en Datumbereik.</p><p>Deze lijst is gebaseerd op gegevens uit de afgelopen 90 dagen. Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Beheerders kunnen de componenten beheren die gebruikers in deze sectie zien door de gewenste componenten te selecteren in de vervolgkeuzelijsten **[!UICONTROL Always Include]** en **[!UICONTROL Always Exclude]** . Alvorens u de componenten beheert die de gebruikers zien, pas eerst **toe tonen alle** filter om ervoor te zorgen u om het even welke componenten ziet die niet met u worden gedeeld.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p> |
   | **[!UICONTROL Similar to]** | <p>Geeft componenten weer met vergelijkbare namen als de component die u bekijkt.</p><p>Er worden maximaal vijf componenten weergegeven voor de vijf primaire componenttypen: Metrisch, Berekend metrisch, Dimension, Segment en Datumbereik.</p><p>Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Om het even welke dubbele componenten in uw rapportreeks ook hier tonen. De beheerders van Analytics zouden alle dubbele componenten moeten identificeren en verwijderen, zoals die in [ wordt beschreven de gezondheid van het Woordenboek van Gegevens van de Monitor ](/help/analyze/analysis-workspace/components/data-dictionary/monitor-data-dictionary-health.md).</p><p>Beheerders kunnen de componenten beheren die gebruikers in deze sectie zien door de gewenste componenten te selecteren in de vervolgkeuzelijsten **[!UICONTROL Always Include]** en **[!UICONTROL Always Exclude]** . Alvorens u de componenten beheert die de gebruikers zien, pas eerst **toe tonen alle** filter om ervoor te zorgen u om het even welke componenten ziet die niet met u worden gedeeld.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p><p>**NOTA:** momenteel, **Gelijkaardig aan** sectie omvat slechts componenten u creeert en niet die verstrekt door Adobe. Door Adobe verschafte onderdelen worden in een toekomstige release toegevoegd.</p> |
   | **[!UICONTROL Tags]** | Hiermee worden alle tags weergegeven die op de component zijn toegepast. Gebruikers met beheerdersrechten kunnen tags toevoegen wanneer ze de component bewerken. |
   | **[!UICONTROL Component type]** | Hiermee wordt het type component weergegeven dat het is, ongeacht of het een Dimension, Metrisch, Segment of Datumbereik betreft. |
   | **[!UICONTROL Created by]** | Geeft de naam weer van de gebruiker die de component heeft gemaakt. |
   | **[!UICONTROL Preview]** | Toont een voorproef van hoe de component in Analysis Workspace kijkt. |
   | **[!UICONTROL Date last modified]** | Hiermee geeft u de dag weer waarop de component voor het laatst is gewijzigd. Deze sectie wordt weergegeven wanneer u Segmenten, Berekende metriek en Datumbereiken weergeeft. |

   {style="table-layout:auto"}

1. Klik **sparen** pictogram ![ Woordenboek van Gegevens sparen pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SaveFloppy_18_N.svg) om uw veranderingen te bewaren.
