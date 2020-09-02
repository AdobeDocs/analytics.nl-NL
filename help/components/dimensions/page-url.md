---
title: Pagina-URL
description: De URL van de pagina.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---


# Pagina-URL

De dimensie Pagina-URL geeft een overzicht van de URL&#39;s op uw site.

>[!IMPORTANT]
>
>Deze dimensie is alleen beschikbaar in de Data Warehouse. Als u een afmeting URL in andere oplossingen van Analytics wilt gebruiken, denk na kopieerend de waarde in een [eVar](evar.md) op elke slag.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van de [`g` en `-g` vraagkoorden](/help/implement/validate/query-parameters.md) in de vraag van de [mening van de Pagina terug (`t()`)](/help/implement/vars/functions/t-method.md). [De het volgen van de verbinding vraag (`tl()`)](/help/implement/vars/functions/tl-method.md) verwijdert altijd deze afmeting, zelfs als het `g` vraagkoord bestaat.

Soms zijn URL&#39;s langer dan 255 bytes. AppMeasurement gebruikt de parameter van het `g` vraagkoord voor de eerste 255 bytes van URL in beeldverzoeken. Als een URL langer is dan 255 bytes, wordt de rest van URL opgeslagen in de parameter van het `-g` vraagkoord. Protocol- en querytekenreeksen in de URL worden opgenomen in deze variabele.

AppMeasurement verzamelt deze gegevens automatisch op basis van de URL van de pagina. U kunt de verzamelde waarde overschrijven met de [`pageURL`](/help/implement/vars/page-vars/pageurl.md) variabele.

## Een eVar met URL vullen

Adobe raadt aan een eVar in te stellen op de samengevoegde tekenreeks `window.location.hostname + window.location.pathname`. Deze tekenreeks werkt meestal beter dan `window.location.href` omdat het protocol, querytekenreeksen en ankerlabels weglaat.

Als u wilt dat de eVar exact overeenkomt met de dimensie &#39;Pagina-URL&#39; in de Data Warehouse, kunt u [dynamische variabelen](/help/implement/vars/page-vars/dynamic-variables.md) gebruiken en de eVar bij elke druk `D=g` instellen.

## Dimension-items

Dimension-items bevatten de URL&#39;s van pagina&#39;s op uw site.
