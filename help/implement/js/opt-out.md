---
title: Koppelingen uitschakelen
description: Leer hoe u de optie om te weigeren koppelingen maakt voor bezoekers van uw site.
exl-id: 08b8c7cc-28c6-45e3-ab44-77471eea8ef1
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Opt-outkoppelingen implementeren

>[!IMPORTANT]
>
>Adobe beveelt aan de opt-in-dienst te gebruiken, met name voor organisaties die zich bezighouden met de GDPR-regelgeving. Zie [Inschakelen-serviceoverzicht](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html) in de gebruikershandleiding voor de Experience Cloud-identiteitsservice.

Sommige bezoekers van uw website hebben liever geen informatie over het bladeren in uw gegevensset. Adobe biedt bezoekers van uw website de mogelijkheid om te weigeren dat hun gegevens worden verzameld. Aan alle implementatietypen wordt tegemoetgekomen; uw organisatie is verantwoordelijk voor uw eigen privacybeleid en voor het naleven van uw ondertekende voorwaarden.

Wanneer een bezoeker een opt-out-URL bereikt, wordt hem gevraagd een uitschakelcookie te installeren. Als een gebruiker ervoor kiest om niet te worden gevolgd en een uitschakelcookie wordt ingesteld, worden de gegevens in het JavaScript-bestand nog steeds naar de Adobe-servers verzonden. Deze gegevens worden echter niet verwerkt of opgenomen in rapporten.

>[!TIP]
>
>Adobe biedt ook privacy-instellingen per rapportsuite. Zie [Privacy-instellingen](../../admin/admin/privacy-settings.md) in de gebruikershandleiding voor Admin.

## URL uitschakelen

De pagina om te weigeren voor uw organisatie is afhankelijk van de variabele [`trackingServer`](../vars/config-vars/trackingserver.md) waarde in uw implementatie.

* In de UI voor gegevensverzameling:
   1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
   1. Klik op de gewenste eigenschap.
   1. Klik op de tab [!UICONTROL Extensions] en klik vervolgens onder Adobe Analytics op [!UICONTROL Configure].
   1. Klik op de accordeon [!UICONTROL General] en noteer de waarde [!UICONTROL Tracking Server].

* In een JavaScript-implementatie:
   1. Open op uw webserver het bestand AppMeasurement.js dat op uw site wordt gebruikt, in een code- of teksteditor.
   1. Noteer de waarde van de variabele `trackingServer`.

* Met de [Adobe Experience Cloud-foutopsporing](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html):
   1. Navigeer naar uw site met de Chrome-browser.
   1. Open de Experience Cloud Debugger en ga naar [!UICONTROL Network tab].
   1. Noteer de waarde [!UICONTROL Request URL - Hostname].

Zodra u het `trackingServer` domein van uw implementatie hebt gevonden, voeg de weg `/optout.html` aan het eind toe. Bijvoorbeeld:

* Cookies van andere bedrijven: `https://example.data.adobedc.net/optout.html`
* Eerste cookies: `https://stats.example.com/optout.html`

## Parameters van queryreeks uitschakelen

Er zijn instellingen die u automatisch op deze pagina kunt laden met querytekenreeksen.

### Landinstelling

Schakel automatisch de taal van de opt-out pagina door de `locale` parameter van het vraagkoord te omvatten. Wijs deze parameter van het vraagkoord één van de volgende waarden toe:

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

`https://example.data.adobedc.net/optout.html?locale=ko_KR` laadt bijvoorbeeld de pagina om te weigeren in het Koreaans.

>[!TIP]
>
>De `en_US` waarde van het vraagkoord wordt niet vereist, aangezien de pagina in het Engels door gebrek laadt.

### Popup

Hiermee voegt u een knop Venster sluiten aan de pagina toe, zodat de optiepagina een pop-upvenster kan worden. Gebruik de `popup` parameter van het vraagkoord, en geef het een waarde van `1`.

`https://example.data.adobedc.net/optout.html?popup=1` laadt bijvoorbeeld de pagina om te weigeren met de knop Venster sluiten.

>[!NOTE]
>
>Historisch forceerde deze parameter van het vraagkoord een popup venster. De meeste moderne browsers geven echter controle over popups aan de eindgebruiker.

### Weigeren met één klik

Hiermee kan de gebruiker zich direct afmelden voor bijhouden. Voeg de twee parameters van het vraagkoord `opt_out` en `confirm_change` toe, die elk een waarde van `1` geven.

`https://example.data.adobedc.net/optout.html?opt_out=1&confirm_change=1` installeert bijvoorbeeld onmiddellijk het uitschakelcookie op de pagina van de bezoeker.

### Aanmelden met één klik

Hiermee kan de gebruiker onmiddellijk terugkeren naar het bijhouden van bestanden door het uitschakelcookie te verwijderen. Voeg de twee parameters van het vraagkoord `opt_in` en `confirm_change` toe, die elk een waarde van `1` geven.

`https://example.data.adobedc.net/optout.html?opt_in=1&confirm_change=1` verwijdert bijvoorbeeld onmiddellijk het uitschakelcookie voor de bezoeker.
