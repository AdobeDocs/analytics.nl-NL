---
title: Pagina
description: De naam van de pagina.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# Pagina

De dimensie &#39;Pagina&#39; geeft een overzicht van de namen van pagina&#39;s op uw site. Het is een van de meest gebruikte afmetingen in Adobe Analytics, omdat het inzicht biedt in welke pagina&#39;s op uw site het beste presteren.

Deze dimensie is verwant met de sectie [van de](site-section.md) Plaats en de afmetingen van de [Server](server.md) . De pagina is korrelig, de Server is het minst korrelig, en de sectie van de Plaats is tussen twee.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van het [`pageName` vraagkoord](/help/implement/validate/query-parameters.md) in de vraag van de [mening van de Pagina terug (`t()`)](/help/implement/vars/functions/t-method.md). [De het volgen van de verbinding vraag (`tl()`)](/help/implement/vars/functions/tl-method.md) verwijdert altijd deze afmeting, zelfs als het `pageName` vraagkoord bestaat.

AppMeturement verzamelt deze gegevens met behulp van de [`pageName`](/help/implement/vars/page-vars/pagename.md) variabele. Als de `pageName` variabele niet is gedefinieerd, wordt de [`pageURL`](/help/implement/vars/page-vars/pageurl.md) variabele opnieuw gebruikt.

## Dimension-items

Dimension-items bevatten de namen van pagina&#39;s op uw site. Uw organisatie bepaalt welke specifieke afmetingspunten u wilt gebruiken. Sommige organisaties gebruiken direct `document.title`, terwijl anderen een douane broodkruimel formuleren. Welke methode u ook gebruikt, zorg ervoor het verenigbaar is en dat u het in een document [van het](/help/implement/prepare/solution-design.md)oplossingsontwerp registreert.

>[!NOTE]
>
>In Rapporten &amp; Analytics, gebruiken de omzettingsmetriek lineaire attributie voor deze afmeting. Zo worden de inkomsten gesplitst tussen alle pagina&#39;s die tijdens een bezoek vóór een `purchase` gebeurtenis worden weergegeven. Analysis Workspace gebruikt standaard de laatste toewijzing, met de optie om een willekeurig toewijzingsmodel te gebruiken.
