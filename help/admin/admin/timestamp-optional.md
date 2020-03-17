---
description: Combineer zowel tijdstempelgegevens als gegevens zonder tijdstempel in één rapportsuite.
title: Tijdstempels optioneel
topic: Admin tools
uuid: 0fa63658-1cc2-4adc-8d51-a0662d0aa941
translation-type: tm+mt
source-git-commit: 984d6034d14cc4256d93bd4f7d1a7f01b63b71e9

---


# Tijdstempels optioneel

Combineer zowel tijdstempelgegevens als gegevens zonder tijdstempel in één rapportsuite.

Met Tijdstempels optioneel kunt u:

* Combineer tijdstempels en niet-tijdstempels gegevens in de zelfde globale rapportreeks.
* Verzend tijdstempelgegevens van een mobiele app naar een algemene rapportsuite.
* Voer een upgrade uit voor apps die offline tracering gebruiken zonder dat u een nieuwe rapportsuite hoeft te maken.

> [!IMPORTANT] Als u Tijdstempels optioneel gebruikt, moet u [s.bezoekorID](/help/implement/vars/config-vars/visitorid.md) niet instellen voor gegevens die al een tijdstempel hebben. Dit kan leiden tot gegevens buiten de bestelling en een negatief effect hebben op tijdberekeningen (zoals waarden voor de tijd die is besteed), attributie (persistentie van de eVar), het aantal bezoeken/bezoek en tekenrapporten.

> [!NOTE] Sessiegegevens waarvoor tijdstempels zijn ingeschakeld, worden maximaal 92 dagen bewaard. Dit betekent dat een bezoek/sessie 92 dagen &#39;open&#39; wordt gehouden, terwijl een extra hit - dat wil zeggen niet 30 minuten na de vorige hit (in de aanraaktijd) - nog steeds in hetzelfde bezoek/dezelfde sessie kan worden opgenomen. Alle &quot;oude&quot; treffers die buiten de bestelling worden ontvangen, zullen &quot;onbekende&quot; resultaten opleveren, aangezien een aantal factoren (segmentatie, toewijzing, vervaldatum, enz.) of deze treffers al dan niet in de rapportage worden opgenomen.

## Nieuwe rapportsets {#section_095A7CFBD280494593B9BEC1592B73A6}

* Indien gecreeerd van een malplaatje, blijft een nieuwe rapportreeks aan Facultatieve Tijdstempels in gebreke.

   (U kunt een nieuwe rapportsuite maken op basis van een sjabloon via **Beheer > Rapportagesuites > Nieuw rapport maken > Rapportsuite**.)
* Indien gekopieerd uit een bestaande rapportsuite, neemt de nieuwe rapportsuite de tijdstempelinstelling over van het origineel, waaronder:

   * **Tijdstempels niet toegestaan** (instelling s.bezoekerID wordt ondersteund)
   * **Vereiste** tijdstempels (instelling s.bezoekorID wordt niet ondersteund)
   * **Tijdstempels optioneel** (de instelling s.bezoekorID wordt ondersteund, maar niet bij treffers met een tijdstempel)

## Bestaande rapportsuites wijzigen in Tijdstempels Optioneel {#section_40BCD3B4639241DEA716F7640ED33E72}

1. Ga naar **Beheer > Rapportagesets > Instellingen bewerken > Algemeen > Tijdstempelconfiguratie**.
1. Selecteer de optie Geselecteerde rapportsuites **converteren naar Tijdstempels optioneel** .

   Hiermee wijzigt u uw rapportsuite in Tijdstempels optioneel.

> [!NOTE] Als een rapportsuite is ingesteld op **Tijdstempels optioneel**, neemt u contact op met de klantenservice van Adobe om deze instelling te wijzigen in een andere instelling.

