---
title: transactionID
description: Gebruik deze variabele om online en offline gegevens aan elkaar te koppelen.
exl-id: 525e90d8-99a7-4f4f-9bce-1395bf72fd8f
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# transactionID

De `transactionID` variabele identificeert uniek een transactie zodat kan de slag aan gegevens verbinden die door Gegevensbronnen worden geupload. Deze variabele is nuttig in gevallen waarin u gegevens van andere kanalen wilt gebruiken en deze aan gegevens wilt koppelen die met AppMeasurement worden verzameld.

>[!NOTE]
>
>Zorg ervoor dat [!UICONTROL Transaction ID Storage] in een rapportreeks wordt toegelaten alvorens deze variabele te gebruiken. Zie [Algemene accountinstellingen](/help/admin/admin/general-acct-settings-admin.md) in de handleiding voor Admin-gebruikers voor meer informatie.

Wanneer u `transactionID` op een hit plaatst, neemt Adobe een &quot;momentopname&quot;van alle variabelen van de Analyse die op dat punt in tijd worden geplaatst of voortgeduurd. Gegevens die via gegevensbronnen met een overeenkomende transactie-id zijn geüpload, zijn permanent gekoppeld aan die variabele waarden.

Standaard onthoudt Adobe alle waarden van de transactie-id (gekoppeld en ongekoppeld) gedurende maximaal 90 dagen. Als uw offline interactieproces langer is dan 90 dagen, neemt u contact op met de klantenservice om deze limiet te verlengen.

## Transactie-id met tags in Adobe Experience Platform

U kunt transactie-id instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de sectie [!UICONTROL Transaction ID].

U kunt transactie-id instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.transactionID in AppMeasurement en de redacteur van de douanecode

De variabele `s.transactionID` is een tekenreeks met een unieke id voor een transactie. Geldige waarden zijn alfanumerieke tekens met een lengte van maximaal 100 bytes. De standaardwaarde is een lege tekenreeks.

```js
s.transactionID = "ABC123";
```

Als u meer dan één transactie-id voor een hit hebt, kunt u elke id scheiden met een komma. Voor meerdere transactie-id&#39;s geldt nog steeds de limiet van 100 bytes.

```js
s.transactionID = "ABC123,XYZ456";
```

>[!NOTE]
>
>Als u veelvoudige off-line kanalen gebruikend deze variabele integreert, zorg ervoor dat de verschillende kanalen geen transactie IDs overlappen. Bijvoorbeeld, als u een waarde van identiteitskaart van de de transactieTransactie van het callcenter van `1234` en een waarde van identiteitskaart van de de transactie van het verkooplood van `1234` hebt, kunnen zij conflicten en onverwachte resultaten veroorzaken. Zorg ervoor dat transactie-id&#39;s unieke indelingen per offlinekanaal bevatten en maak deze indien nodig onderscheid. Bijvoorbeeld, plaats uw identiteitskaart van de de transactie van het vraagcentrum aan `call_1234` en uw identiteitskaart `lead_1234` van de de transactie van het verkooplood in zowel Gegevensbronnen als AppMeasurement.
