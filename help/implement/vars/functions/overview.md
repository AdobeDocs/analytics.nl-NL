---
title: Functies en methoden
description: Leer hoe u de functies en methoden kunt gebruiken die Adobe in uw implementatie aanbiedt.
feature: Variables
exl-id: 9ef5bd92-fae1-4fe4-90ea-c735e8ff4b9c
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Functies en methoden

Adobe biedt verschillende functies en methoden die u in uw implementatie kunt gebruiken. Wanneer u naar deze functies of methoden verwijst, voeren deze algemene taken uit met één coderegel.

Sommige van deze enkele coderegels behoren tot de volgende categorieën:

* **Het volgen vraag**: De meest gebruikte methoden en van essentieel belang in veel implementaties. Hieronder vallen de [`t()`](t-method.md) en [`tl()`](tl-method.md) methoden.
* **Hulpprogramma&#39;s voor AppMeasurementen**: In vorige versies van AppMeasurement moesten implementaties hun eigen code schrijven om deze taken uit te voeren. De Adobe verstrekt deze nutsmethodes om deze gemeenschappelijke taken te stroomlijnen. AppMeasurement-hulpprogramma&#39;s omvatten [`Util.cookieRead()`](util-cookieread.md), [`Util.cookieWrite()`](util-cookiewrite.md), en [`Util.getQueryParam()`](util-getqueryparam.md).
* **Functies registreren**: U kunt uw eigen functies schrijven en AppMeasurement hebben automatisch hen uitvoeren vóór of na het verzenden van een volgende vraag aan Adobe. Variabelen die onder deze categorie vallen, zijn: [`doPlugins()`](doplugins.md), [`registerPreTrackCallback()`](registerpretrackcallback.md), en [`registerPostTrackCallback()`](registerposttrackcallback.md).
