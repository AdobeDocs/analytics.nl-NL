---
description: Deze sectie bevat richtlijnen voor het testen van verwerkingsregels en een lijst met veelvoorkomende fouten die moeten worden vermeden.
subtopic: Processing rules
title: Tips en trucs voor verwerkingsregels
feature: Admin Tools
uuid: e3a9ff8a-b81a-41c9-9f61-e40cb4bf7d99
exl-id: e663d98b-dcfd-4420-84ac-07ddfe55a3f2
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 2%

---

# Tips en trucs voor verwerkingsregels

Deze sectie bevat richtlijnen voor het testen van verwerkingsregels en een lijst met veelvoorkomende fouten die moeten worden vermeden.

## Regels {#section_F092D2FECDE24082AE9FC6F8BE87F29F} voor testverwerking

Deze sectie bevat sommige richtlijnen om testverwerkingsregels te helpen alvorens zij aan productie worden opgesteld.

**Testregels voor het lezen van zoektermen**

Voor om het even welke criteria die op een onderzoek worden gebaseerd, zoals als prop1 &quot;nieuws&quot;bevat, ga naar prop 1 rapport en onderzoek naar &quot;nieuws&quot;en controleer of zijn er om het even welke gelijken u niet verwachtte.

**Testregels voor het lezen van variabelen**

Maak een lege HTML-pagina op uw bureaublad, neem de s_code van uw site op en stel de variabele `s.account` in op een dev-rapportsuite. Als uw regels gebaseerd zijn op referentie, verwijzend domein, etc., neem sommige steekproef URLs van het levende verwijzersrapport, plaats `s.referrer` variabele met één van die waarden en laad de pagina. Op dezelfde manier kunt u `s.pageURL` instellen als de regel is gebaseerd op de URL-waarde van de pagina. Dit proces kan voor om het even welke variabelen worden gebruikt.

**Een Dev Report Suite gebruiken**

Wij adviseren vormend verwerkingsregels op een dev- rapportreeks om ervoor te zorgen zij correct werken. Indien mogelijk, adviseren wij het kopiëren van de regels aan een kleine reeks van het productierapport vóór brede plaatsing.

## Controleren op lege waarden {#section_EE84A5525E26415787930723B0CAAE0F}

Wanneer u een regel maakt, moet u rekening houden met het geval wanneer een waarde leeg is. Als u geen voorwaarde toevoegt die op een lege waarde controleert, kunt u per ongeluk variabelen met lege waarden overschrijven.

![](assets/tips-set-value-acquisition-code.png)

Het is ook belangrijk om de verwerkingsvolgorde in overweging te nemen. In het volgende voorbeeld wordt weergegeven dat de aangepaste eVar Vorige paginanaam wordt ingesteld op de URL als de paginanaam niet aanwezig is. De URL wordt echter in de paginanaam geplaatst nadat de verwerkingsregels zijn toegepast. In dit geval is de paginanaam dus leeg als deze niet op de pagina is ingesteld.

![](assets/tips-copy-page-name-to-evar.png)

## Overschrijven van waarden {#section_49FCCA31E31A433EA2EF5EAF91443DAF} voorkomen

In het volgende voorbeeld worden op de site twee variabelen met contextgegevens gebruikt om zoektermen vast te leggen: search_keyword en search_term. Nochtans, gebaseerd op de configuratie, wordt de search_keyword waarde altijd beschreven, zelfs als search_term leeg is.

Deze regel zou moeten worden aangepast om elke variabele van contextgegevens voor een waarde te testen alvorens de Interne Term van het Onderzoek te bevolken, en naar keuze, aaneenschakelend de twee waarden als er een gebruiksgeval voor het houden van hen allebei is.

![](assets/tips-search-keyword.png)

## Zoektermen coderen naar UTF-8 of Unicode {#section_3BBBE1FB8FEA48589362452DE51DB575}

Zoektermen die u uit een queryreeks hebt opgehaald, moeten correct zijn gecodeerd of worden niet door verwerkingsregels aangepast.

![](assets/tips-multibyte.png)

## Begint met, bevat en eindigt met {#section_80CE853244FC435B844A09EA51868D8D}

Selecteer de correcte aanpassingsvoorwaarde om de meest beperkende voorwaarde te vinden die correct aanpast. U kunt naar waarden in een rapport zoeken alvorens een regel te creëren om ervoor te zorgen er geen onbedoelde gelijken zijn. Bijvoorbeeld, zou u het Prop2 rapport moeten zoeken om alle plaatsen te vinden waar deze voorwaarde alvorens deze regel toe te laten aanpast.

![](assets/tips-startswith.png)
