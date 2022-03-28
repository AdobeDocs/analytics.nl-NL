---
description: Wanneer een rapport vele unieke waarden heeft, gebruikt Adobe het laag-Verkeer afmetingspunt om rapportprestaties te verbeteren.
title: Lage verkeerswaarde in Adobe Analytics
feature: Data Configuration and Collection
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: ddd1473ccfe27dbcb28c0c51992628c9bf03cb5c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Lage verkeerswaarde in Adobe Analytics

Wanneer een rapport vele unieke waarden heeft, verstrekt Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport verschijnen. Unieke variabelewaarden die worden verzameld na ongeveer 500.000 bestaande waarden worden vermeld onder een dimensie-item met het label **[!UICONTROL Low-Traffic]**.

## Hoe [!UICONTROL Low-Traffic] werken

* De rapportage wordt niet beïnvloed als de variabele in een bepaalde maand niet 500.000 unieke waarden bereikt.
* Wanneer een variabele 500.000 unieke waarden bereikt, worden de gegevens ingesloten onder [!UICONTROL Low-Traffic]. Elke waarde boven deze drempel doorloopt de volgende logica:
   * Als er al een waarde wordt weergegeven in rapporten, voegt u deze waarde op de gebruikelijke manier toe.
   * Als een waarde nog niet in rapporten wordt gezien, wordt het aanvankelijk ingesloten in [!UICONTROL Low-Traffic] dimensie-item.
   * Als een waarde onder wordt ingesloten [!UICONTROL Low-Traffic] ontvangt een instroom van verkeer (typisch instanties in de dubbele cijfers in één enkele dag), begint het als zijn eigen afmetingspunt te worden erkend. Instanties die zijn verzameld voordat ze aan de drempelwaarde voldoen, blijven onder [!UICONTROL Low-Traffic]. De nauwkeurige drempel heeft vele gebiedsdelen, zoals het aantal servers die gegevens voor de rapportreeks verwerken en de hoeveelheid tijd tussen elke instantie van het afmetingspunt.
* Als een rapportreeks meer dan 1.000.000 unieke waarden bereikt, wordt het agressievere filtreren toegepast. Unieke waarden vereisen instanties in de drievoudige cijfers op één dag alvorens als zijn eigen afmetingspunt worden erkend.

Deze logica staat Adobe toe om rapporteringsmogelijkheden te optimaliseren terwijl nog het toestaan van uw organisatie om over cruciale afmetingspunten te rapporteren die later in de maand worden verzameld. Uw organisatie voert bijvoorbeeld een site uit met miljoenen artikelen en een nieuw artikel werd populair aan het einde van de maand (nadat beide unieke drempels zijn overschreden). U kunt de prestaties van dat artikel nog steeds analyseren zonder dat het onder [!UICONTROL Low-Traffic]. Deze logica is niet bedoeld om alles op te heffen dat een bepaald aantal paginaweergaven per dag of per maand krijgt.

>[!NOTE]
>De [Pagina](../components/dimensions/page.md) de dimensie gebruikt verscheidene achterste kolommen die allen aan unieke drempels tellen, met inbegrip van `pagename`, `page_url`, `first_hit_pagename`, `first_hit_page_url`, `visit_pagename`, `visit_page_url`, en `click_context`. Deze achterste kolommen kunnen [!UICONTROL Low-Traffic] logica die moet worden toegepast ruim voordat het aantal unieke pagina-afmetingsitems in Workspace 500.000 bereikt.

## Unieke limietdrempels wijzigen

Drempelwaarden zijn standaard 500.000 en 1 miljoen unieke waarden. Deze grenswaarden kunnen per variabele worden gewijzigd. Neem contact op met de klantenservice van Adobe of de accountmanager van uw organisatie om deze wijziging aan te vragen. Neem bij het aanvragen van een wijziging de volgende gegevens op:

* De rapportsuite-id
* De variabele waarvoor u de drempel wilt verhogen
* Zowel de eerste als de tweede gewenste drempel

Wijzigingen in drempelwaarden kunnen van invloed zijn op de prestaties van rapporten. Adobe raadt u ten zeerste aan een goede beoordeling te gebruiken wanneer u een verhoging tot unieke waarden in een variabele aanvraagt. Verhoog alleen de unieke limieten voor variabelen die essentieel zijn voor de rapportagebehoeften van uw organisatie.

Laag-verkeersdrempels zijn niet zichtbaar in Analytics UI. Neem contact op met de klantenservice van Adobe als u meer informatie wilt over bestaande drempelwaarden.

## Laag verkeer dat componenten en andere mogelijkheden gebruikt

De verschillende mogelijkheden behandelen laag-verkeerswaarden op verschillende manieren.

* **Data Warehouse:** Er is geen limiet aan het aantal unieke waarden in rapporten over Data Warehouse. De unieke architectuur ervan maakt het mogelijk om een aantal unieke waarden te rapporteren.
   * In sommige beperkte scenario&#39;s, kunnen de laag-verkeerswaarden nog verschijnen. Voorbeelden zijn list vars, list props, merchandising Vars en de detailafmetingen van marketingkanalen.
* **Segmentatie:** Als de segmentcriteria een variabele met een hoog aantal unieke waarden omvatten, worden de waarden die onder laag verkeer worden gevangen niet inbegrepen.
* **Classificaties:** Indelingsrapporten zijn ook onderworpen aan unieke limieten. Als de waarde van de bovenliggende variabele van een classificatie wordt opgenomen onder laag verkeer, wordt de waarde niet geclassificeerd.
   * De door de importeur verkregen waarden voor de indeling in laagverkeerssituaties kunnen in Data Warehouse worden bekeken. <!-- AN-115871 -->
   * Classificatiewaarden voor laagverkeer die worden verkregen via de regelbuilder *kan* in de Data Warehouse worden weergegeven. <!-- AN-122872 -->
