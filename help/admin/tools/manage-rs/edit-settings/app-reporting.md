---
description: Afmetingen en metriek inschakelen voor gebruik bij het bijhouden van mobiele toepassingen.
title: Toepassingsrapportage
feature: Admin Tools
exl-id: ec19695a-2961-45e4-bf44-434f0ff9e3c9
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
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

[!UICONTROL App Reports] afmetingen en metriek worden gebruikt voor de volgende doeleinden:

* **Verwerving**: Spoor verwijzend URLs voor app downloadcampagnes.
* **Levenscyclus**: Het niveau van de stichting van rapportering die door meting wordt verstrekt die op elke toepassingslancering wordt verzonden.
* **de Acties van de Toepassing**: Rapporten en het kleven die op in-app acties worden gebaseerd.
* **Waarde van het Leven**: Begrijp hoe de gebruikers waarde in tijd opbouwen gebruikend app KPIs (zoals aankopen, en meningen, video voltooit, sociale aandelen, foto uploadt).
* **Gedetailleerde Gebeurtenissen**: Meet de hoeveelheid tijd die (in-app &amp; totale tijd) tussen zeer belangrijke toepassingsacties (zoals tijd vóór eerste aankoop) vervalt.

Wanneer u [!UICONTROL App Reports] inschakelt, zijn de volgende afmetingen beschikbaar:

* [!UICONTROL Action Name] (met [&#x200B; Ingang &#x200B;](/help/components/dimensions/entry-dimensions.md) en [&#x200B; Uitgang &#x200B;](/help/components/dimensions/exit-dimensions.md) dimensies)
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

[!UICONTROL Location Tracking] -afmetingen worden gebruikt voor de volgende doeleinden:

* Breedte- en lengtegegevens bijhouden
* Identificeer, creeer, en visualiseer specifieke Punten van belang. De aandachtspunten moeten in het mobiele SDK configuratiedossier worden bepaald.
* Bluetooth-bakens bijhouden (UUID, major, minor en proximity).

Wanneer u [!UICONTROL Location Tracking] inschakelt, zijn de volgende afmetingen beschikbaar:

* [!UICONTROL Beacon Major] (met [&#x200B; Ingang &#x200B;](/help/components/dimensions/entry-dimensions.md) en [&#x200B; Uitgang &#x200B;](/help/components/dimensions/exit-dimensions.md) dimensies)
* [!UICONTROL Beacon Minor] (met [&#x200B; Ingang &#x200B;](/help/components/dimensions/entry-dimensions.md) en [&#x200B; Uitgang &#x200B;](/help/components/dimensions/exit-dimensions.md) dimensies)
* [!UICONTROL Beacon Proximity] (met [&#x200B; Ingang &#x200B;](/help/components/dimensions/entry-dimensions.md) en [&#x200B; Uitgang &#x200B;](/help/components/dimensions/exit-dimensions.md) dimensies)
* [!UICONTROL Beacon UUID] (met [&#x200B; Ingang &#x200B;](/help/components/dimensions/entry-dimensions.md) en [&#x200B; Uitgang &#x200B;](/help/components/dimensions/exit-dimensions.md) dimensies)
* [!UICONTROL Location (down to 10 km)]
* [!UICONTROL Location (down to 100 m)]
* [!UICONTROL Location (down to 1 m)]
* [!UICONTROL Point of Interest Name]
* [!UICONTROL Distance to Point of Interest Center]
* [!UICONTROL Point of Interest ID]

## [!UICONTROL Voice and Chatbots]

Met [!UICONTROL Voice and Chatbots] afmetingen en metriek kunt u spraakassistenten meten, zoals Alexa of Google Home. Het staat u ook toe om thuis-geteelde praatjebots te meten. Tot de meeteigenschappen behoren:

* **Levenscyclus**: Het niveau van de stichting van het melden voor om het even welke app, zoals het aantal lanceringen en platformtype.
* **Gesprek**: De intenties van maatregelen, reacties, en andere metriek en dimensies met betrekking tot het gesprek.

Wanneer u [!UICONTROL Voice and Chatbots] inschakelt, zijn de volgende afmetingen beschikbaar:

* [!UICONTROL Voice Device Capabilities] (met [&#x200B; Ingang &#x200B;](/help/components/dimensions/entry-dimensions.md) en [&#x200B; Uitgang &#x200B;](/help/components/dimensions/exit-dimensions.md) dimensies)
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

Adobe raadt aan om oudere rapporten uit te schakelen, zodat achtergrondopdrachten niet zichtbaar zijn. Als u achtergrondklappen in uw analyse wilt omvatten, kunt u de [&#x200B; Virtuele rapportreeks &#x200B;](/help/components/vrs/vrs-about.md) plaatsen **[!UICONTROL Include background hits]** toelaten.
