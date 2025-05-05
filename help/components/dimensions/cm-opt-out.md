---
title: Afmelden voor toestemmingsbeheer
description: Zie welke privacy-instellingen een bezoeker heeft opgegeven.
exl-id: 2bf4d22c-5b24-47fb-b489-49388fcca5b1
feature: Dimensions
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 2%

---

# Afmelden voor toestemmingsbeheer

De optie &#39;Opt-out voor beheer van toestemming&#39; [dimensie](overview.md) geeft aan welke privacy-instellingen een bezoeker expliciet heeft opgegeven. U kunt deze dimensie gebruiken om gegevens te filteren op basis van privacy-instellingen, of de meest gebruikelijke redenen voor privacy-opt-out bekijken.

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt gegevens van het volgende [Contextgegevensvariabelen](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['cm.ssf']` wanneer ingesteld op `1`. Indien `cm.ssf` equals `0` of leeg is, heeft deze variabele geen effect.
* `contextData.['opt.dmp']` wanneer ingesteld op `N`. Indien `opt.dmp` equals `Y`de [Inschakelen voor beheer van toestemming](cm-opt-in.md) in plaats daarvan wordt de dimensie gevuld.
* `contextData.['opt.sell']` wanneer ingesteld op `N`. Indien `opt.sell` equals `Y`de [Inschakelen voor beheer van toestemming](cm-opt-in.md) in plaats daarvan wordt de dimensie gevuld.

Uw organisatie bepaalt de logica om deze variabelen van contextgegevens uit te voeren. Ze blijven niet behouden na de hit waarop ze zijn ingesteld. U moet dus elke variabele van de contextgegevens op elke pagina instellen.

## Dimension-items

Items van het Dimension bevatten de volgende drie waarden:

* **`SSF`**: De bezoeker heeft gekozen uit [Server-side doorsturen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md). Deze dimensie-item is aanwezig wanneer de variabele van de contextgegevens `cm.ssf` equals `1`. Zie [Overzicht van privacy van gegevens](https://experienceleague.adobe.com/docs/audience-manager/user-guide/overview/data-privacy/data-privacy.html?lang=nl-NL) in de gebruikershandleiding van de Audience Manager voor meer informatie. De hit wordt niet doorgestuurd naar Adobe Audience Manager.
* **`DMP`**: De bezoeker heeft ervoor gekozen niet meer te delen naar platforms voor gegevensbeheer. Deze dimensie-item is aanwezig wanneer de variabele van de contextgegevens `opt.dmp` equals `N`. Vergelijkbaar met `SSF`, wordt de treffer niet doorgestuurd naar Adobe Audience Manager.
* **`SELL`**: De bezoeker heeft ervoor gekozen de gegevens niet te delen of aan derden te verkopen. Deze dimensie is aanwezig wanneer de variabele contextgegevens `opt.sell` equals `N`.
