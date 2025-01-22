---
title: Gegevensbronnen van transactie-id
description: Leer de algemene workflow voor het gebruik van gegevensbronnen voor transactie-id's.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
role: Admin
source-git-commit: e281d43204e1c5b10508661f04b880125fe8671c
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Gegevensbronnen van transactie-id

De gegevensbronnen van identiteitskaart van de transactie zijn een variatie op summiere gegevensbronnen die u toestaan om online en off-line gegevens samen te binden. Hiervoor is het gebruik van de variabele [`transactionID`](/help/implement/vars/page-vars/transactionid.md) in uw analytische implementatie vereist.

* Als een rij in een gegevensbronbestand een transactie-id bevat die overeenkomt met een transactie-id die al door het AppMeasurement is verzameld, worden de afmetingen en metriek aan de online hit toegevoegd.
* Als een rij in een gegevensbrondossier een transactie-identiteitskaart omvat die geen gelijke bevat, wordt de rij gelijkaardig behandeld aan summiere gegevensbronnen.

>[!NOTE]
>
>Alvorens de gegevensbronnen van identiteitskaart van de transactie te gebruiken, moet u het in [ Algemene Montages van de Rekening ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) voor de gewenste rapportreeks eerst toelaten.

Wanneer u een online treffer verzendt die een [`transactionID`](/help/implement/vars/page-vars/transactionid.md) waarde bevat, neemt de Adobe een &quot;momentopname&quot;van alle vastgestelde of voortgeduurde variabelen. Als een transactie-id wordt gevonden die via gegevensbronnen is geüpload, worden de offline- en onlinegegevens aan elkaar gekoppeld.

Gegevensbronnen van transactie-id hebben de volgende eigenschappen:

* De online gegevens moeten eerst worden verzameld en verwerkt. Als een transactie-id-gegevensbron wordt geüpload voordat een rapportsuite een hit verwerkt die overeenkomt met die transactie-id, zijn de gegevens niet gekoppeld.
* Transactie-id&#39;s die via AppMeasurement zijn verzameld, verlopen na 25 maanden.
* Gegevensbronnen die met een verlopen transactie-id zijn geüpload, worden op dezelfde manier behandeld als gegevens die zonder transactie-id zijn geüpload.
* Als dezelfde variabele in zowel de online hit als de gegevensbron van de transactie-id is opgenomen, wordt de waarde van de gegevensbron van de transactie-id gebruikt.
* Als een variabele is opgenomen in een online hit maar niet in een treffer voor een overeenkomende transactie-id-gegevensbron, blijft de online raakvariabele behouden.
* Als u dezelfde transactie-id instelt voor meerdere online treffers, wordt alleen de eerste instantie gewijzigd met gegevens uit een overeenkomende transactie-id-gegevensbron.
* Als u dezelfde transactie-id instelt op meerdere gegevensbronrijen voor dezelfde afmetingen, wordt het laatste dimensie-item gebruikt.

Bijvoorbeeld:

1. U verzendt een paginaweergave vanuit een AppMeasurement waarin:
   * `eVar1` is gelijk aan `blue`
   * `eVar2` is gelijk aan `water`
   * `events` is gelijk aan `event1`
   * `transactionID` is gelijk aan `1256`
2. Nadat de hit is verzameld en verwerkt, uploadt u een transactie-id-gegevensbron waarin:
   * `eVar1` is gelijk aan `yellow`
   * `eVar3` is gelijk aan `bird`
   * `events` is gelijk aan `event2`
   * `transactionID` is gelijk aan `1256`
3. Nadat de gevonden gegevensbronnen zijn verwerkt, geeft u een rapport weer in de werkruimte. De gegevens geven het volgende weer:
   * `eVar1` is gelijk aan `yellow`
   * `eVar2` is gelijk aan `water`
   * `eVar3` is gelijk aan `bird`
   * `events` is gelijk aan `event2`

De waarde eVar1 `blue` en `event1` zijn niet aanwezig in de rapportage, aangezien de hit van de transactie-id deze respectieve waarden overschrijdt.
