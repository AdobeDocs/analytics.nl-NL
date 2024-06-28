---
title: Invoerafmetingen
description: Hiermee geeft u de invoerafmetingen en het gebruik ervan weer.
keywords: entry page, entry site section, entry server, entry custom understanding
feature: Dimensions
exl-id: 424e2a9a-05ac-4397-921b-c8d7567348ed
source-git-commit: 66be48d0f41061d259cc53fb835ebd155294a710
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Invoerafmetingen

*Deze Help-pagina beschrijft hoe items werken als een [dimensie](overview.md). Voor informatie over hoe de ingangen als metrisch werken, zie [Berichten](../metrics/entries.md) metrisch.*

De afmetingen van het item zijn [op bezoek](../metrics/visits.md). Zij registreren het eerste afmetingspunt, en stellen het voor de volledige duur van dat bezoek voort. Invoerafmetingen zijn beschikbaar voor alle variabelen waarbij tekenen is ingeschakeld onder [verkeersvariabelen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) in de instellingen van de rapportsuite.

>[!TIP]
>Als u gegevens wilt zien op basis van de eerste treffer van een bezoek in plaats van de eerste waarde die tijdens een bezoek wordt getoond, kunt u een [segment](/help/components/segmentation/seg-overview.md). Gebruik een raakcontainer op de plaats waar [Hoogte](hit-depth.md) is gelijk aan 1, dan gebruik dat segment met de gewenste variabele.

## Itemafmetingen vullen met gegevens

Een bepaalde vermelding [dimensie](overview.md) is gebaseerd op zijn bijbehorende verkeersvariabele. Als de niet-entry variabele gegevens heeft, bevat zijn bijbehorende ingangsdimensie ook gegevens. Er zijn geen implementatiewijzigingen vereist voor invoerafmetingen als uw verkeersvariabelen gegevens bevatten.

## Dimension-items

Aangezien de ingangsvariabelen typisch op douanetekenreeksen in uw implementatie gebaseerd zijn, bepaalt uw organisatie wat de afmetingspunten zijn. De waarden in een bepaalde ingangsdimensie passen afmetingspunten in zijn bijbehorende niet-ingangsdimensie aan. Dimensie-items in de afmeting &#39;Pagina-item&#39; bevatten bijvoorbeeld vergelijkbare afmetingsitems in de afmeting &#39;Pagina&#39;.

## Invoerpagina origineel

De oorspronkelijke afmeting van de pagina &#39;Entry&#39; werkt anders dan die van andere vermeldingen. In plaats van de ingangspagina voor een bepaald bezoek te bewaren, behoudt het de allereerste ingangspagina voor het volledige leven van het koekje van die bezoeker. Als u bijvoorbeeld landt op `https://example.com/page4` voor uw eerste bezoek aan de locatie , een jaar later landen `https://example.com/store`, De lijst met de oorspronkelijke afmetingen van de pagina Ingang `https://example.com/page4` als het dimensie-item.
