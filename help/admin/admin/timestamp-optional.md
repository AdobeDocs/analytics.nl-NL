---
description: Combineer zowel tijdstempelgegevens als gegevens zonder tijdstempel in één rapportsuite.
title: Tijdstempels optioneel
feature: Admin Tools
uuid: 0fa63658-1cc2-4adc-8d51-a0662d0aa941
exl-id: 4d64225a-5eb8-4b7b-ba13-3cdc12dd6651
source-git-commit: 3f4d8df911c076a5ea41e7295038c0625a4d7c85
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---

# Tijdstempels optioneel

Combineer zowel tijdstempelgegevens als gegevens zonder tijdstempel in één rapportsuite.

Met Tijdstempels optioneel kunt u:

* Combineer tijdstempels en niet-tijdstempels gegevens in de zelfde globale rapportreeks.
* Verzend tijdstempelgegevens van een mobiele app naar een algemene rapportsuite.
* Voer een upgrade uit voor apps die offline tracering gebruiken zonder dat u een nieuwe rapportsuite hoeft te maken.

>[!WARNING]
>
>Als u Tijdstempels optioneel gebruikt, moet u deze niet instellen [s.bezoekerID](/help/implement/vars/config-vars/visitorid.md) voor gegevens die al een tijdstempel hebben. Dit kan leiden tot gegevens buiten de bestelling en een negatief effect hebben op tijdberekeningen (zoals waarden voor de tijd die is besteed), attributie (persistentie van de eVar), het aantal bezoekers/bezoekers en tekenrapporten.

>[!NOTE]
>
>Sessiegegevens waarvoor tijdstempels zijn ingeschakeld, worden maximaal 92 dagen bewaard. Dit betekent dat een bezoek/sessie 92 dagen &#39;open&#39; wordt gehouden, terwijl een extra hit - dat wil zeggen niet 30 minuten na de vorige hit (in de aanraaktijd) - nog steeds in hetzelfde bezoek/dezelfde sessie kan worden opgenomen. Alle &quot;oude&quot; treffers die buiten de bestelling worden ontvangen, zullen &quot;onbekende&quot; resultaten opleveren, aangezien een aantal factoren (segmentatie, toewijzing, vervaldatum, enz.) of deze treffers al dan niet in de rapportage worden opgenomen.

## Nieuwe rapportsets {#section_095A7CFBD280494593B9BEC1592B73A6}

* Indien gecreeerd van een malplaatje, blijft een nieuwe rapportreeks aan Facultatieve Tijdstempels in gebreke.

   (U kunt een nieuwe rapportreeks van een malplaatje tot stand brengen bij **Admin > Report Suite > Create New > Report Suite**.)
* Indien gekopieerd uit een bestaande rapportsuite, neemt de nieuwe rapportsuite de tijdstempelinstelling over van het origineel, waaronder:

   * **Tijdstempels niet toegestaan** (instelling wordt ondersteund voor s.bezoekerID)
   * **Vereiste tijdstempels** (instelling s.bezoekerID wordt niet ondersteund)
   * **Tijdstempels optioneel** (de instelling s.bezoekerID wordt ondersteund, maar niet bij treffers met een tijdstempel)

## Bestaande rapportsuites wijzigen in Tijdstempels Optioneel {#section_40BCD3B4639241DEA716F7640ED33E72}

1. Ga naar **Beheer > Rapportageopties > Instellingen bewerken > Algemeen > Configuratie tijdstempel**.
1. Selecteer **Geselecteerde rapportsuites converteren naar tijdstempels optioneel** doos.

   Hiermee wijzigt u uw rapportsuite in Tijdstempels optioneel.

>[!NOTE]
>
>Als een rapportsuite is ingesteld op **Tijdstempels optioneel** Neem contact op met de Adobe Client Care als u deze instelling wilt wijzigen in een andere instelling.
