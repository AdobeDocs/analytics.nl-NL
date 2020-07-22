---
title: Server
description: De naam van de server.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Server

De dimensie &#39;Server&#39; geeft doorgaans de hostnaam van de site weer. Voor rapportreeksen die veelvoudige domeinen of subdomeinen combineren, is deze dimensie waardevol om te zien welke domeinen of subdomeinen het beste presteren.

Deze dimensie heeft betrekking op de afmetingen van de sectie [](page.md) Pagina [en](site-section.md) Site. De pagina is korrelig, de Server is het minst korrelig, en de sectie van de Plaats is tussen twee.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van het [`server` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de [`server`](/help/implement/vars/page-vars/server.md) variabele.

## Dimensie-items

Dimensie-items bevatten servers op uw site. Uw organisatie bepaalt welke specifieke afmetingspunten u wilt gebruiken. Sommige organisaties gebruiken `window.location.hostname`, terwijl andere een douanewaarde formuleren. Welke methode u ook gebruikt, zorg ervoor het verenigbaar is en dat u het in een document [van het](/help/implement/prepare/solution-design.md)oplossingsontwerp registreert.
