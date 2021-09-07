---
description: Verklaart de nieuwe ononderbroken strategie van de eigenschapversie voor Adobe Analytics
title: Adobe Analytics-functiereleases
exl-id: 1e403bef-4aab-4a9a-a358-62449ce801ff
source-git-commit: a9d892ab8caaeb797fbbd9b5aa136c5dab76f8bd
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 1%

---

# Adobe Analytics-functiereleases

In het verleden volgden Adobe Analytics-functiereleases een vast maandelijks schema. Vanaf april 2020 is Adobe Analytics overgestapt op een doorlopend leveringsmodel dat een meer schaalbare, gefaseerde benadering van eigenschapplaatsing toestaat.

## Releasestrategie

[!UICONTROL Analysis Workspace] maakt gebruik van functiemarkeringen (ook wel &#39;&#39;schakelingen&#39;&#39; genoemd) om de zichtbaarheid van nieuwe functies te bepalen, zodat tests op gecontroleerde schaal vóór volledige release mogelijk zijn. Deze releasestrategie omvat de volgende fasen:

* **Vrijgave voor productie (RTP)**: De code wordt vrijgegeven aan productie, met de eigenschap zicht uitgezet in Analysis Workspace. Deze functie is soms beschikbaar in de 2.0 Analytics-API.

* **Beperkte tests**: Een gefaseerde versie begint met het testen door interne gebruikers van Adobe. De release wordt vervolgens in de loop van een paar maanden geschaald van 0% naar 100% beschikbaarheid. De gefaseerde uitrol gebeurt op het niveau van de Organisatie van de Experience Cloud, zodat ontvangen alle gemachtigde gebruikers in een organisatie de zelfde ervaring.

* **Algemene beschikbaarheid (GA)**: De functie is beschikbaar voor 100% van de organisaties met bevoegdheid voor Experience Cloud en de release met functies is voltooid.

Bij elke functierelease kan de tijdlijn variëren van RTP tot GA. Het doel is om versies kort te houden, zodat binnen 2 maanden na het begin van de release (RTP) een functie GA zal zijn.

## Functiemarkeringen

De vlaggen van de eigenschap worden gebruikt om de zichtbaarheid van nieuwe eigenschappen tijdens versie te controleren. Adobe raadt aan `app.launchdarkly.com` toe te voegen aan [lijst van gewenste personen](/help/technotes/ip-addresses.md) voor een optimale ervaring tijdens de release. Kort nadat GA is bereikt, wordt de vlag verwijderd.

U kunt uw actieve eigenschapmarkeringen op elk ogenblik bekijken onder **Hulp > over Werkruimte > Actieve eigenschapmarkeringen**.

## Voordelen

Met gefaseerde releases kan Adobe het implementatieproces van de software beter schalen en ervoor zorgen dat de functies volledig zijn beveiligd voordat de algemene beschikbaarheid beschikbaar is. Ook kunnen functies worden vrijgegeven zodra ze beschikbaar zijn, in plaats van zich aan een vast maandelijks releasevenster te houden.

## Veelgestelde vragen

| Vraag | Antwoord |
| --- | --- |
| Kan ik vroege toegang tot een eigenschap vragen? | Nee. Vroegtijdige toegang wordt niet verleend.<br>Als u de concepten van de vroege Analyse wilt testen, moedigen wij u aan om te proberen  [Adobe Analytics ](/help/analyze/labs.md) Labs om feedback over onze industrie-leidende innovaties te verstrekken. |
| Heeft deze releasestrategie invloed op mijn toegang tot functies? | Nee. Zodra een functie GA heeft bereikt, hebt u toegang tot de functie als deze in het pakket Analytics is opgenomen.<br>U kunt de details van uw pakket Analytics onder de Niveaus van de Toegang van de  [Eigenschap bekijken](/help/admin/company/feature-access-levels.md). |