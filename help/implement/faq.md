---
title: Veelgestelde vragen over implementatie
description: Veelgestelde vragen over implementatie en koppelingen naar meer informatie.
feature: Implementation Basics
exl-id: 4bab6d51-0077-42ce-8091-f75207d4c4db
role: Admin, Developer, Leader, User
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 33%

---

# Veelgestelde vragen over de implementatie van Analytics

Veelgestelde vragen over implementatie en koppelingen naar meer informatie.

## Wat is het verschil tussen de bezoeker-id van het Experience Cloud en de bezoeker-id van Analytics?

De Identity Service wijst een unieke, permanente id toe die kan worden gedeeld tussen andere oplossingen in de Experience Cloud. De bezoekers-ID van Analytics wordt alleen gebruikt door Analytics. Adobe raadt u aan de Experience Cloud-bezoekers-ID te gebruiken in uw implementatie.

## Hoe kan ik hartslagvideo bijhouden implementeren?

Zie [Audio en video meten in Adobe Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html).

## Kan een de dienstonderbreking bij Adobe prestaties beïnvloeden?

Nee. Het JavaScript-bestand wordt niet op Adobe-servers gehost, dus een Adobe-storing heeft geen invloed op uw AppMeasurement-bibliotheek. Als u tags gebruikt in Adobe Experience Platform, wordt het JavaScript-bestand gehost door Akamai of op een door uw organisatie bepaalde serverlocatie.

## Kan het verzenden van gegevens van de browser naar Adobe-services de prestaties verminderen?

AppMeasurement maakt een afbeeldingsobject binnen de HTML-pagina en de browser vraagt het afbeeldingsobject vervolgens op bij Adobe-servers voor dataverzameling. Als de servers voor dataverzameling traag of niet antwoorden, wordt de thread waarin de aanvraag wordt behandeld, vertraagd totdat de afbeelding terugkomt of een time-out optreedt. Omdat browsers afbeeldingen met meerdere threads verwerken, heeft een Adobe-stroomstoring een minimale invloed op de laadtijd van de pagina. Hierdoor wordt één thread vastgezet terwijl de andere threads actief blijven.

## Hoe maak ik een analytische implementatie ongeldig of verwijder ik deze?

Soms zou een organisatie een implementatie wegens contractvervaldatum willen verwijderen of het aantal servervraag verminderen.

* **Implementaties met Adobe Experience Platform-gegevensverzameling**: Schakel de toepasselijke extensie Adobe Analytics, Web SDK of Mobile SDK uit of verwijder deze in het dialoogvenster [!UICONTROL Extensions] te publiceren.
* **Implementaties van verouderde AppMeasurementen**: Vervang de gehele inhoud van uw `s_code.js` bestand met de volgende coderegel:

```js
var s = new Object();
```

>[!WARNING]
>
>Niet:
>
>* Wijzig de rapportsuite in een ongeldige waarde, omdat deze onnodige belasting veroorzaakt op de servers van de Adobe.
>* Verwijder de `s_code.js` , tenzij u ook alle verwijzingen naar het bestand op elke pagina verwijdert.
>* Wijzig de `trackingServer` variabele om niet naar Adobe te wijzen. AppMeasurement verzendt nog beeldverzoeken, die 404 fouten terugkeren.

## Ik voerde AppMeasurement door een codesanalist en het markeerde zijn gebruik van `Math.random()` als een potentieel veiligheidsrisico. Is `Math.random()` gebruikt met gevoelige gegevens?

Nee. De gebruikte getallen `Math.random()` niet worden gebruikt om gevoelige gegevens te maskeren, te verzenden of te ontvangen. Gegevens die naar Adobe gegevensverzamelingsservers worden verzonden, zijn afhankelijk van de beveiliging van de onderliggende HTTPS-verbinding. <!-- AN-173590 -->

AppMeasurement gebruikt `Math.random()` op drie belangrijke gebieden :

* **Bemonstering**: Afhankelijk van uw implementatie, zou sommige informatie voor slechts een klein percentage bezoekers aan uw plaats kunnen worden verzameld. `Math.random()` wordt gebruikt om te bepalen of een bepaalde bezoeker gegevens zou moeten verzenden. Bij de meeste implementaties wordt geen sampling gebruikt.
* **ID terugvalbezoeker**: Als de bezoeker-id niet uit cookies kan worden opgehaald, wordt een willekeurige bezoeker-id gegenereerd. Dit deel van AppMeasurement gebruikt twee vraag aan `Math.random()`.
* **Cache busting**: Aan het einde van de afbeeldingsaanvraag-URL&#39;s wordt een willekeurig getal toegevoegd om te voorkomen dat de browser in cache wordt geplaatst.
