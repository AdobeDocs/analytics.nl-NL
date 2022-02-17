---
title: Laatste aanraakkanaal
description: Het meest recente marketingkanaal binnen het aflopen van de betrokkenheid van de bezoeker.
feature: Dimensions
exl-id: 62a47de5-ee1a-4394-aa63-75cdda92ba6a
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Laatste aanraakkanaal

De afmeting &#39;Laatste aanraakkanaal&#39; rapporteert het meest recente marketingkanaal waarmee een bezoeker tijdens de betrokkenheidsperiode van die bezoeker overeenkomt (standaard 30 dagen). Deze dimensie is waardevol om te begrijpen welke marketing kanalen verkeer aan uw plaats drijven die in omzettingen resulteren, toestaand u om marketing inspanningen op gebieden te concentreren die het meest effectief zijn.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst rechtstreeks naar kanaalnamen die u in het dialoogvenster [Marketing Channel Manager](/help/admin/admin/marketing-channels-admin.md).

Elke hit die naar de servers van de gegevensinzameling van de Adobe wordt verzonden loopt door de verwerkingsregels van het Kanaal van de Marketing van uw rapportreeks. Het herhaalt door elke regel in numerieke orde tot het een gelijke vindt, waarin dat marketing kanaal aan de slag bindt. Het laatste aanraakkanaal blijft bij de bezoeker aanwezig totdat deze de site niet langer bezoekt dan de periode van de betrokkenheid van de bezoeker (standaard 30 dagen).

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Plaats het gewenste afmetingspunt als kanaal in de Manager van het Kanaal van de Marketing onder de montages van de Reeks van het Rapport.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* Het resultaat van de bezoeker op uw site moet overeenkomen met de criteria die worden beschreven in de verwerkingsregel voor marketingkanalen.

## Dimension-items

Dimension-items bevatten een kanaalnaam in de marketingkanaalmanager. Standaard bevatten waarden `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"`, en `"Referring domains"`. U kunt kanalen toevoegen of schrappen in de het kanaalmanager van de Marketing, die de waarden van deze afmeting beïnvloedt.
