---
title: zip
description: Vul handmatig de dimensie 'Postcode' in als de instellingen van de rapportsuite dit toestaan.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# zip

Met de `zip` [!UICONTROL Zip Option] variabele kunt u de dimensie &#39;Postcode&#39; handmatig vullen als de instellingen van de rapportsuite dit toestaan. In eerdere versies van Adobe Analytics kon deze variabele alleen handmatig worden ingesteld, meestal bij het invoeren van verzendgegevens op een handelssite. Dankzij de verbeteringen in Adobe Analytics kan deze variabele automatisch worden ingesteld met behulp van geo-locatiegegevens. Deze variabele blijft niet behouden na de hit die is ingesteld.

> [!IMPORTANT] Zorg ervoor [!UICONTROL Zip Option] in de montages van de rapportreeks aan de gewenste waarde wordt geplaatst. U kunt deze variabele niet gebruiken als deze altijd [!UICONTROL geo zip] wordt gebruikt. Zie [Algemene accountinstellingen](/help/admin/admin/general-acct-settings-admin.md) in de gebruikershandleiding voor beheerders voor meer informatie.

## Ga naar Adobe Experience Platform Launch

U kunt Postcode instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Zip] sectie.

U kunt postcode instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.zip in de redacteur van de douanecode van AppMeasurement en van de Lancering

De `s.zip` variabele is een tekenreeks die doorgaans een ZIP-code bevat, maar die elke gewenste waarde van maximaal 50 bytes kan bevatten.

```js
s.zip = "84043";
```
