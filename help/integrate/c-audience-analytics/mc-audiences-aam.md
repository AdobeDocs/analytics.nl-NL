---
description: Adobe Audience Manager (Adobe Audience Manager) is een krachtig platform voor gegevensbeheer waarmee u unieke publieksprofielen kunt maken van de integratie van gegevens van de eerste partij, de tweede partij/partner en derden. Voor adverteerders helpen deze profielen de meest waardevolle segmenten te definiëren die over elk digitaal kanaal kunnen worden gebruikt.
solution: Experience Cloud
title: Audience Analytics-overzicht
feature: Audience Analytics
exl-id: 1665a554-8a6f-4b20-99b7-bb3c2c4bf8cc
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Audience Analytics-overzicht

Adobe Audience Manager (Adobe Audience Manager) is een krachtig platform voor gegevensbeheer waarmee u unieke publieksprofielen kunt maken van de integratie van gegevens van de eerste partij, de tweede partij/partner en derden. Voor adverteerders helpen deze profielen de meest waardevolle segmenten te definiëren die over elk digitaal kanaal kunnen worden gebruikt.

Met de Audience Analytics-integratie kunt u gegevens over het Adobe Audience Manager-publiek, zoals demografische informatie (bv. geslacht of inkomensniveau), psychografische informatie (bv. interesses en hobby&#39;s), CRM-gegevens en impliciete gegevens in een analyseworkflow opnemen.


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; Audience Analytics &#x200B;](https://video.tv.adobe.com/v/25450?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Belangrijkste voordelen {#benefits}

De Audience Analytics-integratie biedt de volgende belangrijke voordelen:

* Het is de eerste productievere integratie tussen een Data Management Platform (DMP) en een Analytics Engine op de markt.
* De segmenten worden gedeeld van Adobe Audience Manager aan Analytics in echt - tijd, om publieksontdekking, segmentatie, en optimalisering te informeren.
* Alle Adobe Audience Manager-segmenten worden standaard gedeeld en verrijken de klantprofielen volledig in Analytics.
* De beheerders van de oplossing kunnen de integratie door het gebruikersinterface toelaten, met minimale vereiste codeveranderingen.
* Alleen segmenten die voldoen aan Audience Manager-besturingselementen voor gegevensexport worden gedeeld.

## Hoe Audience Analytics werkt {#works}

![](assets/mc-aud-dataflow.png)

1. Telkens wanneer een bezoeker naar uw digitale eigenschappen komt, worden de klappen verzameld en naar Analytics verzonden.
1. Met [&#x200B; server-kant door:sturen &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md), elke klap die Analytics ontvangt wordt automatisch verzonden naar Adobe Audience Manager in real time.
1. Via de Audience Analytics-integratie wordt voor elke hit het lidmaatschap van een bezoeker opgezocht in Adobe Audience Manager en wordt een lijst met segment-id&#39;s geretourneerd aan Analytics voor verwerking in real-time.

Omdat Adobe Audience Manager-segmenten op basis van zelfde hit worden ingevoegd, kunt u er zeker van zijn dat alle gegevens die in Adobe Audience Manager beschikbaar zijn over een bezoeker, niet worden overgeslagen en up-to-date zijn voor die hit. Dit is beter dan een AppMeasurement-plug-in, omdat deze segmenten met een plug-in alleen bij de volgende hit beschikbaar kunnen worden gemaakt (in plaats van de huidige hit).

Bovendien classificeren wij automatisch Adobe Audience Manager segment IDs aan hun vriendschappelijke namen voor u, zodat u niet alpha-numerieke IDs in de rapporten van de Analyse zult hoeven te bekijken.

## Vereisten {#prerequisites}

Zorg ervoor dat aan de volgende voorwaarden is voldaan:

* U bent een klant van zowel Audience Manager als Adobe Analytics.
* U bent een Audience Manager-beheerder.
* U gebruikt identiteitsservice v1.5 of hoger.
* Adobe Audience Manager en Adobe Analytics rapporteren suites worden toegewezen aan dezelfde Experience Cloud-organisatie.
* U gebruikt [&#x200B; server-kant het door:sturen &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md) en hebt de [&#x200B; module van het Beheer van de Publiek &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html?lang=nl-NL) (geen code van DIL) - AppMeasurement 1.5 of later uitgevoerd.

Deze eerste vereisten worden beschreven in het [&#x200B; Werkschema van Audience Analytics &#x200B;](/help/integrate/c-audience-analytics/c-workflow/audiences-workflow.md).
