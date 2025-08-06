---
title: Gegevensbronnen van transactie-id
description: Leer de algemene workflow voor het gebruik van gegevensbronnen voor transactie-id's.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
role: Admin
source-git-commit: 1d905aa47b4573a35012d56c0cf70fbc944bc972
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Gegevensbronnen van transactie-id

De gegevensbronnen van identiteitskaart van de transactie zijn een variatie op summiere gegevensbronnen die u toestaan om online en off-line gegevens samen te binden. Hiervoor is het gebruik van de variabele [`transactionID`](/help/implement/vars/page-vars/transactionid.md) in uw analytische implementatie vereist.

* Als een rij in een gegevensbronbestand een transactie-id bevat die overeenkomt met een transactie-id die al door AppMeasurement is verzameld, worden de afmetingen en metriek aan de online hit toegevoegd.
* Als een rij in een gegevensbrondossier een transactie-identiteitskaart omvat die geen gelijke bevat, wordt de rij gelijkaardig behandeld aan summiere gegevensbronnen.

>[!NOTE]
>
>Alvorens de gegevensbronnen van identiteitskaart van de transactie te gebruiken, moet u het in [ Algemene Montages van de Rekening ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) voor de gewenste rapportreeks eerst toelaten.

Wanneer u een online hit verzendt die een [`transactionID`](/help/implement/vars/page-vars/transactionid.md) -waarde bevat, maakt Adobe een &quot;momentopname&quot; van alle ingestelde of geduurde variabelen. Als een transactie-id wordt gevonden die via gegevensbronnen is geüpload, worden de offline- en onlinegegevens aan elkaar gekoppeld.

Gegevensbronnen van transactie-id hebben de volgende eigenschappen:

* De online gegevens moeten eerst worden verzameld en verwerkt. Als een transactie-id-gegevensbron wordt geüpload voordat een rapportsuite een hit verwerkt die overeenkomt met die transactie-id, zijn de gegevens niet gekoppeld.
* Transactie-id&#39;s die via AppMeasurement zijn verzameld, verlopen na 25 maanden.
* Gegevensbronnen die met een verlopen transactie-id zijn geüpload, worden op dezelfde manier behandeld als gegevens die zonder transactie-id zijn geüpload.
* Als dezelfde variabele is opgenomen in zowel de online hit als de transactie-id-gegevensbron, wordt de waarde van de transactie-id-gegevensbron gebruikt in de hit van de transactiegegevensbron.
* Als een variabele is opgenomen in een online hit maar niet in een treffer voor een overeenkomende transactie-id-gegevensbron, blijft de online raakvariabele behouden.
* Als u dezelfde transactie-id instelt voor meerdere online treffers, wordt alleen de eerste instantie gewijzigd met gegevens uit een overeenkomende transactie-id-gegevensbron.

Bijvoorbeeld:

1. U verzendt een paginaweergave vanuit AppMeasurement waarin:
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

De eVar1-waarde `blue` en de `event1` -waarde zijn niet aanwezig in de rapportage, omdat de transactie-id die wordt gevonden, deze respectieve waarden overschrijft.
