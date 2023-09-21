---
title: Server
description: De naam van de server.
feature: Dimensions
exl-id: c2454c0d-497e-46f8-8569-7d0517097cab
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# Server

De &#39;server&#39; [dimensie](overview.md) Hier wordt doorgaans de hostnaam van de site weergegeven. Voor rapportreeksen die veelvoudige domeinen of subdomeinen combineren, is deze dimensie waardevol om te zien welke domeinen of subdomeinen het beste presteren.

Deze dimensie houdt verband met de [Pagina](page.md) en [Sectie Site](site-section.md) afmetingen. De pagina is korrelig, de Server is het minst korrelig, en de sectie van de Plaats is tussen twee.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`server` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeasurement verzamelt deze gegevens met de [`server`](/help/implement/vars/page-vars/server.md) variabele.

## Dimension-items

Dimension-items bevatten servers op uw site. Uw organisatie bepaalt welke specifieke afmetingspunten u wilt gebruiken. Sommige organisaties gebruiken `window.location.hostname`, terwijl anderen aangepaste waarden formuleren. Welke methode u ook gebruikt, zorg ervoor het verenigbaar is en dat u het in een registreert [document ontwerp oplossing](/help/implement/prepare/solution-design.md).
