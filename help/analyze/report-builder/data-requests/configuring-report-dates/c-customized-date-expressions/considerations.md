---
description: Twee belangrijke overwegingen wanneer het gebruiken van de Customize Uitdrukking om de datumwaaier te plaatsen
title: Aangepaste overwegingen voor datums
uuid: a3bb3a63-0f15-4292-ade7-4ea852fe68c8
feature: Report Builder
role: User, Admin
exl-id: 66b817b3-7e9e-4030-92f3-797e730f9661
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Aangepaste overwegingen voor datums

Twee belangrijke overwegingen wanneer het gebruiken van de Customize Uitdrukking om de datumwaaier te plaatsen:

* De dag het rapport (van) in werking wordt gesteld (of de verzoeken worden verfrist) bepaalt welke gegevens beschikbaar zijn.
* De rollover van begin- en einddatum van het rapport is van invloed op het datumbereik waarop het rapport betrekking heeft.

Omdat de beschikbaarheid van gegevens zowel aan het tijdkader van het rapport als de datum gevoelig is die u verzoeken in het rapport vernieuwt, zorg ervoor dat u het rapport op de aangewezen dag in werking stelt om de gewenste informatie te halen. In de onderstaande voorbeelden worden deze twee overwegingen toegelicht.

Stel dat u een verzoek indient om [!UICONTROL Page Views] met geaggregeerde granulariteit. In Noord-Amerika begint de week op zondag. Om bijgewerkte rapporten voor de periode van Zondag tot Zaterdag (bijvoorbeeld, 23 november tot 29 november 2008) te verkrijgen, stel het rapport (verfrist verzoeken) op Zondag (30 november) voor de vorige week (11/23 tot 11/29) in werking.

Gebruik deze aangepaste expressie:

*Van:* cw-1w *Aan:* cw-1d

Een analyse van de aangepaste expressie wanneer de [!UICONTROL End Date] voor het verzoek: 11/30:

*Van:* cw-1w

de dag van de huidige week die op zondag begint, 30 min zeven dagen = de dag van de vorige week die op zondag, 23 november begint

*Aan:* cw-1d

de dag van de huidige week die op zondag begint, 30 november minus één dag = Zaterdag, 29 november

Nadat de aangepaste uitdrukking aan spreadsheet in kaart wordt gebracht, vernieuw het verzoek gebruikend zondag, 30 November, 2008 als inclusieve [!UICONTROL End Date] voor de zwevende aanvraag. De gegevens weerspiegelen de periode van week tot week.

Als in plaats daarvan u de uitdrukking verfrist en zaterdag, 29 november als specificeert [!UICONTROL End Date] voor het zwevende verzoek weerspiegelen de gegevens de week 11/16 tot en met 11/22. De reden hiervoor is dat de referentiedatum voor de aanvraag een dag eerder vernieuwt.

Hier zijn de verschillen wanneer de [!UICONTROL End Date] voor het verzoek: 11/29:

*Van:* cw-1w

de dag van de huidige week die op zondag begint, 23 november min zeven dagen = de dag van de vorige week die op zondag, 16 november begint

*Aan:* cw-1d

de dag van de huidige week die op zondag begint, 23 november minus één dag = zaterdag, 22 november

In Europa en in sommige andere landen begint de week op maandag in plaats van op zondag. In dit geval kunt u de kalender aanpassen om de begindatum te wijzigen. (Zie [Aangepaste kalender](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md).)
