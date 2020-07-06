---
title: maxDelay
description: Bepaal de maximumhoeveelheid tijd die AppMeasurement op een reactie van DFA wacht alvorens een beeldverzoek te verzenden.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# maxDelay

De `s.maxDelay` variabele wordt gebruikt in de DFA gegevensschakelaar om de onderbrekingsperiode te bepalen in het contacteren van de DFA gastheer. Als Adobe geen reactie van de DFA-servers ontvangt binnen de opgegeven periode die in deze variabele is ingesteld, wordt de verbinding verbroken en worden de gegevens op de normale wijze verwerkt. Neem deze variabele op in uw implementatie als u zich zorgen maakt over de responstijd van DFA op elke pagina. Adobe raadt u aan met deze waarde te experimenteren om de optimale time-outperiode te bepalen.

Deze variabele wordt alleen gebruikt in implementaties met behulp van de DFA-gegevensconnector. Zelfs bij implementaties die DFA gebruiken, is deze variabele optioneel.

## Maximale vertraging bij starten Adobe Experience Platform

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.maxDelay in de redacteur van de Code van de Meting App en van de Lancering van de douane

De `s.maxDelay` variabele is een geheel getal dat het aantal milliseconden vertegenwoordigt dat AppMeasurement wacht op een reactie van DFA. Als AppMeasurement niet tijdig een antwoord van DFA ontvangt, wordt een beeldverzoek verzonden naar Adobe zonder DFA-gegevens.

```js
s.maxDelay = 750;
```

## Eigenschappen

* Verhoog de wachttijd om meer DFA-gegevens te verzamelen, maar vergroot ook het risico op gegevensverlies bij een Analytics-hit. Analytics-raakgegevens gaan verloren wanneer de gebruiker tijdens de `s.maxDelay` periode van de pagina af navigeert.
* Als u de wachttijd verkort, loopt u minder risico dat raakgegevens van Analytics verloren gaan, maar wordt minder DFA-gegevens verzonden met raakgegevens.
* Het verliezen van DFA integratiegegevens gebeurt wanneer de `s.maxDelay` periode niet genoeg tijd voor de gastheer DFA aanpast om te antwoorden.

>[!NOTE]
>
>Adobe heeft geen controle over de responstijd van DFA. Raadpleeg de DFA-accountbeheerder van uw organisatie als u consistente problemen ziet, zelfs nadat u de maximale vertragingsperiode binnen een redelijk tijdsbestek hebt gebracht.
