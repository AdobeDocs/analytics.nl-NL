---
description: Voeg of laat marketing kanalen in de Manager van het Kanaal van de Marketing toe. Voor rapportsuites die geen marketing kanalen hebben, laat een automatische opstelling u verscheidene kanalen voor u, samen met hun regels tot stand brengen. U kunt vooraf gedefinieerde kanalen naar wens bewerken of uw eigen kanalen maken (maximaal 25).
subtopic: Marketing channels
title: Verkoopkanalen beheren
feature: Marketing Channels
exl-id: a768a4c2-f922-4d96-a9fb-78a1dfac04d8
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# Verkoopkanalen beheren

>[!NOTE]
>
> Voor algemene informatie over de Kanalen van de Marketing, zie [ begonnen worden met de Kanalen van de Marketing ](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
>
> Om doeltreffendheid van de Kanalen van de Marketing voor Attributie en Customer Journey Analytics te maximaliseren, hebben wij sommige [ herzien beste praktijken ](/help/components/c-marketing-channels/mchannel-best-practices.md) gepubliceerd.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]** .

Voeg of laat marketing kanalen in de Manager van het Kanaal van de Marketing toe. Voor rapportsuites die geen marketing kanalen hebben, laat een automatische opstelling u verscheidene kanalen voor u, samen met hun regels tot stand brengen. U kunt vooraf gedefinieerde kanalen naar wens bewerken of uw eigen kanalen maken (maximaal 25).

Het toevoegen van kanalen aan de [!UICONTROL Marketing Channels] pagina wordt gedaan onafhankelijk van het creëren van regels op de [ pagina van de Regels van de Verwerking van het Kanaal van de Marketing ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-rules.md). U associeert regels met kanalen wanneer het creëren van de regel.

Hier volgen enkele richtlijnen voor het maken van kanalen:

* Maak eerst een lijst met al uw kanalen, zodat alle bezoekershits naar het rechterkanaal worden gecategoriseerd.
* Omvat kanalen voor de categorieën van [ Interne ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-rules.md) klappen.
* Neem een &#39;catch-all&#39;-kanaal op voor &#39;Overige campagnes&#39;, dat na betaalde kanalen en vóór biologische kanalen moet worden geplaatst.


## Vereisten {#prereqs}

* De toegang van de opstelling tot de afmetingen van het Kanaal van de Marketing.

  Zie [ de toestemmingen van Kanalen van de Marketing ](/help/components/c-marketing-channels/c-channel-report-access.md).

## Marketingkanalen toevoegen {#add-mktg-channels}

Voeg marketingkanalen toe in de Marketing Channel Manager.

>[!NOTE]
>
>U kunt een kanaal niet verwijderen. Als u geen kanaal wilt gebruiken, kunt u het onbruikbaar maken of anders noemen, en het bewaren voor later gebruik.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Selecteer op de pagina [!UICONTROL Report Suite Manager] een rapportsuite.

   Als u veelvoudige rapportreeksen selecteert, selecteer een malplaatje dat montages van het malplaatje aan de geselecteerde rapportreeksen kopieert.

   Zie [ de reeksinstellingen van het malplaatjerapport op veelvoudige rapportsuites ](/help/components/c-marketing-channels/c-getting-started-mchannel.md) toepassen.

1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   Als uw rapportreeks geen bepaalde kanalen heeft, de [ AutoOpstelling ](/help/components/c-marketing-channels/c-getting-started-mchannel.md) paginagenvertoningen.

1. Klik op de pagina [!UICONTROL Marketing Channel Manager] op **[!UICONTROL Add Channel]** .

   Deze optie is niet beschikbaar als er 25 kanalen zijn gedefinieerd.

1. Klikken **[!UICONTROL Save.]**
1. Klik op **[!UICONTROL Marketing Channel Processing Rules]** om regels voor het kanaal te configureren.

   Zie [ de verwerkingsregels van het Kanaal van de Marketing ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-rules.md) creëren.

## Kanaalinstellingen toepassen {#mktg-channel-mgr}

Er zijn verschillende instellingen die op elk kanaal op de pagina [!UICONTROL Marketing Channel Manager] kunnen worden toegepast.

| Veld | Definitie |
|--- |--- |
| Ingeschakeld | Hiermee schakelt u dit marketingkanaal in of uit. |
| Kanaalnaam | De vriendelijke naam van het marketingkanaal. |
| Laatste aanraakkanaal overschrijven | Hiermee kunt u kiezen of u een bestaand, blijvend laatste aanraakkanaal wilt overschrijven met het geselecteerde kanaal. Als u dit selectievakje inschakelt, overschrijft elk kanaal (inclusief Direct en Intern) een bestaand laatste aanraakkanaal. Het resultaat is dat conversie wordt toegeschreven aan een kanaal dat geen krediet verdient. Met deze optie kunt u er bijvoorbeeld voor zorgen dat het Direct-kanaal geen conversiekrediet ontvangt als de gebruiker eerder via het Natural Search-kanaal was aangeschaft. |
| Kanaaluitsplitsing | Hiermee kunt u een kanaal opsplitsen op basis van deze waarde. U kunt mogelijke kanaalonderverdelingen (subkanalen) toevoegen wanneer het creëren van [ de classificaties van het marketingkanaal ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/classifications-mchannel.md). |
| Type | Hiermee geeft u op hoe de gebruiker naar uw site is gekomen. U kunt Online of Offline selecteren. Gebruik online kanalen voor bezoekers die via een zoekmachine of e-mailcampagne komen. Offlinekanalen zijn van toepassing op bezoekers die uw site hebben gevonden via krantencoupons of advertenties in tijdschriften. De off-line kanalen omvatten gewoonlijk gegevens die door het melden van Gegevensbronnen worden ingevoerd. Zie [ Gegevensbronnen ](/help/import/data-sources/overview.md). Zie [ Offlinegegevens ](/help/components/c-marketing-channels/c-getting-started-mchannel.md) toevoegen. |

### Beste werkwijzen overschrijven

Het is aan te raden de optie last-touch voor negeren van directe en interne kanalen uit te schakelen, zodat ze geen krediet kunnen halen van andere hardnekkige, laatste aanraakkanalen (of van elkaar).

![](assets/int-channel2.png)

## Kanaalregels definiëren

Alvorens de kanalen en de kanaalgegevens in het rapport kunnen worden getoond, creeer de kanalen en de onderliggende regels die gegevens verwerken. U kunt ook specificeren hoe lang u de [ periode van de bezoekersbetrokkenheid ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/visitor-engagement.md) wilt duren.

Adobe verstrekt verscheidene vooraf bepaalde kanalen tijdens een [ automatische opstelling ](/help/components/c-marketing-channels/c-getting-started-mchannel.md) die u kunt uitgeven om uw behoeften aan te passen. Bovendien, kunt u deze opstelling wijzigen en douaneregels binnen [ de verwerkingsregels van het Kanaal van de Marketing ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-rules.md) bepalen.

>[!NOTE]
>
>Adobe raadt u aan uw rapport in te stellen in een rapportsuite die u als sjabloon voor testdoeleinden kunt gebruiken. U kunt het malplaatje gebruiken om kanaal en regelreeksen globaal op één of meerdere reeksen van het productierapport toe te passen.
>
>Zie [ de Montages van de Reeks van het Rapport van het Malplaatje op Veelvoudige Reeksen van het Rapport toepassen ](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
