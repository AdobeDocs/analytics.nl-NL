---
description: Hoe te met statische rijen in lijsten in wisselwerking te staan.
title: Statische versus dynamische rijen
uuid: caf033ef-d252-4f8a-802e-7edbbac5c8c0
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Statische versus dynamische rijen

De lijsten van de Werkruimte van de analyse produceren &quot;dynamische&quot;rijen wanneer u een afmeting in de lijst laat vallen - betekenend dat alle punten die aan de afmeting, voor bepaalde metrisch beantwoorden, in de lijst worden getrokken.

Wanneer u bijvoorbeeld de afmetingen van de browser naar de tabel sleept, worden alle bijbehorende dimensies (bijvoorbeeld Android-browser, Mobile Safari, Firefox, enz.) dynamisch in de tabel worden geplaatst.

Als u daarentegen handmatig een specifieke metrische, segment-, gegevensbereik- of afzonderlijke dimensie-item in een tabel selecteert en neerzet, is het resultaat een hardcodeerde of &quot;statische&quot; rij of lijst. U kunt nu op de volgende manieren werken met een statische rij:

* Klik op het pictogram Voorvertoning in statische rijen, zodat u een voorvertoning kunt weergeven van segmenten, maateenheden en datumbereiken.
* Klik op het pictogram &quot;x&quot; om die rij uit de tabel te verwijderen.
* Beperk het aantal rijen dat wordt weergegeven en schakel paginering in.
* Voeg &quot;items met gemengde dimensies&quot; toe. Voeg bijvoorbeeld een item uit een browserdimensie en een ander item uit een productdimensie toe.

   Hier volgt een illustratie:

   ![](assets/static_rows.png)

Bovendien (slechts) wanneer u op een statische rijwijze bent, kunt u nu veranderen hoe de kolomtotalen worden berekend. Klik op het tandwielpictogram en schakel tussen deze twee opties:

![](assets/column-totals.png)

| Option | Beschrijving |
|---|---|
| (Standaard) Bereken totalen door de waarden op te tellen die momenteel in elke kolom staan. | Met deze optie worden alleen de rijen berekend die momenteel in de tabel staan. (Clientberekening) |
| Bereken totalen die op alle rijen voor elke metrisch worden gebaseerd. | Deze optie omvat alle afmetingspunten voor deze afmeting, zelfs die niet vermeld in de lijst. (Server-side berekening) |

