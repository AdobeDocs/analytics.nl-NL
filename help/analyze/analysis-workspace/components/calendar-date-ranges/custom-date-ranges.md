---
description: Maak aangepaste datumbereiken in Analysis Workspace en sla deze op als tijdcomponenten.
keywords: Analysis Workspace
title: Aangepaste datumbereiken maken
feature: Date Ranges
role: User, Admin
exl-id: 586bb120-3f20-452c-9867-0b93d2e794bc
source-git-commit: 1281bdc569c9ebc5d8daa151b19dc21710633eab
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Aangepaste datumbereiken maken

U kunt aangepaste datumbereiken maken in Analysis Workspace en deze opslaan als tijdcomponenten.

Voor informatie over het toevoegen van bestaande datumwaaiers aan een project, zie [ Overzicht van kalender en datumwaaiers ](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md).

Een aangepast datumbereik maken:

1. Selecteer in Adobe Analytics **[!UICONTROL Components]** > **[!UICONTROL Date ranges]** .

   ![ pagina van de datumwaaier ](assets/date-ranges.png)

1. Selecteer [!UICONTROL **creeer nieuwe datumwaaier**].

1. Geef de volgende informatie op in de constructor Datumbereik:

   | Optie | Beschrijving |
   |---------|----------|
   | [!UICONTROL **Titel**] | De titel van het datumbereik zoals deze wordt weergegeven wanneer gebruikers de titel selecteren in Analysis Workspace. |
   | [!UICONTROL **Beschrijving**] | Een beschrijving voor het datumbereik. |
   | [!UICONTROL **Markeringen**] | Alle tags die u wilt toepassen op het datumbereik. |
   | [!UICONTROL **de Waaier van de Datum**] | Hiermee kunt u een aangepast datumbereik kiezen. Standaard zijn de laatste 30 dagen geselecteerd. |
   | [!UICONTROL **Vooraf ingesteld**] | Kies van een lijst van vooraf ingestelde datumwaaiers, zoals [!UICONTROL **Gisteren**], [!UICONTROL **Laatste 7 dagen**], [!UICONTROL **Laatste 30 dagen**], etc. |
   | [!UICONTROL **tijd van het Begin**] | De tijd van de dag waarop het datumbereik begint. |
   | [!UICONTROL **Eind tijd**] | De tijd van de dag waarop het datumbereik eindigt. |
   | [!UICONTROL **het rollen van het gebruik data**] | Het rollen datums staan u toe om een dynamisch rapport te produceren dat vooruit of achteruit voor een bepaalde periode kijkt die op wordt gebaseerd wanneer u het rapport in werking stelde. Bijvoorbeeld, als u op alle geplaatste Orden &quot;Vorige Maand&quot;wilt rapporteren (die op het Gemaakt gebied van de Datum wordt gebaseerd) en dat rapport in December in werking stellen, zou u orden zien die in november worden geplaatst. Als je datzelfde rapport in januari zou uitvoeren, zou je orders zien geplaatst in december.<ul><li>**[!UICONTROL Date Preview]**: geeft aan welke tijdsperiode de schuivende kalender omspant.</li><li>**[!UICONTROL Start]**: U kunt kiezen uit de huidige dag, de huidige week, de huidige maand, het huidige kwartaal en het huidige jaar.</li><li>**[!UICONTROL End]**: U kunt kiezen uit de huidige dag, de huidige week, de huidige maand, het huidige kwartaal en het huidige jaar.</li></ul><br> die door gebrek wordt geselecteerd. |

1. Selecteer [!UICONTROL **sparen**].

## Voorbeeld: datumbereik voor &quot;twee maanden geleden&quot; {#section_C4109C57CB444BB2A79CC8082BD67294}

De volgende waaier van de douanedatum toont een datumwaaier voor &quot;twee maanden geleden,&quot;met een Summiere visualisatie van de Verandering die richtingsverandering toont.

![](assets/date-range-two-months-ago.png)

Het aangepaste datumbereik wordt boven in het deelvenster met componenten van [!UICONTROL Date Range] in uw project weergegeven:

![](assets/date-range-panel-two-months-ago.png)

U kunt dit aangepaste datumbereik naar een kolom slepen naast een aangepast maandelijks roldatumbereik met de voorinstelling Laatste maand voor een vergelijking. Voeg een Summiere visualisatie van de Verandering toe en selecteer de totalen van elke kolom om richtingsverandering te tonen:

![](assets/date-range-two-months-table.png)

## Voorbeeld: een 7-daags roldatumbereik gebruiken {#section_7EF63B2E9FF54D2E9144C4F76956A8DD}

U kunt een datumbereik maken dat een 7-daags schuivend venster opgeeft dat een week geleden eindigt:

![](assets/create_date_range.png)

Gebruik *`rolling daily`* .

* De begininstellingen zijn *`current day minus 6 days`* .

* De instellingen voor Einde zijn *`current day minus 7 days`* .

Dit datumbereik kan een component zijn die u naar elke vrije-vormtabel sleept.
