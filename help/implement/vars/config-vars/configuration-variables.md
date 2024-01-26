---
title: Configuratievariabelen
description: Gebruik configuratievariabelen om te bepalen hoe gegevens worden verzameld.
feature: Variables
exl-id: 3f017a94-b71d-47da-8ab4-daf32475ed34
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# Overzicht van configuratievariabelen

De variabelen van de configuratie controleren de manier de gegevens in rapportering worden gevangen en worden verwerkt. Ze bevatten doorgaans geen afmetingen of metrische waarden.

## Configuratievariabelen instellen

In implementaties die de uitbreiding van SDK van het Web of de uitbreiding van Analytics gebruiken, worden de configuratievariabelen typisch gevonden in de montages van de uitbreiding:

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Klik op de knop [!UICONTROL Extensions] en vervolgens klikt u op [!UICONTROL Configure] onder de verlenging.

In JavaScript-implementaties die `AppMeasurement.js`configuratievariabelen worden doorgaans boven aan het JS-bestand ingesteld.

>[!IMPORTANT]
>
>Zorg ervoor dat alle configuratievariabelen zijn ingesteld voordat u een volgende methode aanroept ([`t()`](../functions/t-method.md) of [`tl()`](../functions/tl-method.md)). U kunt configuratievariabelen in het dialoogvenster [`doPlugins()`](../functions/doplugins.md) functie.
