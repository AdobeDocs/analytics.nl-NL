---
description: Veelgestelde vragen over het instellen, configureren en gebruiken van functies in Activity Map.
title: Veelgestelde vragen over Activity Map
uuid: e4f6d4e2-55d1-4e32-bf70-a334178af370
feature: Activity Map
role: User, Admin
exl-id: 6b2767cb-6c2c-4bf3-b9a9-a23418624650
source-git-commit: 0570bea923edc21a0f185f49fd6f604115d4a6e1
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 1%

---

# Veelgestelde vragen over Activity Map

Veelgestelde vragen over het instellen, configureren en gebruiken van functies in Activity Map.

+++Hebben alle klanten van Analytics toegang tot de pagina van Activiteiten ActivityMap Enablement van Admin Tools?
Organisaties met een contract voor Adobe Analytics Standard, Premium en Ultimate hebben toegang tot Activity Map.
+++

+++Hoe biedt Activity Map ondersteuning voor toepassingen van één pagina (SPA)?
Om de paar seconden scant de Activity Map de webpagina, waarbij wordt gezocht naar wijzigingen in de pagina. ActivityMap zoekt naar nieuwe inhoud op de pagina zonder dat een nieuwe pagina moet worden geladen, maar deze nieuwe inhoud wordt altijd toegewezen aan de eerste pageName die wordt gevonden wanneer de pagina is geladen.

* Activity Map controleert of de zichtbaarheid van koppelingen die het kent, is gewijzigd. Als een wijziging in de zichtbaarheid wordt gevonden, wordt de kolom Aanwezigheid van koppelingen in de paginatabel voor die koppeling bijgewerkt met [!UICONTROL Displayed] of [!UICONTROL Hidden].

* Wanneer gebruikersinteractie tot nieuwe inhoud leidt, zullen om het even welke nieuwe elementen die door AppMeasurement om als verbinding worden gevonden worden toegevoegd aan [!UICONTROL Links On Page] tabel. De Activity Map verzendt een nieuw gegevensverzoek dat deze nieuwe verbindingen omvat. De nieuwe koppelingen moeten worden weergegeven in het dialoogvenster [!UICONTROL Links On Page] lijst wanneer het gegevensverzoek door UI wordt behandeld.
+++

+++Verstrekt de Activity Map gegevens over &quot;meningen&quot;?
Nee, Adobe houdt geen koppelingen bij die zijn weergegeven.
+++

+++Welke browsers en versies worden door de Activity Map ondersteund?
Activity Map ondersteunt de nieuwste versie van de meeste moderne browsers.
+++

+++Verhoogt de Activity Map servervraag?
Activity Map verzendt geen servervraag door zich. In plaats daarvan worden Activity Map-contextgegevensvariabelen opgenomen in de paginaweergaveaanroepen voor Analytics op de volgende pagina.
+++

+++Waarom ontbreken sommige gerangschikte itemoverlays?
Bepaalde gerangschikte koppelingen, zoals submenukoppelingen, worden niet op de pagina weergegeven. Daarom worden de bijbehorende koppelingsoverlays niet weergegeven. Rank wordt berekend voor alle koppelingen op de pagina, inclusief verborgen koppelingen.
+++

+++Hoe wordt de rangorde van koppelingen bepaald in het rapport Alle koppelingen?**
* **In de modus Verloop en Bubbel**: Rang wordt bepaald door de metrische kolom. Voor verbindingen met zelfde metrische waarde, is de rang verder gebaseerd op verbinding ID alfabetische orde.
* **In de modus Gainer &amp; Loser**: Rank wordt voornamelijk bepaald door de kolom % verbreding. Voor koppelingen met dezelfde versterking is de rangorde verder gebaseerd op de alfabetische volgorde van de koppelings-id.
+++

+++Hoe werkt de Activity Map met pagina&#39;s die veelvoudige rapportreeksen gebruiken?
Standaard gebruikt Activity Map de rapportsuite die is gekoppeld aan de eerste tag die door de pagina wordt verzonden. U kunt een andere gelabelde rapportsuite selecteren via het dialoogvenster **[!UICONTROL Activity Map Settings]** > **[!UICONTROL Others]** tab.
+++

+++Hoe lang wordt de Activity Map gescand op Adobe Analytics op de pagina?
Activiteitenoverzicht scant tot 20 seconden na een gebeurtenis van het voltooien van een pagina op de aanwezigheid van Adobe Analytics.
+++

+++Hoe verwerkt Activity Map dynamische inhoud?
De Activity Map controleert om de 2 seconden om te zien of heeft het veranderingen in de staat van de Web-pagina zoals gevonden:

* HTML-inhoud die zichtbaar is geworden
* Verborgen HTML-inhoud
* Nieuwe HTML-inhoud die is geïnjecteerd

Als inhoud wordt verborgen of weergegeven, wijzigt de toepassing automatisch de gewijzigde staat van de koppelingen (en dus de bedekkingen) van verborgen naar verborgen of verborgen. Als nieuwe inhoud wordt geïnjecteerd, haalt de toepassing de bijbehorende koppelingen op, haalt de toepassing analytische gegevens voor deze koppelingen op en voegt overlays voor deze koppelingen toe.
+++

+++Welke metrisch is het rapport van de Stroom van de Pagina op wordt gebaseerd?
Alle weergegeven gegevens zijn gebaseerd op paginaweergaven.
+++

+++Kan ik Activity Map contextgegevensvariabelen door gegevensvoer uitvoeren?
Ja. De [Gegevenskolommen](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) het gebruik van de Activity Map `clickmaplink`, `clickmaplinkbyregion`, `clickmappage`, en `clickmapregion`.
+++

+++Werken de segmenten in de live modus?
Nee, segmenten werken niet in de live modus. De functionaliteit is gelijk aan die van rapportering in real time in Rapporten &amp; Analytics, die geen segmentatie steunen.
+++

+++Is Activity Map compatibel met virtuele rapportsuites?
Ja. Vanwege beperkingen van de virtuele rapportsuite is de live modus van de Activity Map echter niet compatibel met virtuele rapportsuites.
+++

+++Hoe kan ik Activity Map onbruikbaar maken?
U hebt drie opties:

* Verwijder de `AppMeasurement_Module_ActivityMap` functie uit het JS-bestand
* Voeg aangepaste code toe die de bovenstaande functie herschrijft met een lege hoofdtekst, bijvoorbeeld:

   ```js
   function AppMeasurement_Module_ActivityMap() {}
   ```

* AppMeasurement configureren door het instellen `s.trackClickMap` en `s.trackInlineStats` tot `false`
+++
