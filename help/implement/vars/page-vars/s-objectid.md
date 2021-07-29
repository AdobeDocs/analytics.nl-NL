---
title: s_objectID
description: De Activity Map van de hulp identificeert unieke verbindingen op uw plaats.
exl-id: 7c0cb750-2bfe-41ca-ab27-30dda4b3a7fa
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# s_objectID

De `s_objectID` variabele verstrekt een uniek herkenningsteken voor een verbinding. Het wordt gebruikt om rapporten in [Activity Map](/help/analyze/activity-map/activity-map.md) nauwkeuriger te maken. Als u koppelingen op een pagina hebt die vaak worden gewijzigd, kunt u de variabele `s_objectID` gebruiken om de Activity Map van een unieke koppelingslocatie te vertellen, zodat gegevens correct kunnen worden gegroepeerd zoals gewenst.

Als de nauwkeurigheid van de Activity Map van cruciaal belang is voor uw organisatie, raadt Adobe aan de `s_objectID`-variabele op te nemen in de `onClick`-gebeurtenis van koppelingen op uw site. Zie [Gebruiksgevallen voor het bijhouden van koppelingen voor Activity Mappen](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-use-case.md) in de gebruikershandleiding Analyseren voor meer informatie.

## Object-id met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s_objectID in AppMeasurement en aangepaste code-editor

De variabele `s_objectID` is een globale variabele, die betekent dat het onafhankelijk van het volgende voorwerp van Analytics (`s` door gebrek) werkt. Geldige waarden voor deze variabele kunnen elke willekeurige tekenreeks met een lengte tot 100 bytes zijn. Als deze variabele niet is gedefinieerd, gebruikt de Activity Map de koppelings-URL als de id voor de koppeling.

Deze variabele wordt doorgaans ingesteld in de gebeurtenis `onClick` van een HTML-koppeling.

```HTML
<a href="https://example.com" onClick="s_objectID='Example identifier';">Example link</a>
```

>[!NOTE]
>
>Neem altijd de puntkomma op die een JavaScript-instructie voltooit. De puntkomma is vereist om Activity Map te laten functioneren.

## Gebruik hoofdletters

De variabele `s_objectID` is waardevol wanneer u grotere nauwkeurigheid in Activity Map het melden wilt.

### Koppelingen van zeer dynamische inhoud samenvoegen

Sommige sites hebben zeer dynamische inhoud, zoals nieuwssites of winkels waar artikelen vaak worden geroteerd. Aangezien de Activity Map de koppeling-URL standaard als id gebruikt, is het moeilijk om de gebieden met de meeste klik te begrijpen op pagina&#39;s waar koppelingen vaak veranderen. Als u `s_objectID` binnen deze verbindingen gebruikt, begrijpt de Activity Map welke verbindingen, ongeacht URLs kunnen worden samengevoegd zij richten aan.

```HTML
<a href="story1.html" onClick="s_objectID='Top left link';">Story 1</a>
<a href="story2.html" onClick="s_objectID='Top center link';">Story 2</a>
<a href="story3.html" onClick="s_objectID='Top right link';">Story 3</a>
```

Ongeacht waar de verbindingen richten of hoe vaak u deze verbindingen verandert, voegt de Activity Map gegevens samen die op de waarde in `s_objectID` worden gebaseerd.

### Koppelingen afzonderlijk op een pagina houden

Sommige sites hebben koppelingen die verwijzen naar dezelfde locatie op verschillende locaties. Bijvoorbeeld een koppeling naar de startpagina in zowel de kop- als voettekst op uw site. Aangezien deze koppelingen dezelfde URL hebben, worden de gegevens door de Activity Map geaggregeerd. U kunt ze scheiden met de variabele `s_objectID`:

```HTML
<a href="index.html" onClick="s_objectID='Header home link';">Example link in Header</a>
<a href="index.html" onClick="s_objectID='Footer home link';">Example link in Footer</a>
```

Zelfs als de verbindingen aan zelfde URL richten, kan de Activity Map `s_objectID` variabele gebruiken om hen in het melden correct te onderscheiden.
