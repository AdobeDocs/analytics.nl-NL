---
title: Pagina-URL
description: De URL van de pagina.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# Pagina-URL

De dimensie Pagina-URL geeft een overzicht van de URL&#39;s op uw site.

>[!IMPORTANT]
>
>Deze dimensie is alleen beschikbaar in Data warehouse. Als u een URL-dimensie wilt gebruiken in andere Analytics-oplossingen, gebruikt u een [eVar](evar.md).

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van het [`g` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de [`pageURL`](/help/implement/vars/page-vars/pageurl.md) variabele.

## Een eVar met URL vullen

Adobe raadt u aan een eVar in te stellen op de samengevoegde tekenreeks `window.location.hostname + window.location.pathname`. Deze tekenreeks werkt meestal beter dan `window.location.href` omdat het protocol, querytekenreeksen en ankerlabels weglaat.

Als u wilt dat de eVar precies de &quot;Pagina URL&quot;afmeting in Data warehouse aanpast, kunt u [dynamische variabelen](/help/implement/vars/page-vars/dynamic-variables.md) gebruiken en eVar plaatsen aan `D=g` bij elke slag. Deze methode werkt niet voor aangepaste koppelingstreffers, aangezien de pagina-URL voor alle [`tl()`](/help/implement/vars/functions/tl-method.md) aanroepen wordt gestript.

## Dimensie-items

Dimensie-items bevatten de URL&#39;s van pagina&#39;s op uw site.
