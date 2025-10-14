---
title: s_objectID
description: Help Activity Map unieke koppelingen op uw site te identificeren.
feature: Appmeasurement Implementation
exl-id: 7c0cb750-2bfe-41ca-ab27-30dda4b3a7fa
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# s_objectID

De variabele `s_objectID` bevat een unieke id voor een koppeling. Het wordt gebruikt om rapporten in [&#x200B; Activity Map &#x200B;](/help/analyze/activity-map/overview.md) nauwkeuriger te maken. Als er koppelingen op een pagina staan die vaak veranderen, kunt u de variabele `s_objectID` gebruiken om Activity Map op de hoogte te stellen van een unieke koppelingslocatie, zodat deze gegevens correct kan groeperen.

Als Activity Map-nauwkeurigheid van cruciaal belang is voor uw organisatie, raadt Adobe aan de variabele `s_objectID` op te nemen in de `onClick` -gebeurtenis van koppelingen op uw site.

## Object-id met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s_objectID in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s_objectID` is een algemene variabele. Dit houdt in dat de variabele onafhankelijk van het object Analytics tracking werkt (`s` standaard). Geldige waarden voor deze variabele kunnen elke willekeurige tekenreeks met een lengte tot 100 bytes zijn. Als deze variabele niet is gedefinieerd, gebruikt Activity Map de koppelingstekst als de id voor de koppeling.

Deze variabele wordt doorgaans ingesteld in de `onClick` -gebeurtenis van een HTML-koppeling.

```HTML
<a href="https://example.com" onClick="s_objectID='Example identifier';">Example link</a>
```

>[!NOTE]
>
>Neem altijd de puntkomma op die een JavaScript-instructie voltooit. Activity Map kan alleen functioneren met de puntkomma.

## Gebruik hoofdletters

De variabele `s_objectID` is waardevol wanneer u een grotere nauwkeurigheid in Activity Map-rapportage wilt.

### Koppelingen van zeer dynamische inhoud samenvoegen

Sommige sites hebben zeer dynamische inhoud, zoals nieuwssites of winkels waar artikelen vaak worden geroteerd. Aangezien Activity Map standaard de URL van de koppeling gebruikt als id, is het moeilijk om de gebieden met de meeste klik te begrijpen op pagina&#39;s waar koppelingen vaak veranderen. Als u `s_objectID` binnen deze koppelingen gebruikt, begrijpt Activity Map welke koppelingen kunnen worden samengevoegd, ongeacht de URL&#39;s waarnaar ze verwijzen.

```HTML
<a href="story1.html" onClick="s_objectID='Top left link';">Story 1</a>
<a href="story2.html" onClick="s_objectID='Top center link';">Story 2</a>
<a href="story3.html" onClick="s_objectID='Top right link';">Story 3</a>
```

Ongeacht waar de koppelingen wijzen of hoe vaak u deze koppelingen wijzigt, aggregeert Activity Map gegevens op basis van de waarde in `s_objectID` .

### Koppelingen afzonderlijk op een pagina houden

Sommige sites hebben koppelingen die verwijzen naar dezelfde locatie op verschillende locaties. Bijvoorbeeld een koppeling naar de startpagina in zowel de kop- als voettekst op uw site. Aangezien deze koppelingen dezelfde URL hebben, aggregeert Activity Map de gegevens ervan. U kunt ze scheiden met de variabele `s_objectID` :

```HTML
<a href="index.html" onClick="s_objectID='Header home link';">Example link in Header</a>
<a href="index.html" onClick="s_objectID='Footer home link';">Example link in Footer</a>
```

Zelfs als koppelingen naar dezelfde URL verwijzen, kan Activity Map de variabele `s_objectID` gebruiken om ze te onderscheiden in de juiste rapportage.
