---
title: maxDelay
description: Bepaal de maximumhoeveelheid tijd die AppMeasurement op een reactie van DFA wacht alvorens een beeldverzoek te verzenden.
exl-id: 154f7e34-39e7-4390-ae36-d4fbc998787f
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# maxDelay

De variabele `s.maxDelay` wordt gebruikt in de DFA gegevensschakelaar om de onderbrekingsperiode te bepalen in het contacteren van de DFA gastheer. Als Adobe geen reactie van de servers van DFA binnen de gespecificeerde periode ontvangt die in deze variabele wordt geplaatst, wordt de verbinding verbroken, en de gegevens worden verwerkt normaal. Neem deze variabele op in uw implementatie als u zich zorgen maakt over de responstijd van DFA op elke pagina. Adobe raadt u aan met deze waarde te experimenteren om de optimale time-outperiode te bepalen.

Deze variabele wordt alleen gebruikt in implementaties met behulp van de DFA-gegevensconnector. Zelfs bij implementaties die DFA gebruiken, is deze variabele optioneel.

## Maximale vertraging met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.maxDelay in AppMeasurement en aangepaste code-editor

De `s.maxDelay` variabele is een geheel dat het aantal milliseconden vertegenwoordigt AppMeasurement wacht op een reactie van DFA. Als AppMeasurement geen reactie van DFA in tijd ontvangt, wordt een beeldverzoek verzonden naar Adobe zonder DFA-gegevens.

```js
s.maxDelay = 750;
```

## Eigenschappen

* Verhoog de wachttijd om meer DFA-gegevens te verzamelen, maar vergroot ook het risico dat gegevens van Analytics worden verloren. De gegevens van de hit Analytics-gegevens gaan verloren wanneer de gebruiker tijdens de periode `s.maxDelay` weg navigeert van de pagina.
* Het verminderen van wachttijd vermindert het risico van het verliezen van Analytics klapgegevens, maar kan de hoeveelheid DFA gegevens verminderen die met klapgegevens worden verzonden.
* Het verliezen van DFA integratiegegevens gebeurt wanneer de `s.maxDelay` periode niet genoeg tijd voor de DFA gastheer aanpast om te antwoorden.

>[!NOTE]
>
>Adobe heeft geen controle over de responstijd van DFA. Raadpleeg de DFA-accountbeheerder van uw organisatie als u consistente problemen ziet, zelfs nadat u de maximale vertragingsperiode binnen een redelijk tijdsbestek hebt gebracht.
