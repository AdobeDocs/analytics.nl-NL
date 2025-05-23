---
title: eVar (dimensie Verkoop)
description: Aangepaste variabelen die zijn gekoppeld aan de productdimensie.
feature: Dimensions
exl-id: a7e224c4-e8ae-4b53-8051-8b5dd43ff380
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---

# eVar (merchandising)

*In deze Help-pagina wordt beschreven hoe eVars als een [dimensie](overview.md). Voor informatie over hoe te om koopwaar uit te voeren, zie [eVar (variabele voor handelsdoeleinden)](/help/implement/vars/page-vars/evar-merchandising.md) in de gebruikershandleiding bij Implementatie.*

Zie voor een gedetailleerde discussie over de werking van eVars op handelsgebied [Verkoop- en productzoekmethoden](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/merchandising-evars.html?lang=nl-NL).

Wanneer het meten van het succes van externe campagnes of externe onderzoekstermijnen, wilt u typisch één enkele waarde om krediet voor om het even welke succesgebeurtenissen te ontvangen die voorkomen. Als een klant bijvoorbeeld in een e-mailcampagne op een koppeling klikt om uw website te bezoeken, worden alle aankopen die als resultaat zijn gedaan, aan die campagne gecrediteerd.

Hoe zit het met gebeurtenissen die door intern onderzoek of door categorie doorbladeren worden gedreven wanneer een klant veelvoudige punten zoekt? Een klant zoekt bijvoorbeeld op uw site naar `"goggles"`voegt vervolgens een paar aan hun winkelwagentje toe:

![Voorbeeld van Goggles](assets/merch-example-goggles.png)

Voor afhandeling zoekt de klant naar `"winter coat"`en voegt vervolgens een omlaag jasje toe aan het winkelwagentje:

![Coatingvoorbeeld](assets/merch-example-coat.png)

Wanneer de bezoeker deze aankoop heeft voltooid, wordt een interne zoekopdracht uitgevoerd naar `"winter coat"` gecrediteerd met de aankoop van een paar goggles (ervan uitgaande dat de eVar de standaardtoewijzing van &#39;Meest recent&#39; gebruikt). Goed voor `"winter coat"`, maar slecht voor marketingbeslissingen:

| Interne zoekterm | Omzet |
|---|---|
| winterjas | $157 |

## Hoe merchandising-variabelen dit probleem oplossen

Met de optie Verwisselingsmarkeringen kunt u de huidige waarde van een eVar aan een product toewijzen op het moment dat een succesgebeurtenis plaatsvindt. Deze waarde blijft aan dat product gekoppeld, zelfs als later een of meer nieuwe waarden voor die specifieke eVar worden ingesteld.

Als de merchandising voor de eVar in het vorige voorbeeld wordt toegelaten, de onderzoekstermijn `"goggles"` is gekoppeld aan de sneeuwgoegels en de zoekterm `"winter coat"` is gebonden aan het onderjasje. De handelswaar wijst inkomsten toe op productniveau, zodat ontvangt elke termijn krediet voor het bedrag van inkomsten voor het product waaraan de termijn werd geassocieerd:

| Interne zoekterm | Omzet |
|---|---|
| winterjas | $119 |
| bril | $38 |

Zie [Merchandising Vars](/help/implement/vars/page-vars/evar-merchandising.md) voor uitvoeringsinstructies.

## Instanties van merchandisingvariabelen

De [Instanties](../metrics/instances.md) Metrisch wordt niet aangeraden voor het gebruik van variabelen voor handelsdoeleinden.

* Voor variabelen die worden verhandeld met productsyntaxis, worden instanties helemaal niet verhoogd.
* Voor handelswijzigingsvariabelen die de syntaxis van een conversievariabele gebruiken, worden instanties geteld telkens wanneer de eVar wordt ingesteld. Nochtans, kenmerkt het aan het afmetingspunt `"None"` tenzij alle volgende situaties zich voordoen bij dezelfde hit:
   * De eVar merchandising wordt ingesteld met een waarde.
   * De `products` variabele wordt gedefinieerd met een waarde.
   * Er wordt een bindingsgebeurtenis ingesteld.

```js
// This merchandising eVar uses conversion variable syntax, and counts an instance.
// However, if the binding event and products variable are not both set, the instance attributes to "None".
s.eVar1 = "Tower defense";

// This merchandising eVar uses product syntax, and does not count an instance.
s.products = "Games;Wizard tower;;;;eVar2=Tower defense";
```

Aangezien de meeste gebruiksgevallen voor het omzetten van veranderlijke syntaxis de eVar en productvariabele op verschillende klappen vereisen, is het gebruiken van metrisch van &quot;Instanties&quot;niet realistisch.
