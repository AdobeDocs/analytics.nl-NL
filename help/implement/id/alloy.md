---
title: Bezoekersidentificatie met de Web SDK JavaScript-bibliotheek
description: Identificeer bezoekers correct wanneer het uitvoeren van de bibliotheek van SDK van het Web JavaScript.
source-git-commit: 779ba5b0a1d71467aaaf3872fd707cc323ae8af2
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Bezoekersidentificatie met de Web SDK JavaScript-bibliotheek

Adobe Experience Platform Web SDK (`alloy.js`) biedt een verenigde, moderne benadering van gegevensinzameling voor alle toepassingen van Adobe Experience Cloud, met inbegrip van Adobe Analytics aan. Identiteitsgegevens kunnen worden uitgebreid voor ondersteuning van aangepaste id&#39;s en meerdere naamruimten met behulp van XDM&#39;s `identityMap` . Adobe raadt u aan de Adobe Experience Cloud ID Service als primaire id voor Analytics te gebruiken en andere opties voor identiteitsbeheer voor geavanceerde scenario&#39;s te gebruiken.

Als uw organisatie de Web SDK JavaScript-bibliotheek gebruikt om gegevens naar Adobe Analytics te verzenden, is een minimale configuratie vereist voor bezoekersidentificatie. De Bezoeker-id-service wordt in de oorspronkelijke versie naar de bibliotheek geschreven, waarbij u alleen **[!UICONTROL Edge Domain]** hoeft in te stellen in de opdracht `configure` . Als dit veld op de gewenste waarde is ingesteld, werkt de identificatie van de bezoeker zonder aanvullende configuratie.
