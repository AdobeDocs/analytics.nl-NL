---
title: XDM-gegevens gebruiken met Analytics
description: Overzicht van het gebruik van XDM-gegevens van Experience Platform in Adobe Analytics
feature: AEP Edge
exl-id: 6f1282fb-8d4a-4d88-9be0-1c939c22cb92
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 2%

---

# Adobe Experience Platform Edge-gegevens gebruiken met Analytics

U kunt de [Adobe Experience Platform (AEP) Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html) om gegevens naar Adobe Analytics te verzenden. Dit werkt door het [Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) in een indeling die wordt gebruikt door Analytics.

Analytics verzamelt XDM-gegevens via twee methoden:

* Automatische toewijzing van XDM-schema&#39;s
* Handmatige toewijzing aan contextgegevens

## Automatische toewijzing

Automatische toewijzing is afhankelijk van een standaardinstelling [schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html) in de XDM die automatisch JSON-objecten vult die zijn opgenomen in standaardgegevensverzameling van Analytics. De variabelen van Analytics die automatisch van XDM aan uw gevormde rapportreeksen worden in kaart gebracht vereisen geen ontwikkelaarssteun om op te nemen. Zie [Variabelen worden automatisch toegewezen in Analytics](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/adobe-analytics/automatically-mapped-vars.html) in de de gebruikersgids van SDK van het Web van het Platform.

## Handmatige toewijzing

[Handmatige toewijzing van XDM-gegevens aan Analytics](xdm-manual.md) vertrouwt op [Contextgegevens voor analyse](../vars/page-vars/contextdata.md) variabelen. Deze variabelen worden in JSON-objecten geplaatst die overeenkomen met de toepasselijke schema&#39;s. Typisch, voegt uw ontwikkelingsteam contextgegevens bij implementatie toe en dan Admins reeks [verwerkingsvoorschriften](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md) om die gegevens op gespecificeerde rapportreeksen toe te passen.

## Instellen

Analytics instellen voor het ontvangen van XDM-gegevens:

1. Installeren en [vormen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html).

2. Controleer of de toepasselijke rapportsuites zijn toegewezen aan de gewenste gegevens. XDM-gegevens worden automatisch vanuit het Adobe Experience-platform naar de rapportsuite verzonden.
