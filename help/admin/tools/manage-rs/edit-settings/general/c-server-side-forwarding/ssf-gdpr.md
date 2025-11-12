---
description: Verklaart verhogingen aan server-kant door:sturen die door de EU verordening van de koekjesnaleving werden veroorzaakt.
title: GDPR/ePrivacy compliance en server-side forward
feature: Report Suite Settings
exl-id: 54e43a16-8f15-4ee8-9aa2-579af30be2c9
role: Admin
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# GDPR/ePrivacy compliance en server-side forward

Deze sectie verklaart verhogingen aan server-kant door:sturen die door de [ de nalevingsverordening van de EU koekjesnaleving ](https://wikis.ec.europa.eu/display/WEBGUIDE/04.+Cookies+gelijksoortige+technologieën) werden veroorzaakt, die op 30 september, 2017 van kracht werd.

Het doorsturen aan de serverzijde wordt gebruikt om gegevens van Adobe Analytics naar andere [!DNL Experience Cloud Solutions], zoals Audience Manager, in real time te delen. Wanneer toegelaten, server-zijhet door:sturen staat ook Analytics toe om gegevens aan andere oplossingen van Experience Cloud te duwen en voor die oplossingen om gegevens aan Analytics tijdens het proces van de gegevensinzameling te duwen.

Eerder, server-zijhet door:sturen had geen manier om tussen toestemmings en pre-toestemmingsgebeurtenissen/treffers te bepalen. Vanaf 1 november 2018 hebt u als de gegevenscontroller (Adobe Analytics-klant) de mogelijkheid om gegevens vóór de toestemming te beperken tot Adobe Analytics en te voorkomen dat deze naar Adobe Audience Manager worden doorgestuurd. Met een nieuwe variabele voor de implementatiecontext kunt u treffers markeren op plaatsen waar geen toestemming is ontvangen. Als de variabele is ingesteld, worden deze treffers niet naar Adobe Audience Manager verzonden totdat de toestemming is ontvangen.

Wanneer deze nieuwe contextvariabele, `cm.ssf=1` , op een hit voorkomt, wordt deze hit gemarkeerd en wordt de server-side niet doorgestuurd naar Adobe Audience Manager. Als deze tekenreeks echter niet wordt weergegeven op een hit, wordt de hit doorgestuurd naar Adobe Audience Manager.

Server-kant door:sturen is bidirectioneel, betekenend dat wanneer het op een klap wordt toegepast en die klap door:sturen aan Adobe Audience Manager, Audience Analytics segmentinformatie voor die klap van Adobe Audience Manager ontvangt en het terugstuurt naar Analytics. Dientengevolge, zullen om het even welke klappen die niet server-kant door van Analytics aan Adobe Audience Manager door:sturen niet met de lijst van segment IDs van Adobe Audience Manager worden verrijkt. Aldus, zal er een ondergroep van verkeer/hits zijn die geen informatie van segmentidentiteitskaart van Adobe Audience Manager zal krijgen.

## Implementatiedetails {#section_FFA8B66085BF469FAB5365C944FE38F7}

Voer deze stappen uit, afhankelijk van de implementatiemethode.

| Implementatiemethode | Stappen |
|--- |--- |
| Tags in Adobe Experience Platform | Ervan uitgaande dat u de geïnstalleerde uitbreiding van Adobe Analytics hebt, voeg de volgende veranderlijke definitie van contextgegevens aan de redacteur van de douanecode binnen de configuratie van de Actie van een Regel toe: <br/>`s.contextData['cm.ssf'] = '1'` <br/> Nota: bepaal de contextgegevensvariabele en plaats het aan 1 als een klant niet aan gerichte marketing toestaat. Plaats de `contextdata` variabele aan *0* voor klanten die aan gerichte marketing goedkeurden. |
| AppMeasurement | Voeg de de veranderlijke definitie van contextgegevens aan het AppMeasurement.js- dossier toe: <br/>`s.contextData['cm.ssf'] = '1'` <br/> Nota: bepaal de contextgegevensvariabele en plaats het aan 1 als een klant niet aan gerichte marketing toestaat. Stel de variabele contextdata in op 0 voor klanten die hebben ingestemd met gerichte marketing. |

## Rapportage (optioneel) {#section_6AD4028EC11C4DABA2A34469DDC99E89}

U kunt Adobe Analytics gebruiken om te melden hoeveel van uw verkeer op toestemming gebaseerd is en dientengevolge door:sturen server-kant tegenover hoeveel van uw verkeer niet toestemming gebaseerd is en niet aan Adobe Audience Manager is doorgestuurd.

Om dit type van rapportering te vormen, kaart de nieuwe contextvariabele aan een variabele van het douaneverkeer (steun) via verwerkingsregels. Dit doen

1. Implementeer de variabele &quot;cm.ssf&quot; (zoals hierboven weergegeven).
1. [ laat prop toe.](/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md)
1. Gebruik verwerkingsregels om de contextvariabele toe te wijzen aan de eigenschap prop.

   1. Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** en selecteer een rapportsuite.
   1. Klik op **[!UICONTROL Edit Report Suite]** > **[!UICONTROL General]** > **[!UICONTROL Processing Rules]** .
   1. Klikken **[!UICONTROL Add Rule.]**
   1. Bij **[!UICONTROL Always Execute]** overschrijft u de waarde van de eigenschap die u hebt ingeschakeld met de contextvariabele &quot;cm.ssf(Context Data)&quot;.
   1. Klik op **[!UICONTROL Save]**.
