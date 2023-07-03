---
title: Datums vergelijken die door een gebeurtenis worden beïnvloed met vorige bereiken
description: Leer meer over de impact van een gebeurtenis, zoals een implementatieprobleem of een stroomstoring, door deze te vergelijken met eerdere trends.
exl-id: 5e4ac1db-2740-4ec1-9d6a-5aa2005fadfd
feature: Event
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Datums vergelijken die door een gebeurtenis worden beïnvloed met vorige bereiken

Als u gegevens hebt [beïnvloed door een gebeurtenis](overview.md)Je kunt naar historische trends kijken om de impact ervan te meten. Deze vergelijking is handig als u precies wilt weten hoeveel invloed een gebeurtenis heeft op uw gegevens. U kunt dus beslissen of u de gegevens wilt uitsluiten, een notitie wilt toevoegen aan rapporten of deze wilt negeren.

## Een datumbereik maken dat de gebeurtenis bevat

Maak een datumbereik dat de gebeurtenis omvat om te beginnen met het verkennen van de impact van die gebeurtenis.

1. Ga naar **[!UICONTROL Components]** > **[!UICONTROL Date ranges]**.
2. Klik op **[!UICONTROL Add]**.
3. Selecteer het datumbereik waarin de gebeurtenis heeft plaatsgevonden. Klik op **[!UICONTROL Save]**.

   ![Bouwer van datumbereik](assets/date_range_builder.png)

## Gebeurtenisdatums en vergelijkbare eerdere bereiken naast elkaar weergeven

U kunt elke metrische waarde tussen het datumbereik van de gebeurtenis en vergelijkbare datumbereiken vergelijken met behulp van een vrije-vormtabelvisualisatie.

1. Open een project van de Werkruimte, en voeg de dimensie &quot;Dag&quot;aan de vrije vormlijst toe. Pas het recent gemaakte datumbereik toe dat op metrische wijze is gestapeld, zoals &#39;Voorvallen&#39;.

   ![Metrisch datumbereik](assets/date_range_metric.png)

2. Klik met de rechtermuisknop op het datumbereik en klik vervolgens op **[!UICONTROL Add time period column]** > **[!UICONTROL Custom date range to this date range]**.
   * Voor een week-over-week vergelijking, selecteer de waaier van de gebeurtenis minus 7 dagen. Zorg ervoor dat de dagen van de week tussen de gebeurtenis en dit datumbereik zijn uitgelijnd.
   * Voor een maand-over-maand vergelijking, selecteer de waaier van de gebeurtenis vorige maand. U kunt ook het bereik van de gebeurtenis min 28 dagen selecteren als u de dagen van de week wilt uitlijnen.
   * Selecteer voor een vergelijking van jaar tot jaar het bereik van de gebeurtenis vorig jaar.
3. Wanneer u het gewenste datumbereik selecteert, worden deze toegevoegd aan de vrije-vormtabel. U kunt met de rechtermuisknop klikken en zoveel datumbereiken toevoegen als u wilt vergelijken.

   ![Gedetailleerde trends](assets/date_aligned_trends.png)

## Bereken percentageverschillen tussen de gebeurtenis en gelijkaardige vroegere waaiers

Vergelijk afmetingspunten tussen de de datumwaaier van een gebeurtenis en gelijkaardige vroegere datumwaaiers gebruikend een vrije lijstvisualisatie. Deze stappen illustreren een voorbeeld van een week-over-week dat u kunt volgen.

1. Open een Workspace-project en voeg een **niet-tijddimensie** naar de vrije-vormtabel. U kunt bijvoorbeeld de dimensie Mobiel apparaattype gebruiken. Pas het recent gemaakte datumbereik toe dat op metrische wijze is gestapeld, zoals &#39;Voorvallen&#39;:

   ![Mobiel apparaattype met beïnvloed datumbereik](assets/mobile_device_type.png)

2. Klik met de rechtermuisknop op het datumbereik en klik vervolgens op **[!UICONTROL Compare time periods]** > **[!UICONTROL Custom date range to this date range]**. Selecteer het bereik van de gebeurtenis min 7 dagen. Zorg ervoor dat de dagen van de week tussen de gebeurtenis en dit datumbereik zijn uitgelijnd.

   ![Tijdsperiode vergelijken, menu](assets/compare_time_custom.png)

3. Wijzig de naam van de resulterende metrische waarde voor Percent Change in een specifiekere waarde, zoals &quot;WoW Affected Range&quot;. Klik op het informatiepictogram en klik vervolgens op het bewerkingspotlood om de metrische naam te bewerken.

   ![Week gedurende week](assets/wow_affected_range.png)

4. Herhaal stap 3 en 4 voor maand-over-maand en jaar-over-jaar vergelijkingen. U kunt deze actie uitvoeren in dezelfde tabel of in afzonderlijke tabellen.

## Vergelijkingsdatumbereiken naast elkaar analyseren als rijen

Als u de bovenstaande procentuele wijzigingen verder wilt analyseren, kunt u ze omzetten in rijen.

1. Voeg een vrije lijstvisualisatie toe en laat de lijstbouwer toe. Met deze handeling kunt u de metrische gegevens voor procentuele wijziging in de gewenste volgorde plaatsen.
2. Statisch `Ctrl` (Windows) of `Cmd` (Mac) en sleep de 3 procent veranderingsmetriek in de rijen van de lijst, één voor één.

   ![Tabelbuilder](assets/table_builder.png)

3. Voeg het segment &quot;Alle bezoeken&quot;aan de kolom van de lijst, en om het even welke andere gewenste segmenten toe.

   ![Tabelbuildsegmenten](assets/table_builder_segments.png)

4. Klik op **[!UICONTROL Build]**. Vanuit de resulterende tabel kunt u de betrokken bereiken in vergelijking met de voorafgaande week, maand en jaar voor alle gewenste segmenten bekijken.

   ![Voltooide tabel](assets/table_builder_finished.png)
