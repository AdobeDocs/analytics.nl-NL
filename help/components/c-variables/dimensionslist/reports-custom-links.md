---
description: Hiermee geeft u de koppelingen weer waarnaar bezoekers van uw site de voorkeur geven. De startpagina voor uw site bevat bijvoorbeeld waarschijnlijk meerdere koppelingen die dezelfde pagina weergeven. Misschien is er zowel een grafische als een tekstkoppeling die beide aan dezelfde pagina koppelen. In dit rapport wordt aangegeven welk percentage bezoekers de grafische koppeling en de tekstkoppeling hebben gebruikt.
title: Aangepaste koppeling
topic: Reports
uuid: 2e0d0175-d5e4-4919-b601-3f488ef3e090
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Aangepaste koppeling

Hiermee geeft u de koppelingen weer waarnaar bezoekers van uw site de voorkeur geven. De startpagina voor uw site bevat bijvoorbeeld waarschijnlijk meerdere koppelingen die dezelfde pagina weergeven. Misschien is er zowel een grafische als een tekstkoppeling die beide aan dezelfde pagina koppelen. In dit rapport wordt aangegeven welk percentage bezoekers de grafische koppeling en de tekstkoppeling hebben gebruikt.

De specifieke koppelingen die u wilt bijhouden, moeten worden gewijzigd met speciale codes. Zie [Koppeling bijhouden](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html).

U kunt het volgende gebruiken [!UICONTROL Custom Links Report] :

* Optimaliseer uw siteontwerp door te weten welke typen koppelingen uw bezoekers verkiezen
* Valideer de behoefte aan overtollige verbindingen aan enige pagina&#39;s

## Mobiele SDK-koppelingsnamen {#section_70C91FE794104B5FBF289B19CC02EA8E}

De [mobiele SDK&#39;s](https://marketing.adobe.com/resources/help/en_US/mobile/home.html) gebruiken aangepaste koppelingen om handelingen en levenscyclusmetriek bij te houden. In rapportsuites die worden gebruikt om mobiele apps te meten, zou u de volgende verbindingsnamen kunnen zien die door SDK worden geplaatst:

| ADBINTERN:levenscyclus | Verzonden door de levenscyclusvraag in 4.x SDKs. |
|---|---|
| AMACTION:[actienaam] | Verzonden door de trackAction()-methode in de 4.x SDK&#39;s, waarbij de naam van de handeling de naam is die is ingesteld toen de methode werd aangeroepen. |
| ADMS BP-gebeurtenis | Verzonden door de levenscyclusvraag in 3.x SDKs. |

