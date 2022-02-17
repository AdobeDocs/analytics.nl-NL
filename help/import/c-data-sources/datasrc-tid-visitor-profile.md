---
description: Gebruik transactie-id in gegevensbronnen om online en offline gegevens aan elkaar te koppelen.
title: Transactie-id en bezoekersprofielen
topic-fix: Developer and implementation
feature: Data Sources
exl-id: ca5f9e8d-853f-4444-a8fd-a20933ef33d7
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 1%

---

# Transactie-id en bezoekersprofielen

Deze sectie bevat belangrijke informatie over de gegevens van het bezoekersprofiel die wordt gebruikt wanneer het uploaden van gegevens gebruikend een transactie-ID.

## Transactie-id {#section_B248FA93ECC84F6290D237EB83618070}

Wanneer een transactie-id wordt opgenomen, wordt een &quot;momentopname&quot; van het huidige bezoekersprofiel opgeslagen en gekoppeld aan de transactie-id. Deze &quot;momentopname&quot; bevat alle variabelewaarden die momenteel zijn ingesteld voor de bezoeker, inclusief persisterende variabelen (zoals eVars en campagnes). De waarden in deze momentopname ontvangen attributie voor succesgebeurtenissen, koopgebeurtenissen, en opbrengst later geupload gebruikend zelfde transactie ID.

Nadat het bezoekersprofiel &quot;momentopname&quot; is gemaakt, wordt deze niet bijgewerkt wanneer het huidige bezoekersprofiel verandert (vanwege onlinegedrag), wordt het alleen bijgewerkt met gegevens die zijn geüpload met behulp van transactie-id-gegevensbronnen. Als u dezelfde transactie-id-waarde op meerdere pagina&#39;s instelt tijdens hetzelfde bezoek, wordt de gegevensbronupload die later plaatsvindt gekoppeld aan de momentopname die de eerste keer dat de id werd ingesteld, is gemaakt.

**Meerdere uploads**

Meerdere rijen gegevens kunnen naar dezelfde transactie-id worden geüpload gedurende het verloopvenster van de transactie-id (zie hieronder).

**Variabele vervaldatum**

Variabele vervaldatum wordt niet in aanmerking genomen voor transactie-id&#39;s, omdat de gegevens van het bezoekersprofiel de bezoekersstatus moeten weerspiegelen op het moment van de transactie. Bijvoorbeeld, als eVar1 wordt gevormd om na bezoek te verlopen, ontvangt de waarde in het bezoekersprofiel &quot;momentopname&quot;krediet zelfs als de waarde in het huidige bezoekersprofiel is verlopen of is vervangen wanneer de gegevens van transactieID worden geupload.

**Producten**

Productinformatie (van `s.products`) is niet opgenomen in de &quot;momentopname&quot; van het bezoekersprofiel, dus moet u de bijbehorende productgegevens in het gegevensbronbestand en de transactie-id uploaden. Merk op dat u slechts één product per rij kunt specificeren, zodat zou u veelvoudige rijen met zelfde transactieID kunnen moeten uploaden om alle producten te omvatten.

**Geüploade eVar persistentie**

Vars die zijn geüpload met de gegevensbronnen van de transactie-id, worden toegevoegd aan de &quot;momentopname&quot; van het bezoekersprofiel. Ze worden niet toegevoegd aan het huidige bezoekersprofiel of de virtuele cookie. Dit betekent dat online gedrag dat na het uploaden plaatsvindt, niet wordt gecrediteerd voor geüploade eVars, aangezien deze waarden geen deel uitmaken van het huidige bezoekersprofiel.

**Venster Verlopen van transactie-id**

Het bezoekersprofiel &quot;momentopname&quot;verbonden aan een transactie ID is verkiesbaar voor schrapping na 90 dagen, hoewel het daadwerkelijke schrappingsprogramma varieert. Indien nodig kunt u contact opnemen met de klantenservice van Adobe om het verloopvenster te verlengen. Als een rij wordt geüpload na het verloopvenster van de transactie-id, worden de gegevens in de rij opgenomen, maar geen van de gegevens in het bezoekersprofiel &quot;momentopname&quot; wordt gecrediteerd als het profiel is verwijderd.

## Uitsplitsingen en segmentatie met behulp van transactie-id&#39;s {#section_A4D39291200A42C496122FDB9EF6EF68}

Vars die zijn geüpload met behulp van gegevensbronnen kunnen worden gebruikt voor het uitsplitsen van eVars die zijn opgenomen in de &quot;momentopname&quot; van het bezoekersprofiel. Aangezien deze gegevens los staan van het huidige bezoekersprofiel, kunt u niet uitsplitsen naar andere eVars die vóór of nadat de transactie-id is ingesteld, zijn ingesteld maar geen deel uitmaken van de &quot;momentopname&quot;.

Er zijn een paar manieren om gekoppelde bezoekersgegevens weer te geven die mogelijk niet beschikbaar zijn in een uitsplitsing. In de rapporten van het gegevenspakhuis, kunt u de gegevens van transactieidentiteitskaart met een bezoekersidentiteitskaart bekijken die de andere klappen van de bezoeker aanpast. Hoewel deze transactie-id-rijen zijn uitgesloten bij het tellen van bezoeken/bezoekers per dag, worden ze gebruikt bij het berekenen van de meeste cijfers en in segmenten.

Dientengevolge, kunt u een segment van bezoekers bouwen die één of andere off-line gebeurtenis uitvoeren die gebruikend de gegevensbronnen van identiteitskaart van de transactie werd geupload. Hiermee wordt alles geretourneerd wat de bezoeker voor en na de transactie-id-gebeurtenis heeft gedaan.

Op dezelfde manier kunt u met deelname van bezoekers zien hoe de transactie-id-props en eVars aan een online gebeurtenis voorafgingen, of hoe online props en eVars aan een transactie-id-gebeurtenis voorafgingen.
