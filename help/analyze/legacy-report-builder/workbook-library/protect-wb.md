---
description: Leer hoe te om alle verzoeken in een werkboek tegen het toevoegen van en het uitgeven van verzoeken te beschermen door het werkboek te sluiten.
title: Werkboeken vergrendelen en ontgrendelen
uuid: ef5c276c-5f74-4741-b6fa-4c79eda29f62
feature: Report Builder
role: User, Admin
exl-id: b5a83532-9fa7-4f1f-b744-e5d74781fffb
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Werkboeken vergrendelen en ontgrendelen

{{legacy-arb}}

U kunt alle verzoeken in een werkboek tegen het toevoegen van en het uitgeven van verzoeken beschermen door het werkboek te sluiten. Dit laat off-line het uitgeven van werkboeken toe door alle rapportverzoeken voor efficiënter het uitgeven te pauzeren.

Als analist, laat het sluiten van een werkboek u uw werkboekverzoeken tegen het knoeien door andere gebruikers binnen uw organisatie beschermen. Tezelfdertijd, kunnen die gebruikers nog de verzoeken in het werkboek verfrissen.

Als u een werkboek wilt beschermen tegen bewerken, klikt u op **[!UICONTROL Locked]** op de werkbalk Report Builder ( ![](assets/locked_icon.png) ).

Als u de beveiliging van een werkboek wilt opheffen, klikt u op **[!UICONTROL Unlocked]** ( ![](assets/unlocked_icon.png) ).

U kunt een gesloten werkboek ontgrendelen als u één van de volgende toestemmingen hebt:

* U bent een beheerder, of
* U bent de persoon die aanvankelijk het werkboek gesloten. In dit geval hoeft u geen beheerder te zijn.

>[!NOTE]
>
>U kunt geen verzoek aan een beschermd werkboek toevoegen tenzij u de toestemmingen hebt om het werkboek te ontgrendelen.

Wanneer een werkboek tegen verzoek het uitgeven wordt gesloten,

* Gebruikers kunnen geen aanvragen maken en toevoegen.
* Gebruikers kunnen aanvragen niet bewerken via de wizard Verzoek.
* Gebruikers kunnen aanvragen niet bewerken via de functie Meerdere aanvragen bewerken.
* Gebruikers kunnen aanvragen niet knippen, kopiëren of plakken. Gebruikers kunnen echter wel het contextmenu van Excel Knippen/Kopiëren/Plakken gebruiken om de inhoud van de aanvraag(en) te knippen, te kopiëren of te plakken.
* Gebruikers kunnen aanvragen afzonderlijk of als onderdeel van een groep vernieuwen.
* Als in de aanvraag invoerwaarden uit cellen worden gebruikt (datumbereik, segment, filters), kunnen gebruikers deze waarden in de cellen wijzigen en zo indirect de aanvragen bewerken door ze te vernieuwen.

Als u een beveiligd werkboek probeert te bewerken via het contextmenu of **[!UICONTROL Request Manager]** of **[!UICONTROL Edit Multiple Requests]** , is het mogelijk dat u dit doet of niet:

* Als u geen toestemmingen hebt om een verzoek te ontgrendelen, zult u een bericht zien erop wijst dat u niet de rechten hebt om het werkboek te ontgrendelen en uit te geven.

  ![ Schermafbeelding die het foutenbericht toont wanneer u geen toestemmingen hebt om een verzoek te ontgrendelen.](assets/locked_workbook_error.png)

## Workflow {#section_260D05FF632B41DB97DB43E2ADBE2E75}

Laten wij veronderstellen werkboek A één verzoek heeft dat in een gesloten staat is en door Gebruiker A gecreeerd.

**Voorbeeld 1: Admin gebruiker (of Gebruiker A)**

1. De gebruiker registreert in Report Builder en opent werkboek A.
1. Werkboek A is momenteel vergrendeld, dus de knop Verzoek maken wordt gedeactiveerd in de werkbalk, samen met alle andere knoppen waarvan de functionaliteit is uitgeschakeld door vergrendeling.
1. Als de gebruiker probeert om één van de gedeactiveerde knopen te gebruiken, lijkt een bericht dat het werkboek momenteel gesloten is.
1. De gebruiker kan het werkboek ontgrendelen, dat volledige het uitgeven functionaliteit toelaat.
1. Na het ontgrendelen blijft het werkboek ontgrendeld tot het expliciet opnieuw is vergrendeld.

**Voorbeeld 2: Niet-Admin gebruiker (Gebruiker B)**

1. De gebruiker registreert in Report Builder en opent werkboek A.
1. Gebruiker kan de aanvraag niet toevoegen/bewerken.
1. De gebruiker kan het werkboek niet ontgrendelen.
