---
title: Vergelijking van verschillende uitsluitingsmethoden
description: Hiermee kunt u verschillende methoden vergelijken om bots uit te sluiten.
exl-id: c54ba98a-b396-479e-bfe8-dc6211b26f61
role: Admin
feature: Bot Removal
source-git-commit: 75c1585f88d9d3adcf66632c52cecf2a97fa2632
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 6%

---

# Vergelijking van verschillende uitsluitingsmethoden

In de volgende tabel worden verschillende methoden getoond voor het uitsluiten van bots en de manier waarop deze met elkaar worden vergeleken.

| Methode | Bot-regels | Exclusief door IP Adres | Klantkenmerken | Segmentatie | 3-partijscoring + segmentatie | De vraag van de Server voor Bots bij Runtime onderdrukken | Aangepaste VISTA-regel voor database |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Beschrijving van methode voor het uitsluiten van gegevens** | Exclusief gebaseerd op gebruiker-agent, IP adres, of IP adreswaaier | IP-adres | Een markering in klantkenmerken die ECID als een beide identificeert | Criteria in een segment Analytics dat bekende bots identificeert op basis van beide gedrag | Een derde partij zoals [ Perimeter X ](https://www.perimeterx.com) of [ Akamai Bot Manager ](https://www.akamai.com/us/en/products/security/bot-manager.jsp) wijst elke paginamening een score toe op hoe waarschijnlijk het een bot moet zijn. De score wordt verzonden naar Analytics en de segmenten kunnen worden gebruikt om gegevens uit te filtreren die op de score worden gebaseerd. | De client-side logica zorgt ervoor dat de aanroep van de Analytics-server niet meer wordt uitgevoerd voor bots. | Een VISTA regel zal verkeer van bots bewegen die aan bepaalde criteria aan een afzonderlijke rapportreeks voldoen. |
| **de namen van de Bot zijn beschikbaar voor het melden?** | Ja | Nee | Nee | Nee | Nee | Nee | Ja |
| **Kon zien welke pagina&#39;s door bots worden bezocht?** | Ja | Nee | Nee | Nee | Ja | Nee | Ja |
| **de kosten van de servervraag voor bots?** | Ja | Ja | Ja | Ja | Ja | Nee | Ja |
| **Bot gegevens beschikbaar in gegevensvoer?** | Nee | Nee | Ja | Nee | Ja | Nee | Ja |
| **Kon op beide verkeer rapporteren alsof zij daadwerkelijke servervraag zijn?** | Nee | Nee | Ja | Ja | Ja | Nee | Nee |
| **kan gegevens uit een gegevensreeks met terugwerkende kracht verwijderen?** | Nee | Nee | Ja, zodra gedeclareerde id&#39;s zijn geïmplementeerd | Ja | Ja, zodra scores zijn geïmplementeerd | Nee | Nee |
| **is onderworpen aan de grenzen van Uniques in criteria?** | Nee | Nee | Nee | Ja | Nee | Nee | Nee |
| **is onderworpen aan extra kosten?** | Nee | Nee | Mogelijk, afhankelijk van Analytics SKU | Nee | Ja | Nee | Ja - kosten voor de implementatie en handhaving van een VISTA-regel |
