---
title: Gegevensbronnen van transactie-id
description: Gebruik opgeslagen waarden van een online hit om offline treffers die een transactie-id delen, te verrijken.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
role: Admin
source-git-commit: 0a65114d598b7c6d2871a2446ad4d574b9ca44bb
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Gegevensbronnen van transactie-id

De gegevensbronnen van identiteitskaart van de transactie zijn een variatie summiere gegevensbronnen die u waarden kunt toepassen die van een online slag aan off-line rijen worden bewaard die zelfde transactieidentiteitskaart delen. Deze benadering is handig wanneer u een transactie online vastlegt, maar later details van een ander systeem ontvangt. De primaire voorbeelden omvatten productwinst, boekende annuleringen, of resultaten van vraagcentrum interactie.

>[!NOTE]
>
>Alvorens de gegevensbronnen van identiteitskaart van de transactie te gebruiken, moet u het in [ Algemene Montages van de Rekening ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) voor de gewenste rapportreeks eerst toelaten.

## Hoe werkt het

Het concept transactie-id&#39;s vereist twee onderdelen:

* **Online hit**: Om het even welke volledige Bevolking Analytics die naar een rapportreeks (AppMeasurement, Web SDK, API, enz.) wordt verzonden. Bij deze hit stelt u de implementatievariabele [`transactionID`](/help/implement/vars/page-vars/transactionid.md) in.
* **Offline hit**: Een rij die door gegevensbronnen wordt geupload. Neem in het bestand de kolom `transactionID` op met een waarde die overeenkomt met een online hit.

Wanneer u een online hit verzendt die de implementatievariabele `transactionID` bevat, maakt Adobe een &quot;momentopname&quot; van de volgende afmetingen die op dat punt zijn ingesteld of aanwezig zijn:

* [Categorie](/help/components/dimensions/category.md)
* [Dagen vóór eerste aankoop](/help/components/dimensions/days-before-first-purchase.md)
* [Dagen sinds laatste aankoop](/help/components/dimensions/days-since-last-purchase.md)
* [eVars 1-250](/help/components/dimensions/evar.md)
* De eigenschap-specifieke dimensies die in [ worden toegelaten de reeksinstellingen van het Rapport ](/help/admin/admin/c-manage-report-suites/report-suites-admin.md) die zich zo ook aan eVars gedragen. Functiespecifieke afmetingen die zich op dezelfde manier gedragen als props, worden niet opgenomen.
* [Lijstvariabelen](/help/implement/vars/page-vars/list.md)
* [Marketingkanaal](/help/components/dimensions/marketing-channel.md)
* [Detailgegevens marketingkanaal](/help/components/dimensions/marketing-detail.md)
* [Mobiele afmetingen](/help/components/dimensions/mobile-dimensions.md)
* [Origineel verwijzend domein](/help/components/dimensions/original-referring-domain.md)
* [Product](/help/components/dimensions/product.md)
* [Verwijzen naar domein](/help/components/dimensions/referring-domain.md)
* [Zoekmachine](/help/components/dimensions/search-engine.md)
* [Trefwoord zoeken](/help/components/dimensions/search-keyword.md)
* [Code bijhouden](/help/components/dimensions/tracking-code.md)
* [Bezoek nummer](/help/components/dimensions/visit-number.md)

>[!NOTE]
>
>De metriek (zoals a [ Orders ](/help/components/metrics/orders.md) of [ de gebeurtenissen van de Douane ](/help/components/metrics/custom-events.md)) zijn niet inbegrepen in de &quot;momentopname&quot;.

Wanneer u een offline hit uploadt via gegevensbronnen die een overeenkomende transactie-id bevatten, worden alle beschikbare afmetingen in de &quot;momentopname&quot; automatisch toegevoegd aan de gegevensbronrij. Als een bepaalde dimensie aanwezig is in zowel online als off-line slag, wordt de off-line klapwaarde gebruikt.

>[!IMPORTANT]
>
>Het concept van de gegevensbronnen van transactieID slechts helpen gegevensbronrijen (off-line klappen) vullen. Ze hebben geen invloed op of veranderen de online hit niet.

## Overwegingen voor de gegevensbron van de transactie-id

Gegevensbronnen van transactie-id hebben de volgende eigenschappen:

* De online gegevens moeten eerst worden verzameld en verwerkt. Als een transactie-id-gegevensbron wordt geüpload voordat een rapportsuite een hit verwerkt die overeenkomt met die transactie-id, worden de gegevens behandeld als een summiere gegevensbron.
* Transactie-id&#39;s die uit online treffers zijn verzameld, verlopen na 25 maanden.
* Gegevensbronnen die met een verlopen transactie-id zijn geüpload, worden op dezelfde manier behandeld als gegevens die zonder transactie-id zijn geüpload.
* Als u dezelfde transactie-id instelt voor meerdere online treffers, wordt alleen de &#39;momentopname&#39; van de eerste instantie gebruikt. Volgende dubbele transactie-ID online treffers worden verwerkt alsof ze geen transactie-ID hebben.
* Zodra u een bepaalde `transactionID` waarde bevolkt, wordt de bijbehorende &quot;momentopname&quot;beschouwd als onveranderlijk tot die transactie-identiteitskaart verloopt.
* Als u dezelfde transactie-id instelt op meerdere gegevensbronrijen, worden alle beschikbare afmetingen van de online hit toegevoegd aan elke offline hit. Offlinetreffers voor dezelfde transactie-id kennen elkaar niets; er worden geen gegevens doorgegeven tussen offline-treffers.
