---
title: Afmelden voor toestemmingsbeheer
description: Zie welke privacy-instellingen een bezoeker heeft opgegeven.
exl-id: 2bf4d22c-5b24-47fb-b489-49388fcca5b1
feature: Dimensions
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 2%

---

# Afmelden voor toestemmingsbeheer

De &quot;Opt-uit van het Beheer van de Toestemming&#39; [ dimensie ](overview.md) toont welke privacymontages die een bezoeker uitdrukkelijk uit heeft gekozen. U kunt deze dimensie gebruiken om gegevens te filteren op basis van privacy-instellingen, of de meest gebruikelijke redenen voor privacy-opt-out bekijken.

## Deze dimensie vullen met gegevens

Deze afmeting verzamelt gegevens van de volgende [ variabelen van de Contextgegevens ](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['cm.ssf']` wanneer ingesteld op `1` . Wanneer `cm.ssf` gelijk is aan `0` of leeg is, heeft deze variabele geen effect.
* `contextData.['opt.dmp']` wanneer ingesteld op `N` . Als `opt.dmp` `Y` evenaart, is de [ Opt-In van het Beheer van de Toestemming ](cm-opt-in.md) dimensie bevolkt in plaats daarvan.
* `contextData.['opt.sell']` wanneer ingesteld op `N` . Als `opt.sell` `Y` evenaart, is de [ Opt-In van het Beheer van de Toestemming ](cm-opt-in.md) dimensie bevolkt in plaats daarvan.

Uw organisatie bepaalt de logica om deze variabelen van contextgegevens uit te voeren. Ze blijven niet behouden na de hit waarop ze zijn ingesteld. U moet dus elke variabele van de contextgegevens op elke pagina instellen.

## Dimension-objecten

Dimension-items bevatten de volgende drie waarden:

* **`SSF`**: De bezoeker verkoos uit [ server-kant het door:sturen ](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md). Dit item voor dimensie is aanwezig wanneer de variabele voor contextgegevens `cm.ssf` gelijk is aan `1` . Zie [ overzicht van de privacy van Gegevens ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/overview/data-privacy/data-privacy.html) in de gebruikersgids van Audience Manager voor meer informatie. De hit wordt niet doorgestuurd naar Adobe Audience Manager.
* **`DMP`**: De bezoeker heeft ervoor gekozen niet meer te delen naar platforms voor gegevensbeheer. Dit item voor dimensie is aanwezig wanneer de variabele voor contextgegevens `opt.dmp` gelijk is aan `N` . Net als `SSF` wordt de hit niet doorgestuurd naar Adobe Audience Manager.
* **`SELL`**: De bezoeker heeft ervoor gekozen de gegevens niet te delen of aan derden te verkopen. Deze dimensie is aanwezig wanneer de variabele van de contextgegevens `opt.sell` gelijk is aan `N` .
