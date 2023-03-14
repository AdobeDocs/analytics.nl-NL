---
title: Pakketanalysatoren
description: De analysatoren van het pakket laten u de gegevens bekijken die door uw implementatie aan de servers van de Adobe gegevensinzameling worden verzonden.
keywords: packet sniffer, http status, 200, 302, charles
feature: Validation
exl-id: db077293-f72c-4933-8a30-f1e1963f332e
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Pakketanalysatoren

De analysatoren van het pakket laten u de gegevens bekijken die door uw implementatie aan de servers van de Adobe gegevensinzameling worden verzonden.

Net als bij de Adobe Experience Cloud-foutopsporing geeft een pakketmonitor aan welke gegevensparameters in een afbeeldingsaanvraag worden doorgegeven. echter, de pakketmonitors verstrekken toegevoegde functionaliteit:

* Aanvragen voor het bijhouden van aangepaste koppelingen weergeven
* Aanvragen voor afbeeldingen weergeven met andere implementatiemethoden dan JavaScript, zoals aanvragen voor afbeeldingen met harde codes of [!DNL Appmeasurement]

Om de verzoeken van Analytics te bekijken, filter uitgaande verzoeken gebruikend &quot;b/ss&quot;.

In zeer zeldzame gevallen zal debugger een beeldverzoek melden hoewel geen verzoek het aan Adobe maakt [!DNL Analytics] verwerkingsservers. Het gebruiken van een pakketmonitor is een grote manier om 100% zeker te zijn dat een specifiek beeldverzoek met succes in brand wordt gestoken.

Hoewel Adobe geen officiële pakketmonitor biedt, zijn er een groot aantal van deze monitoren beschikbaar op internet. Hier volgen enkele voorbeelden van pakketmonitoren die anderen nuttig hebben gevonden.

>[!TIP]
>
>Deze lijsten zijn niet bedoeld als volledig, maar als informatie over veelgebruikte monitoren.

| Firefox | Internet Explorer | Chroom | Zelfstandige programma&#39;s |
|---|---|---|---|
| [Punt waarnemen](https://www.observepoint.com/product#plugin) (tagviewer) | [HttpWatch](https://www.httpwatch.com/) | [Punt waarnemen](https://www.observepoint.com/product#plugin) (tagviewer) | [Charles](https://www.charlesproxy.com/) |
| [HttpFox](https://addons.thunderbird.net/en-us/firefox/addon/httpfox/) |  | [Chrome Developer Tools](https://code.google.com/chrome/devtools/docs/overview.html) | [Fiddler](https://www.fiddler2.com/fiddler2/) |
| [Tampergegevens](https://addons.mozilla.org/en-US/firefox/addon/tamper-data-for-ff-quantum/) |  | [Firebug Lite](https://chrome.google.com/webstore/detail/firebug-lite-for-google-c/ehemiojjcpldeipjhjkepfdaohajpbdo) | [Wireshark](https://www.wireshark.org/) |
| [HttpWatch](https://www.httpwatch.com/) |  |  |  |
| [Firebug](https://getfirebug.com/) |  |  |  |

>[!NOTE]
>
>Adobe steunt of lost GEEN kwesties problemen op u met deze pakketmonitors ervaart. Raadpleeg de bronlocatie van de pakketmonitor voor hulp.

## Typische HTTP-responsstatuscodes

Wanneer AppMeturement gegevens naar de servers van de Adobe- gegevensinzameling verzendt, antwoorden de servers met een code van de reactiestatus.

* **200 OK**: De gemeenschappelijkste reactie van de servers van de gegevensinzameling. De afbeeldingsaanvraag is ontvangen en er is een transparante afbeelding geretourneerd.
* **302 GEVONDEN**: Er zijn een paar mogelijke redenen om dit antwoord te ontvangen:
   * De eerste aanvraag voor een afbeelding van een bezoeker: Omleiding vindt plaats als een gebruiker uw site voor het eerst bezoekt. Deze omleiding is bedoeld om een bezoekerscookie te verkrijgen. Het heeft geen invloed op de gegevensverzameling.
   * Integratie tussen Comscore en Adobe: Als uw organisatie een integratie Comscore/Analytics gebruikt, resulteert elk beeldverzoek altijd in een 302 reactie.
* **404 NIET GEVONDEN**: Dit antwoord betekent dat het beeldverzoek niet werd gevonden, en de gegevens worden niet verzonden naar de servers van de Adobe- gegevensinzameling. Dit antwoord is ook mogelijk wanneer aanvragen voor afbeeldingen met een hardcodering niet correct zijn opgemaakt. Werk samen met de persoon of het team die Analytics heeft geïmplementeerd om dit probleem op te lossen.

## NS_BINDING_ABORTED in responscodes

Dit bericht komt voor omdat het verzoek van de verbinding het volgen beeld wordt ontworpen om browser aan de volgende pagina te laten te werk gaan alvorens op een reactie van de servers van de Adobe gegevensinzameling te wachten.

is gewoon een lege, transparante afbeelding van 1 x 1, die niet relevant is voor de inhoud van de pagina. Als u een lijnpunt in uw pakketmonitor van Adobe ziet, of met een **[!UICONTROL 200 OK]** reactie of een **[!UICONTROL NS_BINDING_ABORTED]** De gegevens hebben Adobe servers bereikt. De pagina hoeft niet langer te worden gewacht.

De pakketmonitors die als stop-in worden geïntegreerd zien zelden de volledige reactie. Zij zien het verzoek meestal als afgebroken omdat het volledige antwoord niet is ontvangen. Deze monitoren maken ook zelden onderscheid tussen het feit of het verzoek of het antwoord is afgebroken. Een stand-alone pakketmonitor heeft typisch gedetailleerdere berichten en rapporteert de status nauwkeuriger. Een gebruiker kan bijvoorbeeld een bericht ophalen in *Charles* zeggen &quot;De cliënt gesloten verbinding alvorens volledige reactie te ontvangen.&quot; Dit betekent dat de gegevens onze servers bereikten, alleen de browser naar de volgende pagina ging voordat de pixel 1x1 werd ontvangen.

Als een externe pakketmonitor meldt dat het verzoek van de gegevensinzameling, eerder dan de reactie wordt geaborteerd, is dit een reden tot zorg. Adobe [!DNL Customer Care] kan hulp bieden bij het oplossen van problemen.
