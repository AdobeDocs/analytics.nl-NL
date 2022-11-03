---
title: Afmelden voor toestemmingsbeheer
description: Zie welke privacy-instellingen een bezoeker heeft opgegeven.
source-git-commit: c305f74d5047db57509de8ff9ee03b8144009f5a
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 2%

---

# Afmelden voor toestemmingsbeheer

De dimensie &#39;Opt-Out voor beheer van toestemming&#39; geeft aan welke privacy-instellingen een bezoeker expliciet heeft opgegeven. U kunt deze dimensie gebruiken om gegevens te filteren op basis van privacy-instellingen, of de meest gebruikelijke redenen voor privacy-opt-out bekijken.

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt gegevens van het volgende [Contextgegevensvariabelen](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['cm.ssf']` wanneer ingesteld op `1`. Indien `cm.ssf` equals `0` of leeg is, heeft deze variabele geen effect.
* `contextData.['opt.dmp']` wanneer ingesteld op `N`. Indien `opt.dmp` equals `Y`de [Inschakelen voor beheer van toestemming](cm-opt-in.md) in plaats daarvan wordt de dimensie gevuld.
* `contextData.['opt.sell']` wanneer ingesteld op `N`. Indien `opt.sell` equals `Y`de [Inschakelen voor beheer van toestemming](cm-opt-in.md) in plaats daarvan wordt de dimensie gevuld.

Uw organisatie bepaalt de logica om deze variabelen van contextgegevens uit te voeren. Ze blijven niet behouden na de hit waarop ze zijn ingesteld. U moet dus elke variabele van de contextgegevens op elke pagina instellen.

## Dimension-items

Dimension-items bevatten de volgende drie waarden:

* **`SSF`**: De bezoeker heeft ervoor gekozen [Server-side doorsturen](/help/admin/admin/c-server-side-forwarding/ssf.md). Deze dimensie-item is aanwezig wanneer de variabele van de contextgegevens `cm.ssf` equals `1`. Zie [Overzicht van privacy van gegevens](https://experienceleague.adobe.com/docs/audience-manager/user-guide/overview/data-privacy/data-privacy.html) in de gebruikershandleiding van de Audience Manager voor meer informatie. De hit wordt niet doorgestuurd naar Adobe Audience Manager.
* **`DMP`**: De bezoeker heeft ervoor gekozen niet meer te delen naar gegevenbeheer-platforms. Deze dimensie-item is aanwezig wanneer de variabele van de contextgegevens `opt.dmp` equals `N`. Vergelijkbaar met `SSF`, wordt de treffer niet doorgestuurd naar Adobe Audience Manager.
* **`SELL`**: De bezoeker heeft ervoor gekozen de gegevens niet te delen of aan derden te verkopen. Deze dimensie is aanwezig wanneer de variabele van de contextgegevens `opt.sell` equals `N`.
