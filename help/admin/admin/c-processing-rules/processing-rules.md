---
description: De verwerkingsregels vereenvoudigen gegevensverzameling en beheren inhoud aangezien het naar rapportering wordt verzonden.
subtopic: Processing rules
title: Overzicht van verwerkingsregels
topic: Beheerprogramma's
uuid: 6b4ee7c9-2b86-47a6-b64c-c8d644fff67d
translation-type: tm+mt
source-git-commit: a42fdbf2938f08ab09f9be7e0e3e89bab4f50eae
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 2%

---


# Overzicht van verwerkingsregels

De verwerkingsregels vereenvoudigen gegevensverzameling en beheren inhoud aangezien het naar rapportering wordt verzonden. De regels van de verwerking helpen interactie met de groepen van IT en de ontwikkelaars van het Web vereenvoudigen door een interface te verstrekken aan:

* Een gebeurtenis instellen op de pagina met productoverzicht
* Campagne vullen met een parameter van het vraagkoord
* Categorie en paginanaam samenvoegen in een hulpmiddel voor gemakkelijker rapportage
* Een eVar naar een profiel kopiëren om paden weer te geven
* Onjuist gespelde sitesecties opruimen
* Interne zoektermen of een campagne-id uit de queryreeks in een eVar aftrekken

>[!VIDEO](https://video.tv.adobe.com/v/26124/?quality=12&learn=on)

## Machtigingen voor verwerkingsregels {#section_8A4846688050453784DAE4D89355169A}

Beheerders hebben standaard rechten om verwerkingsregels **te gebruiken.** Beheerders kunnen deze rechten ook aan niet-beheerders toekennen via de interface Admin Tools. Zie [] voor instructies

![](assets/processing-rules.png)

>[!IMPORTANT]
>
>Omdat de verwerkingsregels de gegevens van Analytics permanent beïnvloeden, adviseert Adobe sterk dat de beheerders van de verwerkingsregels certificatieopleiding in Adobe Analytics ontvangen, en met alle bronnen van gegevens voor uw rapportreeksen vertrouwd zijn (standaardwebsites, mobiele plaatsen, mobiele apps, de Invoeging API van Gegevens, etc.). Kennis van de contextgegevensvariabelen en standaardvariabelen die op verschillende platforms zijn ingevuld, zal helpen te voorkomen dat gegevens per ongeluk worden verwijderd of gewijzigd.

## Contextgegevens gebruiken om gegevensverzameling te vereenvoudigen {#section_09EEA03612D24C15839631AA9E9668D8}

Contextgegevensvariabelen zijn een type variabele dat alleen beschikbaar is voor verwerkingsregels. Om de variabelen van contextgegevens te gebruiken, worden de sleutel/waardegegevensparen verzonden binnen door uw implementatie, en de verwerkingsregels worden gebruikt om deze waarden in standaardvariabelen van de Analyse te vangen. Hierdoor kunnen programmeurs niet precies zien welke eigenschap en/of eVar welke waarde moet bevatten.

```js
s.contextData['author'] = "Robert Munch";
s.contextData['section'] = "Books";
s.contextData['genre'] = "Youth";
```

Als u de code eenmaal hebt ingesteld, kunt u verwerkingsregels instellen om waarden toe te wijzen aan variabelen. Bijvoorbeeld:

1. `author` toewijzen aan `eVar2`
2. `section` toewijzen aan `prop1` en `eVar3`
3. Als `author` en `section` bestaan, plaatst `event5`

Zie [contextData](/help/implement/vars/page-vars/contextdata.md) in de de gebruikershandleiding van de Implementatie voor meer informatie.

## Verwerkingsregels gebruiken om Actief gegevens- en Triggergebeurtenissen om te zetten {#section_8284E72E999244E091CD7FB1A22342B6}

De regels van de verwerking kunnen inkomende waarden controleren om gemeenschappelijke typos om te zetten en gebeurtenissen te plaatsen die op gemelde gegevens worden gebaseerd. Props kunnen naar Vars worden gekopieerd. Waarden kunnen voor rapporten worden samengevoegd en gebeurtenissen kunnen worden ingesteld.

## Contextgegevensvariabelen gebruiken in rapportage {#section_BD098BC503024A0B8703596628071134}

Zodra de variabelen van contextgegevens binnen uw implementatie worden bepaald, moeten zij aan variabelen zoals eVars worden gekopieerd om in rapportering te worden gebruikt.

Zie [Een contextgegevensvariabele kopiëren naar een eVar](processing-rules-examples/processing-rules-copy-context-data.md) en [Een gebeurtenis instellen met een contextgegevensvariabele](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md) voor meer informatie.
