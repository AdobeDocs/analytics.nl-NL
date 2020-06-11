---
title: Pagina
description: De naam van de pagina.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---


# Pagina

De dimensie &#39;Pagina&#39; geeft een overzicht van de namen van pagina&#39;s op uw site. Het is een van de meest gebruikte afmetingen in Adobe Analytics, omdat het inzicht biedt in welke pagina&#39;s op uw site het beste presteren.

Deze dimensie is verwant met de sectie [van de](site-section.md) Plaats en de afmetingen van de [Server](server.md) . De pagina is korrelig, de Server is het minst korrelig, en de sectie van de Plaats is tussen twee.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van het [`pageName` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de `pageName` variabele. Als de `pageName` variabele niet is gedefinieerd, wordt de URL van de pagina weer gebruikt.

## Dimensiewaarden

Tot de waarden voor dimensies behoren de namen van pagina&#39;s op uw site. Uw organisatie bepaalt welke specifieke afmetingswaarden u wilt gebruiken. Sommige organisaties gebruiken direct `document.title`, terwijl anderen een douane broodkruimel formuleren. Welke methode u ook gebruikt, zorg ervoor het verenigbaar is en dat u het in een document [van het](/help/implement/prepare/solution-design.md)oplossingsontwerp registreert.

>[!NOTE] In Rapporten &amp; Analytics, gebruiken de omzettingsmetriek lineaire attributie voor deze afmeting. Zo worden de inkomsten gesplitst tussen alle pagina&#39;s die tijdens een bezoek vóór een `purchase` gebeurtenis worden weergegeven. De Werkruimte van de analyse gebruikt laatste attributie door gebrek, met de optie om het even welk attributiemodel te gebruiken.
