---
title: Gegevens uitsluiten in Adobe Analytics
description: Leer verschillende methoden om gegevens zowel voor als na gegevensverzameling uit te sluiten.
exl-id: dee5bf3b-8bb3-48eb-908d-b4a981f17bfb
feature: Data Configuration and Collection
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Gegevens uitsluiten in Adobe Analytics

Het uitsluiten van gegevens wordt doorgaans gebruikt om te voorkomen dat de testinspanningen van uw organisatie productiegegevens vullen of om te voorkomen dat ongewenste gegevens de rapporten vervalsen. Gebruik een van de volgende methoden om gegevens van Adobe Analytics uit te sluiten, afhankelijk van uw gebruiksscenario.

## Gegevens na gegevensverzameling uitsluiten

De volgende methoden zijn manieren om gegevens in Analytics-rapportage uit te sluiten nadat Adobe-servers voor gegevensverzameling afbeeldingsaanvragen hebben ontvangen. Gegevens die met deze methoden zijn uitgesloten, tellen nog steeds mee voor aanroepen van factureerbare servers.

* **uitsluiten door IP**: Adobe Analytics verstrekt basisfunctionaliteit om gegevens voor IP adressen of waaiers in een rapportreeks uit te sluiten. Zie [ uitsluiten door IP ](/help/admin/tools/exclude-ip.md) in de Admin gebruikersgids.
* **Bot regels**: De Bot regels nemen verkeer van bekende beide koorden van de gebruikersagent en sluiten hen van de rapporten van Analytics uit. Gegevens die via beide regels zijn uitgesloten, worden in het Bots-rapport opgenomen. U kunt aangepaste botregels maken om extra gegevens uit te sluiten. Zie [ Bot Regels ](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md) in de Admin gebruikersgids.
* **VISTA regels**: Afhankelijk van de behoeften van uw organisatie, vallen die uw vereisten aanpassen worden verzonden naar een andere rapportreeks specifiek aan het ontvangen van uitgesloten gegevens. De regels van VISTA worden algemeen gebruikt tegen IP adressen, maar zijn niet beperkt tot hen. U kunt om het even welke afmeting gebruiken om gegevens in rapportreeksen op te nemen of uit te sluiten. De VISTA-regels zijn onderworpen aan extra kosten; neem contact op met uw Adobe-accountteam voor meer informatie.
* **Opt-out koekjes**: Alle bezoekers aan uw plaats kunnen vrijwillig uit worden gevolgd in Adobe Analytics opteren door een pagina specifiek voor uw het volgen server te bezoeken. Zie [ de opt-out verbindingen van het Uitvoeren ](/help/implement/js/opt-out.md) in de de gebruikersgids van het Voer uit.

>[!TIP]
>
>De verwerkingsregels kunnen geen gegevens uitsluiten of gegevens naar een andere rapportreeks verzenden. Bepaalde variabelen kunnen echter voorwaardelijk worden ingesteld en een segment kan worden gebruikt om die gegevens uit te sluiten van rapportage.

## Gegevens vóór gegevensverzameling uitsluiten

Gebruik de variabele [`abort`](/help/implement/vars/config-vars/abort.md) als u wilt voorkomen dat bepaalde resultaten de servers voor gegevensverzameling van Analytics bereiken. Deze markering voorkomt dat de afbeeldingsaanvraag wordt verzonden. Aanroepen van de Billable-server worden niet verhoogd voor afgebroken afbeeldingsaanvragen, omdat deze geen Adobe-gegevensverzamelingsservers bereiken.
