---
description: Leer hoe u kolominstellingen kunt bewerken om kolomopmaak te configureren, waarvan sommige voorwaardelijk kunnen zijn.
title: Kolominstellingen
uuid: 151d66da-04f7-4d0f-985c-4fdd92bc1308
feature: Freeform Tables
role: User, Admin
exl-id: 82034838-b015-4ca2-adb6-736f20a478d8
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 7%

---


# Kolominstellingen

Met [!UICONTROL Column settings] kunt u kolomopmaak configureren, waarvan sommige voorwaardelijk kunnen zijn.


>[!BEGINSHADEBOX]

Zie ![&#x200B; &#x200B;](/help/assets/icons/VideoCheckedOut.svg) Rij en kolommontages 0&rbrace; VideoCheckedOut in een Vrije vormlijst [&#x200B; voor een demo video.](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/row-and-column-settings-in-freeform-tables){target="_blank"}

>[!ENDSHADEBOX]


Om tot [!UICONTROL Column settings] toegang te hebben, selecteer ![&#x200B; montages van de Kolom &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg) in de kolomrubriek.

![Kolominstellingen](assets/column-settings.png)


U kunt instellingen voor meerdere kolommen tegelijk bewerken. Selecteer veelvoudige kolommen en selecteer ![&#x200B; Plaatsend &#x200B;](/help/assets/icons/Setting.svg) in om het even welke geselecteerde kolommen. Alle wijzigingen die u aanbrengt, worden toegepast op alle kolommen met cellen die erin zijn geselecteerd.

| Optie | Beschrijving |
| --- | --- |
| **[!UICONTROL Show total]** | Een som van de kolommen aan de clientzijde weergeven. Dit totaal **&#x200B;**&#x200B;dedupliceert metriek zoals zittingen of personen niet. |
| **[!UICONTROL Show grand total]** | Toon een server-zijsom van de kolom. Het totaal-generaal dedupliceert metriek zoals zittingen of personen. |
| **[!UICONTROL Show sparkline]** | Een lijndiagram weergeven bij de kolomkop. |
| **[!UICONTROL Number]** | Bepaal of een cel de numerieke waarde voor de metrische waarde weergeeft/verbergt. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de numerieke waarde het aantal paginaweergaven voor het rij-item. |
| **[!UICONTROL Percent]** | Bepaal of een cel de percentagewaarde voor metrisch toont/verbergt. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de percentagewaarde het aantal paginaweergaven voor het rijitem, gedeeld door de totale paginaweergaven voor de kolom.  Opmerking: percentages van meer dan 100% zijn mogelijk om accuraat te zijn. Het bovenste gebonden uiteinde kan naar 1.000% worden verplaatst om te voorkomen dat de kolombreedte te groot wordt. |
| **[!UICONTROL Show anomalies]** | Bepaal of de waarden in deze kolom een anomaliedetectie uitvoeren. |
| **[!UICONTROL Show forecast]** | Bepaal of de voorspelde waarden in deze kolom worden weergegeven. |
| **[!UICONTROL Wrap header text]** | Plaats de koptekst in Freeform-tabellen om kopteksten leesbaarder te maken en tabellen beter deelbaar te maken. Overvullen is handig voor PDF-rendering en voor metrische objecten met lange namen. Standaard ingeschakeld. |
| **[!UICONTROL Interpret zero as no value]** | Bepaal of voor cellen met een waarde 0 een cel of een lege cel moet worden weergegeven. Deze interpretatie is handig wanneer u gegevens voor elke dag van een maand bekijkt en bepaalde dagen in de toekomst.  In plaats van &#39;0&#39; voor toekomstige datums weer te geven, worden lege cellen weergegeven. Bij grafieken wordt deze instelling ook gebruikt (diagrammen geven geen lijn of balk met 0 waarden weer). |
| **[!UICONTROL Background]** | Bepaal of in een cel alle celopmaak wordt weergegeven of verborgen, inclusief de staafgrafiek en voorwaardelijke opmaak. |
| **[!UICONTROL Bar Graph]** | Een horizontale staafgrafiek tonen die de waarde van de cel ten opzichte van het totaal voor de kolom vertegenwoordigt. |
| **[!UICONTROL Conditional Formatting]** | Gebruik voorwaardelijke opmaak. Zie de [&#x200B; sectie &#x200B;](#conditional-formatting) hieronder. |
| **[!UICONTROL Table Cell Preview]** | Een voorbeeld van hoe elke cel wordt weergegeven met de momenteel geselecteerde opmaakopties toegepast. |
| **[!UICONTROL Use non-default attribution model]** | Gebruik een niet-standaard toewijzingsmodel. Zie de [&#x200B; sectie &#x200B;](#use-non-default-attribution-model) hieronder. |

## Voorwaardelijke opmaak {#conditional-formatting}

Met voorwaardelijke opmaak wordt opmaak toegepast op de bovenste, middelste en onderste limieten die u kunt definiëren. Het toepassen van voorwaardelijke opmaak in Freeform-tabellen wordt ook automatisch ingeschakeld voor uitsplitsingen, tenzij [!UICONTROL Custom] limieten zijn geselecteerd.

![&#x200B; Voorwaardelijke het formatteren &#x200B;](./assets/conditional-formatting.png)

| Opties voor voorwaardelijke opmaak | Beschrijving |
| --- | --- |
| **[!UICONTROL &#x200B; Use percent limits]** | Wijzig het limietbereik zodat dit op percentages wordt gebaseerd in plaats van op absolute waarden. Het percentagelimietbereik werkt voor metriek die uitsluitend op percentage gebaseerd zijn (zoals Stuitsnelheid) en voor metriek die een telling en een percentage hebben (zoals Paginaweergaven). |
| **[!UICONTROL Auto-generated]** | Berekent automatisch de bovenste/middelste/onderste limieten op basis van de gegevens. De bovengrens is de hoogste waarde in deze kolom. De ondergrens is de laagste en het middelpunt is het gemiddelde van de boven- en ondergrens. |
| **[!UICONTROL Custom]** | Wijs **[!UICONTROL Upper limit]**, **[!UICONTROL Midpoint]** en **[!UICONTROL Lower limit]** handmatig toe. De grenzen verstrekken de flexibiliteit om te bepalen wanneer een kolomwaarde goed, gemiddeld, of slecht wordt. |
| **[!UICONTROL Conditional formatting palette]** | Pas een vooraf geconfigureerde kleurenset toe op cellen. Afhankelijk van welke van de vier beschikbare kleurenschema&#39;s u selecteert, worden de verschillende kleuren toegewezen aan hoge waarden, middelpuntwaarden, en lage waarden. <br> Als u een dimensie in de tabel vervangt, worden de limieten voor voorwaardelijke opmaak opnieuw ingesteld. Wanneer u een metric vervangt, worden de limieten voor die kolom opnieuw berekend (waarbij de metric op de X-as staat en de dimensie op de Y-as). |

## Niet-standaard toewijzingsmodel gebruiken {#use-non-default-attribution-model}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_column_usenondefaultattributionmodel"
>title="Niet-standaard toewijzingsmodel gebruiken"
>abstract="Schakel een niet-standaard toewijzingsmodel in voor de geselecteerde kolommen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_column_usenondefaultattributionmodel_disabled"
>title="Niet-standaard toewijzingsmodel gebruiken"
>abstract="Niet-standaardtoewijzingsmodus is niet beschikbaar voor deze metrische waarde."

<!-- markdownlint-enable MD034 -->


>[!NOTE]
>
>Houd rekening met het volgende wanneer u de toewijzing van een component bijwerkt naar een niet-standaard toewijzingsmodel:
>
>* **wanneer het gebruiken van de component in een rapport met *één enkele afmeting*:** de attributie van de component negeert het toewijzingsmodel wanneer een niet-gebrek attributiemodel wordt gebruikt.
>
>* **wanneer het gebruiken van de component in een rapport met *veelvoudige afmetingen*:** de attributie van de component behoudt het toewijzingsmodel wanneer een niet-gebrek attributiemodel wordt gebruikt.
>
>

Een niet-standaard toewijzingsmodel gebruiken voor een metrisch object in Analysis Workspace:

1. Selecteer **[!UICONTROL Use non-default attribution model]** . Als deze optie al is geselecteerd, gebruikt u **[!UICONTROL Edit]** om het toewijzingsmodel te bewerken. U kunt ook de selectie opheffen om terug te keren naar het standaardtoewijzingsmodel.

   ![&#x200B; de Kolom die opties plaatst die de optie van de Montages van Gegevens benadrukken: Gebruik niet-standaardattributiemodus.](assets/attribution-checkbox.png)

2. Selecteer in **[!UICONTROL Column attribution model]** een **[!UICONTROL Model]** en een **[!UICONTROL Lookback window]** . Het terugkijkvenster bepaalt het venster van gegevensattributie dat voor elke omzetting wordt toegepast.

   ![&#x200B; de Opties van het Model van de Attributie van de Kolom die Lineair tonen.](assets/attribution-select.png)


### Attributiemodellen

{{attribution-models-details}}


### Container

{{attribution-container}}


### Venster Opzoeken

{{attribution-lookback-window}}


### Voorbeeld

{{attribution-example}}

>[!MORELIKETHIS]
>
>* [Databronnen beheren](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md)


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; Dynamische kolommen &#x200B;](https://video.tv.adobe.com/v/23138?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

