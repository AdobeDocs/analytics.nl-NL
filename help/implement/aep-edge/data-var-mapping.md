---
title: Gegevensobjectvariabele toewijzen aan Adobe Analytics
description: Geef aan welke gegevensobjectvelden Experience Platform Edge automatisch wordt toegewezen aan analytische variabelen.
feature: Implementation Basics
role: Admin, Developer
exl-id: 45b2fbbc-73ca-40b3-9484-b406ae99fdad
source-git-commit: 59d9dd8055a13046d05ac4c3b5261a6c5a919b5c
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Gegevensobjectvariabele toewijzen aan Adobe Analytics

In de volgende tabel worden de gegevensobjectvariabelen weergegeven die de Adobe Experience Platform-Edge Network automatisch toewijst aan Adobe Analytics. Als u deze paden voor gegevensobjectvelden gebruikt, is er geen extra configuratie nodig om gegevens naar Adobe Analytics te verzenden.

U wordt aangeraden deze velden te gebruiken als u in de toekomst Customer Journey Analytics wilt gebruiken. Deze implementatiemethode staat uw organisatie toe om gegevens naar Adobe te verzenden gebruikend het Web SDK zonder zich aan een schema XDM in overeenstemming te brengen. Als uw organisatie klaar is om gegevens naar Adobe Experience Platform te verzenden, kunt u [DataStream-toewijzing](https://experienceleague.adobe.com/nl/docs/experience-platform/datastreams/data-prep#mapping) om gegevensobjectvelden te wijzen naar hun respectievelijke XDM-velden.

## Waardeprioriteiten

De meeste gegevensobjectvelden in deze tabel komen overeen met een [toegewezen XDM-veld](xdm-var-mapping.md). Als u zowel een bepaald gegevensobjectveld als het bijbehorende XDM-veld instelt, krijgt het gegevensobjectveld prioriteit. Als het veld `data.__adobe.analytics.events` is aanwezig, worden alle aan gebeurtenissen gerelateerde XDM-objectvelden overschreven.

Sommige gegevensobjectvelden ondersteunen ook hun respectievelijke [Parameterwaarde voor query](../validate/query-parameters.md) als stenorwaarden. U kunt standaardobjectvelden en velden voor steno-gegevensobjecten onderling verwisselbaar gebruiken, zolang ze beide voor unieke variabelen zijn. Stel niet tegelijkertijd zowel een standaard gegevensobjectveld als het desbetreffende stenogegevensobjectveld in. Adobe kan niet garanderen welk terrein prioriteit heeft.

## Gegevensobjectveldtoewijzing

U vindt vorige updates van deze tabel op de pagina [geschiedenis toewijzen op GitHub](https://github.com/AdobeDocs/analytics.nl-NL/commits/main/help/implement/aep-edge/data-var-mapping.md). Net als bij AppMeasurement-variabelen zijn in alle gegevensobjectvelden hoofdlettergevoelig.

| Gegevensobjectveldpad | Variabele en beschrijving voor analyse |
| --- | --- |
| `data.__adobe.analytics.browserHeight` | De [Hoogte browser](../../components/dimensions/browser-height.md) dimensie. Het stenoveld `data.__adobe.analytics.bh` wordt ook ondersteund. |
| `data.__adobe.analytics.browserWidth` | De [Browserbreedte](../../components/dimensions/browser-width.md) dimensie. Het stenoveld `data.__adobe.analytics.bw` wordt ook ondersteund. |
| `data.__adobe.analytics.campaign` | De [Code bijhouden](../../components/dimensions/tracking-code.md) dimensie. Het stenoveld `data.__adobe.analytics.v0` wordt ook ondersteund. |
| `data.__adobe.analytics.channel` | De [Sectie Site](../../components/dimensions/site-section.md) dimensie. Het stenoveld `data.__adobe.analytics.ch` wordt ook ondersteund. |
| `data.__adobe.analytics.colorDepth` | De [Kleurdiepte](../../components/dimensions/color-depth.md) dimensie. Het stenoveld `data.__adobe.analytics.c` wordt ook ondersteund. |
| `data.__adobe.analytics.connectionType` | De [Verbindingstype](../../components/dimensions/connection-type.md) dimensie. Het stenoveld `data.__adobe.analytics.ct` wordt ook ondersteund. |
| `data.__adobe.analytics.contextData` | [Contextgegevensvariabelen](/help/implement/vars/page-vars/contextdata.md). |
| `data.__adobe.analytics.cookiesEnabled` | De [Cookie-ondersteuning](../../components/dimensions/cookie-support.md) dimensie. Het stenoveld `data.__adobe.analytics.k` wordt ook ondersteund. |
| `data.__adobe.analytics.currencyCode` | De [`currencyCode`](../vars/config-vars/currencycode.md) uitvoeringsvariabele. Het stenoveld `data.__adobe.analytics.cc` wordt ook ondersteund. |
| `data.__adobe.analytics.dynamicVariablePrefix` | De [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) uitvoeringsvariabele. |
| `data.__adobe.analytics.eVar1` - `data.__adobe.analytics.eVar250` | [eVar](../../components/dimensions/evar.md) afmetingen. De stenorvelden `data.__adobe.analytics.v1` - `data.__adobe.analytics.v250` worden ook ondersteund. |
| `data.__adobe.analytics.events` | [Aangepaste gebeurtenissen](../../components/metrics/custom-events.md). Dit veld op vergelijkbare wijze opmaken als het [`events`](../vars/page-vars/events/events-overview.md) uitvoeringsvariabele. |
| `data.__adobe.analytics.javaEnabled` | De [Java ingeschakeld](../../components/dimensions/java-enabled.md) dimensie. Het stenoveld `data.__adobe.analytics.v` wordt ook ondersteund. |
| `data.__adobe.analytics.latitude` | Hiermee stelt u de [Locatie](../../components/dimensions/lifecycle-dimensions.md) mobiele levenscyclusafmetingen. Het stenoveld `data.__adobe.analytics.lat` wordt ook ondersteund. |
| `data.__adobe.analytics.linkName` | De [Aangepaste koppeling](../../components/dimensions/custom-link.md), [Koppeling downloaden](../../components/dimensions/download-link.md), of [Koppeling afsluiten](../../components/dimensions/exit-link.md) dimensie, afhankelijk van de waarde in `data.__adobe.analytics.linkType`. Het stenoveld `data.__adobe.analytics.pev2` wordt ook ondersteund. |
| `data.__adobe.analytics.linkURL` | De [`linkURL`](../vars/config-vars/linkurl.md) uitvoeringsvariabele. Het stenoveld `data.__adobe.analytics.pev1` wordt ook ondersteund. |
| `data.__adobe.analytics.linkType` | Bepaalt het type van geklikte verbinding. Geldige waarden zijn `o` (Aangepaste koppelingen), `d` (Koppelingen downloaden) en `e` (Koppelingen afsluiten). Het stenoveld `data.__adobe.analytics.pe` wordt ook ondersteund. |
| `data.__adobe.analytics.list1` - `data.__adobe.analytics.list3` | [`list`](/help/implement/vars/page-vars/list.md) uitvoeringsvariabelen. De stenorvelden `data.__adobe.analytics.l1` - `data.__adobe.analytics.list3` worden ook ondersteund. |
| `data.__adobe.analytics.longitude` | Help stelt de [Locatie](../../components/dimensions/lifecycle-dimensions.md) mobiele levenscyclusafmetingen. Het stenoveld `data.__adobe.analytics.lon` wordt ook ondersteund. |
| `data.__adobe.analytics.pageName` | De [Pagina](/help/components/dimensions/page.md) dimensie. |
| `data.__adobe.analytics.pageURL` | De [Pagina-URL](/help/components/dimensions/page-url.md) dimensie. Het stenoveld `data.__adobe.analytics.g` wordt ook ondersteund. |
| `data.__adobe.analytics.pageType` | De [`pageType`](../vars/page-vars/pagetype.md) uitvoeringsvariabele. |
| `data.__adobe.analytics.prop1` - `data.__adobe.analytics.prop75` | [Prop](../../components/dimensions/prop.md) afmetingen. De stenorvelden `data.__adobe.analytics.c1` - `data.__adobe.analytics.c75` worden ook ondersteund. |
| `data.__adobe.analytics.purchaseID` | De [`purchaseID`](../vars/page-vars/purchaseid.md) uitvoeringsvariabele. |
| `data.__adobe.analytics.products` | De [`products`](../vars/page-vars/products.md) implementatievariabele, met dezelfde opmaak. |
| `data.__adobe.analytics.referrer` | De [Referenter](/help/components/dimensions/referrer.md) dimensie. |
| `data.__adobe.analytics.resolution` | De [Monitorresolutie](../../components/dimensions/monitor-resolution.md) dimensie. Het stenoveld `data.__adobe.analytics.s` wordt ook ondersteund. |
| `data.__adobe.analytics.server` | De [Server](/help/components/dimensions/server.md) dimensie. |
| `data.__adobe.analytics.transactionID` | De [`transactionID`](../vars/page-vars/transactionid.md) uitvoeringsvariabele. Het stenoveld `data.__adobe.analytics.xact` wordt ook ondersteund. |
| `data.__adobe.analytics.zip` | De [Postcode](../../components/dimensions/zip-code.md) dimensie. |

{style="table-layout:auto"}
