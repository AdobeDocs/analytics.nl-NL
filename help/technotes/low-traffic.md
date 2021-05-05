---
description: Wanneer een rapport een groot aantal unieke waarden heeft, verstrekt Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport verschijnen.
title: Lage verkeerswaarde in Adobe Analytics
feature: Metrics
uuid: 56f723f8-94e8-478f-8ea3-16dad21dfa1f
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
translation-type: tm+mt
source-git-commit: 482dcc04b7d68c6a555d318d8493c309e5899ae1
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Lage verkeerswaarde in Adobe Analytics

Wanneer een rapport vele unieke waarden heeft, verstrekt Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport verschijnen. Unieke variabelewaarden die worden verzameld na ongeveer 500.000 bestaande waarden worden vermeld onder een regelitem met de naam **(Low-Traffic)**.

## Hoe het lage verkeer werkt

* De rapportage wordt niet beïnvloed als de variabele in een bepaalde maand niet 500.000 unieke waarden bereikt.
* Wanneer een variabele deze eerste drempel van 500.000 bereikt, beginnen de gegevens onder laag-verkeer te worden ingesloten. Elke waarde boven deze drempel doorloopt de volgende logica:
   * Als er al een waarde in rapporten staat, voegt u deze waarde op de gebruikelijke wijze toe.
   * Als een waarde nog niet in rapportering is, zijn de &quot;aantal waarden gezien&quot;drempels afhankelijk van achtergrondconfiguraties. Ze vormen geen precieze &quot;10&quot; of &quot;100&quot; keer.
* Als een rapportreeks meer dan 1.000.000 unieke waarden bereikt, wordt het agressievere filtreren toegepast:
   * Als er al een waarde in rapporten staat, voegt u deze waarde op de gebruikelijke wijze toe.
   * Als een waarde nog niet in rapportering is, zijn de &quot;aantal waarden gezien&quot;drempels afhankelijk van achtergrondconfiguraties. Ze vormen geen precieze &quot;10&quot; of &quot;100&quot; keer.

>[!NOTE]
>
>Als een veranderlijke waarde genoeg verkeer ontvangt om het laag-verkeersemmer te verlaten, bewegen de eerste verzamelde waarden zich niet naar zijn respectieve lijnpunt. Die eerste 10-100 gevallen blijven onder laag verkeer.

## Unieke limietdrempels wijzigen

Drempelwaarden zijn standaard 500.000 en 1 miljoen unieke waarden. Deze grenswaarden kunnen per variabele worden gewijzigd. Neem contact op met de accountmanager van uw organisatie om deze wijziging aan te vragen. Neem bij het aanvragen van een wijziging de volgende gegevens op:

* De rapportsuite-id
* De variabele waarvoor u de drempel wilt verhogen
* Zowel de eerste als de tweede gewenste drempel

Wijzigingen in drempelwaarden kunnen van invloed zijn op de prestaties van rapporten. Adobe raadt u ten zeerste aan een goede beoordeling te gebruiken wanneer u een verhoging tot unieke waarden in een variabele aanvraagt.

Laag-verkeersdrempels zijn niet zichtbaar in Analytics UI. Neem contact op met de klantenservice van Adobe als u meer informatie wilt over bestaande drempelwaarden.

## Laag verkeer dat componenten en andere mogelijkheden gebruikt

De verschillende mogelijkheden behandelen laag-verkeerswaarden op verschillende manieren.

* **Data Warehouse:** Er is geen limiet aan het aantal unieke waarden in rapporten van de Data Warehouse. De unieke architectuur ervan maakt het mogelijk om een aantal unieke waarden te rapporteren.
   * In sommige beperkte scenario&#39;s, kunnen de laag-verkeerswaarden nog verschijnen. Voorbeelden zijn list vars, list props, merchandising Vars en de detailafmetingen van marketingkanalen.
* **Segmentatie:** Als de segmentcriteria een variabele met een hoog aantal unieke waarden omvatten, worden de waarden die onder laag verkeer worden gevangen niet inbegrepen.
* **classificaties:** classificatierapporten zijn ook onderworpen aan unieke limieten. Als de waarde van de bovenliggende variabele van een classificatie wordt opgenomen onder laag verkeer, wordt de waarde niet geclassificeerd.
   * De door de importeur verkregen waarden voor de indeling in laagverkeerssituaties kunnen in Data Warehouse worden bekeken. <!-- AN-115871 -->
   * De waarden van de laag-verkeersclassificatie die door de regelbouwer *worden verkregen kunnen* niet in Data Warehouse worden bekeken. <!-- AN-122872 -->
