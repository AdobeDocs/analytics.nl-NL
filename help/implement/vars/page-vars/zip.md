---
title: zip
description: Vul handmatig de dimensie 'Postcode' in als de instellingen van de rapportsuite dit toestaan.
feature: Variables
exl-id: 1acf4bf7-3788-46bd-bcdb-9885c7b93b59
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# zip

De `zip` met variabele kunt u de dimensie &#39;Postcode&#39; handmatig vullen als de waarde [!UICONTROL Zip Option] in de montages van de rapportreeks staat het toe. In eerdere versies van Adobe Analytics kon deze variabele alleen handmatig worden ingesteld, meestal bij het invoeren van verzendgegevens op een detailhandelssite. Dankzij de verbeteringen in Adobe Analytics kan deze variabele automatisch worden ingesteld met behulp van geo-locatiegegevens. Deze variabele blijft niet behouden na de hit die is ingesteld.

>[!IMPORTANT]
>
>Zorg ervoor dat de [!UICONTROL Zip Option] in rapportsuite worden de instellingen ingesteld op de gewenste waarde. U kunt deze variabele niet gebruiken als [!UICONTROL geo zip] wordt altijd gebruikt. Zie [Algemene accountinstellingen](/help/admin/admin/general-acct-settings-admin.md) in de gebruikershandleiding voor Admin voor meer informatie.

## Postcode met Adobe Analytics-extensie

U kunt Postcode instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions]klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Zip] sectie.

U kunt postcode instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.zip in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.zip` variabele is een tekenreeks die doorgaans een ZIP-code bevat, maar die een willekeurige gewenste waarde van maximaal 50 bytes kan bevatten.

```js
s.zip = "84043";
```
