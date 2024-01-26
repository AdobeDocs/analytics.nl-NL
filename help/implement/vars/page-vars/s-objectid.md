---
title: s_objectID
description: De Activity Map van de hulp identificeert unieke verbindingen op uw plaats.
feature: Variables
exl-id: 7c0cb750-2bfe-41ca-ab27-30dda4b3a7fa
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# s_objectID

De `s_objectID` De variabele verstrekt een uniek herkenningsteken voor een verbinding. Hiermee kunt u rapporten maken in [Activity Map](/help/analyze/activity-map/activity-map.md) nauwkeuriger. Als er koppelingen op een pagina staan die vaak worden gewijzigd, kunt u de opdracht `s_objectID` variabele om de Activity Map van een unieke koppelingsplaats te vertellen zodat kan het gegevens correct groeperen zoals gewenst.

Als de nauwkeurigheid van de Activity Map van cruciaal belang is voor uw organisatie, raadt de Adobe aan om de `s_objectID` in de `onClick` gebeurtenis van koppelingen op uw site. Zie [Gebruiksgevallen voor het bijhouden van koppelingen Activity Mappen](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-use-case.md) in de gebruikershandleiding Analyseren voor meer informatie.

## Object-id met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s_objectID in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De `s_objectID` variable is a global variable (variabele die onafhankelijk van het object Analytics tracking werkt) (`s` standaard). Geldige waarden voor deze variabele kunnen elke willekeurige tekenreeks met een lengte tot 100 bytes zijn. Als deze variabele niet is gedefinieerd, gebruikt de Activity Map de koppelings-URL als de id voor de koppeling.

Deze variabele wordt doorgaans ingesteld in het dialoogvenster `onClick` gebeurtenis van een HTML-koppeling.

```HTML
<a href="https://example.com" onClick="s_objectID='Example identifier';">Example link</a>
```

>[!NOTE]
>
>Neem altijd de puntkomma op die een JavaScript-instructie voltooit. De puntkomma is vereist om Activity Map te laten functioneren.

## Gebruik hoofdletters

De `s_objectID` Deze variabele is handig wanneer u nauwkeuriger wilt rapporteren over de Activity Map.

### Koppelingen van zeer dynamische inhoud samenvoegen

Sommige sites hebben zeer dynamische inhoud, zoals nieuwssites of winkels waar artikelen vaak worden geroteerd. Aangezien de Activity Map de koppeling-URL standaard als id gebruikt, is het moeilijk om de gebieden met de meeste klik te begrijpen op pagina&#39;s waar koppelingen vaak veranderen. Als u het `s_objectID` binnen deze koppelingen begrijpt de Activity Map welke koppelingen kunnen worden samengevoegd, ongeacht de URL&#39;s waarnaar ze verwijzen.

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

Zelfs als koppelingen naar dezelfde URL verwijzen, kan de Activity Map de opdracht `s_objectID` om ze bij de rapportage correct te onderscheiden.
