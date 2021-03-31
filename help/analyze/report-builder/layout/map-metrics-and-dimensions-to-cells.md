---
description: Voordat u items aan het werkblad toewijst, moet u controleren of het werkblad niet is beveiligd. Als het beveiligingsschema voor uw werkblad gebruikersacties verhindert, kunt u geen cellen selecteren in het werkblad. Verwijder eerst de beveiliging van het vel en voeg vervolgens celtoewijzingen toe.
title: Cijfers en dimensies toewijzen aan cellen
uuid: 50893e1c-5f2c-4558-8001-41e70d74d6e7
feature: Report Builder
role: Bedrijfs Praktijk, Beheerder
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 2%

---


# Cijfers en dimensies toewijzen aan cellen

Voordat u items aan het werkblad toewijst, moet u controleren of het werkblad niet is beveiligd. Als het beveiligingsschema voor uw werkblad gebruikersacties verhindert, kunt u geen cellen selecteren in het werkblad. Verwijder eerst de beveiliging van het vel en voeg vervolgens celtoewijzingen toe.

Het aantal gebieden en cellen dat moet worden toegewezen, is afhankelijk van de geselecteerde metrische waarde, de korreligheid, het datumbereik en de filters die u hebt ingesteld. Als u bijvoorbeeld [!UICONTROL Site Metric] > [!UICONTROL Traffic Report] selecteert, [!UICONTROL Week] granulariteit instelt en datumbereik instelt voor [!UICONTROL Last 2 Weeks], wordt u gevraagd drie cellen toe te wijzen (wanneer u [!UICONTROL Custom Layout] gebruikt) op [!UICONTROL Request Wizard: Step 2]. Het verzoek haalt gegevens voor week één en gegevens voor week twee terug, waar elk gegevenspunt waarde = de waarde van een paginamening. De derde cel fungeert als rijkop, die u kunt configureren met [!UICONTROL Format Options].

Als u per ongeluk incompatibele locaties op het spreadsheet toewijst, geeft de rapportbuilder een fout uit.

De volgende secties bevatten meer informatie:

* [Een bereik met cellen selecteren](/help/analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_1E37FB46DA194FB7A1050B8833A48AC6)
* [Technieken voor het selecteren van cellen](/help/analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_760421C3D7F84D67A639174710C93B22)
* [Problemen bij toewijzing](/help/analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_CC1BCF841291447EB3A994EB08F3A099)

## Een bereik met cellen selecteren {#section_1E37FB46DA194FB7A1050B8833A48AC6}

Op [!UICONTROL Request Wizard: Step 2], wanneer u [!UICONTROL Custom Layout] voor een trended verzoek toelaat, kunt u het verzoek aan een waaier van cellen in kaart brengen.

Klik **[!UICONTROL Range Selector]** ![select_cell_icon.png](assets/select_cell_icon.png)

naast het item dat u wilt toewijzen.

* **Alle cellen in Bereik:** Vereist u om een groep cellen voor een  [!UICONTROL Custom Layout] stijlverzoek te selecteren.
* **Eerste cel van bereik:** hiermee selecteert u de cel linksboven van het bereik en geeft u de  [!UICONTROL Range] richting weer om de horizontale of verticale richting van de invoer- en uitvoercellen (kolom of rij) op te geven. Gebruik deze optie als de rapportbouwer cellen voor u selecteert.
* **Afdrukstand bereik:** Hiermee kunt u de celbereiken oriënteren als kolommen of rijen.
* **Selecteer Hoekcellocatie van bereik:** geeft de celreferenties weer.

## Technieken voor het selecteren van cellen {#section_760421C3D7F84D67A639174710C93B22}

U selecteert de gegevens door op het **[!UICONTROL Range Selection]**-pictogram ![select_cell_icon.png](assets/select_cell_icon.png) te klikken

en klik en sleep de muis over het gewenste bereik cellen in het werkblad. Een doorlopende selectie wordt omgeven door een zwarte rand.

![](assets/twenty_cells.gif)

De afzonderlijke geselecteerde rijen hebben een dunne witte rand rond elke rij.

![](assets/twoXten_cells_highlighted.gif)

Als u afzonderlijke rijen in één aanvraag wilt toewijzen, gebruikt u de [!UICONTROL Control]-toets, klikt u en sleept u de cursor over de gewenste cellen. U zou dit doen als uw verzoek vier gebieden met tien cellen elk, eerder dan één ononderbroken gebied met 40 cellen samen roept.

![](assets/map4.png)

Nadat u cellen hebt geselecteerd, klikt u nogmaals op **[!UICONTROL Range Selector]** op het [!UICONTROL Range Selection]-formulier om terug te keren naar [!UICONTROL Request Wizard: Step 2].

## Problemen bij toewijzing {#section_CC1BCF841291447EB3A994EB08F3A099}

Als u per ongeluk toewijst aan een cel die al een actieve toewijzing heeft, zult u merken dat er geen celverwijzing in het tekstvak naast het pictogram van de bereikkiezer verschijnt. Wanneer u [!UICONTROL OK] klikt, toont de rapportbouwer de fout, &quot;de geselecteerde waaier snijdt de waaier van een ander verzoek over. Wijzig de selectie.&quot;

* Als u de cel nog steeds moet gebruiken, klikt u met de rechtermuisknop op de gewenste cel of cellen en selecteert u **[!UICONTROL Delete Request]**.

Als u dit bericht wilt vermijden, kunt u op twee manieren te werk gaan:

* Plan het formaat van het rapport door het formatteren aan de cellen toe te voegen die verzoeken en afbeeldingen hebben
* Testen op delen van het werkblad die toewijzingen bevatten

Als u gebieden met ingesloten aanvragen wilt testen, kunt u:

* Start [!UICONTROL Request Manager] en klik op afzonderlijke verzoeken in de tabel. Wanneer u op het verzoek klikt, worden de cellen in het werkblad gemarkeerd waar het verzoek is toegewezen.
* Selecteer cellen in het spreadsheet u voor een nieuwe afbeelding van plan bent te gebruiken en klik [!UICONTROL From Sheet]. Met [!UICONTROL Request Manager] selecteert u het verzoek in de lijst met een uitvoeritem dat de geselecteerde cel doorsnijdt. Als er geen aanvraag is geselecteerd, is de cel beschikbaar.
* Selecteer cellen in het werkblad, klik met de rechtermuisknop in het contextmenu en controleer of [!UICONTROL Edit Request] beschikbaar is. Als dit het geval is, is er een verzoek verbonden aan deze cellen.
