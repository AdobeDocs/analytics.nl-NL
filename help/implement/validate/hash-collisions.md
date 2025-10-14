---
title: Hash-botsingen
description: Beschrijft wat een knoeiboelbotsing is en hoe het zich kan manifesteren.
feature: Implementation Basics
exl-id: 693d5c03-4afa-4890-be4f-7dc58a1df553
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# Hash-botsingen

Dimensies in Adobe Analytics verzamelen tekenreekswaarden. Soms zijn deze tekenreeksen honderden tekens lang, terwijl andere tekens kort zijn. Om de prestaties te verbeteren, worden deze tekenreekswaarden niet direct in verwerking gebruikt. In plaats daarvan wordt voor elke waarde een hash berekend om alle waarden tot een uniforme grootte te maken. Alle rapporten lopen op deze gehakte waarden, die drastisch hun prestaties verhogen.

Voor de meeste velden wordt de tekenreeks eerst omgezet in kleine letters. Bij omzetting in kleine letters wordt het aantal unieke waarden verminderd. De waarden worden maandelijks gehasht - het geval voor een bepaalde waarde gebruikt de eerste waarde die elke maand wordt gezien. Van maand tot maand, is er een kleine mogelijkheid dat twee unieke veranderlijke waarden aan de zelfde waarde hakken. Dit concept is gekend als botsing van de a *hash*.

De botsingen van de as kunnen in rapporten als volgt manifesteren:

* Als u een rapport in tijd bekijkt en een onverwachte punt ziet, is het mogelijk dat de veelvoudige unieke waarden voor die variabele de zelfde knoeiboel gebruiken.
* Als u een segment gebruikt en een onverwachte waarde ziet, is het mogelijk dat het onverwachte afmetingspunt de zelfde knoeiboel gebruikt zoals een ander afmetingspunt dat uw segment aanpaste.

## Oneven van een hashbotsing

Adobe Analytics gebruikt hashes met 32 bits voor de meeste afmetingen, zo betekent het dat er 2 <sup> 32 </sup> mogelijke knoeiboelcombinaties (ongeveer 4.3 miljard) zijn. Elke maand wordt een nieuwe hash-tabel voor elke dimensie gemaakt. De benaderende kansen om een knoeiboelbotsing te ontmoeten die op het aantal unieke waarden wordt gebaseerd zijn als volgt. Deze kansen zijn gebaseerd op één enkele dimensie voor één enkele maand.

| Unieke waarden | Oneven |
| --- | --- |
| 1.000 | 0,01% |
| 10.000 | 1% |
| 50.000 | 26% |
| 100.000 | 71% |

{style="table-layout:auto"}

Gelijkaardig aan de [&#x200B; verjaardagsparadox &#x200B;](https://en.wikipedia.org/wiki/Birthday_problem), neemt de waarschijnlijkheid van knoeiboelbotsingen drastisch toe aangezien het aantal unieke waarden stijgt. Bij 1 miljoen unieke waarden, is het waarschijnlijk dat er minstens 100 knoeiboelbotsingen voor die dimensie zijn.

## Hashbotsingen verminderen

De meeste hash-botsingen gebeuren met twee ongebruikelijke waarden, die geen betekenisvolle invloed hebben op rapporten. Zelfs als een hash een algemene en soms voorkomende waarde heeft, is het resultaat te verwaarlozen. In zeldzame gevallen waarin twee populaire waarden een hash-botsing ervaren, is het echter mogelijk het effect ervan duidelijk te zien. Adobe raadt het volgende aan om het effect ervan in rapporten te beperken:

* **verander de datumwaaier**: De lijsten van de knoeiboel veranderen elke maand. Als u het datumbereik wijzigt in een tijdsbereik van een andere maand, kan elke waarde verschillende hashes hebben die niet botsen.
* **Verlaag het aantal unieke waarden**: U kunt uw implementatie aanpassen of [&#x200B; de regels van de Verwerking &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md) gebruiken helpen het aantal unieke waarden verminderen die een dimensie verzamelt. Als uw dimensie bijvoorbeeld een URL verzamelt, kunt u querytekenreeksen of -protocol verwijderen.

<!-- https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=OmniArch&title=Uniques -->
