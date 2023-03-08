---
title: Gegevens uitsluiten in Adobe Analytics
description: Leer verschillende methoden om gegevens zowel voor als na gegevensverzameling uit te sluiten.
exl-id: dee5bf3b-8bb3-48eb-908d-b4a981f17bfb
source-git-commit: b8640d1387a475e2a9dd082759f0514bd18c1b6e
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Gegevens uitsluiten in Adobe Analytics

Het uitsluiten van gegevens wordt doorgaans gebruikt om te voorkomen dat de testinspanningen van uw organisatie productiegegevens vullen of om te voorkomen dat ongewenste gegevens de rapporten vervalsen. Gebruik een van de volgende methoden om gegevens van Adobe Analytics uit te sluiten, afhankelijk van uw gebruiksscenario.

## Gegevens na gegevensverzameling uitsluiten

De volgende methoden zijn manieren om gegevens in Analytics-rapportage uit te sluiten nadat servers voor gegevensverzameling Adobe afbeeldingsverzoeken ontvangen. Gegevens die met deze methoden zijn uitgesloten, tellen nog steeds mee voor aanroepen van factureerbare servers.

* **Uitsluiten door IP**: Adobe Analytics verstrekt basisfunctionaliteit om gegevens voor IP adressen of waaiers in een rapportreeks uit te sluiten. Zie [Uitsluiten door IP](/help/admin/admin/exclude-ip.md) in de handleiding voor Admin-gebruikers.
* **Bot-regels**: Beide regels nemen verkeer van bekende zowel userAgent koorden en sluiten hen van de rapporten van de Analyse uit. Gegevens die via beide regels zijn uitgesloten, worden in het Bots-rapport opgenomen. U kunt aangepaste botregels maken om extra gegevens uit te sluiten. Zie [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) in de handleiding voor Admin-gebruikers.
* **VISTA-regels**: Afhankelijk van de behoeften van uw organisatie worden treffers die aan uw vereisten voldoen, verzonden naar een andere rapportsuite die is gewijd aan het ontvangen van uitgesloten gegevens. De regels van VISTA worden algemeen gebruikt tegen IP adressen, maar zijn niet beperkt tot hen. U kunt om het even welke afmeting gebruiken om gegevens in rapportreeksen op te nemen of uit te sluiten. de VISTA-regels zijn onderworpen aan extra kosten; Neem contact op met de accountmanager van uw organisatie voor meer informatie.
* **Uitschakelen van cookies**: Alle bezoekers van uw site kunnen zich vrijwillig afmelden om in Adobe Analytics te worden bijgehouden door een pagina te bezoeken die specifiek is voor uw trackingserver. Zie [Optie-outkoppelingen implementeren](/help/implement/js/opt-out.md) in de gebruikershandleiding Implementeren.

>[!TIP]
>
>De verwerkingsregels kunnen geen gegevens uitsluiten of gegevens naar een andere rapportreeks verzenden. Bepaalde variabelen kunnen echter voorwaardelijk worden ingesteld en een segment kan worden gebruikt om die gegevens uit te sluiten van rapportage.

## Gegevens vóór gegevensverzameling uitsluiten

Als u bepaalde klappen van de servers van de gegevensinzameling van de Analytics wilt verhinderen, gebruik [`abort`](/help/implement/vars/config-vars/abort.md) variabele. Deze markering voorkomt dat de afbeeldingsaanvraag wordt verzonden. De aanroepen van de Billable server worden niet verhoogd voor geaborteerde beeldverzoeken, aangezien zij de servers van de Adobe gegevensinzameling niet bereiken.
