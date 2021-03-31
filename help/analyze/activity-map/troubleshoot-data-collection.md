---
title: Los de gegevensinzameling van de Activity Map problemen op
description: Bepalen waarom Activity Map-gegevens niet worden weergegeven in afbeeldingsaanvragen
feature: Activity Map
role: Bedrijfs Praktijk, Beheerder
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# Los de gegevensinzameling van de Activity Map problemen op

Als u geen gegevens voor Activity Map afmetingen ziet, gebruik deze pagina helpen bepalen waarom.

## Bevestig gegevensinzameling gebruikend debugger

Eerst, zorg ervoor dat AppMeasurement correct de gegevens van de Activity Map verzamelt.

1. Download en installeer de [Adobe Experience Cloud Debugger Chrome Extension](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html).
2. Navigeer naar uw webpagina en klik op een koppeling.
3. Open foutopsporing wanneer de volgende pagina wordt geladen. Valideer dat u de variabelen ziet van de Activity Map contextgegevens tussen `activitymap.` en `.activitymap`:

![Foutopsporingsgegevens](assets/debugger.png)

## Mogelijke redenen waarom er geen Activity Map-gegevens aanwezig zijn

Controleer elk van de volgende opties om te controleren of er Activity Map-componenten aanwezig zijn:

* **AppMeasurement-versie**: Activity Map wordt ondersteund op versie 1.6 en hoger. Veel problemen met randhoofdletters en kleine letters worden opgelost wanneer u een upgrade uitvoert naar de nieuwste stabiele versie van AppMeasurement.
* **Activity Map module**: Controleer of de  `AppMeasurement_Module_Activity_Map` module aanwezig is in het  `AppMeasurement.js` bestand. Als uw implementatie gebruikmaakt van Adobe Experience Platform Launch, controleert u of **[!UICONTROL Enable ClickMap]** is ingeschakeld bij het configureren van de extensie Analytics onder **[!UICONTROL Link tracking]**.
* **Het  `s_sq` cookie**: Activity Map hangt af van het  `s_sq` cookie voor gegevensverzameling.
   * Zorg ervoor dat de `cookieDomainPeriods` variabele correct wordt geplaatst, vooral voor regionale domeinen zoals `*.co.uk` of `*.co.jp`.
   * Zorg ervoor dat de `linkInternalFilters` variabele aan gewenste waarden wordt geplaatst. Als een aangeklikte koppeling niet overeenkomt met interne filters, beschouwt de Activity Map deze als een exit-koppeling en worden er geen gegevens verzameld.
* **Bedekking Activity Map wordt uitgevoerd**: AppMeasurement houdt geen klikgegevens voor uw Web-pagina bij wanneer de Activity Map bekleding wordt toegelaten.
