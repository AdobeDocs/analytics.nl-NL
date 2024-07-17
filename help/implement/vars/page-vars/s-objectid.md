---
title: s_objectID
description: De Activity Map van de hulp identificeert unieke verbindingen op uw plaats.
feature: Variables
exl-id: 7c0cb750-2bfe-41ca-ab27-30dda4b3a7fa
role: Admin, Developer
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# s_objectID

De variabele `s_objectID` bevat een unieke id voor een koppeling. Het wordt gebruikt om rapporten in [ Activity Map ](/help/analyze/activity-map/overview.md) nauwkeuriger te maken. Als een pagina koppelingen bevat die vaak veranderen, kunt u de variabele `s_objectID` gebruiken om de Activity Map van een unieke koppelingslocatie te vertellen, zodat de gegevens correct kunnen worden gegroepeerd.

Als de nauwkeurigheid van de Activity Map van cruciaal belang is voor uw organisatie, wordt u aangeraden de variabele `s_objectID` op te nemen in de `onClick` -gebeurtenis van koppelingen op uw site.

## Object-id met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s_objectID in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De variabele `s_objectID` is een algemene variabele. Dit houdt in dat de variabele onafhankelijk van het object Analytics tracking werkt (`s` standaard). Geldige waarden voor deze variabele kunnen elke willekeurige tekenreeks met een lengte tot 100 bytes zijn. Als deze variabele niet is gedefinieerd, gebruikt de Activity Map de koppelingstekst als de id voor de koppeling.

Deze variabele wordt doorgaans ingesteld in de `onClick` -gebeurtenis van een HTML-koppeling.

```HTML
<a href="https://example.com" onClick="s_objectID='Example identifier';">Example link</a>
```

>[!NOTE]
>
>Neem altijd de puntkomma op die een JavaScript-instructie voltooit. De puntkomma is vereist om Activity Map te laten functioneren.

## Gebruik hoofdletters

De variabele `s_objectID` is handig wanneer u nauwkeuriger wilt rapporteren over de Activity Map.

### Koppelingen van zeer dynamische inhoud samenvoegen

Sommige sites hebben zeer dynamische inhoud, zoals nieuwssites of winkels waar artikelen vaak worden geroteerd. Aangezien de Activity Map de koppeling-URL standaard als id gebruikt, is het moeilijk om de gebieden met de meeste klik te begrijpen op pagina&#39;s waar koppelingen vaak veranderen. Als u `s_objectID` binnen deze verbindingen gebruikt, begrijpt de Activity Map welke verbindingen, ongeacht URLs kunnen worden bijeengevoegd zij richten aan.

```HTML
<a href="story1.html" onClick="s_objectID='Top left link';">Story 1</a>
<a href="story2.html" onClick="s_objectID='Top center link';">Story 2</a>
<a href="story3.html" onClick="s_objectID='Top right link';">Story 3</a>
```

Ongeacht waar de koppelingen wijzen of hoe vaak u deze koppelingen wijzigt, worden bij de Activity Map gegevens geaggregeerd op basis van de waarde in `s_objectID` .

### Koppelingen afzonderlijk op een pagina houden

Sommige sites hebben koppelingen die verwijzen naar dezelfde locatie op verschillende locaties. Bijvoorbeeld een koppeling naar de startpagina in zowel de kop- als voettekst op uw site. Aangezien deze koppelingen dezelfde URL hebben, worden de gegevens door de Activity Map geaggregeerd. U kunt ze scheiden met de variabele `s_objectID` :

```HTML
<a href="index.html" onClick="s_objectID='Header home link';">Example link in Header</a>
<a href="index.html" onClick="s_objectID='Footer home link';">Example link in Footer</a>
```

Zelfs als koppelingen naar dezelfde URL verwijzen, kan Activity Map de variabele `s_objectID` gebruiken om ze te onderscheiden in de juiste rapportage.
