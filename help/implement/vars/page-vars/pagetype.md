---
title: pageType
description: Bepaal of de huidige pagina een fout van 404 is.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# pageType

De `pageType` variabele is een vlag die wordt gebruikt om foutenpagina&#39;s op uw plaats, zoals 404 fouten aan te wijzen. Als deze variabele de tekenreeks bevat, wordt de dimensie &#39;Pagina&#39;s niet gevonden&#39; gevuld. `errorPage`

>[!IMPORTANT] Stel deze variabele niet in op pagina&#39;s zonder foutmelding.

## Paginatype in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.pageType in AppMeasurement en Launch, aangepaste code-editor

De `s.pageType` variabele is een tekenreeks waarbij de waarde de enige geldige waarde `errorPage` is. Stel deze variabele in op deze waarde op een foutpagina op uw site, bijvoorbeeld op 404 pagina&#39;s.

```js
s.pageType = "errorPage";
```

>[!TIP] Gebruik een eVar om de foutencode te verzamelen zodat kunt u meer informatie krijgen over welke specifieke fouten bezoekers op uw plaats ontmoeten.
