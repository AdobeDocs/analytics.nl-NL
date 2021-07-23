---
title: account
description: Gebruik de accountvariabele om de rapportsuite te bepalen waarnaar gegevens worden verzonden.
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 1%

---

# account

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruik de functie [`s.sa()`](../functions/sa-method.md) als uw implementatie vereist dat u de bestemming van de rapportsuite wijzigt.

In vorige versies van Adobe Analytics bepaalde de `account` variabele de rapportsuite waarnaar u gegevens wilt verzenden. Een rapportsuite-id is vereist om gegevens naar Adobe Analytics te verzenden.

* Als u tags gebruikt in Adobe Experience Platform, staan de rapportsuite onder de accordeon [!UICONTROL Library Management] wanneer u de Adobe Analytics-extensie configureert.
* Wanneer u de functie [`s_gi()`](../functions/s-gi.md) gebruikt om een object Analytics tracking te instantiëren, bestaat de id van de rapportsuite al als een vereist argument in de functie.
