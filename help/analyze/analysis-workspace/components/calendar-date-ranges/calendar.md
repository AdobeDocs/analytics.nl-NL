---
description: In de kalender kunt u datums en datumbereiken opgeven of een voorinstelling selecteren.
title: Overzicht van kalender- en datumbereiken
feature: Calendar
role: User, Admin
exl-id: fbf4bc18-65ba-4e39-96c1-4c41a8e3baa9
source-git-commit: b08200266204bc01c943194ea2b0b002c2bfa878
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 2%

---

# Overzicht van kalender- en datumbereiken

In de kalender kunt u datums en datumbereiken opgeven of een voorinstelling selecteren.

Hier volgt een video over het gebruik van datumbereiken en kalenders in Analysis Workspace:

>[!VIDEO](https://video.tv.adobe.com/v/23973/?quality=12)

De kalenderselecties zijn van toepassing op paneelniveau, maar u hebt de optie om hen op alle panelen toe te passen. Wanneer u in Workspace op een datumbereik klikt, worden de huidige kalendermaand en de vorige kalendermaand in de interface weergegeven. U kunt deze twee kalenders aanpassen door op de rechter- en linkerpijlen in elke respectievelijke bovenhoek te klikken.

![Kalender](assets/aw_calendar1.png)

Met de eerste klik op een kalender wordt een datumbereikselectie gestart. Met de tweede klik voltooit u een datumbereikselectie die wordt gemarkeerd. Als de `Shift` toets ingedrukt houdt (of met de rechtermuisknop klikt), wordt toegevoegd aan het momenteel geselecteerde bereik.

U kunt ook datums (en tijdafmetingen) naar een Workspace-project slepen. U kunt specifieke dagen, weken, maanden, jaren of een roldatum selecteren.

[Datumbereik en -kalender gebruiken in Analysis Workspace](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/using-dates-in-analysis-workspace.html) (4:07)

| Instelling | Beschrijving |
|--- |--- |
| Geselecteerde dagen | Geselecteerde dagen/weken/maanden/jaren. |
| Componenten voor datumbereik ten opzichte van de deelvensterkalender maken | Datums consistent houden op basis van het datumbereik van het deelvenster. |
| Roldatums gebruiken | Het rollen datums staan u toe om een dynamisch rapport te produceren dat vooruit of achteruit voor een bepaalde periode kijkt die op wordt gebaseerd wanneer u het rapport in werking stelde. Bijvoorbeeld, als u op alle geplaatste Orden &quot;Vorige Maand&quot;wilt rapporteren (die op het Gemaakt gebied van de Datum wordt gebaseerd) en dat rapport in December in werking stellen, zou u orden zien die in november worden geplaatst. Als je datzelfde rapport in januari zou uitvoeren, zou je orders zien geplaatst in december.<ul><li>**[!UICONTROL Date Preview]**: Geeft aan welke tijdsperiode de schuivende kalender omspant.</li><li>**[!UICONTROL Start]**: U kunt kiezen uit de huidige dag, de huidige week, de huidige maand, het huidige kwartaal en het huidige jaar.</li><li>**[!UICONTROL End]**: U kunt kiezen uit de huidige dag, de huidige week, de huidige maand, het huidige kwartaal en het huidige jaar.</li></ul>Als u een voorbeeld wilt weergeven, raadpleegt u [Aangepaste datumbereiken](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md). <br>Standaard geselecteerd. |
| Datumbereik | Hiermee kunt u een vooraf ingesteld datumbereik kiezen. De laatste 30 dagen is de standaardinstelling. **[!UICONTROL This week/month/quarter/year (excluding today)]** Hiermee kunt u kiezen uit datumbereiken zonder gegevens van vandaag over een hele dag. |
| Toepassen op alle deelvensters | Hiermee kunt u niet alleen het geselecteerde datumbereik voor het huidige deelvenster wijzigen, maar ook voor alle andere deelvensters in het project. |
| Toepassen | Hiermee past u het datumbereik alleen toe op dit deelvenster. |

## Over datumbereiken in het relatieve deelvenster {#relative-panel-dates}

Als u in Workspace werkt, kunt u de datumbereikcomponenten relatief maken ten opzichte van de deelvensterkalender, zodat de gegevens die u in de linkerrail (of binnen de componenten) bekijkt, worden gebaseerd op het datumbereik van het deelvenster. De volgende drie veelvoorkomende gebruikssituaties gelden voor relatieve deelvensterdatums: combinatiekaarten, overzicht van toetswaarden en datumbereiken van de Freeform-tabel.

Relatieve paneeldatumbereiken gebruiken

1. Selecteer **Werkruimte** tab.
1. Selecteren **Leeg project**.
1. Voeg afmetingen, metriek, en segmenten van het linkerspoor toe.
1. Klik op het veld voor het datumbereik van het deelvenster om de instelling voor het relatieve datumbereik van het deelvenster in of uit te schakelen.
1. Selecteren of deselecteren **Componenten voor datumbereik ten opzichte van de deelvensterkalender maken**.
   * Selecteer de optie om de componenten van het datumbereik te maken ten opzichte van de deelvensterkalender.
   * Als u deze optie uitschakelt, worden de datumbereiken in het deelvenster (Hoofdmetrische overzicht, Combinatieteksten of Pvullingen met paars datum) niet bijgewerkt als het datumbereik van het deelvenster wordt gewijzigd. Dit is de standaardinstelling.

   ![relatieve deelvensterdatums](assets/relative-date-snippet.png)

1. Klikken **Toepassen**.
De relatieve datums worden rechtsboven weergegeven.

   ![relatieve datums in vrije vorm ](assets/relative-date-range1.png)