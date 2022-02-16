---
title: Overzicht van het vergelijkingspaneel voor segmenten
description: Leer hoe u het vergelijkingspaneel voor segmenten gebruikt, onderdeel van de IQ voor segmenten in Analysis Workspace.
keywords: Analysis Workspace;Segment-IQ
feature: Segmentation
role: User, Admin
exl-id: 1f5df6fb-1e9f-4b8f-885c-bf9e68d88c89
source-git-commit: 1ee50c6a2231795b2ad0015a79e09b7c1c74d850
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 4%

---

# Overzicht van het vergelijkingspaneel voor segmenten

Het vergelijkingspaneel Segment maakt deel uit van [Segment-IQ](../../segment-iq.md) dat ontdekt de statistisch meest significante verschillen tussen een onbeperkt aantal segmenten. De functie doorloopt een geautomatiseerde analyse van alle dimensies en metriek waartoe u toegang hebt. Het ontdekt automatisch zeer belangrijke kenmerken van de publiekssegmenten die KPIs van uw bedrijf drijven en laat u zien hoeveel om het even welke segmenten overlappen.

Hier volgt een video over het vergelijken van segmenten:

>[!VIDEO](https://video.tv.adobe.com/v/23976/?quality=12)

## Een vergelijkingspaneel voor segmenten maken

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. Klik op het pictogram met 9 vierkantjes rechtsboven in het venster en klik vervolgens op het gekleurde Analytics-logo.
1. Klik in de bovenste navigatiebalk op Workspace.
1. Klik op de knop &#39;Create New Project&#39; (Nieuw project maken).
1. Controleer of de optie voor &#39;Leeg project&#39; is geselecteerd in het modale pop-upmenu en klik vervolgens op Create (Maken).
1. Klik op de knop Deelvensters aan de linkerkant en sleep het deelvenster Segmentvergelijking boven of onder het automatisch gemaakte deelvenster van de vrije-vormtabel.

   ![Vergelijken, deelvenster](assets/seg-compare-panel.png)

1. Selecteer segmenten die u wilt vergelijken en zet ze neer in het deelvenster.

   ![Soorten publiek vergelijken](assets/compare-audiences.png)

   Nadat u een segment naar het deelvenster hebt gesleept, wordt automatisch een [!UICONTROL 'Everyone Else'] segment dat iedereen NIET in het segment omvat u koos. Het is een vaak gebruikt segment in het vergelijkingspaneel, maar u kunt het wel verwijderen en een ander keuzesegment vergelijken.

   ![Alle anderen](assets/everyone-else.png)

1. Als u hebt bepaald welke twee segmenten moeten worden vergeleken, klikt u op [!UICONTROL Build].

   Deze actie begint een achterste proces dat statistische verschillen tussen de twee geselecteerde segmenten en alle dimensies, metriek en andere segmenten zoekt. Een voortgangsbalk boven in het deelvenster geeft de resterende tijd aan totdat elke meting en dimensie wordt geanalyseerd. De meest gebruikte metriek, de afmetingen, en de segmenten worden voorrang gegeven aan looppas eerst zodat zijn de meest relevante resultaten op een geschikte manier teruggekeerd.

## Componenten uitsluiten van vergelijking

Soms is het gewenst om bepaalde afmetingen, maateenheden of segmenten uit te sluiten van segmentvergelijkingen. U wilt bijvoorbeeld het segment &#39;Amerikaanse mobiele gebruikers&#39; vergelijken met &#39;Duitse mobiele gebruikers&#39;. Het zou niet zinvol zijn om geografische dimensies op te nemen, aangezien deze segmenten al deze verschillen inhouden.

1. Klik op [!UICONTROL 'Show Advanced Options'].
1. Sleep componenten die u wilt uitsluiten naar de [!UICONTROL Excluded Components] deelvenster.

   ![Uitgesloten onderdelen](assets/excluded-components.png)

Klikken [!UICONTROL 'Set as default'] om uw huidige componenten in alle toekomstige segmentvergelijkingen automatisch uit te sluiten. Als u uitgesloten componenten wilt uitgeven, klik een componenttype, dan klik &quot;X&quot;naast een component om het in uw analyse opnieuw op te nemen. Klik op Alles wissen om alle componenten opnieuw op te nemen in de segmentvergelijking.

![Uitgesloten afmetingen](assets/excluded-dimensions.png)

## Het bekijken van een rapport van de segmentvergelijking

Nadat Adobe de twee gewenste segmenten heeft geanalyseerd, worden de resultaten van deze analyse in verschillende visualisaties weergegeven:

![Visualisaties 1](assets/new-viz.png)

![Visualisaties 2](assets/new-viz2.png)

### Grootte en overlapping

Hiermee worden de relatieve grootten van elk geselecteerd segment en de mate waarin ze met elkaar overlappen, geïllustreerd met behulp van een vlinderdiagram. U kunt de muisaanwijzer boven het visuele gedeelte plaatsen om te zien hoeveel bezoekers zich in elke overlappende of niet-overlappende sectie bevonden. U kunt ook met de rechtermuisknop op de overlapping klikken om een gloednieuw segment te maken voor verdere analyse. Als de twee segmenten elkaar uitsluiten, wordt geen overlapping getoond tussen de twee cirkels (typisch gezien met segmenten gebruikend een klapcontainer).

![Grootte en overlapping](assets/size-overlap.png)

### Samenvattingen van de populatie

Rechts van de visualisatie Grootte en Overlap wordt het totale aantal unieke bezoekers in elk segment en de overlapping weergegeven.

![Samenvattingen van de populatie](assets/population_summaries.png)

### Metrische gegevens bovenaan

Geeft de statistisch meest significante cijfers weer tussen de twee segmenten. Elke rij in deze tabel vertegenwoordigt een differentiërende metrische waarde, gerangschikt op basis van de verschillen tussen de segmenten. Een verschilscore van 1 betekent dat deze statistisch significant is, terwijl een verschilscore van 0 betekent dat er geen statistische significantie is.

Deze visualisatie lijkt op vrije-vormtabellen in Analysis Workspace. Als u een diepgaande analyse van een bepaalde metrische waarde wilt uitvoeren, plaatst u de muisaanwijzer boven een regelitem en klikt u op &#39;Zichtbaar maken&#39;. Er wordt een nieuwe tabel gemaakt om die specifieke metrische waarde te analyseren. Als metrisch voor uw analyse irrelevant is, houd over het lijnpunt en klik &quot;X&quot;om het te verwijderen.

>[!NOTE]
>
>De metriek die aan deze lijst wordt toegevoegd nadat de segmentvergelijking is gebeëindigd ontvangen geen Score van het Verschil.

![Metrische gegevens bovenaan](assets/top-metrics.png)

### Metrisch in de tijd per segment

Rechts van de tabel Metriek bevindt zich een gekoppelde visualisatie. U kunt een lijnpunt in de lijst op de linkerzijde klikken, en deze visualisatie werkt bij om te tonen dat metrisch in tijd trended.

![Bovenste metrische regel](assets/linked-viz.png)

### Bovenste afmetingen

Toont de statistisch meest significante afmetingspunten over al uw dimensies. Elke rij toont het percentage van elk segment dat dit afmetingspunt tentoonstelt. Deze tabel kan bijvoorbeeld laten zien dat 100% van de bezoekers in &#39;Segment A&#39; het afmetingitem &#39;Browsertype: Google&quot;, terwijl slechts 19,6% van &quot;Segment B&quot; dit aspect had. Een verschilscore van 1 betekent dat deze statistisch significant is, terwijl een verschilscore van 0 betekent dat er geen statistische significantie is.

Deze visualisatie lijkt op vrije-vormtabellen in Analysis Workspace. Als u een diepgaande analyse van een specifiek dimensie-item wilt uitvoeren, plaatst u de muisaanwijzer boven een lijstitem en klikt u op &#39;Zichtbaar maken&#39;. Er wordt een nieuwe tabel gemaakt om dat specifieke dimensie-item te analyseren. Als een dimensie-item irrelevant is voor uw analyse, plaatst u de muisaanwijzer boven het lijstitem en klikt u op de X-toets om het item te verwijderen.

>[!NOTE]
>
>De punten van Dimension die aan deze lijst worden toegevoegd nadat de segmentvergelijking heeft gebeëindigd ontvangen geen Score van het Verschil.

![Bovenste afmetingen](assets/top-dimension-item1.png)

### Dimension-items per segment

Rechts van de tabel met afmetingen bevindt zich een gekoppelde staafdiagramvisualisatie. Het toont alle getoonde afmetingspunten in een staafdiagram. Als u op een regelitem in de tabel links klikt, wordt de visualisatie rechts bijgewerkt.

![Bovenste dimensiebalkdiagram](assets/top-dimension-item.png)

### Bovenste segmenten

Geeft aan welke andere segmenten (behalve de twee segmenten die ter vergelijking zijn geselecteerd) statistisch significant overlappen. Deze tabel kan bijvoorbeeld laten zien dat een derde segment, &#39;Bezoekers herhalen&#39;, sterk overlapt met &#39;Segment A&#39;, maar niet overlapt met &#39;Segment B&#39;. Een verschilscore van 1 betekent dat deze statistisch significant is, terwijl een verschilscore van 0 betekent dat er geen statistische significantie is.

Deze visualisatie lijkt op vrije-vormtabellen in Analysis Workspace. Als u een diepgaande analyse van een specifiek segment wilt uitvoeren, plaatst u de muisaanwijzer boven een lijstitem en klikt u op &#39;Zichtbaar maken&#39;. Er wordt een nieuwe tabel gemaakt om dat specifieke segment te analyseren. Als een segment irrelevant voor uw analyse is, beweegt u de muisaanwijzer over het lijstitem en klikt u op de X om het te verwijderen.

>[!NOTE]
>
>De segmenten die aan deze lijst worden toegevoegd nadat de segmentvergelijking is gebeëindigd ontvangen geen Score van het Verschil.

![Bovenste segmenten](assets/top-segments.png)

### Segmentoverlapping

Rechts van de segmenttabel bevindt zich een gekoppelde venn-schemavisualisatie. Het toont het statistisch meest significante segment dat op uw vergeleken segmenten wordt toegepast. Bijvoorbeeld &#39;Segment A&#39; + &#39;Statistisch significant segment&#39; vs. &quot;Segment B&quot; + &quot;Statistisch significant segment&quot;. Wanneer u op een segmentregelitem in de tabel links klikt, wordt het vlinderdiagram rechts bijgewerkt.

![Bovenste segmenten vgn. diagram](assets/segment-overlap.png)
