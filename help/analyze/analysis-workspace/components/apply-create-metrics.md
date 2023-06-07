---
description: Er zijn twee manieren om metriek in Analysis Workspace te gebruiken.
title: Metriek in Analysis Workspace
feature: Metrics
role: User, Admin
exl-id: 0a5dc709-c4e8-412a-a6cf-37b85d811f65
source-git-commit: c1b679dab7b66754ae4b6fd7503243f40d0f2178
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 1%

---

# Metrics

Met cijfers kunt u gegevenspunten in Analysis Workspace kwantificeren. Deze worden meestal gebruikt als kolommen in een visualisatie en zijn gekoppeld aan afmetingen.

## Soorten metingen

Adobe biedt verschillende typen maateenheden voor gebruik in Analysis Workspace:

* **Standaardwaarden**: De meeste metriek die u in projecten gebruikt zijn standaardmetriek. Voorbeelden zijn [Paginaweergaven](/help/components/metrics/page-views.md), [Ontvangsten](/help/components/metrics/revenue.md), of [Aangepaste gebeurtenissen](/help/components/metrics/custom-events.md). Zie [Overzicht van statistieken](/help/components/metrics/overview.md) in de gebruikershandleiding van Componenten voor meer informatie.

   ![Standaard metrisch](assets/standard-metric.png)

* **Berekende cijfers**: Door de gebruiker gedefinieerde meetwaarden die zijn gebaseerd op standaardmeetwaarden, statische getallen of algoritmische functies. Door de gebruiker gedefinieerde berekende meetwaarden geven een rekenprijspictogram weer in de lijst met beschikbare componenten. Zie [Overzicht van berekende statistieken](/help/components/c-calcmetrics/cm-overview.md) in de gebruikershandleiding van Componenten voor meer informatie.

   ![Berekende metrische waarde](assets/calculated-metric.png)

* **Berekende metrische sjablonen**: Adobe-bepaalde metriek die zich gelijkaardig aan berekende metriek gedragen. U kunt ze ongewijzigd gebruiken in Workspace-projecten of een kopie opslaan om de logica ervan aan te passen. De berekende metrische malplaatjes tonen een Adobe pictogram in de lijst van beschikbare componenten.

   ![Berekende metrische sjabloon](assets/calculated-metric-template.png)

## Metriek gebruiken in Analysis Workspace

Metriek kan op verschillende manieren in Analysis Workspace worden gebruikt. U kunt:

* Sleep metrisch aan een lege lijst Freeform om te zien die metrisch over de de datumperiode van het project trended.

* Sleep metrisch wanneer een afmeting aanwezig is om dat metrisch vergeleken bij elk afmetingspunt te zien.

* Sleep metrisch bovenop een bestaande metrische kopbal om het te vervangen.

* Sleep metrisch naast een kopbal om beide metriek naast elkaar te zien.

>[!VIDEO](https://video.tv.adobe.com/v/40817/?quality=12)

## Berekende standaarden

Met berekende meetwaarden kunt u gemakkelijk zien hoe de meetgegevens op elkaar betrekking hebben met behulp van eenvoudige operatoren of statistische functies. U kunt op verschillende manieren berekende metriek maken:

* Klik op het plusteken naast de koptekst Metriek onder de lijst met componenten aan de linkerkant.
* Ga naar **[!UICONTROL Components]** > **[!UICONTROL Calculated Metrics]** > **[!UICONTROL Add]**.
* Klik met de rechtermuisknop op een kolomkop > **[!UICONTROL Create metric from selection]** wanneer een of meer cellen van de kopkolom zijn geselecteerd. Deze optie leidt automatisch tot berekende metrisch voor u zonder het moeten de Berekende Metrische Bouwer van de Regel gebruiken.

[Berekende waarden: Metriek zonder implementatie](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/calculated-metrics/calculated-metrics-implementationless-metrics.html) (3:42)

## Metriek vergelijken met verschillende attributiemodellen

Als u het ene attributiemodel snel en gemakkelijk wilt vergelijken met het andere, klikt u met de rechtermuisknop op een metrische waarde en selecteert u **[!UICONTROL Compare Attribution Models]**:

![Kenmerk vergelijken](assets/compare-attribution.png)

Met deze sneltoets kunt u snel en eenvoudig een attributiemodel vergelijken met een ander attribuut zonder dat u dit model in een metrische modus hoeft te slepen en tweemaal hoeft te configureren.

## Gebruik de [!UICONTROL cumulative average] functie om metrisch vloeiend maken toe te passen

Hier volgt een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/27068/?quality=12)
