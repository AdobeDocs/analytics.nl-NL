---
title: Eerste aanraakkanaal
description: Het eerste marketingkanaal binnen het aflopen van de betrokkenheid van de bezoeker.
feature: Dimensions
exl-id: cca9794c-1305-4e54-aa13-809b9ebc6230
source-git-commit: b0d264bb8128f805f5bcb194436e357eef4b6987
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Eerste aanraakkanaal

De dimensie &#39;Eerste aanraakkanaal&#39; rapporteert het eerste marketingkanaal waarmee een bezoeker tijdens de betrokkenheidsperiode van die bezoeker overeenkomt (standaard 30 dagen). Deze dimensie is waardevol om te begrijpen welke marketing kanalen aanvankelijke verkeer aan uw plaats drijven, die u toestaat om marketing inspanningen op gebieden te concentreren die het meest efficiënt zijn.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst rechtstreeks naar kanaalnamen die u in het dialoogvenster [Marketing Channel Manager](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md).

Elke hit die naar de servers van de gegevensinzameling van de Adobe wordt verzonden loopt door de verwerkingsregels van het Kanaal van de Marketing van uw rapportreeks. Het herhaalt door elke regel in numerieke orde tot het een gelijke vindt, waarin dat marketing kanaal aan de slag bindt. Het eerste aanraakkanaal blijft bij de bezoeker aanwezig totdat deze de site niet langer bezoekt dan de periode van de betrokkenheid van de bezoeker (standaard 30 dagen).

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Plaats het gewenste afmetingspunt als kanaal in de Manager van het Kanaal van de Marketing onder de montages van de Reeks van het Rapport.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* Het resultaat van de bezoeker op uw site moet overeenkomen met de criteria die worden beschreven in de verwerkingsregel voor marketingkanalen. _en_ moet de eerste waarde van het marketingkanaal zijn om dit te doen in de aanstellingsperiode van de bezoeker.

Als een volgende hit voldoet aan de criteria onder een ander marketingkanaal, wordt deze dimensie niet overschreven met het nieuwe marketingkanaal.

## Dimension-items

Dimension-items bevatten een kanaalnaam in de marketingkanaalmanager. Standaard bevatten waarden `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"`, en `"Referring domains"`. U kunt kanalen toevoegen of schrappen in de het kanaalmanager van de Marketing, die de waarden van deze afmeting beïnvloedt.
