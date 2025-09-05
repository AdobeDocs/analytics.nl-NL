---
title: Afmetingen afsluiten
description: Vermeldt de exit-afmetingen en het gebruik ervan.
keywords: afsluitpagina, exit site-sectie, exit server, exit custom insight
feature: Dimensions
exl-id: b2b1ee88-e5c3-44b5-8159-85ec53d20258
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Afmetingen afsluiten

*Deze hulppagina beschrijft hoe de uitgang werk als a [ dimensie ](overview.md) is. Voor informatie over hoe uitgang werk als metrisch, zie [ metrisch weggaat ](../metrics/exits.md).*

De dimensies van de uitgang registreren het laatste afmetingspunt, en passen het met terugwerkende kracht op alle treffers in het bezoek toe. De dimensies van de uitgang zijn beschikbaar voor alle variabelen met het kleven die onder [ variabelen van het Verkeer ](/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md) in de reeksinstellingen van het Rapport worden toegelaten.

## Afsluitafmetingen vullen met gegevens

Een bepaalde uitgangsdimensie is gebaseerd op zijn bijbehorende verkeersvariabele. Als de niet-uitgangsvariabele gegevens heeft, bevat zijn bijbehorende uitgangsdimensie ook gegevens. Er zijn geen implementatiewijzigingen vereist voor exit-afmetingen als uw verkeersvariabelen gegevens bevatten.

## Dimension-objecten

Aangezien de uitgangsvariabelen typisch op douanetekenreeksen in uw implementatie gebaseerd zijn, bepaalt uw organisatie wat de afmetingspunten zijn. De waarden in een bepaalde uitgangsdimensie passen afmetingspunten in zijn bijbehorende niet-uitgang afmeting aan. Dimensie-items in de dimensie Pagina afsluiten bevatten bijvoorbeeld vergelijkbare dimensies in de dimensie Pagina.
