---
title: Aan de slag met Activity Map
description: Ga aan de slag met de Activity Map-overlay en -afmetingen.
feature: Activity Map
role: User, Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
source-git-commit: bfafc1f8eddf82b34fb45e3d6197213f0cee0d97
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# Aan de slag met Activity Map

De Activity Map in Adobe Analytics omvat vier belangrijke elementen:

* **Reeks die van het Rapport** plaatst: U moet Activity Map in de montages van de Reeks van het Rapport toelaten. Wanneer toegelaten, leidt de rapportreeks tot verscheidene gereserveerde variabelen voor Activity Map dimensies en metriek.
* **Uitvoering**: Verzamel de gegevens van de Activity Map op uw website of bezit. Door de manier aan te passen waarop gegevens worden verzameld, kunt u de kwaliteit en ervaring van rapporten verbeteren.
* **de afmetingen en metriek van Workspace**: Wanneer uw implementatie correct wordt gevormd, kunt u de dimensies en metriek van de Activity Map in Analysis Workspace gebruiken.
* **Bedekking**: de Adobe biedt een browser uitbreiding aan om de gegevens van de Activity Map in de context van uw website te bekijken.

## Instelling van rapportsuite inschakelen

Voor een rapportsuite moet rapportage van de Activity Map zijn ingeschakeld voordat u kunt beginnen met het verzamelen van gegevens. Als uw implementatie de gegevens van de Activity Map naar een rapportreeks verzendt zonder toegelaten rapportering van de Activity Map, zijn de gegevens van de Activity Map niet inbegrepen in de slag.

**[!UICONTROL Admin]** > **[!UICONTROL Report suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit settings]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map reporting]** > **[!UICONTROL Enable Activity Map Reports]**

Als u rapporten over Activity Mappen inschakelt, worden er verschillende gereserveerde achtergrondvariabelen gemaakt. Zie [ Activity Map die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/activity-map.md) meldt in de admin van Adobe Analytics gids voor meer informatie.

## Code-installatie

Uw implementatie moet correct zijn geconfigureerd om gegevens van de Activity Map naar de Adobe te verzenden.

+++Web SDK-tagextensie

Voor het verzamelen van Activity Map-gegevens is de extensie **[!UICONTROL Adobe Experience Platform Web SDK]** v2.23 of hoger vereist. Extensieversies tot v2.16 bieden beperkte ondersteuning. Deze vorige extensieversies verzenden de gegevens van de Activity Map in een andere gebeurtenis dan de overige gegevens. Deze extra gebeurtenis vergroot het aantal hits dat u naar Adobe Analytics of Adobe Experience Platform verzendt.

Met de configuratie-instelling **[!UICONTROL Click data collection]** wordt de gegevensverzameling van de Activity Map afgehandeld. Deze instelling is standaard standaard ingeschakeld. U kunt controleren om ervoor te zorgen dat het in de configuratiemontages van de uitbreiding wordt toegelaten:

1. Login aan [ experience.adobe.com ](https://experience.adobe.com)
1. Selecteer **[!UICONTROL Data Collection]** in het snelmenu of de productkiezer rechtsboven.
1. Selecteer **[!UICONTROL Tags]** in het navigatiemenu aan de linkerkant.
1. Selecteer de gewenste tag die u wilt bewerken.
1. Selecteer **[!UICONTROL Extensions]** in het navigatiemenu aan de linkerkant.
1. Selecteer **[!UICONTROL Adobe Experience Platform Web SDK]** in de lijst met geïnstalleerde extensies en selecteer vervolgens **[!UICONTROL Configure]** aan de rechterkant.
1. Zoek de sectie met het label [!UICONTROL Data Collection] en controleer of het selectievakje **[!UICONTROL Enable click data collection]** is ingeschakeld.
1. Selecteer **[!UICONTROL Save]** .
1. Indien nodig, bouw uw veranderingen in een bibliotheek en publiceer uw veranderingen in productie.

Zie [ de de markeringsuitbreiding van SDK van het Web ](https://experienceleague.adobe.com/nl/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#data-collection) voor meer informatie vormen.

+++

+++Web SDK JavaScript-bibliotheek (`alloy.js`)

Voor het verzamelen van gegevens voor Activity Mappen is de Web SDK JavaScript-bibliotheek v2.20 of hoger vereist. Bibliotheekversies tot versie 2.15 bieden beperkte ondersteuning. Deze vorige bibliotheekversies verzenden de gegevens van de Activity Map in een afzonderlijke gebeurtenis van de rest van uw gegevens. Deze extra gebeurtenis vergroot het aantal hits dat u naar Adobe Analytics of Adobe Experience Platform verzendt.

De de configuratievariabele van SDK van het Web [`clickCollectionEnabled` ](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) behandelt de automatische inzameling van Activity Map gegevens. Deze optie is standaard ingeschakeld, tenzij deze expliciet is uitgeschakeld.

```js
alloy("configure", {
  datastreamId: "ebebf826-a01f-4458-8cec-ef61de241c93",
  orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg",
  clickCollectionEnabled: true
});
```

+++

+++Adobe Analytics-tagextensie

Met de configuratie-instelling **[!UICONTROL Use Activity Map]** wordt de gegevensverzameling van de Activity Map afgehandeld. Deze instelling is standaard standaard ingeschakeld. Deze is beschikbaar voor alle tagextensies versie 1.9.0 of hoger. U kunt controleren om ervoor te zorgen dat het in de configuratiemontages van de uitbreiding wordt toegelaten:

1. Login aan [ experience.adobe.com ](https://experience.adobe.com)
1. Selecteer **[!UICONTROL Data Collection]** in het snelmenu of de productkiezer rechtsboven.
1. Selecteer **[!UICONTROL Tags]** in het navigatiemenu aan de linkerkant.
1. Selecteer de gewenste tag die u wilt bewerken.
1. Selecteer **[!UICONTROL Extensions]** in het navigatiemenu aan de linkerkant.
1. Selecteer **[!UICONTROL Adobe Analytics]** in de lijst met geïnstalleerde extensies en selecteer vervolgens **[!UICONTROL Configure]** aan de rechterkant.
1. Controleer of het selectievakje **[!UICONTROL Use Activity Map]** is ingeschakeld.
1. Selecteer **[!UICONTROL Save]** .
1. Indien nodig, bouw uw veranderingen in een bibliotheek en publiceer uw veranderingen in productie.

Zie het [ de uitbreidingsoverzicht van Adobe Analytics ](https://experienceleague.adobe.com/nl/docs/experience-platform/tags/extensions/client/analytics/overview) voor meer informatie.

+++

+++Adobe Analytics JavaScript-bibliotheek (`AppMeasurement.js`)

De module van de Activity Map behandelt de gegevensinzameling van de Activity Map, en is inbegrepen met alle bibliotheken van het AppMeasurement v1.6 of later. U kunt het `AppMeasurement.js` -bestand controleren om te controleren of het is opgenomen.

1. Navigeer aan de [ Laatste versie van het AppMeasurement van Adobe Analytics ](https://github.com/adobe/appmeasurement/releases/latest) op GitHub.
1. Download het gecomprimeerde bibliotheekbestand van het AppMeasurement en open vervolgens `AppMeasurement.js` in het bibliotheekbestand.
1. De module Activity Map bevindt zich boven in dit bestand. Zorg ervoor dat deze module is opgenomen in de bibliotheek met AppMeasurementen die uw site gebruikt.

+++

## Beschikbare afmetingen

Wanneer de Activity Map voor zowel uw rapportreeks als implementatie wordt toegelaten, kunt u beginnen gebruikend de volgende dimensies in Analysis Workspace:

* [[!UICONTROL Activity Map Link]](/help/components/dimensions/activity-map-link.md)
* [[!UICONTROL Activity Map Region]](/help/components/dimensions/activity-map-region.md)
* [[!UICONTROL Activity Map Page]](/help/components/dimensions/activity-map-page.md)
* [[!UICONTROL Activity Map Link By Region]](/help/components/dimensions/activity-map-link-by-region.md)

## De browserextensie of invoegtoepassing downloaden en installeren

Naast de afmetingen die beschikbaar zijn in Analysis Workspace, kunt u ook de gegevens van de Activity Map weergeven als een overlay op uw website. Download en installeer de browserextensie of invoegtoepassing voor Activity Map om deze overlay weer te geven.

**[!UICONTROL Tools]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Download Activity Map]**

Met deze koppeling gaat u naar de door uw browser ondersteunde extensie of add-on Marketplace waar u deze kunt installeren. Nadat de extensie of invoegtoepassing is geïnstalleerd, wordt deze rechtsboven in uw browser weergegeven waar u zich kunt aanmelden en de overlay kunt inschakelen.
