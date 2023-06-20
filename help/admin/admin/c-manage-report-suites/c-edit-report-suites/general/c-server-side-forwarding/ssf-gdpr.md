---
description: Verklaart verhogingen aan server-kant door:sturen die door de EU verordening van de koekjesnaleving werden veroorzaakt.
title: GDPR/ePrivacy-compliance en server-side doorsturen
feature: Server-Side Forwarding
exl-id: 54e43a16-8f15-4ee8-9aa2-579af30be2c9
source-git-commit: 15f1cd260709c2ab82d56a545494c31ad86d0ab0
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 2%

---

# GDPR/ePrivacy-compliance en server-side doorsturen

Deze sectie verklaart verhogingen aan server-kant door:sturen die door werden veroorzaakt [EU-verordening betreffende de naleving van cookies](https://wikis.ec.europa.eu/display/WEBGUIDE/04.+Cookies+gelijksoortige+technologieën), die van kracht werd op 30 september 2017.

Server-kant het door:sturen wordt gebruikt om gegevens van Adobe Analytics aan andere te delen [!DNL Experience Cloud Solutions], zoals Audience Manager, in real time. Wanneer toegelaten, server-zijhet door:sturen staat ook Analytics toe om gegevens aan andere oplossingen van Experience Cloud te duwen en voor die oplossingen om gegevens aan Analytics tijdens het proces van de gegevensinzameling te duwen.

Eerder, server-zijhet door:sturen had geen manier om tussen toestemmings en pre-toestemmingsgebeurtenissen/treffers te bepalen. Vanaf 1 november 2018 hebt u als de gegevenscontroller (Adobe Analytics-klant) de mogelijkheid om gegevens vóór de toestemming te beperken tot Adobe Analytics en te voorkomen dat deze naar Adobe Audience Manager worden doorgestuurd. Een nieuwe variabele van de implementatiecontext laat u treffers markeren waar de toestemming niet is ontvangen. Als de variabele is ingesteld, worden deze treffers niet naar Adobe Audience Manager verzonden totdat de toestemming is ontvangen.

Wanneer deze nieuwe contextvariabele `cm.ssf=1`, bestaat op een hit, wordt deze hit gemarkeerd en wordt de server-side niet doorgestuurd naar Adobe Audience Manager. Als deze tekenreeks echter niet wordt weergegeven op een hit, wordt de hit doorgestuurd naar Adobe Audience Manager.

Server-kant door:sturen is bidirectioneel, betekenend dat wanneer het op een klap wordt toegepast en die klap door:sturen aan Adobe Audience Manager, Audience Analytics segmentinformatie voor die klap van Adobe Audience Manager ontvangt en het terugstuurt naar Analytics. Dientengevolge, zullen om het even welke klappen die niet server-kant door van Analytics aan Adobe Audience Manager door:sturen niet met de lijst van segment IDs van Adobe Audience Manager worden verrijkt. Aldus, zal er een ondergroep van verkeer/hits zijn die geen informatie van segmentidentiteitskaart van Adobe Audience Manager zal krijgen.

## Implementatiedetails {#section_FFA8B66085BF469FAB5365C944FE38F7}

Voer deze stappen uit, afhankelijk van de implementatiemethode.

| Implementatiemethode | Stappen |
|--- |--- |
| Tags in Adobe Experience Platform | Ervan uitgaande dat u de Adobe Analytics-extensie hebt geïnstalleerd, voegt u de volgende definitie van de variabele van de contextgegevens toe aan de aangepaste code-editor binnen de actieconfiguratie van een Regel: <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>Opmerking: Definieer de contextdata-variabele en stel deze in op 1 als een klant niet instemt met gerichte marketing. Stel de `contextdata` variabele tot *0* voor klanten die akkoord zijn gegaan met gerichte marketing. |
| AppMeasurement | Voeg de de veranderlijke definitie van contextgegevens aan het AppMeasurement.js- dossier toe:  <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>Opmerking: Definieer de contextdata-variabele en stel deze in op 1 als een klant niet instemt met gerichte marketing. Stel de variabele contextdata in op 0 voor klanten die hebben ingestemd met gerichte marketing. |

## Rapportage (optioneel) {#section_6AD4028EC11C4DABA2A34469DDC99E89}

U kunt Adobe Analytics gebruiken om te melden hoeveel van uw verkeer op toestemming gebaseerd is en dientengevolge door:sturen server-kant tegenover hoeveel van uw verkeer niet toestemming gebaseerd is en niet aan Adobe Audience Manager is doorgestuurd.

Om dit type van rapportering te vormen, kaart de nieuwe contextvariabele aan een variabele van het douaneverkeer (steun) via verwerkingsregels. Daartoe

1. Implementeer de variabele &quot;cm.ssf&quot; (zoals hierboven weergegeven).
1. [De eigenschap Prop inschakelen.](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md)
1. Gebruik verwerkingsregels om de contextvariabele toe te wijzen aan de eigenschap prop.

   1. Ga naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** en selecteer vervolgens een rapportsuite.
   1. Klik op  **[!UICONTROL Edit Report Suite]** > **[!UICONTROL General]** > **[!UICONTROL Processing Rules]** .
   1. Klik op **[!UICONTROL Add Rule.]**
   1. Onder **[!UICONTROL Always Execute]**, overschrijft u de waarde van de eigenschap die u hebt ingeschakeld met de contextvariabele &quot;cm.ssf(Context Data)&quot;.
   1. Klik op **[!UICONTROL Save]**.
