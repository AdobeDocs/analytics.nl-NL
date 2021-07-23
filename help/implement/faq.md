---
title: Veelgestelde vragen over implementatie
description: Veelgestelde vragen over implementatie en koppelingen naar meer informatie.
exl-id: 4bab6d51-0077-42ce-8091-f75207d4c4db
source-git-commit: 562ed0e190954b7687fa79efaf5c5c54eb202af8
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 42%

---

# Veelgestelde vragen over de implementatie van Analytics

Veelgestelde vragen over implementatie en koppelingen naar meer informatie.

## Wat is het verschil tussen de Experience Cloud-bezoekers-ID en de Analytics-bezoekers-ID?

De Identity Service wijst een unieke, permanente id toe die kan worden gedeeld tussen andere oplossingen in de Experience Cloud. De bezoekers-ID van Analytics wordt alleen gebruikt door Analytics. Adobe raadt u aan de Experience Cloud-bezoekers-ID te gebruiken in uw implementatie.

## Hoe kan ik momentopnamen van videotracering implementeren?

Zie [Audio en video meten in Adobe Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html).

## Kan een onderbreking van de service bij Adobe de prestaties beïnvloeden?

Nee. Het JavaScript-bestand wordt niet op Adobe-servers gehost, dus een Adobe-storing heeft geen invloed op uw AppMeasurement-bibliotheek. Als u tags gebruikt in Adobe Experience Platform, wordt het JavaScript-bestand gehost door Akamai of op een door uw organisatie bepaalde serverlocatie.

## Kan het verzenden van data van de browser naar Adobe-services de prestaties verminderen?

AppMeasurement maakt een afbeeldingsobject binnen de HTML-pagina en de browser vraagt het afbeeldingsobject vervolgens op bij Adobe-servers voor dataverzameling. Als de servers voor dataverzameling traag of niet antwoorden, wordt de thread waarin de aanvraag wordt behandeld, vertraagd totdat de afbeelding terugkomt of een time-out optreedt. Omdat browsers afbeeldingen met meerdere threads verwerken, heeft een Adobe-stroomstoring een minimale invloed op de laadtijd van de pagina. Hierdoor wordt één thread vastgezet terwijl de andere threads actief blijven.

## Hoe maak ik een analytische implementatie ongeldig of verwijder ik deze?

Soms zou een organisatie een implementatie wegens contractvervaldatum willen verwijderen of het aantal servervraag verminderen.

* **Implementaties met tags in Adobe Experience Platform**: U kunt de Adobe Analytics-extensie op het  [!UICONTROL Extensions] tabblad uit- of verwijderen en vervolgens publiceren.
* **Legacy AppMeasurement-implementaties**: Vervang de gehele inhoud van het  `s_code.js` bestand door de volgende coderegel:

```js
var s = new Object();
```

>[!WARNING]
>
>Niet:
>
>* Verander de rapportreeks in een ongeldige waarde, aangezien het tot onnodige lading op Adobe servers leidt.
>* Verwijder het `s_code.js`-bestand in zijn geheel, tenzij u ook alle verwijzingen naar het bestand op elke pagina verwijdert.
>* Wijzig de variabele `trackingServer` om niet naar Adobe te wijzen. AppMeasurement verzendt nog beeldverzoeken, die 404 fouten terugkeren.


## Ik stelde AppMeturement door een codeanalysator in, en het benadrukte zijn gebruik van `Math.random()` als potentieel veiligheidsrisico. Wordt `Math.random()` gebruikt met om het even welke gevoelige gegevens?

Nee. De aantallen die `Math.random()` gebruiken worden niet gebruikt om, gevoelige gegevens te maskeren te verzenden of te ontvangen. Gegevens die naar Adobe-gegevensverzamelingsservers worden verzonden, zijn afhankelijk van de beveiliging van de onderliggende HTTPS-verbinding. <!-- AN-173590 -->

AppMeturement gebruikt `Math.random()` op drie zeer belangrijke gebieden:

* **Bemonstering**: Afhankelijk van uw implementatie, kon sommige informatie voor slechts een klein percentage bezoekers aan uw plaats worden verzameld. `Math.random()` wordt gebruikt om te bepalen of een bepaalde bezoeker gegevens zou moeten verzenden. Bij de meeste implementaties wordt geen sampling gebruikt.
* **ID** terugvalbezoeker: Als de bezoeker-id niet uit cookies kan worden opgehaald, wordt een willekeurige bezoeker-id gegenereerd. Dit deel van AppMeasurement gebruikt twee vraag aan `Math.random()`.
* **Cache busting**: Aan het einde van de afbeeldingsaanvraag-URL&#39;s wordt een willekeurig getal toegevoegd om te voorkomen dat de browser in cache wordt geplaatst.
