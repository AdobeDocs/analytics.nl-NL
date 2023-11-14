---
description: Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.
title: Activity Map inschakelen
feature: Activity Map
role: Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
mini-toc-levels: 3
source-git-commit: ae1c2ff1987e2fe5d147bfe74874b53492d48b5e
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 2%

---


# Activity Map activeren en inschakelen

Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.

## Stap 1. Activity Map activeren {#update_code}

De module van de Activity Map maakt deel uit van AppMeasurement.js, de markeringen van Adobe Experience Platform, en het Web SDK (alloy.js). Gegevens over Activity Mappen kunnen alleen worden verzameld als u de update naar **Web SDK versie 2.15.0** of hoger, **Adobe Analytics-tagextensie v1.90** of hoger, **AppMeasurement versie 1.6** of hoger.

+++Web SDK (Adobe Experience Platform-tagextensie)

1. Navigeer in Adobe Experience Platform-tags naar de eigenschap waarvoor u Analytics implementeert. Onder [!UICONTROL Extensions] -> [!UICONTROL Adobe Experience Platform Web SDK], selecteert u **[!UICONTROL Enable click data collection]** zoals hieronder gemarkeerd.
1. Maak de bibliotheek met de wijzigingen.
1. Publiceer de bibliotheek naar productie.

![](assets/web_sdk.png)

**Validatie**

Interactie vraag gebruikend het Lusje van het Netwerk van de Console van de Ontwikkelaar:

1. Laad het manuscript van de Lancering van de Ontwikkeling op de plaats.
1. Bij klikken op elementen zoekt u naar &#39;/ee&#39; op het tabblad Netwerk

   ![](assets/validation1.png)

Adobe Experience Platform Debugger:

1. Download en installeer de [Adobe Experience Platform debugger](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob).
1. Ga naar [!UICONTROL Logs] > [!UICONTROL Edge] > [!UICONTROL Connect to Edge].

   ![](assets/validation2.jpg)

**Veelgestelde vragen**

* **De interactieve vraag vuurt niet in het lusje van het Netwerk.**
De klikgegevensinzameling in een inzamelingsvraag, moeten wij met of &quot;/ee&quot;of &quot;verzamelen?&quot;filtreren

* **Er is geen weergave voor Payload voor de verzamelvraag.**
De verzamelvraag wordt ontworpen op dusdanige wijze dat het volgen niet navigatie aan andere plaatsen zou moeten beïnvloeden, zodat is de eigenschap van het document unload toepasselijk voor de inzamelingsvraag. Dit heeft geen invloed op uw gegevensverzameling, maar als u op pagina moet valideren, voegt u target = &quot;_blank&quot; toe aan het desbetreffende element. Vervolgens wordt de koppeling geopend op een nieuw tabblad.

* **Hoe negeer ik de inzameling van PII?**
Voeg de respectievelijke voorwaarden toe in&lt;&lt; op alvorens de verbinding klikt verzendt callback>> en keert vals terug om die waarden te negeren. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=en)

  Voorbeeldcode:

  ![](assets/sample-code.png)

+++

+++Handmatige Web SDK-implementatie

Zie [Koppelingen bijhouden](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html) voor informatie over hoe te om verbinding het volgen uit te voeren en hoe te om Activity Map toe te laten door te vangen `region` van het aangeklikte HTML-element.

>[!NOTE]
>
>Het toelaten van verbinding het volgen met SDK van het Web verzendt momenteel verbindingsgebeurtenissen wanneer een klant van één pagina aan volgende navigeert. Dit is anders dan hoe AppMeasurement werkt en kan mogelijk leiden tot extra factureerbare hits die naar de Adobe worden verzonden.

+++

+++extensie Analytics (Adobe Experience Platform-tags)

Navigeer in Adobe Experience Platform-tags naar de eigenschap waarvoor u Analytics implementeert. In de [!UICONTROL Install Extension] dialoogvenster, selecteren **[!UICONTROL Use Activity Map]**.

![](assets/aa_extension.png)

+++

+++AppMeasurement

1. Download de nieuwste JavaScript-bibliotheek voor AppMeasurement.
Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Code manager]**.
1. Implementeren door het volgende uit te voeren [deze instructies](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html).

+++

## Stap 2. Rapporten Activity Map inschakelen {#enable}

U moet de rapporten van de Activity Map op rapport-reeks niveau toelaten.

1. Meld u aan bij Adobe Analytics en ga naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map Reporting]** .

1. De Activity Map verzamelt de verbindingsgegevens in de rapporten van de Activity Map. Voor activering moet u eerst de variabelen activeren door op **[!UICONTROL Enable Activity Map Reports]**.

   Met deze stap voegt u alle analytische afmetingen toe die u nodig hebt om gegevens te verzamelen.

   ![](assets/enable.png)

1. Controleer na ongeveer een uur de instelling [Rapport Activity Map pagina](/help/analyze/activity-map/activitymap-reporting-analytics.md), waarin alle pagina&#39;s worden weergegeven waarop gebruikers op een koppeling hebben geklikt.

## Stap 3. Gebruikers toevoegen aan [!UICONTROL Activity Map Access] productprofiel {#add_users}

1. Klik op **[!UICONTROL Add Users to Group]**.

   Hiermee gaat u naar de pagina met productprofielen in het dialoogvenster [Adobe Admin Console](https://adminconsole.adobe.com/E2F05B3B52F54D2E0A490D44@AdobeOrg/overview).

1. Als u geen [!UICONTROL Activity Map Access] productprofiel, doe dit nu. De voor dit profiel vereiste machtigingsitems zijn [!UICONTROL Analytics Tools] > [!UICONTROL Activity Map] en [!UICONTROL Analytics Tools] > [!UICONTROL Segment Publishing].

1. Voeg gebruikers toe aan dat productprofiel. Hierdoor kunnen uw gebruikers Activity Map downloaden van  **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL ActivityMap]** .

