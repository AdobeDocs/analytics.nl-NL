---
title: Eerste aanraakkanaal
description: Het eerste marketingkanaal binnen het aflopen van de betrokkenheid van de bezoeker.
feature: Dimensions
exl-id: cca9794c-1305-4e54-aa13-809b9ebc6230
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Eerste aanraakkanaal

De &quot;Eerste aanrakingskanaal&quot;[ dimensie ](overview.md) meldt het eerste marketing kanaal een bezoeker met tijdens de de betrokkenheidsperiode van die bezoeker (30 dagen door gebrek) aanpast. Deze dimensie is waardevol om te begrijpen welke marketing kanalen aanvankelijke verkeer aan uw plaats drijven, die u toestaat om marketing inspanningen op gebieden te concentreren die het meest efficiënt zijn.

## Deze dimensie vullen met gegevens

Deze afmeting verwijst direct kanaalnamen die u in de [ manager van het Kanaal van de Marketing ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-channels.md) hebt bepaald.

Elke hit die naar Adobe-servers voor gegevensverzameling wordt verzonden, wordt uitgevoerd via de verwerkingsregels voor marketingkanalen van uw rapportsuite. Het herhaalt door elke regel in numerieke orde tot het een gelijke vindt, waarin dat marketing kanaal aan de slag bindt. Het eerste aanraakkanaal blijft bij de bezoeker aanwezig totdat deze de site niet langer bezoekt dan de periode van de betrokkenheid van de bezoeker (standaard 30 dagen).

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Plaats het gewenste afmetingspunt als kanaal in de Manager van het Kanaal van de Marketing onder de montages van de Reeks van het Rapport.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* De klap van de bezoeker aan uw plaats moet de criteria aanpassen die in de de verwerkingsregel van het Kanaal van de Marketing worden geschetst, _en_ moet de eerste marketing kanaalwaarde zijn om dit in de de betrokkenheidsperiode van de bezoeker te doen.

Als een volgende hit voldoet aan de criteria onder een ander marketingkanaal, wordt deze dimensie niet overschreven met het nieuwe marketingkanaal.

## Dimension-objecten

Dimension-items bevatten een kanaalnaam in de marketingkanaalmanager. Waarden zijn standaard `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"` en `"Referring domains"` . U kunt kanalen toevoegen of schrappen in de het kanaalmanager van de Marketing, die de waarden van deze afmeting beïnvloedt.
