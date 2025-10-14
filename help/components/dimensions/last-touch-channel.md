---
title: Laatste aanraakkanaal
description: Het meest recente marketingkanaal binnen het aflopen van de betrokkenheid van de bezoeker.
feature: Dimensions
exl-id: 62a47de5-ee1a-4394-aa63-75cdda92ba6a
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Laatste aanraakkanaal

De &quot;Laatste afmeting van het aanrakingskanaal&quot;[&#128279;](overview.md) meldt het meest recente marketing kanaal een bezoeker met tijdens de de betrokkenheidsperiode van die bezoeker (30 dagen door gebrek) aanpast. Deze dimensie is waardevol om te begrijpen welke marketing kanalen verkeer aan uw plaats drijven die in omzettingen resulteren, toestaand u om marketing inspanningen op gebieden te concentreren die het meest effectief zijn.

## Deze dimensie vullen met gegevens

Deze afmeting verwijst direct kanaalnamen die u in de [&#x200B; manager van het Kanaal van de Marketing &#x200B;](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-channels.md) hebt bepaald.

Elke hit die naar Adobe-servers voor gegevensverzameling wordt verzonden, wordt uitgevoerd via de verwerkingsregels voor marketingkanalen van uw rapportsuite. Het herhaalt door elke regel in numerieke orde tot het een gelijke vindt, waarin dat marketing kanaal aan de slag bindt. Het laatste aanraakkanaal blijft bij de bezoeker aanwezig totdat deze de site niet langer bezoekt dan de periode van de betrokkenheid van de bezoeker (standaard 30 dagen).

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Plaats het gewenste afmetingspunt als kanaal in de Manager van het Kanaal van de Marketing onder de montages van de Reeks van het Rapport.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* Het resultaat van de bezoeker op uw site moet overeenkomen met de criteria die worden beschreven in de verwerkingsregel voor marketingkanalen.

## Dimension-objecten

Dimension-items bevatten een kanaalnaam in de marketingkanaalmanager. Waarden zijn standaard `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"` en `"Referring domains"` . U kunt kanalen toevoegen of schrappen in de het kanaalmanager van de Marketing, die de waarden van deze afmeting beïnvloedt.
