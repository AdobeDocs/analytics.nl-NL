---
title: pageType
description: Bepaal of de huidige pagina een fout van 404 is.
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---

# pageType

De variabele `pageType` is een vlag die wordt gebruikt om foutenpagina&#39;s op uw plaats, zoals 404 fouten aan te wijzen. Als deze variabele de tekenreeks `errorPage` bevat, wordt de dimensie &#39;Pagina&#39;s niet gevonden&#39; gevuld.

>[!IMPORTANT]
>
>Stel deze variabele niet in op pagina&#39;s zonder foutmelding.

## Paginatype met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.pageType in AppMeasurement en aangepaste code-editor

De variabele `s.pageType` is een tekenreeks waarbij de waarde `errorPage` de enige geldige waarde is. Stel deze variabele in op deze waarde op een foutpagina op uw site, bijvoorbeeld op 404 pagina&#39;s.

```js
s.pageType = "errorPage";
```

>[!TIP]
>
>Gebruik een eVar om de foutcode te verzamelen, zodat u meer informatie krijgt over de specifieke fouten die bezoekers op uw site tegenkomen.
