---
title: Verwerking en architectuurverschillen tussen analytische platforms
description: Leer hoe sommige gegevens worden verzameld en op verschillende platforms worden weergegeven, zoals Adobe Analytics en Google Analytics.
translation-type: tm+mt
source-git-commit: 3211598c2ff43493b329a9be4fb6877ae29cf08b
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---


# Verwerking en architectuurverschillen tussen analytische platforms

Hoewel Adobe Analytics en Google Analytics beide hulpprogramma&#39;s voor Analytics zijn, is de manier waarop gegevens worden verzameld en verwerkt tussen platforms zeer verschillend. Op deze pagina ziet u enkele belangrijke verschillen in de manier waarop bepaalde dimensies en metriek worden verzameld en waarom er verschillende getallen kunnen worden weergegeven in vergelijkbare rapporten.

## [!UICONTROL Bounce Rate]

[!UICONTROL Bounce Rate] is een veelgebruikte PKI die wordt gebruikt om de doeltreffendheid en de relevantie van landingspagina&#39;s in de meeste analysehulpmiddelen te meten. Dit wordt meestal gedefinieerd als bezoeken die de website binnenkomen maar geen klik naar een andere pagina bevatten.

* In Adobe Analytics wordt [!UICONTROL Bounce Rate] berekend met behulp van de formule **Bounces gedeeld door Enter**.
* In Google Analytics wordt [!UICONTROL Bounce Rate] berekend met de formule Sessions **van**&#x200B;één pagina gedeeld door Sessies.

Op beide platforms geldt dat als meerdere hits tijdens hetzelfde bezoek of tijdens dezelfde sessie worden verzonden, dit niet als een stuit wordt beschouwd. In Adobe Analytics zijn aangepaste koppelingen beschikbaar en vaak voorkomende koppelingen, waardoor een bezoek niet als een stuit kan worden beschouwd. Google Analytics verzendt doorgaans niet meer dan één gegevensaanvraag op dezelfde pagina.

Voor een betere pariteit tussen de rapportagegereedschappen gebruikt u de [!UICONTROL Single Page Visits] metrische waarde in Adobe Analytics in plaats van [!UICONTROL Bounces] als onderdeel van een berekende maatstaf. Deze [!UICONTROL Single Page Visits] meting omvat het totale aantal bezoeken dat slechts een paginaweergave bevatte, of bezoeken die de website binnenkomen maar geen klik aan een andere pagina omvatten.

Zie de metrische [Stuitsnelheid](/help/components/c-variables/c-metrics/metrics-bounce-rate.md) in de gebruikersgids van Componenten voor meer informatie.

## [!UICONTROL Visits] en sessies

[!UICONTROL Visits] (ook wel sessies genoemd in Google Analytics) is een groep paginaweergaven die in een korte tijd door dezelfde gebruiker worden gemaakt. [!UICONTROL Visits] op beide platforms verlopen doorgaans na 30 minuten inactiviteit. Beide platforms staan aanpassing toe wanneer een [!UICONTROL Visit] verloopt. Er zijn verscheidene scenario&#39;s die verschillen op elk platform kunnen veroorzaken.

* **Einde van de dag:** Alle sessies in Google Analytics verlopen na 23:59 uur op een bepaalde dag. Als de gebruiker na 12.00 uur nog steeds actief is op uw site, wordt een nieuwe sessie gemaakt. Adobe Analytics gaat de volgende dag door met een bezoek.
* **Verschillende campagnes:** Een nieuwe sessie in Google Analytics wordt gestart als de campagnebron van een gebruiker verandert. Als er een nieuwe [!UICONTROL Tracking Code] waarde wordt weergegeven in Adobe Analytics, wordt deze beschouwd als onderdeel van hetzelfde bezoek.
* **Handmatige sessieoverschrijving:** Een nieuwe sessie in Google Analytics wordt gestart als u een sessie handmatig start of beëindigt. `sessionControl` [!UICONTROL Visits] kan niet handmatig worden beëindigd in Adobe Analytics.
* **Detectie van eerdere bezoeken in Adobe Analytics:** Een nieuwe functie [!UICONTROL Visit] in Adobe Analytics wordt automatisch gestart als een gebruiker 12 uur doorlopende activiteit bereikt, 2500 resultaten of 100 resultaten binnen 100 seconden. Elk van deze detectiecriteria wordt doorgaans geactiveerd door beide activiteiten.

Zie metrisch [Bezoekt](/help/components/c-variables/c-metrics/metrics-visit.md) in de de gebruikersgids van Componenten voor meer informatie.
