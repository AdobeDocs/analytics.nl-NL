---
title: Specifieke data in de analyse uitsluiten
description: Tips voor het uitsluiten van datums of datumbereiken als u deze niet wilt opnemen in rapporten.
exl-id: 744666c0-17f3-443b-9760-9c8568bec600
feature: Curate and Share, Segmentation
source-git-commit: 29ab0cc535bd8f74b50428c11756bf8b446a23ab
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 0%

---

# Specifieke data in de analyse uitsluiten

Als u gegevens [&#x200B; hebt die door een gebeurtenis &#x200B;](overview.md) worden beïnvloed, kunt u een segment gebruiken om het even welke datumwaaiers uit te sluiten die u niet in uw rapporten wilt omvatten. Door datums met invloed op gebeurtenissen te segmenteren, kan uw organisatie er beter van worden weerhouden beslissingen te nemen over onvolledige gegevens.

## Betrokken dagen isoleren {#isolate}

Maak een segment dat de betrokken dag of het betrokken datumbereik isoleert. Dit segment is handig als u zich alleen wilt richten op de probleemdagen om meer informatie over de impact ervan te zien.

1. Open de segmentbuilder door naar **[!UICONTROL Components]** > **[!UICONTROL Segments]** te gaan en vervolgens op **[!UICONTROL Add]** te klikken.
2. Sleep de dimensie &#39;Dag&#39; naar het definitiekanvas en stel deze in op de dag die u wilt isoleren.
3. Herhaal bovenstaande stap voor elke dag die u in uw rapport wilt isoleren.

![&#x200B; Betrokken dagensegment &#x200B;](assets/affected_days.jpg)

>[!TIP]
>
>Als u de instructie OR wilt wijzigen in een instructie AND, klikt u op de pijl omlaag naast OR en selecteert u AND.

Adobe raadt aan om de dimensie van de oranje dimensie te gebruiken, en niet de paarse datumbereikcomponenten. Als u componenten van het paarse datumbereik gebruikt, overschrijven deze het kalenderbereik van het project:

![&#x200B; sluit segment dagtype &#x200B;](assets/exclude_segment_day_type.jpg) uit

## Betrokken dagen uitsluiten {#exclude}

Maak een segment dat de betrokken dag of het betrokken datumbereik uitsluit. Dit segment is handig als u de dagen wilt uitsluiten waarop problemen zijn opgetreden om het effect op de algehele rapportage te minimaliseren.

1. Open de segmentbuilder door naar **[!UICONTROL Components]** > **[!UICONTROL Segments]** te gaan en vervolgens op **[!UICONTROL Add]** te klikken.
2. Klik in de rechterbovenhoek van het canvas voor segmentdefinitie op **[!UICONTROL Options]** > **[!UICONTROL Exclude]** .
3. Sleep de dimensie &#39;Dag&#39; naar het definitiekanvas en stel deze in op de dag die u wilt verwijderen.
4. Herhaal bovenstaande stap voor elke dag die u in uw rapport wilt verwijderen.

![&#x200B; sluit beïnvloede dagen &#x200B;](assets/exclude_affected_days.jpg) uit

## Deze segmenten gebruiken in rapporten

Zodra u hebt gemaakt exclusief segment, kunt u het precies gebruiken aangezien u andere segmenten zou gebruiken.

### Vergelijk segmenten in een trended rapport {#compare}

U kunt het segment &#39;Betrokken dagen&#39; en het segment &#39;Betrokken dagen uitsluiten&#39; in een rapport toepassen om ze naast elkaar te vergelijken. Sleep beide segmenten boven of onder een metrische waarde om ze te vergelijken:

![&#x200B; Beide segmenten &#x200B;](assets/affected_and_exclude.png)

Als u geen nullen in uw tabel of visualisaties wilt weergeven (dips veroorzaken), schakelt u **[!UICONTROL Interpret zero as no value]** in onder kolominstellingen.

![&#x200B; interpreteer nul &#x200B;](assets/interpret_zero.png)

Als u geen nullen in uw tabel of visualisaties wilt weergeven (dips veroorzaken), schakelt u **[!UICONTROL Interpret zero as no value]** in onder kolominstellingen.

![&#x200B; interpreteer nul &#x200B;](assets/interpret_zero.png)

### Pas het uitsluitingssegment op een project toe {#apply}

U kunt het segment &#39;Betrokken dagen uitsluiten&#39; toepassen op een Workspace-project. Sleep exclusief segment aan de het canvassectie geëtiketteerde van Workspace *Daling hier een segment*.

>[!TIP]
>
>Neem een notitie over uitgesloten gegevens op in de beschrijving van het deelvenster om gebruikers te helpen het rapport weer te geven. Klik met de rechtermuisknop op de titel van een deelvenster en klik vervolgens op **[!UICONTROL Edit description]** .

![&#x200B; Segment dat op een paneel &#x200B;](assets/exclude_segment_panel.jpg) wordt toegepast

### Gebruik het sluit segment in een virtuele rapportreeks uit {#use-vrs}

U kunt het segment in a [&#x200B; virtuele rapportreeks &#x200B;](/help/components/vrs/vrs-about.md) gebruiken om de gegevens geschikter uit te sluiten. Deze optie is ideaal in zoverre dat u niet moet herinneren om het segment voor elk rapport toe te passen dat de beïnvloede datumwaaier omvat. Als u reeds virtuele rapportreeksen als uw primaire bron van gegevens gebruikt, kunt u het segment aan een bestaande Virtuele rapportreeksen toevoegen.

1. Ga naar **[!UICONTROL Components]** > **[!UICONTROL Virtual report suites]**.
2. Klik op **[!UICONTROL Add]**.
3. Voer de gewenste naam en beschrijving in voor de virtuele rapportsuite.
4. Sleep het uitsluitingssegment naar het gebied met het label **[!UICONTROL Add segment]** .
5. Klik op **[!UICONTROL Continue]** in de rechterbovenhoek en klik vervolgens op **[!UICONTROL Save]** .

![&#x200B; Segment dat op Virtuele rapportreeks &#x200B;](assets/exclude_segment_vrs.png) wordt toegepast
