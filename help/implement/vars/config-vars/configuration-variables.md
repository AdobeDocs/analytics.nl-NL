---
title: Configuratievariabelen
description: Gebruik configuratievariabelen om te bepalen hoe gegevens worden verzameld.
feature: Variables
exl-id: 3f017a94-b71d-47da-8ab4-daf32475ed34
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# Overzicht van configuratievariabelen

De variabelen van de configuratie controleren de manier gegevens in rapportering wordt gevangen en verwerkt. Ze bevatten doorgaans geen afmetingen of metrische waarden.

## Configuratievariabelen instellen

In JavaScript-implementaties die `AppMeasurement.js`configuratievariabelen worden doorgaans boven aan het JS-bestand ingesteld.

In implementaties die Adobe Experience Platform-tags gebruiken, worden configuratievariabelen doorgaans gevonden door de Adobe Analytics-extensie te configureren:

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de eigenschap die u wilt bewerken.
1. Klik op de knop [!UICONTROL Extensions] en vervolgens klikt u op [!UICONTROL Configure] onder Adobe Analytics.

>[!IMPORTANT]
>
>Zorg ervoor alle configuratievariabelen alvorens een het volgen methode ([`t()`](../functions/t-method.md) of [`tl()`](../functions/tl-method.md)). U kunt configuratievariabelen in het dialoogvenster [`doPlugins()`](../functions/doplugins.md) functie.
