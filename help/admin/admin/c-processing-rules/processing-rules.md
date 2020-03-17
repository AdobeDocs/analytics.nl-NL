---
description: De verwerkingsregels vereenvoudigen gegevensverzameling en beheren inhoud aangezien het naar rapportering wordt verzonden.
subtopic: Processing rules
title: Overzicht van verwerkingsregels
topic: Admin tools
uuid: 6b4ee7c9-2b86-47a6-b64c-c8d644fff67d
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Overzicht van verwerkingsregels

De verwerkingsregels vereenvoudigen gegevensverzameling en beheren inhoud aangezien het naar rapportering wordt verzonden. De regels van de verwerking helpen interactie met de groepen van IT en de ontwikkelaars van het Web vereenvoudigen door een interface te verstrekken aan:

* Een gebeurtenis instellen op de pagina met productoverzicht
* Campagne vullen met een parameter van het vraagkoord
* Categorie en paginanaam samenvoegen in een hulpmiddel voor gemakkelijker rapportage
* Een eVar naar een pop kopiëren om paden te zien
* Onjuist gespelde sitesecties opruimen
* Interne zoektermen of een campagne-id uit de queryreeks in een eVar plakken

>[!VIDEO](https://tv.adobe.com/embed/1181/16506/)

*Bekijk het overzicht van de verwerkingsregels en de training van de Adobe-top om te leren waarom u verwerkingsregels moet gebruiken.*

## Ervoor worden geautoriseerd om verwerkingsregels te gebruiken {#section_8A4846688050453784DAE4D89355169A}

Vóór 20 april 2017 moesten alle gebruikers (inclusief beheerders) een examen afleggen en toestemming krijgen om verwerkingsregels te gebruiken door de klantenservice van Adobe.

Nu, hebben de beheerders rechten om verwerkingsregels **door gebrek** te gebruiken. Het examen is niet meer noodzakelijk. Beheerders kunnen deze rechten ook aan niet-beheerders toekennen via de interface Admin Tools. Hieronder wordt beschreven hoe:

1. Als u dit nog niet hebt gedaan, [creeert u een groep](/help/admin/user-management2/c-user-groups/groups.md) die slechts die niet-beheerders omvat die toestemming zouden moeten hebben om verwerkingsregels te gebruiken.
1. [Voeg de niet-beheerders toe aan die groep](/help/admin/user-management2/c-user-management/t-add-user-to-group.md).
1. Ga vervolgens naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]** > **[!UICONTROL Groups]** > **[!UICONTROL-[groepsnaam]]** > **[!UICONTROL Edit]** > **[!UICONTROL Report Access]** **[!UICONTROL Report Suite Tools]** **[!UICONTROL Customize]** **[!UICONTROL Report Suite Management]**>  > .
1. Schakel het selectievakje naast [!UICONTROL Processing Rules] en klik op **[!UICONTROL OK]**.

![](assets/processing-rules.png)

>[!IMPORTANT]
>
>Omdat de verwerkingsregels de gegevens van Analytics permanent beïnvloeden, adviseren wij sterk dat de beheerders van de verwerkingsregels certificatie in de Analytics van Adobe ontvangen, en vertrouwd met alle bronnen van gegevens voor uw rapportreeksen (standaardwebsites, mobiele plaatsen, mobiele apps, de Invoeging API van Gegevens, etc.) zijn. Kennis van de contextgegevensvariabelen en standaardvariabelen die op verschillende platforms zijn ingevuld, zal helpen te voorkomen dat gegevens per ongeluk worden verwijderd of gewijzigd.

## Contextgegevens gebruiken om gegevensverzameling te vereenvoudigen {#section_09EEA03612D24C15839631AA9E9668D8}

Contextgegevensvariabelen zijn een nieuw type variabele dat alleen beschikbaar is voor verwerkingsregels. Om de variabelen van contextgegevens te gebruiken, worden de sleutel/waardegegevensparen verzonden binnen door uw implementatie, en de verwerkingsregels worden gebruikt om deze waarden in standaardvariabelen van de Analyse te vangen. Hierdoor kunnen programmeurs precies zien welke eigenschap en/of eVar moet bevatten.

![](assets/evar-context-map.png)

Zie [Contextgegevensvariabelen](https://marketing.adobe.com/resources/help/en_US/sc/implement/context_data_variables.html) in de Help bij Implementatie.

## Verwerkingsregels gebruiken om Actief-gegevens- en Triggergebeurtenissen te transformeren {#section_8284E72E999244E091CD7FB1A22342B6}

De regels van de verwerking kunnen inkomende waarden controleren om gemeenschappelijke typos om te zetten en gebeurtenissen te plaatsen die op gemelde gegevens worden gebaseerd. Props kunnen naar Vars worden gekopieerd. Waarden kunnen voor rapporten worden samengevoegd en gebeurtenissen kunnen worden ingesteld.

## Contextgegevensvariabelen gebruiken bij rapportage {#section_BD098BC503024A0B8703596628071134}

Zodra de variabelen van contextgegevens binnen uw implementatie worden bepaald, moeten zij aan variabelen zoals eVars worden gekopieerd om in rapportering te worden gebruikt.

Voor meer informatie, ga [hier](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md) en [hier](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md).
