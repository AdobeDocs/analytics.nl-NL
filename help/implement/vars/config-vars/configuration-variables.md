---
title: Configuratievariabelen
description: Gebruik configuratievariabelen om te bepalen hoe gegevens worden verzameld.
feature: Appmeasurement Implementation
exl-id: 3f017a94-b71d-47da-8ab4-daf32475ed34
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# Overzicht van configuratievariabelen

De variabelen van de configuratie controleren de manier de gegevens in rapportering worden gevangen en worden verwerkt. Ze bevatten doorgaans geen afmetingen of metrische waarden.

## Configuratievariabelen instellen

In implementaties die de uitbreiding van SDK van het Web of de uitbreiding van Analytics gebruiken, worden de configuratievariabelen typisch gevonden in de montages van de uitbreiding:

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Klik op de tab [!UICONTROL Extensions] en klik vervolgens op [!UICONTROL Configure] onder de extensie.

In JavaScript-implementaties met `AppMeasurement.js` worden configuratievariabelen doorgaans boven aan het JS-bestand ingesteld.

>[!IMPORTANT]
>
>Zorg ervoor dat alle configuratievariabelen worden geplaatst alvorens een volgende methode ([`t()`](../functions/t-method.md) of [`tl()`](../functions/tl-method.md)) te roepen. Stel configuratievariabelen niet in de functie [`doPlugins()`](../functions/doplugins.md) in.
