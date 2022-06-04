---
title: Adobe Analytics implementeren met de Adobe Experience Platform Mobile SDK
description: Gebruik de extensie Mobile SDK in Adobe Experience Platform Data Collection om gegevens naar Adobe Analytics te verzenden.
source-git-commit: 6979736e1849d25af2141e0ab76a143605a90620
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Adobe Analytics implementeren met de Adobe Experience Platform Mobile SDK

De Adobe Experience Platform Mobile SDK helpt Adobe Experience Cloud-oplossingen en -services aan te schaffen in uw mobiele apps. Deze functie is beschikbaar voor Android, iOS en verschillende platformonafhankelijke ontwikkelframeworks. De configuratie wordt behandeld door de UI van de Inzameling van Gegevens van Adobe Experience Platform.

Gegevens naar Adobe Experience Edge verzenden met de Mobile SDK:

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection).
2. Selecteer de gewenste eigenschap in de lijst, of [een mobiele eigenschap instellen](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).
3. Ga naar het tabblad Extensies en installeer de [Identiteit voor Edge Network](https://aep-sdks.gitbook.io/docs/foundation-extensions/identity-for-edge-network) extensie.
4. Installeer de [Adobe Experience Platform Edge Network](https://aep-sdks.gitbook.io/docs/foundation-extensions/experience-platform-extension).
5. [Een gegevensstroom configureren](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams)Adobe Analytics toevoegen als een service die naar de gewenste rapportsuite verwijst.
6. [De SDK installeren](https://aep-sdks.gitbook.io/docs/getting-started/get-the-sdk) op uw mobiele app.

>[!IMPORTANT]
>
>Een extensie Adobe Analytics is ook beschikbaar in de gebruikersinterface voor gegevensverzameling. Als u deze extensie installeert, profiteert u niet van XDM of Edge Network.
