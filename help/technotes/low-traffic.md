---
description: Wanneer een rapport vele unieke waarden heeft, gebruikt de Adobe het laag-Verkeer afmetingspunt om rapportprestaties te verbeteren.
title: Lage verkeerswaarde in Adobe Analytics
feature: Metrics, Data Configuration and Collection
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: d3a959d128f4740fd98ff40e5b92a3ea983d3c05
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Lage verkeerswaarde in Adobe Analytics

Wanneer een rapport vele unieke waarden heeft, verstrekt de Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport verschijnen. Unieke variabelewaarden die boven een bepaalde drempel worden verzameld (zie hieronder) worden vermeld onder een dimensie-item met het label **[!UICONTROL Low-Traffic]**.

## Hoe [!UICONTROL Low-Traffic] werken

* Adobe Analytics gebruikt twee drempels om te bepalen welke unieke waarden in rapporten elke maand worden getoond: A **[!UICONTROL low threshold]** en **[!UICONTROL high threshold]**. Deze drempelwaarden kunnen van tijd tot tijd met Adobe worden aangepast. De huidige drempelwaarden zijn:
   * **[!UICONTROL Low threshold]**: >500.000 unieke waarden gedurende de maand.
   * **[!UICONTROL High threshold]**: >1.000.000 unieke waarden gedurende de maand.
* De rapportage wordt niet beïnvloed als de variabele de lage drempel in een bepaalde maand niet bereikt.
* Wanneer een variabele de lage drempel bereikt, beginnen de gegevens onder te worden ingesloten [!UICONTROL Low-Traffic]. Elke waarde boven deze drempel doorloopt de volgende logica:
   * Als er al een waarde wordt weergegeven in rapporten, voegt u deze waarde op de gebruikelijke manier toe.
   * Als een waarde nog niet in rapporten wordt gezien, wordt het aanvankelijk ingesloten in [!UICONTROL Low-Traffic] dimensie-item.
   * Als een waarde onder wordt ingesloten [!UICONTROL Low-Traffic] ontvangt een instroom van verkeer (typisch instanties in de dubbele cijfers in één enkele dag), begint het als zijn eigen afmetingspunt te worden erkend. Instanties die zijn verzameld voordat ze aan de drempelwaarde voldoen, blijven onder [!UICONTROL Low-Traffic]. Het nauwkeurige punt waarop het afmetingspunt in rapporten begint te verschijnen heeft vele gebiedsdelen, zoals het aantal servers die gegevens voor de rapportreeks verwerken en de hoeveelheid tijd tussen elke instantie van het afmetingspunt.
* Als een variabele de hoge drempel bereikt, wordt het agressievere filtreren toegepast. Unieke waarden vereisen instanties in de drievoudige cijfers op één dag alvorens als zijn eigen afmetingspunt worden erkend.

Deze logica staat Adobe toe om rapporteringsmogelijkheden te optimaliseren terwijl nog het toestaan van uw organisatie om over cruciale afmetingspunten te rapporteren die later in de maand worden verzameld. Als uw organisatie bijvoorbeeld een site met miljoenen artikelen uitvoert en een nieuw artikel populair wordt aan het einde van de maand (nadat beide unieke drempelwaarden zijn overschreden), kunt u de prestaties van dat artikel nog steeds analyseren zonder dat het onder de drempel wordt ingesloten [!UICONTROL Low-Traffic]. Deze logica is niet bedoeld om alles op te heffen dat een bepaald aantal paginaweergaven per dag of per maand krijgt.

>[!NOTE]
>De [Pagina](../components/dimensions/page.md) de dimensie gebruikt verscheidene achterste kolommen die allen aan unieke drempels tellen, met inbegrip van `pagename`, `page_url`, `first_hit_pagename`, `first_hit_page_url`, `visit_pagename`, `visit_page_url`, en `click_context`. Deze achterste kolommen kunnen [!UICONTROL Low-Traffic] logica die moet worden toegepast ruim voordat het aantal unieke pagina-elementen in Workspace de lage drempel bereikt.

Merk op dat de laag-verkeerslogica hierboven wordt beschreven het best met variabelen werkt die afmetingspunten hebben die vele tijden tijdens de maand terugkomen. Als de de afmetingspunten van een variabele bijna of volledig uniek op elke klap zijn, zal de variabele de lage drempel snel bereiken en alle nieuwe afmetingspunten voor de maand zullen omhoog in het laag-verkeersemmer eindigen.

## Unieke limietdrempels wijzigen

Drempelwaarden kunnen soms per variabele worden gewijzigd. Neem contact op met de klantenservice van de Adobe of met het accountteam van de Adobe om deze wijziging aan te vragen. De mate waarin de drempelwaarden kunnen worden verhoogd, hangt af van meerdere factoren en de Adobe kan in alle gevallen niet in staat zijn de drempelverhogingen te verwerken. Neem bij het aanvragen van een wijziging de volgende gegevens op:

* De rapportsuite-id
* De variabele waarvoor u de drempel wilt verhogen
* Zowel de eerste als de tweede gewenste drempelwaarde

Wijzigingen in drempelwaarden kunnen van invloed zijn op de prestaties van rapporten. Adobe raadt u ten zeerste aan een goede beoordeling te gebruiken wanneer u een verhoging tot unieke waarden in een variabele aanvraagt. Verhoog alleen de unieke limieten voor variabelen die essentieel zijn voor de rapportagebehoeften van uw organisatie.

Laag-verkeersdrempels zijn niet zichtbaar in Analytics UI. Neem contact op met de klantenservice van de Adobe als u meer informatie wilt over bestaande drempelwaarden.

## Laag verkeer dat componenten en andere mogelijkheden gebruikt

De verschillende mogelijkheden behandelen laag-verkeerswaarden op verschillende manieren.

* **Data Warehouse:** Er is geen limiet aan het aantal unieke waarden in rapporten over Data Warehouse. De unieke architectuur ervan maakt het mogelijk om een aantal unieke waarden te rapporteren.
   * In sommige beperkte scenario&#39;s, kunnen de laag-verkeerswaarden nog verschijnen. Voorbeelden zijn list vars, list props, merchandising Vars en de detailafmetingen van marketingkanalen.
* **Segmentatie:** Als de segmentcriteria een variabele met een hoog aantal unieke waarden omvatten, worden de waarden die onder laag verkeer worden gevangen niet inbegrepen.
* **Classificaties:** Indelingsrapporten zijn ook onderworpen aan unieke limieten. Als de waarde van de bovenliggende variabele van een classificatie wordt opgenomen onder laag verkeer, wordt de waarde niet geclassificeerd.
   * De door de importeur verkregen waarden voor de indeling in laagverkeerssituaties kunnen in Data Warehouse worden bekeken. <!-- AN-115871 -->
   * Classificatiewaarden voor laagverkeer die worden verkregen via de regelbuilder *kan* in de Data Warehouse worden weergegeven. <!-- AN-122872 -->
