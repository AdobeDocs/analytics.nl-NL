---
description: De verwerkingsregels vereenvoudigen gegevensverzameling en beheren inhoud aangezien het naar rapportering wordt verzonden.
subtopic: Processing rules
title: Overzicht van verwerkingsregels
feature: Processing Rules
role: Admin
exl-id: 0244aba2-4345-463a-8528-d4dcd2f872ff
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Overzicht van verwerkingsregels

De verwerkingsregels vereenvoudigen gegevensverzameling en beheren inhoud aangezien het naar rapportering wordt verzonden. De regels van de verwerking helpen interactie met de groepen van IT en de ontwikkelaars van het Web vereenvoudigen door een interface te verstrekken aan:

* Een gebeurtenis instellen op de pagina met productoverzicht
* Campagne vullen met een parameter van het vraagkoord
* Categorie en paginanaam samenvoegen in een hulpmiddel voor gemakkelijker rapportage
* Een eVar naar een profiel kopiëren om paden te zien
* Onjuist gespelde sitesecties opruimen
* Interne zoektermen of een campagne-id uit de queryreeks in een eVar aftrekken



>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ overzicht van de Regels van de Verwerking ](https://video.tv.adobe.com/v/26124/?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Rechten voor verwerkingsregels {#section_8A4846688050453784DAE4D89355169A}

De beheerders hebben rechten om verwerkingsregels **door gebrek** te gebruiken. Beheerders kunnen deze rechten ook aan niet-beheerders toekennen via de interface Admin Tools. Zie [] voor instructies

![ Regels van de Verwerking ](assets/processing-rules.png)

## Contextgegevens gebruiken om gegevensverzameling te vereenvoudigen {#section_09EEA03612D24C15839631AA9E9668D8}

Contextgegevensvariabelen zijn een type variabele dat alleen beschikbaar is voor verwerkingsregels. Om de variabelen van contextgegevens te gebruiken, worden de sleutel/waardegegevensparen verzonden binnen door uw implementatie, en de verwerkingsregels worden gebruikt om deze waarden in standaardvariabelen van de Analyse te vangen. Hierdoor hebben programmeurs geen precies inzicht in welke eigenschap en/of eVar welke waarde moet bevatten.

```js
s.contextData['author'] = "Robert Munch";
s.contextData['section'] = "Books";
s.contextData['genre'] = "Youth";
```

Als u de code eenmaal hebt ingesteld, kunt u verwerkingsregels instellen om waarden toe te wijzen aan variabelen. Bijvoorbeeld:

1. Toewijzen `author` aan `eVar2`
2. Toewijzen `section` aan `prop1` en `eVar3`
3. Indien `author` en `section` bestaan, stelt u `event5` in

Zie [ contextData ](/help/implement/vars/page-vars/contextdata.md) in de de gebruikersgids van het Uitvoeren voor meer informatie.

## Verwerkingsregels gebruiken om Actief-gegevens- en Triggergebeurtenissen te transformeren {#section_8284E72E999244E091CD7FB1A22342B6}

De regels van de verwerking kunnen inkomende waarden controleren om gemeenschappelijke typos om te zetten en gebeurtenissen te plaatsen die op gemelde gegevens worden gebaseerd. Props kunnen naar Vars worden gekopieerd. Waarden kunnen voor rapporten worden samengevoegd en gebeurtenissen kunnen worden ingesteld.

## Contextgegevensvariabelen gebruiken bij rapportage {#section_BD098BC503024A0B8703596628071134}

Zodra de variabelen van contextgegevens binnen uw implementatie worden bepaald, moeten zij aan variabelen zoals eVars worden gekopieerd om in rapportering te worden gebruikt.

Zie [ exemplaar een variabele van contextgegevens aan een eVar ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md) en [ plaats een gebeurtenis gebruikend een variabele van contextgegevens ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md) voor meer informatie.

## Bekende beperkingen

**Gebruik van katten (^) in verwerkingsregels.** Als u in de verwerkingsregels kartels wilt gebruiken als scheidingstekens of voor andere doeleinden, moet elk karaat door twee kartels worden vertegenwoordigd. Eén karaat bijvoorbeeld weergeven als ^^, een dubbele karaat als ^^^, enzovoort.