---
description: Een basiscontainer maken voor gegevensverzameling in Adobe Analytics
title: Een rapportsuite maken
feature: Report Suite Settings
exl-id: 255ae051-d993-41a5-8cf3-819a54c17e34
source-git-commit: 9057cc83881a72fa039e9398ed3daaf4259ef2bf
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 6%

---

# Een rapportsuite maken

Een rapportenreeks is een silo van gegevens die Adobe Analytics gebruikt om rapporten te trekken. Een organisatie kan vele rapportreeksen hebben, elk die verschillende gegevensreeksen bevatten. Afzonderlijke rapportsuites waren in het verleden belangrijk, maar het hebben van één enkele rapportsuite is voordeliger geworden. De invoering van [virtuele rapportsuites](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=nl-NL#virtual-report-suites) en de verwerking van de rapporttijd staat beheerders toe om uw eigen ondergroepen van gegevens tot stand te brengen, die de flexibiliteit toestaan om zowel globale als plaats-specifieke gegevens te verkrijgen.

Dit artikel is bedoeld voor systeembeheerders of Adobe Analytics-beheerders die zich moeten voorbereiden op gegevensverzameling.

## Vereisten

[Adobe Analytics First Admin Guide](/help/admin/admin-console/first-admin-guide.md): Zorg ervoor dat een systeembeheerder u toegang tot Adobe Analytics via de Admin Console van de Experience Cloud heeft verleend.

## Een rapportsuite maken {#create-report-suite}

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Klik op **[!UICONTROL Create New]** > **[!UICONTROL Report Suite]**.
1. Selecteer een vooraf gedefinieerde sjabloon of een bestaande rapportsuite die u als een [template](/help/admin/admin/c-manage-report-suites/c-report-suite-templates/report-suite-templates.md).

   >[!NOTE]
   >
   >Alleen instellingen kunnen worden gekopieerd, niet de gegevens. Als de klantenservice de instellingen overschrijdt, moet u een schriftelijke bevestiging geven aan de disclaimer die door de klantenservice is verstrekt over de betrokken risico&#39;s. Zie [Instellingen die niet uit een bronrapportsuite zijn gekopieerd](/help/admin/admin/c-manage-report-suites/c-new-report-suite/settings-not-copied-from-rs.md) voor meer informatie .

1. Vul de velden in die worden beschreven in [Nieuwe rapportsuite](/help/admin/admin/c-manage-report-suites/c-new-report-suite/new-report-suite.md).
1. Klik op **[!UICONTROL Create Report Suite]**.

Een rapportsuite-id mag maximaal 40 bytes lang zijn. Een rapportsuite-vriendelijke naam heeft een maximumlengte van 255 bytes.

## Problemen oplossen

**Nadat u zich hebt aangemeld bij de Experience Cloud, wordt het pictogram Analytics grijs weergegeven.**

Dit betekent dat aan uw account niet de juiste machtigingen voor Analytics zijn verleend. Werk samen met een beheerder op systeemniveau in uw organisatie om ervoor te zorgen dat u tot een profiel behoort met de juiste machtigingen om toegang te krijgen tot Adobe Analytics.

## Volgende stappen

[Een Adobe Analytics-tageigenschap maken](/help/implement/launch/create-analytics-property.md): Maak een gebied voor het beheer van de implementatie van Analytics.
