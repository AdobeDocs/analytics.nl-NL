---
description: Het segmenteren op individuele metriek staat u toe om metrische vergelijkingen binnen het zelfde rapport te maken.
title: Gesegmenteerde cijfers
feature: Calculated Metrics
exl-id: 1e7e048b-9d90-49aa-adcc-15876c864e04
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Gesegmenteerde cijfers

In de Berekende metrische bouwer, kunt u segmenten binnen uw metrische definitie toepassen. Dit is nuttig als u nieuwe metriek aan gebruik in uw analyse wilt afleiden. Houd in mening, kunnen de segmentdefinities door de bouwer van het Segment worden bijgewerkt. Als de veranderingen worden aangebracht, zal het segment automatisch bijwerken overal het wordt toegepast, met inbegrip van als het deel van een berekende metrische definitie uitmaakt.

![](assets/german-visitors.png)

## Een gesegmenteerde metrisch maken {#create}

Laten we zeggen dat u verschillende aspecten van een &quot;Duitse bezoeker&quot;-segment wilt vergelijken met die van een &quot;International Visitors&quot;-segment. U kunt metriek tot stand brengen die u inzichten zoals zal geven:

* Hoe vergelijk het gedrag van bladeren door inhoud tussen de twee groepen? (Een ander voorbeeld is: Hoe vergelijk de omrekeningskoers tussen de twee segmenten?)
* Hoeveel Duitse bezoekers zijn als percentage van het totale aantal bezoekers op bepaalde pagina&#39;s te vinden, in tegenstelling tot internationale bezoekers?
* Waar zijn de grootste verschillen in termen van welke inhoud door deze verschillende segmenten wordt betreden?

1. Als u geen vergelijkbaar segment hebt, maakt u een ad-hocsegment in de Berekende metrische bouwer met de naam &quot;Duitse bezoekers&quot;, waarbij &quot;Landen&quot; gelijk is aan &quot;Duitsland&quot;. Sleep gewoon de dimensie Landen naar het canvas Definition en selecteer Duitsland als waarde:

   ![](assets/segment-from-dimension.png)

   >[!NOTE]
   >
   >U kunt dit ook doen in het dialoogvenster [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-build.md), maar we hebben de workflow vereenvoudigd door afmetingen beschikbaar te maken in de Calculated Metric Builder. &quot;Ad hoc&quot; betekent dat het segment niet zichtbaar is in de **[!UICONTROL Segments]** lijst in de linkerspoorstaaf. U kunt het echter openbaar maken door de muisaanwijzer boven het pictogram &quot;i&quot; naast het pictogram te plaatsen en op **[!UICONTROL Make public]**.

1. Als u geen vergelijkbaar segment hebt, maakt u een segment met de naam &quot;Internationale Bezoekers&quot;, waarbij &quot;Landen&quot; niet gelijk is aan &quot;Duitsland&quot;.
1. Bouw en bewaar metrisch genoemd &quot;Duitse Bezoekers&quot;door het segment van Duitsland in het canvas van de Definitie te slepen en de Unieke Bezoekers metrisch binnen het te slepen:

   ![](assets/german-visitors.png)

1. Herhaal Stap 3 met het Internationale segment van Bezoekers en de Unieke metrisch van Bezoekers om Internationale metrische Bezoekers tot stand te brengen.
1. Sleep in Analysis Workspace de **[!UICONTROL Page]** Dimension in een lijst van de Vrije Vorm en sleep de 2 nieuwe berekende metriek naast elkaar aan de bovenkant:

   ![](assets/workspace-pages.png)

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/25407/?quality=12)

## Percentage van totale metriek {#percent-total}

U kunt het voorbeeld boven een stap verder nemen door uw segment te vergelijken met een totale populatie. Hiertoe maakt u twee nieuwe meeteenheden: &quot;% van de totale Duitse bezoekers&quot; en &quot;% van de totale internationale bezoekers&quot;:

1. Verplaats het segment Duitse (of internationale) bezoekers naar het canvas.
1. Zet een ander Duits (of Internationaal) bezoekerssegment hieronder neer. Deze keer klikt u echter op het pictogram voor configuratie (versnelling) om het metrische type &quot;Totaal&quot; te selecteren. De notatie moet &#39;Percentage&#39; zijn. De exploitant zou &quot;gedeeld door&quot;moeten zijn. U eindigt omhoog met deze metrische definitie:

   ![](assets/cm_metric_total.png)

1. Pas deze metrisch op uw project toe:

   ![](assets/cm_percent_total.png)
