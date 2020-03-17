---
description: 'null'
keywords: Analytics Implementation
title: Overzicht van variabelen voor handelsdoeleinden
topic: Developer and implementation
uuid: 2ccf516a-a7ee-48ab-92aa-414228a4102f
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Overzicht van variabelen voor handelsdoeleinden

Wanneer het meten van het succes van externe campagnes of externe onderzoekstermijnen, wilt u typisch één enkele waarde om krediet voor om het even welke succesgebeurtenissen te ontvangen die voorkomen. Als een klant bijvoorbeeld in een e-mailcampagne op een koppeling klikt om uw website te bezoeken, worden alle aankopen die als resultaat zijn gedaan, aan die campagne gecrediteerd.

Maar wat met gebeurtenissen die door intern onderzoek of door categorie doorbladeren worden gedreven wanneer een klant veelvoudige punten zoekt? Een klant zoekt bijvoorbeeld op uw site naar &quot;goggles&quot; en voegt vervolgens een paar aan het winkelwagentje toe:

![](assets/merch-example-goggles.png)

Vóór het afrekenen zoekt de klant naar &quot;winterjas&quot; en voegt vervolgens een omlaag jasje toe aan het winkelwagentje:

![](assets/merch-example-coat.png)

Wanneer deze aankoop is voltooid, ervan uitgaande dat de toewijzing niet is gewijzigd ten opzichte van Recentste, wordt een interne zoekopdracht naar &quot;winterjas&quot; uitgevoerd die is gecrediteerd voor de aankoop van een paar bril. Goed voor &quot;winterjas&quot;, maar slecht voor marketingbeslissingen:

| Interne zoekterm | Ontvangsten |
|---|---|
| winterjas | $157 |

**Hoe merchandising-variabelen dit probleem oplossen**

Met de handelsvariabelen voor verschillende categorieën, of &#39;merchandising evars&#39;, kunt u de huidige waarde van een eVar toewijzen aan een product op het moment dat een succesgebeurtenis plaatsvindt. Deze waarde blijft aan dat product gekoppeld, zelfs als een of meer nieuwe waarden later voor dat specifieke eVar worden ingesteld.

Als merchandising is ingeschakeld voor de eVar in het vorige voorbeeld, is de zoekterm &quot;goggles&quot; gekoppeld aan de Fernie Snow Goggles en is de zoekterm &quot;winterjas&quot; gekoppeld aan de El Gordo Down Jacket. Handelsvariabelen wijzen ontvangsten toe op productniveau, zodat elke termijn kredieten ontvangt voor het bedrag aan inkomsten van het product waarop de term betrekking had:

| Interne zoekterm | Ontvangsten |
|---|---|
| winterjas | $119 |
| bril | $38 |

