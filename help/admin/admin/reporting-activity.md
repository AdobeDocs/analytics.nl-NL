---
description: Leer over hoe te om de Manager van de Activiteit van de Rapportering te gebruiken om capaciteitskwesties tijdens piekrapporteringstijden te diagnostiseren en te bevestigen.
title: Activity Manager rapporteren
feature: Admin Tools
mini-toc-levels: 3
hide: true
hidefromtoc: true
source-git-commit: 123a2131be1a3cb23246e2ba591be645c7025b26
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 1%

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

Wanneer het openen van de overzichtspagina van de Manager van de Activiteit van de Rapportering, ziet u een lijst van uw toegelaten reeksen van het basisrapport.

![rapportwachtrij](assets/reporting-activity1.png)

| UI-element | Beschrijving |
| --- | --- |
| **[!UICONTROL Report Suite]** | De set met basisrapporten waarvan u de rapportactiviteiten controleert. |
| **[!UICONTROL Virtual Report Suite]** | Toont alle virtuele rapportsuites die in deze reeks van het basisrapport van toepassing zijn. De virtuele rapportsuites voegen ingewikkeldheid aan rapporteringsverzoeken toe toe toe te schrijven aan extra niveaus van toegepaste filtratie en segmentatie. Alle verzoeken die uit de virtuele rapportreeksen komen worden gecombineerd en neer aan de reeks van het basisrapport.<p>Bijvoorbeeld, als u 10 verzoeken hebt die uit 5 VRSs komen, is dat 50 verzoeken bij de het rapportreeks van het basisniveau. Op deze manier kun je snel de capaciteit raken. |
| **[!UICONTROL Usage Capacity]** | Percentage wijs, hoeveel van de rapporteringscapaciteit van de rapportreeks wordt gebruikt, in echt - tijd. |
| **[!UICONTROL Status]** | Vier mogelijke statusindicatoren: <ul><li>**Rood -[!UICONTROL At Capacity]**: De rapportenreeks is samengesteld in termen van rapporteringscapaciteit.</li><li>**Geel -[!UICONTROL Nearing capacity]**: Dit pakket verslagen dreigt zijn maximumcapaciteit te bereiken.</li><li>**Groen -[!UICONTROL All good]**: Er is genoeg rapportagecapaciteit.</li><li>**[!UICONTROL Status pending]**: ?</li><li>**Grijs - Niet beschikbaar**: De rapportsuite is niet geconfigureerd voor rapportagecapaciteit.</li></ul> |

### Overige activiteiten op het gebied van rapportageactiviteiten

* Klikken **[!UICONTROL Refresh]** bovenaan rechts om de resultaten te vernieuwen.
* Klik op de ster links van de naam van de rapportsuite aan de favoriet van deze rapportsuite.
* Controleren **[!UICONTROL Favorites]** linksboven om uw favorieten te tonen.
* Zoek op rapportsuites door naam of door identiteitskaart in de onderzoeksbar.
* De rapportsuites van de filter door hun status.

## Rapportactiviteiten voor afzonderlijke rapportsuites weergeven

Klik de titelverbinding van een rapportreeks waarvoor u details wilt bekijken.

![rapportsuite](assets/indiv-report-ste.png)

### Lijngrafiek

De lijngrafiek toont de rapportactiviteit voor de geselecteerde rapportreeks over de laatste 2 uren.

* Op de x-as worden de gegevens over de rapportagecapaciteit gedurende de laatste twee uur weergegeven.
* De y-as toont de gemiddelde wachttijd voor een vraag, in seconden.
* U kunt de muisaanwijzer boven het lijndiagram plaatsen om de punten in de tijd en de gemiddelde wachttijd voor dat moment weer te geven.

   ![detail](assets/detail.png)

### Filter

U kunt de lijst door Toepassing (zie lijst in de lijst hieronder), door Gebruiker, en door Project filtreren.

![filter](assets/filter.png)

### Samenvattingsnummers

![filter](assets/summary_numbers.png)

De overzichtsaantallen tonen de volgende informatie:

| Samenvattingsnummer | Beschrijving |
| --- | --- |
| Gebruikers | Hoeveel gebruikers verzenden momenteel rapporteringsverzoeken naar deze rapportsuite. |
| Projecten |  |
| Zoekopdrachten |  |
| Gemiddelde wachttijd |  |
| Gebruikscapaciteit | De huidige gebruikscapaciteit voor deze rapportsuite. |

{style=&quot;table-layout:auto&quot;}

### Tabel

De gedetailleerde tabel hieronder toont

| Kolom | Beschrijving |
| --- | --- |
| Query-id |  |
| Runtime |  |
| Wacht op tijd |  |
| Begintijd |  |
| Toepassing | De toepassingen die door de Manager van de Activiteit van de Rapportering worden gesteund zijn: <ul><li>Analysis Workspace-gebruikersinterface</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende cijfers, Annotaties, Soorten publiek, enz.</li></ul> |
| Gebruiker |  |
| Project |  |
| Maandgrenzen |
| Kolommen |  |
| Segmenten |  |
| Status |  |

{style=&quot;table-layout:auto&quot;}


