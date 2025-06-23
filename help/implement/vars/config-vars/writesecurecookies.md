---
title: writeSecureCookies
description: Hiermee staat u AppMeasurement toe cookies in te stellen met het kenmerk Secure.
feature: Appmeasurement Implementation
exl-id: 0e03d621-5770-4c25-981d-e4af1431ec69
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# writeSecureCookies

De `writeSecureCookies` variabele staat AppMeasurement toe om [ Veilige koekjes ](https://en.wikipedia.org/wiki/Secure_cookie) voor Analytics te plaatsen. Deze instelling is van toepassing op cookies van de bezoeker-id die zijn ingesteld door AppMeasurement en op cookies die u instelt met de methode `Util.CookieWrite()` . Hiervoor is AppMeasurement 2.18.0 of hoger vereist.

`writeSecureCookies` is alleen van toepassing op cookies die zijn ingesteld door AppMeasurement JavaScript (`s_fid` , `s_cc` en `s_sq`). Cookies die zijn ingesteld door `https` response (`s_vi` en `s_ecid`) kunnen worden ingesteld op &#39;secure&#39; door contact op te nemen met de klantenservice van Adobe.

Leer meer over de koekjes van Analytics [ hier ](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=nl-NL).

>[!WARNING]
>
>Als u de variabele `writeSecureCookies` inschakelt, moet u ervoor zorgen dat alle inhoud op uw site veilig via HTTPS wordt aangeboden. Gegevensverzameling werkt niet goed als deze variabele is ingeschakeld en u onveilige inhoud op de pagina hebt.

## Beveiligde cookies gebruiken met de Web SDK

Als uw site het HTTPS-protocol gebruikt, wordt het kenmerk Secure ingesteld voor alle cookies die de Web SDK instelt.

## Beveiligde cookies schrijven met de Adobe Analytics-extensie

[!UICONTROL Write secure cookies] is een selectievakje onder de accordeon van [!UICONTROL Cookies] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Cookies] uit, zodat het selectievakje [!UICONTROL Write secure cookies] zichtbaar wordt.

## s.writeSecureCookies in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.writeSecureCookies` is een Booleaanse waarde die bepaalt of AppMeasurement het kenmerk Secure instelt bij het maken van een cookie. De standaardwaarde is `false` . Stel deze variabele in op `true` als alle inhoud op uw site veilig is en u wilt dat cookies die door AppMeasurement zijn ingesteld het kenmerk Secure hebben.

```js
s.writeSecureCookies = true;
```
