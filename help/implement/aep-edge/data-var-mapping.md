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

U wordt aangeraden deze velden te gebruiken als u Customer Journey Analytics in de toekomst wilt gebruiken. Deze implementatiemethode staat uw organisatie toe om gegevens naar Adobe te verzenden gebruikend het Web SDK zonder zich aan een schema XDM in overeenstemming te brengen. Wanneer uw organisatie bereid is om gegevens naar Adobe Experience Platform te verzenden, kunt u [&#x200B; afbeelding DataStream &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/datastreams/data-prep#mapping) gebruiken om gegevensobjecten gebieden aan hun respectieve gebieden te richten XDM.

## Waardeprioriteiten

De meeste gebieden van gegevensobjecten in deze lijst beantwoorden aan a [&#x200B; in kaart gebracht XDM gebied &#x200B;](xdm-var-mapping.md). Tijdens Adobe Analytics-opname worden waarden eerst toegewezen van XDM aan analytische variabelen. De herkende gegevensobjecten gebieden worden dan in kaart gebracht en om het even welke eerder vastgestelde waarden beschrijven wanneer zij aan de zelfde variabele Analytics toewijzen. Als `data.__adobe.analytics.events` bijvoorbeeld aanwezig is, vervangt deze de gehele set gebeurtenissen die anders uit XDM zouden worden afgeleid; gebeurtenissen worden niet gecombineerd tussen beide bronnen. Een lege tekenreeks (`""`) in een gegevensobjectveld laat de toegewezen analytische variabele voor de hit leeg, zelfs als het corresponderende XDM-veld een waarde bevat.

Sommige gebieden van gegevensobjecten steunen ook hun respectieve [&#x200B; de parameterwaarde van de Vraag &#x200B;](../validate/query-parameters.md) als steno waarden. U kunt standaardobjectvelden en velden voor steno-gegevensobjecten onderling verwisselbaar gebruiken, zolang ze beide voor unieke variabelen zijn. Stel niet tegelijkertijd zowel een standaard gegevensobjectveld als het desbetreffende stenogegevensobjectveld in. Adobe kan niet garanderen welk veld prioriteit heeft.

## Gegevensobjectveldtoewijzing

De vorige updates aan deze lijst kunnen op [&#x200B; worden gevonden van deze pagina begaat geschiedenis op GitHub &#x200B;](https://github.com/AdobeDocs/analytics.nl-NL/commits/main/help/implement/aep-edge/data-var-mapping.md). Net als bij AppMeasurement-variabelen zijn in alle gegevensobjectvelden hoofdlettergevoelig.

| Gegevensobjectveldpad | Variabele en beschrijving voor analyse |
| --- | --- |
| `data.__adobe.analytics.browserHeight` | De [&#x200B; Browser hoogte &#x200B;](../../components/dimensions/browser-height.md) afmeting. Het stenoveld `data.__adobe.analytics.bh` wordt ook ondersteund. |
| `data.__adobe.analytics.browserWidth` | De [&#x200B; Browser breedte &#x200B;](../../components/dimensions/browser-width.md) afmeting. Het stenoveld `data.__adobe.analytics.bw` wordt ook ondersteund. |
| `data.__adobe.analytics.campaign` | De [&#x200B; het Volgen code &#x200B;](../../components/dimensions/tracking-code.md) dimensie. Het stenoveld `data.__adobe.analytics.v0` wordt ook ondersteund. |
| `data.__adobe.analytics.channel` | De [&#x200B; sectie van de Plaats &#x200B;](../../components/dimensions/site-section.md) dimensie. Het stenoveld `data.__adobe.analytics.ch` wordt ook ondersteund. |
| `data.__adobe.analytics.colorDepth` | De [&#x200B; diepte van de Kleur &#x200B;](../../components/dimensions/color-depth.md) afmeting. Het stenoveld `data.__adobe.analytics.c` wordt ook ondersteund. |
| `data.__adobe.analytics.connectionType` | Het [&#x200B; type van Verbinding &#x200B;](../../components/dimensions/connection-type.md) afmeting. Het stenoveld `data.__adobe.analytics.ct` wordt ook ondersteund. |
| `data.__adobe.analytics.contextData` | [&#x200B; variabelen van contextgegevens &#x200B;](/help/implement/vars/page-vars/contextdata.md). |
| `data.__adobe.analytics.cookiesEnabled` | De [&#x200B; steun van het Koekje &#x200B;](../../components/dimensions/cookie-support.md) dimensie. Het stenoveld `data.__adobe.analytics.k` wordt ook ondersteund. |
| `data.__adobe.analytics.currencyCode` | De implementatievariabele [`currencyCode`](../vars/config-vars/currencycode.md) . Het stenoveld `data.__adobe.analytics.cc` wordt ook ondersteund. |
| `data.__adobe.analytics.dynamicVariablePrefix` | De implementatievariabele [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) . |
| `data.__adobe.analytics.eVar1` - `data.__adobe.analytics.eVar250` | [&#x200B; eVar &#x200B;](../../components/dimensions/evar.md) afmetingen. De steno-velden `data.__adobe.analytics.v1` - `data.__adobe.analytics.v250` worden ook ondersteund. |
| `data.__adobe.analytics.events` | [&#x200B; de gebeurtenissen van de Douane &#x200B;](../../components/metrics/custom-events.md). Maak dit veld op ongeveer dezelfde manier op als de implementatievariabele [`events`](../vars/page-vars/events/events-overview.md) . |
| `data.__adobe.analytics.javaEnabled` | De [&#x200B; toegelaten Java &#x200B;](../../components/dimensions/java-enabled.md) dimensie. Het stenoveld `data.__adobe.analytics.v` wordt ook ondersteund. |
| `data.__adobe.analytics.latitude` | De hulp plaatst de [&#x200B; mobiele de levenscyclusafmetingen van de Plaats &#x200B;](../../components/dimensions/lifecycle-dimensions.md). Het stenoveld `data.__adobe.analytics.lat` wordt ook ondersteund. |
| `data.__adobe.analytics.linkName` | De [&#x200B; verbinding van de Douane &#x200B;](../../components/dimensions/custom-link.md), [&#x200B; verbinding van de Download &#x200B;](../../components/dimensions/download-link.md), of [&#x200B; Verbinding van de Uitgang &#x200B;](../../components/dimensions/exit-link.md) dimensie, afhankelijk van de waarde in `data.__adobe.analytics.linkType`. Het stenoveld `data.__adobe.analytics.pev2` wordt ook ondersteund. |
| `data.__adobe.analytics.linkURL` | De implementatievariabele [`linkURL`](../vars/config-vars/linkurl.md) . Het stenoveld `data.__adobe.analytics.pev1` wordt ook ondersteund. |
| `data.__adobe.analytics.linkType` | Bepaalt het type van geklikte verbinding. Geldige waarden zijn `o` (Aangepaste koppelingen), `d` (Koppelingen downloaden) en `e` (Koppelingen afsluiten). Het stenoveld `data.__adobe.analytics.pe` wordt ook ondersteund. |
| `data.__adobe.analytics.list1` - `data.__adobe.analytics.list3` | [`list`](/help/implement/vars/page-vars/list.md) implementatievariabelen. De steno-velden `data.__adobe.analytics.l1` - `data.__adobe.analytics.list3` worden ook ondersteund. |
| `data.__adobe.analytics.longitude` | De hulp plaatst de [&#x200B; mobiele de levenscyclusafmetingen van de Plaats &#x200B;](../../components/dimensions/lifecycle-dimensions.md). Het stenoveld `data.__adobe.analytics.lon` wordt ook ondersteund. |
| `data.__adobe.analytics.pageName` | De [&#x200B; dimensie van de Pagina &#x200B;](/help/components/dimensions/page.md). |
| `data.__adobe.analytics.pageURL` | De [&#x200B; pagina URL &#x200B;](/help/components/dimensions/page-url.md) afmeting. Het stenoveld `data.__adobe.analytics.g` wordt ook ondersteund. |
| `data.__adobe.analytics.pageType` | De implementatievariabele [`pageType`](../vars/page-vars/pagetype.md) . |
| `data.__adobe.analytics.prop1` - `data.__adobe.analytics.prop75` | [&#x200B; afmetingen van 0&rbrace; Prop &lbrace;. &#x200B;](../../components/dimensions/prop.md) De steno-velden `data.__adobe.analytics.c1` - `data.__adobe.analytics.c75` worden ook ondersteund. |
| `data.__adobe.analytics.purchaseID` | De implementatievariabele [`purchaseID`](../vars/page-vars/purchaseid.md) . |
| `data.__adobe.analytics.products` | De implementatievariabele [`products`](../vars/page-vars/products.md) , met dezelfde opmaak. |
| `data.__adobe.analytics.referrer` | De [&#x200B; dimensie van de Verwijzer &#x200B;](/help/components/dimensions/referrer.md). |
| `data.__adobe.analytics.resolution` | De [&#x200B; resolutie van de Monitor &#x200B;](../../components/dimensions/monitor-resolution.md) dimensie. Het stenoveld `data.__adobe.analytics.s` wordt ook ondersteund. |
| `data.__adobe.analytics.server` | De [&#x200B; dimensie van de Server &#x200B;](/help/components/dimensions/server.md). |
| `data.__adobe.analytics.transactionID` | De implementatievariabele [`transactionID`](../vars/page-vars/transactionid.md) . Het stenoveld `data.__adobe.analytics.xact` wordt ook ondersteund. |
| `data.__adobe.analytics.zip` | De [&#x200B; dimensie van het Postcode &#x200B;](../../components/dimensions/zip-code.md). |

{style="table-layout:auto"}
