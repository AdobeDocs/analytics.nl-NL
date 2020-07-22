---
title: Laatste aanraakkanaal
description: Het meest recente marketingkanaal binnen het aflopen van de betrokkenheid van de bezoeker.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# Laatste aanraakkanaal

De afmeting &#39;Laatste aanraakkanaal&#39; rapporteert het meest recente marketingkanaal waarmee een bezoeker tijdens de betrokkenheidsperiode van die bezoeker overeenkomt (standaard 30 dagen). Deze dimensie is waardevol om te begrijpen welke marketing kanalen verkeer aan uw plaats drijven die in omzettingen resulteren, toestaand u om marketing inspanningen op gebieden te concentreren die het meest effectief zijn.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst direct naar kanaalnamen die u in de manager [van het](/help/admin/admin/marketing-channels-admin.md)Kanaal van de Marketing hebt bepaald.

Elke hit die naar Adobe-servers voor gegevensverzameling wordt verzonden, wordt uitgevoerd volgens de verwerkingsregels van uw rapportsuite voor marketingkanalen. Het herhaalt door elke regel in numerieke orde tot het een gelijke vindt, waarin dat marketing kanaal aan de slag bindt. Het laatste aanraakkanaal blijft bij de bezoeker aanwezig totdat deze de site niet langer bezoekt dan de periode van de betrokkenheid van de bezoeker (standaard 30 dagen).

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Plaats het gewenste afmetingspunt als kanaal in de Manager van het Kanaal van de Marketing onder de montages van de Reeks van het Rapport.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* Het resultaat van de bezoeker op uw site moet overeenkomen met de criteria die worden beschreven in de verwerkingsregel voor marketingkanalen.

## Dimensie-items

Dimensie-items bevatten elke kanaalnaam in het marketingkanaalbeheer. Standaard bevatten waarden `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"`en `"Referring domains"`. U kunt kanalen toevoegen of schrappen in de het kanaalmanager van de Marketing, die de waarden van deze afmeting beïnvloedt.
