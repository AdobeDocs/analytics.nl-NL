---
title: writeSecureCookies
description: Hiermee staat u toe dat AppMeasurement cookies instelt met het kenmerk Secure.
translation-type: tm+mt
source-git-commit: defb701d01747685a421b89a553f47efe40f1432
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# writeSecureCookies

Met de `writeSecureCookies` variabele kan AppMeasurement [veilige cookies](https://en.wikipedia.org/wiki/Secure_cookie) instellen voor Analytics. Deze instelling is van toepassing op zowel cookies van de bezoeker-id die zijn ingesteld door AppMeasurement als op cookies die u met de `Util.CookieWrite()` methode hebt ingesteld. Hiervoor is AppMeasurement 2.18.0 of hoger vereist.

>[!IMPORTANT]
>
>Als u de `writeSecureCookies` variabele inschakelt, moet u ervoor zorgen dat alle inhoud op uw site veilig via HTTPS wordt aangeboden. AppMeasurement werkt niet als deze variabele wordt toegelaten en u onveilige inhoud op uw pagina hebt.

## Beveiligde cookies schrijven in Adobe Experience Platform Launch

[!UICONTROL Write secure cookies] is een selectievakje onder de [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Vouw de [!UICONTROL Cookies] accordeon uit, zodat het [!UICONTROL Write secure cookies] selectievakje zichtbaar wordt.

## s.writeSecureCookies in AppMeasurement en Launch, aangepaste code-editor

De `s.writeSecureCookies` variabele is een Booleaanse waarde die bepaalt of AppMeturement het kenmerk Secure instelt bij het maken van een cookie. De standaardwaarde is `false`. Stel deze variabele in op `true` als alle inhoud op uw site veilig is en u cookies die door AppMeasurement zijn ingesteld, het kenmerk Secure wilt laten gebruiken.

```js
s.writeSecureCookies = true;
```
