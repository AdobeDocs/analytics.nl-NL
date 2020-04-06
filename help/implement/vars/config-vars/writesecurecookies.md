---
title: writeSecureCookies
description: Hiermee staat u toe dat AppMeasurement cookies instelt met het kenmerk Secure.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# writeSecureCookies

Met de `writeSecureCookies` variabele kan AppMeasurement [veilige cookies](https://en.wikipedia.org/wiki/Secure_cookie) instellen voor Analytics. Deze instelling is van toepassing op zowel cookies van de bezoeker-id die zijn ingesteld door AppMeasurement als op cookies die u met de `Util.CookieWrite()` methode hebt ingesteld. Hiervoor is AppMeasurement 2.18.0 of hoger vereist.

>[!IMPORTANT] Als u de `writeSecureCookies` variabele inschakelt, moet u ervoor zorgen dat alle inhoud op uw site veilig via HTTPS wordt aangeboden. AppMeasurement werkt niet als deze variabele wordt toegelaten en u onveilige inhoud op uw pagina hebt.

## Beveiligde cookies schrijven in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.writeSecureCookies in AppMeasurement en Launch, aangepaste code-editor

De `s.writeSecureCookies` variabele is een Booleaanse waarde die bepaalt of AppMeturement het kenmerk Secure instelt bij het maken van een cookie. De standaardwaarde is `false`. Stel deze variabele in op `true` als alle inhoud op uw site veilig is en u cookies die door AppMeasurement zijn ingesteld, het kenmerk Secure wilt laten gebruiken.

```js
s.writeSecureCookies = true;
```
