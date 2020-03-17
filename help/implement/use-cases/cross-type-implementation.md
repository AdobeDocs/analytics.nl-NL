---
title: Houd verschillende implementatietypen bij
description: Gebruik verschillende implementatietypen en volg bezoekers naadloos tussen hen.
translation-type: tm+mt
source-git-commit: 819f719c4ce131c04916f3b668bcbda1a1b03651

---


# Houd verschillende implementatietypen bij

Deze informatie is bedoeld voor gevorderde gebruikers die goed op de hoogte zijn van zowel rapportage als implementatie. Probeer uw implementatie niet te bewerken zonder de gevolgen te begrijpen. Neem contact op met de accountmanager van uw organisatie als u implementatiewijzigingen nodig hebt.

Als u meer dan één type implementatie gebruikt (zoals JavaScript en verzoeken om een gecodeerde afbeelding), moet u ervoor zorgen dat de volgende variabelen worden opgegeven en met elkaar overeenkomen:

* *`s_account`*
* *`s.visitorNamespace`*
* *`s.trackingServer`*
* *`s.trackingServerSecure`* (als SSL wordt gebruikt)

Als deze niet overeenkomen met de verschillende implementaties, kunnen gebruikers worden bijgehouden als afzonderlijke bezoekers.
