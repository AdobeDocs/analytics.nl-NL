---
title: Functies en methoden
description: Leer hoe u de functies en methoden kunt gebruiken die Adobe in uw implementatie aanbiedt.
feature: Appmeasurement Implementation
exl-id: 9ef5bd92-fae1-4fe4-90ea-c735e8ff4b9c
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Functies en methoden

Adobe biedt verschillende functies en methoden die u in uw implementatie kunt gebruiken. Wanneer u naar deze functies of methoden verwijst, voeren deze algemene taken uit met één coderegel.

Sommige van deze enkele coderegels behoren tot de volgende categorieën:

* **het Volgen vraag**: De gemeenschappelijkste methodes, en essentieel in vele implementaties. Deze omvatten de methoden [`t()`](t-method.md) en [`tl()`](tl-method.md) .
* **de nut van AppMeasurement**: In vorige versies van AppMeasurement, moesten de implementaties hun eigen code schrijven om deze taken uit te voeren. Adobe biedt deze hulpprogrammamethoden om deze algemene taken te stroomlijnen. AppMeasurement-hulpprogramma&#39;s zijn [`Util.cookieRead()`](util-cookieread.md) , [`Util.cookieWrite()`](util-cookiewrite.md) en [`Util.getQueryParam()`](util-getqueryparam.md) .
* **functies van het Register**: U kunt uw eigen functies schrijven en AppMeasurement hebben automatisch hen vóór of na het verzenden van een volgende vraag naar Adobe uitvoeren. Variabelen die onder deze categorie vallen, zijn [`doPlugins()`](doplugins.md), [`registerPreTrackCallback()`](registerpretrackcallback.md) en [`registerPostTrackCallback()`](registerposttrackcallback.md) .
