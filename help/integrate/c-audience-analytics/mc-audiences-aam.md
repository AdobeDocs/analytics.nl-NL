---
description: Adobe Audience Manager (Adobe Audience Manager) is een krachtig platform voor gegevensbeheer waarmee u unieke publieksprofielen kunt maken van de integratie van gegevens van de eerste partij, de tweede partij/partner en derden. Voor adverteerders helpen deze profielen de meest waardevolle segmenten te definiëren die over elk digitaal kanaal kunnen worden gebruikt.
solution: Experience Cloud
title: Overzicht van Audience Analytics
feature: Audience Analytics
exl-id: 1665a554-8a6f-4b20-99b7-bb3c2c4bf8cc
source-git-commit: c947de8eaa4e4dc3a0c10989ef6ae450cebc1f3e
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Overzicht van Audience Analytics

Adobe Audience Manager (Adobe Audience Manager) is een krachtig platform voor gegevensbeheer waarmee u unieke publieksprofielen kunt maken van de integratie van gegevens van de eerste partij, de tweede partij/partner en derden. Voor adverteerders helpen deze profielen de meest waardevolle segmenten te definiëren die over elk digitaal kanaal kunnen worden gebruikt.

Met de Audience Analytics-integratie kunt u gegevens over het Adobe Audience Manager-publiek, zoals demografische informatie (bijvoorbeeld geslacht of inkomensniveau), psychografische informatie (bijvoorbeeld interesses en hobby&#39;s), CRM-gegevens en impressiegegevens, in elke analyseworkflow opnemen.

>[!VIDEO](https://video.tv.adobe.com/v/25450/?quality=12)

## Belangrijkste voordelen {#benefits}

De integratie van het Audience Analytics biedt de volgende voordelen:

* Het is de eerste productievere integratie tussen een Data Management Platform (DMP) en een Analytics Engine op de markt.
* De segmenten worden gedeeld van Adobe Audience Manager aan Analytics in echt - tijd, om publieksontdekking, segmentatie, en optimalisering te informeren.
* Alle Adobe Audience Manager-segmenten worden standaard gedeeld en verrijken de klantprofielen volledig in Analytics.
* De beheerders van de oplossing kunnen de integratie door het gebruikersinterface toelaten, met minimale vereiste codeveranderingen.
* Alleen segmenten die zich houden aan besturingselementen voor het exporteren van Audience Manager-gegevens, worden gedeeld.

## Hoe Audience Analytics werkt {#works}

![](assets/mc-aud-dataflow.png)

1. Telkens wanneer een bezoeker naar uw digitale eigenschappen komt, worden de klappen verzameld en naar Analytics verzonden.
1. Met [server-kant door:sturen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md), wordt elke hit die door Analytics wordt ontvangen, automatisch in real-time naar Adobe Audience Manager verzonden.
1. Door de integratie van het Audience Analytics, voor elke klap, wordt het het publiekslidmaatschap van een bezoeker opgezocht in Adobe Audience Manager en een lijst van segment IDs is teruggekeerd aan Analytics voor verwerking in echt - tijd.

Omdat Adobe Audience Manager-segmenten op basis van zelfde hit worden ingevoegd, kunt u er zeker van zijn dat alle gegevens die in Adobe Audience Manager beschikbaar zijn over een bezoeker, niet worden overgeslagen en up-to-date zijn voor die hit. Dit is beter dan een insteekmodule voor AppMeasurementen, omdat deze segmenten met een insteekmodule alleen bij de volgende druk beschikbaar kunnen worden gemaakt (in plaats van de huidige druk).

Bovendien classificeren wij automatisch Adobe Audience Manager segment IDs aan hun vriendschappelijke namen voor u, zodat u niet alpha-numerieke IDs in de rapporten van de Analyse zult hoeven te bekijken.

## Vereisten {#prerequisites}

Zorg ervoor dat aan de volgende voorwaarden is voldaan:

* U bent een klant van zowel Audience Manager als Adobe Analytics.
* U bent beheerder van Audience Managers.
* U gebruikt identiteitsservice v1.5 of hoger.
* Adobe Audience Manager en Adobe Analytics rapporteren suites worden toegewezen aan dezelfde organisatie van Experiencen Cloud.
* U gebruikt [server-kant door:sturen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md) en de [De module Audience Management](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html) (geen DIL-code) - AppMeasurement 1.5 of hoger.

Deze voorwaarden worden beschreven in de [Workflow Audience Analytics](/help/integrate/c-audience-analytics/c-workflow/audiences-workflow.md).
