---
description: Lijst met foutberichten in Adobe Analysis Workspace en de bijbehorende componenten
title: Algemene foutberichten in Analysis Workspace
translation-type: tm+mt
source-git-commit: 1df7eb2b8734a7c260f843494c414a927638ebb4
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# Algemene foutberichten

Er kunnen fouten optreden bij de interactie met Analysis Workspace die ook van invloed zijn op de prestaties. Hieronder ziet u de meest voorkomende fouttypen, de reden waarom deze voorkomen en optimalisaties die kunnen worden gemaakt.

| Foutbericht | Waarom gebeurt dit? | Optimalisatie |
| --- | --- | --- |
| Er is een systeemfout opgetreden. Meld een verzoek voor de klantenservice aan onder Help > Ondersteuningstabel verzenden en voeg uw foutcode toe. | Adobe heeft een probleem dat moet worden opgelost. | Stuur de foutcode naar de klantenservice. |
| Fout 500: Kan pagina niet laden | De kwesties met uw lokaal netwerk, zoals een [firewallmontages](https://docs.adobe.com/content/help/en/analytics/technotes/ip-addresses.html)van het bedrijf, zijn een bijdragende factor aan deze fout. Bovendien kan Adobe een probleem ervaren dat moet worden opgelost. | Meld u na enkele minuten opnieuw aan. Als het probleem zich blijft voordoen, dient u de EIM-ID-code van de instantie in bij de klantenservice. |
| Een van de segmenten of de zoekopdracht in deze visualisatie bevat een tekstzoekopdracht die te veel resultaten heeft opgeleverd. | Uw segmentcriteria of rapportfilter zijn te breed. | Verfijn uw zoektekstcriteria en probeer het verzoek opnieuw. |
| De rapportenreeks ervaart ongebruikelijk zware rapportering. Probeer het later opnieuw. | Uw organisatie probeert teveel gezamenlijke verzoeken tegen een specifieke rapportreeks in werking te stellen. Medewerkers aan deze fout zijn API verzoeken, geplande projecten, geplande rapporten, geplande alarm, en gezamenlijke gebruikers die het melden verzoeken. | Verspreid uw verzoeken en programma&#39;s voor de rapportreeks gelijkmatiger door de dag. |
| Het verzoek is te ingewikkeld. | Uw rapportageaanvraag is te groot en kan niet worden uitgevoerd. Medewerkers aan deze fout zijn onderbrekingen wegens de grootte van het verzoek, teveel overeenkomende punten in een segment of een zoekfilter, teveel inbegrepen metriek, incompatibele afmeting en metrische combinaties, enz. | Vereenvoudig uw verzoek door sommige kolommen of rijen in uw lijst te verwijderen, of denk na het splitsen van de lijst in afzonderlijke verzoeken. |
| Deze dimensie ondersteunt momenteel geen niet-standaard attributiemodellen. | Niet-standaardtoewijzing wordt niet ondersteund voor de dimensie die u gebruikt. | Vervang de dimensie in de tabel door een dimensie die compatibel is met [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md). |
| Uw verzoek is mislukt als gevolg van te veel kolommen of vooraf geconfigureerde rijen. | Uw tabel bevat te veel vrije-vormcellen (rij * kolommen). | Verwijder kolommen of rijen in de tabel of u kunt de tabel opsplitsen in afzonderlijke aanvragen. |
