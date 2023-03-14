---
description: Leer over hoe te om de Manager van de Activiteit van de Rapportering te gebruiken om capaciteitskwesties tijdens piekrapporteringstijden te diagnostiseren en te bevestigen.
title: Activity Manager rapporteren
feature: Admin Tools
mini-toc-levels: 3
exl-id: f638c6a9-1c2c-4936-a787-281269f95afc
source-git-commit: e7346b11a7d3eb4c18ec02df6c8a07574e02a2b4
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 2%

---

# Activity Manager rapporteren

>[!NOTE]
>
>Deze functionaliteit wordt momenteel getest in bèta.

De [!UICONTROL Reporting Activity Manager] laat u de rapporteringscapaciteit voor elke rapportreeks in uw organisatie zien. Het biedt u als beheerder gedetailleerde zichtbaarheid bij het melden van het verbruik en helpt u om problemen met de capaciteit tijdens piekrapporteringstijden eenvoudig te diagnosticeren en op te lossen.

Wanneer uw organisatie het melden van verzoekcapaciteit bereikt en een degradatie in het melden van prestaties ervaart, hebt u nu een manier om het melden van problemen zonder tussenkomst van de klantenzorg of de techniek van Adobe zelf te diagnostiseren. U kunt rapportrijen gemakkelijk beheren binnen één enkele interface en onmiddellijk handelen &#x200B; &#x200B; om uw gebruikerservaring te verbeteren. Dit gereedschap:

* Vertel u, in echt - tijd, over uw huidige rapporteringscapaciteit over uw rapportseries.
* Verstrekt gedetailleerde informatie van de rapportvraag over huidige rapporteringsverzoeken, of een rij gevormd of lopend.
* Hiermee kunt u de rapportwachtrij optimaliseren door een aantal prioriteiten toe te wijzen en andere rapportageaanvragen te annuleren om capaciteit vrij te maken. Met andere woorden, u kunt in real time vragen: Is dit verslag op dit moment noodzakelijk of kan ik het intrekken ten gunste van urgente verslagen?

## Toegang tot de rapportageactiviteitsmanager

In Adobe Analytics gaan beheerders naar **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

## Toestemmingen

U hebt de toestemming van de Beheerder van het Product van de Analyse (in Adobe Admin Console) nodig om rapporteringsactiviteit te beheren.

![machtiging](/help/admin/admin/assets/rep-mgr-permission.png)

## De wachtrij met rapporten weergeven

Wanneer u het dialoogvenster [!UICONTROL Reporting Activity] De overzichtspagina van de manager, ziet u een lijst van uw toegelaten reeksen van het basisrapport.

![rapportwachtrij](/help/admin/admin/assets/reporting-activity1.png)

| UI-element | Beschrijving |
| --- | --- |
| **[!UICONTROL Report Suite]** | De set met basisrapporten waarvan u de rapportactiviteiten controleert. |
| **[!UICONTROL Virtual Report Suite]** | Toont alle virtuele rapportsuites die in deze reeks van het basisrapport van toepassing zijn. De virtuele rapportsuites voegen ingewikkeldheid aan rapporteringsverzoeken toe toe toe te schrijven aan extra niveaus van toegepaste filtratie en segmentatie. Alle verzoeken die uit de virtuele rapportreeksen komen worden gecombineerd en neer aan de reeks van het basisrapport.<p>Bijvoorbeeld, als u 10 verzoeken hebt die uit 5 VRSs komen, is dat 50 verzoeken bij de het rapportreeks van het basisniveau. Op deze manier kun je snel de capaciteit raken. |
| **[!UICONTROL Usage Capacity]** | Percentage wijs, hoeveel van de rapporteringscapaciteit van de rapportreeks wordt gebruikt, in echt - tijd. |
| **[!UICONTROL Status]** | Vier mogelijke statusindicatoren: <ul><li>**Rood -[!UICONTROL At Capacity]**: De rapportenreeks is samengesteld in termen van rapporteringscapaciteit. (100%) </li><li>**Geel -[!UICONTROL Nearing capacity]**: Dit pakket verslagen dreigt zijn maximumcapaciteit te bereiken. (90% - 99%)</li><li>**Groen -[!UICONTROL All good]**: Er is genoeg rapportagecapaciteit. (0% - 89%)</li><li>**Grijs -[!UICONTROL Status pending/Not enabled]**: Rapportcapaciteit niet beschikbaar.</li></ul> |

{style="table-layout:auto"}

### Overige activiteiten op het gebied van rapportageactiviteiten

* Klikken **[!UICONTROL Refresh]** bovenaan rechts om de resultaten te vernieuwen.
* Klik op de ster links van de naam van de rapportsuite aan de favoriet van deze rapportsuite.
* Controleren **[!UICONTROL Favorites]** linksboven om uw favorieten te tonen.
* Zoek op rapportsuites door naam of door identiteitskaart in de onderzoeksbar.
* De rapportsuites van de filter door hun status.

## Rapportactiviteiten voor afzonderlijke rapportsuites weergeven

Klik de titelverbinding van een rapportreeks waarvoor u details wilt bekijken.

![rapportsuite](/help/admin/admin/assets/indiv-report-ste.png)

### Lijngrafiek

De lijngrafiek toont de rapportactiviteit voor de geselecteerde rapportreeks over de laatste 2 uren.

* Op de x-as worden de gegevens over de rapportagecapaciteit gedurende de laatste twee uur weergegeven.
* De y-as toont de gemiddelde wachttijd voor een vraag, in seconden.
* U kunt de muisaanwijzer boven het lijndiagram plaatsen om de punten in de tijd en de gemiddelde wachttijd voor dat moment weer te geven.

   ![detail](/help/admin/admin/assets/detail.png)

### Filter

U kunt de lijst door Toepassing (zie lijst in de lijst hieronder), door Gebruiker, en door Project filtreren.

![filter](/help/admin/admin/assets/filter.png)

### Samenvattingsnummers

![filter](/help/admin/admin/assets/summary_numbers.png)

De overzichtsaantallen tonen de volgende informatie:

| Samenvattingsnummer | Beschrijving |
| --- | --- |
| [!UICONTROL Users] | Het aantal gebruikers dat momenteel rapportageaanvragen naar deze rapportsuite verzendt. |
| [!UICONTROL Projects] | Werkruimteprojecten, Report Builder-werkboeken, enz. |
| [!UICONTROL Queries] | Het aantal query&#39;s dat momenteel wordt uitgevoerd. |
| [!UICONTROL Average Wait Time] | De gemiddelde wachttijd voor alle lopende vragen. |
| [!UICONTROL Usage Capacity] | De huidige gebruikscapaciteit voor deze rapportsuite. |

{style="table-layout:auto"}

### Tabel

De gedetailleerde tabel hieronder bevat details over de rapportsuite.

| Kolom | Beschrijving |
| --- | --- |
| [!UICONTROL Query ID] | Kan voor het oplossen van problemendoeleinden worden gebruikt. |
| [!UICONTROL Running Time] | Hoe lang de query is uitgevoerd. |
| [!UICONTROL Wait Time] | Hoe lang de vraag alvorens wordt verwerkt heeft gewacht. In het algemeen bij &quot;0&quot; wanneer er voldoende capaciteit is. |
| [!UICONTROL Start Time] | Wanneer de query is gestart met de verwerking (lokale beheertijd). |
| [!UICONTROL Application] | De toepassingen die worden ondersteund door de [!UICONTROL Reporting Activity Manager] zijn: <ul><li>Analysis Workspace-gebruikersinterface</li><li>Werkruimte geplande projecten</li><li>Report Builder</li><li>Builder-gebruikersinterface: Segment, Berekende cijfers, Annotaties, Soorten publiek, enz.</li><li>API-aanroepen van 1.4 of 2.0 API</li><li>Intelligente waarschuwingen</li></ul> |
| [!UICONTROL User] | De gebruiker die de query heeft gestart. |
| [!UICONTROL Project] | Opgeslagen projectnamen voor Workspace, API-rapport-id&#39;s, enz. (Metagegevens kunnen per toepassing verschillen.) |
| [!UICONTROL Month Boundaries] | Hoeveel maandelijkse grenzen een verzoek overschrijdt. Dit vergroot de complexiteit van het verzoek. |
| [!UICONTROL Columns] | Het aantal metriek en onderverdelingen in Werkruimte om de ingewikkeldheid van het verzoek te meten. |
| [!UICONTROL Segments] | Hoeveel segmenten worden toegepast op dit verzoek. Dit vergroot de complexiteit van het verzoek. |
| [!UICONTROL Status] | Statusindicatoren: <ul><li>**Wordt uitgevoerd**: Aanvraag wordt momenteel verwerkt.</li><li>**In behandeling**: De aanvraag is in afwachting van verwerking.</li></ul> |

{style="table-layout:auto"}

## Rapportageverzoeken annuleren

Een aanvraag annuleren

1. Vink het vakje links van een of meer aan **[!UICONTROL Query ID]** in de tabel en klik op **[!UICONTROL Cancel requests]** onderaan.

   U kunt aanvragen ook bulksgewijs annuleren door details te bekijken door [!UICONTROL User], [!UICONTROL Project], of [!UICONTROL Application]. Volgende aanvragen voor een project, een gebruiker of een toepassing die zich niet in de wachtrij of bij annulering bevonden, kunnen nog steeds worden weergegeven wanneer de activiteit wordt vernieuwd.

1. In de **[!UICONTROL Cancel x query]** venster dat wordt weergegeven, kunt u het annuleringsbericht indien nodig wijzigen.
1. Klik op **[!UICONTROL Continue]**.

   ![cancel-query](/help/admin/admin/assets/cancel-query.png)

De gebruikers van de toepassing in Werkruimte, bijvoorbeeld, zullen de volgende verklaring in hun projecten zien verschijnen:

![cancel-user-notice](/help/admin/admin/assets/cancel-user-facing.png)

## Veelgestelde vragen

| Vraag | Antwoord |
| --- | --- |
| Kan ik extra rapporteringscapaciteit kopen? | Deze mogelijkheid zal in de nabije toekomst beschikbaar zijn. |

{style="table-layout:auto"}
