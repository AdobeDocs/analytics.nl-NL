---
title: Pakketanalysatoren
description: Met pakketanalysatoren kunt u de gegevens weergeven die door uw implementatie naar Adobe-servers voor gegevensverzameling worden verzonden.
keywords: packet sniffer, http status, 200, 302, charles
feature: Implementation Basics
exl-id: db077293-f72c-4933-8a30-f1e1963f332e
role: Admin, Developer, Leader
source-git-commit: 29ab0cc535bd8f74b50428c11756bf8b446a23ab
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# Pakketanalysatoren

Met pakketanalysatoren kunt u de gegevens weergeven die door uw implementatie naar Adobe-servers voor gegevensverzameling worden verzonden.

Net als bij de Adobe Experience Cloud-foutopsporing geeft een pakketmonitor aan welke gegevensparameters in een afbeeldingsaanvraag worden doorgegeven; pakketmonitors bieden echter extra functionaliteit:

* Aanvragen voor het bijhouden van aangepaste koppelingen weergeven
* Aanvragen voor afbeeldingen weergeven met andere implementatiemethoden dan JavaScript, zoals aanvragen voor afbeeldingen met harde codes of [!DNL Appmeasurement]

Om de verzoeken van Analytics te bekijken, filter uitgaande verzoeken gebruikend &quot;b/ss&quot;.

In zeer zeldzame gevallen rapporteert de debugger een aanvraag voor een image, hoewel er geen aanvraag is die deze naar Adobe [!DNL Analytics] -verwerkingsservers stuurt. Het gebruiken van een pakketmonitor is een grote manier om 100% zeker te zijn dat een specifiek beeldverzoek met succes wordt in brand gestoken.

Hoewel Adobe geen officiële pakketmonitor biedt, zijn er een groot aantal van deze monitoren op het internet. Hier volgen enkele voorbeelden van pakketmonitoren die anderen nuttig hebben gevonden.

>[!TIP]
>
>Deze lijsten zijn niet bedoeld als volledig, maar als informatie over veelgebruikte monitoren.

| Firefox | Internet Explorer | Chrome | Zelfstandige programma&#39;s |
|---|---|---|---|
| [ observeren Punt ](https://www.observepoint.com/product#plugin) (markeringskijker) | [ HttpWatch ](https://www.httpwatch.com/) | [ observeren Punt ](https://www.observepoint.com/product#plugin) (markeringskijker) | [ Karel ](https://www.charlesproxy.com/) |
| [ HttpFox ](https://addons.thunderbird.net/en-us/firefox/addon/httpfox/) |  | [ de Hulpmiddelen van de Ontwikkelaar van Chrome ](https://code.google.com/chrome/devtools/docs/overview.html) | [ Fiddler ](https://www.telerik.com/fiddler) |
| [ Gegevens van de Tamper ](https://addons.mozilla.org/en-US/firefox/addon/tamper-data-for-ff-quantum/) |  | [ Firebug Lite ](https://chromewebstore.google.com/detail/firebug-lite-for-google-c/ehemiojjcpldeipjhjkepfdaohajpbdo) | [ Wireshark ](https://www.wireshark.org/) |
| [ HttpWatch ](https://www.httpwatch.com/) |  |  |  |
| [ Vuurwerk ](https://getfirebug.com/) |  |  |  |

>[!NOTE]
>
>Adobe biedt GEEN ondersteuning voor problemen die u met deze pakketmonitoren ondervindt of lost deze problemen niet op. Raadpleeg de bronlocatie van de pakketmonitor voor hulp.

## Typische HTTP-responsstatuscodes

Wanneer AppMeasurement gegevens verzendt naar Adobe-gegevensverzamelingsservers, reageren servers met een antwoordstatuscode.

* **200 OK**: De gemeenschappelijkste reactie van de servers van de gegevensinzameling. De afbeeldingsaanvraag is ontvangen en er is een transparante afbeelding geretourneerd.
* **302 VOND**: Er zijn een paar mogelijke redenen om deze reactie te ontvangen:
   * Het eerste verzoek om een afbeelding van een bezoeker: een omleiding vindt plaats als een gebruiker uw site voor het eerst bezoekt. Deze omleiding is bedoeld om een bezoekerscookie te verkrijgen. Het heeft geen invloed op de gegevensverzameling.
   * Integratie tussen Comscore en Adobe: als uw organisatie een Comscore/Analytics-integratie gebruikt, resulteert elk verzoek om een afbeelding altijd in een 302-reactie.
* **404 NIET GEVONDEN**: Deze reactie betekent dat het beeldverzoek niet werd gevonden, en het gegeven wordt niet verzonden naar de servers van de de gegevensinzameling van Adobe. Dit antwoord is ook mogelijk wanneer aanvragen voor afbeeldingen met een hardcodering niet correct zijn opgemaakt. Werk samen met de persoon of het team die Analytics heeft geïmplementeerd om dit probleem op te lossen.

## NS_BINDING_ABORTED in responscodes

Dit bericht treedt op omdat de aanvraag voor het bijhouden van koppelingen zo is ontworpen dat de browser naar de volgende pagina kan gaan voordat wordt gewacht op een reactie van de Adobe-servers voor gegevensverzameling.

Het Adobe-antwoord op het verzoek om een afbeelding is gewoon een lege, transparante afbeelding van 1 x 1, die niet relevant is voor de inhoud van de pagina. Als u een lijstitem in uw pakketmonitor van Adobe ziet, met een **[!UICONTROL 200 OK]** reactie of een **[!UICONTROL NS_BINDING_ABORTED]** reactie, hebben de gegevens Adobe-servers bereikt. De pagina hoeft niet langer te worden gewacht.

De pakketmonitors die als stop-in worden geïntegreerd zien zelden de volledige reactie. Zij zien het verzoek meestal als afgebroken omdat het volledige antwoord niet is ontvangen. Deze monitoren maken ook zelden onderscheid tussen het feit of het verzoek of het antwoord is afgebroken. Een stand-alone pakketmonitor heeft typisch gedetailleerdere berichten en rapporteert de status nauwkeuriger. Bijvoorbeeld, kan een gebruiker een bericht in *Karel* krijgen die &quot;Cliënt gesloten verbinding alvorens volledige reactie te ontvangen.&quot; Dit betekent dat de gegevens onze servers bereikten, alleen de browser naar de volgende pagina ging voordat de pixel 1x1 werd ontvangen.

Als een externe pakketmonitor meldt dat het verzoek van de gegevensinzameling, eerder dan de reactie wordt geaborteerd, is dit een reden tot zorg. Adobe [!DNL Customer Care] kan hulp bieden bij het oplossen van problemen.
