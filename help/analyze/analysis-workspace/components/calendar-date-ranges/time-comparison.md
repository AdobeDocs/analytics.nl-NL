---
description: Met Datumvergelijking in Analysis Workspace kunt u elke kolom met een datumbereik gebruiken en een algemene datumvergelijking maken, zoals jaar-over-jaar, kwartaal-over-kwartaal, maand-over-maand enzovoort.
title: Datumvergelijking
feature: Calendar
role: User, Admin
exl-id: ea7a42ef-89de-4f70-b468-8a5cf69fea05
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 5%

---

# Datumvergelijking

Met Datumvergelijking in Analysis Workspace kunt u elke kolom met een datumbereik gebruiken en een algemene datumvergelijking maken, zoals: jaar-over-jaar, kwartaal-over-kwartaal, maand-over-maand enzovoort.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ vergelijking van de Datum ](https://video.tv.adobe.com/v/30753?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]



## Vergelijk tijdsperiodes {#section_C4E36BFE0F5C4378A74E705747C9DEE4}

>[!NOTE]
>[!UICONTROL Compare Time Periods] maakt gebruik van geavanceerde berekende cijfers. Dientengevolge, is het beschikbaar slechts aan klanten met Analytics Uitgezochte, Prime, en SKUs van Ultimate.

De analyse vereist context, en vaak wordt die context verstrekt door een vorige tijdspanne. Bijvoorbeeld de vraag &quot;Hoeveel beter of slechter doen we dan op dit moment vorig jaar?&quot; is fundamenteel voor het begrijpen van uw zaken. De Vergelijking van de datum omvat automatisch een &quot;verschilkolom&quot;, die de percentageverandering in vergelijking met een gespecificeerde tijdspanne toont.

1. Maak een tabel voor vrije vorm met de afmetingen en metriek die u over een tijdsperiode wilt vergelijken.
1. Klik met de rechtermuisknop op een tabelrij en selecteer **[!UICONTROL Compare time periods]** .

   ![](assets/compare-time.png)

   >[!NOTE]
   >
   >Deze klikoptie is gehandicapt voor metrische rijen, de rijen van de datumwaaier, en de rijen van de tijddimensie.

1. Afhankelijk van de manier waarop u het datumbereik van de tabel hebt ingesteld, kunt u het volgende vergelijken:

   | Optie | Beschrijving |
   |---|---|
   | **[!UICONTROL Prior week/month/quarter/year to this date range]** | Vergelijkt met week/maand/enz. onmiddellijk voor dit datumbereik. |
   | **[!UICONTROL This week/month/quarter/year last year to this date range]** | Vergelijkt tot de zelfde datumwaaier een jaar geleden. |
   | **[!UICONTROL Custom date range to this date range]** | Hiermee kunt u een aangepast datumbereik selecteren. |

   >[!NOTE]
   >
   >Wanneer u een aangepast aantal dagen selecteert, bijvoorbeeld 7 oktober - 20 oktober (een bereik van 14 dagen), krijgt u slechts twee opties: **[!UICONTROL Prior 14 days before this date range]** en **[!UICONTROL Custom date range to this date range]** .

1. De resulterende vergelijking ziet er als volgt uit:

   ![](assets/compare-time-result.png)

   De rijen in de kolom Percentage wijziging worden rood weergegeven voor negatieve waarden en groen voor positieve waarden.

1. (Optioneel) Net als bij andere Workspace-projecten kunt u op basis van deze tijdvergelijkingen visualisaties maken. Hier ziet u bijvoorbeeld een staafgrafiek:

   ![](assets/compare-time-barchart.png)

   Als u het percentage van de wijziging in het staafdiagram wilt weergeven, moet de instelling [!UICONTROL Percentages] zijn ingecheckt in [!UICONTROL Visualization Settings] .

## Een tijdspannekolom toevoegen ter vergelijking {#section_93CC2B4F48504125BEC104046A32EB93}

U kunt nu een tijdsperiode toevoegen aan elke tabelkolom. Zo kunt u een andere tijdsperiode toevoegen dan de periode waarop uw kalender is ingesteld. Dit is een andere manier om datums te vergelijken.

1. Klik met de rechtermuisknop op een kolom in de tabel en selecteer **[!UICONTROL Add time period column]** .

   ![](assets/add-time-period-column.png)

1. Afhankelijk van de manier waarop u het datumbereik van de tabel hebt ingesteld, kunt u het volgende vergelijken:

   | Optie | Beschrijving |
   |---|---|
   | **[!UICONTROL Prior week/month/quarter/year to this date range]** | Voegt een kolom met de week/maand/enz. toe. onmiddellijk voor dit datumbereik. |
   | **[!UICONTROL This week/month/quarter/year last year to this date range]** | Hiermee voegt u hetzelfde datumbereik toe een jaar geleden. |
   | **[!UICONTROL Custom date range to this date range]** | Hiermee kunt u een aangepast datumbereik selecteren. |

   >[!NOTE]
   >
   >Wanneer u een aangepast aantal dagen selecteert, bijvoorbeeld 7 oktober - 20 oktober (een bereik van 14 dagen), krijgt u slechts twee opties: **[!UICONTROL Prior 14 days before this date range]** en **[!UICONTROL Custom date range to this date range]** .

1. De tijdsperiode wordt ingevoegd vóór de kolom die u hebt geselecteerd:

   ![](assets/add-time-period-column2.png)

1. U kunt zoveel tijdkolommen toevoegen als u wilt, maar u kunt ook verschillende datumbereiken combineren en met elkaar in overeenstemming brengen:

   ![](assets/add-time-period-column4.png)

1. Bovendien kunt u op elke kolom sorteren, die de orde van dagen afhankelijk van de kolom zult veranderen u sorteert.

## Kolom-datums uitlijnen zodat deze op dezelfde rij beginnen {#section_5085E200082048CB899C3F355062A733}

U kunt de datums van elke kolom uitlijnen op alle datums die op dezelfde rij beginnen.

Als u bijvoorbeeld kiest om de datums op één lijn te brengen en u een vergelijking maakt van maand tot maand tussen oktober en september 2016, begint de linkerkolom met 1 oktober en begint de rechterkolom met 1 september:

![](assets/add-time-period-column3.png)

>[!NOTE]
>
>Houd rekening met het volgende wanneer u deze optie gebruikt:
>
>* Deze instelling wordt standaard ingeschakeld voor alle nieuwe projecten.
>
>* Deze instelling is van toepassing op de hele tabel. Als u deze instelling bijvoorbeeld wijzigt voor een indeling in de tabel, wordt de instelling voor de hele tabel gewijzigd.
>

Deze instelling inschakelen als deze nog niet is ingeschakeld:

1. In de lijst waar u kolomdata wilt richten, selecteer het **pictogram van Montages** in de lijstkopbal.

1. Voor het [!UICONTROL **lusje van Montages**], uitgezochte **[!UICONTROL Align Dates from each column to all start on the same row (applies to entire table)]**.

![](assets/date-comparison-setting.png)


