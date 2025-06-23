---
title: pageType
description: Bepaal of de huidige pagina een fout van 404 is.
feature: Appmeasurement Implementation
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# pageType

De variabele `pageType` is een vlag die wordt gebruikt om foutenpagina&#39;s op uw plaats, zoals 404 fouten aan te wijzen. Als deze variabele het koord `errorPage` bevat, bevolkt het de &quot;Pagina&#39;s niet Gevonden&quot;[ dimensie ](/help/components/dimensions/pages-not-found.md) en [ metrisch ](/help/components/metrics/pages-not-found.md).

>[!IMPORTANT]
>
>Stel deze variabele niet in op pagina&#39;s zonder foutmelding.

## Paginatype met Web SDK

Kanaal wordt toegewezen aan de volgende variabelen:

* [ voorwerp XDM ](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webPageDetails.isErrorPage` - dit gebied XDM is een booleaanse waarde; plaats het aan `true` om het als foutenpagina te markeren, of `false` als het geen foutenpagina is.
* [ voorwerp van Gegevens ](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.pageType` - dit gebied van gegevensobjecten is een koord; plaats het aan `"errorPage"` om het als dusdanig te markeren.

## Paginatype met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.pageType in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.pageType` is een tekenreeks waarvan de waarde `errorPage` de enige geldige waarde is. Stel deze variabele in op deze waarde op een foutpagina op uw site, bijvoorbeeld op 404 pagina&#39;s.

```js
s.pageType = "errorPage";
```

>[!TIP]
>
>Gebruik een eVar om de foutcode te verzamelen, zodat u meer informatie kunt krijgen over specifieke fouten die bezoekers op uw site tegenkomen.
