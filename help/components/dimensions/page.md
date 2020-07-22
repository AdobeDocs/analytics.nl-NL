---
title: Pagina
description: De naam van de pagina.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# Pagina

De dimensie &#39;Pagina&#39; geeft een overzicht van de namen van pagina&#39;s op uw site. Het is een van de meest gebruikte afmetingen in Adobe Analytics, omdat het inzicht biedt in welke pagina&#39;s op uw site het beste presteren.

Deze dimensie is verwant met de sectie [van de](site-section.md) Plaats en de afmetingen van de [Server](server.md) . De pagina is korrelig, de Server is het minst korrelig, en de sectie van de Plaats is tussen twee.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van het [`pageName` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de `pageName` variabele. Als de `pageName` variabele niet is gedefinieerd, wordt de URL van de pagina weer gebruikt.

## Dimensie-items

Dimensie-items bevatten de namen van pagina&#39;s op uw site. Uw organisatie bepaalt welke specifieke afmetingspunten u wilt gebruiken. Sommige organisaties gebruiken direct `document.title`, terwijl anderen een douane broodkruimel formuleren. Welke methode u ook gebruikt, zorg ervoor het verenigbaar is en dat u het in een document [van het](/help/implement/prepare/solution-design.md)oplossingsontwerp registreert.

>[!NOTE]
>
>In Rapporten &amp; Analytics gebruiken conversiemetriek lineaire toewijzing voor deze dimensie. Zo worden de inkomsten gesplitst tussen alle pagina&#39;s die tijdens een bezoek vóór een `purchase` gebeurtenis worden weergegeven. Analysis Workspace gebruikt standaard de laatste toewijzing, met de optie om een willekeurig toewijzingsmodel te gebruiken.
