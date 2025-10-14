---
description: Een basiscontainer maken voor gegevensverzameling in Adobe Analytics
title: Een rapportsuite maken
feature: Report Suite Settings
exl-id: 255ae051-d993-41a5-8cf3-819a54c17e34
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 2%

---

# Een rapportsuite maken

Een rapportenreeks is een silo van gegevens die Adobe Analytics gebruikt om rapporten te trekken. Een organisatie kan vele rapportreeksen hebben, elk die verschillende gegevensreeksen bevatten. Afzonderlijke rapportsuites waren in het verleden belangrijk, maar het hebben van één enkele rapportsuite is voordeliger geworden. De introductie van [&#x200B; virtuele rapportsuites &#x200B;](/help/components/vrs/vrs-about.md#virtual-report-suites) en de verwerking van de rapporttijd staat beheerders toe om uw eigen ondergroepen van gegevens tot stand te brengen, die de flexibiliteit toestaan om zowel globale als plaats-specifieke gegevens te verkrijgen.

Dit artikel is bedoeld voor systeembeheerders of Adobe Analytics-beheerders die zich moeten voorbereiden op gegevensverzameling.

## Vereisten

[&#x200B; Adobe Analytics Eerste Gids Admin &#x200B;](/help/admin/admin-console/first-admin-guide.md): Zorg ervoor dat een systeem-vlakke beheerder u toegang tot Adobe Analytics via Experience Cloud Admin Console heeft verleend.

## Een rapportsuite maken {#create-report-suite}

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Klik op **[!UICONTROL Add Report Suite]**.
1. Selecteer of een vooraf bepaald malplaatje of een bestaande rapportreeks om als a [&#x200B; malplaatje &#x200B;](/help/admin/tools/manage-rs/rs-templates/report-suite-templates.md) te gebruiken.

   >[!NOTE]
   >
   >Alleen instellingen kunnen worden gekopieerd, niet de gegevens. Als de klantenservice de instellingen overschrijdt, moet u een schriftelijke bevestiging geven aan de disclaimer die door de klantenservice is verstrekt over de betrokken risico&#39;s. Zie [&#x200B; Montages niet die van een bronrapportreeks &#x200B;](/help/admin/tools/manage-rs/new-rs/settings-not-copied-from-rs.md) voor meer informatie worden gekopieerd.

1. Vul de gebieden in die in [&#x200B; worden beschreven Nieuwe Reeks van het Rapport &#x200B;](/help/admin/tools/manage-rs/new-rs/new-report-suite.md).
1. Klik op **[!UICONTROL Create Report Suite]**.

Een rapportsuite-id mag maximaal 40 bytes lang zijn. Een rapportsuite-vriendelijke naam heeft een maximumlengte van 255 bytes.

## Problemen oplossen

**Na het aanmelden bij Experience Cloud, wordt het pictogram Analytics grijs weergegeven.**

Dit betekent dat aan uw account niet de juiste machtigingen voor Analytics zijn verleend. Werk samen met een beheerder op systeemniveau in uw organisatie om ervoor te zorgen dat u tot een profiel behoort met de juiste machtigingen om toegang te krijgen tot Adobe Analytics.

## Volgende stappen

[&#x200B; creeer een de markeringsbezit van Adobe Analytics &#x200B;](/help/implement/launch/create-analytics-property.md): Creeer een gebied om uw implementatie van Analytics te beheren.
