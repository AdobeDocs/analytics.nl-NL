---
title: Invoerafmetingen
description: Hiermee geeft u de invoerafmetingen en het gebruik ervan weer.
keywords: entry page, entry site section, entry server, entry custom understanding
feature: Dimensions
exl-id: 424e2a9a-05ac-4397-921b-c8d7567348ed
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# Invoerafmetingen

*Deze Help-pagina beschrijft hoe ingangen werken als een dimensie. Voor informatie over hoe de ingangen als metrisch werken, zie [Berichten](../metrics/entries.md) metrisch.*

Invoerafmetingen zijn gebaseerd op bezoeken. Zij registreren het eerste afmetingspunt, en stellen het voor de volledige duur van dat bezoek voort. Invoerafmetingen zijn beschikbaar voor alle variabelen waarbij tekenen is ingeschakeld onder [Verkeersvariabelen](/help/admin/admin/c-traffic-variables/traffic-var.md) in de instellingen van de rapportsuite.

## Itemafmetingen vullen met gegevens

Een bepaalde ingangsdimensie is gebaseerd op zijn bijbehorende verkeersvariabele. Als de niet-entry variabele gegevens heeft, bevat zijn bijbehorende ingangsdimensie ook gegevens. Er zijn geen implementatiewijzigingen vereist voor invoerafmetingen als uw verkeersvariabelen gegevens bevatten.

## Dimension-items

Aangezien de ingangsvariabelen typisch op douanetekenreeksen in uw implementatie gebaseerd zijn, bepaalt uw organisatie wat de afmetingspunten zijn. De waarden in een bepaalde ingangsdimensie passen afmetingspunten in zijn bijbehorende niet-ingangsdimensie aan. Dimensie-items in de afmeting &#39;Pagina-item&#39; bevatten bijvoorbeeld vergelijkbare afmetingsitems in de afmeting &#39;Pagina&#39;.

## Invoerpagina origineel

De oorspronkelijke afmeting van de pagina &#39;Entry&#39; werkt anders dan die van andere vermeldingen. In plaats van de ingangspagina voor een bepaald bezoek te bewaren, behoudt het de allereerste ingangspagina voor het volledige leven van het koekje van die bezoeker. Als u bijvoorbeeld landt op `https://example.com/page4` voor uw eerste bezoek aan de locatie , een jaar later landen `https://example.com/store`, De lijst met de oorspronkelijke afmetingen van de pagina Ingang `https://example.com/page4` als het dimensie-item.
