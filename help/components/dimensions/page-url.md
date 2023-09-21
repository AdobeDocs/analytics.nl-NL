---
title: Pagina-URL
description: De URL van de pagina.
feature: Dimensions
exl-id: 7c0ec494-d79b-4b65-9161-bdc48485af84
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---

# Pagina-URL

De &#39;pagina-URL&#39; [dimensie](overview.md) geeft de URL&#39;s op uw site weer.

>[!IMPORTANT]
>
>Deze dimensie is alleen beschikbaar in de Data Warehouse. Als u een afmeting URL in andere oplossingen van Analytics wilt gebruiken, overweeg het kopiëren van de waarde in een [eVar](evar.md) bij elke hit.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`g` en `-g` querytekenreeksen](/help/implement/validate/query-parameters.md) in [Aanroepen in de paginaweergave (`t()`)](/help/implement/vars/functions/t-method.md). [Aanroepen voor het bijhouden van koppelingen (`tl()`)](/help/implement/vars/functions/tl-method.md) verwijdert deze dimensie altijd, zelfs als de `g` queryreeks bestaat.

Soms zijn URL&#39;s langer dan 255 bytes. AppMeasurement gebruikt de `g` De parameter van het vraagkoord voor de eerste 255 bytes van URL in beeldverzoeken. Als een URL langer is dan 255 bytes, wordt de rest van de URL opgeslagen in de `-g` querytekenreeksparameter. Protocol- en querytekenreeksen in de URL worden opgenomen in deze variabele.

AppMeasurement verzamelt deze gegevens automatisch op basis van de URL van de pagina. U kunt de verzamelde waarde overschrijven met de opdracht [`pageURL`](/help/implement/vars/page-vars/pageurl.md) variabele.

## Een eVar vullen met URL

Adobe raadt aan een eVar in te stellen op de samengevoegde tekenreeks `window.location.hostname + window.location.pathname`. Deze tekenreeks werkt doorgaans beter dan `window.location.href` omdat het protocol, vraagkoorden, en ankermarkeringen weglaat.

Als u wilt dat de eVar exact overeenkomt met de dimensie &#39;Pagina-URL&#39; in de Data Warehouse, kunt u [dynamische variabelen](/help/implement/vars/page-vars/dynamic-variables.md) en stel de eVar in op `D=g` bij elke treffer.

## Dimension-items

Tot Dimension-items behoren de URL&#39;s van pagina&#39;s op uw site.
