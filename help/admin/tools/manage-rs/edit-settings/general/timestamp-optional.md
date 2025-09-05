---
description: Combineer zowel tijdstempelgegevens als gegevens zonder tijdstempel in één rapportsuite.
title: Tijdstempels optioneel
feature: Admin Tools
uuid: 0fa63658-1cc2-4adc-8d51-a0662d0aa941
exl-id: 4d64225a-5eb8-4b7b-ba13-3cdc12dd6651
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# Tijdstempels optioneel

Combineer zowel tijdstempelgegevens als gegevens zonder tijdstempel in één rapportsuite.

Tijdstempels optioneel:

* Combineer tijdstempels en niet-tijdstempels gegevens in de zelfde globale rapportreeks.
* Verzend tijdstempelgegevens van een mobiele app naar een algemene rapportsuite.
* Voer een upgrade uit voor apps die offline tracering gebruiken zonder dat u een nieuwe rapportsuite hoeft te maken.

>[!WARNING]
>
>Als u Facultatieve Tijdstempels gebruikt, plaats [ s.bezoekorID ](/help/implement/vars/config-vars/visitorid.md) op gegevens niet die reeds timestamped is. Dit kan leiden tot gegevens buiten de bestelling en een negatief effect hebben op tijdberekeningen (zoals waarden voor de tijd die is besteed), attributie (eVar persistence), het aantal bezoeken/bezoek en tekenrapporten.

>[!NOTE]
>
>Sessiegegevens waarvoor tijdstempels zijn ingeschakeld, worden maximaal 92 dagen bewaard. Dit betekent dat een bezoek/sessie 92 dagen &#39;open&#39; wordt gehouden, terwijl een extra hit - dat wil zeggen niet 30 minuten na de vorige hit (in de aanraaktijd) - nog steeds in hetzelfde bezoek/dezelfde sessie kan worden opgenomen. Alle &quot;oude&quot; treffers die buiten de bestelling worden ontvangen, zullen &quot;onbekende&quot; resultaten opleveren, aangezien een aantal factoren (segmentatie, toewijzing, vervaldatum, enz.) van invloed zijn op de vraag of deze treffers al dan niet in de rapportage worden opgenomen.

## Nieuwe rapportsets {#section_095A7CFBD280494593B9BEC1592B73A6}

* Indien gecreeerd van een malplaatje, blijft een nieuwe rapportreeks aan Facultatieve Tijdstempels in gebreke.

  (U kunt een nieuwe rapportreeks van een malplaatje bij **tot stand brengen Admin > de Reeksen van het Rapport > creëren Nieuw > de Reeks van het Rapport**.)
* Indien gekopieerd uit een bestaande rapportsuite, neemt de nieuwe rapportsuite de tijdstempelinstelling over van het origineel, waaronder:

   * **Tijdstempels niet toegestaan** (het plaatsen s.bezoekorID gesteund)
   * **vereiste Tijdstempels** (het plaatsen s.bezoekorID niet gesteund)
   * **facultatieve Tijdstempels** (het plaatsen s.bezoekorID gesteund maar niet op timestamped klappen)

## Bestaande rapportsuites wijzigen in Tijdstempels Optioneel {#section_40BCD3B4639241DEA716F7640ED33E72}

1. Ga naar **Admin > de Reeksen van het Rapport > geeft Montages > Algemeen > de Configuratie van de Chronologie uit**.
1. Selecteer de **Bekeerling geselecteerde rapportreeksen in de Facultatieve doos van Tijdstempels**.

   Hiermee wijzigt u uw rapportsuite in Tijdstempels optioneel.

>[!NOTE]
>
>Als een rapportreeks aan **Facultatieve Tijdstempels** werd geplaatst, om dit in een andere het plaatsen te veranderen, gelieve de Zorg van de Cliënt van Adobe te contacteren.
