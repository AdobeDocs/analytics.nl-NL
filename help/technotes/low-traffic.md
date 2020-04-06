---
description: Wanneer een rapport een groot aantal unieke waarden bevat, biedt Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport worden weergegeven.
title: Waarde voor laag verkeer in Adobe Analytics
topic: Metrics
uuid: 56f723f8-94e8-478f-8ea3-16dad21dfa1f
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Waarde voor laag verkeer in Adobe Analytics

Wanneer een rapport een groot aantal unieke waarden bevat, biedt Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport worden weergegeven. Unieke variabelewaarden die worden verzameld na ongeveer 500.000 bestaande waarden worden vermeld onder een regelitem met de naam **(Low-Traffic)**.

## Hoe het lage verkeer werkt

* De rapportage wordt niet beïnvloed als de variabele in een bepaalde maand niet 500.000 unieke waarden bereikt.
* Wanneer een variabele deze eerste drempel van 500.000 bereikt, beginnen de gegevens onder laag-verkeer te worden ingesloten. Elke waarde boven deze drempel doorloopt de volgende logica:
   * Als er al een waarde in rapporten staat, voegt u deze waarde op de gebruikelijke wijze toe.
   * Als er nog geen waarde wordt gerapporteerd, controleert u of die waarde vandaag meer dan ongeveer tien keer is waargenomen. Als dit het geval is, voegt u deze waarde toe aan de rapportage. Als het niet meer dan tien keer is geteld, laat het onder laag verkeer.
* Als een rapportreeks meer dan 1.000.000 unieke waarden bereikt, wordt het agressievere filtreren toegepast:
   * Als er al een waarde in rapporten staat, voegt u deze waarde op de gebruikelijke wijze toe.
   * Als er nog geen waarde wordt gerapporteerd, controleert u of die waarde vandaag meer dan ongeveer 100 keer is waargenomen. Als dit het geval is, voegt u de waarde toe aan de rapportage. Als dat niet het geval is, laat het dan onder laag verkeer.

>[!NOTE] Als een veranderlijke waarde genoeg verkeer ontvangt om het laag-verkeersemmer te verlaten, bewegen de eerste verzamelde waarden zich niet naar zijn respectieve lijnpunt. Die eerste 10-100 gevallen blijven onder laag verkeer.

## Unieke limietdrempels wijzigen

Drempelwaarden zijn standaard 500.000 en 1 miljoen unieke waarden. Deze grenswaarden kunnen per variabele worden gewijzigd. Neem contact op met de accountmanager van uw organisatie om deze wijziging aan te vragen. Neem bij het aanvragen van een wijziging de volgende gegevens op:

* De rapportsuite-id
* De variabele waarvoor u de drempel wilt verhogen
* Zowel de eerste als de tweede gewenste drempel

Wijzigingen in drempelwaarden kunnen van invloed zijn op de prestaties van rapporten. Adobe raadt u ten zeerste aan een goede beoordeling te gebruiken wanneer u een verhoging tot unieke waarden in een variabele aanvraagt.

Laag-verkeersdrempels zijn niet zichtbaar in Analytics UI. Neem contact op met de klantenservice van Adobe als u meer informatie wilt over bestaande drempelwaarden.

## Laag verkeer dat componenten en andere mogelijkheden gebruikt

De verschillende mogelijkheden behandelen laag-verkeerswaarden op verschillende manieren.

* **Data Warehouse:** Er is geen limiet aan het aantal unieke waarden in Data Warehouse-rapporten. De unieke architectuur ervan maakt het mogelijk om een aantal unieke waarden te rapporteren.
   * In sommige beperkte scenario&#39;s, kunnen de laag-verkeerswaarden nog verschijnen. Voorbeelden zijn list vars, list props, merchandising Vars en de detailafmetingen van marketingkanalen.
* **Segmentatie:** Als de segmentcriteria een variabele met een hoog aantal unieke waarden omvatten, worden de waarden die onder laag verkeer worden gevangen niet inbegrepen.
* **Classificaties:** Indelingsrapporten zijn ook onderworpen aan unieke limieten. Als de waarde van de bovenliggende variabele van een classificatie wordt opgenomen onder laag verkeer, wordt de waarde niet geclassificeerd.
   * Als u waarden classificeert voordat ze in gegevens worden gezien, tellen die waarden mee voor de unieke drempel voor die maand.
