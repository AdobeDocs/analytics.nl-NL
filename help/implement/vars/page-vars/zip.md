---
title: zip
description: Vul handmatig de dimensie 'Postcode' in als de instellingen van de rapportsuite dit toestaan.
feature: Variables
exl-id: 1acf4bf7-3788-46bd-bcdb-9885c7b93b59
role: Admin, Developer
source-git-commit: 5ef92db2f5edb5fded497dddedd56abd49d8a019
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# zip

De `zip` met variabele kunt u de dimensie &#39;Postcode&#39; handmatig vullen als de waarde [!UICONTROL Zip Option] in de montages van de rapportreeks staat het toe. In eerdere versies van Adobe Analytics kon deze variabele alleen handmatig worden ingesteld, meestal bij het invoeren van verzendgegevens op een detailhandelssite. Dankzij de verbeteringen in Adobe Analytics kan deze variabele automatisch worden ingesteld met behulp van geo-locatiegegevens. Deze variabele blijft niet behouden na de hit die is ingesteld.

>[!IMPORTANT]
>
>Zorg ervoor dat de [!UICONTROL Zip Option] in rapportsuite worden de instellingen ingesteld op de gewenste waarde. U kunt deze variabele niet gebruiken als [!UICONTROL Geo zip] wordt altijd gebruikt. Zie [Algemene accountinstellingen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) in de gebruikershandleiding voor Admin voor meer informatie.

## Postcode die de Web SDK gebruikt

Postcode wordt toegewezen aan de volgende variabelen:

* [XDM-object](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.placeContext.geo.postalCode`
* [Data, object](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.zip`

## Postcode met Adobe Analytics-extensie

U kunt Postcode instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Zip] sectie.

U kunt postcode instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.zip in AppMeasurement en de de uitbreidingsredacteur van de douanecode van de Analyse

De `s.zip` variabele is een tekenreeks die doorgaans een ZIP-code bevat, maar die een willekeurige gewenste waarde van maximaal 50 bytes kan bevatten.

```js
s.zip = "84043";
```
