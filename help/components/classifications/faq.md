---
title: Veelgestelde vragen over classificaties
description: Veelgestelde vragen over classificaties.
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Veelgestelde vragen over classificaties

Veelgestelde vragen over classificaties.

## Hoe classificeer ik afmetingspunt &quot;0&quot;?

Classificatiebestanden die zijn geüpload met een sleutelwaarde of classificatiewaarde nul (`0`), resulteren in een fout. Het omvat alle waarden die slechts nul (`00`, `000`, etc.) bevatten. Er zijn verschillende methoden om dit probleem op te lossen:

* **Alternatieve waarden** implementeren: Het gebruik van een andere tekstwaarde dan `"0"` is de beste en eenvoudigste manier om dit probleem op te lossen. Wijzig bijvoorbeeld `s.campaign = "0";` de implementatie in `s.campaign = "Zero";`.

* **Verwerkingsregels** gebruiken: U kunt afmetingspunten tussen gegevensinzameling en hun opslag in een rapportreeks wijzigen. Maak de volgende verwerkingsregel:

   *Als de[dimensie]gelijk is`0`, overschrijft u de waarde van de[dimensie]met de aangepaste waarde`Zero`.*

* **Een VISTA-regel** aanvragen: Een consultant van de Diensten van de Techniek plaatst - omhoog een server-zijregel voor u tegen extra kosten. Neem contact op met de accountmanager van uw organisatie om een VISTA-regel aan te vragen.

## Kan ik de uploader gebruiken om dimensie-items te classificeren die nog niet bestaan?

Ja, *nochtans tellen het doen dit elk afmeting punt als factureerbare servervraag.*

* Dimension-objecten die al bestaan, brengen geen extra kosten met zich mee.
* Het gebruik van de builder van de classificatieregel classificeert geen niet-bestaande items en brengt daarom geen extra kosten met zich mee.
