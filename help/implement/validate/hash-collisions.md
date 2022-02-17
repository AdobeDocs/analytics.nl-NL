---
title: Hash-botsingen
description: Beschrijft wat een knoeiboelbotsing is en hoe het zich kan manifesteren.
feature: Validation
exl-id: 693d5c03-4afa-4890-be4f-7dc58a1df553
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 2%

---

# Hash-botsingen

Adobe beschouwt de waarde van de eigenschap en van de eVar als koorden, zelfs als de waarde een aantal is. Soms zijn deze tekenreeksen honderden tekens lang, andere keren zijn ze kort. Als u ruimte wilt besparen, de prestaties wilt verbeteren en alles op dezelfde grootte wilt plaatsen, worden de tekenreeksen niet rechtstreeks in de verwerking gebruikt. In plaats daarvan wordt voor elke waarde een 32-bits of 64-bits hash berekend. Alle rapporten lopen op deze gehakte waarden, waar elke knoeiboel door de originele tekst wordt vervangen. Hashes verhoogt drastisch de prestaties van de rapporten van de Analyse.

Voor de meeste velden wordt de tekenreeks eerst omgezet in kleine letters (waardoor het aantal unieke waarden wordt verminderd). Waarden worden maandelijks gehasht (de eerste keer dat ze elke maand worden gezien). Van maand tot maand is er een kleine mogelijkheid dat twee unieke veranderlijke waarden aan de zelfde waarde hakken. Dit concept wordt een *hash-botsing*.

De botsingen van de as kunnen zich in het melden als volgt manifesteren:

* Als u een waarde trending en u een piek voor een maand ziet, is het waarschijnlijk dat een andere waarden voor die variabele hashed aan de zelfde waarde zoals de waarde werd u bekijkt.
* Hetzelfde geldt voor segmenten voor een bepaalde waarde.

## Voorbeeld van een hash-botsing

De waarschijnlijkheid van knoeiboelbotsingen neemt met het aantal unieke waarden in een dimensie toe. Een van de waarden die laat in de maand komen, kan bijvoorbeeld dezelfde hashwaarde krijgen als een waarde eerder in de maand. In het volgende voorbeeld kunt u uitleggen hoe dit tot gevolg kan hebben dat de resultaten van segmenten worden gewijzigd. Stel dat eVar62 op 18 februari &quot;waarde 100&quot; ontvangt. Analytics zal een lijst handhaven die als dit kan kijken:

<table id="table_6A49D1D5932E485DB2083154897E5074"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> eVar62 tekenreekswaarde </th> 
   <th colname="col2" class="entry"> Hash </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Waarde 99 </p> </td> 
   <td colname="col2"> <p> 111 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> Waarde 100</b> </p> </td> 
   <td colname="col2"> <p> <b> 123</b> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Waarde 101 </p> </td> 
   <td colname="col2"> <p> 222 </p> </td> 
  </tr> 
 </tbody> 
</table>

Als u een segment bouwt dat bezoeken zoekt waar eVar62= &quot;waarde 500&quot;, bepaalt de Analyse als &quot;waarde 500&quot;een knoeiboel bevat. Omdat &quot;waarde 500&quot;niet bestaat, keert de Analyse nul bezoeken terug. Op 23 februari ontvangt eVar62 &quot;waarde 500&quot;, en de hash daarvoor is ook 123. De tabel ziet er als volgt uit:

<table id="table_5FCF0BCDA5E740CCA266A822D9084C49"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> eVar62 tekenreekswaarde </th> 
   <th colname="col2" class="entry"> Hash </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Waarde 99 </p> </td> 
   <td colname="col2"> <p> 111 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> Waarde 100</b> </p> </td> 
   <td colname="col2"> <p> <b> 123</b> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Waarde 101 </p> </td> 
   <td colname="col2"> <p> 222 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> Waarde 500</b> </p> </td> 
   <td colname="col2"> <p> <b> 123</b> </p> </td> 
  </tr> 
 </tbody> 
</table>

Wanneer het zelfde segment opnieuw loopt, zoekt het de knoeiboel van &quot;waarde 500&quot;, vindt 123, en het rapport keert alle bezoeken terug die knoeiboel 123 bevatten. Nu zullen bezoeken die op 18 februari hebben plaatsgevonden in de resultaten worden opgenomen.

Deze situatie kan problemen veroorzaken wanneer het gebruiken van Analytics. Adobe blijft onderzoeken hoe de kans op deze hash-botsingen in de toekomst kan worden verkleind. De suggesties om deze situatie te vermijden zijn manieren te vinden om de unieke waarden tussen variabelen te verspreiden, onnodige waarden met verwerkingsregels te verwijderen, of anders het aantal waarden per variabele te verminderen.
