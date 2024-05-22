---
title: Koppelingen uitschakelen
description: Leer hoe u de optie om te weigeren koppelingen maakt voor bezoekers van uw site.
feature: Implementation Basics
exl-id: 08b8c7cc-28c6-45e3-ab44-77471eea8ef1
hide: true
hidefromtoc: true
role: Developer
source-git-commit: 48f1974a0c379a4e619d9a04ae80e43cce9527c1
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 0%

---

# Optie-out-koppelingen implementeren

>[!IMPORTANT]
>
> Dit artikel biedt **Adobe Analytics-klanten die Adobe Analytics willen implementeren** op hun website instructies te geven over hoe gebruikers van websites kunnen kiezen voor de optie om te weigeren. <p><p>
> Als u **bezoeken van een website die Adobe Analytics heeft geïmplementeerd** en wilt u weigeren, **<span style="color:red">dit artikel is NIET voor u</span>**. Zie [Privacykeuzen Adobe](https://www.adobe.com/privacy/opt-out.html) om te bepalen hoe de Adobe uw informatie gebruikt.

Sommige bezoekers van uw website hebben liever geen informatie over het bladeren in uw gegevensset. Adobe biedt de mogelijkheid om bezoekers van uw website de mogelijkheid te bieden zich af te melden voor de analyse van hun gegevens.

Koppelingen met de optie om te weigeren zijn een manier waarop bezoekers van uw website hun gegevens kunnen weglaten uit de rapportage Analytics. Deze koppelingen zijn beperkt tot implementaties van AppMeasurementen; Adobe raadt aan de [Adobe Experience Cloud Inschakelen-service](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html) in plaats daarvan. De open-in dienst is robuuster en werkt over veelvoudige producten van Adobe Experience Cloud, met inbegrip van Adobe Analytics en AppMeasurement.

Wanneer een bezoeker een opt-out-URL bereikt, wordt hem gevraagd een uitschakelcookie te installeren. Als een gebruiker ervoor kiest om niet te worden gevolgd en een uitschakelcookie wordt ingesteld, worden de gegevens door het AppMeasurement nog steeds naar de Adobe verzonden. Deze gegevens worden echter niet verwerkt of opgenomen in rapporten.

>[!TIP]
>
>Adobe biedt ook privacy-instellingen per rapportsuite. Zie [Privacy-instellingen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/privacy-settings.md) in de handleiding voor Admin-gebruikers.

## URL uitschakelen

De pagina om te weigeren voor uw organisatie is afhankelijk van de [`trackingServer`](../vars/config-vars/trackingserver.md) variabele waarde in uw implementatie.

* In de extensie Analytics:
   1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
   1. Klik op de gewenste tageigenschap.
   1. Klik op de knop [!UICONTROL Extensions] tab, en klik vervolgens op [!UICONTROL Configure] onder Adobe Analytics.
   1. Klik op de knop [!UICONTROL General] en noteer de [!UICONTROL Tracking Server] waarde.

* In een JavaScript-implementatie:
   1. Open op uw webserver het bestand AppMeasurement.js dat op uw site wordt gebruikt, in een code- of teksteditor.
   1. Noteer de `trackingServer` variabele waarde.

* Met de [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/experience-platform/debugger/home.html):
   1. Navigeer naar uw site met de Chrome-browser.
   1. Open het Experience Cloud Debugger en ga naar de [!UICONTROL Network tab].
   1. Noteer de [!UICONTROL Request URL - Hostname] waarde.

Zodra u de `trackingServer` domein, pad toevoegen `/optout.html` tot het einde toe. Bijvoorbeeld:

* Cookies van andere bedrijven: `https://example.data.adobedc.net/optout.html`
* Eerste cookies: `https://stats.example.com/optout.html`

## Parameters van queryreeks uitschakelen

Er zijn instellingen die u automatisch op deze pagina kunt laden met querytekenreeksen.

### Landinstelling

Schakel automatisch de taal van de optiepagina uit door de `locale` querytekenreeksparameter. Wijs deze parameter van het vraagkoord één van de volgende waarden toe:

* `en_US` (Engels, standaard)
* `bg_BG` (Bulgaars)
* `zh_CN` (Vereenvoudigd Chinees)
* `zh_TW` (Traditioneel Chinees)
* `cs_CZ` (Tsjechisch)
* `da_NK` (Deens)
* `nl_NL` (Nederlands)
* `et_EE` (Ests)
* `fi_FI` (Fins)
* `fr_FR` (Frans)
* `de_DE` (Duits)
* `el_GR` (Grieks)
* `it_IT` (Italiaans)
* `jp_JP` (Japans)
* `ko_KR` (Koreaans)
* `lv_LV` (Lets)
* `lt_LT` (Litouws)
* `nb_NO` (Noors)
* `pl_PL` (Pools)
* `pt_BR` (Portugees)
* `sk_SK` (Slowaaks)
* `es_ES` (Spaans)

Bijvoorbeeld: `https://example.data.adobedc.net/optout.html?locale=ko_KR` laadt de pagina voor niet-deelname in het Koreaans.

### Popup

Hiermee voegt u een knop Venster sluiten aan de pagina toe, zodat de optiepagina een pop-upvenster kan worden. Gebruik de `popup` query string parameter, en geef deze de waarde van `1`.

Bijvoorbeeld: `https://example.data.adobedc.net/optout.html?popup=1` Hiermee laadt u de pagina met de optie Weigeren met de knop Venster sluiten.

>[!NOTE]
>
>Historisch forceerde deze parameter van het vraagkoord een popup venster. De meeste moderne browsers geven echter controle over popups aan de eindgebruiker.

### Weigeren met één klik

Hiermee kan de gebruiker zich direct afmelden voor bijhouden. De twee parameters van de queryreeks toevoegen `opt_out` en `confirm_change`, waarbij elk een waarde van `1`.

Bijvoorbeeld: `https://example.data.adobedc.net/optout.html?opt_out=1&confirm_change=1` installeert de uitschakelcookie onmiddellijk op de pagina van de bezoeker.

### Aanmelden met één klik

Hiermee kan de gebruiker onmiddellijk terugkeren naar het bijhouden van bestanden door het uitschakelcookie te verwijderen. De twee parameters van de queryreeks toevoegen `opt_in` en `confirm_change`, waarbij elk een waarde van `1`.

Bijvoorbeeld: `https://example.data.adobedc.net/optout.html?opt_in=1&confirm_change=1` verwijdert onmiddellijk het uitschakelcookie voor de bezoeker.
