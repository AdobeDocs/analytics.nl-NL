---
title: account
description: (In ruste) Bepaal de rapportsuite waarnaar gegevens worden verzonden.
feature: Appmeasurement Implementation
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# account

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruik de functie [`s.sa()`](../functions/sa-method.md) als uw implementatie vereist dat u de bestemming van de rapportsuite wijzigt.

In eerdere versies van Adobe Analytics bepaalde de variabele `account` de rapportsuite waarnaar u gegevens wilt verzenden. Een rapportsuite-id is vereist om gegevens naar Adobe Analytics te verzenden.

* Als u het Web SDK gebruikt, zijn de rapportreeksen in de de dienstmontages van Adobe Analytics binnen de Datasstream die SDK van het Web gegevens naar verzendt.
* Als u de Adobe Analytics-extensie gebruikt, staan de rapportsuite onder de accordeon [!UICONTROL Library Management] wanneer u de Adobe Analytics-extensie configureert.
* Als u de functie [`s_gi()`](../functions/s-gi.md) gebruikt om een object Analytics tracking te instantiëren, bestaan de id(&#39;s) van de rapportsuite al als een vereist argument in de functie.
