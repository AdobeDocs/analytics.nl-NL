---
title: Invoerafmetingen
description: Hiermee geeft u de invoerafmetingen en het gebruik ervan weer.
keywords: entry page, entry site section, entry server, entry custom insight
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Invoerafmetingen

*Deze Help-pagina beschrijft hoe ingangen werken als een dimensie. Voor informatie over hoe de ingangen als metrisch werken, zie metrische[Ingangen](../metrics/entries.md).*

Invoerafmetingen zijn gebaseerd op bezoeken. Zij registreren de eerste afmetingswaarde, en stellen het voor de volledige duur van dat bezoek voort. De afmetingen van de ingang zijn beschikbaar voor alle variabelen met het kleven die onder de variabelen [van het](/help/admin/admin/c-traffic-variables/traffic-var.md) Verkeer in de reeksinstellingen van het Rapport worden toegelaten.

## Itemafmetingen vullen met gegevens

Een bepaalde ingangsdimensie is gebaseerd op zijn bijbehorende verkeersvariabele. Als de niet-entry variabele gegevens heeft, bevat zijn bijbehorende ingangsdimensie ook gegevens. Er zijn geen implementatiewijzigingen vereist voor invoerafmetingen als uw verkeersvariabelen gegevens bevatten.

## Dimensiewaarden

Aangezien de ingangsvariabelen typisch op douanetekenreeksen in uw implementatie gebaseerd zijn, bepaalt uw organisatie wat de afmetingswaarden zijn. Waarden in een opgegeven entry-dimensie komen overeen met waarden van de dimensies in de bijbehorende niet-entry-dimensie. Dimensiewaarden in de dimensie &#39;Entry page&#39; bevatten bijvoorbeeld vergelijkbare waarden voor de dimensie &#39;Page&#39;.

## Invoerpagina origineel

De oorspronkelijke afmeting van de pagina &#39;Entry&#39; werkt anders dan die van andere vermeldingen. In plaats van de ingangspagina voor een bepaald bezoek te bewaren, behoudt het de allereerste ingangspagina voor het volledige leven van het koekje van die bezoeker. Als u bijvoorbeeld aan land gaat `https://example.com/page4` voor uw eerste bezoek aan de site, laat u een jaar later landen op `https://example.com/store`, dan geeft de dimensie &#39;Entry page original&#39; `https://example.com/page4` de waarde van de dimensie weer.
