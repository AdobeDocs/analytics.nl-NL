---
title: transactionID
description: Gebruik deze variabele om online en offline gegevens aan elkaar te koppelen.
feature: Appmeasurement Implementation
exl-id: 525e90d8-99a7-4f4f-9bce-1395bf72fd8f
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# transactionID

De `transactionID` variabele identificeert uniek een transactie zodat de slag afmetingswaarden aan gegevens kan verstrekken die door [ gegevensbronnen van identiteitskaart van de Transactie ](/help/import/data-sources/transactionid.md) worden geupload. Deze variabele is handig wanneer u de gegevens van offlinekanalen wilt invullen met waarden die zijn verzameld op basis van de gegevens van het onlinekanaal.

>[!NOTE]
>
>Controleer of [!UICONTROL Transaction ID Storage] is ingeschakeld in een rapportsuite voordat u deze variabele gebruikt. Zie [ Algemene Montages van de Rekening ](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) in de Admin gebruikersgids voor meer informatie.

Wanneer u `transactionID` instelt op een hit, maakt Adobe een momentopname van alle variabelen van Analytics die op dat moment zijn ingesteld of aanwezig zijn. Zie [ de gegevensbronnen van identiteitskaart van de Transactie ](/help/import/data-sources/transactionid.md) voor de lijst van dimensies inbegrepen in de momentopname. Adobe onthoudt alle waarden van de transactie-id (gekoppeld en ongekoppeld) gedurende maximaal 25 maanden.

## Transactie-id met de Web SDK

De transactie-id wordt toegewezen aan de volgende variabelen:

* [ voorwerp XDM ](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.commerce.order.payments[3].transactionID` of `xdm.commerce.order.payments.transactionID`
* [ voorwerp van Gegevens ](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.transactionID` of `data.__adobe.analytics.xact`

## Transactie-id met Adobe Analytics-extensie

U kunt transactie-id instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL Transaction ID] .

U kunt transactie-id instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.transactionID in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De variabele `s.transactionID` is een tekenreeks met een unieke id voor een transactie. Geldige waarden zijn alfanumerieke tekens met een lengte van maximaal 100 bytes. De standaardwaarde is een lege tekenreeks.

```js
s.transactionID = "ABC123";
```

Als u meer dan één transactie-id voor een hit hebt, kunt u elke id scheiden met een komma. Voor meerdere transactie-id&#39;s geldt nog steeds de limiet van 100 bytes.

```js
s.transactionID = "ABC123,XYZ456";
```

>[!TIP]
>
>Als u veelvoudige off-line kanalen gebruikend deze variabele integreert, zorg ervoor dat de verschillende kanalen geen transactie IDs overlappen. Als u bijvoorbeeld een transactie-id van het callcenter hebt met de waarde `1234` en de transactie-id van de verkooplead met de waarde `1234` , kunnen er conflicten optreden en onverwachte resultaten optreden. Zorg ervoor dat transactie-id&#39;s unieke indelingen per offlinekanaal bevatten en maak deze indien nodig onderscheid. Stel bijvoorbeeld de transactie-id van het callcenter in op `call_1234` en de transactie-id van de verkooplead `lead_1234` in zowel Gegevensbronnen als AppMeasurement.
