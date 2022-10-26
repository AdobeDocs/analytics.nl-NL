---
description: Leer over hoe te om de Manager van de Activiteit van de Rapportering te gebruiken om capaciteitskwesties tijdens piekrapporteringstijden te diagnostiseren en te bevestigen.
title: Activity Manager rapporteren
feature: Admin Tools
hide: true
hidefromtoc: true
source-git-commit: 6ab2f39bdfc3a50c2b91f020c98b0e81da8b2b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Activity Manager rapporteren

>[!NOTE]
>
>Deze functionaliteit wordt momenteel getest in bèta.

De manager van de Activiteit van de Rapportering laat u de rapporteringscapaciteit voor elke rapportreeks in uw organisatie zien. Het biedt u als beheerder gedetailleerde zichtbaarheid bij het melden van het verbruik en helpt u om problemen met de capaciteit tijdens piekrapporteringstijden eenvoudig te diagnosticeren en op te lossen. Wanneer uw organisatie het melden van verzoekcapaciteit bereikt en een degradatie in het melden van prestaties ervaart, hebt u nu een manier om het melden van problemen zonder tussenkomst van de klantenzorg of de techniek van Adobe zelf te diagnostiseren. U kunt rapportrijen gemakkelijk beheren binnen één enkele interface en onmiddellijk handelen &#x200B; &#x200B; om uw gebruikerservaring te verbeteren. Dit gereedschap:

* Vertel u over uw huidige rapporteringscapaciteit over uw rapportseries.
* Verstrekt gedetailleerde informatie van de rapportvraag over huidige rapporteringsverzoeken, of een rij gevormd en lopend.
* Hiermee kunt u de rapportwachtrij optimaliseren door een aantal prioriteiten toe te wijzen en andere rapportageaanvragen te annuleren om capaciteit vrij te maken. Met andere woorden, u kunt in real time vragen: Is dit verslag op dit moment noodzakelijk of kan ik het intrekken ten gunste van urgente verslagen?

## Toegang tot de rapportageactiviteitsmanager

In Adobe Analytics gaan beheerders naar **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

## De wachtrij met rapporten weergeven

Wanneer het openen van de overzichtspagina van de Manager van de Activiteit van de Rapportering, zult u een lijst van uw toegelaten reeksen van het basisrapport zien.

![rapportwachtrij](assets/reporting-activity1.png)

| UI-element | Beschrijving |
| --- | --- |
| **[!UICONTROL Report Suite]** | De set met basisrapporten |
| **[!UICONTROL Virtual Report Suite]** | Alle virtuele rapportsuites die in deze reeks van het basisrapport bijdragen. De virtuele rapportsuites voegen ingewikkeldheid aan rapporteringsverzoeken toe toe toe te schrijven aan extra niveaus van toegepaste filtratie en segmentatie. Alle verzoeken die uit de virtuele rapportreeksen komen worden gecombineerd en neer aan de reeks van het basisrapport.<p>Als u 10 verzoeken hebt die uit 5 VRSs komen, is dat 50 verzoeken bij de reeks van het het rapport van het basisniveau. Op deze manier kun je snel de capaciteit raken. |
| **[!UICONTROL Usage Capacity]** | Percentage wijs, hoeveel van de rapporteringscapaciteit van de rapportreeks wordt gebruikt, in echt - tijd. |
| **[!UICONTROL Status]** | Vier mogelijke statusindicatoren: <ul><li>**Rood - bij capaciteit**: De rapportenreeks is samengesteld in termen van rapporteringscapaciteit.</li><li>**Geel - Nearcapaciteit**: Dit pakket verslagen dreigt zijn maximumcapaciteit te bereiken.</li><li>**Groen - beschikbaar**: Er is genoeg rapportagecapaciteit.</li><li>**Grijs - Niet beschikbaar**: De rapportsuite is niet geconfigureerd voor rapportagecapaciteit.</li></ul> |

Vernieuw de pagina om de resultaten te wijzigen.

## Gebruik van filterrapporten

U kunt de rapportsuites filteren door