---
title: Geretourneerde frequentie
description: De hoeveelheid tijd die tussen het huidige en het vorige bezoek is verstreken.
feature: Dimensions
exl-id: 8ec31e17-a57d-416f-b471-c2c37a98d134
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Geretourneerde frequentie

De &#39;retourfrequentie&#39; [dimensie](overview.md) toont de tijdsduur tussen bezoeken van terugkerende bezoekers. Wanneer een bezoeker naar uw site terugkeert, kijkt de Adobe hoe lang geleden het vorige bezoek was, en knipt de hit in het juiste dimensie-item. Deze dimensie is nuttig om de aantrekkingskracht van uw website en de relevantie ervan voor bezoekers in de loop van de tijd te meten. Het kan ook helpen de impact van de inhoud en promoties van uw site op uw bezoekers te identificeren.

>[!TIP]
>
>Deze dimensie omvat geen nieuwe bezoekers.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

De gegevens voor deze dimensie zijn vastgesteld bij de eerste treffer van het bezoek en blijven gedurende het hele bezoek bestaan. De waarde kan het middelste bezoek niet wijzigen.

## Dimension-items

De punten van het Dimension omvatten op tijd-gebaseerde emmers, afhankelijk van verstreken tijd van hun vorig bezoek.

* Minder dan 1 dag
* 1 tot 3 dagen
* 3 tot 7 dagen
* 7 tot 14 dagen
* 14 dagen tot 1 maand
* langer dan 1 maand

## De punten van het Dimension verschijnen onder emmers buiten de de datumwaaier van het project

Wanneer u de de datumwaaier van een project plaatst, is het gemeenschappelijk om de attributen van afmetingspunten aan bezoeken buiten de datumwaaier te zien. Een bezoeker komt bijvoorbeeld in juli naar uw site en komt vervolgens twee keer terug op dezelfde dag in september. De retourfrequentie voor de maand september zou een bezoek onder &quot;langer dan 1 maand&quot; en een bezoek onder &quot;minder dan 1 dag&quot; laten zien.
