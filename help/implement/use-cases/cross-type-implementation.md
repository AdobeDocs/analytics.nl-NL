---
title: Verschillende implementatietypen bijhouden
description: Gebruik verschillende implementatietypen en volg bezoekers naadloos tussen hen.
feature: Implementation Basics
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---

# Verschillende implementatietypen bijhouden

Deze informatie is bedoeld voor gevorderde gebruikers die goed op de hoogte zijn van zowel rapportage als implementatie. Probeer uw implementatie niet te bewerken zonder de gevolgen te begrijpen. Neem contact op met de accountmanager van uw organisatie als u implementatiewijzigingen nodig hebt.

Als u meer dan één type implementatie gebruikt (zoals JavaScript en verzoeken om een gecodeerde afbeelding), moet u ervoor zorgen dat de volgende variabelen worden opgegeven en met elkaar overeenkomen:

* *`s_account`*
* *`s.visitorNamespace`*
* *`s.trackingServer`*
* *`s.trackingServerSecure`* (als SSL wordt gebruikt)

Als deze niet overeenkomen met de verschillende implementaties, kunnen gebruikers worden bijgehouden als afzonderlijke bezoekers.
