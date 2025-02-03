---
description: In de kalender kunt u datums en datumbereiken opgeven of een voorinstelling selecteren.
title: Overzicht van kalender- en datumbereiken
feature: Calendar
role: User, Admin
exl-id: fbf4bc18-65ba-4e39-96c1-4c41a8e3baa9
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Overzicht van kalender- en datumbereiken {#date-range}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_dateranges_endtime"
>title="Eindtijd"
>abstract="Eindtijden omvatten altijd 59 seconden."

<!-- markdownlint-enable MD034 -->


In de kalender kunt u datums en datumbereiken opgeven of een voorinstelling selecteren.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Overzicht van kalender en datumwaaiers ](https://video.tv.adobe.com/v/23973?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


De kalenderselecties zijn van toepassing op paneelniveau, maar u hebt de optie om hen op alle panelen toe te passen. Wanneer u in Workspace op een datumbereik klikt, worden de huidige kalendermaand en de vorige kalendermaand in de interface weergegeven. U kunt deze twee kalenders aanpassen door op de rechter- en linkerpijlen in elke respectievelijke bovenhoek te klikken.

![ Kalender ](assets/aw_calendar2.png){width="60%"}

## Datumbereiken selecteren en toepassen {#select-apply}

Met de eerste klik op een kalender wordt een datumbereikselectie gestart. Met de tweede klik voltooit u een datumbereikselectie die wordt gemarkeerd. Als u de toets `Shift` ingedrukt houdt (of met de rechtermuisknop klikt), wordt deze toegevoegd aan het momenteel geselecteerde bereik.

U kunt ook datums (en tijdafmetingen) naar een Workspace-project slepen. U kunt specifieke dagen, weken, maanden, jaren of een roldatum selecteren.

[ Gebruikend de Waaier en Kalender van de Datum in Analysis Workspace ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/using-dates-in-analysis-workspace.html) (4:07)

| Instelling | Beschrijving |
|--- |--- |
| Geselecteerde dagen | Geselecteerde dagen/weken/maanden/jaren. |
| Componenten voor datumbereik ten opzichte van de deelvensterkalender maken | Als deze optie is uitgeschakeld, overschrijven alle componenten van het datumbereik die worden gebruikt in een tabel, visualisatie of neerzetzone van het deelvenster de deelvensterkalender. <p>Als deze optie is ingeschakeld, hebben componenten van het datumbereik die worden gebruikt in een tabel, visualisatie of neerzetzone van het deelvenster betrekking op het datumbereik van het deelvenster. Bijvoorbeeld, als de waaier van de paneeldatum aan 1 November door 30 wordt geplaatst, en een component van de de datumwaaier van de Laatste Week wordt gebruikt in een vrije vormlijst, verwijst de informatie in de vrije vormlijst naar de laatste week in Oktober. |
| Roldatums gebruiken | Het rollen datums staan u toe om een dynamisch rapport te produceren dat vooruit of achteruit voor een bepaalde periode kijkt die op wordt gebaseerd wanneer u het rapport in werking stelde. Bijvoorbeeld, als u op alle geplaatste Orden &quot;Vorige Maand&quot;wilt rapporteren (die op het Gemaakt gebied van de Datum wordt gebaseerd) en dat rapport in December in werking stellen, zou u orden zien die in november worden geplaatst. Als je datzelfde rapport in januari zou uitvoeren, zou je orders zien geplaatst in december.<ul><li>**[!UICONTROL Date Preview]**: geeft aan welke tijdsperiode de schuivende kalender omspant.</li><li>**[!UICONTROL Start]**: U kunt kiezen uit de huidige dag, de huidige week, de huidige maand, het huidige kwartaal en het huidige jaar.</li><li>**[!UICONTROL End]**: U kunt kiezen uit de huidige dag, de huidige week, de huidige maand, het huidige kwartaal en het huidige jaar.</li></ul>Om een voorbeeld te bekijken, zie [ de datumwaaiers van de Douane ](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md). <br> die door gebrek wordt geselecteerd. |
| Datumbereik | Hiermee kunt u een vooraf ingesteld datumbereik kiezen. De laatste 30 dagen is de standaardinstelling. In **[!UICONTROL This week/month/quarter/year (excluding today)]** kunt u kiezen uit datumbereiken zonder gegevens van vandaag over een hele dag. |
| Toepassen op alle deelvensters | Hiermee kunt u niet alleen het geselecteerde datumbereik voor het huidige deelvenster wijzigen, maar ook voor alle andere deelvensters in het project. |
| Toepassen | Hiermee past u het datumbereik alleen toe op dit deelvenster. |

## Over datumbereiken in het relatieve deelvenster {#relative-panel-dates}

Als u in Workspace werkt, kunt u de datumbereikcomponenten relatief maken ten opzichte van de deelvensterkalender.
Drie veelvoorkomende gebruiksgevallen waarbij relatieve deelvensterdatums van kracht worden, zijn Combo-diagrammen, Overzicht van belangrijkste metriek en Datumbereiken van de Freeform-tabel.

Relatieve paneeldatumbereiken gebruiken

1. Selecteer het **Workspace** lusje.
1. Selecteer **Leeg project**.
1. Voeg afmetingen, metriek, en segmenten van het linkerspoor toe.
1. Klik op het veld voor het datumbereik van het deelvenster om de instelling voor het relatieve datumbereik van het deelvenster in of uit te schakelen.
1. Selecteer **maken de componenten van de datumwaaier met betrekking tot paneelkalender**.
   * Selecteer de optie om de componenten van het datumbereik te maken ten opzichte van de deelvensterkalender.
Als u relatieve datums selecteert, worden de roldatums gebaseerd op de begindatum van de deelvensterkalender en niet op de datum van vandaag.
   * Als deze optie niet wordt geselecteerd, dan zal het rollen van data op de datum van vandaag gebaseerd zijn.

   ![ relatieve deelvensterdata ](assets/relative-date-selected.png){width="60%"}

1. Klik **toepassen**.
De relatieve datums worden rechtsboven weergegeven.

   ![ relatieve datums in vrije vorm ](assets/relative-date-range1.png)

## Richtlijnen voor datumbereiken in het relatieve deelvenster {#guidelines}

Houd rekening met de volgende richtlijnen wanneer u relatieve datumbereiken in het deelvenster gebruikt.

### Formulieren en relatieve datumbereiken {#formula-relative-dates}

Als u relatieve datums hebt geselecteerd, wordt voor alle datumformules de begindatum van het deelvenster gebruikt als beginpunt.

### Aangepaste kalenders en relatieve datumbereiken {#custom-calendar-formulas}

Wanneer u een aangepaste weekkalender gebruikt en u maanden of jaren toevoegt, berekent de formule de verschuiving van de dag in de opgegeven periode. De werkelijke datum kan verschillen vanwege de verschuiving. De formule kiest de dag die op de zelfde plaats in de douanekalender aankomt. Bijvoorbeeld de derde vrijdag van de derde week in een aangepaste kalender.

### Informatie over segmenten die roldatums en relatieve paneeldatumbereiken gebruiken {#segments-relative-dates}

Als u een segment bouwt of een segment met een het rollen datum, bijvoorbeeld, de Laatste 7 Dagen of Laatste 2 Weken gebruikt, en u op de segmentvoorproef klikt, zal het de het rollen datum van *vandaag* in plaats van de datum van het paneelbegin beginnen. Dientengevolge zal de voorproef voor het segment niet aanpassen wanneer u werkelijk het segment in de lijst gebruikt. De voorvertoning wordt beïnvloed, niet het segment zelf.

## Richtlijnen voor datumbereiken en voorvertoningen in het deelvenster {#guidelines-panel-dates}

* Vanaf de release van februari worden voorvertoningen van componenten en gegevens gebaseerd op het datumbereik van het deelvenster en niet op de laatste 90 dagen.
* Alle componenten die in de linkerspoorstaaf worden vermeld zullen beschikbaar zijn gebaseerd op de waaier van de paneeldatum.
* Alle datumvoorvertoningen in het segment en de berekende metrische builders worden gebaseerd op het bereik van de deelvensterdatum (tenzij ze worden benaderd door de componentmanagers, die geen bijbehorend deelvenster hebben, zijn ze nog steeds gebaseerd op de laatste 90 dagen).
* In alle voorvertoningen van gegevens worden gegevens of componenten weergegeven op basis van het datumbereik van het deelvenster.