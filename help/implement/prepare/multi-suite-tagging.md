---
description: Leer hoe u tagging met meerdere suite implementeert om een verzoek om een image naar meerdere rapportsuite te verzenden.
title: Tags implementeren met meerdere suite
exl-id: null
source-git-commit: 81da9ff9b00a69c49c028fc7f006c161d8ff21d4
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---


# Tags implementeren met meerdere suite

[Met ](/help/admin/c-manage-report-suites/rollup-report-suite.md) gelabelde multisuite kunt u verzoeken om images niet alleen naar een algemene rapportsuite verzenden, maar ook naar afzonderlijke onderdelen van het rapport, zodat u subsets van de algemene rapportsuite van uw bedrijf aan verschillende eindgebruikers kunt leveren.

Om multi-suite het etiketteren uit te voeren, moet u identiteitskaart van de Reeks van het Rapport (RSID) voor de globale rapportreeks en ook RSIDs voor de toepasselijke reeksen van het kindrapport in de volgende code voor uw webpagina&#39;s en apps omvatten.

* Voor Adobe Experience Platform Launch-implementaties geeft u elk van de rapportsuites voor de [[!DNL Analytics] extension](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/analytics-extension/overview.html) op.

* Voor verouderde implementaties van JavaScript en mobiele SDK, scheidt RSIDs met komma&#39;s en geen ruimten (`rsid1,rsid2,rsid3` etc.).

* Voor andere implementatietypen, gebruik de vereiste syntaxis om van veelvoudige RSIDs een lijst te maken.

>[!TIP]
>
> De beste praktijken moeten de globale rapportreeks of rapportreeks ID eerst een lijst maken.

Tags voor meerdere suite leiden tot meerdere serveraanroepen voor elke aanvraag voor een image: een primaire vraag aan de globale rapportreeks en een secundaire vraag voor elke reeks van het kindrapport.

>[!NOTE]
>
> [De virtuele rapportsuites](/help/components/vrs/vrs-about.md), die u ook toestaan om ondergroepen van de globale gegevens van de rapportsuite van uw bedrijf aan verschillende eind te verstrekken - gebruikers, doen geen secundaire servervraag.

## Moet ik multi-suite tagging of virtuele rapportsuites implementeren?

Het gebruik van virtuele rapportsuites in plaats van multi-suite het etiketteren is vaak een beste praktijk, maar uw bedrijfsbehoeften bepalen de beste benadering van de rapportsuite voor uw organisatie.

Om te begrijpen of zijn de virtuele rapportsuites uw beste benadering, zie &quot;[Virtuele rapportsuites en multi-suite het etiketteren overwegingen](/help/components/vrs/vrs-considerations.md).&quot; Zie ook &quot;[Virtual Report Suites vs. Multisuite Tagging](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78)&quot; voor een vergelijking van de tagging met meerdere suite en de functionaliteit van de virtuele rapportsuite.
