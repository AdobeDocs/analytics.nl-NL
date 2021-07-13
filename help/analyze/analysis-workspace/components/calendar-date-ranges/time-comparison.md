---
description: Met Datumvergelijking in Analysis Workspace kunt u elke kolom met een datumbereik gebruiken en een algemene datumvergelijking maken, zoals jaar-over-jaar, kwartaal-over-kwartaal, maand-over-maand enzovoort.
title: Datumvergelijking
uuid: ef18f9d9-b6ad-4859-b7c9-9750ca0df519
feature: Basisprincipes van werkruimte
role: User, Admin
exl-id: ea7a42ef-89de-4f70-b468-8a5cf69fea05
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 6%

---

# Datumvergelijking

Met Datumvergelijking in Analysis Workspace kunt u elke kolom met een datumbereik gebruiken en een algemene datumvergelijking maken, zoals: jaar-over-jaar, kwartaal-over-kwartaal, maand-over-maand, enz.

## Vergelijk tijdsperiodes {#section_C4E36BFE0F5C4378A74E705747C9DEE4}

>[!NOTE]
>[!UICONTROL Compare Time Periods] hefboomwerkingen geavanceerde Berekende Metriek. Dientengevolge, is het beschikbaar slechts aan klanten met Analytics Uitgezochte, eerste, en Ultimate SKUs.

De analyse vereist context, en vaak wordt die context verstrekt door een vorige tijdspanne. Bijvoorbeeld de vraag &quot;Hoeveel beter/slechter doen we dan op dit moment vorig jaar?&quot; is fundamenteel voor het begrijpen van uw zaken. De Vergelijking van de datum omvat automatisch een &quot;verschilkolom&quot;, die de percentageverandering in vergelijking met een gespecificeerde tijdspanne toont.

1. Maak een tabel voor vrije vorm met de afmetingen en metriek die u over een tijdsperiode wilt vergelijken.
1. Klik met de rechtermuisknop op een tabelrij en selecteer **[!UICONTROL Compare Time Periods]**.

   ![](assets/compare-time.png)

   >[!IMPORTANT]
   >
   >Deze klikoptie is gehandicapt voor metrische rijen, de rijen van de datumwaaier, en de rijen van de tijddimensie.

1. Afhankelijk van de manier waarop u het datumbereik van de tabel hebt ingesteld, kunt u het volgende vergelijken:

   | Optie | Beschrijving |
   |---|---|
   | **[!UICONTROL Prior week/month/quarter/year to this date range]** | Vergelijkt met week/maand/enz. onmiddellijk voor dit datumbereik. |
   | **[!UICONTROL This week/month/quarter/year last year]** | Vergelijkt tot de zelfde datumwaaier een jaar geleden. |
   | **[!UICONTROL Select range]** | Hiermee kunt u een aangepast datumbereik selecteren. |

   >[!NOTE]
   >
   >Wanneer u een aangepast aantal dagen selecteert, bijvoorbeeld 7 oktober - 20 oktober (een bereik van 14 dagen), krijgt u slechts twee opties: **[!UICONTROL Prior 14 days before this date range]** en **[!UICONTROL Select range]**.

1. De resulterende vergelijking ziet er als volgt uit:

   ![](assets/compare-time-result.png)

   De rijen in de kolom Percentage wijziging worden rood weergegeven voor negatieve waarden en groen voor positieve waarden.

1. (Optioneel) Net als bij andere Workspace-projecten kunt u visualisaties maken op basis van deze tijdvergelijkingen. Hier ziet u bijvoorbeeld een staafgrafiek:

   ![](assets/compare-time-barchart.png)

   Merk op dat om de percentageverandering in het bar grafiek te tonen, u [!UICONTROL Percentages] het plaatsen moet hebben gecontroleerd in [!UICONTROL Visualization Settings].

## Een tijdspannekolom toevoegen ter vergelijking {#section_93CC2B4F48504125BEC104046A32EB93}

U kunt nu een tijdsperiode toevoegen aan elke tabelkolom. Zo kunt u een andere tijdsperiode toevoegen dan de periode waarop uw kalender is ingesteld. Dit is een andere manier om datums te vergelijken.

1. Klik met de rechtermuisknop op een kolom in de tabel en selecteer **[!UICONTROL Add Time Period Column]** ![](assets/add-time-period-column.png)

1. Afhankelijk van de manier waarop u het datumbereik van de tabel hebt ingesteld, kunt u het volgende vergelijken:

   | Optie | Beschrijving |
   |---|---|
   | **[!UICONTROL Prior week/month/quarter/year to this date range]** | Voegt een kolom met de week/maand/enz. toe. onmiddellijk voor dit datumbereik. |
   | **[!UICONTROL This week/month/quarter/year last year]** | Hiermee voegt u hetzelfde datumbereik toe een jaar geleden. |
   | **[!UICONTROL Select range]** | Hiermee kunt u een aangepast datumbereik selecteren. |

   >[!NOTE]
   >
   >Wanneer u een aangepast aantal dagen selecteert, bijvoorbeeld 7 oktober - 20 oktober (een bereik van 14 dagen), krijgt u slechts twee opties: **[!UICONTROL Prior 14 days before this date range]** en **[!UICONTROL Select range]**.

1. De tijdsperiode wordt ingevoegd vóór de kolom die u hebt geselecteerd:

   ![](assets/add-time-period-column2.png)

1. U kunt zoveel tijdkolommen toevoegen als u wilt, maar u kunt ook verschillende datumbereiken combineren en met elkaar in overeenstemming brengen:

   ![](assets/add-time-period-column4.png)

1. Bovendien kunt u op elke kolom sorteren, die de orde van dagen afhankelijk van de kolom zult veranderen u sorteert.

## Kolom-datums uitlijnen zodat deze op dezelfde rij beginnen {#section_5085E200082048CB899C3F355062A733}

Met een nieuwe instelling voor alle tabellen kunt u **[!UICONTROL Align Dates from each column to all start on the same row (applies to entire table)]**. &quot;Is van toepassing op volledige lijst&quot;betekent dat als u, bijvoorbeeld een uitsplitsing in de lijst doet, en als u dit het plaatsen voor de uitsplitsing verandert, het het plaatsen voor de volledige lijst zal veranderen.

![](assets/date-comparison-setting.png)

>[!IMPORTANT]
>
>Deze instelling is **uitgeschakeld** (uitgeschakeld) voor alle bestaande projecten en **ingeschakeld** (ingeschakeld) voor alle nieuwe projecten.

Voorbeeld: Wanneer u ervoor kiest om de datums op één lijn te brengen, als u een maand-over-maand vergelijking tussen oktober en september 2016 doet, zal de linkerkolom met 1 Oktober beginnen en de juiste kolom zal met 1 September beginnen:

![](assets/add-time-period-column3.png)

<!-- 

<p>See Jonny Moon's email from November 3. </p>

 -->
