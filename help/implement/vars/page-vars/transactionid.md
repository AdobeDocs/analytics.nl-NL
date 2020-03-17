---
title: transactionID
description: Gebruik deze variabele om online en offline gegevens aan elkaar te koppelen.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# transactionID

De `transactionID` variabele identificeert uniek een transactie zodat kan de slag aan gegevens verbinden die door Gegevensbronnen worden geupload. Deze variabele is nuttig in gevallen waarin u gegevens van andere kanalen wilt gebruiken en deze aan gegevens wilt koppelen die met AppMeasurement worden verzameld.

> [!NOTE] Zorg ervoor dat [!UICONTROL Transaction ID Storage] wordt toegelaten in een rapportreeks alvorens deze variabele te gebruiken. Zie [Algemene accountinstellingen](/help/admin/admin/general-acct-settings-admin.md) in de gebruikershandleiding voor beheerders voor meer informatie.

Wanneer u een hit `transactionID` activeert, maakt Adobe een &quot;momentopname&quot; van alle variabelen voor Analytics die op dat moment zijn ingesteld of blijven bestaan. Gegevens die via gegevensbronnen met een overeenkomende transactie-id zijn geüpload, zijn permanent gekoppeld aan die variabele waarden.

Adobe onthoudt standaard alle waarden voor de transactie-id (gekoppeld en ongekoppeld) gedurende maximaal 90 dagen. Als uw offline interactieproces langer is dan 90 dagen, neemt u contact op met de klantenservice om deze limiet te verlengen.

## Transactie-id in Adobe Experience Platform Starten

U kunt transactie-id instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Transaction ID] sectie.

U kunt transactie-id instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.transactionID in AppMeasurement en Launch de redacteur van de douanecode

De `s.transactionID` variabele is een tekenreeks met een unieke id voor een transactie. Geldige waarden zijn alfanumerieke tekens met een lengte van maximaal 100 bytes. De standaardwaarde is een lege tekenreeks.

```js
s.transactionID = "ABC123";
```

Als u meer dan één transactie-id voor een hit hebt, kunt u elke id scheiden met een komma. Voor meerdere transactie-id&#39;s geldt nog steeds de limiet van 100 bytes.

```js
s.transactionID = "ABC123,XYZ456";
```

> [!NOTE] Als u veelvoudige off-line kanalen gebruikend deze variabele integreert, zorg ervoor dat de verschillende kanalen geen transactie IDs overlappen. Bijvoorbeeld, als u een waarde van identiteitskaart van de transactie van het callcenter van `1234` `1234`en een waarde van identiteitskaart van de transactie van het verkooplood van hebt, kunnen zij conflicten veroorzaken en onverwachte resultaten veroorzaken. Zorg ervoor dat transactie-id&#39;s unieke indelingen per offlinekanaal bevatten en maak deze indien nodig onderscheid. Bijvoorbeeld, plaats uw identiteitskaart van de de transactie van het vraagcentrum aan `call_1234` en uw identiteitskaart van de verkooploodtransactie `lead_1234` in zowel Gegevensbronnen als AppMeasurement.
