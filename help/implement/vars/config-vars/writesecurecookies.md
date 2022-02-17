---
title: writeSecureCookies
description: Hiermee staat u toe dat AppMeasurement cookies instelt met het kenmerk Secure.
feature: Variables
exl-id: 0e03d621-5770-4c25-981d-e4af1431ec69
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# writeSecureCookies

De `writeSecureCookies` met variabele kan AppMeasurement worden ingesteld [Beveiligde cookies](https://en.wikipedia.org/wiki/Secure_cookie) voor Analytics. Deze instelling is van toepassing op zowel cookies van de bezoeker-id die zijn ingesteld door AppMeasurement als op cookies die u instelt met de `Util.CookieWrite()` methode. Hiervoor is AppMeasurement 2.18.0 of hoger vereist.

`writeSecureCookies` is alleen van toepassing op cookies die zijn ingesteld door AppMeasurement JavaScript (`s_fid`, `s_cc` en `s_sq`). Cookies ingesteld door `https` response (`s_vi` en `s_ecid`) kan worden ingesteld op &#39;veilig&#39; door contact op te nemen met de klantenservice van Adobe.

Meer informatie over cookies van Analytics [hier](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html).

>[!IMPORTANT]
>
>Als u de optie `writeSecureCookies` variabele, zorgt u ervoor dat alle inhoud op uw site veilig via HTTPS wordt aangeboden. AppMeasurement werkt niet als deze variabele wordt toegelaten en u onveilige inhoud op uw pagina hebt.

## Beveiligde cookies schrijven met tags in Adobe Experience Platform

[!UICONTROL Write secure cookies] is een selectievakje onder [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder Adobe Analytics.
4. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL Write secure cookies] selectievakje.

## s.writeSecureCookies in AppMeasurement en aangepaste code-editor

De `s.writeSecureCookies` De variabele is een booleaanse waarde die bepaalt of AppMeasurement het kenmerk Secure instelt bij het maken van een cookie. De standaardwaarde is `false`. Deze variabele instellen op `true` als alle inhoud op uw site veilig is en u cookies die zijn ingesteld door AppMeasurement, het kenmerk Secure wilt laten gebruiken.

```js
s.writeSecureCookies = true;
```
