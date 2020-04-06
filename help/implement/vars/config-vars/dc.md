---
title: dc
description: Een gepensioneerde variabele waarmee u kunt bepalen welk datacenter u wilt gebruiken.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# dc

>[!IMPORTANT] Deze variabele wordt uitgeschakeld. Gebruik [`trackingServer`](trackingserver.md) in plaats hiervan.

In eerdere versies van Adobe Analytics moest Adobe opgeven naar welk datacenter u gegevens wilt verzenden. Het verzenden van hits naar het verkeerde datacenter leidde tot gegevensverlies.

Adobe heeft deze ervaring verbeterd doordat implementaties resultaten kunnen sturen naar `sc.omtrdc.net`. Het opgeven van een datacenter is niet meer nodig.
