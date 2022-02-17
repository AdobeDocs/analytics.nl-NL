---
title: Een ontwikkelimplementatie valideren en publiceren naar productie
description: Leer hoe u Adobe Experience Platform-tags kunt gebruiken om Adobe Analytics in uw productieomgeving te implementeren.
feature: Launch Implementation
exl-id: 2f5bcfee-d75e-4dac-bea9-91c6cc545173
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Een ontwikkelimplementatie valideren en publiceren naar productie

Zodra uw tagbibliotheek aan productie wordt geduwd, kan uw organisatie beginnen Adobe Analytics te gebruiken om basisrapporten te trekken.

>[!NOTE]
>Adobe Experience Platform Launch is omgedoopt tot een reeks technologieën voor gegevensverzameling in Experience Platform. Diverse terminologische wijzigingen zijn als gevolg hiervan in de productdocumentatie doorgevoerd. Raadpleeg het volgende [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) voor een geconsolideerde referentie van de terminologische wijzigingen.

## Vereisten

[Implementeer uw analytische implementatie in uw ontwikkelomgeving](deploy-dev.md): Er moet een analytische implementatie naar uw ontwikkelomgeving worden gepubliceerd om deze pagina te kunnen volgen.

## Valideer uw dev implementatie gebruikend debugger van de Experience Cloud

Foutopsporing in Experience Cloud is een Chrome-plug-in die alle Experience Cloud-tags op een pagina weergeeft.

1. Openen [Chrome-webbrowser](https://www.google.com/chrome/) en ga naar [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj) in de Chrome Web Store om de extensie te installeren.
2. Navigeer naar uw ontwikkelingswebsite waarop u tags hebt geïmplementeerd.
3. Klik op het Adobe Experience Cloud-foutopsporingspictogram rechtsboven in Chrome
4. Als alles correct is geïmplementeerd, ziet u de inhoud in Adobe Analytics, tags en de Adobe Experience Cloud Visitor ID-service:

![foutopsporing][assets/debugger.png]

## Implementeer uw dev-implementatie in stappen/vooruit

Zodra u hebt bevestigd u gegevens ziet, kunt u uw implementatie aan de levende versie van uw plaats duwen.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de eigenschap tag die u op uw site wilt implementeren.
1. Klik op de knop **[!UICONTROL Publishing]** en zoek de bibliotheek in de ontwikkelingskolom.
1. Klik op het vervolgkeuzemenu in de bibliotheek en selecteer vervolgens **[!UICONTROL Submit for Approval]**. Klikken **[!UICONTROL Submit]** in het modale venster.
1. Klik nogmaals op het vervolgkeuzemenu van de bibliotheek (nu in de kolom Verzenden) en selecteer **[!UICONTROL Build for Staging]**.
1. Na enkele ogenblikken wordt het geel gekleurde licht op de bibliotheek groen, wat aangeeft dat het is gemaakt.
1. Klik nogmaals op het vervolgkeuzemenu van de bibliotheek en selecteer **[!UICONTROL Approve for Publishing]**.
1. Klik nogmaals op het vervolgkeuzemenu van de bibliotheek (nu in het dialoogvenster [!UICONTROL Approved] kolom) en selecteer **[!UICONTROL Build and Publish to Production]**.
1. Ga naar het tabblad Omgevingen en klik op **[!UICONTROL Production Environment]**.
1. Kopieer de koptekst- en voettekstcode voor de productie en geef deze door aan de eigenaars van uw website. Vraag of zij deze code in de productieomgeving van uw site willen implementeren.

## De productieimplementatie valideren

Bevestig dat u gegevens op de live versie van uw site ziet en dat u met de officiële gegevensverzameling voor Adobe Analytics begint.

1. Nadat u van de eigenaars van uw website hebt bevestigd dat ze de code naar de productie hebben geduwd, navigeert u naar de homepage van uw website in Chrome en opent u de [!UICONTROL Adobe Experience Cloud debugger].
2. Als alles werkt, zou u gelijkaardige gegevens aan uw tests in uw ontwikkelomgeving moeten zien. U verzamelt nu gegevens op uw site en kunt nu Adobe Analytics gebruiken voor rapportage.

## Problemen oplossen

**Er worden geen gegevens weergegeven in het foutopsporingsprogramma.**

Open op uw site de ontwikkelaarsconsole van de browser (doorgaans F12). Bekijk de broncode van de pagina en zorg ervoor het volgende wordt voldaan:

* De console bevat geen JavaScript-fouten. Werk samen met de eigenaars van uw website om ervoor te zorgen dat alle JS-fouten worden opgelost.
* Koptekstcode is correct geïmplementeerd: Zorg ervoor dat de koptekstcode zich in de `<head>` en of het bestand bestaat.
* De bibliotheek AppMeasurement bestaat: Navigeer rechtstreeks naar de JS-bron om ervoor te zorgen dat het JS-bestand code bevat. Als dit niet het geval is, moet u ervoor zorgen dat elke omgeving is gemaakt en dat de bibliotheek naar de desbetreffende omgeving wordt gepubliceerd.
* Bezig met interfereren van plug-ins: Bepaalde Chrome-plug-ins kunnen voorkomen dat verzoeken om afbeeldingen worden geactiveerd. Schakel plug-ins uit die het verzenden van gegevens naar Adobe kunnen stoppen.

## Volgende stappen

Nu een basisimplementatie is ingesteld, kan uw rol binnen uw organisatie van invloed zijn op welk pad u meer wilt weten over:

* [Een document voor het ontwerp van een oplossing maken](../prepare/solution-design.md): Maak een plan voor hoe u douanevariabelen wilt gebruiken, dan hen opnemen in uw implementatie
* [Ga aan de slag met Analysis Workspace](/help/analyze/analysis-workspace/home.md): Ga naar Adobe Analytics met de vlaggenschipfunctie van het gereedschap.
