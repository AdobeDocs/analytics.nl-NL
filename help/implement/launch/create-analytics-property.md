---
title: Een Analytics-eigenschap maken in Launch
description: Met Adobe Experience Platform Launch maakt u een spatie om aan te passen hoe gegevens worden verzameld.
translation-type: tm+mt
source-git-commit: a492de4ccbcd6f3f8ca81c9fecbcca4780e0f589
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---


# Een Analytics-eigenschap maken in Adobe Experience Platform Launch

Adobe Experience Platform Launch is het hulpmiddel dat u kunt gebruiken om Experience Cloud-oplossingen op uw website (inclusief Analytics) te integreren. Deze pagina schetst specifiek hoe een beheerder van de Lancering een basisimplementatie van Adobe Analytics kan krijgen correct wordt gevormd.

## Vereisten

[Maak een rapportsuite](/help/admin/admin-console/create-report-suite.md): Een silo maken voor Analytics-gegevens die moeten worden verzameld

## Een eigenschap maken en vitale extensies installeren

Eigenschappen zijn overkoepelende containers die u gebruikt om tags te beheren. Met extensies kunt u productspecifieke tags installeren en configureren.

1. Ga naar [launch.adobe.com](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op Nieuwe eigenschap.
1. Geef uw eigenschap een naam, zoals de titel van uw website, en voer het domein in waarop u Analytics wilt implementeren. Klik op Opslaan.
1. Klik op de nieuwe eigenschap om de instellingen in te voeren.
1. Klik op het tabblad Extensies en klik vervolgens op Catalogus.
1. Ga naar Identiteitsservice en klik op Installeren.
1. Alle instellingen, inclusief de Experience Cloud Organisatie-id, moeten al zijn ingevuld. Klik op Opslaan.
1. Ga terug naar Adobe Analytics in de extensiecatalogus en klik op Installeren.

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

      >[!NOTE] Opmerking: Dit is een voorbeeldwaarde om aan de slag te gaan. Als uw organisatie een betere waarde voor paginanaam, zoals een waarde van de gegevenslaag bepaalt, kunt u het hier ingaan.
   * Tekst reinigen ingeschakeld
   * Duur: Voorvertoning
5. Klik op Opslaan.

## Regels maken voor Adobe Analytics

Regels wijzen gegevenselementen de veranderlijke waarden van Analytics in kaart, en bepalen wanneer die waarden naar Adobe servers worden verzonden.

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

* [Adobe Analytics-extensiedocumentatie](https://docs.adobelaunch.com/extension-reference/web/adobe-analytics-extension): Volledige documentatie specifiek voor de Adobe Analytics-extensie in Adobe Experience Platform Launch.
* [Aan de slag met starten](https://docs.adobelaunch.com/getting-started): Volledige documentatie voor Starten, met inbegrip van een meer diepgaande gids aan de slag
* [Adobe Experience Platform Launch YouTube-kanaal](https://www.youtube.com/channel/UCa84ntcvYhPArOBsZIRE2Jw/videos?view=0&amp;shelf_id=0&amp;sort=dd): Leer hoe u Starten via video&#39;s kunt gebruiken

## Volgende stappen

[Implementeer uw Analytics-implementatie in uw ontwikkelomgeving](deploy-dev.md): Analytics-code laten werken in een testomgeving.
