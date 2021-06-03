---
title: JavaScript-implementatie problemen oplossen
description: Meer informatie over algemene problemen en aanbevolen procedures voor het oplossen van problemen met uw JavaScript-implementatie.
exl-id: e7181e78-65bf-446d-8d5c-b47323dbec1d
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# JavaScript-implementatie problemen oplossen

Hieronder volgt een aantal redenen waarom uw organisatie problemen kan hebben met het correct ophalen van gegevens in Adobe Analytics.

## Aanhalingstekens gebruiken

De meeste variabelen die naar Adobe worden verzonden, zijn tekenreeksen. In JavaScript kunt u enkele of dubbele aanhalingstekens gebruiken.

### Aanhalingstekens mengen om een variabele te definiëren

U kunt het beste de typen aanhalingstekens die u gebruikt op dezelfde manier gebruiken. Als één enkel citaat het begin van een koord aanwijst, moet één enkel citaat worden gebruikt om het te sluiten.

Zowel `s.eVar1 = 'Value'` als `s.eVar1 = "Value"` zijn bijvoorbeeld geldig. `s.eVar1 = 'Value"` is ongeldig.

### Enkelvoudige of dubbele aanhalingstekens in een tekenreeks opnemen

Soms is het gewenst een enkel of dubbel aanhalingsteken in een tekenreeks op te nemen. U wilt bijvoorbeeld de waarde `Alex's sale` of `John the "Hunter"` in rapporten opnemen. Er zijn twee methoden om deze waarden op te nemen:

* **Gebruik het andere aanhalingsteken**: Bijvoorbeeld,  `s.eVar1 = "Alex's sale"` en  `s.eVar1 = 'John the "Hunter"'` zijn allebei geldig.
* **Escape-aanhalingstekens**: Gebruik een backslash om aanhalingstekens te omzeilen. `s.eVar1 = 'Alex\'s sale'` en `s.eVar1 = "John the \"Hunter\""` zijn bijvoorbeeld beide geldig.

### Gebruik geen gekrulde aanhalingstekens

In sommige programma&#39;s worden neutrale aanhalingstekens (`"..."` en `'...'`) automatisch omgezet in gekrulde aanhalingstekens (`“...”` en `‘...’`). Vermijd het gebruik van documenteditors (zoals Microsoft Word) of het verzenden van codefragmenten via e-mail. Curly-aanhalingstekens kunnen niet worden gebruikt in JavaScript.

## Verwijzen naar het object Analytics

Alle variabelen die naar Adobe worden verzonden, gebruiken het object Analytics. De meeste implementaties gebruiken het `s` voorwerp. Zorg ervoor dat u bij het verwijzen naar variabelen het object Analytics opneemt in de referentie.

`s.eVar1 = 'Value'` is bijvoorbeeld geldig, `eVar1 = 'Value'` niet.

## Elke variabele één keer definiëren

Wanneer een spoorfunctie (`s.t()`) loopt, neemt AppMeasurement alle bepaalde variabelen en compileert hen in een beeldverzoek. Als u een variabele meer dan eens in uw implementatie bepaalt, slechts wordt de recentste waarde gebruikt. Zorg ervoor dat alle waarden van variabelen de juiste waarde bevatten wanneer de functie track wordt uitgevoerd.

## Variabel hoofdlettergebruik corrigeren

Sommige variabelen gebruiken hoofdletters. JavaScript-variabelen zijn hoofdlettergevoelig. Zorg ervoor dat u het juiste hoofdlettergebruik gebruikt bij het definiëren van variabelen. `s.eVar1 = 'Value'` is bijvoorbeeld geldig, `s.evar1 = 'Value'` niet.

## Plug-ins

Sommige organisaties gebruiken insteekmodules om de implementatie van Adobe Analytics te verbeteren. Vergeet niet om geïnstalleerde plug-ins opnieuw op te nemen wanneer u AppMeturement-versies bijwerkt. De code die in [!UICONTROL Code Manager] wordt gecreeerd heeft geen stop-in code met het. Maak een exemplaar van uw bestaande code voor het geval u aan een vorige versie van AppMeasurement moet terugkeren.

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

In dit geval wordt `document.title` `s.pageName` gevuld en krijgt deze de waarde &quot;Startpagina&quot;. Sommige browsers kunnen witruimte echter anders interpreteren. Het resultaat kan een van de volgende twee voorbeelden zijn:

```js
s.pageName = "Home Page";
```

```js
s.pageName = "        Home Page";
```

Deze twee variabelewaarden worden in Adobe Analytics als afzonderlijk beschouwd. De witruimte wordt echter automatisch verwijderd voor weergavedoeleinden. Het resultaat is een rapport waarin twee schijnbaar identieke regelitems voor de &quot;startpagina&quot; worden weergegeven. Controleer of de waarden van variabelen geen witruimte voor of na de gewenste waarde bevatten.

## Verzoeken om afgekapte afbeelding

Implementaties die veel variabelen vullen met lange waarden, kunnen soms worden uitgevoerd in afgebroken afbeeldingsaanvragen. Sommige oudere browsers, zoals Internet Explorer, leggen een limiet van 2083 tekens op voor het aanvragen van URL&#39;s voor afbeeldingen. Als uw organisatie met zeer lange beeldverzoeken wordt geconfronteerd, probeer het volgende:

* **Gebruik de Experience Cloud ID-service**: In AppMeasurement-bibliotheken 1.4.1 en hoger worden afbeeldingsaanvragen automatisch verzonden met HTTP-POST als deze te lang zijn. Gegevens die met deze methode worden verzonden, worden niet afgebroken, ongeacht de lengte. Zie [Adobe Experience Cloud ID service](https://experienceleague.adobe.com/docs/id-service/using/home.html) voor meer informatie.
* **Verwerkingsregels** gebruiken:  [Met ](/help/admin/admin/c-processing-rules/processing-rules.md) verwerkingslinialen kunt u waarden van de ene variabele naar de andere kopiëren. Met deze methode hoeft u niet dezelfde waarde in meerdere variabelen in te stellen. Bijvoorbeeld:

   Altijd uitvoeren:<br>
Overschrijf de waarde van prop1 met eVar1<br>
Waarde van eVar2 overschrijven met eVar1<br>
Waarde van prop2 overschrijven met eVar1<br>

   Stel vervolgens eVar1 in in uw implementatie:

   ```js
   s.eVar1 = "The quick brown fox jumps over the lazy dog";
   ```

* **Dynamische variabelen** gebruiken: Als in uw implementatie veel variabelen met dezelfde waarde worden gevuld, kunt u de aanvraag-URL verkorten met behulp van  [dynamische ](/help/implement/vars/page-vars/dynamic-variables.md) variabelen:

   ```js
   s.eVar1 = "The quick brown fox jumps over the lazy dog";
   s.eVar2 = "D=v1";
   s.prop1 = "D=v1";
   s.prop2 = "D=v1";
   ```

* **Classificaties** gebruiken: Als de product- of paginanamen ongebruikelijk lang zijn, kunt u een identificerende waarde of code gebruiken, dan  [](/help/components/classifications/c-classifications.md) classificaties gebruiken om een vriendelijkere naam te tonen.
