---
description: Verklaart de ononderbroken strategie van de eigenschapversie voor Adobe Analytics
title: Adobe Analytics-functiereleases
feature: Release Notes
exl-id: 1e403bef-4aab-4a9a-a358-62449ce801ff
source-git-commit: cc18ac659400b572967e06cc2946d602e825bc97
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 1%

---

# Adobe Analytics-functiereleases

De versies van Adobe Analytics werken op een ononderbroken leveringsmodel dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat.

## Releasestrategie

[!UICONTROL Analysis Workspace] gebruikt functiemarkeringen (ook wel &#39;schakelmarkeringen&#39; genoemd) om de zichtbaarheid van nieuwe functies te bepalen, zodat u de functionaliteit op gecontroleerde schaal kunt testen voordat de volledige versie wordt uitgebracht. Deze releasestrategie omvat de volgende fasen:

* **Beperkte het Testen**: Een gefaseerde versie begint met het testen door interne gebruikers van de Adobe. Het wordt dan ter beschikking gesteld aan een kleine groep klantenrekeningen om ervoor te zorgen dat de eigenschap aan klantenbehoeften en verwachtingen voldoet.

* **Begin van Uitvoer**: De Uitvoer van een gefaseerde versie begint met de Beperkte het Testen fase. De release wordt vervolgens in de loop van een paar maanden geschaald van 0% naar 100% beschikbaarheid voor klanten. De gefaseerde uitrol gebeurt op het niveau van de Organisatie van het Experience Cloud, zodat ontvangen alle gemachtigde gebruikers in een organisatie de zelfde ervaring.

* **Algemene Beschikbaarheid (GA)**: De eigenschap is beschikbaar aan 100% van de gemachtigde organisaties van de Experience Cloud, en de eigenschapversie is volledig.

Bij elke functierelease kan de tijdlijn variëren van het begin van de rollout tot GA. Het doel is om de releases kort te houden, zodat binnen twee maanden na het begin van de rollout een functie GA is.

## Functiemarkeringen

De vlaggen van de eigenschap worden gebruikt om de zichtbaarheid van nieuwe eigenschappen tijdens versie te controleren. De Adobe adviseert toevoegend `app.launchdarkly.com` aan de lijst van gewenste personen van uw firewall [ ](/help/technotes/ip-addresses.md) voor een optimale ervaring tijdens versie. Kort nadat GA is bereikt, wordt de vlag verwijderd.

U kunt uw actieve eigenschapvlaggen op elk ogenblik bekijken onder **Hulp > over Workspace > Actieve eigenschapmarkeringen**.

## Voordelen

De gefaseerde versies laten Adobe toe om het proces van de softwareplaatsing beter te schrapen en ervoor te zorgen de eigenschappen volledig worden versterkt alvorens Algemene Beschikbaarheid. Ook kunnen functies worden vrijgegeven zodra ze beschikbaar zijn, in plaats van zich aan een vast maandelijks releasevenster te houden.

## Veelgestelde vragen

| Vraag | Antwoord |
| --- | --- |
| Kan ik vroege toegang tot een eigenschap vragen? | Nee. Vroegtijdige toegang wordt niet verleend.<br> Als u de vroegere concepten van Analytics wilt testen, moedigen wij u aan om [ Labs van Adobe Analytics ](/help/analyze/labs.md) te proberen om feedback op onze industrie-leidende innovaties te verstrekken. |
| Heeft deze releasestrategie invloed op mijn toegang tot functies? | Nee. Zodra een functie GA heeft bereikt, hebt u toegang tot de functie als deze in het pakket Analytics is opgenomen.<br> u kunt details van uw pakket Analytics onder [ de Niveaus van de Toegang van de Eigenschap bekijken ](/help/admin/admin/company/feature-access-levels.md). |
