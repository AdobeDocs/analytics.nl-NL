---
title: writeSecureCookies
description: Staat AppMeasurement toe om koekjes met de Veilige attributen te plaatsen.
feature: Variables
exl-id: 0e03d621-5770-4c25-981d-e4af1431ec69
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# writeSecureCookies

De `writeSecureCookies` variabele maakt AppMeasurement mogelijk om in te stellen [Beveiligde cookies](https://en.wikipedia.org/wiki/Secure_cookie) voor Analytics. Deze instelling is van toepassing op cookies van de bezoeker-id die zijn ingesteld op AppMeasurement en op cookies die u instelt met de `Util.CookieWrite()` methode. Hiervoor is AppMeasurement 2.18.0 of hoger vereist.

`writeSecureCookies` is alleen van toepassing op cookies die zijn ingesteld door AppMeasurement JavaScript (`s_fid`, `s_cc` en `s_sq`). Cookies ingesteld door `https` response (`s_vi` en `s_ecid`) kan worden ingesteld op &#39;veilig&#39; door contact op te nemen met de klantenservice van de Adobe.

Meer informatie over cookies van Analytics [hier](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html).

>[!WARNING]
>
>Als u de optie `writeSecureCookies` variabele, zorgt u ervoor dat alle inhoud op uw site veilig via HTTPS wordt aangeboden. Gegevensverzameling werkt niet goed als deze variabele is ingeschakeld en u onveilige inhoud op de pagina hebt.

## Beveiligde cookies gebruiken met de Web SDK

Als uw site het HTTPS-protocol gebruikt, wordt het kenmerk Secure ingesteld voor alle cookies die de Web SDK instelt.

## Beveiligde cookies schrijven met de Adobe Analytics-extensie

[!UICONTROL Write secure cookies] is een selectievakje onder [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL Write secure cookies] selectievakje.

## s.writeSecureCookies in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.writeSecureCookies` De variabele is een booleaanse waarde die bepaalt of het AppMeasurement het kenmerk Secure instelt bij het maken van een cookie. De standaardwaarde is `false`. Deze variabele instellen op `true` als alle inhoud op uw site veilig is en u cookies die door het AppMeasurement zijn ingesteld, het kenmerk Secure wilt hebben.

```js
s.writeSecureCookies = true;
```
