---
title: account
description: Gebruik de accountvariabele om de rapportsuite te bepalen waarnaar gegevens worden verzonden.
feature: Variables
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 1%

---

# account

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruik de [`s.sa()`](../functions/sa-method.md) functie als uw implementatie vereist dat u de bestemming van de rapportsuite wijzigt.

In eerdere versies van Adobe Analytics `account` De variabele bepaalt de rapportsuite waarnaar u gegevens wilt verzenden. Een rapportsuite-id is vereist om gegevens naar Adobe Analytics te verzenden.

* Als u tags gebruikt in Adobe Experience Platform, staan de rapportsuites onder de [!UICONTROL Library Management] accordeon bij het configureren van de Adobe Analytics-extensie.
* Als u het [`s_gi()`](../functions/s-gi.md) functie om een Analytics tracking-object te instantiëren, bestaat de id van de rapportsuite al als een vereist argument in de functie.
