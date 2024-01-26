---
title: JavaScript-implementatie problemen oplossen
description: Meer informatie over algemene problemen en aanbevolen procedures voor het oplossen van problemen met uw JavaScript-implementatie.
feature: Implementation Basics
exl-id: e7181e78-65bf-446d-8d5c-b47323dbec1d
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# JavaScript-implementatie problemen oplossen

Hieronder volgt een aantal redenen waarom uw organisatie problemen kan hebben met het correct ophalen van gegevens in Adobe Analytics.

## Aanhalingstekens gebruiken

De meeste variabelen die naar de Adobe worden verzonden, zijn tekenreeksen. In JavaScript kunt u enkele of dubbele aanhalingstekens gebruiken.

### Aanhalingstekens mengen om een variabele te definiëren

U kunt het beste de typen aanhalingstekens die u gebruikt op dezelfde manier gebruiken. Als één enkel citaat het begin van een koord aanwijst, moet één enkel citaat worden gebruikt om het te sluiten.

Bijvoorbeeld beide `s.eVar1 = 'Value'` en `s.eVar1 = "Value"` zijn beide geldig. `s.eVar1 = 'Value"` is ongeldig.

### Enkelvoudige of dubbele aanhalingstekens in een tekenreeks opnemen

Soms is het gewenst een enkel of dubbel aanhalingsteken in een tekenreeks op te nemen. U wilt bijvoorbeeld de waarde `Alex's sale` of `John the "Hunter"` in verslagen. Er zijn twee methoden om deze waarden op te nemen:

* **Het andere type aanhalingsteken gebruiken**: Bijvoorbeeld: `s.eVar1 = "Alex's sale"` en `s.eVar1 = 'John the "Hunter"'` zijn beide geldig.
* **Escape-aanhalingstekens**: Gebruik een backslash om aanhalingstekens te laten ontsnappen. Bijvoorbeeld: `s.eVar1 = 'Alex\'s sale'` en `s.eVar1 = "John the \"Hunter\""` zijn beide geldig.

### Gebruik geen gekrulde aanhalingstekens

In sommige programma&#39;s worden neutrale aanhalingstekens automatisch omgezet (`"..."` en `'...'`) tot gekrulde aanhalingstekens (`"..."` en `'...'`). Vermijd het gebruik van documenteditors (zoals Microsoft Word) of het verzenden van codefragmenten via e-mail. Curly-aanhalingstekens kunnen niet worden gebruikt in JavaScript.

## Verwijzen naar het object Analytics

Alle variabelen die naar de Adobe worden verzonden, gebruiken het object Analytics. De meeste implementaties gebruiken de `s` object. Zorg ervoor dat u bij het verwijzen naar variabelen het object Analytics opneemt in de referentie.

Bijvoorbeeld: `s.eVar1 = 'Value'` is geldig, terwijl `eVar1 = 'Value'` is niet.

## Elke variabele één keer definiëren

Wanneer een trackfunctie (`s.t()`) worden uitgevoerd, neemt AppMeasurement alle gedefinieerde variabelen en compileert deze in een afbeeldingsaanvraag. Als u een variabele meer dan eens in uw implementatie bepaalt, slechts wordt de recentste waarde gebruikt. Zorg ervoor dat alle waarden van variabelen de juiste waarde bevatten wanneer de functie track wordt uitgevoerd.

## Variabel hoofdlettergebruik corrigeren

Sommige variabelen gebruiken hoofdletters. JavaScript-variabelen zijn hoofdlettergevoelig. Zorg ervoor dat u het juiste hoofdlettergebruik gebruikt bij het definiëren van variabelen. Bijvoorbeeld: `s.eVar1 = 'Value'` is geldig, terwijl `s.evar1 = 'Value'` is niet.

## Plug-ins

Sommige organisaties gebruiken insteekmodules om de implementatie van Adobe Analytics te verbeteren. Vergeet niet om geïnstalleerde plug-ins opnieuw op te nemen wanneer u een upgrade uitvoert van de versies van het AppMeasurement. De code die in het dialoogvenster [!UICONTROL Code Manager] bevat geen plug-incode. Maak een kopie van de bestaande code voor het geval dat u naar een vorige versie van het AppMeasurement moet terugkeren.

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

In dit geval: `document.title` vullen `s.pageName`, die de waarde &#39;Startpagina&#39; krijgt. Sommige browsers kunnen witruimte echter anders interpreteren. Het resultaat kan een van de volgende twee voorbeelden zijn:

```js
s.pageName = "Home Page";
```

```js
s.pageName = "        Home Page";
```

Deze twee variabelewaarden worden in Adobe Analytics als afzonderlijk beschouwd. De witruimte wordt echter automatisch verwijderd voor weergavedoeleinden. Het resultaat is een rapport waarin twee schijnbaar identieke regelitems voor de &quot;startpagina&quot; worden weergegeven. Controleer of de waarden van variabelen geen witruimte voor of na de gewenste waarde bevatten.

## Verzoeken om afgekapte afbeelding

Implementaties die veel variabelen vullen met lange waarden, kunnen soms worden uitgevoerd in afgebroken afbeeldingsaanvragen. Sommige oudere browsers, zoals Internet Explorer, leggen een limiet van 2083 tekens op voor het aanvragen van URL&#39;s voor afbeeldingsverzoeken. Als uw organisatie met zeer lange beeldverzoeken wordt geconfronteerd, probeer het volgende:

* **De service Experience Cloud-id gebruiken**: In AppMeasurementen bibliotheken 1.4.1 en hoger worden afbeeldingsaanvragen automatisch verzonden met HTTP-POST als deze te lang zijn. Gegevens die met deze methode worden verzonden, worden niet afgebroken, ongeacht de lengte. Zie [Adobe Experience Cloud ID-service](https://experienceleague.adobe.com/docs/id-service/using/home.html) voor meer informatie .
* **Verwerkingsregels gebruiken**: [Verwerkingsregels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) U kunt waarden van de ene variabele naar de andere kopiëren. Met deze methode hoeft u niet dezelfde waarde in meerdere variabelen in te stellen. Bijvoorbeeld:

  Altijd uitvoeren:<br>
Overschrijf de waarde van prop1 met eVar1<br>
Waarde van eVar2 overschrijven met eVar1<br>
Waarde van prop2 overschrijven met eVar1<br>

  Stel vervolgens eVar1 in uw implementatie in:

  ```js
  s.eVar1 = "The quick brown fox jumps over the lazy dog";
  ```

* **Dynamische variabelen gebruiken**: Als in uw implementatie veel variabelen met dezelfde waarde worden gevuld, kunt u [dynamische variabelen](/help/implement/vars/page-vars/dynamic-variables.md) om de aanvraag-URL te verkorten:

  ```js
  s.eVar1 = "The quick brown fox jumps over the lazy dog";
  s.eVar2 = "D=v1";
  s.prop1 = "D=v1";
  s.prop2 = "D=v1";
  ```

* **Classificaties gebruiken**: Als de product- of paginanamen ongebruikelijk lang zijn, kunt u een identificatiewaarde of code gebruiken. Gebruik vervolgens [classificaties](/help/components/classifications/c-classifications.md) om een vriendelijkere naam weer te geven.
