---
title: Gegevensbronnen van transactie-id
description: Leer de algemene workflow voor het gebruik van gegevensbronnen voor transactie-id's.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
source-git-commit: 54c88a275b48f2b401be450ce35767ab3ea9d40b
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Gegevensbronnen van transactie-id

De gegevensbronnen van identiteitskaart van de transactie zijn een variatie op summiere gegevensbronnen die u toestaan om online en off-line gegevens samen te binden. Het vereist het gebruik van [`transactionID`](/help/implement/vars/page-vars/transactionid.md) in uw analytische implementatie.

* Als een rij in een gegevensbronbestand een transactie-id bevat die overeenkomt met een transactie-id die al door AppMeturement is verzameld, worden de afmetingen en metriek aan de online hit toegevoegd.
* Als een rij in een gegevensbrondossier een transactie-identiteitskaart omvat die geen gelijke bevat, wordt de rij gelijkaardig behandeld aan summiere gegevensbronnen.

>[!NOTE]
>
>Voordat u gegevensbronnen voor transactie-id kunt gebruiken, moet u deze eerst inschakelen in [Algemene accountinstellingen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) voor de gewenste rapportsuite.

Wanneer u een online hit verzendt die een [`transactionID`](/help/implement/vars/page-vars/transactionid.md) waarde, maakt Adobe een &quot;momentopname&quot; van alle variabelen die op dat moment zijn ingesteld of blijven bestaan. Als een transactie-id wordt gevonden die via gegevensbronnen is geüpload, worden de offline- en onlinegegevens aan elkaar gekoppeld.

Gegevensbronnen van transactie-id hebben de volgende eigenschappen:

* De online gegevens moeten eerst worden verzameld en verwerkt. Als een transactie-id-gegevensbron wordt geüpload voordat een rapportsuite een hit verwerkt die overeenkomt met die transactie-id, zijn de gegevens niet gekoppeld.
* Transactie-id&#39;s die via AppMeasurement zijn verzameld, verlopen na ongeveer 90 dagen. Neem contact op met de klantenservice van Adobe als uw organisatie een langer venster met de transactie-id nodig heeft.
* Gegevensbronnen die met een verlopen transactie-id zijn geüpload, worden op dezelfde manier behandeld als gegevens die zonder transactie-id zijn geüpload.
* Als dezelfde variabele in zowel de online hit als de gegevensbron van de transactie-id is opgenomen, wordt de waarde van de gegevensbron van de transactie-id gebruikt.
* Als een variabele is opgenomen in een online hit maar niet in een treffer voor een overeenkomende transactie-id-gegevensbron, blijft de online raakvariabele behouden.
* Als u dezelfde transactie-id instelt voor meerdere online treffers, wordt alleen de eerste instantie gewijzigd met gegevens uit een overeenkomende transactie-id-gegevensbron.
* Als u dezelfde transactie-id instelt op meerdere gegevensbronrijen voor dezelfde afmetingen, wordt het laatste dimensie-item gebruikt.

Bijvoorbeeld:

1. U verzendt in een paginamening van AppMeasurement waar:
   * `eVar1` equals `blue`
   * `eVar2` equals `water`
   * `events` equals `event1`
   * `transactionID` equals `1256`
2. Nadat de hit is verzameld en verwerkt, uploadt u een transactie-id-gegevensbron waarin:
   * `eVar1` equals `yellow`
   * `eVar3` equals `bird`
   * `events` equals `event2`
   * `transactionID` equals `1256`
3. Nadat de gevonden gegevensbronnen zijn verwerkt, geeft u een rapport weer in de werkruimte. De gegevens geven het volgende weer:
   * `eVar1` equals `yellow`
   * `eVar2` equals `water`
   * `eVar3` equals `bird`
   * `events` equals `event2`

De waarde eVar1 `blue` en de `event1` Er is geen metrische waarde in de rapportage aanwezig, aangezien de transactie-ID die respectieve waarden overschrijdt.
