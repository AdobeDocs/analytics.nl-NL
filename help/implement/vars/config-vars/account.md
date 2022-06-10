---
title: account
description: Gebruik de accountvariabele om de rapportsuite te bepalen waarnaar gegevens worden verzonden.
feature: Variables
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---

# account

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruik de [`s.sa()`](../functions/sa-method.md) functie als uw implementatie vereist dat u de bestemming van de rapportsuite wijzigt.

In eerdere versies van Adobe Analytics `account` De variabele bepaalt de rapportsuite waarnaar u gegevens wilt verzenden. Een rapportsuite-id is vereist om gegevens naar Adobe Analytics te verzenden.

* Als u SDK van het Web gebruikt, zijn de rapportreeksen in de de dienstmontages van Adobe Analytics binnen de datastream die SDK van het Web gegevens naar verzendt.
* Als u de extensie Adobe Analytics gebruikt, worden de rapportsuites onder de extensie [!UICONTROL Library Management] accordeon bij het configureren van de Adobe Analytics-extensie.
* Als u het [`s_gi()`](../functions/s-gi.md) om een Analytics tracking-object te instantiëren, bestaan de rapportsuite-id(&#39;s) al als een vereist argument in de functie.
