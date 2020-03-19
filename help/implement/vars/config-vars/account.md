---
title: account
description: Gebruik de accountvariabele om de rapportsuite te bepalen waarnaar gegevens worden verzonden.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# account

> [!IMPORTANT] Deze variabele wordt uitgeschakeld. Gebruik de [`s.sa()`](../functions/sa-method.md) functie als uw implementatie vereist dat u de bestemming van de rapportsuite wijzigt.

In eerdere versies van Adobe Analytics bepaalde de `account` variabele de rapportsuite waarnaar u gegevens wilt verzenden. Een rapportsuite-id is vereist om gegevens naar Adobe Analytics te verzenden.

* Als u Adobe Experience Platform Launch gebruikt, staan de rapportsuite onder de [!UICONTROL Library Management] accordeon wanneer u de extensie Adobe Analytics configureert.
* Als u de [`s_gi()`](../functions/s-gi.md) functie gebruikt om een Analytics tracking-object te instantiëren, bestaat de ID van de rapportsuite al als een vereist argument in de functie.
