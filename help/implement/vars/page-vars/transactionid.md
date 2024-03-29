---
title: transactionID
description: Gebruik deze variabele om online en offline gegevens aan elkaar te koppelen.
feature: Variables
exl-id: 525e90d8-99a7-4f4f-9bce-1395bf72fd8f
role: Admin, Developer
source-git-commit: 5ef92db2f5edb5fded497dddedd56abd49d8a019
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# transactionID

De `transactionID` De variabele identificeert uniek een transactie zodat kan de slag aan gegevens verbinden die door Gegevensbronnen worden geupload. Deze variabele is nuttig in gevallen waarin u gegevens uit andere kanalen wilt gebruiken en deze aan gegevens wilt koppelen die met AppMeasurement zijn verzameld.

>[!NOTE]
>
>Controleer of [!UICONTROL Transaction ID Storage] wordt toegelaten in een rapportreeks alvorens deze variabele te gebruiken. Zie [Algemene accountinstellingen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) in de gebruikershandleiding voor Admin voor meer informatie.

Wanneer u instelt `transactionID` Bij een hit maakt Adobe gebruik van een &quot;momentopname&quot; van alle analytische variabelen die op dat moment zijn ingesteld of blijven bestaan. Gegevens die via gegevensbronnen met een overeenkomende transactie-id zijn geüpload, zijn permanent gekoppeld aan die variabele waarden.

Standaard onthoudt de Adobe alle waarden van de transactie-id (gekoppeld en ongekoppeld) gedurende maximaal 90 dagen. Als uw offline interactieproces langer is dan 90 dagen, neemt u contact op met de klantenservice om deze limiet te verlengen.

## Transactie-id met de Web SDK

De transactie-id wordt toegewezen aan de volgende variabelen:

* [XDM-object](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.commerce.order.payments[0].transactionID`
* [Data, object](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.transactionID` of `data.__adobe.analytics.xact`

## Transactie-id met Adobe Analytics-extensie

U kunt transactie-id instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Transaction ID] sectie.

U kunt transactie-id instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.transactionID in AppMeasurement en de de uitbreidingsredacteur van de douanecode van de Analyse

De `s.transactionID` variabele is een tekenreeks die een unieke id voor een transactie bevat. Geldige waarden zijn alfanumerieke tekens met een lengte van maximaal 100 bytes. De standaardwaarde is een lege tekenreeks.

```js
s.transactionID = "ABC123";
```

Als u meer dan één transactie-id voor een hit hebt, kunt u elke id scheiden met een komma. Voor meerdere transactie-id&#39;s geldt nog steeds de limiet van 100 bytes.

```js
s.transactionID = "ABC123,XYZ456";
```

>[!TIP]
>
>Als u veelvoudige off-line kanalen gebruikend deze variabele integreert, zorg ervoor dat de verschillende kanalen geen transactie IDs overlappen. Bijvoorbeeld, als u een waarde van identiteitskaart van de transactie van het callcenter van `1234` en een transactie-id voor verkooplead van `1234`kunnen conflicten veroorzaken en onverwachte resultaten tot gevolg hebben. Zorg ervoor dat transactie-id&#39;s unieke indelingen per offlinekanaal bevatten en maak deze indien nodig onderscheid. Bijvoorbeeld, plaats uw identiteitskaart van de transactie van het callcenter aan `call_1234` en je transactie-ID voor lead in `lead_1234` in zowel Gegevensbronnen als AppMeasurement.
