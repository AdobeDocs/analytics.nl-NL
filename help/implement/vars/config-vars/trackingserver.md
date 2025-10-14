---
title: trackingServer
description: Het domein dat wordt gebruikt om gegevens via HTTP naar Adobe te verzenden.
feature: Appmeasurement Implementation
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
role: Admin, Developer
source-git-commit: 35675c2e65456a175d1516dd421b80d2af809286
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# trackingServer

>[!IMPORTANT]
>
>Deze variabele is vervangen. Gebruik in plaats hiervan [`trackingServerSecure`](trackingserversecure.md) , aangezien HTTPS een prevalentie heeft.

De variabele `trackingServer` bepaalt het domein dat AppMeasurement gebruikt om gegevens via HTTP naar Adobe te verzenden. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

Vóór de [&#x200B; Dienst van de Identiteit van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/nl/docs/id-service/using/home), bepaalde deze variabele ook waar de derdekoekjes werden geplaatst. Adobe raadt ten zeerste aan de id-service waar mogelijk in alle implementaties te gebruiken.

AppMeasurement gebruikt `trackingServer` als fallback als [`trackingServerSecure`](trackingserversecure.md) niet is ingesteld. Veel oudere implementaties stellen `trackingServerSecure` niet in en gebruiken `trackingServer` als fallback op beveiligde pagina&#39;s. Met de prevalentie van HTTPS raadt Adobe aan `trackingServerSecure` waar mogelijk te gebruiken.
