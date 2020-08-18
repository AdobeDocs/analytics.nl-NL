---
title: Veelgestelde vragen over implementatie
description: Veelgestelde vragen over implementatie en koppelingen naar meer informatie.
translation-type: tm+mt
source-git-commit: b569f87dde3b9a8b323e0664d6c4d1578d410bb7
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 68%

---


# Veelgestelde vragen over de implementatie van Analytics

Veelgestelde vragen over implementatie en koppelingen naar meer informatie.

## Wat is het verschil tussen de Experience Cloud-bezoekers-ID en de Analytics-bezoekers-ID?

De Identity Service wijst een unieke, permanente id toe die kan worden gedeeld tussen andere oplossingen in de Experience Cloud. De bezoekers-ID van Analytics wordt alleen gebruikt door Analytics. Adobe raadt u aan de Experience Cloud-bezoekers-ID te gebruiken in uw implementatie.

## Hoe kan ik momentopnamen van videotracering implementeren?

Zie [Audio en video meten in Adobe Analytics](https://docs.adobe.com/content/help/nl-NL/media-analytics/using/media-overview.html).

## Kan een onderbreking van de service bij Adobe de prestaties beïnvloeden?

Nee. Het JavaScript-bestand wordt niet op Adobe-servers gehost, dus een Adobe-storing heeft geen invloed op uw AppMeasurement-bibliotheek. Als u Adobe Experience Platform Launch gebruikt, wordt het JavaScript-bestand gehost door Akamai of op een door uw organisatie bepaalde serverlocatie.

## Kan het verzenden van data van de browser naar Adobe-services de prestaties verminderen?

AppMeasurement maakt een afbeeldingsobject binnen de HTML-pagina en de browser vraagt het afbeeldingsobject vervolgens op bij Adobe-servers voor dataverzameling. Als de servers voor dataverzameling traag of niet antwoorden, wordt de thread waarin de aanvraag wordt behandeld, vertraagd totdat de afbeelding terugkomt of een time-out optreedt. Omdat browsers afbeeldingen met meerdere threads verwerken, heeft een Adobe-stroomstoring een minimale invloed op de laadtijd van de pagina. Hierdoor wordt één thread vastgezet terwijl de andere threads actief blijven.

## Hoe maak ik een analytische implementatie ongeldig of verwijder ik deze?

Soms zou een organisatie een implementatie wegens contractvervaldatum willen verwijderen of het aantal servervraag verminderen.

* **Implementaties bij starten**: Schakel de Adobe Analytics-extensie op het [!UICONTROL Extensions] tabblad uit of verwijder deze. Publiceer de extensie vervolgens.
* **Legacy AppMeasurement-implementaties**: Vervang de gehele inhoud van het `s_code.js` bestand door de volgende coderegel:

```js
var s = new Object();
```

>[!WARNING]
>
>Niet:
>
>* Verander de rapportreeks in een ongeldige waarde, aangezien het tot onnodige lading op Adobe servers leidt.
>* Verwijder het `s_code.js` bestand helemaal, tenzij u ook alle verwijzingen naar het bestand op elke pagina verwijdert.
>* Wijzig de `trackingServer` variabele om niet naar Adobe te wijzen. AppMeasurement verzendt nog beeldverzoeken, die 404 fouten terugkeren.

