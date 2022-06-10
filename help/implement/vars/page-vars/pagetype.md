---
title: pageType
description: Bepaal of de huidige pagina een fout van 404 is.
feature: Variables
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 1%

---

# pageType

De `pageType` variabele is een vlag die wordt gebruikt om foutenpagina&#39;s op uw plaats, zoals 404 fouten aan te wijzen. Als deze variabele de tekenreeks bevat `errorPage`, wordt de dimensie &#39;Pagina&#39;s niet gevonden&#39; gevuld.

>[!IMPORTANT]
>
>Stel deze variabele niet in op pagina&#39;s zonder foutmelding.

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
