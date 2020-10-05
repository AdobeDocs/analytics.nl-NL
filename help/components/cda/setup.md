---
title: Apparaatanalyse instellen
description: Configureer een virtuele rapportsuite om CDA in te schakelen.
translation-type: tm+mt
source-git-commit: 60fe85adaebee8ca390e59727dda949c12c1ee26
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---


# Apparaatanalyse instellen

Als aan alle voorwaarden is voldaan, voert u de volgende stappen uit om Apparaatanalyse op andere apparaten in te schakelen. U moet tot een groep van de Admin van het Profiel van het Product behoren of beheerdervoorrechten in Adobe Analytics hebben om deze stappen te volgen.

>[!IMPORTANT]
>
>Aan alle voorwaarden moet worden voldaan voordat u deze stappen uitvoert. Als niet aan alle voorwaarden wordt voldaan, is de functie niet beschikbaar of werkt deze niet. Zie de [overzichtspagina](overview.md) en de gewenste tekenmethode ([Veldgebaseerde stitching](field-based-stitching.md) of Grafiek [van het](device-graph.md)Apparaat, respectievelijk) voor eerste vereisten en beperkingen.

## Kies de rapportsuite voor alle apparaten die wordt ingeschakeld voor CDA

Wanneer uw organisatie is ingericht om CDA te gebruiken, kiest u welke rapportsuite moet worden gebruikt. Deze keuze kan via uw accountmanager van Adobe worden doorgegeven. Adobe laat dan uw gekozen rapportreeks voor CDA verwerking toe.

## Maak een virtuele-rapportsuite voor meerdere apparaten om de apparaatweergave te bekijken

Beheerders die toegang hebben tot het maken van virtuele rapportsuites, kunnen als volgt virtuele CDA-rapportensuites maken:

1. Navigeer naar [Experience.adobe.com](https://experiencecloud.adobe.com) en meld u aan met uw Adobe-id-referenties.
2. Klik op het pictogram met het 9-raster bovenaan en klik vervolgens op Analytics.
3. Houd de muis boven Componenten en klik vervolgens op Virtuele rapportsets.
4. Klik op Toevoegen.
5. Voer een naam in voor uw virtuele-rapportsuite en zorg ervoor dat de CDA-compatibele rapportsuite is geselecteerd.
6. (Optioneel) Pas een segment toe op de virtuele rapportsuite. Bijvoorbeeld, kunt u een segment toepassen dat de virtuele rapportreeks tot data beperkt nadat CDA werd aangezet en het stitching begon. Dit segment staat gebruikers toe om slechts gestikte datumwaaiers binnen VRS te zien.
7. Klik op het selectievakje &#39;Tijdverwerking rapport inschakelen&#39;, waarmee u meer opties kunt inschakelen, waaronder Apparaatanalyse.
8. Klik op het selectievakje &#39;Gebruikersbezoeken op apparaten plaatsen&#39;.
9. Klik op Doorgaan, voltooi de configuratie van de virtuele rapportsuite en klik op Opslaan.

![CDA-selectievakje](assets/cda-checkbox.png)

## Toevoegingen en wijzigingen aan virtuele-rapportsuites voor meerdere apparaten

Houd rekening met de volgende wijzigingen wanneer Apparaatanalyse is ingeschakeld voor een virtuele rapportsuite:

* Er verschijnt een nieuw apparaatpictogram naast de naam van de virtuele rapportsuite. Dit pictogram is exclusief voor virtuele rapportsuites op meerdere apparaten.
* Er is een nieuwe dimensie beschikbaar met het label [Identified state](../dimensions/identified-state.md) . Deze dimensie bepaalt of de Experience Cloud-id op die hit bekend is door de apparaatgrafiek op dat moment.
* Er zijn nieuwe metriek beschikbaar met het label [Personen](../metrics/people.md) en [Unieke apparaten](../metrics/unique-devices.md) .
* De metrische [Unieke Bezoekers](../metrics/unique-visitors.md) zijn niet beschikbaar, omdat deze worden vervangen door &#39;Mensen&#39; en &#39;Unieke Apparaten&#39;.
* Bij het maken van segmenten wordt de segmentcontainer &#39;Visitor&#39; vervangen door een container &#39;Person&#39;.
