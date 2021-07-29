---
title: zip
description: Vul handmatig de dimensie 'Postcode' in als de instellingen van de rapportsuite dit toestaan.
exl-id: 1acf4bf7-3788-46bd-bcdb-9885c7b93b59
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# zip

Met de variabele `zip` kunt u de dimensie &#39;Postcode&#39; handmatig vullen als de instellingen van de rapportsuite dit toestaan. [!UICONTROL Zip Option] In eerdere versies van Adobe Analytics kon deze variabele alleen handmatig worden ingesteld, meestal bij het invoeren van verzendgegevens op een detailhandelssite. Dankzij de verbeteringen in Adobe Analytics kan deze variabele automatisch worden ingesteld met behulp van geo-locatiegegevens. Deze variabele blijft niet behouden na de hit die is ingesteld.

>[!IMPORTANT]
>
>Zorg ervoor [!UICONTROL Zip Option] in de montages van de rapportreeks aan de gewenste waarde wordt geplaatst. U kunt deze variabele niet gebruiken als [!UICONTROL geo zip] altijd wordt gebruikt. Zie [Algemene accountinstellingen](/help/admin/admin/general-acct-settings-admin.md) in de handleiding voor Admin-gebruikers voor meer informatie.

## Postcode met tags in Adobe Experience Platform

U kunt Postcode instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de sectie [!UICONTROL Zip].

U kunt postcode instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.zip in AppMeasurement en aangepaste code-editor

De `s.zip` variabele is een koord dat typisch een Code van het PIT bevat, maar om het even welke gewenste waarde tot 50 bytes in lengte kan bevatten.

```js
s.zip = "84043";
```
