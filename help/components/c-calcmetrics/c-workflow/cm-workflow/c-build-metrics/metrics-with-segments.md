---
description: Het segmenteren op individuele metriek staat u toe om metrische vergelijkingen binnen het zelfde rapport te maken.
title: Gesegmenteerde metriek
feature: Calculated Metrics
exl-id: 1e7e048b-9d90-49aa-adcc-15876c864e04
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# Gesegmenteerde metriek

In de Berekende metrische bouwer, kunt u segmenten binnen uw metrische definitie toepassen. Dit is nuttig als u nieuwe metriek aan gebruik in uw analyse wilt afleiden. Houd in mening, kunnen de segmentdefinities door de bouwer van het Segment worden bijgewerkt. Als de veranderingen worden aangebracht, zal het segment automatisch bijwerken overal het wordt toegepast, met inbegrip van als het deel van een berekende metrische definitie uitmaakt.

![](assets/german-visitors.png)

## Een gesegmenteerde metrisch maken {#create}

Laten we zeggen dat u verschillende aspecten van een &quot;Duitse bezoeker&quot;-segment wilt vergelijken met die van een &quot;International Visitors&quot;-segment. U kunt metriek tot stand brengen die u inzichten zoals zal geven:

* Hoe vergelijk het gedrag van bladeren door inhoud tussen de twee groepen? (Een ander voorbeeld zou zijn: Hoe vergelijk de omrekeningskoers tussen de twee segmenten?)
* Hoeveel Duitse bezoekers zijn als percentage van het totale aantal bezoekers op bepaalde pagina&#39;s te vinden, in tegenstelling tot internationale bezoekers?
* Waar zijn de grootste verschillen in termen van welke inhoud door deze verschillende segmenten wordt betreden?

Bouw en bewaar metrisch genoemd &quot;Duitse Bezoekers&quot;en metrisch genoemd &quot;Internationale Bezoekers&quot;:

1. Maak een ad-hocsegment in de berekende metrische bouwer, &quot;Duitse bezoekers&quot; genoemd, waarbij &quot;Landen&quot; gelijk is aan &quot;Duitsland&quot;.

   Sleep de dimensie van Landen in het canvas van de Definitie en selecteer [!UICONTROL **Duitsland**] als waarde:

   ![](assets/segment-from-dimension.png)

   >[!NOTE]
   >
   >U kunt dit in de [ Bouwer van het Segment ](/help/components/segmentation/segmentation-workflow/seg-build.md) ook doen, maar wij hebben het werkschema vereenvoudigd door dimensies beschikbaar te maken in de Berekende metrische bouwer. &quot;Ad hoc&quot; betekent dat het segment niet zichtbaar is in de **[!UICONTROL Segments]** -lijst in de linkertrack. U kunt het bestand echter openbaar maken door de muisaanwijzer boven het pictogram &quot;i&quot; naast het object te plaatsen en op **[!UICONTROL Make public]** te klikken.

1. Sleep het segment Duitsland naar het canvas Definition en sleep de metrische waarde van de Unique Visitors erin:

   ![](assets/german-visitors.png)

1. Selecteer [!UICONTROL **sparen**] om berekende metrisch te bewaren.

1. Maak een ad-hocsegment in de berekende metrische bouwer genaamd &quot;Internationale Bezoekers&quot;, waarbij &quot;Landen&quot; niet gelijk is aan &quot;Duitsland&quot;.

   Sleep de dimensie van Landen in het canvas van de Definitie, uitgezochte [!UICONTROL **Duitsland**] als waarde, dan uitgezocht [!UICONTROL **gelijk niet**] als exploitant.

1. Sleep de metrische gegevens van de Unieke Bezoekers erin.

1. Selecteer [!UICONTROL **sparen**] om berekende metrisch te bewaren.

1. In Analysis Workspace sleept u het Dimension **[!UICONTROL Page]** naar een tabel voor vrije vorm en sleept u de twee nieuwe berekende meetgegevens naast elkaar naar de bovenkant:

   ![](assets/workspace-pages.png)


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Gesegmenteerde metriek ](https://video.tv.adobe.com/v/25409?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Percentage van totale metriek {#percent-total}

U kunt het voorbeeld boven een stap verder nemen door uw segment te vergelijken met een totale populatie. Hiertoe maakt u twee nieuwe meeteenheden: &quot;% van de totale Duitse bezoekers&quot; en &quot;% van de totale internationale bezoekers&quot;:

1. Verplaats het segment Duitse (of internationale) bezoekers naar het canvas.
1. Zet een ander Duits (of Internationaal) bezoekerssegment hieronder neer. Deze keer klikt u echter op het pictogram voor configuratie (versnelling) om het metrische type &quot;Totaal&quot; te selecteren. De notatie moet &#39;Percentage&#39; zijn. De exploitant zou &quot;gedeeld door&quot;moeten zijn. U eindigt omhoog met deze metrische definitie:

   ![](assets/cm_metric_total.png)

1. Pas deze metrisch op uw project toe:

   ![](assets/cm_percent_total.png)
