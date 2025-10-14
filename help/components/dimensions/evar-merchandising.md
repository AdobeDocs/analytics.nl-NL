---
title: eVar (Merchandising-dimensie)
description: Aangepaste variabelen die zijn gekoppeld aan de productdimensie.
feature: Dimensions
exl-id: a7e224c4-e8ae-4b53-8051-8b5dd43ff380
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# eVar (Merchandising)

*Deze hulppagina beschrijft hoe het verhandelen van eVars als a [&#x200B; afmeting &#x200B;](overview.md) werkt. Voor informatie over hoe te om het verhandelen eVars uit te voeren, zie [&#x200B; eVar (het verhandelen variabele) &#x200B;](/help/implement/vars/page-vars/evar-merchandising.md) in de de gebruikersgids van de Implementatie.*

Voor een gedetailleerde bespreking van hoe de handel drijvende eVars werkt, zie [&#x200B; het Merchandising Vars en product het vinden methodes &#x200B;](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/merchandising-evars.md).

Wanneer het meten van het succes van externe campagnes of externe onderzoekstermijnen, wilt u typisch één enkele waarde om krediet voor om het even welke succesgebeurtenissen te ontvangen die voorkomen. Als een klant bijvoorbeeld in een e-mailcampagne op een koppeling klikt om uw website te bezoeken, worden alle aankopen die als resultaat zijn gedaan, aan die campagne gecrediteerd.

Hoe zit het met gebeurtenissen die door intern onderzoek of door categorie doorbladeren worden gedreven wanneer een klant veelvoudige punten zoekt? Een klant zoekt bijvoorbeeld naar `"goggles"` op uw site en voegt vervolgens een paar toe aan het winkelwagentje:

![&#x200B; Voorbeeld van Goggles &#x200B;](assets/merch-example-goggles.png)

Vóór het uitchecken zoekt de klant naar `"winter coat"` en voegt vervolgens een omlaag jasje toe aan het winkelwagentje:

![&#x200B; Voorbeeld van de Hoek &#x200B;](assets/merch-example-coat.png)

Wanneer de bezoeker deze aankoop heeft voltooid, wordt interne zoekactie uitgevoerd naar `"winter coat"` waarvoor de aanschaf van een paar bril is gecrediteerd (ervan uitgaande dat de eVar de standaardtoewijzing &#39;Meest recent&#39; gebruikt). Goed voor `"winter coat"`, maar slecht voor marketingbeslissingen:

| Interne zoekterm | Ontvangsten |
|---|---|
| winterjas | $ 157 |

## Hoe merchandising-variabelen dit probleem oplossen

Door eVars te transformeren kunt u de huidige waarde van een eVar aan een product toewijzen op het moment dat een succesgebeurtenis plaatsvindt. Deze waarde blijft aan dat product gekoppeld, zelfs als later een of meer nieuwe waarden voor die specifieke eVar worden ingesteld.

Als merchandising in het vorige voorbeeld is ingeschakeld voor de eVar, is de zoekterm `"goggles"` gekoppeld aan de sneeuwgoegels en is de zoekterm `"winter coat"` gekoppeld aan het onderjasje. De handelswaar wijst inkomsten toe op productniveau, zodat ontvangt elke termijn krediet voor het bedrag van inkomsten voor het product waaraan de termijn werd geassocieerd:

| Interne zoekterm | Ontvangsten |
|---|---|
| winterjas | $ 119 |
| bril | $ 38 |

Zie [&#x200B; het Merchandising Vars &#x200B;](/help/implement/vars/page-vars/evar-merchandising.md) voor implementatieinstructies.

## Instanties van variabelen voor handelsdoeleinden

De [&#x200B; metrische instanties &#x200B;](../metrics/instances.md) wordt niet geadviseerd voor gebruik op het verhandelen van variabelen.

* Voor variabelen die worden verhandeld met productsyntaxis, worden instanties helemaal niet verhoogd.
* Voor handelswijzigingsvariabelen die de syntaxis van een conversievariabele gebruiken, worden instanties geteld telkens wanneer de eVar wordt ingesteld. Het kenmerk wordt echter aan het dimensie-item `"None"` toegewezen, tenzij alle volgende gebeurtenissen zich voordoen bij dezelfde druk:
   * De eVar voor handelsdoeleinden wordt ingesteld met een waarde.
   * De variabele `products` wordt gedefinieerd met een waarde.
   * Er wordt een bindingsgebeurtenis ingesteld.

```js
// This merchandising eVar uses conversion variable syntax, and counts an instance.
// However, if the binding event and products variable are not both set, the instance attributes to "None".
s.eVar1 = "Tower defense";

// This merchandising eVar uses product syntax, and does not count an instance.
s.products = "Games;Wizard tower;;;;eVar2=Tower defense";
```

Aangezien de meeste gevallen voor het omzetten van veranderlijke syntaxis de eVar en productvariabele op verschillende klappen vereisen, is het gebruiken van metrisch van &quot;Instanties&quot;niet realistisch.
