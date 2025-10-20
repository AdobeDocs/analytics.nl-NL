---
title: Visitor-identificatie met AppMeasurement
description: Identificeer bezoekers correct wanneer het uitvoeren van Adobe Analytics gebruikend AppMeasurement.
source-git-commit: 779ba5b0a1d71467aaaf3872fd707cc323ae8af2
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Visitor-identificatie met AppMeasurement

AppMeasurement is de verouderde JavaScript-bibliotheek van Adobe Analytics voor gegevensverzameling. Hoewel AppMeasurement zelf een native manier biedt om bezoekers te identificeren, wijzen veel moderne browsers de cookies van derden die het probeert in te stellen, af. Adobe raadt ten zeerste aan de Adobe Experience Cloud Visitor ID Service in alle implementaties te gebruiken om te voldoen aan de moderne privacystandaarden voor browsers. Alle versies van AppMeasurement worden meegeleverd met `VisitorAPI.js` , de JavaScript-bibliotheek die wordt gebruikt om de Bezoeker-id-service te implementeren.

## Bezoekers identificeren aan de hand van de Bezoekersidentiteitsservice (aanbevolen)

Zorg ervoor dat u voorbereid bent met het volgende:

* Download de [&#x200B; Meest recente versie van AppMeasurement &#x200B;](https://github.com/adobe/appmeasurement). De gedownloade bibliotheek bevat zowel `AppMeasurement.js` als `VisitorAPI.js` .
* De reeks ID van het ontwikkelings [&#x200B; Rapport &#x200B;](/help/admin/tools/manage-rs/new-rs/new-report-suite.md).
* Het gewenste randdomein voor [`trackingServerSecure`](/help/implement/vars/config-vars/trackingserversecure.md) .
* Uw IMS org-id:
   1. Login aan [&#x200B; experience.adobe.com &#x200B;](https://experience.adobe.com) gebruikend uw geloofsbrieven van Adobe ID.
   1. Druk overal in de Experience Cloud-interface op `[Cmd]` + `[I]` (iOS) of `[Ctrl]` + `[I]` (Windows).
   1. Er verschijnt een **[!UICONTROL User data debugger]** . Selecteer het tabblad **[!UICONTROL Assigned orgs]**. 
   1. Breid de gewenste organisatie IMS uit.
   1. Zoek het veld **[!UICONTROL ID]** .

Zodra u de bovengenoemde middelen hebt, bevat de volgende basisvoorbeeldpagina de minimum vereiste vraag om gegevens naar Adobe Analytics te verzenden:

```html
<html>
  <head>
    <title>Example AppMeasurement implementation page</title>
    <script src="AppMeasurement.js"></script>
    <script src="VisitorAPI.js"></script>
  </head>
  <body>
    <h1>Hello world!</h1>
    <script>
      var s = s_gi("examplersid"); // Include development report suite ID here
      s.trackingServerSecure = "example.data.adobedc.net"; // Include edge domain here
      s.visitor = Visitor.getInstance("ADB3LETTERSANDNUMBERS@AdobeOrg"); // Include IMS org ID here
      s.pageName = document.title;
      s.t();
    </script>
  </body>
</html>
```

>[!TIP]
>
>U kunt bijhouden of een hit gebruikmaakt van de service Bezoeker-id door de aanwezigheid van `Visitor` toe te wijzen aan een aangepaste variabele in [`doPlugins`](/help/implement/vars/functions/doplugins.md) :
>
>```js
>s.doPlugins = function() {
>   s.prop1 = typeof(Visitor) != "undefined" ? "VisitorAPI present" : "VisitorAPI missing";
>};
>```

## Bezoekers identificeren aan de hand van het cookie `s_vi` (niet aanbevolen)

>[!IMPORTANT]
>
>Adobe raadt u af deze methode te gebruiken om bezoekers te identificeren.

Als uw organisatie de Bezoeker-id-service niet gebruikt, gebruikt AppMeasurement een eigen vorm van bezoekersidentificatie. Wanneer een bezoeker voor het eerst bij uw plaats aankomt, controleert de bibliotheek een [`s_vi` &#x200B;](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) koekje. Deze cookie wordt ingesteld op het overeenkomende domein [`trackingServerSecure`](/help/implement/vars/config-vars/trackingserversecure.md) (voor HTTPS) of [`trackingServer`](/help/implement/vars/config-vars/trackingserver.md) (voor HTTP).

* Als u aan het [&#x200B; Beheerde certificaatprogramma &#x200B;](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/adobe-managed-cert) deelneemt, zou uw het volgen server typisch een eerste-partijdomein zijn, makend `s_vi` koekjes eerste-partij.
* Als u niet deelneemt aan het beheerde certificaatprogramma, is de trackingserver doorgaans een subdomein van `adobedc.net` , `omtrdc.net` of `2o7.net` , waardoor de `s_vi` -cookie een cookie van een derde wordt. Vanwege de moderne privacystandaarden van browsers worden cookies van derden door de meeste browsers geweigerd. Als AppMeasurement eenmaal is geweigerd, probeert het een fallback-cookie van de eerste partij (`fid`) in te stellen.

Als u `trackingServerSecure` op de juiste wijze instelt, zijn geen verdere identificatiemaatregelen voor de bezoeker vereist.

## Bezoekers identificeren met `visitorID` (niet aanbevolen)

>[!IMPORTANT]
>
>Adobe raadt u af deze methode te gebruiken om bezoekers te identificeren.

Met de variabele [`visitorID`](/help/implement/vars/config-vars/visitorid.md) kan uw organisatie volledig onafhankelijke controle gebruiken om bezoekers te identificeren. Houd rekening met de volgende beperkingen wanneer u `visitorID` gebruikt:

* Elke treffer moet dezelfde `visitorID` -waarde bevatten die als één bezoeker moet worden geteld.
   * Bij alle treffers waarbij `visitorID` wordt weggelaten, wordt automatisch geprobeerd een andere methode voor bezoekersidentificatie te gebruiken, waarbij deze als een aparte bezoeker worden behandeld.
   * Alle treffers die een andere `visitorID` -waarde dan een vorige treffer bevatten, worden beschouwd als een aparte bezoeker.
   * Adobe biedt geen enkele manier om treffers aan elkaar te koppelen met behulp van verschillende bezoeker-id&#39;s.
* Gedeeld publiek, Analytics for Target en klantkenmerken worden niet ondersteund voor bezoekers die zijn geïdentificeerd met `visitorID` .

Zie [`visitorID`](/help/implement/vars/config-vars/visitorid.md) voor implementatieinstructies die deze variabele gebruiken.
