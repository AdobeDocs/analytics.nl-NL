---
description: Leer hoe u tagging met meerdere suite implementeert om een verzoek om een image naar meerdere rapportsuite te verzenden.
title: Tags implementeren met meerdere suite
feature: Implementation Basics
exl-id: c7fb0478-97e1-4367-8742-e7539f6f82e7
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---

# Tags implementeren met meerdere suite

[Tags toevoegen met meerdere suite](/help/admin/c-manage-report-suites/rollup-report-suite.md) staat u toe om beeldverzoeken niet alleen naar een globale rapportreeks maar ook naar individuele de reeksen van het kindrapport te verzenden zodat u ondergroepen van de globale gegevens van de rapportreeks van uw bedrijf aan verschillende eind kunt verstrekken - gebruikers.

Om multi-suite het etiketteren uit te voeren, moet u identiteitskaart van de Reeks van het Rapport (RSID) voor de globale rapportreeks en ook RSIDs voor de toepasselijke reeksen van het kindrapport in de volgende code voor uw webpagina&#39;s en apps omvatten.

* Geef voor Adobe Experience Platform-tagimplementaties elke rapportsuite op voor de [[!DNL Analytics] extension](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html).

* Voor verouderde implementatie van JavaScript en mobiele SDK, scheidt RSIDs met komma&#39;s en geen ruimten (`rsid1,rsid2,rsid3` enzovoort).

* Voor andere implementatietypen, gebruik de vereiste syntaxis om van veelvoudige RSIDs een lijst te maken.

>[!TIP]
>
> De beste praktijken moeten de globale rapportreeks of rapportreeks ID eerst een lijst maken.

Tags voor meerdere suite leiden tot meerdere serveraanroepen voor elke aanvraag voor een image: een primaire vraag aan de globale rapportreeks en een secundaire vraag voor elke reeks van het kindrapport.

>[!NOTE]
>
> [Virtuele rapportsuites](/help/components/vrs/vrs-about.md), die u ook toestaan om ondergroepen van de gegevens van de het rapportreeks van uw bedrijf globale aan verschillende eind te verstrekken - gebruikers, geen secundaire servervraag doen.

## Moet ik multi-suite tagging of virtuele rapportsuites implementeren?

Het gebruik van virtuele rapportsuites in plaats van multi-suite het etiketteren is vaak een beste praktijk, maar uw bedrijfsbehoeften bepalen de beste benadering van de rapportsuite voor uw organisatie.

Om te begrijpen of zijn de virtuele rapportsuites uw beste benadering, zie &quot;[Virtuele rapportreeksen en tagging met meerdere suite-overwegingen](/help/components/vrs/vrs-considerations.md).&quot; Zie ook &quot;[Virtuele rapportsuite versus meerdere suite-tags](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78)&quot; voor een vergelijking van de multi-suite-tagging en de functionaliteit van de virtuele rapportsuite.
