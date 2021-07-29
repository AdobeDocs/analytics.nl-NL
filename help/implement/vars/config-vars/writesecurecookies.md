---
title: writeSecureCookies
description: Hiermee staat u toe dat AppMeasurement cookies instelt met het kenmerk Secure.
exl-id: 0e03d621-5770-4c25-981d-e4af1431ec69
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# writeSecureCookies

Met de variabele `writeSecureCookies` kan AppMeasurement [Secure cookies](https://en.wikipedia.org/wiki/Secure_cookie) instellen voor Analytics. Deze instelling is van toepassing op zowel cookies van de bezoekersidentiteitskaart die zijn ingesteld door AppMeasurement als cookies die u instelt met de methode `Util.CookieWrite()`. Hiervoor is AppMeasurement 2.18.0 of hoger vereist.

`writeSecureCookies` is alleen van toepassing op cookies die zijn ingesteld door AppMeasurement JavaScript (`s_fid`,  `s_cc` en  `s_sq`). Cookies die zijn ingesteld door de reactie `https` (`s_vi` en `s_ecid`) kunnen worden ingesteld op &#39;secure&#39; door contact op te nemen met de klantenservice van Adobe.

Meer informatie over Analytics cookies [hier](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html).

>[!IMPORTANT]
>
>Als u de variabele `writeSecureCookies` inschakelt, moet u ervoor zorgen dat alle inhoud op uw site veilig via HTTPS wordt aangeboden. AppMeasurement werkt niet als deze variabele wordt toegelaten en u onveilige inhoud op uw pagina hebt.

## Beveiligde cookies schrijven met tags in Adobe Experience Platform

[!UICONTROL Write secure cookies] is een selectievakje onder de  [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Breid [!UICONTROL Cookies] accordeon uit, die [!UICONTROL Write secure cookies] checkbox openbaart.

## s.writeSecureCookies in AppMeasurement en aangepaste code-editor

De variabele `s.writeSecureCookies` is een Booleaanse waarde die bepaalt of AppMeturement het kenmerk Secure instelt bij het maken van een cookie. De standaardwaarde is `false`. Stel deze variabele in op `true` als alle inhoud op uw site veilig is en u cookies die door AppMeasurement zijn ingesteld, het kenmerk Secure wilt laten gebruiken.

```js
s.writeSecureCookies = true;
```
