---
title: Hoogte
description: Het aantal hits in het bezoek.
feature: Dimensions
exl-id: 84c27e3f-4228-4455-95bf-0239928337b5
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 7%

---

# Hoogte

De &#39;hakdiepte&#39; [dimensie](overview.md) meldt hoe ver een bezoek aan een bepaalde hit is . Deze dimensie is handig als u wilt weten tot in welke mate bezoekers acties op uw site uitvoeren. Met de optie Pit-diepte worden alle typen resultaten geteld, inclusief paginaweergaven ([`t()`](/help/implement/vars/functions/t-method.md)) en links bijhouden ([`tl()`](/help/implement/vars/functions/tl-method.md)).

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

Items van het Dimension bevatten de tekenreeks `"Hit Depth"` gevolgd door een nummer dat het aantal bezoekers in het bezoek aangeeft. Het item Dimensie van `"Hit Depth 1"` staat voor de eerste hit van het bezoek, terwijl het item Dimensie `"Hit Depth 8"` staat voor de achtste treffer van het bezoek .

## Vergelijking met diepte bezoek

Bij een stippeldiepte worden alle typen treffers geteld, zoals de paginaweergave en de resultaten van het bijhouden van koppelingen. Alleen dieptealleen stappen voor treffers in de paginaweergave bezoeken _en_ de [Pagina](page.md) Dimensie-item is niet hetzelfde als de waarde op de vorige pagina. De diepte van het bezoek is ook een op bezoek-gebaseerde dimensie, die het betekent is de zelfde waarde voor alle treffers in het bezoek. In de volgende tabel wordt een voorbeeldoverzicht beschreven en wordt uitgelegd hoe u de diepte van een hit en een bezoek bekijkt:

| Paginareeks | Hoogte | Voegt u af naar de diepte van het bezoek? | Diepte bezoeken |
| --- | --- | --- | --- |
| Homepage | 1 | Ja | 4 |
| Productpagina | 2 | Ja | 4 |
| Homepage | 3 | Ja | 4 |
| Aangepaste koppeling klikken | 4 | Nee (aangepaste koppeling) | 4 |
| Aangepaste koppeling klikken | 5 | Nee (aangepaste koppeling) | 4 |
| Productpagina | 6 | Ja | 4 |
| Aangepaste koppeling klikken | 7 | Nee (aangepaste koppeling) | 4 |
| Productpagina | 8 | Nee (gelijk aan vorige pagina) | 4 |
