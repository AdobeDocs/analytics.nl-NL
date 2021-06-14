---
title: Implementeren met hardwarematige verzoeken voor afbeeldingen
description: Adobe Analytics implementeren met een HTML-afbeeldingstag (aanvraag voor een hardcoded afbeelding)
exl-id: 84247daf-c94b-456c-9824-6d4a0b3e6065
source-git-commit: de0424db27f9d1a3ce07632df8fd5e76b4d7bb4c
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Implementeren met hardwarematige verzoeken voor afbeeldingen

AppMeasurement-bibliotheken die door Adobe worden aangeboden, compileren variabelen die op de pagina aanwezig zijn en verzenden deze vervolgens als een afbeeldingsaanvraag naar Adobe. U kunt AppMeasurement-bibliotheken volledig overslaan en handmatig een afbeeldingsaanvraag naar Adobe verzenden. Deze methode vereist dat u de afbeeldingsaanvraag en queryreeks handmatig formuleert.

Deze implementatiemethode kan worden gebruikt op elk platform waarop afbeeldingen van externe bronnen worden weergegeven. Er wordt helemaal geen gebruik gemaakt van JavaScript.

>[!NOTE]
>
>Terwijl de hard-gecodeerde beeldverzoeken gemakkelijk aan opstelling zijn, zijn zij moeilijk om, over grotere projecten te zuiveren te handhaven en te schrapen. Zorg ervoor dat de verzoeken om een gehard beeld de beste optie voor u zijn alvorens te werk te gaan.

## Syntaxis verzoek afbeelding

Hier volgt een voorbeeld van een hardcoded afbeeldingsaanvraag met HTML:

```html
<img src="https://example.data.adobedc.net/b/ss/examplersid/1?AQB=1&g=http%3A%2F%2Fexample.com&pageName=Example%20hardcoded%20hit&v1=Example%20value&AQE=1"/>
```

* `https://` wijst het protocol aan. Pas het protocol dat in het beeldverzoek wordt gebruikt aan het protocol aan dat de rest van uw plaats gebruikt.
* `example.data.adobedc.net` is de waarde in de  [`trackingServer`](/help/implement/vars/config-vars/trackingserver.md) variabele.
* `/b/ss/` wordt opgenomen in alle verzoeken om afbeeldingen. Het maakt deel uit van de bestandsstructuur voor afbeeldingen die zijn opgeslagen op Adobe-gegevensverzamelingsservers.
* `examplersid` is de rapportsuite-id waarnaar u gegevens wilt verzenden. Voor veelvoudige rapportreeksen, scheidt identiteitskaarts met komma&#39;s en geen ruimten (zoals `examplersid1,examplersid2` etc.).
* `/1/` is de aanraakbron. Zie `hit_source` onder [Referentie gegevenskolom](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) in de gebruikershandleiding bij Exporteren. Hiermee bepaalt u de volgorde die cookies en andere methoden gebruiken om bezoekers te identificeren.
* Alles na het scheidingsteken van het vraagkoord (`?`) is gegevens die u in rapporten wilt omvatten. Zie [De parameters van de inzamelingsvraag van gegevens](../validate/query-parameters.md) voor de volledige lijst van parameters u in een beeldverzoek kunt omvatten.

## Verzoeken om geharde afbeeldingen in Microsoft Outlook

Aangezien de meeste e-mails op HTML zijn gebaseerd, is het mogelijk om geopende e-mailberichten te volgen en deze gegevens naar Adobe Analytics te verzenden. Houd rekening met het volgende als uw organisatie ervoor kiest deze methode te gebruiken:

* Elke e-mailrender kan een aanroepbare serveraanroep verhogen.
* Alleen e-mailclients die HTML ondersteunen en afbeeldingen toestaan, worden bijgehouden. Sommige e-mailclients, zoals Microsoft Outlook, blokkeren standaard externe afbeeldingen. Deze e-mailberichten worden pas bijgehouden wanneer de ontvanger ervoor kiest externe afbeeldingen te downloaden.

Een Outlook-e-mailbericht samenstellen dat een verzoek om een afbeelding bevat:

1. Open een HTML-editor. Als er geen HTML-editor beschikbaar is, werkt ook een teksteditor zonder opmaak.
2. Voeg in een nieuw HTML-bestand een `<img>`-tag met een hardcoderingsverzoek in in een `<body>`-tag.
3. Sla het HTML-bestand op.
4. Open Microsoft Outlook en stel een e-mailbericht samen.
5. Ga naar het lusje van het Tussenvoegsel en klik **Dossier** vastmaken. Selecteer het HTML-bestand voor de afbeeldingsaanvraag.
6. Klik op het pop-upmenu naast Invoegen en selecteer **Invoegen als tekst**. Als u zonder het pop-upmenu op de knop Invoegen klikt, wordt het HTML-bestand een bijlage die niet werkt.

Uw e-mail lijkt niet te veranderen, aangezien het beeldverzoek een 1x1 transparante pixel is. Als u de afbeeldingsaanvraag voor testdoeleinden wilt bekijken, wijzigt u het HTML-bestand zodat het een rand, extra tekst of andere inhoud bevat.

## Veelgestelde vragen

Meer informatie over veelgestelde vragen met aanvragen voor afbeeldingen met een hardcodering.

### Zijn de parameters van het vraagkoord case-sensitive?

Ja. Zorg ervoor dat de parameters van het vraagkoord precies aanpassen, of anders worden zij niet geregistreerd. `pagename` is bijvoorbeeld geen geldige parameter voor een querytekenreeks, terwijl `pageName` dat wel is.

### Kan ik spaties in het vraagkoord omvatten?

Waarden voor elk van de parameters van de queryreeks zijn URL-gecodeerd. URL-codering converteert tekens die normaal gesproken ongeldig zijn in URL&#39;s naar geldige tekens. Een spatieteken wordt bijvoorbeeld omgezet in `%20`. Zorg ervoor dat elk teken dat niet alfanumeriek is, URL-gecodeerd is. Adobe URL decodeert automatisch waarden wanneer de beeldverzoeken de servers van de gegevensinzameling bereiken.

Zie [HTML URL-coderingsreferentie](https://www.w3schools.com/tags/ref_urlencode.asp) op W3Schools voor meer informatie over hoe URL-codering werkt.

### Wat is het maximum aantal tekens dat één waarde kan bevatten?

Elke variabele heeft een andere maximumlengte. De meeste verkeersvariabelen houden tot 100 bytes, terwijl de meeste omzettingsvariabelen tot 255 bytes houden. Wanneer een afbeeldingsaanvraag gegevensverzamelingsservers bereikt, verlaagt Adobe deze waarden automatisch tot de maximale lengte.
