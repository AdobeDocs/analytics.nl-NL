---
title: zip
description: Vul handmatig de dimensie 'Postcode' in als de instellingen van de rapportsuite dit toestaan.
feature: Appmeasurement Implementation
exl-id: 1acf4bf7-3788-46bd-bcdb-9885c7b93b59
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# zip

Met de variabele `zip` kunt u de dimensie &#39;Postcode&#39; handmatig vullen als de instellingen van [!UICONTROL Zip Option] in de rapportsuite dit toestaan. In eerdere versies van Adobe Analytics kon deze variabele alleen handmatig worden ingesteld, meestal bij het invoeren van verzendgegevens op een detailhandelssite. Dankzij de verbeteringen in Adobe Analytics kan deze variabele automatisch worden ingesteld met behulp van geo-locatiegegevens. Deze variabele blijft niet behouden na de hit die is ingesteld.

>[!IMPORTANT]
>
>Controleer of de instellingen voor [!UICONTROL Zip Option] in de rapportsuite op de gewenste waarde zijn ingesteld. U kunt deze variabele niet gebruiken als [!UICONTROL Geo zip] altijd wordt gebruikt. Zie [ Algemene Montages van de Rekening ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) in de Admin gebruikersgids voor meer informatie.

## Postcode met gebruik van Web SDK

Postcode wordt toegewezen aan de volgende variabelen:

* [ voorwerp XDM ](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.placeContext.geo.postalCode`
* [ voorwerp van Gegevens ](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.zip`

## Postcode met Adobe Analytics-extensie

U kunt Postcode instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL Zip] .

U kunt postcode instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.zip in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.zip` variabele is een tekenreeks die doorgaans een ZIP-code bevat, maar die elke gewenste waarde van maximaal 50 bytes kan bevatten.

```js
s.zip = "84043";
```
