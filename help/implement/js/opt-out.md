---
title: Koppelingen uitschakelen
description: Leer hoe u de optie om te weigeren koppelingen maakt voor bezoekers van uw site.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Optie-outkoppelingen implementeren

>[!IMPORTANT] Adobe raadt u aan de aanmeldingsservice te gebruiken, vooral voor organisaties die zich bezighouden met GDPR-regels. Zie [Inschakelen-serviceoverzicht](https://docs.adobe.com/content/help/en/id-service/using/implementation/opt-in-service/optin-overview.html) in de gebruikershandleiding van Experience Cloud Identity Service.

Sommige bezoekers van uw website hebben liever geen informatie over het bladeren in uw gegevensset. Adobe biedt de mogelijkheid om bezoekers van uw website de mogelijkheid te bieden zich af te melden van de gegevens die worden verzameld. Aan alle implementatietypen wordt tegemoetgekomen; uw organisatie is verantwoordelijk voor uw eigen privacybeleid en voor het naleven van uw ondertekende voorwaarden.

Wanneer een bezoeker een opt-out-URL bereikt, wordt hem gevraagd een uitschakelcookie te installeren. Als een gebruiker ervoor kiest om niet te worden gevolgd en een uitschakelcookie wordt ingesteld, worden gegevens nog steeds naar Adobe-servers verzonden door het JavaScript-bestand. Deze gegevens worden echter niet verwerkt of opgenomen in rapporten.

>[!TIP] Adobe biedt ook privacy-instellingen per rapportsuite. Zie [Privacy-instellingen](../../admin/admin/privacy-settings.md) in de gebruikershandleiding voor Admin.

## URL uitschakelen

De pagina om te weigeren voor uw organisatie is afhankelijk van de waarde van de [`trackingServer`](../vars/config-vars/trackingserver.md) variabele in uw implementatie.

* In Adobe Experience Platform Launch:
   1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) en klik op de gewenste eigenschap.
   2. Klik op het [!UICONTROL Extensions] tabblad en klik vervolgens [!UICONTROL Configure] onder Adobe Analytics.
   3. Klik op de [!UICONTROL General] accordeon en noteer de [!UICONTROL Tracking Server] waarde.

* In een JavaScript-implementatie:
   1. Open op uw webserver het bestand AppMeasurement.js dat op uw site wordt gebruikt, in een code- of teksteditor.
   2. Noteer de waarde van de `trackingServer` variabele.

* Werken met [Adobe Experience Cloud Debugger](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html):
   1. Navigeer naar uw site met de Chrome-browser.
   2. Open de Experience Cloud Debugger en ga naar de [!UICONTROL Network tab].
   3. Noteer de [!UICONTROL Request URL - Hostname] waarde.

Zodra u het `trackingServer` domein van uw implementatie hebt gevonden, voeg de weg `/optout.html` aan het eind toe. Bijvoorbeeld:

* Cookies van andere bedrijven: `https://example.sc.omtrdc.net/optout.html`
* Eerste cookies: `https://stats.example.com/optout.html`

## Parameters van queryreeks uitschakelen

Er zijn instellingen die u automatisch op deze pagina kunt laden met querytekenreeksen.

### Landinstelling

Schakel automatisch de taal van de opt-out-pagina uit door de parameter voor de `locale` queryreeks op te nemen. Wijs deze parameter van het vraagkoord één van de volgende waarden toe:

* nl_NL (Engels, standaard)
* bg_BG (Bulgaars)
* zh_CN (Vereenvoudigd Chinees)
* zh_TW (Traditioneel Chinees)
* cs_CZ (Tsjechisch)
* da_NK (Deens)
* nl_NL (Nederlands)
* et_EE (Ests)
* fi_FI (Fins)
* fr_FR (Frans)
* de_DE (Duits)
* el_GR (Grieks)
* it_IT (Italiaans)
* jp_JP (Japans)
* ko_KR (Koreaans)
* lv_LV (Lets)
* lt_LT (Litouws)
* nb_NO (Noors)
* pl_PL (Pools)
* pt_BR (Portugees)
* sk_SK (Slowaaks)
* es_ES (Spaans)

Hiermee wordt bijvoorbeeld de pagina om te weigeren in het Koreaans geladen. `https://example.sc.omtrdc.net/optout.html?locale=ko_KR`

>[!TIP] De waarde van de `en_US` querytekenreeks is niet vereist, omdat de pagina standaard in het Engels wordt geladen.

### Popup

Hiermee voegt u een knop Venster sluiten aan de pagina toe, zodat de optiepagina een pop-upvenster kan worden. Gebruik de parameter van het `popup` vraagkoord, en geef het een waarde van `1`.

Laadt bijvoorbeeld de pagina met de optie Weigeren met de knop Venster sluiten. `https://example.sc.omtrdc.net/optout.html?popup=1`

>[!NOTE] Historisch forceerde deze parameter van het vraagkoord een popup venster. De meeste moderne browsers geven echter controle over popups aan de eindgebruiker.

### Weigeren met één klik

Hiermee kan de gebruiker zich direct afmelden voor bijhouden. Voeg de twee parameters van het vraagkoord toe `opt_out` en `confirm_change`, die elk een waarde van geven `1`.

Het uitschakelcookie wordt bijvoorbeeld `https://example.sc.omtrdc.net/optout.html?opt_out=1&confirm_change=1` onmiddellijk op de pagina van de bezoeker geïnstalleerd.

### Aanmelden met één klik

Hiermee kan de gebruiker onmiddellijk terugkeren naar het bijhouden van bestanden door het uitschakelcookie te verwijderen. Voeg de twee parameters van het vraagkoord toe `opt_in` en `confirm_change`, die elk een waarde van geven `1`.

Hiermee verwijdert u bijvoorbeeld `https://example.sc.omtrdc.net/optout.html?opt_in=1&confirm_change=1` onmiddellijk het uitschakelcookie voor de bezoeker.
