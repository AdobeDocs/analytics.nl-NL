---
title: pageType
description: Bepaal of de huidige pagina een fout van 404 is.
feature: Variables
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
source-git-commit: 8a6c639af7427a9975ccd061d059696d4611dff3
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# pageType

De `pageType` variabele is een vlag die wordt gebruikt om foutenpagina&#39;s op uw plaats, zoals 404 fouten aan te wijzen. Als deze variabele de tekenreeks bevat `errorPage`, vult het bestand &#39;Pagina&#39;s niet gevonden&#39; [dimensie](/help/components/dimensions/pages-not-found.md) en [metrisch](/help/components/metrics/pages-not-found.md).

>[!IMPORTANT]
>
>Stel deze variabele niet in op pagina&#39;s zonder foutmelding.

## Paginatype met de Web SDK

Paginatype is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `web.webPageDetails.isErrorPage`. Dit XDM-veld is een booleaanse waarde. instellen op `true` om deze te markeren als een foutpagina, of `false` als het geen foutpagina is. Adobe zet de booleaanse waarde automatisch om in de tekenreekswaarde `errorPage` wanneer deze naar een analytische rapportsuite wordt verzonden.

## Paginatype met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.pageType in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.pageType` variabele is een tekenreeks waarbij de waarde `errorPage` is de enige geldige waarde. Stel deze variabele in op deze waarde op een foutpagina op uw site, bijvoorbeeld op 404 pagina&#39;s.

```js
s.pageType = "errorPage";
```

>[!TIP]
>
>Gebruik een eVar om de foutcode te verzamelen, zodat u meer informatie krijgt over de specifieke fouten die bezoekers op uw site tegenkomen.
