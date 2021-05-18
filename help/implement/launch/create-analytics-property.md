---
title: Een eigenschap Analytics maken in Launch
description: Met Adobe Experience Platform Launch maakt u een spatie om aan te passen hoe gegevens worden verzameld.
exl-id: ffcd8e97-4d29-489e-bc2b-88805400dad5
source-git-commit: c46feec3f08b78ca7882193ab86914db49617c1c
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 3%

---

# Een eigenschap Analytics maken in Adobe Experience Platform Launch

Adobe Experience Platform Launch is het hulpprogramma waarmee u Experience Cloud-oplossingen kunt integreren op uw website (inclusief Analytics). Deze pagina schetst specifiek hoe een beheerder van de Lancering een basisimplementatie van Adobe Analytics kan krijgen correct wordt gevormd.

## Vereisten

[Maak een rapportsuite](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Een silo maken voor analysegegevens die moeten worden verzameld

## Een eigenschap maken en vitale extensies installeren

Eigenschappen zijn overkoepelende containers die u gebruikt om tags te beheren. Met extensies kunt u productspecifieke tags installeren en configureren.

1. Ga naar [launch.adobe.com](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op **[!UICONTROL New Property]**.
1. Geef uw eigenschap een naam, zoals de titel van uw website, en voer het domein in waarop u Analytics wilt implementeren. Klik op **[!UICONTROL Save]**.
1. Klik op de nieuwe eigenschap om de instellingen in te voeren.
1. Klik op de tab **[!UICONTROL Extensions]** en klik vervolgens op **[!UICONTROL Catalog]**.
1. Ga naar Identiteitsservice en klik vervolgens op **[!UICONTROL Install]**.
1. Alle instellingen, inclusief de Experience Cloud Organisatie-id, moeten al zijn ingevuld. Klik op **[!UICONTROL Save]**.
1. Zoek Adobe Analytics weer in de extensiecatalogus en klik op **[!UICONTROL Install]**.

## Gegevenselementen maken voor Adobe Analytics

Gegevenselementen zijn verwijzingen naar specifieke delen van uw site om variabelewaarden te verzamelen.

1. Ga naar [launch.adobe.com](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op de eigenschap Starten die u op uw site wilt implementeren.
1. Klik op de tab **[!UICONTROL Data Elements]** en klik vervolgens op **[!UICONTROL Create New Data Element]**.
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

1. Ga naar [launch.adobe.com](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op de eigenschap Starten die u op uw site wilt implementeren.
1. Klik **[!UICONTROL Create New Rule]** en noem het `Global Rule`.
1. Klik op **[!UICONTROL Add]** naast gebeurtenissen en voer de volgende instellingen in:
   * Extensie: Kern
   * Type gebeurtenis: Bibliotheek geladen (pagina boven)
   * Naam: Kern - Bibliotheek geladen (pagina boven)
   * Volgorde: 50
1. Klik op **[!UICONTROL Keep Changes]**.
1. Klik onder **[!UICONTROL Actions]** op **[!UICONTROL Add]** en voer de volgende instellingen in:
   * Extensie: Adobe Analytics
   * Type handeling: Variabelen instellen
   * Paginanaam: Klik op het containerpictogram en selecteer het gegevenselement `Page Name`.
   * Campagne: De parameter van de vraag met een waarde van `cid`
1. Klik op **[!UICONTROL Keep Changes]**.
1. Klik op het plusteken naast handelingen om nog een handeling toe te voegen en voer de volgende instellingen in:
   * Extensie: Adobe Analytics
   * Type handeling: Band verzenden
   * Naam: Adobe Analytics - Send Beacon
   * Tekstspatiëring: s.t()
1. Klik op **[!UICONTROL Keep Changes]**.
1. Controleer of u de gebeurtenis en twee handelingen hebt ingesteld en klik op **[!UICONTROL Save]**.

## Documentatie en aanvullende middelen

* [Adobe Analytics-extensiedocumentatie](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/analytics-extension/overview.html?lang=en#extensions-ref): Volledige documentatie specifiek voor de Adobe Analytics-extensie in Adobe Experience Platform Launch.
* [Aan de slag met starten](https://experienceleague.adobe.com/docs/launch/using/get-started/quick-start.html?lang=en#get-started): Volledige documentatie voor Starten, met inbegrip van een meer diepgaande gids aan de slag
* [Adobe Experience Platform Launch-kanaal](https://experienceleague.adobe.com/?tag=Launch#recommended/solutions/experience-platform): Leer hoe u Starten via video&#39;s kunt gebruiken

## Volgende stappen

[Implementeer uw analytische implementatie in uw ontwikkelomgeving](deploy-dev.md): De code Analytics van de Krijg werkend in een testmilieu.
