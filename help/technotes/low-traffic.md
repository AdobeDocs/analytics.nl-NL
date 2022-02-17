---
description: Wanneer een rapport een groot aantal unieke waarden heeft, verstrekt Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport verschijnen.
title: Lage verkeerswaarde in Adobe Analytics
feature: Data Configuration and Collection
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Lage verkeerswaarde in Adobe Analytics

Wanneer een rapport vele unieke waarden heeft, verstrekt Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport verschijnen. Unieke variabelewaarden die na ongeveer 500.000 bestaande waarden worden verzameld, worden vermeld onder een regelitem met de naam **[!UICONTROL Low-Traffic]**.

## Hoe [!UICONTROL Low-Traffic] werken

* De rapportage wordt niet beïnvloed als de variabele in een bepaalde maand niet 500.000 unieke waarden bereikt.
* Wanneer een variabele deze eerste drempel van 500.000 bereikt, beginnen de gegevens onder laag-verkeer te worden ingesloten. Elke waarde boven deze drempel doorloopt de volgende logica:
   * Als er al een waarde wordt weergegeven in rapporten, voegt u deze waarde op de gebruikelijke manier toe.
   * Als er nog geen waarde wordt weergegeven in rapporten, wordt deze weergegeven in het dialoogvenster [!UICONTROL Low-Traffic] regelitem. Als een waarde is opgenomen in de [!UICONTROL Low-Traffic] line item wordt binnen een korte tijd gezien als een significant aantal keren, en wordt opgenomen als een eigen lijstitem. Het significante aantal tijden dat een punt moet worden gezien heeft vele gebiedsdelen, zoals het aantal verwerkingsservers en daemons die gegevens voor die bepaalde rapportreeks verwerken.
* Als een rapportreeks meer dan 1.000.000 unieke waarden bereikt, wordt het agressievere filtreren toegepast:
   * Als er al een waarde wordt weergegeven in rapporten, voegt u deze waarde op de gebruikelijke manier toe.
   * Als er nog geen waarde wordt weergegeven in rapporten, wordt deze weergegeven in het dialoogvenster [!UICONTROL Low-Traffic] regelitem. Als een waarde is opgenomen in de [!UICONTROL Low-Traffic] line item wordt binnen een korte tijd gezien als een significant aantal keren, en wordt opgenomen als een eigen lijstitem. Het significante aantal tijden dat een punt moet worden gezien heeft vele gebiedsdelen, zoals het aantal verwerkingsservers en daemons die gegevens voor die bepaalde rapportreeks verwerken.

Waarom verplaatst Adobe een item van de [!UICONTROL Low Traffic] lijstitem naar eigen lijstitem? Deze verplaatsing herkent bijvoorbeeld een populaire nieuwe pagina of een nieuw item dat later in de maand is toegevoegd (nadat de unieke waarden zijn overschreden) en dat veel resultaten/weergaven oplevert. De verplaatsing is niet bedoeld om alles af te vangen wat een bepaald aantal hits/weergaven per dag of per maand oplevert.

>[!NOTE]
>De opzoektelling van de pagina bevat niet alleen waarden voor de [!UICONTROL pagename]/[!UICONTROL page_url]. De opzoektabel van de pagina bevat meerdere kolommen/velden, zoals [!UICONTROL pagename], [!UICONTROL first_hit_pagename]/[!UICONTROL page_url], [!UICONTROL visit_pagename]/[!UICONTROL page_url]en de klikcontext (de oude gegevens Clickmap).

## Unieke limietdrempels wijzigen

Drempelwaarden zijn standaard 500.000 en 1 miljoen unieke waarden. Deze grenswaarden kunnen per variabele worden gewijzigd. Neem contact op met de accountmanager van uw organisatie om deze wijziging aan te vragen. Neem bij het aanvragen van een wijziging de volgende gegevens op:

* De rapportsuite-id
* De variabele waarvoor u de drempel wilt verhogen
* Zowel de eerste als de tweede gewenste drempel

Wijzigingen in drempelwaarden kunnen van invloed zijn op de prestaties van rapporten. Adobe raadt u ten zeerste aan een goede beoordeling te gebruiken wanneer u een verhoging tot unieke waarden in een variabele aanvraagt.

Laag-verkeersdrempels zijn niet zichtbaar in Analytics UI. Neem contact op met de klantenservice van Adobe als u meer informatie wilt over bestaande drempelwaarden.

## Laag verkeer dat componenten en andere mogelijkheden gebruikt

De verschillende mogelijkheden behandelen laag-verkeerswaarden op verschillende manieren.

* **Data Warehouse:** Er is geen limiet aan het aantal unieke waarden in rapporten over Data Warehouse. De unieke architectuur ervan maakt het mogelijk om een aantal unieke waarden te rapporteren.
   * In sommige beperkte scenario&#39;s, kunnen de laag-verkeerswaarden nog verschijnen. Voorbeelden zijn list vars, list props, merchandising Vars en de detailafmetingen van marketingkanalen.
* **Segmentatie:** Als de segmentcriteria een variabele met een hoog aantal unieke waarden omvatten, worden de waarden die onder laag verkeer worden gevangen niet inbegrepen.
* **Classificaties:** Indelingsrapporten zijn ook onderworpen aan unieke limieten. Als de waarde van de bovenliggende variabele van een classificatie wordt opgenomen onder laag verkeer, wordt de waarde niet geclassificeerd.
   * De door de importeur verkregen waarden voor de indeling in laagverkeerssituaties kunnen in Data Warehouse worden bekeken. <!-- AN-115871 -->
   * Classificatiewaarden voor laagverkeer die worden verkregen via de regelbuilder *kan* in de Data Warehouse worden weergegeven. <!-- AN-122872 -->
