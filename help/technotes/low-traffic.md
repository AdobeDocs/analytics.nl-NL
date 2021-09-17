---
description: Wanneer een rapport een groot aantal unieke waarden heeft, verstrekt Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport verschijnen.
title: Lage verkeerswaarde in Adobe Analytics
feature: Metrics
uuid: 56f723f8-94e8-478f-8ea3-16dad21dfa1f
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: 7036c6d3bc15c2cb7bd62af79229052cd772f8f8
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Lage verkeerswaarde in Adobe Analytics

Wanneer een rapport vele unieke waarden heeft, verstrekt Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport verschijnen. Unieke variabelewaarden die worden verzameld na ongeveer 500.000 bestaande waarden worden vermeld onder een regelitem met de naam **[!UICONTROL Low-Traffic]**.

## Hoe werkt [!UICONTROL Low-Traffic]

* De rapportage wordt niet beïnvloed als de variabele in een bepaalde maand niet 500.000 unieke waarden bereikt.
* Wanneer een variabele deze eerste drempel van 500.000 bereikt, beginnen de gegevens onder laag-verkeer te worden ingesloten. Elke waarde boven deze drempel doorloopt de volgende logica:
   * Als er al een waarde wordt weergegeven in rapporten, voegt u deze waarde op de gebruikelijke manier toe.
   * Als een waarde nog niet in rapporten wordt gezien, zal het in [!UICONTROL Low-Traffic] lijnpunt verschijnen. Als een waarde die in het [!UICONTROL Low-Traffic] lijnpunt is inbegrepen een significant aantal tijden binnen een korte tijd wordt gezien, zal het beginnen als zijn eigen lijnpunt te worden erkend. Het significante aantal tijden dat een punt moet worden gezien heeft vele gebiedsdelen, zoals het aantal verwerkingsservers en daemons die gegevens voor die bepaalde rapportreeks verwerken.
* Als een rapportreeks meer dan 1.000.000 unieke waarden bereikt, wordt het agressievere filtreren toegepast:
   * Als er al een waarde wordt weergegeven in rapporten, voegt u deze waarde op de gebruikelijke manier toe.
   * Als een waarde nog niet in rapporten wordt gezien, zal het in [!UICONTROL Low-Traffic] lijnpunt verschijnen. Als een waarde die in het [!UICONTROL Low-Traffic] lijnpunt is inbegrepen een significant aantal tijden binnen een korte tijd wordt gezien, zal het beginnen als zijn eigen lijnpunt te worden erkend. Het significante aantal tijden dat een punt moet worden gezien heeft vele gebiedsdelen, zoals het aantal verwerkingsservers en daemons die gegevens voor die bepaalde rapportreeks verwerken.

Waarom verplaatst Adobe een punt van [!UICONTROL Low Traffic] lijnpunt aan zijn eigen lijnpunt? Deze verplaatsing herkent bijvoorbeeld een populaire nieuwe pagina of een nieuw item dat later in de maand is toegevoegd (nadat de unieke waarden zijn overschreden) en dat veel resultaten/weergaven oplevert. De verplaatsing is niet bedoeld om alles af te vangen wat een bepaald aantal hits/weergaven per dag of per maand oplevert.

>[!NOTE]
>De opzoektelling van de pagina omvat niet alleen waarden voor [!UICONTROL pagename]/[!UICONTROL page_url]. De pagina raadpleginglijst omvat verscheidene kolommen/gebieden zoals [!UICONTROL pagename], [!UICONTROL first_hit_pagename]/[!UICONTROL page_url], [!UICONTROL visit_pagename]/[!UICONTROL page_url], en de klikcontext (de oude gegevens van Clickmap).

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
