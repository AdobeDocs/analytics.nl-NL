---
description: U kunt vanuit een aanraakpunt segmenten maken, segmenten als aanraakpunt toevoegen en de belangrijkste workflows in verschillende segmenten in Analysis Workspace vergelijken.
keywords: fallout en segmentatie;segmenten in falloutanalyse;vergelijk segmenten in fallout
title: Segmenten toepassen in een uitvalanalyse
feature: Visualizations
role: User, Admin
exl-id: 2177cd09-5a27-4295-8414-580cf53062cb
source-git-commit: 3bbf89cf522d9e0be62e0cabb28133bfa2b7a167
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 2%

---

# Segmenten toepassen in een uitvalanalyse

U kunt vanuit een aanraakpunt segmenten maken, segmenten als aanraakpunt toevoegen en de belangrijkste workflows in verschillende segmenten in Analysis Workspace vergelijken.

>[!IMPORTANT]
>
>De segmenten die als controlepunten in Vallout worden gebruikt moeten een container gebruiken die op een lager niveau dan de algemene context van de Vallout visualisatie is. Met een bezoeker-contextVallout, moeten de segmenten die als controlepunten worden gebruikt bezoek of op slag-gebaseerde segmenten zijn. Met een bezoek-contextVallout, moeten de segmenten die als controlepunt worden gebruikt op hit-Gebaseerde segmenten zijn. Als u een ongeldige combinatie gebruikt, is de fallout 100%. We hebben een waarschuwing toegevoegd aan de Fallout-visualisatie die wordt weergegeven wanneer u een incompatibel segment toevoegt als aanraakpunt. Bepaalde ongeldige combinaties van segmentcontainers leiden tot ongeldige evaluatieschema&#39;s, zoals:

* Een op bezoekers gebaseerd segment gebruiken als aanraakpunt binnen een bezoekerscontext-Fallout-visualisatie
* Een op bezoekers gebaseerd segment gebruiken als aanraakpunt binnen een visualisatie voor &#39;visit-context&#39;
* Het gebruiken van een op bezoek-gebaseerd segment als touchpoint binnen een bezoek-contextVallout visualisatie

## Een segment maken van een aanraakpunt {#section_915E8FBF35CD4F34828F860C1CCC2272}

1. Maak een segment van een bepaald aanraakpunt waarin u bijzonder geïnteresseerd bent en dat u op andere rapporten kunt toepassen. U doet dit door met de rechtermuisknop op het aanraakpunt te klikken en **[!UICONTROL Create segment from touchpoint]**.

   ![](assets/segment-from-touchpoint.png)

   De Bouwer van het Segment opent, vooraf bevolkt met het pre-gebouwde opeenvolgende segment dat aanraakpunt aanpast u selecteerde:

   ![](assets/segment-builder.png)

1. Geef het segment een titel en een beschrijving en sla het op.

   U kunt dit segment nu gebruiken in elk gewenst rapport.

## Een segment toevoegen als aanraakpunt {#section_17611C1A07444BE891DC21EE8FC03EFC}

Als u bijvoorbeeld wilt zien hoe uw gebruikers in de VS zich ontwikkelen en de neerslag beïnvloeden, sleept u gewoon het Amerikaanse gebruikerssegment naar de uitval:

![](assets/segment-touchpoint.png)

U kunt ook een AND-aanraakpunt maken door het Amerikaanse gebruikerssegment naar een ander controlepunt te slepen.

## Segmenten vergelijken bij uitvallen {#section_E0B761A69B1545908B52E05379277B56}

U kunt een onbeperkt aantal segmenten vergelijken in de Fallout-visualisatie. (In de onderstaande video staat dat u maximaal drie segmenten kunt vergelijken. Dit is onjuist.)

Hier volgt een video over het vergelijken van segmenten in de uitval:

>[!VIDEO](https://video.tv.adobe.com/v/24046/?quality=12)

1. Selecteer de segmenten die u wilt vergelijken in het dialoogvenster [!UICONTROL Segments] spoorstaaf links. In ons voorbeeld hebben we twee segmenten geselecteerd: US Users en Non-US Users.
1. Sleep ze naar de neerzetzone Segment bovenaan.

   ![](assets/segment-drop.png)

1. Optioneel: u kunt &quot;Alle bezoeken&quot; behouden als de standaardcontainer of deze verwijderen.

   ![](assets/seg-compare.png)

1. U kunt nu de uitval over de twee segmenten vergelijken, zoals waar één segment een andere overtreft, of andere inzichten.
