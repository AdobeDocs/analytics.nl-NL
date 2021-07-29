---
title: Configuratievariabelen
description: Gebruik configuratievariabelen om te bepalen hoe gegevens worden verzameld.
exl-id: 3f017a94-b71d-47da-8ab4-daf32475ed34
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# Overzicht van configuratievariabelen

De variabelen van de configuratie controleren de manier gegevens in rapportering wordt gevangen en verwerkt. Ze bevatten doorgaans geen afmetingen of metrische waarden.

## Configuratievariabelen instellen

In JavaScript-implementaties met `AppMeasurement.js` worden configuratievariabelen doorgaans boven aan het JS-bestand ingesteld.

In implementaties die Adobe Experience Platform-tags gebruiken, worden configuratievariabelen doorgaans gevonden door de Adobe Analytics-extensie te configureren:

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de eigenschap die u wilt bewerken.
1. Klik op de tab [!UICONTROL Extensions] en klik vervolgens onder Adobe Analytics op [!UICONTROL Configure].

>[!IMPORTANT]
>
>Zorg ervoor alle configuratievariabelen worden geplaatst alvorens een volgende methode ([`t()`](../functions/t-method.md) of [`tl()`](../functions/tl-method.md)) te roepen. Stel geen configuratievariabelen in de functie [`doPlugins()`](../functions/doplugins.md) in.
