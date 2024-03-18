---
title: pageType
description: Bepaal of de huidige pagina een fout van 404 is.
feature: Variables
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
role: Admin, Developer
source-git-commit: 5ef92db2f5edb5fded497dddedd56abd49d8a019
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# pageType

De `pageType` variabele is een vlag die wordt gebruikt om foutenpagina&#39;s op uw plaats, zoals 404 fouten aan te wijzen. Als deze variabele de tekenreeks bevat `errorPage`, vult het bestand Pagina&#39;s niet gevonden [dimensie](/help/components/dimensions/pages-not-found.md) en [metrisch](/help/components/metrics/pages-not-found.md).

>[!IMPORTANT]
>
>Stel deze variabele niet in op pagina&#39;s zonder foutmelding.

## Paginatype met de Web SDK

Kanaal wordt toegewezen aan de volgende variabelen:

* [XDM-object](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webPageDetails.isErrorPage` - dit XDM-veld is een Booleaanse waarde; stel het in op `true` om deze te markeren als een foutpagina, of `false` als het geen foutpagina is.
* [Data, object](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.pageType` - dit gegevensobjectveld is een tekenreeks; stel het in op `"errorPage"` om het als zodanig te markeren.

## Paginatype met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.pageType in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De `s.pageType` variabele is een tekenreeks waarbij de waarde `errorPage` is de enige geldige waarde. Stel deze variabele in op deze waarde op een foutpagina op uw site, bijvoorbeeld op 404 pagina&#39;s.

```js
s.pageType = "errorPage";
```

>[!TIP]
>
>Gebruik een eVar om de foutcode te verzamelen, zodat u meer informatie krijgt over de specifieke fouten die bezoekers op uw site tegenkomen.
