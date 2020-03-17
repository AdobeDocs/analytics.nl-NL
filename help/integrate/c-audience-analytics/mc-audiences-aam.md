---
description: Adobe Audience Manager (AAM) is een krachtig platform voor gegevensbeheer dat u helpt unieke publieksprofielen te maken van de integratie van gegevens van eerste partijen, tweede partijen/partners en van derden. Voor adverteerders helpen deze profielen de meest waardevolle segmenten te definiëren die over elk digitaal kanaal kunnen worden gebruikt.
solution: Experience Cloud
title: Overzicht van Audience Analytics
uuid: 86ef9391-dd6a-495f-a10e-e98bc069dde4
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Overzicht van Audience Analytics

Adobe Audience Manager (AAM) is een krachtig platform voor gegevensbeheer dat u helpt unieke publieksprofielen te maken van de integratie van gegevens van eerste partijen, tweede partijen/partners en van derden. Voor adverteerders helpen deze profielen de meest waardevolle segmenten te definiëren die over elk digitaal kanaal kunnen worden gebruikt.

Met de integratie van Audience Analytics op zijn plaats, kunt u AAM publieksgegevens zoals demografische informatie (b.v. geslacht of inkomensniveau), psychografische informatie (b.v. interesses en hobby&#39;s), CRM-gegevens, en imitatiegegevens in om het even welke analysewerkschema opnemen.

## Belangrijkste voordelen {#section_94816D17283349E0BA28521BE55BB868}

De integratie van Audience Analytics biedt de volgende belangrijke voordelen:

* Het is de eerste productievere integratie tussen een Data Management Platform (DMP) en een Analytics Engine op de markt.
* De segmenten worden gedeeld van AAM aan Analytics in echt - tijd, om publieksontdekking, segmentatie, en optimalisering te informeren.
* Alle segmenten AAM worden gedeeld door gebrek, volledig verrijkend klantenprofielen in Analytics.
* De beheerders van de oplossing kunnen de integratie door het gebruikersinterface toelaten, met minimale vereiste codeveranderingen.
* Alleen segmenten die zich houden aan besturingselementen voor gegevensexport van Audience Manager worden gedeeld.

## Hoe het werkt {#section_CECDF5A0FEC64264B206EFEF54F19EF2}

![](assets/mc-aud-dataflow.png)

1. Telkens wanneer een bezoeker naar uw digitale eigenschappen komt, worden de klappen verzameld en naar Analytics verzonden.
1. Met [server-kant door:sturen](/help/admin/admin/c-server-side-forwarding/ssf.md), wordt elke klap die Analytics ontvangt automatisch verzonden naar AAM in echt - tijd.
1. Door de integratie van Analytics van het Publiek, voor elke klap, wordt het het publiekslidmaatschap van een bezoeker opgezocht in AAM en een lijst van segment IDs is teruggekeerd aan Analytics voor verwerking in echt - tijd.

Omdat de segmenten AAM op zelfde-raakbasis worden opgenomen, kunt u zeker zijn dat om het even welke gegevens in AAM over een bezoeker beschikbaar zijn niet zullen worden gemist en bijgewerkt voor die klap zijn. Dit is beter dan een insteekmodule AppMeasurement, omdat een insteekmodule deze segmenten alleen bij de volgende druk beschikbaar kan maken (in plaats van de huidige hit).

Bovendien classificeren wij automatisch AAM segment IDs aan hun vriendschappelijke namen voor u, zodat u niet alpha-numerieke IDs in de rapporten van de Analyse zult hoeven te bekijken.

## Vereisten {#section_A345DC31F7D44EAE9DC1AB53E824C0CC}

Zorg ervoor dat aan de volgende voorwaarden is voldaan:

* U bent een klant van zowel Audience Manager als de Analytics van Adobe.
* U bent beheerder van Audience Manager.
* U gebruikt identiteitsservice v1.5 of hoger.
* AAM en Adobe Analytics-rapportreeksen zijn [toegewezen aan dezelfde Experience Cloud-organisatie](https://marketing.adobe.com/resources/help/en_US/mcloud/report-suite-mapping.html).
* U gebruikt [server-zijdoor:sturen](/help/admin/admin/c-server-side-forwarding/ssf.md) en hebt de module [van het Beheer van de](https://marketing.adobe.com/resources/help/en_US/aam/c_profiles_audiences.html) Publiek (geen code DIL) - AppMeasurement 1.5 of later uitgevoerd.

Deze voorwaarden worden beschreven in de Workflow [van de Analyse van de](/help/integrate/c-audience-analytics/c-workflow/audiences-workflow.md)Publiek.
