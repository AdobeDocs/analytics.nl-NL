---
title: Een eigenschap Analytics maken in Launch
description: Maak een spatie om aan te passen hoe gegevens worden verzameld met Adobe Experience Platform Launch.
translation-type: tm+mt
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# Een eigenschap Analytics maken in Adobe Experience Platform Launch

Adobe Experience Platform Launch is het programma waarmee u Experience Cloud-oplossingen kunt integreren op uw website (inclusief Analytics). Op deze pagina wordt specifiek beschreven hoe een basisimplementatie van Adobe Analytics correct is geconfigureerd voor een opstartbeheerder.

## Vereisten

[Maak een rapportsuite](/help/admin/admin-console/create-report-suite.md): Een silo maken voor analysegegevens die moeten worden verzameld

## Een eigenschap maken en vitale extensies installeren

Eigenschappen zijn overkoepelende containers die u gebruikt om tags te beheren. Met extensies kunt u productspecifieke tags installeren en configureren.

1. Ga naar [launch.adobe.com](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op Nieuwe eigenschap.
1. Geef uw eigenschap een naam, zoals de titel van uw website, en voer het domein in waarop u Analytics wilt implementeren. Klik op Opslaan.
1. Klik op de nieuwe eigenschap om de instellingen in te voeren.
1. Klik op het tabblad Extensies en klik vervolgens op Catalogus.
1. Ga naar Identiteitsservice en klik op Installeren.
1. Alle instellingen, inclusief de Experience Cloud Organization-id, moeten al worden ingevuld. Klik op Opslaan.
1. Zoek Adobe Analytics terug in de extensiecatalogus en klik op Installeren.

## Gegevenselementen maken voor Adobe Analytics

Gegevenselementen zijn verwijzingen naar specifieke delen van uw site om variabelewaarden te verzamelen.

1. Ga naar [launch.adobe.com](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
2. Klik op de eigenschap Starten die u op uw site wilt implementeren.
3. Klik op het tabblad Gegevenselementen en klik vervolgens op Nieuw gegevenselement maken.
4. Geef het gegevenselement de volgende instellingen:
   * Naam: Paginanaam
   * Extensie: Kern
   * Type gegevenselement: JavaScript-variabele
   * Pad naar variabele: `window.document.title`
      > [!NOTE] Opmerking: Dit is een voorbeeldwaarde om aan de slag te gaan. Als uw organisatie een betere waarde voor paginanaam, zoals een waarde van de gegevenslaag bepaalt, kunt u het hier ingaan.
   * Tekst reinigen ingeschakeld
   * Duur: Voorvertoning
5. Klik op Opslaan.

## Regels maken voor Adobe Analytics

Regels wijzen gegevenselementen aan de veranderlijke waarden van Analytics toe, en bepalen wanneer die waarden naar de servers van Adobe worden verzonden.

1. Ga naar [launch.adobe.com](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op de eigenschap Starten die u op uw site wilt implementeren.
1. Klik op Nieuwe regel maken en geef deze een naam `Global Rule`.
1. Klik op Toevoegen naast gebeurtenissen en voer de volgende instellingen in:
   * Extensie: Kern
   * Type gebeurtenis: Bibliotheek geladen (pagina boven)
   * Naam: Kern - Bibliotheek geladen (pagina boven)
   * Volgorde: 50
1. Klik op Wijzigingen behouden.
1. Klik onder Handelingen op Toevoegen en voer de volgende instellingen in:
   * Extensie: Adobe Analytics
   * Type handeling: Variabelen instellen
   * Paginanaam: Klik op het containerpictogram en selecteer het `Page Name` gegevenselement.
   * Campagne: De parameter van de vraag met een waarde van `cid`
1. Klik op Wijzigingen behouden.
1. Klik op het plusteken naast handelingen om nog een handeling toe te voegen en voer de volgende instellingen in:
   * Extensie: Adobe Analytics
   * Type handeling: Band verzenden
   * Naam: Adobe Analytics - Send Beacon
   * Tekstspatiëring: s.t()
1. Klik op Wijzigingen behouden.
1. Controleer of u de gebeurtenis en twee handelingen hebt ingesteld en klik op Opslaan.

## Documentatie en aanvullende middelen

* [Adobe Analytics-extensiedocumentatie](https://docs.adobelaunch.com/extension-reference/web/adobe-analytics-extension): Volledige documentatie die specifiek is voor de extensie Adobe Analytics in Adobe Experience Platform Launch.
* [Aan de slag met starten](https://docs.adobelaunch.com/getting-started): Volledige documentatie voor Starten, met inbegrip van een meer diepgaande gids aan de slag
* [Adobe Experience Platform Launch YouTube-kanaal](https://www.youtube.com/channel/UCa84ntcvYhPArOBsZIRE2Jw/videos?view=0&shelf_id=0&sort=dd): Leer hoe u Starten via video&#39;s kunt gebruiken

## Volgende stappen

[Implementeer uw analytische implementatie in uw ontwikkelomgeving](deploy-dev.md): De code Analytics van de Krijg werkend in een testmilieu.
