---
description: Met kolominstellingen kunt u kolomopmaak configureren, waarvan sommige voorwaardelijk kunnen zijn.
title: Kolominstellingen
uuid: 151d66da-04f7-4d0f-985c-4fdd92bc1308
feature: Freeform Tables
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 20%

---


# [!UICONTROL Column Settings]

[!UICONTROL Column Settings] Laat u kolom het formatteren vormen, wat waarvan voorwaardelijk kan zijn.

## [!UICONTROL Column Settings] {#edit-column-settings} bewerken

Als u [!UICONTROL Column Settings] wilt openen, sleept u een tabel voor vrije vorm naar het project en klikt u op het tandwielpictogram in de kolomkop.

![](assets/column_settings.png)

U kunt instellingen **voor meerdere kolommen tegelijk bewerken**. Dit is heel eenvoudig: selecteer meerdere kolommen en klik op het instellingenpictogram van een van de kolommen. Alle wijzigingen die u aanbrengt, worden toegepast op alle kolommen waarin u cellen hebt geselecteerd.

| Element | Beschrijving |
| --- | --- |
| **Totaal aantal cellen** |  |
| Totalen tonen | Dit totaal is doorgaans gelijk aan of een subset van [!UICONTROL Grand Total]. Het geeft alle tabelfilters weer die binnen de vrije-vormtabel worden toegepast, inclusief de optie [!UICONTROL Include None]. |
| Totaal-generaal tonen | Dit totaal vertegenwoordigt alle treffers die zijn verzameld, soms genoemd &quot;rapportsuite total&quot;. Wanneer een segment wordt toegepast op deelvensterniveau of binnen de vrije-vormtabel, wordt dit totaal aangepast aan alle resultaten die overeenkomen met de segmentcriteria. Groot totaal wordt niet ondersteund voor tabellen of uitsplitsingen met [statische rijen](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md). |
| **Tabelcellen** |  |
| Getal | Hiermee wordt bepaald of in een cel de numerieke waarde voor de metrische waarde wordt weergegeven of verborgen. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de numerieke waarde het aantal paginaweergaven voor het rij-item. |
| Percentage | Bepaalt of een cel de percentagewaarde voor metrisch toont/verbergt. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de percentagewaarde het aantal paginaweergaven voor het rijitem gedeeld door de totale paginaweergaven voor de kolom.  Opmerking:  We kunnen percentages van meer dan 100 procent laten zien, om nauwkeuriger te zijn. We verplaatsen het bovenste gebonden plafond ook naar 1000% om ervoor te zorgen dat kolommen te groot kunnen worden. |
| Anomalies | Hiermee wordt bepaald of de waarden in deze kolom een anomaliedetectie uitvoeren. |
| Tekst tekstomloop | Hiermee kunt u de koptekst laten omlopen in Freeform-tabellen om kopteksten leesbaarder te maken en tabellen beter deelbaar te maken. Dit is handig voor .pdf-rendering en voor metriek met lange namen. Standaard ingeschakeld. |
| nul interpreteren als geen waarde | Voor cellen met een waarde 0 bepaalt u of een cel van 0 of een lege cel moet worden weergegeven. Dit is handig wanneer u gegevens bekijkt voor elke dag van een maand, en sommige dagen zijn nog niet gebeurd.  In plaats van &#39;0&#39; voor toekomstige datums weer te geven, kunnen lege cellen worden weergegeven. Grafieken voldoen ook aan deze instelling (ze geven dus geen lijn of balk weer met 0 waarden als deze instelling is ingeschakeld). |
| Achtergrond | Hiermee bepaalt u of alle celopmaak, inclusief de staafgrafiek en voorwaardelijke opmaak, in een cel wordt weergegeven of verborgen. |
| Staafgrafiek | Hiermee wordt een horizontale staafgrafiek weergegeven die de waarde van de cel ten opzichte van het totaal voor de kolom vertegenwoordigt. |
| Voorwaardelijke opmaak | Zie de onderstaande paragraaf. |
| Voorvertoning tabelcel | Toont een voorproef van hoe elke cel met de momenteel geselecteerde opmaakopties wordt getoond. |

## Voorwaardelijke opmaak {#conditional-formatting}

Met voorwaardelijke opmaak wordt opmaak toegepast op de bovenste, middelste en onderste limieten die u kunt definiëren. Het toepassen van voorwaardelijke opmaak (kleuren, enz.) in Freeform-tabellen wordt ook automatisch ingeschakeld voor onderverdelingen, tenzij &quot;Aangepaste&quot; limieten zijn geselecteerd.

![](assets/conditional-formatting.png)

| Element | Beschrijving |
| --- | --- |
| Voorwaardelijke opmaak | Hiermee worden de volgende kleuren toegepast op cellen, op basis van datawaarden worden: <ul><li>Groen: hoge waarden</li><li>Geel: middelpuntwaarden</li><li>Rood: lage waarden</li></ul> <br> Als u een dimensie in de tabel vervangt, worden de limieten voor voorwaardelijke opmaak opnieuw ingesteld. Wanneer u een metric vervangt, worden de limieten voor die kolom opnieuw berekend (waarbij de metric op de X-as staat en de dimensie op de Y-as). |
| Percentagelimieten gebruiken | Wijzig het limietbereik zodat dit op percentages wordt gebaseerd in plaats van op absolute waarden. Dit werkt voor metriek die uitsluitend op percentage-gebaseerd (zoals het Tarief van de Stuiting) evenals voor metriek zijn die een telling en een percentage (zoals de Weergaven van de Pagina. hebben) |
| Automatisch genereren | Berekent automatisch de bovenste/middelste/onderste limieten op basis van de gegevens. De bovengrens is de hoogste waarde in deze kolom. De ondergrens is de laagste en het middelpunt is het gemiddelde van de boven- en ondergrens. |
| Aangepast | Handmatig bovenste/middelste/onderste limieten toewijzen. Dit biedt u de flexibiliteit om te bepalen wanneer een kolomwaarde goed, gemiddeld, of slecht wordt. |

## Niet-standaard toewijzingsmodel gebruiken {#attribution}

Analysis Workspace ondersteunt [attributie](/help/analyze/analysis-workspace/attribution/overview.md) voor bijna elke metrische waarde.

1. Klik op het pictogram Instellingen (versnelling) in een kolom Tabel vrije vorm.

   ![Selectievakje voor kenmerken](assets/attribution-checkbox.png)

1. Controleer **[!UICONTROL Use non-default attribution model]** onder **[!UICONTROL Data Settings]**. Zie [Attributiemodellen](/help/analyze/analysis-workspace/attribution/models.md) voor meer informatie over verschillende attributiemodellen.

   ![Kenmerkingsmodel selecteren](assets/attribution-select.png)

>[!MORELIKETHIS]
>
>* [Databronnen beheren](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md)

