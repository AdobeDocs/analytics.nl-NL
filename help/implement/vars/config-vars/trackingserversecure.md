---
title: trackingServerSecure
description: Het domein dat wordt gebruikt om gegevens via HTTPS naar Adobe te verzenden.
feature: Appmeasurement Implementation
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
role: Admin, Developer
source-git-commit: 7918b18e73618368543a996ca121b64b7afb33ab
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# trackingServerSecure

De variabele `trackingServerSecure` bepaalt het domein dat AppMeasurement gebruikt om gegevens via HTTPS naar Adobe te verzenden. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

Vóór de [ Dienst van de Identiteit van Adobe Experience Cloud ](https://experienceleague.adobe.com/en/docs/id-service/using/home), bepaalde deze variabele ook waar de derdekoekjes werden geplaatst. Adobe raadt ten zeerste aan de id-service waar mogelijk in alle implementaties te gebruiken.

## Edge-domein met de extensie Web SDK

Het Web SDK gebruikt [!UICONTROL Edge domain] om zowel de het Volgen Server als Veilige het Volgen Server te behandelen. U kunt de gewenste [!UICONTROL Edge domain] -waarde instellen wanneer u de extensie Web SDK configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Selecteer de gewenste eigenschap tag.
1. Ga naar de tab [!UICONTROL Extensions] en selecteer vervolgens de knop **[!UICONTROL Configure]** onder [!UICONTROL Adobe Experience Platform Web SDK] .
1. Stel het gewenste tekstveld in **[!UICONTROL Edge domain]** .

Zie [ de uitbreiding van SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html) in de documentatie van SDK van het Web voor meer informatie vormen.

>[!TIP]
>
>Als uw organisatie vanuit een AppMeasurement- of analytische extensie-implementatie naar de Web SDK gaat, kan voor dit veld dezelfde waarde worden gebruikt als in `trackingServerSecure` (of `trackingServer` ).

## Edge-domein handmatig implementeren van de Web SDK

Vorm SDK gebruikend [`edgeDomain` ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/edgedomain). Het veld is een tekenreeks die het domein bepaalt waarnaar gegevens moeten worden verzonden.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## SSL-traceringsserver met de Adobe Analytics-extensie

[!UICONTROL SSL Tracking Server] is een veld onder de accordeon van [!UICONTROL General] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Selecteer de gewenste eigenschap tag.
1. Ga naar de tab [!UICONTROL Extensions] en selecteer vervolgens de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Vouw de accordeon [!UICONTROL General] uit, zodat het veld [!UICONTROL SSL Tracking Server] zichtbaar wordt.

Als dit veld niet wordt ingevuld, wordt standaard de waarde in [!UICONTROL Tracking Server] gebruikt. Als zowel [!UICONTROL SSL Tracking Server] als [!UICONTROL Tracking Server] leeg zijn, wordt standaard `[rsid].data.adobedc.net` gebruikt.

## s.trackingServerSecure in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.trackingServerSecure` is een tekenreeks die het domein bevat dat gegevens naar Adobe moet verzenden. Het is slechts domein; weglaat protocol, weg, haven, en schuine strepen. Als deze variabele leeg is, wordt de waarde in de variabele `s.trackingServer` gebruikt. Als zowel `s.trackingServerSecure` als `s.trackingServer` leeg zijn, wordt standaard `[rsid].2o7.net` gebruikt.

```js
// Example value when participating in the Adobe-managed certificate program
s.trackingServerSecure = "data.example.com";

// Example value sending data directly to Adobe
s.trackingServerSecure = "example.data.adobedc.net";
```

## Overwegingen bij het bepalen van de waarde voor `trackingServerSecure`

De waarde die u gebruikt voor `trackingServerSecure` (of `edgeDomain` ), is afhankelijk van verschillende factoren:

* Uw deelname aan het [ Adobe-Beheerde certificaatprogramma ](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/adobe-managed-cert)
* Als u de [ uitgevoerde dienst van de Identiteit van Adobe Experience Cloud ](https://experienceleague.adobe.com/en/docs/id-service/using/home) en correct opstelling hebt

**als uw organisatie aan het Adobe-Beheerde certificaatprogramma** deelneemt, plaats de waarde aan het eerste partijdomein dat toen vestiging het certificaat werd geselecteerd. Deze waarde is doorgaans een subdomein dat eigendom is van uw organisatie. Bijvoorbeeld `data.example.com` . CNAME-records in uw organisatie leiden die gegevens om naar Adobe.

**als het niet deelnemen aan het certificaatprogramma**, plaats de waarde aan subdomain van `data.adobedc.net`. Adobe raadt u aan de bedrijfs-id van uw organisatie te gebruiken voor consistentie. Bijvoorbeeld `example.data.adobedc.net` . Gebruik de volgende stappen om uw bedrijfs-id te bepalen:

1. Login aan [ experience.adobe.com ](https://experience.adobe.com) gebruikend uw geloofsbrieven van Adobe ID.
1. Druk overal in de Experience Cloud-interface op `[Cmd]` + `[I]` (iOS) of `[Ctrl]` + `[I]` (Windows).
1. Er verschijnt een **[!UICONTROL User data debugger]** . Selecteer het tabblad **[!UICONTROL Assigned orgs]**. 
1. Breid de gewenste organisatie IMS uit.
1. Zoek het veld **[!UICONTROL Tenant]** . Deze waarde is het aanbevolen subdomein van `data.adobedc.net` om te gebruiken.

>[!NOTE]
>
>Gebruik geen subdomeinen die dieper zijn dan `example.data.adobedc.net` . `custom.example.data.adobedc.net` is bijvoorbeeld geen geldige trackingserver.

Oudere implementaties kunnen waarden als `sc.omtrdc.net` of `2o7.net` hebben. Deze werden voornamelijk gebruikt in eerdere versies van Adobe Analytics en zijn nog steeds geldig.

Adobe adviseert hoogst het handhaven van deze informatie in het document van het a [ oplossingsontwerp ](../../prepare/solution-design.md) voor consistentie over uw organisatie.

## Ramingen voor het niet gebruiken van de dienst van identiteitskaart van de Bezoeker

Adobe adviseert sterk gebruikend de [ dienst van de Identiteit van Adobe Experience Cloud ](https://experienceleague.adobe.com/en/docs/id-service/using/home) in alle implementaties. De id-service kan op verschillende manieren worden geïmplementeerd:

* Handmatige AppMeasurement-implementaties gebruiken `VisitorAPI.js` en roepen de methode `getInstance` aan. Zie [ de Dienst van de Identiteit van Experience Cloud voor Analytics ](https://experienceleague.adobe.com/en/docs/id-service/using/implementation/setup-analytics) voor meer informatie uitvoeren.
* De uitvoeringen die de de markeringsuitbreiding gebruiken van Adobe Analytics gebruiken de [ de dienstmarkeringsuitbreiding van identiteitskaart van Adobe Experience Cloud ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/id-service/overview). Zodra toegevoegd, wordt geen extra configuratie vereist.
* Implementaties die om het even welke vorm van het Web SDK (`alloy.js` of de de markeringsuitbreiding van SDK van het Web) gebruiken hebben reeds de dienst van identiteitskaart binnen wordt gebakken. Er is geen configuratie vereist behalve het instellen van de waarde `edgeDomain` .

**als uw implementatie niet de identiteitsdienst** gebruikt, overweeg de volgende gevolgen aan uw implementatie:

* Als u de identiteitsservice niet gebruikt, bepaalt `trackingServerSecure` de locatie van het cookie. Door deze variabele in te stellen op een domein van derden, dwingt u AppMeasurement een fallback-cookie te gebruiken, aangezien de meeste moderne browsers cookies van derden afwijzen.
* Het bijhouden van interne koppelingen en Activity Map zijn mogelijk minder betrouwbaar.
