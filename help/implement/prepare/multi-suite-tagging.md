---
description: Leer hoe u tagging met meerdere suite implementeert om een verzoek om een image naar meerdere rapportsuite te verzenden.
title: Labelen met meerdere suite's implementeren
feature: Implementation Basics
exl-id: c7fb0478-97e1-4367-8742-e7539f6f82e7
role: Admin, Developer, Leader
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Labelen met meerdere suite&#39;s implementeren

[ multi-suite het etiketteren ](/help/admin/tools/manage-rs/rollup-report-suite.md) staat u toe om beeldverzoeken niet alleen naar een globale rapportreeks maar ook naar individuele de reeksen van het kindrapport te verzenden zodat u subsets van de globale gegevens van de rapportreeks van uw bedrijf aan verschillende eind kunt verstrekken - gebruikers.

Om multi-suite het etiketteren uit te voeren, moet u identiteitskaart van de Reeks van het Rapport (RSID) voor de globale rapportreeks en ook RSIDs voor de toepasselijke reeksen van het kindrapport in de volgende code voor uw webpagina&#39;s en apps omvatten.

* Voor de markeringsimplementaties van Adobe Experience Platform, specificeer elk van de rapportreeksen voor de [[!DNL Analytics]  uitbreiding ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=nl-NL).

* Voor erfenis JavaScript en mobiele implementaties van SDK, scheidt RSIDs met komma&#39;s en geen ruimten (`rsid1,rsid2,rsid3` etc.).

* Voor andere implementatietypen, gebruik de vereiste syntaxis om van veelvoudige RSIDs een lijst te maken.

>[!TIP]
>
> De beste praktijken moeten de globale rapportreeks of rapportreeks ID eerst een lijst maken.

Het etiketteren van meerdere reeksen komt veelvoudige servervraag voor elke beeldverzoek in werking: een primaire vraag aan de globale rapportreeks en een secundaire vraag voor elke reeks van het kindrapport.

>[!NOTE]
>
> [ Virtuele rapportsuites ](/help/components/vrs/vrs-about.md), die u ook toestaan om ondergroepen van de gegevens van de het rapportsuite van uw bedrijf globale aan verschillende eind te verstrekken - gebruikers, geen secundaire servervraag maken.

## Moet ik multi-suite tagging of virtuele rapportsuites implementeren?

Het gebruik van virtuele rapportsuites in plaats van multi-suite het etiketteren is vaak een beste praktijk, maar uw bedrijfsbehoeften bepalen de beste benadering van de rapportsuite voor uw organisatie.

Om te begrijpen als de virtuele rapportsuites uw beste benadering zijn, zie &quot;[ Virtuele rapportsuites en multi-suite het etiketteren overwegingen ](/help/components/vrs/vrs-considerations.md).&quot; Zie ook &quot;[ Virtuele rapportreeksen vs., multi-suite het etiketteren ](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78)&quot;voor een vergelijking van multi-suite het etiketteren en de virtuele functionaliteit van de rapportreeks.
