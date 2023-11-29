---
title: Marketingkanalen analyseren
description: Leer hoe u de dimensies Marketingkanalen in Workspace gebruikt.
feature: Marketing Channels
exl-id: 7030e41a-4e92-45c7-9725-66a3ef019313
source-git-commit: 2eff7656741bdba3d5d7d1f33e9261b59f8e6083
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 1%

---

# Marketingkanalen analyseren

>[!NOTE]
>
>Om de doeltreffendheid van de Kanalen van de Marketing voor Attributie en Customer Journey Analytics te maximaliseren, hebben wij sommige gepubliceerd [herziene beste praktijken](/help/components/c-marketing-channels/mchannel-best-practices.md).
>
>Analysebeheerders kunnen marketingkanalen voor hun organisaties beheren, zoals beschreven in [Marketingkanalen beheren](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md).

U wilt waarschijnlijk weten welke van uw marketingkanalen het meest effectief is en met wie, zodat u uw inspanningen beter kunt richten en een beter rendement op uw marketingdollars kunt krijgen. In Adobe Analytics zijn de dimensies en maatstaven van de Kanalen van de Marketing in Workspace één van de hulpmiddelen die u kunnen helpen de invloed van verschillende kanalen op uw orden, opbrengst, enz. volgen. en geeft u nuttige kanaalinzichten. Hier zijn de afmetingen en de metriek u met betrekking tot de Kanalen van de Marketing kunt gebruiken:

![](assets/mc-dims.png)

| Dimension/metrisch | Definitie |
| --- | --- |
| Marketingkanaal | Dit is de geadviseerde dimensie van de Kanalen van de Marketing aan gebruik. Attributiemodellen kunnen hierop worden toegepast tijdens runtime. Deze dimensie gedraagt zich als laatste de dimensie van het Kanaal van de Aanraking, maar verschillend geëtiketteerd om verwarring te verhinderen wanneer het gebruiken van het met een verschillend attributiemodel. |
| Laatste aanraakkanaal | Verouderde dimensie, met het laatste aanraakattributiemodel vooraf toegepast en onveranderbaar. |
| Eerste aanraakkanaal | Verouderde dimensie, met het eerste aanraakattributiemodel vooraf toegepast en onveranderbaar. |
| Marketing Channel-instanties | Deze metrische meting meet het aantal tijden een marketing kanaal in een beeldverzoek, met inbegrip van standaardpaginameningen en douaneverbindingsvraag werd bepaald. Bevat geen aaneengesloten waarden. |
| Nieuwe contracten | Deze metrische waarde lijkt op Instanties, maar wordt alleen verhoogd wanneer first-touch marketingkanaal wordt gedefinieerd in een afbeeldingsaanvraag. |

## Basisanalyse

Deze lijst van Freeform toont de metriek Online Orders, Online Ontvangsten, en het Tarief van de Omzetting voor elk van de Kanalen van de Marketing:

![](assets/mc-viz1.png)

Hier ziet u de Online Orders en Online-inkomsten van elk marketingkanaal in een Donut-overzicht:

![](assets/mc-viz2.png)

Dit diagram van Lijn toont tendensen in Online Orden voor diverse kanalen in tijd:

![](assets/mc-viz3.png)

## Geavanceerde analyse

De Details van de Kanalen van de marketing duiken dieper in elk kanaal om u specifieke campagnes, plaatsen, enz. te tonen. U kunt elk marketingkanaal onderverdelen in details:

![](assets/mc-viz4.png)

## Kenmerkingsmodellen toepassen

U kunt [Attributie](/help/analyze/analysis-workspace/attribution/overview.md) verschillende toerekeningsmodellen tegelijk toe te passen:

![](assets/mc-viz5.png)

U ziet hoe dezelfde metrische waarde (Online bestellingen) verschillende resultaten genereert wanneer u verschillende attributiemodellen toepast.

## Analyse van intertab-marketing

Met het verouderde First-Touch Channel en Last-Touch Channel kunt u een handige weergave krijgen in kanaalinteracties:

![](assets/mc-viz6.png)

Meer informatie over de marketinganalyse op verschillende tabbladen vindt u in deze video: [Analyse op verschillende tabbladen gebruiken om de basismarketingkenmerken in Analysis Workspace te verkennen](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/attribution-iq/using-cross-tab-analysis-to-explore-basic-marketing-attribution-in-analysis-workspace.html).
