---
title: Koppelingen uitschakelen
description: Leer hoe u de optie om te weigeren koppelingen maakt voor bezoekers van uw site.
feature: Implementation Basics
exl-id: 08b8c7cc-28c6-45e3-ab44-77471eea8ef1
hide: true
hidefromtoc: true
role: Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 0%

---

# Optie-out-koppelingen implementeren

>[!IMPORTANT]
>
> Dit artikel verstrekt **klanten van Adobe Analytics die (van plan zijn om) Adobe Analytics** op hun website met instructies op uit te voeren hoe te om websitegebruikers van opt-out verbindingen te voorzien. <p><p>
><p>-ERR:REF-NOT-FOUND-<p>-ERR:REF-NOT-FOUND-> Als u **een website bezoekt die Adobe Analytics** heeft uitgevoerd, en u wilt uit kiezen, **<span style="color:red">is dit artikel NIET voor u</span>**. Gelieve te zien {de Keuzen van de Privacy van 0} Adobe [ om te controleren hoe Adobe uw informatie gebruikt.](https://www.adobe.com/privacy/opt-out.html)

Sommige bezoekers van uw website hebben liever geen informatie over het bladeren in uw gegevensset. Adobe biedt de mogelijkheid om bezoekers van uw website de mogelijkheid te bieden zich af te melden voor het analyseren van hun gegevens.

Koppelingen met de optie om te weigeren zijn een manier waarop bezoekers van uw website hun gegevens kunnen weglaten uit de rapportage Analytics. Deze verbindingen zijn beperkt tot de implementaties van AppMeasurement; Adobe adviseert in plaats daarvan het gebruiken van de [ opt-in dienst van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=nl-NL). De open-in dienst is robuuster en werkt over veelvoudige producten van Adobe Experience Cloud, met inbegrip van Adobe Analytics en AppMeasurement.

Wanneer een bezoeker een opt-out-URL bereikt, wordt hem gevraagd een uitschakelcookie te installeren. Als een gebruiker ervoor kiest om niet te worden gevolgd en een uitschakelcookie wordt ingesteld, blijft AppMeasurement gegevens verzenden naar Adobe. Deze gegevens worden echter niet verwerkt of opgenomen in rapporten.

>[!TIP]
>
>Adobe biedt ook privacy-instellingen per rapportsuite. Zie [ Montages van de Privacy ](/help/admin/tools/manage-rs/edit-settings/general/privacy-settings.md) in de Admin gebruikersgids.

## URL uitschakelen

De pagina om te weigeren voor uw organisatie is afhankelijk van de waarde van de variabele [`trackingServer`](../vars/config-vars/trackingserver.md) in uw implementatie.

* In de extensie Analytics:
   1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
   1. Klik op de gewenste tageigenschap.
   1. Klik op de tab [!UICONTROL Extensions] en klik vervolgens op [!UICONTROL Configure] onder Adobe Analytics.
   1. Klik op de accordeon [!UICONTROL General] en noteer de waarde [!UICONTROL Tracking Server] .

* In een JavaScript-implementatie:
   1. Open op uw webserver het AppMeasurement.js-bestand dat op uw site wordt gebruikt, in een code- of teksteditor.
   1. Noteer de waarde van de variabele `trackingServer` .

* Gebruikend [ Debugger van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/experience-platform/debugger/home.html?lang=nl-NL):
   1. Navigeer naar uw site met de Chrome-browser.
   1. Open de Experience Cloud Debugger en ga vervolgens naar de [!UICONTROL Network tab] .
   1. Noteer de waarde [!UICONTROL Request URL - Hostname] .

Nadat u het domein `trackingServer` van uw implementatie hebt gevonden, voegt u het pad `/optout.html` aan het einde toe. Bijvoorbeeld:

* Cookies van andere bedrijven: `https://example.data.adobedc.net/optout.html`
* First-party cookies: `https://stats.example.com/optout.html`

## Parameters van queryreeks uitschakelen

Er zijn instellingen die u automatisch op deze pagina kunt laden met querytekenreeksen.

### Landinstelling

Schakel automatisch de taal van de optiepagina over door de parameter voor de querytekenreeks `locale` op te nemen. Wijs deze parameter van het vraagkoord één van de volgende waarden toe:

* `en_US` (Engels, standaard)
* `bg_BG` (Bulgaarse)
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
* `nb_NO` (Noorse)
* `pl_PL` (Pools)
* `pt_BR` (Portugees)
* `sk_SK` (Slowaaks)
* `es_ES` (Spaans)

`https://example.data.adobedc.net/optout.html?locale=ko_KR` laadt bijvoorbeeld de pagina om te weigeren in het Koreaans.

### Popup

Hiermee voegt u een knop Venster sluiten aan de pagina toe, zodat de optiepagina een pop-upvenster kan worden. Gebruik de parameter van de `popup` querytekenreeks en geef deze de waarde `1` .

`https://example.data.adobedc.net/optout.html?popup=1` laadt bijvoorbeeld de pagina met de optie Weigeren met de knop Venster sluiten.

>[!NOTE]
>
>Historisch forceerde deze parameter van het vraagkoord een popup venster. De meeste moderne browsers geven echter controle over popups aan de eindgebruiker.

### Weigeren met één klik

Hiermee kan de gebruiker zich direct afmelden voor bijhouden. Voeg de twee parameters voor de queryreeks `opt_out` en `confirm_change` toe en geef elk de waarde `1` .

`https://example.data.adobedc.net/optout.html?opt_out=1&confirm_change=1` installeert bijvoorbeeld onmiddellijk het uitschakelcookie op de pagina van de bezoeker.

### Aanmelden met één klik

Hiermee kan de gebruiker onmiddellijk terugkeren naar het bijhouden van bestanden door het uitschakelcookie te verwijderen. Voeg de twee parameters voor de queryreeks `opt_in` en `confirm_change` toe en geef elk de waarde `1` .

`https://example.data.adobedc.net/optout.html?opt_in=1&confirm_change=1` verwijdert bijvoorbeeld onmiddellijk het uitschakelcookie voor de bezoeker.
