---
description: Voeg of laat marketing kanalen in de Manager van het Kanaal van de Marketing toe. Voor rapportsuites die geen marketing kanalen hebben, laat een automatische opstelling u verscheidene kanalen voor u, samen met hun regels tot stand brengen. U kunt vooraf gedefinieerde kanalen naar wens bewerken of uw eigen kanalen maken (maximaal 25).
subtopic: Marketing channels
title: Verkoopkanalen beheren
feature: Marketing Channels
exl-id: a768a4c2-f922-4d96-a9fb-78a1dfac04d8
role: Admin
source-git-commit: def7d071de1765acf524a638a8f8d13ae69e1a1f
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# Verkoopkanalen beheren

>[!NOTE]
>
> Voor algemene informatie over de Kanalen van de Marketing, zie [Aan de slag met marketingkanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
>
> Om de doeltreffendheid van de Kanalen van de Marketing voor Attributie en Customer Journey Analytics te maximaliseren, hebben wij sommige gepubliceerd [herziene beste praktijken](/help/components/c-marketing-channels/mchannel-best-practices.md).

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

Voeg of laat marketing kanalen in de Manager van het Kanaal van de Marketing toe. Voor rapportsuites die geen marketing kanalen hebben, laat een automatische opstelling u verscheidene kanalen voor u, samen met hun regels tot stand brengen. U kunt vooraf gedefinieerde kanalen naar wens bewerken of uw eigen kanalen maken (maximaal 25).

Kanalen toevoegen aan de [!UICONTROL Marketing Channels] pagina wordt uitgevoerd onafhankelijk van het maken van regels voor de [Verwerkingsregels voor marketingkanalen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md) pagina. U associeert regels met kanalen wanneer het creëren van de regel.

Hier volgen enkele richtlijnen voor het maken van kanalen:

* Maak eerst een lijst met al uw kanalen, zodat alle bezoekershits naar het rechterkanaal worden gecategoriseerd.
* Inclusief kanalen voor de categorieën van [Intern](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md) treffers.
* Neem een &#39;catch-all&#39;-kanaal op voor &#39;Overige campagnes&#39;, dat na betaalde kanalen en vóór biologische kanalen moet worden geplaatst.


## Vereisten {#prereqs}

* De toegang van de opstelling tot de afmetingen van het Kanaal van de Marketing.

  Zie [Machtigingen voor marketingkanalen](/help/components/c-marketing-channels/c-channel-report-access.md).

## Marketingkanalen toevoegen {#add-mktg-channels}

Voeg marketingkanalen toe in de Marketing Channel Manager.

>[!NOTE]
>
>U kunt een kanaal niet verwijderen. Als u geen kanaal wilt gebruiken, kunt u het onbruikbaar maken of anders noemen, en het bewaren voor later gebruik.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Op de [!UICONTROL Report Suite Manager] pagina, selecteert u een rapportsuite.

   Als u veelvoudige rapportreeksen selecteert, selecteer een malplaatje dat montages van het malplaatje aan de geselecteerde rapportreeksen kopieert.

   Zie [Pas de montages van de de reeksreeks van het malplaatjerapport op veelvoudige rapportreeksen toe](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   Als er in uw rapportsuite geen kanalen zijn gedefinieerd, worden de [Automatisch instellen](/help/components/c-marketing-channels/c-getting-started-mchannel.md) wordt weergegeven.

1. Op de [!UICONTROL Marketing Channel Manager] pagina, klikt u **[!UICONTROL Add Channel]**.

   Deze optie is niet beschikbaar als er 25 kanalen zijn gedefinieerd.

1. Klikken **[!UICONTROL Save.]**
1. Om regels voor het kanaal te vormen, klik **[!UICONTROL Marketing Channel Processing Rules]**.

   Zie [Verwerkingsregels voor marketingkanalen maken](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md).

## Kanaalinstellingen toepassen {#mktg-channel-mgr}

Er zijn verschillende instellingen die op elk kanaal op het [!UICONTROL Marketing Channel Manager] pagina.

| Veld | Definitie |
|--- |--- |
| Ingeschakeld | Hiermee schakelt u dit marketingkanaal in of uit. |
| Kanaalnaam | De vriendelijke naam van het marketingkanaal. |
| Laatste aanraakkanaal overschrijven | Hiermee kunt u kiezen of u een bestaand, blijvend laatste aanraakkanaal wilt overschrijven met het geselecteerde kanaal. Als u dit selectievakje inschakelt, overschrijft elk kanaal (inclusief Direct en Intern) een bestaand laatste aanraakkanaal. Het resultaat is dat conversie wordt toegeschreven aan een kanaal dat geen krediet verdient. Met deze optie kunt u er bijvoorbeeld voor zorgen dat het Direct-kanaal geen conversiekrediet ontvangt als de gebruiker eerder via het Natural Search-kanaal was aangeschaft. |
| Kanaaluitsplitsing | Hiermee kunt u een kanaal opsplitsen op basis van deze waarde. U kunt mogelijke kanaalstoringen (subkanalen) toevoegen tijdens het maken van [classificaties van marketingkanalen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/classifications-mchannel.md). |
| Type | Hiermee geeft u op hoe de gebruiker naar uw site is gekomen. U kunt Online of Offline selecteren. Gebruik online kanalen voor bezoekers die via een zoekmachine of e-mailcampagne komen. Offlinekanalen zijn van toepassing op bezoekers die uw site hebben gevonden via krantencoupons of advertenties in tijdschriften. De off-line kanalen omvatten gewoonlijk gegevens die door het melden van Gegevensbronnen worden ingevoerd. Zie [Gegevensbronnen](https://experienceleague.adobe.com/docs/analytics/import/data-sources/datasrc-home.html?lang=nl-NL). Zie [Offline gegevens toevoegen](/help/components/c-marketing-channels/c-getting-started-mchannel.md). |

### Beste werkwijzen overschrijven

Het is aan te raden de optie last-touch voor negeren van directe en interne kanalen uit te schakelen, zodat ze geen krediet kunnen halen van andere hardnekkige, laatste aanraakkanalen (of van elkaar).

![](assets/int-channel2.png)

## Kanaalregels definiëren

Alvorens de kanalen en de kanaalgegevens in het rapport kunnen worden getoond, creeer de kanalen en de onderliggende regels die gegevens verwerken. U kunt ook opgeven hoe lang u de [periode van betrokkenheid van bezoekers](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/visitor-engagement.md) tot en met laatste.

Adobe biedt verschillende vooraf gedefinieerde kanalen tijdens een [automatische installatie](/help/components/c-marketing-channels/c-getting-started-mchannel.md) die u naar wens kunt bewerken. Bovendien kunt u deze opstelling wijzigen en douaneregels bepalen binnen [Verwerkingsregels voor distributiekanalen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md).

>[!NOTE]
>
>Adobe raadt u aan uw rapport in te stellen in een rapportsuite die u als sjabloon voor testdoeleinden kunt gebruiken. U kunt het malplaatje gebruiken om kanaal en regelreeksen globaal op één of meerdere reeksen van het productierapport toe te passen.
>
>Zie [Suite-instellingen voor sjabloonrapport toepassen op meerdere rapportsets](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
