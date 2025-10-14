---
title: Invoerafmetingen
description: Hiermee geeft u de invoerafmetingen en het gebruik ervan weer.
keywords: entry page, entry site section, entry server, entry custom insight
feature: Dimensions
exl-id: 424e2a9a-05ac-4397-921b-c8d7567348ed
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Invoerafmetingen

*Deze hulppagina beschrijft hoe de ingangen als a [&#x200B; dimensie &#x200B;](overview.md) werken. Voor informatie over hoe de ingangen als metrisch werken, zie de [&#x200B; metrische Ingangen &#x200B;](../metrics/entries.md).*

De dimensies van de ingang zijn [&#x200B; op bezoek-Gebaseerd &#x200B;](../metrics/visits.md). Zij registreren het eerste afmetingspunt, en stellen het voor de volledige duur van dat bezoek voort. De dimensies van de ingang zijn beschikbaar voor alle variabelen met het kleven die onder [&#x200B; variabelen van het Verkeer &#x200B;](/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md) in de reeksinstellingen van het Rapport worden toegelaten.

>[!TIP]
>Als u gegevens wilt zien die op de eerste klap van een bezoek in plaats van de eerste waarde in een bezoek worden gebaseerd, kunt u a [&#x200B; segment &#x200B;](/help/components/segmentation/seg-overview.md) gebruiken. Gebruik een klapcontainer waar [&#x200B; de diepte van het Actief &#x200B;](hit-depth.md) 1 evenaart, dan gebruik dat segment met de gewenste variabele.

## Itemafmetingen vullen met gegevens

Een bepaalde ingang [&#x200B; dimensie &#x200B;](overview.md) is gebaseerd op zijn bijbehorende verkeersvariabele. Als de niet-entry variabele gegevens heeft, bevat zijn bijbehorende ingangsdimensie ook gegevens. Er zijn geen implementatiewijzigingen vereist voor invoerafmetingen als uw verkeersvariabelen gegevens bevatten.

## Dimension-objecten

Aangezien de ingangsvariabelen typisch op douanetekenreeksen in uw implementatie gebaseerd zijn, bepaalt uw organisatie wat de afmetingspunten zijn. De waarden in een bepaalde ingangsdimensie passen afmetingspunten in zijn bijbehorende niet-ingangsdimensie aan. Dimensie-items in de afmeting &#39;Pagina-item&#39; bevatten bijvoorbeeld vergelijkbare afmetingsitems in de afmeting &#39;Pagina&#39;.

## Invoerpagina origineel

De oorspronkelijke afmeting van de pagina &#39;Entry&#39; werkt anders dan die van andere vermeldingen. In plaats van de ingangspagina voor een bepaald bezoek te bewaren, behoudt het de allereerste ingangspagina voor het volledige leven van het koekje van die bezoeker. Als u bijvoorbeeld op `https://example.com/page4` landt voor uw eerste bezoek aan de site, en een jaar later op `https://example.com/store` landt, wordt met de dimensie &#39;Pagina in eerste opname&#39; `https://example.com/page4` het dimensie-item weergegeven.
