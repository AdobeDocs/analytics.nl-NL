---
title: Bezoekersidentificatie met de Web SDK-tagextensie
description: Identificeer bezoekers correct wanneer het uitvoeren van de de markeringsuitbreiding van SDK van het Web.
source-git-commit: 779ba5b0a1d71467aaaf3872fd707cc323ae8af2
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Bezoekersidentificatie met de Web SDK-tagextensie

De de markeringsuitbreiding van SDK van het Web in de Inzameling van Gegevens van Adobe Experience Platform machtigt organisaties om het Web SDK uit te voeren gebruikend een interface van het markeringsbeheer. Geavanceerde scenario&#39;s zoals het delen van identiteitskaart over verschillende domeinen en de migratie van het bezoekersprofiel worden gemakkelijk gevormd door uitbreidingsregels en acties. Met de Web SDK kunt u uw implementatie op de toekomst controleren en kunt u een naadloze upgrade naar Customer Journey Analytics uitvoeren.

Aangezien de Bezoeker-id-service in een native omgeving is gekoppeld aan de tagextensie, hoeft u alleen **[!UICONTROL Edge Domain]** in te stellen op de gewenste waarde. Als dit veld op de juiste wijze is ingesteld, werkt de identificatie van de bezoeker zonder aanvullende configuratie.

>[!NOTE]
>
>Neem de extensie van de service-tag voor bezoekers-id niet op als u de extensie van de Web SDK-tag gebruikt. De de markeringsuitbreiding van de Dienst van identiteitskaart van de Bezoeker wordt slechts vereist als u de [&#x200B; uitbreiding van Adobe Analytics &#x200B;](analytics-extension.md) gebruikt.
