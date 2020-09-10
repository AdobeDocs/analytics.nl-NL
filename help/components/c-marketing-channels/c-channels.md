---
description: Voeg of laat marketing kanalen in de Manager van het Kanaal van de Marketing toe. Voor rapportsuites die geen marketing kanalen hebben, laat een automatische opstelling u verscheidene kanalen voor u, samen met hun regels tot stand brengen. U kunt vooraf gedefinieerde kanalen naar wens bewerken of uw eigen kanalen maken (maximaal 25).
subtopic: Marketing channels
title: Marketingkanalen beheren
topic: Reports and analytics
uuid: 9d367bb6-a17b-49b8-9cd5-24fac35ae982
translation-type: tm+mt
source-git-commit: f96be5fb0ba50b9b06aa65da7eff51c869e2a6f4
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 3%

---


# Marketingkanalen beheren

Voeg of laat marketing kanalen in de Manager van het Kanaal van de Marketing toe. Voor rapportsuites die geen marketing kanalen hebben, laat een automatische opstelling u verscheidene kanalen voor u, samen met hun regels tot stand brengen. U kunt vooraf gedefinieerde kanalen naar wens bewerken of uw eigen kanalen maken (maximaal 25).

Het toevoegen van kanalen aan de [!UICONTROL Marketing Channels] pagina wordt gedaan onafhankelijk van het creëren van regels op de pagina van de Regels [van de Verwerking van het Kanaal van de](/help/components/c-marketing-channels/c-rules.md) Marketing. U associeert regels met kanalen wanneer het creëren van de regel.

Hier volgen enkele richtlijnen voor het maken van kanalen:

* Maak eerst een lijst met al uw kanalen, zodat alle bezoekershits naar het rechterkanaal worden gecategoriseerd.
* Neem kanalen op voor de categorieën [interne](/help/components/c-marketing-channels/c-rules.md) treffers en [directe](/help/components/c-marketing-channels/c-rules.md) treffers.
* Neem een &#39;catch-all&#39;-kanaal op voor &#39;Overige campagnes&#39;, dat na betaalde kanalen en vóór biologische kanalen moet worden geplaatst.


## Vereisten {#prereqs}

* De toegang van de opstelling tot de afmetingen van het Kanaal van de Marketing.

   See [Marketing Channels permissions](/help/components/c-marketing-channels/c-channel-report-access.md).

## Marketingkanalen toevoegen {#add-mktg-channels}

Voeg marketingkanalen toe in de Marketing Channel Manager.

>[!NOTE]
>
>U kunt een kanaal niet verwijderen. Als u geen kanaal wilt gebruiken, kunt u het onbruikbaar maken of anders noemen, en het bewaren voor later gebruik.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Selecteer een rapportsuite op de [!UICONTROL Report Suite Manager] pagina.

   Als u veelvoudige rapportreeksen selecteert, selecteer een malplaatje dat montages van het malplaatje aan de geselecteerde rapportreeksen kopieert.

   Zie de montages van de [Sjabloonrapportreeks op veelvoudige rapportreeksen](/help/components/c-marketing-channels/c-getting-started-mchannel.md)toepassen.

1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   Als er in uw rapportsuite geen kanalen zijn gedefinieerd, wordt de pagina [Automatisch instellen](/help/components/c-marketing-channels/c-getting-started-mchannel.md) weergegeven.

1. Klik op de [!UICONTROL Marketing Channel Manager] pagina **[!UICONTROL Add Channel]**.

   Deze optie is niet beschikbaar als er 25 kanalen zijn gedefinieerd.

1. Klik op **[!UICONTROL Save.]**
1. Om regels voor het kanaal te vormen, klik **[!UICONTROL Marketing Channel Processing Rules]**.

   Zie [Verwerkingsregels](/help/components/c-marketing-channels/c-rules.md)voor marketingkanalen maken.

## Kanaalinstellingen toepassen {#mktg-channel-mgr}

Er zijn verschillende instellingen die op elk kanaal op de [!UICONTROL Marketing Channel Manager] pagina kunnen worden toegepast.

| Veld | Definitie |
|--- |--- |
| Ingeschakeld | Hiermee schakelt u dit marketingkanaal in of uit. |
| Kanaalnaam | De vriendelijke naam van het marketingkanaal. |
| Laatste aanraakkanaal overschrijven | Hiermee kunt u kiezen of u een bestaand, blijvend laatste aanraakkanaal wilt overschrijven met het geselecteerde kanaal. Als u dit selectievakje inschakelt, overschrijft elk kanaal (inclusief Direct en Intern) een bestaand laatste aanraakkanaal. Het resultaat is dat conversie wordt toegeschreven aan een kanaal dat geen krediet verdient. Met deze optie kunt u er bijvoorbeeld voor zorgen dat het Direct-kanaal geen conversiekrediet ontvangt als de gebruiker eerder via het Natural Search-kanaal was aangeschaft. |
| Kanaaluitsplitsing | Hiermee kunt u een kanaal opsplitsen op basis van deze waarde. U kunt mogelijke kanaalstoringen (subkanalen) toevoegen bij het maken van [marketingkanaalclassificaties](/help/components/c-marketing-channels/classifictions-mchannel.md). |
| Type | Hiermee bepaalt u hoe de gebruiker naar uw site is gekomen. U kunt Online of Offline selecteren. Gebruik online kanalen voor bezoekers die via een zoekmachine of e-mailcampagne komen. Offlinekanalen zijn van toepassing op bezoekers die uw site hebben gevonden via krantencoupons of advertenties in tijdschriften. De off-line kanalen omvatten gewoonlijk gegevens die door het melden van Gegevensbronnen worden ingevoerd. See [Data Sources](https://docs.adobe.com/content/help/en/analytics/import/data-sources/datasrc-home.html). Zie Offlinegegevens [toevoegen](/help/components/c-marketing-channels/c-getting-started-mchannel.md). |
| Kleur | Alleen rapporten en analyses: De kleur die aan dit marketingkanaal is gekoppeld. Deze kleur vertegenwoordigt het kanaal in het rapport van het Kanaal van de Marketing. |

### Beste werkwijzen overschrijven

U kunt het beste de optie last-touch negeren uitschakelen voor Direct en Intern kanaal, zodat ze geen krediet kunnen opnemen van andere hardnekkige laatste aanraakkanalen (of van elkaar).

![](assets/int-channel2.png)

## Kanaalregels definiëren

Alvorens de kanalen en de kanaalgegevens in het rapport kunnen worden getoond, creeer de kanalen en de onderliggende regels die gegevens verwerken. U kunt ook opgeven hoe lang de periode [van de](/help/components/c-marketing-channels/visitor-engagement.md) betrokkenheid van de bezoeker moet duren.

Adobe biedt verschillende vooraf gedefinieerde kanalen tijdens een [automatische installatie](/help/components/c-marketing-channels/c-getting-started-mchannel.md) die u naar wens kunt bewerken. Bovendien, kunt u deze opstelling wijzigen en douaneregels binnen de de verwerkingsregels [van het Kanaal van de](/help/components/c-marketing-channels/c-rules.md)Marketing bepalen.

>[!NOTE]
>
>Adobe raadt u aan uw rapport in te stellen in een rapportsuite die u als sjabloon voor testdoeleinden kunt gebruiken. U kunt het malplaatje gebruiken om kanaal en regelreeksen globaal op één of meerdere reeksen van het productierapport toe te passen.
>
>Zie [Suite-instellingen voor sjabloonrapport toepassen op meerdere rapportsets](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

