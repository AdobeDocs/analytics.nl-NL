---
description: Lijst met foutberichten in Adobe Analysis Workspace en de bijbehorende onderdelen
title: Algemene foutberichten in Analysis Workspace
feature: Workspace Basics
role: User, Admin
exl-id: e5c6f710-a205-48db-aeee-ee5b83c42795
source-git-commit: e7e03531454bd56ebe6152edc08765f42ebec728
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Algemene foutberichten

Er kunnen fouten optreden bij de interactie met Analysis Workspace die ook van invloed zijn op de prestaties. Hieronder ziet u de meest voorkomende fouttypen, de reden waarom deze voorkomen en optimalisaties die kunnen worden gemaakt.

| Foutbericht | Waarom gebeurt dit? | Optimalisatie |
| --- | --- | --- |
| [!UICONTROL The report suite is experiencing unusually heavy reporting. Please try again later.] | Uw organisatie probeert teveel gezamenlijke verzoeken tegen een specifieke rapportreeks in werking te stellen. Medewerkers aan deze fout zijn API verzoeken, geplande projecten, en gezamenlijke gebruikers die rapportageverzoeken indienen. | Verspreid uw verzoeken en programma&#39;s voor de rapportreeks gelijkmatiger door de dag. <p>De beheerders kunnen de [ Rapporterende Manager van de Activiteit gebruiken om verzoeken ](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md) te identificeren en te annuleren die rapporteringscapaciteit verbruiken. |
| [!UICONTROL The report suite is currently exceeding its reporting capacity. Please simplify the request or try again later.] | Uw organisatie probeert teveel gezamenlijke verzoeken tegen een specifieke rapportreeks in werking te stellen. Medewerkers aan deze fout zijn API verzoeken, geplande projecten, geplande rapporten, geplande alarm, en gezamenlijke gebruikers die het melden verzoeken. | Verspreid uw verzoeken en programma&#39;s voor de rapportreeks gelijkmatiger door de dag. |
| [!UICONTROL A system error has occurred. Please log a Customer Care request under Help > Submit Support Ticket and include your error code.] | Adobe heeft te maken met een probleem dat moet worden opgelost. | Stuur de foutcode naar de klantenservice. |
| [!UICONTROL An unexpected error has occurred; try refreshing your project again. If the problem persists, please submit this error ID to Adobe Customer Care for further diagnosis.] | Adobe heeft te maken met een probleem dat moet worden opgelost. | Vernieuw uw project en als het probleem zich blijft voordoen, dient u de foutcode in bij de klantenservice. |
| [!UICONTROL Error 500: Failed to load page] | De kwesties met uw lokaal netwerk, zoals bedrijf [ firewallmontages ](https://experienceleague.adobe.com/docs/analytics/technotes/ip-addresses.html), zijn een bijdragende factor aan deze fout. Bovendien kan Adobe een probleem ervaren dat moet worden opgelost. | Meld u na enkele minuten opnieuw aan. Als het probleem zich blijft voordoen, dient u de EIM-ID-code van de instantie in bij de klantenservice. |
| [!UICONTROL One of the segments or the search in this visualization contains a text search that returned too many results.] | Uw segmentcriteria of rapportfilter zijn te breed. | Verfijn uw zoektekstcriteria en probeer het verzoek opnieuw. |
| [!UICONTROL This dimension does not currently support non-default attribution models.] | Niet-standaardtoewijzing wordt niet ondersteund voor de dimensie die u gebruikt. | Vervang de afmeting in uw lijst met die met [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) compatibel is. |
| [!UICONTROL Your request failed as a result of too many columns or pre-configured rows.] | Uw tabel bevat te veel vrije-vormcellen (rij * kolommen). | Verwijder kolommen of rijen in de tabel of u kunt de tabel opsplitsen in afzonderlijke aanvragen. |
