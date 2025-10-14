---
title: Datums vergelijken die door een gebeurtenis worden beïnvloed met vorige bereiken
description: Leer meer over de impact van een gebeurtenis, zoals een implementatieprobleem of een stroomstoring, door deze te vergelijken met eerdere trends.
exl-id: 5e4ac1db-2740-4ec1-9d6a-5aa2005fadfd
feature: Curate and Share
source-git-commit: 29ab0cc535bd8f74b50428c11756bf8b446a23ab
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Datums vergelijken die door een gebeurtenis worden beïnvloed met vorige bereiken

Als u gegevens [&#x200B; hebt die door een gebeurtenis &#x200B;](overview.md) worden beïnvloed, kunt u historische tendensen bekijken om zijn effect te meten. Deze vergelijking is handig als u precies wilt weten hoeveel invloed een gebeurtenis heeft op uw gegevens. U kunt dus beslissen of u de gegevens wilt uitsluiten, een notitie wilt toevoegen aan rapporten of deze wilt negeren.

## Een datumbereik maken dat de gebeurtenis bevat

Maak een datumbereik dat de gebeurtenis omvat om te beginnen met het verkennen van de impact van die gebeurtenis.

1. Ga naar **[!UICONTROL Components]** > **[!UICONTROL Date ranges]**.
2. Klik op **[!UICONTROL Add]**.
3. Selecteer het datumbereik waarin de gebeurtenis heeft plaatsgevonden. Klik op **[!UICONTROL Save]**.

   ![&#x200B; de waaierbouwer van de Datum &#x200B;](assets/date_range_builder.png)

## Gebeurtenisdatums en vergelijkbare eerdere bereiken naast elkaar weergeven

U kunt elke metrische waarde tussen het datumbereik van de gebeurtenis en vergelijkbare datumbereiken vergelijken met behulp van een vrije-vormtabelvisualisatie.

1. Open een Workspace-project en voeg de dimensie &#39;Dag&#39; toe aan de tabel in vrije vorm. Pas het recent gemaakte datumbereik toe dat op metrische wijze is gestapeld, zoals &#39;Voorvallen&#39;.

   ![&#x200B; metrische waaier van de Datum &#x200B;](assets/date_range_metric.png)

2. Klik met de rechtermuisknop op het datumbereik en klik vervolgens op **[!UICONTROL Add time period column]** > **[!UICONTROL Custom date range to this date range]** .
   * Voor een week-over-week vergelijking, selecteer de waaier van de gebeurtenis minus 7 dagen. Zorg ervoor dat de dagen van de week tussen de gebeurtenis en dit datumbereik zijn uitgelijnd.
   * Voor een maand-over-maand vergelijking, selecteer de waaier van de gebeurtenis vorige maand. U kunt ook het bereik van de gebeurtenis min 28 dagen selecteren als u de dagen van de week wilt uitlijnen.
   * Selecteer voor een vergelijking van jaar tot jaar het bereik van de gebeurtenis vorig jaar.
3. Wanneer u het gewenste datumbereik selecteert, worden deze toegevoegd aan de vrije-vormtabel. U kunt met de rechtermuisknop klikken en zoveel datumbereiken toevoegen als u wilt vergelijken.

   ![&#x200B; Datum gerichte tendensen &#x200B;](assets/date_aligned_trends.png)

## Bereken percentageverschillen tussen de gebeurtenis en gelijkaardige vroegere waaiers

Vergelijk afmetingspunten tussen de de datumwaaier van een gebeurtenis en gelijkaardige vroegere datumwaaiers gebruikend een vrije lijstvisualisatie. Deze stappen illustreren een voorbeeld van een week-over-week dat u kunt volgen.

1. Open een project van Workspace, en voeg a **niet-tijddimensie** aan de vrije vormlijst toe. U kunt bijvoorbeeld de dimensie Mobiel apparaattype gebruiken. Pas het recent gemaakte datumbereik toe dat op metrische wijze is gestapeld, zoals &#39;Voorvallen&#39;:

   ![&#x200B; Mobiel apparatentype door beïnvloede datumwaaier &#x200B;](assets/mobile_device_type.png)

2. Klik met de rechtermuisknop op het datumbereik en klik vervolgens op **[!UICONTROL Compare time periods]** > **[!UICONTROL Custom date range to this date range]** . Selecteer het bereik van de gebeurtenis min 7 dagen. Zorg ervoor dat de dagen van de week tussen de gebeurtenis en dit datumbereik zijn uitgelijnd.

   ![&#x200B; vergelijk tijdspanne menu &#x200B;](assets/compare_time_custom.png)

3. Wijzig de naam van de resulterende metrische waarde voor Percent Change in iets specifiekers, zoals &quot;WoW Affected Range&quot;. Klik op het informatiepictogram en klik vervolgens op het bewerkingspotlood om de metrische naam te bewerken.

   ![&#x200B; Week over week &#x200B;](assets/wow_affected_range.png)

4. Herhaal stap 3 en 4 voor maand-over-maand en jaar-over-jaar vergelijkingen. U kunt deze actie uitvoeren in dezelfde tabel of in afzonderlijke tabellen.

## Vergelijkingsdatumbereiken naast elkaar analyseren als rijen

Als u de bovenstaande procentuele wijzigingen verder wilt analyseren, kunt u ze omzetten in rijen.

1. Voeg een vrije lijstvisualisatie toe en laat de lijstbouwer toe. Met deze handeling kunt u de metrische gegevens voor procentuele wijziging in de gewenste volgorde plaatsen.
2. Houd `Ctrl` (Windows) of `Cmd` (Mac) ingedrukt en sleep de 3 procent veranderingswaarden één voor één naar de rijen van de tabel.

   ![&#x200B; Bouwer van de Lijst &#x200B;](assets/table_builder.png)

3. Voeg het segment &#39;Alle bezoeken&#39; toe aan de kolom van de tabel en aan alle andere gewenste segmenten.

   ![&#x200B; de buildersegmenten van de Lijst &#x200B;](assets/table_builder_segments.png)

4. Klik op **[!UICONTROL Build]**. Vanuit de resulterende tabel kunt u de betrokken bereiken in vergelijking met de voorafgaande week, maand en jaar voor alle gewenste segmenten bekijken.

   ![&#x200B; Voltooide lijst &#x200B;](assets/table_builder_finished.png)
