---
title: Bezoek nummer
description: Het nde bezoek van de bezoeker.
translation-type: tm+mt
source-git-commit: 05ea2778cd5cd324c660fd0f1d2ac02373829f0f
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# Bezoek nummer

De dimensierapporten &#39;Visitenummer&#39; die de bezoeker bezoeken, zijn momenteel in gebruik. Wanneer een nieuw bezoek begint, stijgt deze afmetingswaarde met 1. Deze dimensie is handig wanneer u wilt begrijpen hoe betrokken bezoekers zijn bij het terugkeren naar uw site. Het is een op bezoek-gebaseerde dimensie, die betekent dat het de zelfde waarde voor het volledige bezoek bevat en niet kan veranderen. Het is op het leven van de bezoeker, ongeacht de waaier van de projectdatum van toepassing.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimensiewaarden

Tot de waarden van de afmeting behoren de tekenreeks `"Visit number"` gevolgd door de numerieke weergave van het bezoek dat de bezoeker momenteel aandoet. Als de bezoeker bijvoorbeeld nog nooit eerder naar uw site is geweest, behoort het eerste bezoek tot de waarde voor de dimensie `"Visit number 1"`. Als dit het dertiende bezoek van de bezoeker aan uw plaats is, behoren zij tot de afmetingswaarde `"Visit number 13"`.
