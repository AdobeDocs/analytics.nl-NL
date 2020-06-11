---
title: Eerste aanraakkanaal
description: Het eerste marketingkanaal binnen het aflopen van de betrokkenheid van de bezoeker.
translation-type: tm+mt
source-git-commit: 2c262e5345c39a71a6a54062c607273528294b24
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---


# Eerste aanraakkanaal

De dimensie &#39;Eerste aanraakkanaal&#39; rapporteert het eerste marketingkanaal waarmee een bezoeker tijdens de betrokkenheidsperiode van die bezoeker overeenkomt (standaard 30 dagen). Deze dimensie is waardevol om te begrijpen welke marketing kanalen aanvankelijke verkeer aan uw plaats drijven, die u toestaat om marketing inspanningen op gebieden te concentreren die het meest efficiënt zijn.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst direct naar kanaalnamen die u in de manager [van het](/help/admin/admin/marketing-channels-admin.md)Kanaal van de Marketing hebt bepaald.

Elke hit die naar Adobe-servers voor gegevensverzameling wordt verzonden, wordt uitgevoerd volgens de verwerkingsregels van uw rapportsuite voor marketingkanalen. Het herhaalt door elke regel in numerieke orde tot het een gelijke vindt, waarin dat marketing kanaal aan de slag bindt. Het eerste aanraakkanaal blijft bij de bezoeker aanwezig totdat deze de site niet langer bezoekt dan de periode van de betrokkenheid van de bezoeker (standaard 30 dagen).

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Plaats de gewenste afmetingswaarde als kanaal in de Manager van het Kanaal van de Marketing onder de montages van de Reeks van het Rapport.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* De treffer van de bezoeker naar uw site moet voldoen aan de criteria die worden beschreven in de regel voor verwerking van marketingkanalen __ en moet de eerste waarde van het marketingkanaal zijn om dit te doen in de aanspreekperiode van de bezoeker.

Als een volgende hit voldoet aan de criteria onder een ander marketingkanaal, wordt deze dimensie niet overschreven met het nieuwe marketingkanaal.

## Dimensiewaarden

Tot de waarden van de afmeting behoren alle kanaalnamen in het marketingkanaalbeheer. Standaard bevatten waarden `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"`en `"Referring domains"`. U kunt kanalen toevoegen of schrappen in de het kanaalmanager van de Marketing, die de waarden van deze afmeting beïnvloedt.
