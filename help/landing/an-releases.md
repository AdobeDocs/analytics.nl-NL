---
description: Verklaart de nieuwe ononderbroken eigenschaprelease strategie voor de Analytics van Adobe
title: Adobe Analytics - releasestrategie
translation-type: tm+mt
source-git-commit: 0b00405e9e27a427a85b0f4a0d970671ada4aa67
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Adobe Analytics - releasestrategie

In het verleden volgden de Adobe Analytics-functies een vast maandelijks schema. Vanaf april 2020 gaat Adobe Analytics over naar een doorlopend leveringsmodel dat een meer schaalbare, gefaseerde benadering van eigenschapplaatsing toestaat.

## Releasestrategie

[!UICONTROL Analysis Workspace] maakt gebruik van functiemarkeringen (ook wel &#39;&#39;schakelingen&#39;&#39; genoemd) om de zichtbaarheid van nieuwe functies te bepalen, zodat tests op gecontroleerde schaal vóór volledige release mogelijk zijn. Deze releasestrategie omvat de volgende fasen:

* **Vrijgave voor productie (RTP)**: De code wordt vrijgegeven aan productie, met eigenschapzicht uitgezet in de Werkruimte van de Analyse. **Opmerking**: Op dit moment is de functie mogelijk beschikbaar in de 2.0 Analytics-API.

* **Beperkte tests**: Een gefaseerde release begint met testen door interne Adobe-gebruikers. De release wordt vervolgens in de loop van een paar maanden geschaald van 0% naar 100% beschikbaarheid. De gefaseerde uitrol gebeurt op het niveau van de organisatie van de Ervaring Cloud, zodat ontvangen alle gemachtigde gebruikers in een organisatie de zelfde ervaring.

* **Algemene beschikbaarheid (GA)**: De functie is beschikbaar voor 100% van de organisaties van de Ervaring Cloud en de release met functies is voltooid.

Bij elke functierelease kan de tijdlijn variëren van RTP tot GA. Het doel is om versies kort te houden, zodat binnen 2 maanden na het begin van de release (RTP) een functie GA zal zijn.

## Voordelen

Met gefaseerde releases kan Adobe het implementatieproces van de software beter schalen en ervoor zorgen dat de functies volledig zijn verbeterd voordat algemene beschikbaarheid beschikbaar is. Ook kunnen functies worden vrijgegeven zodra ze beschikbaar zijn, in plaats van zich aan een vast maandelijks releasevenster te houden.

## Veelgestelde vragen

| Vraag | Antwoord |
|---|---|
| Kan ik vroege toegang tot een eigenschap vragen? | Nee. Vroegtijdige toegang wordt niet verleend.<br>Als u de concepten voor vroegtijdige analyse wilt testen, raden we u aan om te proberen [Adobe Analytics Labs](https://docs.adobe.com/content/help/en/analytics/analyze/tech-previews/overview.html) feedback te geven over onze toonaangevende innovaties. |
| Heeft deze releasestrategie invloed op mijn toegang tot functies? | Nee. Zodra een functie GA heeft bereikt, hebt u toegang tot de functie als deze in het pakket Analytics is opgenomen.<br>U kunt de details van uw Analytics-pakket weergeven onder [!UICONTROL Admin] > [!UICONTROL Company Settings] > [Functietoegangsniveaus](https://docs.adobe.com/content/help/en/analytics/admin/company-settings/feature-access-levels.html). |