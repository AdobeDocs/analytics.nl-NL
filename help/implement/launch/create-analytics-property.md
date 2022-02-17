---
title: Een eigenschap Analytics maken in tags
description: Maak een spatie om aan te passen hoe gegevens worden verzameld met tags.
feature: Launch Implementation
exl-id: ffcd8e97-4d29-489e-bc2b-88805400dad5
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 1%

---

# Een Adobe Analytics-tageigenschap maken

Met tags in Adobe Experience Platform kunt u Experience Cloud-oplossingen integreren in uw website (inclusief Analytics). Deze pagina schetst specifiek hoe een markeringsbeheerder een basisimplementatie van Adobe Analytics kan krijgen correct wordt gevormd.

>[!NOTE]
>Adobe Experience Platform Launch is omgedoopt tot een reeks technologieën voor gegevensverzameling in Experience Platform. Diverse terminologische wijzigingen zijn als gevolg hiervan in de productdocumentatie doorgevoerd. Raadpleeg het volgende [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) voor een geconsolideerde referentie van de terminologische wijzigingen.

## Vereisten

[Een rapportsuite maken](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Maak een silo voor analysegegevens die moeten worden verzameld.

## Een eigenschap voor tags maken en vitale extensies installeren

Eigenschappen zijn overkoepelende containers die u gebruikt om tags te beheren. Met extensies kunt u productspecifieke tags installeren en configureren.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op **[!UICONTROL New Property]**.
1. Geef uw eigenschap een naam, zoals de titel van uw website, en voer het domein in waarop u Analytics wilt implementeren. Klik op **[!UICONTROL Save]**.
1. Klik op de nieuwe tageigenschap om de instellingen in te voeren.
1. Klik op de knop **[!UICONTROL Extensions]** tab, en klik vervolgens op **[!UICONTROL Catalog]**.
1. Identiteitsservice zoeken en klik vervolgens op **[!UICONTROL Install]**.
1. Alle instellingen, inclusief de Experience Cloud Organisatie-id, moeten al zijn ingevuld. Klik op **[!UICONTROL Save]**.
1. Ga terug in de extensiecatalogus naar Adobe Analytics en klik op **[!UICONTROL Install]**.

## Gegevenselementen maken voor Adobe Analytics

Gegevenselementen zijn verwijzingen naar specifieke delen van uw site om variabelewaarden te verzamelen.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de eigenschap tag die u op uw site wilt implementeren.
1. Klik op de knop **[!UICONTROL Data Elements]** tab, en klik vervolgens op **[!UICONTROL Create New Data Element]**.
1. Geef het gegevenselement de volgende instellingen:

   * Naam: Paginanaam
   * Extensie: Kern
   * Type gegevenselement: JavaScript-variabele
   * Pad naar variabele: `window.document.title`

      >[!NOTE]
      >
      >Dit is een voorbeeldwaarde om aan de slag te gaan. Als uw organisatie een betere waarde voor paginanaam, zoals een waarde van de gegevenslaag bepaalt, kunt u het hier ingaan.
   * Tekst reinigen ingeschakeld
   * Duur: Voorvertoning
1. Klik op **[!UICONTROL Save]**.

## Regels maken voor Adobe Analytics

Regels wijzen gegevenselementen aan de veranderlijke waarden van de Analyse in kaart, en bepalen wanneer die waarden naar Adobe worden verzonden.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de eigenschap tag die u op uw site wilt implementeren.
1. Klikken **[!UICONTROL Create New Rule]** en noem deze `Global Rule`.
1. Klikken **[!UICONTROL Add]** naast gebeurtenissen en voer de volgende instellingen in:
   * Extensie: Kern
   * Type gebeurtenis: Bibliotheek geladen (pagina boven)
   * Naam: Kern - Bibliotheek geladen (pagina boven)
   * Volgorde: 50
1. Klik op **[!UICONTROL Keep Changes]**.
1. Onder **[!UICONTROL Actions]**, klikt u op **[!UICONTROL Add]** en voer de volgende instellingen in:
   * Extensie: Adobe Analytics
   * Type handeling: Variabelen instellen
   * Paginanaam: Klik op het containerpictogram en selecteer de `Page Name` gegevenselement.
   * Campagne: De parameter van de vraag met een waarde van `cid`
1. Klik op **[!UICONTROL Keep Changes]**.
1. Klik op het plusteken naast handelingen om nog een handeling toe te voegen en voer de volgende instellingen in:
   * Extensie: Adobe Analytics
   * Type handeling: Band verzenden
   * Naam: Adobe Analytics - Send Beacon
   * Tekstspatiëring: s.t()
1. Klik op **[!UICONTROL Keep Changes]**.
1. Controleer of u de gebeurtenis en twee handelingen hebt ingesteld en klik vervolgens op **[!UICONTROL Save]**.

## Documentatie en aanvullende middelen

* [Adobe Analytics-extensiedocumentatie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=en): Volledige documentatie die specifiek is voor de Adobe Analytics-extensie in tags.
* [Aan de slag met tags](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html?lang=en): Volledige documentatie voor tags, inclusief een uitgebreidere gids om aan de slag te gaan
* [Adobe Experience Platform Launch-kanaal](https://experienceleague.adobe.com/?tag=Launch#recommended/solutions/experience-platform): Leer hoe u tags kunt gebruiken via video&#39;s

## Volgende stappen

[Implementeer uw analytische implementatie in uw ontwikkelomgeving](deploy-dev.md): De code Analytics van de Krijg werkend in een testmilieu.
