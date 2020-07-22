---
title: Hoogte
description: Het aantal hits in het bezoek.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 7%

---


# Hoogte

De dimensie &#39;De diepte van de Kit&#39; meldt hoe ver een bezoek aan een bepaalde hit is. Deze dimensie is handig als u wilt weten tot in welke mate bezoekers acties op uw site uitvoeren. Bij de bitdiepte worden alle typen resultaten geteld, inclusief paginaweergaven ([`t()`](/help/implement/vars/functions/t-method.md))en treffers voor het bijhouden van koppelingen ([`tl()`](/help/implement/vars/functions/tl-method.md)).

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimensie-items

Items voor de dimensie bevatten de tekenreeks `"Hit Depth"` gevolgd door een getal dat het aantal hits in het bezoek vertegenwoordigt. Het item Dimensie van `"Hit Depth 1"` staat voor de eerste hit van het bezoek, terwijl het item Dimensie de achtste hit van het bezoek `"Hit Depth 8"` vertegenwoordigt.

## Vergelijking met diepte bezoek

Bij een stippeldiepte worden alle typen treffers geteld, zoals de paginaweergave en de resultaten van het bijhouden van koppelingen. Alleen diepte zoeken in stappen voor treffers in de paginaweergave _en het_ item voor de [pagina](page.md) -dimensie is niet hetzelfde als de waarde op de vorige pagina. De diepte van het bezoek is ook een op bezoek-gebaseerde dimensie, die het betekent is de zelfde waarde voor alle treffers in het bezoek. In de volgende tabel wordt een voorbeeldoverzicht beschreven en wordt uitgelegd hoe u de diepte van een hit en een bezoek bekijkt:

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
