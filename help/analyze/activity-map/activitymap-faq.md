---
description: Veelgestelde vragen over het instellen, configureren en gebruiken van functies in Activity Map.
title: Veelgestelde vragen over Activity Map
uuid: e4f6d4e2-55d1-4e32-bf70-a334178af370
feature: Activity Map
role: Business Practitioner, Administrator
exl-id: 6b2767cb-6c2c-4bf3-b9a9-a23418624650
translation-type: tm+mt
source-git-commit: a283ba5d5678498cde9d0065a4f9f6b8a98558dd
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 1%

---

# Veelgestelde vragen over Activity Map

Veelgestelde vragen over het instellen, configureren en gebruiken van functies in Activity Map.

## Hebben alle klanten van Analytics toegang tot de pagina van Activiteiten ActivityMap Enablement Admin Tools?

Organisaties met een contract voor Adobe Analytics Standard, Premium en Ultimate hebben toegang tot Activity Map.

## Hoe biedt Activity Map ondersteuning voor toepassingen van één pagina (SPA)?

Om de paar seconden scant de Activity Map de webpagina, waarbij wordt gezocht naar wijzigingen in de pagina. ActivityMap zoekt naar nieuwe inhoud op de pagina zonder dat een nieuwe pagina moet worden geladen, maar deze nieuwe inhoud wordt altijd toegewezen aan de eerste pageName die wordt gevonden wanneer de pagina is geladen.

* Activity Map controleert of de zichtbaarheid van koppelingen die het kent, is gewijzigd. Als een wijziging in de zichtbaarheid wordt gevonden, wordt de kolom Aanwezigheid van koppelingen voor die koppeling bijgewerkt met [!UICONTROL Displayed] of [!UICONTROL Hidden].

* Wanneer gebruikersinteractie tot nieuwe inhoud leidt, zullen om het even welke nieuwe elementen die door AppMeasurement om een verbinding worden gevonden worden toegevoegd aan de [!UICONTROL Links On Page] lijst. De Activity Map verzendt een nieuw gegevensverzoek dat deze nieuwe verbindingen omvat. De nieuwe verbindingen zouden in [!UICONTROL Links On Page] lijst moeten verschijnen wanneer het gegevensverzoek door UI wordt behandeld.


## Verstrekt de Activity Map gegevens over &quot;meningen&quot;?

Nee, Adobe houdt geen koppelingen bij die zijn weergegeven.

## Welke browsers en versies worden door de Activity Map ondersteund?

Activity Map ondersteunt de nieuwste versie van de meeste moderne browsers.

## Verhoogt de Activity Map servervraag?

Activity Map verzendt geen servervraag door zich. In plaats daarvan worden Activity Map-contextgegevensvariabelen opgenomen in de paginaweergaveaanroepen voor Analytics op de volgende pagina.

## Waarom ontbreken sommige gerangschikte itemoverlays?**

Bepaalde gerangschikte koppelingen, zoals submenukoppelingen, worden niet op de pagina weergegeven. Daarom worden de bijbehorende koppelingsoverlays niet weergegeven. Rank wordt berekend voor alle koppelingen op de pagina, inclusief verborgen koppelingen.

## Hoe wordt de rangorde van koppelingen bepaald in het rapport Alle koppelingen?**

* **In de modus** Verloop en Bubbel: Rang wordt bepaald door de metrische kolom. Voor verbindingen met zelfde metrische waarde, is de rang verder gebaseerd op verbinding ID alfabetische orde.
* **In de modus** Gainer &amp; Loser: Rank wordt voornamelijk bepaald door de kolom % verbreding. Voor koppelingen met dezelfde versterking is de rangorde verder gebaseerd op de alfabetische volgorde van de koppelings-id.

## Hoe werkt Activity Map met pagina&#39;s die veelvoudige rapportreeksen gebruiken?

Standaard gebruikt Activity Map de rapportsuite die is gekoppeld aan de eerste tag die door de pagina wordt verzonden. U kunt een verschillende geëtiketteerde rapportreeks door **[!UICONTROL Activity Map Settings]** > **[!UICONTROL Others]** tabel selecteren.

## Hoe lang scant de Activity Map naar Adobe Analytics op de pagina?

Activiteitenoverzicht scant tot 20 seconden na een gebeurtenis van het voltooien van een pagina op de aanwezigheid van Adobe Analytics.

## Hoe verwerkt Activity Map dynamische inhoud?

De Activity Map controleert om de 2 seconden om te zien of heeft het veranderingen in de staat van de Web-pagina zoals gevonden:

* HTML-inhoud die zichtbaar is geworden
* HTML-inhoud die verborgen is
* Nieuwe HTML-inhoud die is geïnjecteerd

Als inhoud wordt verborgen of weergegeven, wijzigt de toepassing automatisch de gewijzigde staat van de koppelingen (en dus de bedekkingen) van verborgen naar verborgen of verborgen. Als nieuwe inhoud wordt geïnjecteerd, haalt de toepassing de bijbehorende koppelingen op, haalt de toepassing analytische gegevens voor deze koppelingen op en voegt overlays voor deze koppelingen toe.

## Op welke maateenheid is het rapport van de Stroom van de Pagina gebaseerd?

Alle weergegeven gegevens zijn gebaseerd op paginaweergaven.

## Kan ik Activity Map contextgegevensvariabelen door gegevensvoer uitvoeren?

Contextgegevensvariabelen van activiteitsstructuren zijn niet beschikbaar in gegevensfeeds.

## Werken segmenten in de live modus?

Nee, segmenten werken niet in de live modus. De functionaliteit is gelijk aan die van rapportering in real time in Rapporten &amp; Analytics, die geen segmentatie steunen.

## Is de Activity Map compatibel met virtuele rapportsuites?

Ja. Vanwege beperkingen van de virtuele rapportsuite is de live modus van de Activity Map echter niet compatibel met virtuele rapportsuites.
