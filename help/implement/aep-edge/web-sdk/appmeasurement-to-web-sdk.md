---
title: Migreren van AppMeasurement naar de Web SDK
description: Werk uw Adobe Analytics-implementatie bij van de AppMeasurement JavaScript-bibliotheek naar de Web SDK JavaScript-bibliotheek.
exl-id: c90246e8-0f04-4655-9204-33c0ef611b13
source-git-commit: bfafc1f8eddf82b34fb45e3d6197213f0cee0d97
workflow-type: tm+mt
source-wordcount: '1323'
ht-degree: 0%

---

# Migreren van AppMeasurement naar de Web SDK

Deze implementatieweg impliceert een methodische migratiebenadering om zich van een implementatie van het AppMeasurement aan een de bibliotheekimplementatie van SDK van het Web te bewegen JavaScript. Andere implementatiepaden worden op afzonderlijke pagina&#39;s behandeld:

* [ uitbreiding Analytics aan de uitbreiding van SDK van het Web ](analytics-extension-to-web-sdk.md): Neem een vlotte en methodische benadering om zich van de de markeringsuitbreiding van Adobe Analytics naar de de markeringsuitbreiding van SDK van het Web te bewegen. Deze benadering onderdrukt de behoefte om XDM te gebruiken tot uw organisatie klaar is om de diensten van Adobe Experience Platform, zoals Customer Journey Analytics te gebruiken. Gebruik het object `data` in plaats van het object `xdm` om gegevens naar de Adobe te verzenden.
* [ de bibliotheek van SDK van het Web JavaScript ](web-sdk-javascript-library.md): Een verse installatie van SDK van het Web die de bibliotheek van JavaScript van SDK van het Web gebruikt (`alloy.js`). Beheer de implementatie zelf in plaats van de gebruikersinterface voor tags te gebruiken. Hiervoor is de Adobe Analytics ExperienceEvent-veldgroep vereist, die typische analytische variabelen bevat die in uw XDM-schema moeten worden opgenomen.
* [ de markeringsuitbreiding van SDK van het Web ](web-sdk-tag-extension.md): Een verse installatie van SDK van het Web waar u de implementatie gebruikend markeringen in de Inzameling van Gegevens van Adobe Experience Platform beheert. Hiervoor is de Adobe Analytics ExperienceEvent-veldgroep vereist, die typische analytische variabelen bevat die in uw XDM-schema moeten worden opgenomen.

## Voordelen en nadelen van dit implementatiepad

Het gebruik van deze migratiebenadering heeft zowel voor- als nadelen. Let zorgvuldig op elke optie om te bepalen welke benadering het beste is voor uw organisatie.

| Voordelen | Nadelen |
| --- | --- |
| <ul><li>**gebruikt uw bestaande implementatie**: Terwijl deze benadering sommige implementatieveranderingen vereist, vereist het geen volledig nieuwe implementatie van kras. U kunt uw bestaande gegevenslaag en code met minimale veranderingen in implementatielogica gebruiken.</li><li>**vereist geen schema**: voor dit stadium van het migreren aan het Web SDK, hebt u geen schema XDM nodig. In plaats daarvan kunt u het object `data` vullen, dat gegevens rechtstreeks naar Adobe Analytics verzendt. Zodra de migratie naar SDK van het Web volledig is, dan kunt u een schema voor uw organisatie tot stand brengen en gegevensstroomafbeelding gebruiken om toepasselijke gebieden te bevolken XDM. Als een schema in dit stadium van het migratieproces werd vereist, zou uw organisatie worden gedwongen om een Adobe Analytics XDM schema te gebruiken. Het gebruik van dit schema maakt het voor uw organisatie moeilijker om uw eigen schema in de toekomst te gebruiken.</li></ul> | <ul><li>**de veranderingen van de Implementatie vereisen ontwikkelaarinterventie**: Als u veranderingen in uw implementatie van SDK van het Web wilt aanbrengen, moet u met uw ontwikkelingsteam werken om de code op uw plaats uit te geven. De benadering die [ aan de de markeringsuitbreiding van SDK van het Web ](analytics-extension-to-web-sdk.md) migreert vermijdt dit nadeel.</li><li>**Technische schuld van de Implementatie**: Aangezien deze benadering een gewijzigde vorm van uw bestaande implementatie gebruikt, kan het moeilijker zijn om implementatielogica te volgen en veranderingen in de toekomst uit te voeren wanneer nodig.</li><li>**vereist afbeelding om gegevens naar Platform** te verzenden: Wanneer uw organisatie klaar is om Customer Journey Analytics te gebruiken, moet u gegevens naar een gegevensreeks in Adobe Experience Platform verzenden. Deze actie vereist dat elk gebied in het `data` voorwerp een ingang in het hulpmiddel is van de gegevenstoewijzing dat het aan een XDM schemagebied toewijst. Voor deze workflow hoeft u slechts één keer toewijzingen uit te voeren, en dit betekent niet dat u implementatiewijzigingen aanbrengt. Het is echter een extra stap die niet vereist is bij het verzenden van gegevens in een XDM-object.</li></ul> |

De Adobe beveelt aan dit implementatiepad in de volgende scenario&#39;s te volgen:

* U hebt een bestaande implementatie met de Adobe Analytics AppMeasurement JavaScript-bibliotheek. Als u een implementatie gebruikend de de markeringsuitbreiding van Adobe Analytics hebt, volg [ Migrate van de de markeringsuitbreiding van Adobe Analytics aan de de markeringsuitbreiding van SDK van het Web ](analytics-extension-to-web-sdk.md) in plaats daarvan.
* U bent van plan om Customer Journey Analytics in de toekomst te gebruiken, maar wilt uw implementatie Analytics niet met een implementatie van SDK van het Web van kras vervangen. Het vervangen van uw implementatie van kras op het Web SDK vereist de meeste inspanning, maar ook biedt de meest levensvatbare implementatiearchitectuur op lange termijn aan. Als uw organisatie bereid is door de inspanning van een schone implementatie van SDK van het Web te gaan, zie [ Samenvattingsgegevens via het Web SDK van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk) in de gebruikersgids van de Customer Journey Analytics.

## Stappen vereist om naar SDK van het Web te migreren

De volgende stappen bevatten concrete doelstellingen die moeten worden nagestreefd. Klik op elke stap voor gedetailleerde instructies over hoe u deze kunt uitvoeren.

+++**1. Creeer en vorm een gegevensstroom**

Maak een gegevensstroom in de gegevensverzameling van Adobe Experience Platform. Wanneer u gegevens naar deze gegevensstroom verzendt, stuurt het gegevens door naar Adobe Analytics. In de toekomst stuurt dezelfde gegevensstroom gegevens door naar de Customer Journey Analytics.

1. Navigeer aan [ experience.adobe.com ](https://experience.adobe.com) en login gebruikend uw geloofsbrieven.
1. Gebruik de startpagina of de productkiezer rechtsboven om naar **[!UICONTROL Data Collection]** te navigeren.
1. Selecteer **[!UICONTROL Datastreams]** in de linkernavigatie.
1. Selecteer **[!UICONTROL New Datastream]** .
1. Voer de gewenste naam in en selecteer vervolgens **[!UICONTROL Save]** .
1. Wanneer de gegevensstroom is gemaakt, selecteert u **[!UICONTROL Add Service]** .
1. Selecteer **[!UICONTROL Adobe Analytics]** in het vervolgkeuzemenu voor de service.
1. Voer dezelfde rapportsuite-id in als de site waarnaar u momenteel analysegegevens verzendt. Klik op **[!UICONTROL Save]**.

![ voeg de dienst van Adobe Analytics ](assets/datastream-rsid.png) toe {style="border:1px solid lightslategray"}

Uw gegevensstroom is nu klaar om gegevens te ontvangen en door te geven aan Adobe Analytics. Noteer de gegevensstroom-id, aangezien deze id vereist is voor het configureren van de Web SDK in code.

+++

+++**2. De SDK van het Web JavaScript-bibliotheek installeren**

Verwijs naar de recentste versie van `alloy.js` zodat kan zijn methodevraag worden gebruikt. Zie [ SDK van het Web installeren gebruikend de bibliotheek van JavaScript ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/install/library) voor details en codeblokken aan gebruik.

+++

+++**3. Vorm SDK van het Web**

Opstelling uw implementatie om aan de datastream te richten die in de vorige stap wordt gecreeerd door het Web SDK [`configure` te gebruiken ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) bevel. De opdracht `configure` moet op elke pagina worden ingesteld, zodat u deze naast de installatiecode van de bibliotheek kunt plaatsen.

Gebruik de eigenschappen [`datastreamId` ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/datastreamId) en [`orgId` ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/orgid) binnen het bevel van SDK van het Web `configure`:

* Stel de `datastreamId` in op de gegevensstroom-id die u uit de vorige stap hebt opgehaald.
* Stel de `orgId` in op IMS org van uw organisatie.

```js
alloy("configure", {
    datastreamId: "ebebf826-a01f-4458-8cec-ef61de241c93",
    orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg"
});
```

U kunt naar keuze andere eigenschappen in het [`configure` plaatsen ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) bevel afhankelijk van de implementatievereisten van uw organisatie.

+++

+++**4. De codelogica van de update om een nuttige lading te gebruiken JSON**

Wijzig de analytische implementatie zodat deze niet afhankelijk is van `AppMeasurement.js` of het `s` -object. Stel in plaats daarvan variabelen in in een JavaScript-object met de juiste indeling, dat wordt omgezet in een JSON-object wanneer het naar de Adobe wordt verzonden. Het hebben van de laag van a [ Gegevens ](../../prepare/data-layer.md) op uw plaats helpt enorm wanneer het plaatsen van waarden, aangezien u die zelfde waarden kunt blijven van verwijzingen voorzien.

Voor het verzenden van gegevens naar Adobe Analytics moet de Web SDK-payload `data.__adobe.analytics` gebruiken met alle analytische variabelen die binnen dit object zijn ingesteld. Variabelen in dit object hebben dezelfde namen en indelingen als de variabele tegenhangers van het AppMeasurement. Als u bijvoorbeeld de variabele `products` instelt, moet u deze niet splitsen in afzonderlijke objecten, zoals bij XDM. Neem de variabele in plaats daarvan op als een tekenreeks, precies wanneer u de variabele `s.products` instelt:

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "products": "Shoes,Men's sneakers,1,49.99"
      }
    }
  }
}
```

Uiteindelijk bevat deze payload alle gewenste waarden en worden alle verwijzingen naar het `s` -object in de implementatie verwijderd. U kunt alle bronnen die JavaScript biedt, gebruiken om dit payload-object in te stellen, inclusief puntnotatie voor het instellen van individuele waarden.

```js
// Define the payload and set objects within it
var dataObj = {data: {__adobe: {analytics: {}}}};
dataObj.data.__adobe.analytics.pageName = window.document.title;
dataObj.data.__adobe.analytics.eVar1 = "Example value";

// Alternatively, set values in an object and use a spread operator to achieve identical results
var a = new Object;
a.pageName = window.document.title;
a.eVar1 = "Example value";
var dataObj = {data:{__adobe:{analytics:{...a}}}};
```

+++

+++**5. De methodevraag van de update om het Web SDK te gebruiken**

Werk alle instanties bij waar u [`s.t()`](../../vars/functions/t-method.md) en [`s.tl()`](../../vars/functions/tl-method.md) roept, die hen met het [`sendEvent` ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/sendevent/overview) bevel vervangen. Er zijn drie scenario&#39;s om te overwegen:

* **het volgen van de mening van de Pagina**: Vervang de het volgen vraag van de paginamening met het bevel van SDK van het Web `sendEvent`:

  ```js
  // If your current implementation has this line of code:
  s.t();
  
  // Replace it with this line of code. The dataObj object contains the variables to send.
  alloy("sendEvent", dataObj);
  ```

* **Automatische verbinding het volgen**: Het [`clickCollectionEnabled` ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) configuratiebezit wordt toegelaten door gebrek. De juiste variabelen voor het bijhouden van koppelingen worden automatisch ingesteld om gegevens naar Adobe Analytics te verzenden. Als u automatische verbinding het volgen wilt onbruikbaar maken, plaats dit bezit aan `false` binnen het [`configure` ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) bevel.

* **Handmatig verbinding het volgen**: Het Web SDK heeft geen afzonderlijke bevelen tussen de voorproef en niet-voorproefvraag. Geef dat onderscheid op in het object payload.

  ```js
  // If your current implementation has this line of code:
  s.tl(true,"o","Example custom link");
  
  // Replace it with these lines of code. Add the required fields to the dataObj object.
  dataObj.data.__adobe.analytics.linkName = "Example custom link";
  dataObj.data.__adobe.analytics.linkType = "o";
  dataObj.data.__adobe.analytics.linkURL = "https://example.com";
  alloy("sendEvent", dataObj);
  ```

+++

+++**6. Wijzigingen valideren en publiceren**

Nadat u alle verwijzingen naar het AppMeasurement en het `s` -object hebt verwijderd, publiceert u uw wijzigingen in de ontwikkelomgeving om te controleren of de nieuwe implementatie werkt. Nadat u hebt gecontroleerd dat alles correct werkt, kunt u uw updates publiceren voor productie.

Als de migratie correct is, is `AppMeasurement.js` niet meer vereist op uw site en kunnen alle verwijzingen naar dit script worden verwijderd.

+++

Op dit punt, is uw implementatie van Analytics volledig op het Web SDK en is voldoende bereid om aan Customer Journey Analytics in de toekomst te bewegen.
