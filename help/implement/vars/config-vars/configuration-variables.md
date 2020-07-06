---
title: Configuratievariabelen
description: Gebruik configuratievariabelen om te bepalen hoe gegevens worden verzameld.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 5%

---


# Overzicht van configuratievariabelen

De variabelen van de configuratie controleren de manier gegevens in rapportering wordt gevangen en verwerkt. Ze bevatten doorgaans geen afmetingen of metrische waarden.

## Configuratievariabelen instellen

In JavaScript-implementaties die gebruikmaken van `AppMeasurement.js`, worden configuratievariabelen doorgaans boven aan het JS-bestand ingesteld.

In implementaties die gebruikmaken van het Adobe Experience Platform Launch, worden configuratievariabelen doorgaans gevonden door de Adobe Analytics-extensie te configureren:

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your Adobe ID credentials.
2. Klik op de eigenschap die u wilt bewerken.
3. Klik op het [!UICONTROL Extensions] tabblad en klik vervolgens [!UICONTROL Configure] onder Adobe Analytics.

>[!IMPORTANT]
>
>Zorg ervoor alle configuratievariabelen worden geplaatst alvorens een het volgen methode ([`t()`](../functions/t-method.md) of [`tl()`](../functions/tl-method.md)) te roepen. Stel geen configuratievariabelen in de [`doPlugins()`](../functions/doplugins.md) functie in.
