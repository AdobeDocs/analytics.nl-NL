---
title: Bezoek nummer
description: Het nde bezoek van de bezoeker.
feature: Dimensions
exl-id: daef34b3-c270-476d-a45c-a20be6138c6b
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# Bezoek nummer

Het bezoeknummer [dimensie](overview.md) meldingen die de bezoeker bezoeken, zijn momenteel ingeschakeld. Wanneer een nieuw bezoek begint, stijgt dit afmetingspunt met 1. Deze dimensie is handig wanneer u wilt begrijpen hoe betrokken bezoekers zijn bij het terugkeren naar uw site. Het is een op bezoek-gebaseerde dimensie, die betekent dat het de zelfde waarde voor het volledige bezoek bevat en niet kan veranderen. Het is op het leven van de bezoeker, ongeacht de waaier van de projectdatum van toepassing.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

Items van het Dimension bevatten de tekenreeks `"Visit number"` gevolgd door de numerieke weergave van het bezoek dat de bezoeker momenteel aanbrengt. Als de bezoeker bijvoorbeeld nog nooit eerder naar uw site is geweest, behoort het eerste bezoek tot het dimensie-item `"Visit number 1"`. Als dit het dertiende bezoek van de bezoeker aan uw plaats is, behoren zij tot het afmetingspunt `"Visit number 13"`.
