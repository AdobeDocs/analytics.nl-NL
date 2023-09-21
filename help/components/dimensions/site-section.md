---
title: Sectie Site
description: De naam van de sitesectie.
feature: Dimensions
exl-id: 349bace0-4596-4b4c-bf29-6cd8866c246b
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Sectie Site

De sectie Site [dimensie](overview.md) geeft de namen van sitesecties op uw site weer. Voor grote sites is het handig om pagina&#39;s in secties te groeperen. Deze dimensie is handig om de bovenste of bovenste sitesecties te zien.

Deze dimensie houdt verband met de [Pagina](page.md) en [Server](server.md) afmetingen. De pagina is korrelig, de Server is het minst korrelig, en de sectie van de Plaats is tussen twee.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`ch` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeasurement verzamelt deze gegevens met de [`channel`](/help/implement/vars/page-vars/channel.md) variabele.

## Dimension-items

Items van Dimensionen bevatten de namen van sitesecties op uw site. Uw organisatie bepaalt welke specifieke afmetingspunten u wilt gebruiken. Welke methode u ook gebruikt, zorg ervoor het verenigbaar is en dat u het in een registreert [document ontwerp oplossing](/help/implement/prepare/solution-design.md).
