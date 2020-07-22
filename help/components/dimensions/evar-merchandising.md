---
title: eVar (Merchandising)
description: Aangepaste variabelen die zijn gekoppeld aan de productdimensie.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 2%

---


# eVar (Merchandising)

*Deze Help-pagina beschrijft hoe merchandising eVars werkt als een dimensie. Raadpleeg[Vars](/help/implement/vars/page-vars/evar.md)in de gebruikershandleiding Implementeren voor informatie over het implementeren van merchandising-eVars.*

Wanneer het meten van het succes van externe campagnes of externe onderzoekstermijnen, wilt u typisch één enkele waarde om krediet voor om het even welke succesgebeurtenissen te ontvangen die voorkomen. Als een klant bijvoorbeeld in een e-mailcampagne op een koppeling klikt om uw website te bezoeken, worden alle aankopen die als resultaat zijn gedaan, aan die campagne gecrediteerd.

Hoe zit het met gebeurtenissen die door intern onderzoek of door categorie doorbladeren worden gedreven wanneer een klant veelvoudige punten zoekt? Een klant zoekt bijvoorbeeld naar uw site `"goggles"`en voegt vervolgens een paar toe aan het winkelwagentje:

![Voorbeeld van Goggles](assets/merch-example-goggles.png)

Vóór controle, zoekt de klant naar `"winter coat"`, dan voegt een benedenjasje aan hun kar toe:

![Coatingvoorbeeld](assets/merch-example-coat.png)

Wanneer de bezoeker deze aankoop heeft voltooid, wordt intern gezocht naar `"winter coat"` gecrediteerd bij de aankoop van een paar bril (ervan uitgaande dat de Var de standaardtoewijzing &#39;Meest recent&#39; gebruikt). Goed voor `"winter coat"`, maar slecht voor marketing besluiten:

| Interne zoekterm | Omzet |
|---|---|
| winterjas | $157 |

## Hoe merchandising-variabelen dit probleem oplossen

Door eVars te verwisselen kunt u de huidige waarde van een eVar aan een product toewijzen op het moment dat een succesgebeurtenis plaatsvindt. Deze waarde blijft aan dat product gekoppeld, zelfs als een of meer nieuwe waarden later voor dat specifieke eVar worden ingesteld.

Als de merchandising voor eVar in het vorige voorbeeld wordt toegelaten, `"goggles"` is de onderzoekstermijn gebonden aan de sneeuwknevels, en de onderzoekstermijn `"winter coat"` is gebonden aan het benedenjasje. De handelswaar wijst inkomsten toe op productniveau, zodat ontvangt elke termijn krediet voor het bedrag van inkomsten voor het product waaraan de termijn werd geassocieerd:

| Interne zoekterm | Omzet |
|---|---|
| winterjas | $119 |
| bril | $38 |

Zie [Verwisselingsvariabelen](/help/implement/vars/page-vars/evar-merchandising.md) voor implementatieinstructies.

## Instanties van merchandisingvariabelen

De metrische waarde [Instanties](../metrics/instances.md) wordt niet aanbevolen voor het gebruik op variabelen voor handelsdoeleinden.

* Voor variabelen die worden verhandeld met productsyntaxis, worden instanties helemaal niet verhoogd.
* Voor variabelen die worden verhandeld met de syntaxis van de conversievariabele, worden instanties geteld telkens wanneer de variabele wordt ingesteld. Het kenmerk wordt echter toegewezen aan het dimensie-item, `"None"` tenzij alle volgende gebeurtenissen zich voordoen bij hetzelfde resultaat:
   * De merchandising-variabele wordt ingesteld met een waarde.
   * De `products` variabele wordt gedefinieerd met een waarde.
   * Er wordt een bindingsgebeurtenis ingesteld.

```js
// This merchandising eVar uses conversion variable syntax, and counts an instance.
// However, if the binding event and products variable are not both set, the instance attributes to "None".
s.eVar1 = "Tower defense";

// This merchandising eVar uses product syntax, and does not count an instance.
s.products = "Games;Wizard tower;;;;eVar2=Tower defense";
```

Aangezien de meeste gebruiksgevallen voor de syntaxis van conversievariabelen de variabele eVar en producten op verschillende treffers vereisen, is het gebruiken van metrisch van &quot;Instanties&quot;niet realistisch.
