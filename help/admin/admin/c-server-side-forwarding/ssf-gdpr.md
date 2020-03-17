---
description: 'null'
title: GDPR/ePrivacy compliance en server-side forward
uuid: 1b90c567-3321-4dbd-a699-38c04e809fa4
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# GDPR/ePrivacy compliance en server-side forward

In dit gedeelte worden recente verbeteringen aan het doorsturen aan de serverzijde beschreven die werden veroorzaakt door de [EU-regelgeving](https://ec.europa.eu/ipg/basics/legal/cookies/index_en.htm)inzakede naleving van cookies, die op 30 september 2017 van kracht werd.

Het doorsturen aan de serverzijde wordt gebruikt om gegevens van de Analytics van Adobe aan andere [!DNL Experience Cloud Solutions], zoals Manager van de Audience, in echt te delen - tijd. Wanneer toegelaten, server-zijhet door:sturen staat ook Analytics toe om gegevens aan andere oplossingen van de Wolk van de Ervaring te duwen en voor die oplossingen om gegevens aan Analytics tijdens het proces van de gegevensinzameling te duwen.

Tot voor kort, server-zijhet door:sturen had geen manier om tussen toestemmings en pre-toestemmingsgebeurtenissen/treffers te bepalen. Vanaf 1 november 2018 kunt u als de gegevenscontroller (Adobe Analytics-klant) de gegevens vóór de goedkeuring beperken tot Adobe Analytics en voorkomen dat deze worden doorgestuurd naar AAM. Een nieuwe variabele van de implementatiecontext laat u treffers markeren waar de toestemming niet is ontvangen. De variabele, wanneer ingesteld, voorkomt dat deze treffers naar AAM worden verzonden totdat toestemming is ontvangen.

Wanneer deze nieuwe contextvariabele, `cm.ssf=1`, op een hit bestaat, wordt deze hit gemarkeerd en niet server-kant-door:sturen aan AAM. Omgekeerd, als dit koord niet op een klap verschijnt, door:sturen de klap aan AAM.

Server-kant door:sturen is bidirectioneel, betekenend dat wanneer het op een klap wordt toegepast en die klap door:sturen aan AAM, Analytics van de Audience segmentinformatie voor die klap van AAM ontvangt en het terugstuurt naar Analytics. Dientengevolge, zullen om het even welke klappen die niet server-kant door:sturen van Analytics aan AAM niet met de lijst van segment IDs van AAM worden verrijkt. Aldus, zal er een ondergroep van verkeer/hits zijn die geen informatie van segmentidentiteitskaart van AAM zullen krijgen.

## Implementatiedetails {#section_FFA8B66085BF469FAB5365C944FE38F7}

Voer deze stappen uit, afhankelijk van de implementatiemethode.

| Implementatiemethode | Stappen |
|--- |--- |
| Adobe Experience Platform Launch | Ervan uitgaande dat u de extensie Adobe Analytics hebt geïnstalleerd, voegt u de volgende definitie van de variabele van de contextgegevens toe aan de aangepaste code-editor in de configuratie Action van een Regel: <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>Opmerking:  Definieer de contextdata-variabele en stel deze in op 1 als een klant niet instemt met gerichte marketing. Stel de `contextdata` variabele in op *0* voor klanten die hebben ingestemd met gerichte marketing. |
| DTM | Voeg de definitie van de variabele van de contextgegevens aan de redacteur van de Code van de Pagina van de Douane toe: <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>Opmerking:  Definieer de contextdata-variabele en stel deze in op 1 als een klant niet instemt met gerichte marketing. Stel de variabele contextdata in op 0 voor klanten die hebben ingestemd met gerichte marketing. |
| AppMeasurement | Voeg de de veranderlijke definitie van contextgegevens aan het AppMeasurement.js- dossier toe:  <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>Opmerking:  Definieer de contextdata-variabele en stel deze in op 1 als een klant niet instemt met gerichte marketing. Stel de variabele contextdata in op 0 voor klanten die hebben ingestemd met gerichte marketing. |

## Rapportage (optioneel) {#section_6AD4028EC11C4DABA2A34469DDC99E89}

U kunt de Analytics van Adobe gebruiken om op hoeveel van uw verkeer gebaseerd op toestemming is en dientengevolge server-kant door:sturen tegenover hoeveel van uw verkeer niet toestemming gebaseerd is en niet aan AAM is doorgestuurd.

Om dit type van rapportering te vormen, kaart de nieuwe contextvariabele aan een variabele van het douaneverkeer (steun) via verwerkingsregels. Daartoe

1. Implementeer de variabele &quot;cm.ssf&quot; (zoals hierboven weergegeven).
1. [De eigenschap Prop inschakelen.](/help/admin/admin/c-traffic-variables/traffic-var.md)
1. Gebruik verwerkingsregels om de contextvariabele toe te wijzen aan de eigenschap prop.

   1. Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** en selecteer vervolgens een rapportsuite.
   1. Klik op  **[!UICONTROL Edit Report Suite]** > **[!UICONTROL General]** > **[!UICONTROL Processing Rules]** .
   1. Klik op **[!UICONTROL Add Rule.]**
   1. Overschrijf onder **[!UICONTROL Always Execute]**, de waarde van de eigenschap die u had ingeschakeld met de contextvariabele &quot;cm.ssf(Context Data)&quot;.
   1. Klik op **[!UICONTROL Save]**.

