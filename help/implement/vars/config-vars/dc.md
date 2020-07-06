---
title: dc
description: Een gepensioneerde variabele waarmee u kunt bepalen welk datacenter u wilt gebruiken.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 2%

---


# dc

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruik [`trackingServer`](trackingserver.md) in plaats hiervan.

In eerdere versies van Adobe Analytics moest Adobe opgeven naar welk datacenter u gegevens wilt verzenden. Het verzenden van hits naar het verkeerde datacenter leidde tot gegevensverlies.

Adobe heeft deze ervaring verbeterd doordat implementaties resultaten kunnen sturen naar `sc.omtrdc.net`. Het opgeven van een datacenter is niet meer nodig.
