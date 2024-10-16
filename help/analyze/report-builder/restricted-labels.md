---
title: Wat zijn beperkte labels in Report Builder?
description: Beschrijft beperkte etiketten in Report Builder
role: User
feature: Report Builder
type: Documentation
solution: Analytics
source-git-commit: eedabc6295f9b918e1e00b93993680e676c216c3
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Beperkte labels in Report Builder

Over het algemeen worden aan gegevensbeheer gerelateerde instellingen in Adobe Analytics overgenomen van Adobe Experience Platform. Dankzij de integratie tussen Adobe Analytics en Adobe Experience Platform Data Governance kunnen gevoelige gegevens van Adobe Analytics worden geëtiketteerd en kan het privacybeleid worden gehandhaafd.

De etiketten en het beleid van de privacy die op datasets werden gecreeerd die door Experience Platform worden verbruikt kunnen in de het rapportwerkschema van Adobe Analytics worden rond gekomen. Deze labels stoppen of waarschuwen gebruikers die metriek en/of afmetingen van gevoelige velden maken. Voor informatie over datasets, zie [ Overzicht van Datasets ](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html)

Wanneer gegevens uit Adobe Analytics worden geëxporteerd (via rapportage, export, API, enz.), worden bovendien waarschuwingen of labels toegevoegd om gebruikers te laten weten dat een rapport gevoelige informatie bevat die op een specifieke manier moet worden behandeld.

Dankzij deze integratie kunt u de compatibiliteit eenvoudiger beheren. Gegevensstewards in uw organisatie kunnen beleid plaatsen om gebruik te beperken. Dit betekent dat uw Adobe Analytics-gebruikers gegevens betrouwbaarder kunnen gebruiken, in de wetenschap dat deze in overeenstemming zijn met het beleid dat wordt gedefinieerd door data stewards.

Voor meer informatie, zie [ Adobe Analytics en de Governance van Gegevens ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-privacy/privacy-overview.html)

## Beperkte gegevens weergeven in Report Builder

In Adobe Analytics worden twee door de Adobe gedefinieerde beleidsregels weergegeven die van invloed zijn op rapportage, downloaden en delen:

* Beleid voor analyse afdwingen
* Downloadbeleid afdwingen

Componenten die door dit beleid worden beïnvloed, worden grijs weergegeven. Wanneer u over een component beweegt die een toegepast beleid heeft, wordt een nota getoond om op het volgende te wijzen: **het Beleid is toegepast op dit gebied dat gebruik van deze gegevens verhindert.** voor meer informatie zie [ Etiketten en beleid ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-governance.html).

![ de beleidsnota die op het verboden gebruik van gegevens wijst.](assets/rb-restricted-label.png)

## Rapporten met beperkte gegevens bijwerken

In gevallen waar een gebruiker een rapport van de Report Builder met gegevenselementen creeerde die later worden beperkt, wanneer het rapport wordt verfrist, wordt een foutenmelding getoond.

![ het foutenbericht wordt getoond nadat de gegevenselementen later worden beperkt.](assets/error-restricted-data.png)
