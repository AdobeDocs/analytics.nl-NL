---
title: Adobe Analytics implementeren in een ontwikkelomgeving
description: Leer hoe u Adobe Experience Platform Launch gebruikt om Adobe Analytics te implementeren in uw ontwikkelomgeving.
translation-type: tm+mt
source-git-commit: 2ffa989156dd9bc4f6ef9a216e8c06425cc39440

---


# Een ontwikkelimplementatie valideren en publiceren naar productie

Zodra de Adobe Experience Platform Launch-bibliotheek naar de productie is gestuurd, kan uw organisatie Adobe Analytics gaan gebruiken om basisrapporten op te halen.

## Vereisten

[Implementeer uw analytische implementatie in uw ontwikkelomgeving](deploy-dev.md): Er moet een analytische implementatie naar uw ontwikkelomgeving worden gepubliceerd om deze pagina te kunnen volgen.

## Uw ontwikkelimplementatie valideren met de foutopsporingsprogramma voor de Experience Cloud

De Experience Cloud-foutopsporing is een Chrome-plug-in die alle Experience Cloud-tags op een pagina weergeeft.

1. Open de [Chrome-webbrowser](https://www.google.com/chrome/) en ga naar [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj) in de Chrome Web Store om de extensie te installeren.
2. Navigeer naar uw ontwikkelingswebsite waarop u Starten hebt geïmplementeerd.
3. Klik op het foutopsporingspictogram van Adobe Experience Cloud rechtsboven in Chrome
4. Als alles correct is geïmplementeerd, ziet u de inhoud in Adobe Analytics, Adobe Experience Platform Launch en de Adobe Experience Cloud Visitor ID-service:

![foutopsporing][assets/debugger.png]

## Implementeer uw ontwikkelimplementatie in stappen/vooruit

Zodra u hebt bevestigd u gegevens ziet, kunt u uw implementatie aan de levende versie van uw plaats duwen.

1. Ga naar [Adobe Experience Platform Launch](https://launch.adobe.com) en meld u aan als daarom wordt gevraagd.
2. Klik op de eigenschap Starten die u op uw site wilt implementeren.
3. Klik op het tabblad Publiceren en zoek de bibliotheek in de ontwikkelingskolom.
4. Klik op het vervolgkeuzemenu in de bibliotheek en selecteer Verzenden voor goedkeuring. Klik op Verzenden in het modale venster.
5. Klik nogmaals op het vervolgkeuzemenu van de bibliotheek (nu in de kolom Verzenden) en selecteer Samenstellen voor opslaan.
6. Na enkele ogenblikken wordt het geel gekleurde licht op de bibliotheek groen, wat aangeeft dat het is gemaakt.
7. Klik nogmaals op het vervolgkeuzemenu van de bibliotheek en selecteer Goedkeuren voor publicatie.
8. Klik nogmaals op het vervolgkeuzemenu van de bibliotheek (nu in de kolom Goedgekeurd) en selecteer Samenstellen en Publiceren op productie.
9. Ga naar het tabblad Milieu en klik op Productomgeving.
10. Kopieer de koptekst- en voettekstcode voor de productie en geef deze door aan de eigenaars van uw website. Vraag of zij deze code in de productieomgeving van uw site willen implementeren.

## De productieimplementatie valideren

Bevestig dat u gegevens op de live versie van uw site ziet en dat u met de officiële gegevensverzameling voor Adobe Analytics begint.

1. Nadat u van de eigenaars van uw website hebt bevestigd dat ze de opstartcode hebben geproduceerd, navigeert u naar de homepage van uw website in Chrome en opent u de foutopsporing voor Adobe Experience Cloud.
2. Als alles werkt, zou u gelijkaardige gegevens aan uw tests in uw ontwikkelomgeving moeten zien. U verzamelt nu gegevens op uw site en kunt nu Adobe Analytics gebruiken voor rapportage.

## Problemen oplossen

**Er worden geen gegevens weergegeven in het foutopsporingsprogramma.**

Open op uw site de ontwikkelaarsconsole van de browser (doorgaans F12). Bekijk de broncode van de pagina en zorg ervoor het volgende wordt voldaan:

* De console bevat geen JavaScript-fouten. Werk samen met de eigenaars van uw website om ervoor te zorgen dat alle JS-fouten worden opgelost.
* Koptekstcode is correct geïmplementeerd: Zorg ervoor dat de koptekstcode zich binnen de `<head>` tag bevindt en dat het bestand bestaat.
* De bibliotheek AppMeasurement bestaat: Navigeer rechtstreeks naar de JS-bron om ervoor te zorgen dat het JS-bestand code bevat. Als dit niet het geval is, moet u ervoor zorgen dat elke omgeving is gemaakt en dat de bibliotheek naar de desbetreffende omgeving wordt gepubliceerd.
* Bezig met interfereren van plug-ins: Bepaalde Chrome-plug-ins kunnen voorkomen dat verzoeken om afbeeldingen worden geactiveerd. Schakel plug-ins uit die kunnen voorkomen dat gegevens naar de servers van Adobe worden verzonden.

## Volgende stappen

Nu een basisimplementatie is ingesteld, kan uw rol binnen uw organisatie van invloed zijn op het pad waarover u meer wilt weten:

* [Maak een document](../prepare/solution-design.md)voor het ontwerp van een oplossing: Maak een plan voor hoe u douanevariabelen wilt gebruiken, dan hen opnemen in uw implementatie
* [Ga aan de slag met de analysewerkruimte](/help/analyze/analysis-workspace/home.md): Blader naar Adobe Analytics met behulp van de vlaggenschipfunctie van het hulpprogramma.
