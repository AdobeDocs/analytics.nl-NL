---
title: Verwerking en architectuurverschillen tussen analytische platforms
description: Leer hoe sommige gegevens worden verzameld en verschillend worden weergegeven tussen platforms zoals Adobe Analytics en Google Analytics.
feature: Third-party Integration
exl-id: 3e457915-3c2d-49f7-9b77-df18c04d49cd
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Verwerking en architectuurverschillen tussen analytische platforms

Hoewel Adobe Analytics en Google Analytics beide analysehulpmiddelen zijn, is de manier waarop gegevens worden verzameld en verwerkt tussen platforms zeer verschillend. Op deze pagina ziet u enkele belangrijke verschillen in de manier waarop bepaalde dimensies en metriek worden verzameld en waarom er verschillende getallen kunnen worden weergegeven in vergelijkbare rapporten.

## [!UICONTROL Bounce Rate]

[!UICONTROL Bounce Rate] is een veelgebruikte PKI die wordt gebruikt om de doeltreffendheid en de relevantie van landingspagina&#39;s in de meeste analysehulpmiddelen te meten. Dit wordt meestal gedefinieerd als bezoeken die de website binnenkomen maar geen klik naar een andere pagina bevatten.

* In Adobe Analytics: [!UICONTROL Bounce Rate] wordt berekend met behulp van de formule **Bounces gedeeld door Berichten**.
* In Google Analytics, [!UICONTROL Bounce Rate] wordt berekend met behulp van de formule **Sessies van één pagina gedeeld door sessies**.

Op beide platforms geldt dat als meerdere hits tijdens hetzelfde bezoek of tijdens dezelfde sessie worden verzonden, dit niet als een stuit wordt beschouwd. In Adobe Analytics zijn er aangepaste koppelingen beschikbaar en vaak, waardoor een bezoek niet als een stuit kan worden beschouwd. Google Analytics verzenden doorgaans niet meer dan één gegevensaanvraag op dezelfde pagina.

Om een betere pariteit tussen de rapporteringsinstrumenten te bereiken, gebruik [!UICONTROL Single Page Visits] metrisch in Adobe Analytics in plaats van [!UICONTROL Bounces] als onderdeel van een berekende metrische waarde. De [!UICONTROL Single Page Visits] De meting omvat het totale aantal bezoeken die slechts een paginamening omvatten, of bezoeken die de website ingaan maar een klik aan een andere pagina niet omvatten.

Zie de [Stuitsnelheid](/help/components/metrics/bounce-rate.md) metrisch in de de gebruikersgids van Componenten voor meer informatie.

## [!UICONTROL Visits] en sessies

[!UICONTROL Visits] (sessies in Google Analytics genoemd) zijn een groep paginaweergaven die door dezelfde gebruiker in een korte tijd worden gemaakt. [!UICONTROL Visits] op beide platforms verlopen doorgaans na 30 minuten inactiviteit. Beide platforms staan aanpassing toe wanneer een [!UICONTROL Visit] verloopt. Er zijn verscheidene scenario&#39;s die verschillen op elk platform kunnen veroorzaken.

* **Einde van de dag:** Alle sessies in Google Analytics verlopen na 23:59 uur op een bepaalde dag. Als de gebruiker na 12.00 uur nog steeds actief is op uw site, wordt een nieuwe sessie gemaakt. In het kader van hetzelfde bezoek gaat Adobe Analytics de volgende dag verder.
* **Verschillende campagnes:** Een nieuwe sessie in Google Analytics wordt gestart als de campagnebron van een gebruiker verandert. Als een nieuwe [!UICONTROL Tracking Code] In Adobe Analytics wordt deze waarde als onderdeel van hetzelfde bezoek beschouwd.
* **Handmatige sessieoverschrijving:** Een nieuwe sessie in Google Analytics begint als u `sessionControl` om een sessie handmatig te starten of te beëindigen. [!UICONTROL Visits] kan niet handmatig worden beëindigd in Adobe Analytics.
* **Detectie van eerdere bezoeken in Adobe Analytics:** Een nieuwe [!UICONTROL Visit] in Adobe Analytics wordt automatisch gestart wanneer een gebruiker 12 uur ononderbroken activiteit bereikt, 2500 hits of 100 hits binnen 100 seconden. Elk van deze detectiecriteria wordt doorgaans geactiveerd door beide activiteiten.

Zie de [Bezoeken](/help/components/metrics/visits.md) metrisch in de de gebruikersgids van Componenten voor meer informatie.
