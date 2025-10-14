---
title: Problemen met JavaScript-implementatie oplossen
description: Meer informatie over algemene problemen en aanbevolen procedures voor het oplossen van problemen met uw JavaScript-implementatie.
feature: Implementation Basics
exl-id: e7181e78-65bf-446d-8d5c-b47323dbec1d
role: Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Problemen met JavaScript-implementatie oplossen

Hieronder volgt een aantal redenen waarom uw organisatie problemen kan hebben met het correct ophalen van gegevens in Adobe Analytics.

## Aanhalingstekens gebruiken

De meeste variabelen die naar Adobe worden verzonden, zijn tekenreeksen. In JavaScript kunt u enkele of dubbele aanhalingstekens gebruiken.

### Aanhalingstekens mengen om een variabele te definiëren

U kunt het beste de typen aanhalingstekens die u gebruikt op dezelfde manier gebruiken. Als één enkel citaat het begin van een koord aanwijst, moet één enkel citaat worden gebruikt om het te sluiten.

Zowel `s.eVar1 = 'Value'` als `s.eVar1 = "Value"` zijn bijvoorbeeld geldig. `s.eVar1 = 'Value"` is niet geldig.

### Enkelvoudige of dubbele aanhalingstekens in een tekenreeks opnemen

Soms is het gewenst een enkel of dubbel aanhalingsteken in een tekenreeks op te nemen. U wilt bijvoorbeeld de waarde `Alex's sale` of `John the "Hunter"` in rapporten opnemen. Er zijn twee methoden om deze waarden op te nemen:

* **Gebruik het andere citaattype**: Bijvoorbeeld, `s.eVar1 = "Alex's sale"` en `s.eVar1 = 'John the "Hunter"'` zijn allebei geldig.
* **Escape aanhalingstekens**: Gebruik backslash aan vluchtaanhalingstekens. `s.eVar1 = 'Alex\'s sale'` en `s.eVar1 = "John the \"Hunter\""` zijn bijvoorbeeld allebei geldig.

### Gebruik geen gekrulde aanhalingstekens

Sommige programma&#39;s zetten neutrale aanhalingstekens (`"..."` en `'...'`) automatisch om in gekrulde aanhalingstekens (`"..."` en `'...'`). Vermijd het gebruik van documenteditors (zoals Microsoft Word) of het verzenden van codefragmenten via e-mail. Curly-aanhalingstekens kunnen niet worden gebruikt in JavaScript.

## Verwijzen naar het object Analytics

Alle variabelen die naar Adobe worden verzonden, gebruiken het object Analytics. Bij de meeste implementaties wordt het object `s` gebruikt. Zorg ervoor dat u bij het verwijzen naar variabelen het object Analytics opneemt in de referentie.

`s.eVar1 = 'Value'` is bijvoorbeeld geldig, terwijl `eVar1 = 'Value'` dat niet is.

## Elke variabele één keer definiëren

Wanneer een spoorfunctie (`s.t()`) loopt, neemt AppMeasurement alle bepaalde variabelen en compileert hen in een beeldverzoek. Als u een variabele meer dan eens in uw implementatie bepaalt, slechts wordt de recentste waarde gebruikt. Zorg ervoor dat alle waarden van variabelen de juiste waarde bevatten wanneer de functie track wordt uitgevoerd.

## Variabel hoofdlettergebruik corrigeren

Sommige variabelen gebruiken hoofdletters. JavaScript-variabelen zijn hoofdlettergevoelig. Zorg ervoor dat u het juiste hoofdlettergebruik gebruikt bij het definiëren van variabelen. `s.eVar1 = 'Value'` is bijvoorbeeld geldig, terwijl `s.evar1 = 'Value'` dat niet is.

## Plug-ins

Sommige organisaties gebruiken insteekmodules om de implementatie van Adobe Analytics te verbeteren. Vergeet niet om geïnstalleerde plug-ins opnieuw op te nemen wanneer u AppMeasurement-versies bijwerkt. De code die in [!UICONTROL Code Manager] wordt gemaakt, bevat geen insteekcode. Maak een kopie van de bestaande code voor het geval dat u naar een vorige versie van AppMeasurement moet terugkeren.

## Witruimte in variabele waarden

In HTML zijn er verschillende tekens die witruimte maken. Dit zijn een spatie, een tab en een regelterugloop (of lijnvoer). Bekijk het volgende voorbeeld:

```html
<head>
  <title>
    Home Page
  </title>
</head>
<body>
<script language="javascript">
  s.pageName = document.title;
</script>
</body>
```

In dit geval vult `document.title` `s.pageName` . Deze krijgt de waarde &quot;Startpagina&quot;. Sommige browsers kunnen witruimte echter anders interpreteren. Het resultaat kan een van de volgende twee voorbeelden zijn:

```js
s.pageName = "Home Page";
```

```js
s.pageName = "        Home Page";
```

Deze twee variabelewaarden worden in Adobe Analytics als afzonderlijk beschouwd. De witruimte wordt echter automatisch verwijderd voor weergavedoeleinden. Het resultaat is een rapport waarin twee schijnbaar identieke regelitems voor de &quot;startpagina&quot; worden weergegeven. Controleer of de waarden van variabelen geen witruimte voor of na de gewenste waarde bevatten.

## Verzoeken om afgekapte afbeelding

Implementaties die veel variabelen vullen met lange waarden, kunnen soms worden uitgevoerd in afgebroken afbeeldingsaanvragen. Sommige oudere browsers, zoals Internet Explorer, leggen een limiet van 2083 tekens op voor het aanvragen van URL&#39;s voor afbeeldingsverzoeken. Als uw organisatie met zeer lange beeldverzoeken wordt geconfronteerd, probeer het volgende:

* **gebruik de dienst van identiteitskaart van Experience Cloud**: De bibliotheken van AppMeasurement 1.4.1 en verzenden later automatisch beeldverzoeken gebruikend HTTP POST als zij te lang zijn. Gegevens die met deze methode worden verzonden, worden niet afgebroken, ongeacht de lengte. Zie [&#x200B; de dienst van identiteitskaart van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=nl-NL) voor meer informatie.
* **de verwerkingsregels van het Gebruik**: [&#x200B; de regels van de Verwerking &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md) kunnen waarden van één variabele aan een andere kopiëren. Met deze methode hoeft u niet dezelfde waarde in meerdere variabelen in te stellen. Bijvoorbeeld:

  Altijd uitvoeren:<br>
Waarde prop1 overschrijven met eVar1 <br>
Overschrijvingswaarde van eVar2 met eVar1 <br>
Waarde prop2 overschrijven met eVar1 <br>

  Stel vervolgens eVar1 in in uw implementatie:

  ```js
  s.eVar1 = "The quick brown fox jumps over the lazy dog";
  ```

* **Dynamische variabelen van het Gebruik**: Als uw implementatie vele variabelen met de zelfde waarde bevolkt, kunt u [&#x200B; dynamische variabelen &#x200B;](/help/implement/vars/page-vars/dynamic-variables.md) gebruiken om het verzoek URL te verkorten:

  ```js
  s.eVar1 = "The quick brown fox jumps over the lazy dog";
  s.eVar2 = "D=v1";
  s.prop1 = "D=v1";
  s.prop2 = "D=v1";
  ```

* **de classificaties van het Gebruik**: Als het product of de paginanamen ongebruikelijk lang zijn, kunt u een identificerende waarde of code gebruiken, dan gebruik [&#x200B; classificaties &#x200B;](/help/components/classifications/classifications-overview.md) om een vriendelijkere naam te tonen.
