---
title: Implementeren met hardwarematige verzoeken voor afbeeldingen
description: Adobe Analytics implementeren met een HTML-afbeeldingstag (aanvraag voor een gecodeerde afbeelding)
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Implementeren met hardwarematige verzoeken voor afbeeldingen

In de door Adobe verschafte meetbibliotheken voor toepassingen worden de variabelen op de pagina gecompileerd en vervolgens als een afbeeldingsaanvraag naar Adobe verzonden. U kunt AppMeasurement-bibliotheken volledig overslaan en handmatig een afbeeldingsaanvraag naar Adobe verzenden. Deze methode vereist dat u de afbeeldingsaanvraag en queryreeks handmatig formuleert.

Deze implementatiemethode kan worden gebruikt op elk platform waarop afbeeldingen van externe bronnen worden weergegeven. Er wordt helemaal geen gebruik gemaakt van JavaScript.

>[!NOTE] Terwijl de hard-gecodeerde beeldverzoeken gemakkelijk aan opstelling zijn, zijn zij moeilijk om, over grotere projecten te zuiveren te handhaven en te schrapen. Zorg ervoor dat de verzoeken om een gehard beeld de beste optie voor u zijn alvorens te werk te gaan.

## Syntaxis verzoek afbeelding

Hier volgt een voorbeeld van een hardcoded afbeeldingsaanvraag met HTML:

```html
<img src="https://example.sc.omtrdc.net/b/ss/examplersid/1?AQB=1&g=http%3A%2F%2Fexample.com&pageName=Example%20hardcoded%20hit&v1=Example%20value&AQE=1"/>
```

* `https://` wijst het protocol aan. Pas het protocol dat in het beeldverzoek wordt gebruikt aan het protocol aan dat de rest van uw plaats gebruikt.
* `example.sc.omtrdc.net` is de waarde in de `trackingServer` variabele.
* `/b/ss/` wordt opgenomen in alle verzoeken om afbeeldingen. Het maakt deel uit van de bestandsstructuur voor afbeeldingen die zijn opgeslagen op Adobe-servers voor gegevensverzameling.
* `examplersid` is de rapportsuite-id waarnaar u gegevens wilt verzenden.
* `/1/` is de aanraakbron. Zie `hit_source` onder [Gegevens kolomverwijzing](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) in de de gebruikersgids van de Uitvoer. Hiermee bepaalt u de volgorde die cookies en andere methoden gebruiken om bezoekers te identificeren.
* Alles na het scheidingsteken voor queryreeksen (`?`) zijn gegevens die u in rapporten wilt opnemen. Zie de parameters [van de de inzamelingsvraag van](../validate/query-parameters.md) Gegevens voor de volledige lijst van parameters u in een beeldverzoek kunt omvatten.

## Veelgestelde vragen

Meer informatie over veelgestelde vragen met aanvragen voor afbeeldingen met een hardcodering.

**Zijn de parameters van het vraagkoord case-sensitive?**

Ja. Zorg ervoor dat de parameters van het vraagkoord precies aanpassen, of anders worden zij niet geregistreerd. Is bijvoorbeeld `pagename` geen geldige querytekenreeks-parameter, terwijl `pageName` wel.

**Kan ik spaties in het vraagkoord omvatten?**

Waarden voor elk van de parameters van de queryreeks zijn URL-gecodeerd. URL-codering converteert tekens die normaal gesproken ongeldig zijn in URL&#39;s naar geldige tekens. Een spatieteken wordt bijvoorbeeld omgezet in `%20`. Zorg ervoor dat elk teken dat niet alfanumeriek is, URL-gecodeerd is. De waarden worden automatisch door Adobe URL gedecodeerd wanneer afbeeldingsaanvragen gegevensverzamelingsservers bereiken.

Zie [HTML URL Encoding Reference](https://www.w3schools.com/tags/ref_urlencode.asp) on W3Schools voor meer informatie over hoe URL encoding werkt.

**Wat is het maximum aantal tekens dat één waarde kan bevatten?**

Elke variabele heeft een andere maximumlengte. De meeste verkeersvariabelen houden tot 100 bytes, terwijl de meeste omzettingsvariabelen tot 255 bytes houden. Wanneer een afbeeldingsaanvraag gegevensverzamelingsservers bereikt, worden deze waarden door Adobe automatisch ingekort tot de maximale lengte.
