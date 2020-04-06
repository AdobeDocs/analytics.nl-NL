---
title: s_objectID
description: De Activiteitenkaart van de hulp identificeert unieke verbindingen op uw plaats.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# s_objectID

De `s_objectID` variabele verschaft een unieke id voor een koppeling. Het wordt gebruikt om rapporten in de [Kaart](/help/analyze/activity-map/activity-map.md) van de Activiteit nauwkeuriger te maken. Als u koppelingen op een pagina hebt die vaak veranderen, kunt u de `s_objectID` variabele gebruiken om Activiteitenkaart van een unieke verbindingsplaats te vertellen zodat het gegevens correct kan groeperen zoals gewenst.

Als de nauwkeurigheid van de Activiteitenkaart van cruciaal belang is voor uw organisatie, raadt Adobe aan de `s_objectID` variabele op te nemen in het `onClick` geval van koppelingen op uw site. Zie [Activiteitenkaart gebruiken gevallen](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-use-case.md) voor het bijhouden van koppelingen in de gebruikershandleiding Analyseren voor meer informatie.

## Object-id in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s_objectID in de aangepaste code-editor van AppMeasurement en Launch

De `s_objectID` variabele is een algemene variabele, wat betekent dat deze onafhankelijk van het object Analytics tracking werkt (`s` standaard). Geldige waarden voor deze variabele kunnen elke willekeurige tekenreeks met een lengte tot 100 bytes zijn. Als deze variabele niet is gedefinieerd, gebruikt Activiteitenkaart de koppeling-URL als id voor de koppeling.

Deze variabele wordt doorgaans ingesteld in het `onClick` geval van een HTML-koppeling.

```HTML
<a href="https://example.com" onClick="s_objectID='Example identifier';">Example link</a>
```

>[!NOTE] Neem altijd de puntkomma op die een JavaScript-instructie voltooit. De puntkomma is vereist voor Activity Map aan functie.

## Gebruik hoofdletters

De `s_objectID` variabele is waardevol wanneer u een grotere nauwkeurigheid in de rapportage van de Activiteitenkaart wilt.

### Koppelingen van zeer dynamische inhoud samenvoegen

Sommige sites hebben zeer dynamische inhoud, zoals nieuwssites of winkels waar artikelen vaak worden geroteerd. Aangezien de Kaart van de Activiteit de verbinding URL als herkenningsteken door gebrek gebruikt, is het moeilijk om de meest geklikte gebieden op pagina&#39;s te begrijpen waar de verbindingen vaak veranderen. Als u de koppelingen `s_objectID` binnen deze koppelingen gebruikt, begrijpt Activity Map welke koppelingen kunnen worden samengevoegd, ongeacht de URL&#39;s waarnaar ze verwijzen.

```HTML
<a href="story1.html" onClick="s_objectID='Top left link';">Story 1</a>
<a href="story2.html" onClick="s_objectID='Top center link';">Story 2</a>
<a href="story3.html" onClick="s_objectID='Top right link';">Story 3</a>
```

Ongeacht waar de verbindingen richten of hoe vaak u deze verbindingen verandert, de Kaart van de Activiteit aggregeert gegevens die op de waarde in worden gebaseerd `s_objectID`.

### Koppelingen afzonderlijk op een pagina houden

Sommige sites hebben koppelingen die verwijzen naar dezelfde locatie op verschillende locaties. Bijvoorbeeld een koppeling naar de startpagina in zowel de kop- als voettekst op uw site. Aangezien deze koppelingen dezelfde URL hebben, worden de gegevens van Activiteitenkaart samengevoegd. U kunt ze scheiden met de `s_objectID` variabele:

```HTML
<a href="index.html" onClick="s_objectID='Header home link';">Example link in Header</a>
<a href="index.html" onClick="s_objectID='Footer home link';">Example link in Footer</a>
```

Zelfs als koppelingen naar dezelfde URL verwijzen, kan Activity Map de `s_objectID` variabele gebruiken om deze op de juiste manier te onderscheiden in de rapportage.
