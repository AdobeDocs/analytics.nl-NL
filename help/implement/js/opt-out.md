---
title: Koppelingen uitschakelen
description: Leer hoe u de optie om te weigeren koppelingen maakt voor bezoekers van uw site.
feature: Implementation Basics
exl-id: 08b8c7cc-28c6-45e3-ab44-77471eea8ef1
source-git-commit: 574c705a3127c82c947d0a1cba4beab63109d2c9
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---

# Opt-outkoppelingen implementeren

*Deze Help-pagina biedt Adobe Analytics-klanten de mogelijkheid om hun gebruikers de mogelijkheid te bieden zich af te melden. Als u geen Adobe Analytics-klant bent, raadpleegt u [Privacykeuzen Adobe](https://www.adobe.com/privacy/opt-out.html) om te bepalen hoe de Adobe uw informatie gebruikt.*

>[!IMPORTANT]
>
>Adobe beveelt aan gebruik te maken van de opt-in-dienst, met name voor organisaties die betrokken zijn bij de GDPR-regelgeving. Zie [Overzicht van de service voor aanmelden](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html) in de gebruikershandleiding van de Experience Cloud Identity Service.

Sommige bezoekers van uw website hebben liever geen informatie over het bladeren in uw gegevensset. Adobe biedt de mogelijkheid om bezoekers van uw website de mogelijkheid te bieden zich af te melden van de gegevens die worden verzameld. Alle implementatietypen zijn inbegrepen; uw organisatie is verantwoordelijk voor uw eigen privacybeleid en voor het naleven van uw ondertekende voorwaarden.

Wanneer een bezoeker een opt-out-URL bereikt, wordt hem gevraagd een uitschakelcookie te installeren. Als een gebruiker ervoor kiest om niet te worden gevolgd en een uitschakelcookie wordt ingesteld, worden de gegevens in het JavaScript-bestand nog steeds naar Adobe servers verzonden. Deze gegevens worden echter niet verwerkt of opgenomen in rapporten.

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

Bijvoorbeeld: `https://example.data.adobedc.net/optout.html?locale=ko_KR` laadt de pagina voor niet-deelname in het Koreaans.

>[!TIP]
>
>De `en_US` de waarde van het vraagkoord wordt niet vereist, aangezien de pagina in het Engels door gebrek laadt.

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
