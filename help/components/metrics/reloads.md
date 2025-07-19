---
title: Opnieuw laden
description: Het aantal keren dat de pagina opnieuw is geladen.
feature: Metrics
exl-id: 9539a733-9e9f-48b3-b8ab-8d969de27f87
source-git-commit: c9b7c32adfb44a04ab792d12ca049106b3009710
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Opnieuw laden

&quot;herlaadt&quot;[ metrisch ](overview.md) toont het aantal tijden een afmetingspunt tijdens een herlading aanwezig was. Een bezoeker die zijn browser vernieuwt, is de meest gebruikelijke manier om een nieuwe laadbewerking te starten.

## Hoe deze metrische waarde wordt berekend

Deze metrische tellingen het aantal treffers waar de [ dimensie van de Pagina ](../dimensions/page.md) de zelfde waarde zoals de vorige klap bevat.

Het concept van een herladen is op de dimensie van de Pagina van toepassing ongeacht welke afmeting die u in rapportering gebruikt. Bijvoorbeeld, als u [ eVar1 ](../dimensions/evar.md) als afmeting gebruikt en als metrisch opnieuw laadt, toont de lijst u het aantal tijden dat elke waarde van eVar tijdens een herlading (twee opeenvolgende paginawaarden) aanwezig was. Het geeft niet het aantal keren weer dat twee opeenvolgende eVar1-waarden aanwezig waren.
