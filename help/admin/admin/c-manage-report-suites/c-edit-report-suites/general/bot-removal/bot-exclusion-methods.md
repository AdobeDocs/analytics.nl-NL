---
title: Vergelijking van verschillende uitsluitingsmethoden
description: Hiermee kunt u verschillende methoden vergelijken om bots uit te sluiten.
exl-id: c54ba98a-b396-479e-bfe8-dc6211b26f61
role: Admin
feature: Bot Removal
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 6%

---

# Vergelijking van verschillende uitsluitingsmethoden

In de volgende tabel worden verschillende methoden getoond voor het uitsluiten van bots en de manier waarop deze met elkaar worden vergeleken.

| Methode | Bot-regels | Exclusief door IP Adres | Klantkenmerken | Segmentering | 3-partijscoring + segmentatie | De &#x200B; van de Vraag van de Server van de onderdrukking &#x200B; voor Bots bij Runtime | Aangepaste VISTA-regel voor database |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Beschrijving van de methode voor het uitsluiten van gegevens** | &#x200B; Uitsluiten op gebruiker-agent, IP adres, of IP adreswaaier wordt gebaseerd die | IP-adres | &#x200B; een markering in klantkenmerken die ECID als een beide identificeert | &#x200B; Criteria in een segment Analytics dat bekende bots identificeert op basis van beide gedrag | &#x200B; een derde partij, zoals [Perimeter X](https://www.perimeterx.com) of [Akamai Bot Manager](https://www.akamai.com/us/en/products/security/bot-manager.jsp) Wijst aan elke paginaweergave een score toe op de waarschijnlijkheid dat het een bot is. De score wordt verzonden naar Analytics en de segmenten kunnen worden gebruikt om gegevens uit te filtreren die op de score worden gebaseerd. | &#x200B; client-side logica zorgt ervoor dat de aanroep van de Analytics-server niet voor bots wordt uitgevoerd. | &#x200B; een VISTA regel zal verkeer van bots bewegen die aan bepaalde criteria aan een afzonderlijke rapportreeks voldoen. |
| **&#x200B; zijn de namen van de Bot beschikbaar voor rapportering?** | Ja | Nee | Nee | Nee | Nee | Nee | Ja |
| **&#x200B; Kan zien welke pagina&#39;s door bots worden bezocht?** | Ja | Nee | Nee | Nee | Ja | Nee | Ja |
| &#x200B;**Zorgt u voor kosten van serveroproepen voor bots?** | Ja | Ja | Ja | Ja | Ja | Nee | Ja |
| **Bot data available in data feeds?** | Nee | Nee | Ja | Ja | Ja | Nee | Ja |
| **Kan rapport over beide verkeer &#x200B; alsof zij daadwerkelijke servervraag zijn?** | Nee | Nee | Ja | Ja | Ja | Nee | Nee |
| **Kan gegevens met terugwerkende kracht uit een gegevensset verwijderen?** | Nee | Nee | &#x200B; Ja, zodra opgegeven id&#39;s zijn geïmplementeerd | Ja | Ja, zodra scores zijn geïmplementeerd | Nee | Nee |
| **Is er sprake van Uniques-limieten in criteria?** | Nee | Nee | Nee | Ja | Nee | Nee | Nee |
| **Is er &#x200B; sprake van extra kosten?** | Nee | Nee | &#x200B; mogelijk, afhankelijk van Analytics SKU | Nee | Ja | Nee | &#x200B; Ja - kosten voor de implementatie en handhaving van een VISTA-regel |
