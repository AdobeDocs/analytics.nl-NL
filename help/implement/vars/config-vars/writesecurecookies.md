---
title: writeSecureCookies
description: Hiermee staat u toe dat AppMeasurement cookies instelt met het kenmerk Secure.
exl-id: 0e03d621-5770-4c25-981d-e4af1431ec69
source-git-commit: b93cd06c2a8867f4848dc317e426b73dcfbb5dfd
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 1%

---

# writeSecureCookies

Met de variabele `writeSecureCookies` kan AppMeasurement [Secure cookies](https://en.wikipedia.org/wiki/Secure_cookie) instellen voor Analytics. Deze instelling is van toepassing op zowel cookies van de bezoekersidentiteitskaart die zijn ingesteld door AppMeasurement als cookies die u instelt met de methode `Util.CookieWrite()`. Hiervoor is AppMeasurement 2.18.0 of hoger vereist.

`writeSecureCookies` is alleen van toepassing op cookies die zijn ingesteld door AppMeasurement JavaScript (`s_fid`,  `s_cc` en  `s_sq`). Cookies die zijn ingesteld door de reactie `https` (`s_vi` en `s_ecid`) kunnen worden ingesteld op &#39;secure&#39; door contact op te nemen met de klantenservice van Adobe.

Meer informatie over Analytics cookies [hier](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html).

>[!IMPORTANT]
>
>Als u de variabele `writeSecureCookies` inschakelt, moet u ervoor zorgen dat alle inhoud op uw site veilig via HTTPS wordt aangeboden. AppMeasurement werkt niet als deze variabele wordt toegelaten en u onveilige inhoud op uw pagina hebt.

## Beveiligde cookies schrijven in Adobe Experience Platform Launch

[!UICONTROL Write secure cookies] is een selectievakje onder de  [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Breid [!UICONTROL Cookies] accordeon uit, die [!UICONTROL Write secure cookies] checkbox openbaart.

## s.writeSecureCookies in AppMeasurement en Launch, aangepaste code-editor

De variabele `s.writeSecureCookies` is een Booleaanse waarde die bepaalt of AppMeturement het kenmerk Secure instelt bij het maken van een cookie. De standaardwaarde is `false`. Stel deze variabele in op `true` als alle inhoud op uw site veilig is en u cookies die door AppMeasurement zijn ingesteld, het kenmerk Secure wilt laten gebruiken.

```js
s.writeSecureCookies = true;
```
