---
title: Hoe worden segmenten in Report Builder in Adobe Analytics gebruikt?
description: Beschrijft hoe te om segmenten in Report Builder voor Adobe Analytics te gebruiken
role: User
feature: Report Builder
type: Documentation
solution: Analytics
source-git-commit: eedabc6295f9b918e1e00b93993680e676c216c3
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Werken met segmenten in Report Builder

U kunt segmenten toepassen wanneer u een nieuw gegevensblok creeert of wanneer u **uitgezocht geef gegevensblok** optie van het paneel van BEVELINGEN uit.

## Segmenten toepassen op een gegevensblok

Als u een segment wilt toepassen op het volledige gegevensblok, dubbelklikt u op een segment of sleept u de filters uit de lijst met componenten naar het gedeelte Segmenten van de tabel.

## Segmenten toepassen op afzonderlijke metriek

Als u segmenten wilt toepassen op afzonderlijke metrische elementen, sleept u een segment naar een metrische waarde in de tabel. U kunt **ook klikken...** pictogram aan het recht van metrisch in de ruit van de Lijst en dan selecteren **metrisch segment**. Als u toegepaste segmenten wilt weergeven, plaatst u de muisaanwijzer boven of selecteert u een metrische waarde in het deelvenster Tabel. De metriek met toegepaste segmenten tonen een filterpictogram.

![ het lusje van Segmenten die metriek tonen.](./assets/filter_by.png)

## Snel segmenten bewerken

Met het deelvenster Snel bewerken kunt u segmenten voor bestaande gegevensblokken toevoegen, verwijderen of vervangen.

Wanneer u een waaier van cellen in spreadsheet selecteert, de **verbinding van Segmenten** in Snel uitgeeft paneel toont een summiere lijst van de segmenten die door de gegevensblokken in die selectie worden gebruikt.

Segmenten bewerken met het deelvenster Snel bewerken

1. Selecteer een bereik cellen uit een of meerdere gegevensblokken.

   ![ Snel geef segmentpaneel uit die segmentopties voor rapportsuites, datumwaaier, en segmenten tonen.](./assets/select_multiple_dbs.png)

1. Klik op de koppeling Segmenten om het deelvenster Snel bewerken - Filters te starten.

   ![ het paneel van Segmenten die het Add gebied van Segmenten en Toegepaste Segmenten tonen lijsten.](./assets/quick_edit_filters.png)

### Een segment toevoegen of verwijderen

U kunt segmenten toevoegen of verwijderen met de opties Toevoegen/Verwijderen.

1. Selecteer **toevoegen/verwijderen** lusje in Snel geef-segmenten paneel uit.

   Alle segmenten die zijn toegepast op de geselecteerde gegevensblokken, worden weergegeven in het deelvenster Snel bewerken-segmenten. De segmenten die op alle gegevensblokken in de selectie worden toegepast worden vermeld onder **op alle geselecteerde gegevensblokken** rubriek worden toegepast. De segmenten die op sommige maar niet alle gegevensblokken worden toegepast zijn vermeld onder **op 1 of meer geselecteerde gegevensblokken** rubriek worden toegepast.

   Wanneer de veelvoudige segmenten in de geselecteerde gegevensblokken aanwezig zijn, kunt u naar specifieke segmenten zoeken gebruikend **toevoegen het onderzoeksgebied van de Filter**.

   ![ het Add gebied van Segmenten.](./assets/add_filter.png)

1. Voeg segmenten toe door segmenten van **te selecteren voeg segment** drop-down menu toe.

   De lijst van doorzoekbare segmenten omvat alle segmenten die voor de rapportreeksen toegankelijk zijn die in één of meerdere geselecteerde gegevensblokken evenals alle segmenten aanwezig zijn die globaal in de organisatie beschikbaar zijn.

   Als u een segment toevoegt, wordt het segment toegepast op alle gegevensblokken in de selectie.

1. Om segmenten te verwijderen, klik het schrappingspictogram **x** rechts van segmenten in de **toegepaste Segmenten** lijst.

1. Klik **toepassen** om veranderingen te bewaren en aan het hubpaneel terug te keren.

   De Report Builder toont een bericht om de toegepaste segmentveranderingen te bevestigen.

### Een segment vervangen

U kunt een bestaand segment vervangen door een ander segment om te wijzigen hoe de gegevens worden gesegmenteerd.

1. Selecteer **vervangen** lusje in Snel uitgeven-segment paneel.

   ![ selecteer Replace tabel.](./assets/replace_filter.png)

1. Gebruik het **de lijst van het Onderzoek** onderzoeksgebied om van specifieke segmenten de plaats te bepalen.

1. Kies een of meer segmenten die u wilt vervangen.

1. Zoeken naar een of meer segmenten in het veld Vervangen door.

   Het selecteren van een filter voegt het aan **toe vervangt met**... lijst.

   ![ het Replace lusje met de Mensen op App geselecteerde gegevensblok en Replace met lijst die Personen op Herziene App tonen.](./assets/replace_screen_new.png)

1. Klik **toepassen**.

   De Report Builder werkt de lijst van segmenten bij om op de vervanging te wijzen.

### Gegevensbloksegmenten vanuit cel definiëren

Gegevensblokken kunnen verwijzen naar segmenten uit een cel. De veelvoudige gegevensblokken kunnen de zelfde cel voor segmenten van verwijzingen voorzien, toestaand u om segmenten voor veelvoudige gegevensblokken tegelijkertijd gemakkelijk te schakelen.

Segmenten uit een cel toepassen

1. Navigeer naar stap 2 in het maken of bewerken van gegevensblokken. Zie [ een Blok van Gegevens ](./create-a-data-block.md) creëren.
1. Klik het **lusje van Segmenten** om filters te bepalen.
1. Klik **creeer segment van cel**.

   ![ creeer segment van celpictogram.](./assets/create-filter-from-cell.png)

1. Selecteer de cel waaruit u wilt dat de gegevensblokken naar een segment verwijzen.

1. Voeg de segmentkeuze toe die u aan de cel wilt toevoegen door te dubbelklikken op het segment of door deze te slepen naar de sectie Segmenten inclusief.

   Opmerking: Er kan slechts één keuze voor de desbetreffende cel tegelijk worden geselecteerd.

   ![ voegt segment van celvenster toe die de inbegrepen Filters tonen.](./assets/select-filters.png)

1. Klik **toepassen** om de verwijzingscel tot stand te brengen.

1. Van het **lusje van Segmenten**, voeg de pas gecreëerde segmenten van de verwijzingscel aan uw gegevensblok toe.

   ![ het lusje van Segmenten die Sheet1 tonen!J1 (Alle Gegevens) segment aan de lijst wordt toegevoegd.](./assets/reference-cell-filter.png)

1. Klik **Afwerking**.

   Nu kan naar deze cel worden verwezen door andere gegevensblokken in hun segmenten. Als u de referentiecel als een segment wilt toepassen op andere gegevensblokken, voegt u vanuit het tabblad Segmenten de celverwijzing naar de desbetreffende segmenten toe.

#### De referentiecel gebruiken om gegevensbloksegmenten te wijzigen

1. Selecteer de referentiecel in het werkblad.

1. Klik de verbinding onder **Segmenten van Cel** in Snel uitgeven menu.

   ![ Segmenten van celverbinding die Sheet1 tonen!J1 (Alle Gegevens) ](./assets/filters-from-cell-link.png)

1. Selecteer het segment in het keuzemenu.

   ![ de daling van Segmenten onderaan menu ](./assets/filter-drop-down.png)

1. Klik **toepassen**.
