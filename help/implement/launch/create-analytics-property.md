---
title: Een eigenschap Analytics maken in tags
description: Maak een spatie om aan te passen hoe gegevens worden verzameld met behulp van codes.
feature: Tags
exl-id: ffcd8e97-4d29-489e-bc2b-88805400dad5
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 2%

---

# Een Adobe Analytics-tageigenschap maken

Met tags in Adobe Experience Platform kunt u Experience Cloud-oplossingen integreren in uw website (inclusief Analytics). Deze pagina schetst specifiek hoe een markeringsbeheerder een basisimplementatie van Adobe Analytics kan krijgen correct wordt gevormd.

## Vereisten

[&#x200B; creeer een rapportreeks &#x200B;](/help/admin/tools/manage-rs/new-rs/t-create-a-report-suite.md): Creeer een silo voor de gegevens van Analytics die moeten worden verzameld.

## Een eigenschap voor tags maken en vitale extensies installeren

Eigenschappen zijn overkoepelende containers die u gebruikt om tags te beheren. Met extensies kunt u productspecifieke tags installeren en configureren.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op **[!UICONTROL New Property]**.
1. Geef uw eigenschap een naam, zoals de titel van uw website, en voer het domein in waarop u Analytics wilt implementeren. Klik op **[!UICONTROL Save]**.
1. Klik op de nieuwe tageigenschap om de instellingen in te voeren.
1. Klik op de tab **[!UICONTROL Extensions]** en klik vervolgens op **[!UICONTROL Catalog]** .
1. Zoek &#39;Experience Cloud ID Service&#39; en klik vervolgens op **[!UICONTROL Install]** .
1. Alle instellingen, inclusief Experience Cloud-organisatie-id, moeten al zijn ingevuld. Klik op **[!UICONTROL Save]**.
1. Zoek Adobe Analytics en klik op **[!UICONTROL Install]** in de extensiecatalogus.

Zie de volledige documentatie voor de [&#x200B; uitbreiding van Adobe Analytics &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=nl-NL) voor meer gedetailleerde informatie.

## Gegevenselementen maken voor Adobe Analytics

Gegevenselementen zijn verwijzingen naar specifieke delen van uw site om variabelewaarden te verzamelen.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de eigenschap tag die u op uw site wilt implementeren.
1. Klik op de tab **[!UICONTROL Data Elements]** en klik vervolgens op **[!UICONTROL Add Data Element]** .
1. Geef het gegevenselement de volgende instellingen:

   * Naam: paginanaam
   * Extensie: Core
   * Type gegevenselement: JavaScript-variabele
   * Naam variabele JavaScript: `window.document.title`

     >[!NOTE]
     >
     >Deze waarde dient als voorbeeld om aan de slag te gaan. Als uw organisatie een betere waarde voor paginanaam, zoals een waarde van de gegevenslaag bepaalt, kunt u het hier ingaan.
   * Tekst reinigen ingeschakeld
   * Opslagduur: geen
1. Klik op **[!UICONTROL Save]**.

## Regels maken voor Adobe Analytics

Regels wijzen gegevenselementen aan de veranderlijke waarden van de Analyse toe, en bepalen wanneer die waarden naar de servers van Adobe worden verzonden.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de eigenschap tag die u op uw site wilt implementeren.
1. Klik op de tab **[!UICONTROL Rules]** en klik vervolgens op **[!UICONTROL Add Rule]** . Noem het `Global Rule`.
1. Klik op **[!UICONTROL Add]** naast gebeurtenissen en voer de volgende instellingen in:
   * Extensie: Core
   * Type gebeurtenis: bibliotheek geladen (pagina boven)
   * Naam: Kern - Bibliotheek geladen (Pagina boven)
1. Klik op **[!UICONTROL Keep Changes]**.
1. Klik onder **[!UICONTROL Actions]** op **[!UICONTROL Add]** en voer de volgende instellingen in:
   * Extensie: Adobe Analytics
   * Type handeling: variabelen instellen
   * Paginanaam: klik op het containerpictogram en selecteer het gegevenselement `Page Name` .
   * Campagne: Query-parameter met de waarde `cid`
1. Klik op **[!UICONTROL Keep Changes]**.
1. Klik op het plusteken naast handelingen om nog een handeling toe te voegen en voer de volgende instellingen in:
   * Extensie: Adobe Analytics
   * Handelingstype: baken verzenden
   * Naam: Adobe Analytics - Send Beacon
   * Tekstspatiëring: s.t()
1. Klik op **[!UICONTROL Keep Changes]**.
1. Controleer of u de gebeurtenis en twee handelingen hebt ingesteld en klik op **[!UICONTROL Save]** .

## Volgende stappen

[&#x200B; stelt uw implementatie van Analytics aan uw ontwikkelomgeving &#x200B;](deploy-dev.md) op: Krijg de code van Analytics die in een testmilieu werkt.
