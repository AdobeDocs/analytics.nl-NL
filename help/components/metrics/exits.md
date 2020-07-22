---
title: Gesloten
description: Een instantie van de laatste waarde in een bezoek.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# Gesloten

*Deze Help-pagina beschrijft hoe afsluiten werkt als metrisch. Voor informatie over hoe de uitgang werk als dimensie, zie de dimensies[van de](../dimensions/exit-dimensions.md)Uitgang.*

De metrische waarde &#39;Afsluiten&#39; toont het aantal keren dat een bepaald dimensie-item wordt vastgelegd als de laatste waarde in een bezoek. Deze maatstaf is handig wanneer u meer wilt weten over het laatste wat bezoekers zien voordat ze uw site verlaten. Door de laatste waarden van een dimensie te zien, kunt u de ervaring begrijpen en optimaliseren die een bezoeker krijgt voordat hij of zij vertrekt.

## Hoe deze metrische waarde wordt berekend

Nadat een [bezoek](visits.md) eindigt, registreer het meest recente afmetingspunt als uitgang. Per bezoek bestaat slechts één uitgang. Het is niet noodzakelijkerwijs de laatste hit van het bezoek als de dimensie in eerdere treffers werd vastgesteld. Het is een op bezoek-gebaseerde metrisch; zij is met terugwerkende kracht van toepassing op alle bezoekerslijsten .

>[!TIP]
>
>Als u deze metrische waarde weergeeft in vergelijking met een dimensie die niet altijd bij elk bezoek is ingesteld, kunt u het item &#39;Niet-opgegeven&#39; dimensie verbergen in Analysis Workspace. Klik op het filterpictogram en schakel de optie uit [!UICONTROL Include unspecified (None)].
