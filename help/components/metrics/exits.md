---
title: Gesloten
description: Een instantie van de laatste waarde in een bezoek.
feature: Metrics
exl-id: 0997ed1f-29b0-403d-9ed2-644a5ff19aef
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# Gesloten

*Deze Help-pagina beschrijft hoe afsluiten werkt als metrisch. Voor informatie over hoe de uitgang als dimensie werkt, zie [Afmetingen afsluiten](../dimensions/exit-dimensions.md).*

De &#39;uitgangen&#39; [metrisch](overview.md) toont het aantal keren dat een bepaald dimensie-item wordt vastgelegd als de laatste waarde in een bezoek. Deze maatstaf is handig wanneer u meer wilt weten over het laatste wat bezoekers zien voordat ze uw site verlaten. Door de laatste waarden van een dimensie te zien, kunt u de ervaring begrijpen en optimaliseren die een bezoeker krijgt voordat hij of zij vertrekt.

## Hoe deze metrische waarde wordt berekend

Na een [bezoek](visits.md) besluit, registreer het meest recente afmetingspunt als uitgang. Per bezoek bestaat slechts één uitgang. Het is niet noodzakelijkerwijs de laatste hit van het bezoek als de dimensie in eerdere treffers werd vastgesteld. Het is een op een bezoek gebaseerde meting; het is met terugwerkende kracht van toepassing op alle treffers in het bezoek.

>[!TIP]
>
>Als u deze metrische waarde weergeeft in vergelijking met een dimensie die niet altijd bij elk bezoek is ingesteld, kunt u het item &#39;Niet-opgegeven&#39; dimensie verbergen in Analysis Workspace. Klik op het filterpictogram en schakel vervolgens de optie uit [!UICONTROL Include unspecified (None)].
