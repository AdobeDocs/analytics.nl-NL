---
title: Toewijzing van gegevensobjectvelden aan Adobe Analytics
description: Geef weer welke gegevensobjectvelden Experience Platform Edge automatisch toewijst aan analytische variabelen.
feature: Implementation Basics
role: Admin, Developer
exl-id: 45b2fbbc-73ca-40b3-9484-b406ae99fdad
source-git-commit: b3546e67cccc37cbdb89db2e80b3b34b2dbe417b
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 0%

---

# Toewijzing van gegevensobjectvelden aan Adobe Analytics

In de volgende tabel ziet u het gegevensobjectveld dat de Adobe Experience Platform Edge Network automatisch toewijst aan Adobe Analytics. Als u deze paden voor gegevensobjectvelden gebruikt, is er geen extra configuratie nodig om gegevens naar Adobe Analytics te verzenden.

U wordt aangeraden deze velden te gebruiken als u Customer Journey Analytics in de toekomst wilt gebruiken. Deze implementatiemethode staat uw organisatie toe om gegevens naar Adobe te verzenden gebruikend het Web SDK zonder zich aan een schema XDM in overeenstemming te brengen. Wanneer uw organisatie bereid is om gegevens naar Adobe Experience Platform te verzenden, kunt u [ afbeelding DataStream ](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/data-prep#mapping) gebruiken om gegevensobjecten gebieden aan hun respectieve gebieden te richten XDM.

## Waardeprioriteiten

De meeste gebieden van gegevensobjecten in deze lijst beantwoorden aan a [ in kaart gebracht XDM gebied ](xdm-var-mapping.md). Tijdens Adobe Analytics-opname worden waarden eerst toegewezen van XDM aan analytische variabelen. De herkende gegevensobjecten gebieden worden dan in kaart gebracht en om het even welke eerder vastgestelde waarden beschrijven wanneer zij aan de zelfde variabele Analytics toewijzen. Als `data.__adobe.analytics.events` bijvoorbeeld aanwezig is, vervangt deze de gehele set gebeurtenissen die anders uit XDM zouden worden afgeleid; gebeurtenissen worden niet gecombineerd tussen beide bronnen. Een lege tekenreeks (`""`) in een gegevensobjectveld laat de toegewezen analytische variabele voor de hit leeg, zelfs als het corresponderende XDM-veld een waarde bevat.

Sommige gebieden van gegevensobjecten steunen ook hun respectieve [ de parameterwaarde van de Vraag ](../validate/query-parameters.md) als steno waarden. U kunt standaardobjectvelden en velden voor steno-gegevensobjecten onderling verwisselbaar gebruiken, zolang ze beide voor unieke variabelen zijn. Stel niet tegelijkertijd zowel een standaard gegevensobjectveld als het desbetreffende stenogegevensobjectveld in. Adobe kan niet garanderen welk veld prioriteit heeft.

## Gegevensobjectveldtoewijzing

De vorige updates aan deze lijst kunnen op [ worden gevonden van deze pagina begaat geschiedenis op GitHub ](https://github.com/AdobeDocs/analytics.en/commits/main/help/implement/aep-edge/data-var-mapping.md). Net als bij AppMeasurement-variabelen zijn in alle gegevensobjectvelden hoofdlettergevoelig.

| Gegevensobjectveldpad | Variabele en beschrijving voor analyse |
| --- | --- |
| `data.__adobe.analytics.browserHeight` | De [ Browser hoogte ](../../components/dimensions/browser-height.md) afmeting. Het stenoveld `data.__adobe.analytics.bh` wordt ook ondersteund. |
| `data.__adobe.analytics.browserWidth` | De [ Browser breedte ](../../components/dimensions/browser-width.md) afmeting. Het stenoveld `data.__adobe.analytics.bw` wordt ook ondersteund. |
| `data.__adobe.analytics.campaign` | De [ het Volgen code ](../../components/dimensions/tracking-code.md) dimensie. Het stenoveld `data.__adobe.analytics.v0` wordt ook ondersteund. |
| `data.__adobe.analytics.channel` | De [ sectie van de Plaats ](../../components/dimensions/site-section.md) dimensie. Het stenoveld `data.__adobe.analytics.ch` wordt ook ondersteund. |
| `data.__adobe.analytics.colorDepth` | De [ diepte van de Kleur ](../../components/dimensions/color-depth.md) afmeting. Het stenoveld `data.__adobe.analytics.c` wordt ook ondersteund. |
| `data.__adobe.analytics.connectionType` | Het [ type van Verbinding ](../../components/dimensions/connection-type.md) afmeting. Het stenoveld `data.__adobe.analytics.ct` wordt ook ondersteund. |
| `data.__adobe.analytics.contextData` | [ variabelen van contextgegevens ](/help/implement/vars/page-vars/contextdata.md). |
| `data.__adobe.analytics.cookiesEnabled` | De [ steun van het Koekje ](../../components/dimensions/cookie-support.md) dimensie. Het stenoveld `data.__adobe.analytics.k` wordt ook ondersteund. |
| `data.__adobe.analytics.currencyCode` | De implementatievariabele [`currencyCode`](../vars/config-vars/currencycode.md) . Het stenoveld `data.__adobe.analytics.cc` wordt ook ondersteund. |
| `data.__adobe.analytics.dynamicVariablePrefix` | De implementatievariabele [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) . |
| `data.__adobe.analytics.eVar1` - `data.__adobe.analytics.eVar250` | [ eVar ](../../components/dimensions/evar.md) afmetingen. De steno-velden `data.__adobe.analytics.v1` - `data.__adobe.analytics.v250` worden ook ondersteund. |
| `data.__adobe.analytics.events` | [ de gebeurtenissen van de Douane ](../../components/metrics/custom-events.md). Maak dit veld op ongeveer dezelfde manier op als de implementatievariabele [`events`](../vars/page-vars/events/events-overview.md) . |
| `data.__adobe.analytics.javaEnabled` | De [ toegelaten Java ](../../components/dimensions/java-enabled.md) dimensie. Het stenoveld `data.__adobe.analytics.v` wordt ook ondersteund. |
| `data.__adobe.analytics.latitude` | De hulp plaatst de [ mobiele de levenscyclusafmetingen van de Plaats ](../../components/dimensions/lifecycle-dimensions.md). Het stenoveld `data.__adobe.analytics.lat` wordt ook ondersteund. |
| `data.__adobe.analytics.linkName` | De [ verbinding van de Douane ](../../components/dimensions/custom-link.md), [ verbinding van de Download ](../../components/dimensions/download-link.md), of [ Verbinding van de Uitgang ](../../components/dimensions/exit-link.md) dimensie, afhankelijk van de waarde in `data.__adobe.analytics.linkType`. Het stenoveld `data.__adobe.analytics.pev2` wordt ook ondersteund. |
| `data.__adobe.analytics.linkURL` | De implementatievariabele [`linkURL`](../vars/config-vars/linkurl.md) . Het stenoveld `data.__adobe.analytics.pev1` wordt ook ondersteund. |
| `data.__adobe.analytics.linkType` | Bepaalt het type van geklikte verbinding. Geldige waarden zijn `o` (Aangepaste koppelingen), `d` (Koppelingen downloaden) en `e` (Koppelingen afsluiten). Het stenoveld `data.__adobe.analytics.pe` wordt ook ondersteund. |
| `data.__adobe.analytics.list1` - `data.__adobe.analytics.list3` | [`list`](/help/implement/vars/page-vars/list.md) implementatievariabelen. De steno-velden `data.__adobe.analytics.l1` - `data.__adobe.analytics.list3` worden ook ondersteund. |
| `data.__adobe.analytics.longitude` | De hulp plaatst de [ mobiele de levenscyclusafmetingen van de Plaats ](../../components/dimensions/lifecycle-dimensions.md). Het stenoveld `data.__adobe.analytics.lon` wordt ook ondersteund. |
| `data.__adobe.analytics.pageName` | De [ dimensie van de Pagina ](/help/components/dimensions/page.md). |
| `data.__adobe.analytics.pageURL` | De [ pagina URL ](/help/components/dimensions/page-url.md) afmeting. Het stenoveld `data.__adobe.analytics.g` wordt ook ondersteund. |
| `data.__adobe.analytics.pageType` | De implementatievariabele [`pageType`](../vars/page-vars/pagetype.md) . |
| `data.__adobe.analytics.prop1` - `data.__adobe.analytics.prop75` | [ afmetingen van 0} Prop {. ](../../components/dimensions/prop.md) De steno-velden `data.__adobe.analytics.c1` - `data.__adobe.analytics.c75` worden ook ondersteund. |
| `data.__adobe.analytics.purchaseID` | De implementatievariabele [`purchaseID`](../vars/page-vars/purchaseid.md) . |
| `data.__adobe.analytics.products` | De implementatievariabele [`products`](../vars/page-vars/products.md) , met dezelfde opmaak. |
| `data.__adobe.analytics.referrer` | De [ dimensie van de Verwijzer ](/help/components/dimensions/referrer.md). |
| `data.__adobe.analytics.resolution` | De [ resolutie van de Monitor ](../../components/dimensions/monitor-resolution.md) dimensie. Het stenoveld `data.__adobe.analytics.s` wordt ook ondersteund. |
| `data.__adobe.analytics.server` | De [ dimensie van de Server ](/help/components/dimensions/server.md). |
| `data.__adobe.analytics.transactionID` | De implementatievariabele [`transactionID`](../vars/page-vars/transactionid.md) . Het stenoveld `data.__adobe.analytics.xact` wordt ook ondersteund. |
| `data.__adobe.analytics.zip` | De [ dimensie van het Postcode ](../../components/dimensions/zip-code.md). |

{style="table-layout:auto"}
