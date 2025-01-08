---
description: Wanneer een rapport vele unieke waarden heeft, gebruikt de Adobe het laag-Verkeer afmetingspunt om rapportprestaties te verbeteren.
title: Lage verkeerswaarde in Adobe Analytics
feature: Metrics, Data Configuration and Collection
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: f242ec6613cf046224f76f7edc7813a34c65fff8
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Lage verkeerswaarde in Adobe Analytics

Wanneer een rapport vele unieke waarden heeft, verstrekt de Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport verschijnen. Unieke variabelewaarden die boven een bepaalde drempel worden verzameld (zie hieronder), worden vermeld onder een dimensie-item met het label **[!UICONTROL Low-Traffic]** .

## Hoe [!UICONTROL Low-Traffic] werkt

* Adobe Analytics gebruikt twee drempelwaarden om te bepalen welke unieke waarden elke maand in rapporten worden weergegeven: A **[!UICONTROL low threshold]** en a **[!UICONTROL high threshold]** . Deze drempels kunnen van tijd tot tijd door Adobe worden aangepast. De huidige drempelwaarden zijn:
   * **[!UICONTROL Low threshold]**: 2.000.000 unieke waarden gedurende de maand.
   * **[!UICONTROL High threshold]**: 2.100.000 unieke waarden gedurende de maand.
* De rapportage wordt niet beïnvloed als een variabele de lage drempel in een bepaalde maand niet bereikt.
* Wanneer een variabele de lage drempel bereikt, beginnen de gegevens onder een afmetingspunt worden ingebed geëtiketteerd [!UICONTROL Low-Traffic]. Elke waarde boven deze drempel doorloopt de volgende logica:
   * Als er al een waarde wordt weergegeven in rapporten, voegt u deze waarde op de gebruikelijke manier toe.
   * Als er nog geen waarde wordt weergegeven in rapporten, voegt u deze eerst toe aan het item voor de [!UICONTROL Low-Traffic] dimensie.
   * Als een waarde die onder [!UICONTROL Low-Traffic] wordt geknipt een stroom van verkeer ontvangt (typisch instanties in de dubbele cijfers in één enkele dag), herkent het als zijn eigen afmetingspunt. Instanties die zijn verzameld vóór de instroom van verkeer blijven onder [!UICONTROL Low-Traffic] . Het nauwkeurige punt waarop het afmetingspunt in rapporten begint te verschijnen heeft vele gebiedsdelen, zoals het aantal servers die gegevens voor de rapportreeks verwerken en de hoeveelheid tijd tussen elke instantie van het afmetingspunt.
* Als een variabele de hoge drempel bereikt, wordt het agressievere filtreren toegepast. Unieke waarden vereisen instanties in de drievoudige cijfers op één dag alvorens als zijn eigen afmetingspunt worden erkend.

Deze logica staat Adobe toe om rapporteringsmogelijkheden te optimaliseren terwijl nog het toestaan van uw organisatie om over cruciale afmetingspunten te rapporteren die later in de maand worden verzameld. Als uw organisatie bijvoorbeeld een site met miljoenen artikelen uitvoert en een nieuw artikel populair wordt aan het einde van de maand (nadat beide unieke drempelwaarden zijn overschreden), kunt u de prestaties van dat artikel nog steeds analyseren zonder dat het onder [!UICONTROL Low-Traffic] wordt gebundeld. Deze logica is niet bedoeld om alles op te heffen dat een bepaald aantal paginaweergaven per dag of per maand krijgt.

>[!NOTE]
>De [ dimensie van de Pagina ](../components/dimensions/page.md) gebruikt verscheidene achterste kolommen die allen naar unieke drempels, met inbegrip van `pagename` tellen, `page_url`, `first_hit_pagename`, `first_hit_page_url`, `visit_pagename`, `visit_page_url`, en `click_context`. Deze achterste kolommen kunnen [!UICONTROL Low-Traffic] logica veroorzaken om toe te passen ruim alvorens het aantal unieke pagina afmetingspunten in Workspace de lage drempel bereikt.

Merk op dat de laag-verkeerslogica het best met variabelen werkt die afmetingspunten hebben die vele tijden tijdens de maand terugkomen. Als de de afmetingspunten van een variabele bijna of volledig uniek op elke klap zijn, bereikt het aantal unieke waarden van de variabele zowel drempels snel als alle verdere afmetingspunten voor de maand omhoog in het laag-verkeersemmer beëindigen.

## Unieke limietdrempels wijzigen

Drempelwaarden kunnen soms per variabele worden gewijzigd. Neem contact op met de klantenservice van de Adobe of met het accountteam van de Adobe om deze wijziging aan te vragen. De mate waarin de drempelwaarden kunnen worden verhoogd, hangt af van meerdere factoren en de Adobe kan in niet alle gevallen rekening houden met de drempelverhogingen. Neem bij het aanvragen van een wijziging de volgende gegevens op:

* De rapportsuite-id
* De variabele waarvoor u de drempel wilt verhogen
* Zowel de eerste als de tweede gewenste drempelwaarde

Wijzigingen in drempelwaarden kunnen van invloed zijn op de prestaties van rapporten. Adobe raadt u ten zeerste aan een goede beoordeling te gebruiken wanneer u een verhoging tot unieke waarden in een variabele aanvraagt. Verhoog alleen de unieke limieten voor variabelen die essentieel zijn voor de rapportagebehoeften van uw organisatie.

Laag-verkeersdrempels zijn niet zichtbaar in Analytics UI. Neem contact op met de klantenservice van de Adobe als u meer informatie wilt over bestaande drempelwaarden.

## Laag verkeer dat componenten en andere mogelijkheden gebruikt

De verschillende mogelijkheden behandelen laag-verkeerswaarden op verschillende manieren.

* **Data Warehouse:** Er is geen grens aan het aantal unieke waarden in de rapporten van de Data Warehouse. De unieke architectuur ervan maakt het mogelijk om een aantal unieke waarden te rapporteren.
   * In sommige beperkte scenario&#39;s, kunnen de laag-verkeerswaarden nog verschijnen. Voorbeelden zijn list vars, list props, merchandising Vars en de detailafmetingen van marketingkanalen.
* **Segmentatie:** als de segmentcriteria een variabele met een hoog aantal unieke waarden omvat, zijn de waarden die onder laag-verkeer worden gevangen niet inbegrepen.
* **Classificaties:** de rapporten van de Classificatie zijn ook onderworpen aan unieke grenzen. Als de waarde van de bovenliggende variabele van een classificatie wordt opgenomen onder laag verkeer, wordt de waarde niet geclassificeerd.
   * De door de importeur verkregen waarden voor de indeling in laagverkeerssituaties kunnen in Data Warehouse worden bekeken. <!-- AN-115871 -->
   * De waarden van de laag-verkeersclassificatie die door de regelbouwer *worden verkregen kunnen* niet in Data Warehouse worden bekeken. <!-- AN-122872 -->
