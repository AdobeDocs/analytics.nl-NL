---
title: Functies en methoden
description: Leer hoe u de functies en methoden kunt gebruiken die Adobe in uw implementatie aanbiedt.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Functies en methoden

Adobe biedt verschillende functies en methoden die u in uw implementatie kunt gebruiken. Wanneer u naar deze functies of methoden verwijst, voeren deze algemene taken uit met één coderegel.

Sommige van deze enkele coderegels behoren tot de volgende categorieën:

* **Het volgen vraag**: De meest gebruikte methoden en van essentieel belang in veel implementaties. Zij omvatten de [`t()`](t-method.md) en de [`tl()`](tl-method.md) methoden.
* **Hulpprogramma**&#39;s voor meten van toepassingen: In vorige versies van AppMeasurement, moesten de implementaties hun eigen code schrijven om deze taken uit te voeren. Adobe biedt deze hulpprogrammamethoden om deze algemene taken te stroomlijnen. De hulpprogramma&#39;s van AppMeasurement omvatten [`Util.cookieRead()`](util-cookieread.md), [`Util.cookieWrite()`](util-cookiewrite.md)en [`Util.getQueryParam()`](util-getqueryparam.md).
* **Registratiefuncties**: U kunt uw eigen functies schrijven en ervoor zorgen dat AppMeasurement deze automatisch uitvoert vóór of na het verzenden van een trackingaanroep naar Adobe. Variabelen die onder deze categorie vallen, zijn [`doPlugins()`](doplugins.md), [`registerPreTrackCallback()`](registerpretrackcallback.md)en [`registerPostTrackCallback()`](registerposttrackcallback.md).
