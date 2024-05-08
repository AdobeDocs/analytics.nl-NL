---
title: Hash-botsingen
description: Beschrijft wat een knoeiboelbotsing is en hoe het zich kan manifesteren.
feature: Validation
exl-id: 693d5c03-4afa-4890-be4f-7dc58a1df553
role: Admin, Developer
source-git-commit: 06f61fa7b39faacea89149650e378c8b8863ac4f
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# Hash-botsingen

Dimensionen in Adobe Analytics verzamelen tekenreekswaarden. Soms zijn deze tekenreeksen honderden tekens lang, terwijl andere tekens kort zijn. Om de prestaties te verbeteren, worden deze tekenreekswaarden niet direct in verwerking gebruikt. In plaats daarvan wordt voor elke waarde een hash berekend om alle waarden tot een uniforme grootte te maken. Alle rapporten lopen op deze gehakte waarden, die drastisch hun prestaties verhogen.

Voor de meeste velden wordt de tekenreeks eerst omgezet in kleine letters. Bij omzetting in kleine letters wordt het aantal unieke waarden verminderd. De waarden worden maandelijks gehasht - het geval voor een bepaalde waarde gebruikt de eerste waarde die elke maand wordt gezien. Van maand tot maand, is er een kleine mogelijkheid dat twee unieke veranderlijke waarden aan de zelfde waarde hakken. Dit concept wordt een *hash-botsing*.

De botsingen van de as kunnen in rapporten als volgt manifesteren:

* Als u een rapport in tijd bekijkt en een onverwachte punt ziet, is het mogelijk dat de veelvoudige unieke waarden voor die variabele de zelfde knoeiboel gebruiken.
* Als u een segment gebruikt en een onverwachte waarde ziet, is het mogelijk dat het onverwachte afmetingspunt de zelfde knoeiboel gebruikt zoals een ander afmetingspunt dat uw segment aanpaste.

## Oneven van een hashbotsing

Adobe Analytics gebruikt 32-bits hashes voor de meeste afmetingen, wat betekent dat er 2 zijn<sup>32</sup> mogelijke hash-combinaties (ongeveer 4,3 miljard). Elke maand wordt een nieuwe hash-tabel voor elke dimensie gemaakt. De benaderende kansen om een knoeiboelbotsing te ontmoeten die op het aantal unieke waarden wordt gebaseerd zijn als volgt. Deze kansen zijn gebaseerd op één enkele dimensie voor één enkele maand.

| Unieke waarden | Oneven |
| --- | --- |
| 1.000 | 0,01% |
| 10.000 | 1% |
| 50.000 | 26% |
| 100.000 | 71% |

{style="table-layout:auto"}

Vergelijkbaar met de [verjaardagsparadox](https://en.wikipedia.org/wiki/Birthday_problem)De kans op hash-botsingen neemt aanzienlijk toe naarmate het aantal unieke waarden toeneemt. Bij 1 miljoen unieke waarden, is het waarschijnlijk dat er minstens 100 knoeiboelbotsingen voor die dimensie zijn.

## Hashbotsingen verminderen

De meeste hash-botsingen gebeuren met twee ongebruikelijke waarden, die geen betekenisvolle invloed hebben op rapporten. Zelfs als een hash een algemene en soms voorkomende waarde heeft, is het resultaat te verwaarlozen. In zeldzame gevallen waarin twee populaire waarden een hash-botsing ervaren, is het echter mogelijk het effect ervan duidelijk te zien. Adobe beveelt het volgende aan om het effect ervan in rapporten te verminderen:

* **Het datumbereik wijzigen**: Hash-tabellen worden elke maand gewijzigd. Als u het datumbereik wijzigt in een tijdsbereik van een andere maand, kan elke waarde verschillende hashes hebben die niet botsen.
* **Het aantal unieke waarden verminderen**: U kunt uw implementatie of gebruik aanpassen [Verwerkingsregels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) helpen het aantal unieke waarden dat een dimensie verzamelt, te verminderen. Als uw dimensie bijvoorbeeld een URL verzamelt, kunt u querytekenreeksen of -protocol verwijderen.

<!-- https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=OmniArch&title=Uniques -->
