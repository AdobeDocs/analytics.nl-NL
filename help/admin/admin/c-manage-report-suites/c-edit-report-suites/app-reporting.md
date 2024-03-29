---
description: Afmetingen en metriek inschakelen voor gebruik bij het bijhouden van mobiele toepassingen.
title: Toepassingsrapportage
feature: Admin Tools
exl-id: ec19695a-2961-45e4-bf44-434f0ff9e3c9
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Toepassingsrapportage

Met de interface App Reporting kunt u de afmetingen en metriek van de levenscyclus voor gebruik in het bijhouden van mobiele toepassingen inschakelen.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL App Management]** > **[!UICONTROL App Reporting]**

>[!IMPORTANT]
>
>Nadat een van deze functies is ingeschakeld, kunnen ze niet meer worden uitgeschakeld. Als u een bepaalde functie inschakelt, zijn de respectieve afmetingen en maatstaven permanent beschikbaar in Analysis Workspace.

## [!UICONTROL App Reports]

[!UICONTROL App Reports] de afmetingen en meetwaarden worden gebruikt voor de volgende doeleinden:

* **Verwerving**: URL&#39;s met verwijzingen bijhouden voor downloadcampagnes voor apps.
* **Levenscyclus**: Het niveau van de stichting van rapportering verstrekt door meting die op elke app lancering wordt verzonden.
* **Toepassingshandelingen**: rapporteert en plakt op basis van handelingen in de app.
* **Lifetime-waarde**: Begrijp hoe gebruikers in de loop der tijd waarde opbouwen met app-KPI&#39;s (zoals aankopen, weergaven, voltooide video, sociale aandelen, uploaden van foto&#39;s).
* **Geteste gebeurtenissen**: Meet de hoeveelheid tijd die verstrijkt (in-app en totale tijd) tussen de belangrijkste handelingen van de app (bijvoorbeeld het tijdstip vóór de eerste aankoop).

Wanneer u [!UICONTROL App Reports]zijn de volgende afmetingen beschikbaar:

* [!UICONTROL Action Name] (met [Invoer](/help/components/dimensions/entry-dimensions.md) en [Afsluiten](/help/components/dimensions/exit-dimensions.md) afmetingen)
* [!UICONTROL App Id]
* [!UICONTROL Acquisition Content]
* [!UICONTROL Acquisition Medium]
* [!UICONTROL Acquisition Name]
* [!UICONTROL Acquisition Source]
* [!UICONTROL Acquisition Term]
* [!UICONTROL Day of Week (SDK)]
* [!UICONTROL Days Since First Use]
* [!UICONTROL Days Since Last Use]
* [!UICONTROL Device Name (SDK)]
* [!UICONTROL Hour of Day (SDK)]
* [!UICONTROL First Launch Date]
* [!UICONTROL Launch Number]
* [!UICONTROL Lifetime Value (evar)]
* [!UICONTROL Operating System Version (SDK)]
* [!UICONTROL Resolution (SDK)]

De volgende cijfers zijn beschikbaar:

* [!UICONTROL Action Time In App]
* [!UICONTROL Action Time Total]
* [!UICONTROL Crashes]
* [!UICONTROL First Launches]
* [!UICONTROL Launches]
* [!UICONTROL Lifetime Value (event)]
* [!UICONTROL Total Session Length]
* [!UICONTROL Upgrades]

## [!UICONTROL Location Tracking]

[!UICONTROL Location Tracking] de afmetingen worden gebruikt voor de volgende doeleinden:

* Breedte- en lengtegegevens bijhouden
* Identificeer, creeer, en visualiseer specifieke Punten van belang. De aandachtspunten moeten in het mobiele configuratiedossier van SDK worden bepaald.
* Bluetooth-bakens bijhouden (UUID, major, minor en proximity).

Wanneer u [!UICONTROL Location Tracking]zijn de volgende afmetingen beschikbaar:

* [!UICONTROL Beacon Major] (met [Invoer](/help/components/dimensions/entry-dimensions.md) en [Afsluiten](/help/components/dimensions/exit-dimensions.md) afmetingen)
* [!UICONTROL Beacon Minor] (met [Invoer](/help/components/dimensions/entry-dimensions.md) en [Afsluiten](/help/components/dimensions/exit-dimensions.md) afmetingen)
* [!UICONTROL Beacon Proximity] (met [Invoer](/help/components/dimensions/entry-dimensions.md) en [Afsluiten](/help/components/dimensions/exit-dimensions.md) afmetingen)
* [!UICONTROL Beacon UUID] (met [Invoer](/help/components/dimensions/entry-dimensions.md) en [Afsluiten](/help/components/dimensions/exit-dimensions.md) afmetingen)
* [!UICONTROL Location (down to 10 km)]
* [!UICONTROL Location (down to 100 m)]
* [!UICONTROL Location (down to 1 m)]
* [!UICONTROL Point of Interest Name]
* [!UICONTROL Distance to Point of Interest Center]
* [!UICONTROL Point of Interest ID]

## [!UICONTROL Voice and Chatbots]

[!UICONTROL Voice and Chatbots] Met afmetingen en maatstaven kunt u spraakassistenten meten, zoals Alexa of Google Home. Het staat u ook toe om thuis-geteelde praatjebots te meten. Tot de meeteigenschappen behoren:

* **Levenscyclus**: Het niveau van de stichting van rapportering voor om het even welke app, zoals het aantal lanceringen en platformtype.
* **Gesprek**: De intents van maatregelen, reacties, en andere metriek en dimensies met betrekking tot het gesprek.

Wanneer u [!UICONTROL Voice and Chatbots]zijn de volgende afmetingen beschikbaar:

* [!UICONTROL Voice Device Capabilities] (met [Invoer](/help/components/dimensions/entry-dimensions.md) en [Afsluiten](/help/components/dimensions/exit-dimensions.md) afmetingen)
* [!UICONTROL Voice Authentication]
* [!UICONTROL Voice Error Type]
* [!UICONTROL Voice Intent]
* [!UICONTROL Voice App Response]
* [!UICONTROL Voice Language]

De volgende cijfers zijn beschikbaar:

* [!UICONTROL Voice End Session]
* [!UICONTROL Voice Error]
* [!UICONTROL Voice Utterances]

## Verouderde rapportage en attributie voor achtergrondeits

Oudere rapporten betekenen dat hits die worden gegenereerd wanneer een toepassing zich op de achtergrond bevindt, worden behandeld als normale voorgrondresultaten. Ze verschijnen in rapporten en beïnvloeden de attributie. Deze oudere configuratie is doorgaans gewenst om consistentie met oudere implementaties te behouden.

Adobe raadt u aan de oudere rapportage uit te schakelen, zodat achtergrondopdrachten niet zichtbaar zijn. Als u achtergrondtreffers in uw analyse wilt omvatten, kunt u toelaten [Virtuele rapportsuite](/help/components/vrs/vrs-about.md) instellen **[!UICONTROL Include background hits]**.
