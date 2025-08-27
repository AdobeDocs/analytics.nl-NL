---
description: Wanneer een rapport vele unieke waarden heeft, gebruikt Adobe het de afmetingspunt van het Laag-Verkeer om rapportprestaties te verbeteren.
title: Lage verkeerswaarde in Adobe Analytics
feature: Metrics, Data Configuration and Collection
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: 42d044c3c56f13a232b721ef60f64bcf622ffa9f
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# [!UICONTROL Low-Traffic] -waarde in Adobe Analytics

Wanneer een dimensie miljoenen unieke waarden bevat, verstrekt Adobe functionaliteit om ervoor te zorgen dat de belangrijkste waarden in uw rapport op geschikte wijze verschijnen. Unieke waarden die boven een bepaalde drempel worden verzameld, worden weergegeven onder een dimensie-item met het label **[!UICONTROL Low-Traffic]** .

Met het item [!UICONTROL Low-Traffic] Dimensie kan Adobe ervoor zorgen dat rapporten tijdig worden geretourneerd door buitensporige unieke waarden te nemen en samen te voegen.

Merk op dat [!UICONTROL Low-traffic] logica het best met afmetingen werkt die punten hebben die vele tijden tijdens de maand terugkomen. Als dimensie-items bijna of volledig uniek zijn op elke hit, bereikt het aantal unieke waarden snel de drempel en komen alle volgende waarden voor de maand in het [!UICONTROL Low-Traffic] emmertje te staan.

## Invoeren van waarden [!UICONTROL Low-Traffic]

Door gebrek, wordt een drempel van **2.000.000 unieke waarden** geplaatst per afmeting, per rapportreeks, per kalendermaand. Dimension-items die deze unieke waardedrempel overschrijden, worden onder [!UICONTROL Low-Traffic] gebundeld.

* Dimension-objecten die zijn verzameld voordat de drempelwaarde is bereikt, worden normaal berekend.
* Dimension-items die worden verzameld nadat de drempelwaarde is overschreden, worden onder [!UICONTROL Low-Traffic] gebundeld.

>[!NOTE]
>De [ dimensie van de Pagina ](../components/dimensions/page.md) gebruikt verscheidene achterste kolommen die allen naar de unieke drempel, met inbegrip van `pagename` tellen, `page_url`, `first_hit_pagename`, `first_hit_page_url`, `visit_pagename`, `visit_page_url`, en `click_context`. Deze achterste kolommen kunnen [!UICONTROL Low-Traffic] logica veroorzaken om toe te passen ruim alvorens het aantal unieke pagina afmetingspunten in Workspace de drempel bereikt.

De unieke limiet van 2.000.000 kan per dimensie worden gewijzigd. Zie [ Veranderend unieke grensdrempels ](#changing-unique-limit-thresholds) hieronder. Aan het einde van een kalendermaand wordt het aantal bijgehouden unieke waarden globaal opnieuw ingesteld.

## Hoe waarden kunnen ontsnappen [!UICONTROL Low-Traffic] wanneer de drempelwaarde wordt overschreden

Als een bepaalde dimensie in een bepaalde maand meer dan 2.000.000 unieke waarden verzamelt, kunnen individuele dimensieitems terugkeren naar de rapportage van hun eigen dimensie-item. Het belangrijkste gebruik van deze functie is het rapporteren van cruciale dimensie-items die een sterke populariteit zouden kunnen krijgen laat in de maand nadat de unieke drempel is overschreden. Als uw organisatie bijvoorbeeld een site met miljoenen artikelen uitvoert en een nieuw artikel tegen het einde van de maand populair wordt, kunt u nog steeds de prestaties van dat artikel analyseren. Deze logica is niet bedoeld om alles op te heffen dat een bepaald aantal instanties krijgt, maar biedt een manier om inhoud te analyseren die een toestroom van verkeer ontvangt.

De vereisten voor een afzonderlijk dimensie-item om te ontsnappen [!UICONTROL Low-Traffic] zijn afhankelijk van vele factoren, die er in veel gevallen toe leiden dat een exacte drempel niet kan worden berekend:

* **Aantal servers die gegevens voor de rapportreeks** verwerken: De reeksen van het rapport met meer verkeer vereisen meer instanties van één enkel afmeting punt om [!UICONTROL Low-Traffic] te ontsnappen.
* **Hoeveelheid tijd tussen elke instantie van het afmetingspunt**: Hits die een afmetingspunt bevatten dat door de dag wordt verspreid vereist meer instanties dan een geconcentreerde opkomst van hits.
* **Aantal unieke waarden voor de afmeting**: Elke afmeting heeft een tweede drempel die aan een waarde van 2.100.000 unieke waarden door gebrek wordt geplaatst. Als het aantal unieke waarden in een dimensie deze hogere drempel overschrijdt, wordt het filter veel agressiever toegepast.

Rekening houdend met bovenstaande factoren, verwacht **honderden aan duizenden** instanties voor één enkel afmetingspunt om [!UICONTROL Low-Traffic] te ontsnappen als slechts de eerste drempel wordt overschreden. Verwacht **duizenden aan tienduizenden** instanties voor één enkel afmetingspunt om [!UICONTROL Low-Traffic] te ontsnappen als de hogere drempel wordt overschreden. Adobe garandeert niet dat dimensies op betrouwbare wijze buiten het emmertje van [!UICONTROL Low-Traffic] komen. Dit concept is typisch gereserveerd voor ongebruikelijk hoog-volume afmetingspunten laat in de maand.

Wanneer een afmetingsitem uit het emmertje van [!UICONTROL Low-Traffic] ontsnapt, blijven instanties die vóór de instroom van verkeer zijn verzameld onder [!UICONTROL Low-Traffic] .

## Unieke limietdrempels wijzigen

Drempelwaarden kunnen soms per dimensie worden gewijzigd. Neem contact op met de klantenservice van Adobe of uw Adobe-accountteam om deze wijziging aan te vragen. De mate waarin de drempelwaarden kunnen worden verhoogd, hangt af van meerdere factoren; Adobe garandeert niet dat aan alle verzoeken tot drempelverhoging kan worden voldaan. Neem bij het aanvragen van een wijziging de volgende gegevens op:

* De rapportsuite-id
* De dimensie die u wilt verhogen voor
* Zowel de eerste als de tweede gewenste drempel:
   * De eerste drempel (aanvankelijke het opsluiten) wordt geplaatst aan **2.000.000** door gebrek.
   * De tweede drempel (agressievere het filtreren) wordt geplaatst aan **2.100.000** door gebrek.

>[!IMPORTANT]
>
>Wijzigingen in drempelwaarden kunnen van invloed zijn op de prestaties van rapporten. Adobe raadt u ten zeerste aan goed te zijn wanneer u vraagt om een verhoging naar unieke waarden voor een dimensie. Verhoog alleen unieke limieten voor dimensies die van essentieel belang zijn voor de rapportagebehoeften van uw organisatie.

[!UICONTROL Low-Traffic] -drempels zijn niet zichtbaar in de gebruikersinterface voor analyse. Neem contact op met de klantenservice van Adobe als u meer informatie wilt over bestaande drempelwaarden.

## Interacties met andere mogelijkheden

Met verschillende mogelijkheden worden [!UICONTROL Low-Traffic] -waarden op verschillende manieren behandeld.

* **Data Warehouse:** In de meeste gevallen, is er geen grens aan het aantal unieke waarden in de rapporten van Data Warehouse. De unieke architectuur ervan maakt het mogelijk om een aantal unieke waarden te rapporteren. [!UICONTROL Low-Traffic] -waarden kunnen echter nog steeds in bepaalde beperkte scenario&#39;s worden weergegeven. Voorbeelden zijn lijstvariabelen, lijsteigenschappen, het verhandelen van eVars, en de detaildimensies van het marketingkanaal.
* **Segmentatie:** als de segmentcriteria een afmeting met een hoog aantal unieke waarden omvat, zijn de waarden onder [!UICONTROL Low-Traffic] worden gevangen niet inbegrepen.
* **Classificaties:** de rapporten van de Classificatie zijn ook onderworpen aan unieke grenzen. Als het item voor de bovenliggende dimensie van een classificatie is opgenomen onder [!UICONTROL Low-Traffic] , wordt de waarde niet geclassificeerd.
   * [!UICONTROL Low-Traffic] -waarden die via de importer zijn geclassificeerd, kunnen in Data Warehouse worden weergegeven. <!-- AN-115871 -->
   * [!UICONTROL Low-Traffic] waarden die door de regelbouwer *worden geclassificeerd kunnen niet* in Data Warehouse worden bekeken. <!-- AN-122872 -->
