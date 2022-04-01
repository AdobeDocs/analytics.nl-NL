---
title: Specifieke datums in de analyse uitsluiten
description: Tips voor het uitsluiten van datums of datumbereiken als u deze niet wilt opnemen in rapporten.
exl-id: 744666c0-17f3-443b-9760-9c8568bec600
source-git-commit: 84f00a330334d6f4272f35140da0fecbf43622c9
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 2%

---

# Specifieke datums in de analyse uitsluiten

Als u gegevens hebt [beïnvloed door een gebeurtenis](overview.md), kunt u een segment gebruiken om het even welke datumwaaiers uit te sluiten die u niet in uw rapporten wilt omvatten. Door datums met invloed op gebeurtenissen te segmenteren, kan uw organisatie er beter van worden weerhouden beslissingen te nemen over onvolledige gegevens.

## Betrokken dagen isoleren

Maak een segment dat de betrokken dag of het betrokken datumbereik isoleert. Dit segment is handig als u zich alleen wilt richten op de probleemdagen om meer informatie over de impact ervan te zien.

1. Open de segmentbuilder door naar **[!UICONTROL Components]** > **[!UICONTROL Segments]** en klik vervolgens op **[!UICONTROL Add]**.
2. Sleep de dimensie &#39;Dag&#39; naar het definitiekanvas en stel deze in op de dag die u wilt isoleren.
3. Herhaal bovenstaande stap voor elke dag die u in uw rapport wilt isoleren.

![Betrokken segment dagen](assets/affected_days.jpg)

>[!TIP]
>
>Als u de instructie OR wilt wijzigen in een instructie AND, klikt u op de pijl omlaag naast OR en selecteert u AND.

Adobe raadt u aan om de dimensie van de oranje dimensie te gebruiken in plaats van de component van het paarse datumbereik. Als u componenten van het paarse datumbereik gebruikt, overschrijven deze het kalenderbereik van het project:

![Segmenttype uitsluiten](assets/exclude_segment_day_type.jpg)

## Betrokken dagen uitsluiten

Maak een segment dat de betrokken dag of het betrokken datumbereik uitsluit. Dit segment is handig als u de dagen wilt uitsluiten waarop problemen zijn opgetreden om het effect op de algehele rapportage te minimaliseren.

1. Open de segmentbuilder door naar **[!UICONTROL Components]** > **[!UICONTROL Segments]** en klik vervolgens op **[!UICONTROL Add]**.
2. Klik in de rechterbovenhoek van het canvas voor segmentdefinitie op **[!UICONTROL Options]** > **[!UICONTROL Exclude]**.
3. Sleep de dimensie &#39;Dag&#39; naar het definitiekanvas en stel deze in op de dag die u wilt verwijderen.
4. Herhaal bovenstaande stap voor elke dag die u in uw rapport wilt verwijderen.

![Betrokken dagen uitsluiten](assets/exclude_affected_days.jpg)

## Deze segmenten gebruiken in rapporten

Zodra u hebt gemaakt exclusief segment, kunt u het precies gebruiken aangezien u andere segmenten zou gebruiken.

### Vergelijk segmenten in een trended rapport

U kunt het segment &#39;Betrokken dagen&#39; en het segment &#39;Betrokken dagen uitsluiten&#39; in een rapport toepassen om ze naast elkaar te vergelijken. Sleep beide segmenten boven of onder een metrische waarde om ze te vergelijken:

![Beide segmenten](assets/affected_and_exclude.png)

Als u geen nullen in uw lijst of visualisaties (veroorzakend dips) wilt tonen, laat toe **[!UICONTROL Interpret zero as no value]** onder kolominstellingen.

![Voorvertoning nul](assets/interpret_zero.png)

Als u geen nullen in uw lijst of visualisaties (veroorzakend dips) wilt tonen, laat toe **[!UICONTROL Interpret zero as no value]** onder kolominstellingen.

![Voorvertoning nul](assets/interpret_zero.png)

### Pas het uitsluitingssegment op een project toe

U kunt het segment &#39;Betrokken dagen uitsluiten&#39; toepassen op een Workspace-project. Sleep het uitsluitingssegment naar de sectie Workspace canvas met het label *Een segment hier neerzetten*.

>[!TIP]
>
>Neem een notitie over uitgesloten gegevens op in de beschrijving van het deelvenster om gebruikers te helpen het rapport weer te geven. Klik met de rechtermuisknop op de titel van een deelvenster en klik vervolgens op **[!UICONTROL Edit description]**.

![Segment dat is toegepast op een deelvenster](assets/exclude_segment_panel.jpg)

### Gebruik het sluit segment in een virtuele rapportreeks uit

U kunt het segment in een [Virtuele rapportsuite](/help/components/vrs/vrs-about.md) om de gegevens gemakkelijker uit te sluiten. Deze optie is ideaal in zoverre dat u niet moet herinneren om het segment voor elk rapport toe te passen dat de beïnvloede datumwaaier omvat. Als u reeds virtuele rapportreeksen als uw primaire bron van gegevens gebruikt, kunt u het segment aan bestaande VRS toevoegen.

1. Ga naar **[!UICONTROL Components]** > **[!UICONTROL Virtual report suites]**.
2. Klik op **[!UICONTROL Add]**.
3. Voer de gewenste naam en beschrijving in voor de virtuele rapportsuite.
4. Sleep het uitsluitingssegment naar het gebied met het label **[!UICONTROL Add segment]**.
5. Klikken **[!UICONTROL Continue]** in de rechterbovenhoek klikt u op **[!UICONTROL Save]**.

![Segment toegepast op VRS](assets/exclude_segment_vrs.png)
