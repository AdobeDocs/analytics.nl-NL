---
description: Leer meer over de Activity Map-extensie en hoe u door de interface ervan kunt navigeren.
title: Activity Map-extensie-interface
uuid: f6734b60-0b77-4f50-a45a-6a6936d1524e
feature: Activity Map
role: User, Admin
exl-id: 461abda1-3238-4a32-b9d3-5a57b00cf0d3
source-git-commit: c45e52d38f8ade19c09fa0d4d7955c3208cbe5aa
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# Activity Map-extensie-interface

Met de extensie Activity Map kunt u klikgegevens op uw website weergeven. U kunt de extensie downloaden door naar de volgende pagina te gaan, die een koppeling naar de webwinkel bevat:

**[!UICONTROL Tools]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Download Activity Map]**

Nadat de interface is geïnstalleerd en ingeschakeld, bestaat deze uit verschillende onderdelen:

* Een bovenste deelvenster waarmee u de extensie en rapporten kunt configureren
* Een overlay waarin de populairste koppelingen worden weergegeven
* Een onderste deelvenster met meetgegevens voor de populairste koppelingen

## Deelvenster Boven

Het bovenste deelvenster bevat de basisbesturingselementen voor de Activity Map-overlay.

![ Bedekking ](../assets/overlay.png)

De toepassing heeft de volgende instellingen:

* **Standaard/Levende mening**: Knevels tussen standaardmening en levende mening.
   * Standaardweergave: geeft de overlay weer op basis van historische gegevens.
   * Live weergave: geeft de overlay weer op basis van live-gegevens. De datumkiezer verandert in een vervolgkeuzemenu waarin u de granulariteit van live gegevens kunt wijzigen.
* **Metrische selecteur**: Staat u toe om metrisch te veranderen dat de bekleding rapporteert. Alleen [!UICONTROL Link Clicks] zijn beschikbaar als Live View is geselecteerd.
* **de selecteur van het Segment**: Staat u toe om a [ segment ](/help/components/segmentation/seg-overview.md) te selecteren, die een ondergroep van gegevens bekijken binnen uw bekleding. Segmenten zijn niet beschikbaar in Live View.
* **visualisatietype van de Bedekking**: Staat u toe om te veranderen hoe de bedekking het rangschikken van verbindingen visualiseert.
   * **[!UICONTROL Bubble]**: Bovenste koppelingen ontvangen een groene bel die de numerieke positie van de hyperlink tijdens de rapportageperiode weergeeft. U kunt de bel kleur in [ Montages ](settings.md) veranderen.
   * **[!UICONTROL Gradient]**: Bovenste koppelingen worden gearceerd weergegeven in transparant rood. De populairste koppelingen zijn de donkerste rode. U kunt de gradiëntkleur in [ Montages ](settings.md) veranderen.
   * **[!UICONTROL Off]**: koppelingsoverlays uitschakelen.
* **de selecteur van de Datum**: Staat u toe om de rapporteringsperiode te veranderen.

De koptekst van dit deelvenster bevat de volgende instellingen:

* **uitvouwen/doen ineenstorten hoogste paneel**: Knevels het hoogste paneel om montages horizontaal of verticaal (dubbel pijlpictogram) te tonen.
* **[!UICONTROL Toggle page details]**: het onderste deelvenster (oogpictogram) weergeven of verbergen.
* **[!UICONTROL Show settings]**: opent een menu voor instellingen die u kunt wijzigen (tandwielpictogram):
   * **[!UICONTROL Settings]**: Opent de 1} Montages van de uitbreiding [.](settings.md)
   * **[!UICONTROL Help]**: opent de documentatie naar Experience League (deze pagina).
   * **[!UICONTROL Adobe community]**: Opent de [ gemeenschap van Experience League ](https://experienceleaguecommunities.adobe.com/).
   * **[!UICONTROL About]**: geeft de extensieversie weer.
   * **[!UICONTROL Logout]**: hiermee meldt u zich af van de extensie, waarbij u zich opnieuw moet aanmelden.
* **[!UICONTROL Quit Activity Map]**: hiermee worden alle bedekkingen voor de extensie gesloten (X-pictogram).

## Paginabedekking

De paginabedekking bevat uw site-inhoud met een bedekking die u de locatie laat zien van de populairste koppelingen waarop tijdens de rapportageperiode is geklikt. U kunt deze koppelingsoverlays zodanig configureren dat deze als bellen of verlopen worden weergegeven in de bovenste deelvensters **[!UICONTROL Overlay visualization type]** .

Als u op een ballon of een verloop klikt, kunt u details voor die bepaalde verbinding bekijken.

![ Bubble van de Verbinding ](../assets/link-bubble.png)

## Deelvenster Onder

In het onderste deelvenster ziet u een geaggregeerde weergave van de koppelingen die op de overlay worden weergegeven.

* **type van Rapport**: Knevel het bodempaneel om het **[!UICONTROL Links on page]** rapport of het **[!UICONTROL Page details]** rapport te tonen.
* **[!UICONTROL Page name]**: De huidige [ pagina ](/help/components/dimensions/page.md) afmetingsnaam.
* **[!UICONTROL Search]**: Filter het rapport zodat alleen de koppelingsnamen worden weergegeven die overeenkomen met de ingevoerde tekst.
* **[!UICONTROL Download]**: exporteert het rapport naar CSV. U kunt het rapport [!UICONTROL Links on page] , het rapport [!UICONTROL Page] en het rapport [!UICONTROL Page flow] in hetzelfde downloadbestand opnemen.
* **[!UICONTROL Change report docking position]**: hiermee schakelt u de positie van dit deelvenster in of uit op het onderste of bovenste gedeelte van het browservenster.
* **[!UICONTROL Close the report]**: sluit dit deelvenster. U kunt het deelvenster opnieuw openen met de knop **[!UICONTROL Toggle page details]** in het bovenste deelvenster (het oogpictogram).

Het rapport **[!UICONTROL Links on page]** bevat een basiswerkruimterapport met de volgende instellingen:

* De [ de verbinding van Activity Map ](/help/components/dimensions/activity-map-link.md) dimensie
* [ komt voor ](/help/components/metrics/occurrences.md) metrisch (geëtiketteerd als **[!UICONTROL Link clicks]**)
* De huidige [ pagina ](/help/components/dimensions/page.md) waarde die als segment wordt toegepast

![ Verbindingen op paginapaneel ](../assets/links-on-page.png)

Het **[!UICONTROL Page details]** rapport toont de visualisatie van de a [ Stroom ](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) gebruikend de [ pagina ](/help/components/dimensions/page.md) dimensie, die op de huidige pagina concentreren. De volgende maatstaven voor de huidige pagina worden links weergegeven:

* Totaal [ paginameningen ](/help/components/metrics/page-views.md)
* [!UICONTROL % of all page views]
* [ Ingang ](/help/components/metrics/entries.md) telling
* [ Uitgang ](/help/components/metrics/exits.md) aantal
* [Eén pagina bezoeken](/help/components/metrics/single-page-visits.md)
* [!UICONTROL Avg clicks to page]
* Gemiddelde [ Tijd besteed aan pagina ](/help/components/metrics/time-spent.md)
* Aantal [ herlaadt ](/help/components/metrics/reloads.md)
* [Stuitpercentage](/help/components/metrics/bounce-rate.md)
* [!UICONTROL Link clicks]

![Paginadata](../assets/page-details.png)
