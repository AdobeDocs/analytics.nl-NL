---
title: s_objectID
description: De Activity Map van de hulp identificeert unieke verbindingen op uw plaats.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# s_objectID

De `s_objectID` variabele verschaft een unieke id voor een koppeling. Het wordt gebruikt om verslagen in de [Activity Map](/help/analyze/activity-map/activity-map.md) nauwkeuriger te maken. Als u koppelingen op een pagina hebt die vaak worden gewijzigd, kunt u de `s_objectID` variabele gebruiken om de Activity Map van een unieke koppelingslocatie te vertellen, zodat gegevens correct kunnen worden gegroepeerd.

Als de nauwkeurigheid van de Activity Map van cruciaal belang is voor uw organisatie, raadt Adobe aan de `s_objectID` variabele op te nemen in het `onClick` geval van koppelingen op uw site. Raadpleeg de gebruikershandleiding bij Analyseren voor meer informatie over het gebruik van koppelingen voor het bijhouden van [Activity Mappen](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-use-case.md) .

## Object-id in Adobe Experience Platform starten

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s_objectID in de aangepaste code-editor van AppMeasurement en Launch

De `s_objectID` variabele is een algemene variabele. Dit houdt in dat de variabele onafhankelijk van het object Analytics tracking werkt (`s` standaard). Geldige waarden voor deze variabele kunnen elke willekeurige tekenreeks met een lengte tot 100 bytes zijn. Als deze variabele niet is gedefinieerd, gebruikt de Activity Map de koppelings-URL als de id voor de koppeling.

Deze variabele wordt doorgaans ingesteld in het `onClick` geval van een HTML-koppeling.

```HTML
<a href="https://example.com" onClick="s_objectID='Example identifier';">Example link</a>
```

>[!NOTE]
>
>Neem altijd de puntkomma op die een JavaScript-instructie voltooit. De puntkomma is vereist om Activity Map te laten functioneren.

## Gebruik hoofdletters

De `s_objectID` variabele is handig wanneer u nauwkeuriger wilt rapporteren over de Activity Map.

### Koppelingen van zeer dynamische inhoud samenvoegen

Sommige sites hebben zeer dynamische inhoud, zoals nieuwssites of winkels waar artikelen vaak worden geroteerd. Aangezien de Activity Map de koppeling-URL standaard als id gebruikt, is het moeilijk om de gebieden met de meeste klik te begrijpen op pagina&#39;s waar koppelingen vaak veranderen. Als u de koppelingen `s_objectID` binnen deze koppelingen gebruikt, begrijpt de Activity Map welke koppelingen kunnen worden samengevoegd, ongeacht de URL&#39;s waarnaar ze verwijzen.

```HTML
<a href="story1.html" onClick="s_objectID='Top left link';">Story 1</a>
<a href="story2.html" onClick="s_objectID='Top center link';">Story 2</a>
<a href="story3.html" onClick="s_objectID='Top right link';">Story 3</a>
```

Ongeacht waar de verbindingen richten of hoe vaak u deze verbindingen verandert, voegt de Activity Map gegevens samen die op de waarde in worden gebaseerd `s_objectID`.

### Koppelingen afzonderlijk op een pagina houden

Sommige sites hebben koppelingen die verwijzen naar dezelfde locatie op verschillende locaties. Bijvoorbeeld een koppeling naar de startpagina in zowel de kop- als voettekst op uw site. Aangezien deze koppelingen dezelfde URL hebben, worden de gegevens door de Activity Map geaggregeerd. U kunt ze scheiden met de `s_objectID` variabele:

```HTML
<a href="index.html" onClick="s_objectID='Header home link';">Example link in Header</a>
<a href="index.html" onClick="s_objectID='Footer home link';">Example link in Footer</a>
```

Zelfs als koppelingen naar dezelfde URL verwijzen, kan Activity Map de `s_objectID` variabele gebruiken om deze op de juiste manier te onderscheiden in de rapportage.
