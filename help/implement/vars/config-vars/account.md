---
title: account
description: Gebruik de accountvariabele om de rapportsuite te bepalen waarnaar gegevens worden verzonden.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# account

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruik de [`s.sa()`](../functions/sa-method.md) functie als uw implementatie vereist dat u de bestemming van de rapportsuite wijzigt.

In eerdere versies van Adobe Analytics bepaalde de `account` variabele de rapportsuite waarnaar u gegevens wilt verzenden. Een rapportsuite-id is vereist om gegevens naar Adobe Analytics te verzenden.

* Als u Adobe Experience Platform starten gebruikt, staan de rapportsuites onder de [!UICONTROL Library Management] accordeon wanneer u de Adobe Analytics-extensie configureert.
* Als u de [`s_gi()`](../functions/s-gi.md) functie gebruikt om een Analytics tracking-object te instantiëren, bestaat de ID van de rapportsuite al als een vereist argument in de functie.
