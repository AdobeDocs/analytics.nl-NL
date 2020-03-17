---
description: Een groep rapporten die op weganalyse wordt gebaseerd. Technisch gezien betekent tekenen dat de naam van een pagina wordt gewijzigd (van de ene waarde naar de andere).
title: Plakken
topic: Reports
uuid: c4ff9fa8-e567-4039-9c86-322800a942da
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Plakken

Een groep rapporten die op weganalyse wordt gebaseerd. Technisch gezien betekent tekenen dat de naam van een pagina wordt gewijzigd (van de ene waarde naar de andere).

Gebruik [Analyse Workspace Flow](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/flow.html) voor flexibelere tekenopties.

> [!NOTE] Ga naar **[!UICONTROL Admin > Report Suites > Edit Settings > Traffic > Traffic Variables]** om plakken mogelijk te maken. Neem contact op met de klantenservice om het plakken in de Site-sectie en de serverrapporten mogelijk te maken.

Als u de orde moet weten waarin de waarden worden verzameld, dan moet u het kleven voor de variabele toelaten die die waarden verzamelt. Paden is standaard ingeschakeld voor pagina&#39;s. Pathing is niet standaard ingeschakeld voor props, omdat dit alleen in bepaalde gevallen van toepassing is. Neem contact op met de klantenservice om het plakken op een prop in te schakelen.

> [!NOTE] Wanneer u in Ad hoc Analyse classificaties inschakelt op een proxy, worden de maatstaven voor het tekenen beschikbaar voor alle classificaties die zijn ingesteld voor de ingeschakelde proxy.

**Voorbeeld - Tekenen op sitesecties**

Als u paden inschakelt voor de *`s.channel`* variabele, kunt u bijhouden hoe bezoekers van de site schakelen tussen secties van de site (wanneer de waarde verandert).

![](assets/path_sections.png)

Verf is vervolgens beschikbaar in verschillende padrapporten, zoals [!UICONTROL Next Site Section Flow]een rapport waarin wordt weergegeven hoe bezoekers door paginagroepen of secties van uw site bladeren.

![](assets/paths_report.png)

**Voorbeeld - Tekenen op zoekopdrachten**

Dit zelfde concept van het gaan van één waarde naar een andere waarde is ook op andere verkeersvariabelen van toepassing, met inbegrip van *`s.props`*. Als u bijvoorbeeld het plakken inschakelt voor de interne zoekterm *`s.prop`*, ziet u dat de padbezoekers de zoektermen doorlopen.

**Voorbeeld: status van Paden per aanmelding**

Mogelijk wilt u weten hoe mensen door uw site gaan op basis van de aanmeldingsstatus van een bezoeker. Om deze informatie te zien zou u niet de het plakken rapporten voor login status bekijken, omdat zij u zouden tonen hoe de bezoekers waarden in dat rapport veranderden, of hoe de bezoekers van het programma geopende in het programma geopende konden veranderd zijn. In plaats daarvan voegt u de segmentwaarde samen met de *`s.pageName`* variabele en vervolgens het pad naar die resulterende variabele. Hier volgt een voorbeeldcode voor pagina-paden per lidstatus:

```js
s.pageName="Home Page"; 
s.prop18="Gold"; // Member Status 
s.prop19=s.prop18 + ":" + s.pageName;
```

Schakel vervolgens de optie voor plakken in *`s.prop19`* om te zien hoe leden pagina&#39;s doorlopen.

> [!NOTE] Als u ad hoc analyse uitvoert, kunt u paginaden segmenteren zonder de behoefte om segmentwaarden samen te voegen, en om het even welk segment op het kleven rapporten toepassen.

