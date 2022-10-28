---
description: Lijst met foutberichten in Adobe Analysis Workspace en de bijbehorende componenten
title: Algemene foutberichten in Analysis Workspace
feature: Workspace Basics
role: User, Admin
exl-id: e5c6f710-a205-48db-aeee-ee5b83c42795
source-git-commit: 25eccb2b9fe3827e62b0ae98d9bebf7a97b239f5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Algemene foutberichten

Er kunnen fouten optreden bij de interactie met Analysis Workspace die ook van invloed zijn op de prestaties. Hieronder ziet u de meest voorkomende fouttypen, de reden waarom deze voorkomen en optimalisaties die kunnen worden gemaakt.

| Foutbericht | Waarom gebeurt dit? | Optimalisatie |
| --- | --- | --- |
| [!UICONTROL A system error has occurred. Please log a Customer Care request under Help > Submit Support Ticket and include your error code.] | Adobe heeft een probleem dat moet worden opgelost. | Stuur de foutcode naar de klantenservice. |
| [!UICONTROL An unexpected error has occurred; try refreshing your project again. If the problem persists, please submit this error ID to Adobe Customer Care for further diagnosis.] | Adobe heeft een probleem dat moet worden opgelost. | Vernieuw uw project en als het probleem zich blijft voordoen, dient u de foutcode in bij de klantenservice. |
| [!UICONTROL Error 500: Failed to load page] | De kwesties met uw lokaal netwerk, zoals bedrijf [firewallinstellingen](https://experienceleague.adobe.com/docs/analytics/technotes/ip-addresses.html), een factor die aan deze fout bijdraagt. Bovendien kan Adobe een probleem ervaren dat moet worden opgelost. | Meld u na enkele minuten opnieuw aan. Als het probleem zich blijft voordoen, dient u de EIM-ID-code van de instantie in bij de klantenservice. |
| [!UICONTROL One of the segments or the search in this visualization contains a text search that returned too many results.] | Uw segmentcriteria of rapportfilter zijn te breed. | Verfijn uw zoektekstcriteria en probeer het verzoek opnieuw. |
| [!UICONTROL The report suite is experiencing unusually heavy reporting. Please try again later.] | Uw organisatie probeert teveel gezamenlijke verzoeken tegen een specifieke rapportreeks in werking te stellen. Medewerkers aan deze fout zijn API verzoeken, geplande projecten, geplande rapporten, geplande alarm, en gezamenlijke gebruikers die het melden verzoeken. | Verspreid uw verzoeken en programma&#39;s voor de rapportreeks gelijkmatiger door de dag. |
| [!UICONTROL The request is too complex.] | Uw rapportageaanvraag is te groot en kan niet worden uitgevoerd. Medewerkers aan deze fout zijn onderbrekingen wegens de grootte van het verzoek, teveel overeenkomende punten in een segment of een zoekfilter, teveel inbegrepen metriek, incompatibele afmeting en metrische combinaties, enz. | Vereenvoudig uw verzoek door sommige kolommen of rijen in uw lijst te verwijderen, of denk na het splitsen van de lijst in afzonderlijke verzoeken. |
| [!UICONTROL This dimension does not currently support non-default attribution models.] | Niet-standaardtoewijzing wordt niet ondersteund voor de dimensie die u gebruikt. | Vervang de dimensie in uw tabel door een dimensie die compatibel is met [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md). |
| [!UICONTROL Your request failed as a result of too many columns or pre-configured rows.] | Uw tabel bevat te veel vrije-vormcellen (rij * kolommen). | Verwijder kolommen of rijen in de tabel of u kunt de tabel opsplitsen in afzonderlijke aanvragen. |
