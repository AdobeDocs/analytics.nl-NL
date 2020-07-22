---
title: Invoerafmetingen
description: Hiermee geeft u de invoerafmetingen en het gebruik ervan weer.
keywords: entry page, entry site section, entry server, entry custom insight
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Invoerafmetingen

*Deze Help-pagina beschrijft hoe ingangen werken als een dimensie. Voor informatie over hoe de ingangen als metrisch werken, zie metrische[Ingangen](../metrics/entries.md).*

Invoerafmetingen zijn gebaseerd op bezoeken. Zij registreren het eerste afmetingspunt, en stellen het voor de volledige duur van dat bezoek voort. De afmetingen van de ingang zijn beschikbaar voor alle variabelen met het kleven die onder de variabelen [van het](/help/admin/admin/c-traffic-variables/traffic-var.md) Verkeer in de reeksinstellingen van het Rapport worden toegelaten.

## Itemafmetingen vullen met gegevens

Een bepaalde ingangsdimensie is gebaseerd op zijn bijbehorende verkeersvariabele. Als de niet-entry variabele gegevens heeft, bevat zijn bijbehorende ingangsdimensie ook gegevens. Er zijn geen implementatiewijzigingen vereist voor invoerafmetingen als uw verkeersvariabelen gegevens bevatten.

## Dimensie-items

Aangezien de ingangsvariabelen typisch op douanetekenreeksen in uw implementatie gebaseerd zijn, bepaalt uw organisatie wat de afmetingspunten zijn. De waarden in een bepaalde ingangsdimensie passen afmetingspunten in zijn bijbehorende niet-ingangsdimensie aan. Dimensie-items in de afmeting &#39;Pagina-item&#39; bevatten bijvoorbeeld vergelijkbare afmetingsitems in de afmeting &#39;Pagina&#39;.

## Invoerpagina origineel

De oorspronkelijke afmeting van de pagina &#39;Entry&#39; werkt anders dan die van andere vermeldingen. In plaats van de ingangspagina voor een bepaald bezoek te bewaren, behoudt het de allereerste ingangspagina voor het volledige leven van het koekje van die bezoeker. Als u bijvoorbeeld aan land gaat `https://example.com/page4` voor uw eerste bezoek aan de site, en een jaar later op `https://example.com/store`de site landt, wordt de dimensie &#39;Pagina van item origineel&#39; weergegeven `https://example.com/page4` als dimensie-item.
