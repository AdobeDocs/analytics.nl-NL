---
title: Communiceren met gevolgen voor gebruikers
description: Leer effectieve manieren om het effect van een gebeurtenis in uw organisatie te communiceren.
exl-id: 9ba83f3f-2eea-44c2-80b2-a0a9111d51cf
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 1%

---

# De invloed van gebeurtenissen doorgeven aan gebruikers

Als u gegevens [door een gebeurtenis](overview.md) hebt beïnvloed, is het belangrijk om die gebeurtenis aan gebruikers in uw organisatie mee te delen.

* Ontwikkel een gemeenschappelijke ontkenning die u in mededelingen voor consistentie kunt gebruiken
* Doorlopende communicatie bieden aan gebruikers van Analytics en belangrijke belanghebbenden tijdens en na de gebeurtenis
* Plaats een kalenderherinnering voor volgende mijlpalen, zoals de volgende maand of het volgende jaar. Deze mededeling helpt gebruikers die rapporten bekijken in de toekomst herinneren aan de gevolgen in maand-over-maand of jaar-over-jaar rapporten.

In Adobe Analytics worden in de volgende secties verschillende manieren getoond waarop u kunt communiceren met gebruikers in uw organisatie. U kunt ook andere methoden buiten Adobe Analytics gebruiken, zoals e-mail, om te communiceren met gebruikers.

## Communiceren via het deelvenster of visualisatiebeschrijvingen

Als u een Werkruimteproject hebt dat onder gebruikers in uw organisatie wordt gedeeld, kunt u het effect van een gebeurtenis door paneel of visualisatiebeschrijvingen meedelen. Klik met de rechtermuisknop op een deelvenster of een visualisatiekop en selecteer **[!UICONTROL Edit description]**.

![Beschrijving van deelvenster](assets/panel_description.png)

## Communiceren via tekstvisualisatie

U kunt het effect van een gebeurtenis ook communiceren via speciale tekstvisualisaties. Zie [Tekstvisualisaties](/help/analyze/analysis-workspace/visualizations/text.md) in de gebruikershandleiding Analyseren.

![Tekstvisualisatie](assets/text_visualization.png)

## Aangepaste kalendergebeurtenissen toevoegen aan trends in Workspace

Voor elke trendvisualisatie in Workspace, kunt u in een reeks toevoegen die uw beïnvloede datumwaaier vertegenwoordigt.

1. Maak een berekende metrische waarde met het segment &#39;Betrokken dagen&#39; door [Specifieke datums in analyse uitsluiten](segments.md) te volgen.
1. Voeg de gewenste metrische waarde toe aan het berekende metrische canvas.

   ![Metrisch](assets/calcmetric_event.png)

1. Voeg een titel en een beschrijving toe om gebruikers op de hoogte te brengen van de gevolgen. U kunt deze metrische waarde desgewenst ook labelen als een kalenderannotatie.

   ![Titel en beschrijving](assets/calcmetric_title_description.png)

1. Voeg in een vrije-vormlijst de dimensie &#39;Dag&#39; toe. Voeg &#39;Bezoeken&#39; toe en de berekende maateenheid als kolommen naast elkaar.

   ![Vrije-vormentabel](assets/calcmetric_freeform.png)

1. Klik op het tandwielpictogram voor kolominstellingen voor de berekende metrische waarde en schakel **[!UICONTROL Interpret zero as no value]** in.

   ![Berekende metrische instellingen](assets/calcmetric_zero_no_value.png)

1. Voeg een lijnvisualisatie toe. Betrokken dagen worden weergegeven met een andere kleur. Gebruikers kunnen ook op het pictogram &#39;Info&#39; in de berekende maatstaf klikken voor meer informatie.

   ![Info, pictogram](assets/calcmetric_infoicon.png)

## Een agendagebeurtenis gebruiken in Rapporten en Analyses

Als u Rapporten &amp; Analytics gebruikt, kunt u [agendagebeurtenis ](/help/components/t-calendar-event.md) gebruiken om beïnvloede dagen in om het even welk trended rapport te benadrukken. Deze methode is niet van toepassing op Analysis Workspace.

1. Ga naar **[!UICONTROL Components]** > **[!UICONTROL All components]** > **[!UICONTROL Calendar events]**.
2. Voer de gewenste titel, het gewenste datumbereik en de notitietekst in.
3. Klik op **[!UICONTROL Save]**.

![Agenda, gebeurtenis](assets/exclude_calendar_event.png)
