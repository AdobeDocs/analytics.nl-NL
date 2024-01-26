---
title: Een eigenschap Analytics maken in tags
description: Maak een spatie om aan te passen hoe gegevens worden verzameld met behulp van codes.
feature: Tags
exl-id: ffcd8e97-4d29-489e-bc2b-88805400dad5
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 2%

---

# Een Adobe Analytics-tageigenschap maken

Met tags in Adobe Experience Platform kunt u oplossingen voor Experiencen Cloud integreren in uw website (inclusief Analytics). Deze pagina schetst specifiek hoe een markeringsbeheerder een basisimplementatie van Adobe Analytics kan krijgen correct wordt gevormd.

## Vereisten

[Een rapportsuite maken](/help/admin/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Maak een silo voor analysegegevens die moeten worden verzameld.

## Een eigenschap voor tags maken en vitale extensies installeren

Eigenschappen zijn overkoepelende containers die u gebruikt om tags te beheren. Met extensies kunt u productspecifieke tags installeren en configureren.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op **[!UICONTROL New Property]**.
1. Geef uw eigenschap een naam, zoals de titel van uw website, en voer het domein in waarop u Analytics wilt implementeren. Klik op **[!UICONTROL Save]**.
1. Klik op de nieuwe tageigenschap om de instellingen in te voeren.
1. Klik op de knop **[!UICONTROL Extensions]** tab, en klik vervolgens op **[!UICONTROL Catalog]**.
1. Zoek &#39;Experience Cloud-id-service&#39; en klik op **[!UICONTROL Install]**.
1. Alle instellingen, inclusief de organisatie-id van het Experience Cloud, moeten al zijn ingevuld. Klik op **[!UICONTROL Save]**.
1. Ga terug in de extensiecatalogus naar Adobe Analytics en klik op **[!UICONTROL Install]**.

Zie de volledige documentatie voor de [Adobe Analytics-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html) voor meer gedetailleerde informatie.

## Gegevenselementen maken voor Adobe Analytics

Gegevenselementen zijn verwijzingen naar specifieke delen van uw site om variabelewaarden te verzamelen.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de eigenschap tag die u op uw site wilt implementeren.
1. Klik op de knop **[!UICONTROL Data Elements]** tab, en klik vervolgens op **[!UICONTROL Add Data Element]**.
1. Geef het gegevenselement de volgende instellingen:

   * Naam: paginanaam
   * Extensie: Core
   * Type gegevenselement: JavaScript-variabele
   * Naam JavaScript-variabele: `window.document.title`

     >[!NOTE]
     >
     >Deze waarde dient als voorbeeld om aan de slag te gaan. Als uw organisatie een betere waarde voor paginanaam, zoals een waarde van de gegevenslaag bepaalt, kunt u het hier ingaan.
   * Tekst reinigen ingeschakeld
   * Opslagduur: geen
1. Klik op **[!UICONTROL Save]**.

## Regels maken voor Adobe Analytics

Regels wijzen gegevenselementen aan de veranderlijke waarden van de Analyse toe, en bepalen wanneer die waarden naar de servers van de Adobe worden verzonden.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de eigenschap tag die u op uw site wilt implementeren.
1. Klik op de knop **[!UICONTROL Rules]** tab, en klik vervolgens op **[!UICONTROL Add Rule]**. Naam geven `Global Rule`.
1. Klikken **[!UICONTROL Add]** naast gebeurtenissen en voer de volgende instellingen in:
   * Extensie: Core
   * Type gebeurtenis: bibliotheek geladen (pagina boven)
   * Naam: Kern - Bibliotheek geladen (Pagina boven)
1. Klik op **[!UICONTROL Keep Changes]**.
1. Onder **[!UICONTROL Actions]**, klikt u op **[!UICONTROL Add]** en voer de volgende instellingen in:
   * Extensie: Adobe Analytics
   * Type handeling: variabelen instellen
   * Paginanaam: klik op het containerpictogram en selecteer de `Page Name` gegevenselement.
   * Campagne: Query-parameter met de waarde van `cid`
1. Klik op **[!UICONTROL Keep Changes]**.
1. Klik op het plusteken naast handelingen om nog een handeling toe te voegen en voer de volgende instellingen in:
   * Extensie: Adobe Analytics
   * Handelingstype: baken verzenden
   * Naam: Adobe Analytics - Send Beacon
   * Tekstspatiëring: s.t()
1. Klik op **[!UICONTROL Keep Changes]**.
1. Controleer of u de gebeurtenis en twee handelingen hebt ingesteld en klik vervolgens op **[!UICONTROL Save]**.

## Volgende stappen

[Implementeer uw analytische implementatie in uw ontwikkelomgeving](deploy-dev.md): Krijg de code van de Analyse werkend in een testmilieu.
