---
title: Afmetingen afsluiten
description: Vermeldt de exit-afmetingen en het gebruik ervan.
keywords: afsluitpagina, sectie Site afsluiten, server afsluiten, aangepast inzicht afsluiten
feature: Dimensions
exl-id: b2b1ee88-e5c3-44b5-8159-85ec53d20258
source-git-commit: 17b5185e5358d661157c20a2504cacdbd4a2cc3d
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Afmetingen afsluiten

*Deze Help-pagina beschrijft hoe afsluiten werkt als een dimensie. Voor informatie over hoe de uitgang als metrisch werkt, zie [Afsluiten](../metrics/exits.md) metrisch.*

De dimensies van de uitgang registreren het laatste afmetingspunt, en passen het met terugwerkende kracht op alle treffers in het bezoek toe. Afsluitafmetingen zijn beschikbaar voor alle variabelen waarvoor tekenen is ingeschakeld onder [Verkeersvariabelen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) in de instellingen van de rapportsuite.

## Afsluitafmetingen vullen met gegevens

Een bepaalde uitgangsdimensie is gebaseerd op zijn bijbehorende verkeersvariabele. Als de niet-uitgangsvariabele gegevens heeft, bevat zijn bijbehorende uitgangsdimensie ook gegevens. Er zijn geen implementatiewijzigingen vereist voor exit-afmetingen als uw verkeersvariabelen gegevens bevatten.

## Dimension-items

Aangezien de uitgangsvariabelen typisch op douanetekenreeksen in uw implementatie gebaseerd zijn, bepaalt uw organisatie wat de afmetingspunten zijn. De waarden in een bepaalde uitgangsdimensie passen afmetingspunten in zijn bijbehorende niet-uitgang afmeting aan. Dimensie-items in de dimensie Pagina afsluiten bevatten bijvoorbeeld vergelijkbare dimensies in de dimensie Pagina.
