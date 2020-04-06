---
title: Pakketanalysatoren
description: Met pakketanalysatoren kunt u de gegevens weergeven die door uw implementatie naar Adobe-servers voor gegevensverzameling worden verzonden.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Pakketanalysatoren

Met pakketanalysatoren kunt u de gegevens weergeven die door uw implementatie naar Adobe-servers voor gegevensverzameling worden verzonden.

Net als bij de Adobe Experience Cloud-foutopsporing, geeft een pakketmonitor aan welke gegevensparameters worden doorgegeven in een afbeeldingsaanvraag. echter, de pakketmonitors verstrekken toegevoegde functionaliteit:

* Aanvragen voor het bijhouden van aangepaste koppelingen weergeven
* Aanvragen voor afbeeldingen weergeven met andere implementatiemethoden dan JavaScript, zoals aanvragen voor afbeeldingen met harde codes of [!DNL Appmeasurement]

Om de verzoeken van Analytics te bekijken, filter uitgaande verzoeken gebruikend &quot;b/ss&quot;.

In zeer zeldzame gevallen rapporteert de debugger een aanvraag voor een image, hoewel er geen aanvraag is ingediend bij de [!DNL Analytics] verwerkingsservers van Adobe. Het gebruiken van een pakketmonitor is een grote manier om 100% zeker te zijn dat een specifiek beeldverzoek met succes in brand wordt gestoken.

Hoewel Adobe geen officiële pakketmonitor biedt, zijn er een groot aantal van deze monitoren beschikbaar op internet. Hier volgen enkele voorbeelden van pakketmonitoren die anderen nuttig hebben gevonden.

>[!NOTE] Deze lijsten zijn niet bedoeld als volledig, maar als informatie over veelgebruikte monitoren. Als u een pakketmonitor hebt die u met succes gebruikt en nuttig vindt, voelt u vrij om terugkoppelen te verstrekken gebruikend de [!UICONTROL Feedback] knoop op de rechterkant van dit venster.

| Firefox | Internet Explorer | Chroom | Zelfstandige programma&#39;s |
|---|---|---|---|
| [Punt](https://www.observepoint.com/product#plugin) waarnemen (tagviewer) | [HttpWatch](https://www.httpwatch.com/) | [Punt](https://www.observepoint.com/product#plugin) waarnemen (tagviewer) | [Charles](https://www.charlesproxy.com/) |
| [HttpFox](https://addons.mozilla.org/en-US/firefox/addon/httpfox/) |  | [Chrome Developer Tools](https://code.google.com/chrome/devtools/docs/overview.html) | [Fiddler](https://www.fiddler2.com/fiddler2/) |
| [Tampergegevens](https://addons.mozilla.org/en-us/firefox/addon/tamper-data/) |  | [Firebug Lite](https://chrome.google.com/webstore/detail/bmagokdooijbeehmkpknfglimnifench) | [Wireshark](https://www.wireshark.org/) |
| [HttpWatch](https://www.httpwatch.com/) |  |  |  |
| [Firebug](https://getfirebug.com/) |  |  |  |

>[!NOTE] Adobe biedt geen ondersteuning voor problemen die zich bij deze pakketmonitoren kunnen voordoen, of lost deze problemen niet op. Raadpleeg in plaats daarvan de bronlocatie van de pakketmonitor voor hulp.

## NS_BINDING_ABORTED in responscodes

Deze fout treedt op omdat de aanvraag voor het bijhouden van koppelingen zo is ontworpen dat de browser naar de volgende pagina kan gaan voordat wordt gewacht op een reactie van de servers voor gegevensverzameling van Adobe.

Het antwoord van Adobe op het verzoek om een afbeelding is gewoon een lege, transparante afbeelding van 1 x 1 die niet relevant is voor de inhoud van de pagina. Als u een lijstitem in uw pakketmonitor van Adobe ziet, of met een **[!UICONTROL 200 OK]** reactie of een **[!UICONTROL NS_BINDING_ABORTED]** reactie, hebben de gegevens onze servers bereikt. De pagina hoeft niet langer te worden gewacht.

De pakketmonitors die als stop-in worden geïntegreerd zien zelden de volledige reactie. Zij zien het verzoek meestal als afgebroken omdat het volledige antwoord niet is ontvangen. Deze monitoren maken ook zelden onderscheid tussen het feit of het verzoek of het antwoord is afgebroken. Een stand-alone pakketmonitor heeft typisch gedetailleerdere berichten en rapporteert de status nauwkeuriger. Bijvoorbeeld, kan een gebruiker een bericht in *Charles* krijgen die &quot;Cliënt gesloten verbinding alvorens volledige reactie te ontvangen.&quot;zegt Dit betekent dat de gegevens onze servers bereikten, alleen de browser naar de volgende pagina ging voordat de pixel 1x1 werd ontvangen.

Als een externe pakketsniffer meldt dat het verzoek van de gegevensinzameling, eerder dan de reactie wordt geaborteerd, is dit een reden tot zorg. Adobe [!DNL Customer Care] kan hulp bieden bij het oplossen van problemen.
