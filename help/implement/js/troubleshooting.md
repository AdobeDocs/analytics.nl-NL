---
title: JavaScript-implementatie problemen oplossen
description: Meer informatie over algemene problemen en aanbevolen procedures voor het oplossen van problemen met uw JavaScript-implementatie.
translation-type: tm+mt
source-git-commit: ''

---


# JavaScript-implementatie problemen oplossen

Hieronder volgt een aantal redenen waarom uw organisatie problemen kan hebben met het correct opnemen van gegevens in Adobe Analytics.

## Aanhalingstekens gebruiken

De meeste variabelen die naar Adobe worden verzonden, zijn tekenreeksen. In JavaScript kunt u enkele of dubbele aanhalingstekens gebruiken.

### Aanhalingstekens mengen om een variabele te definiëren

U kunt het beste de typen aanhalingstekens die u gebruikt op dezelfde manier gebruiken. Als één enkel citaat het begin van een koord aanwijst, moet één enkel citaat worden gebruikt om het te sluiten.

Zowel `s.eVar1 = 'Value'` als `s.eVar1 = "Value"` zijn bijvoorbeeld geldig. `s.eVar1 = 'Value"` is ongeldig.

### Enkelvoudige of dubbele aanhalingstekens in een tekenreeks opnemen

Soms is het gewenst een enkel of dubbel aanhalingsteken in een tekenreeks op te nemen. U wilt bijvoorbeeld de waarde `Alex's sale` of `John the "Hunter"` in rapporten opnemen. Er zijn twee methoden om deze waarden op te nemen:

* **Gebruik het andere aanhalingsteken**: Bijvoorbeeld, `s.eVar1 = "Alex's sale"` en `s.eVar1 = 'John the "Hunter"'` zijn allebei geldig.
* **Escape-aanhalingstekens**: Gebruik een backslash om aanhalingstekens te omzeilen. Bijvoorbeeld, `s.eVar1 = 'Alex\'s sale'` en `s.eVar1 = "John the \"Hunter\""` zijn allebei geldig.

### Gebruik geen gekrulde aanhalingstekens

In sommige programma&#39;s worden neutrale aanhalingstekens (`"..."` en `'...'`) automatisch omgezet in gekrulde aanhalingstekens (`“...”` en `‘...’`). Vermijd het gebruik van documenteditors (zoals Microsoft Word) of het verzenden van codefragmenten via e-mail. Curly-aanhalingstekens kunnen niet worden gebruikt in JavaScript.

## Verwijzen naar het object Analytics

Alle variabelen die naar Adobe worden verzonden, gebruiken het object Analytics. De meeste implementaties gebruiken het `s` object. Zorg ervoor dat u bij het verwijzen naar variabelen het object Analytics opneemt in de referentie.

is bijvoorbeeld geldig, terwijl `s.eVar1 = 'Value'` `eVar1 = 'Value'` dit niet het geval is.

## Elke variabele één keer definiëren

Wanneer een trackfunctie (`s.t()`) wordt uitgevoerd, neemt AppMeasurement alle gedefinieerde variabelen en compileert deze in een afbeeldingsaanvraag. Als u een variabele meer dan eens in uw implementatie bepaalt, slechts wordt de recentste waarde gebruikt. Zorg ervoor dat alle waarden van variabelen de juiste waarde bevatten wanneer de functie track wordt uitgevoerd.

## Variabel hoofdlettergebruik corrigeren

Sommige variabelen gebruiken hoofdletters. JavaScript-variabelen zijn hoofdlettergevoelig. Zorg ervoor dat u het juiste hoofdlettergebruik gebruikt bij het definiëren van variabelen. is bijvoorbeeld geldig, terwijl `s.eVar1 = 'Value'` `s.evar1 = 'Value'` dit niet het geval is.

## Plug-ins

Sommige organisaties gebruiken insteekmodules om hun implementatie van Adobe Analytics te verbeteren. Vergeet niet om geïnstalleerde plug-ins opnieuw op te nemen wanneer u AppMeturement-versies bijwerkt. De code die in de code wordt gemaakt, bevat [!UICONTROL Code Manager] geen insteekcode. Maak een exemplaar van uw bestaande code voor het geval u aan een vorige versie van AppMeasurement moet terugkeren.

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

In dit geval wordt `document.title` de waarde &quot;Startpagina&quot; ingevuld `s.pageName`. Sommige browsers kunnen witruimte echter anders interpreteren. Het resultaat kan een van de volgende twee voorbeelden zijn:

```js
s.pageName = "Home Page";
```

```js
s.pageName = "        Home Page";
```

Deze twee variabelewaarden worden in Adobe Analytics als afzonderlijk beschouwd. De witruimte wordt echter automatisch verwijderd voor weergavedoeleinden. Het resultaat is een rapport waarin twee schijnbaar identieke regelitems voor de &quot;startpagina&quot; worden weergegeven. Controleer of de waarden van variabelen geen witruimte voor of na de gewenste waarde bevatten.
