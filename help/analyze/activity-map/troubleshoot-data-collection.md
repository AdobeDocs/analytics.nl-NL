---
title: Los de gegevensinzameling van de Activity Map problemen op
description: Bepalen waarom Activity Map-gegevens niet worden weergegeven in afbeeldingsaanvragen
feature: Activity Map
role: User, Admin
exl-id: 7f9e06ba-4040-483b-b18b-cdfe85bca486
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Los de gegevensinzameling van de Activity Map problemen op

Als u geen gegevens voor Activity Map afmetingen ziet, gebruik deze pagina helpen bepalen waarom.

## Bevestig gegevensinzameling gebruikend debugger

Eerst, zorg ervoor dat AppMeasurement correct de gegevens van de Activity Map verzamelt.

1. Download en installeer de [Adobe Experience Cloud Debugger Chrome Extension](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html).
2. Navigeer naar uw webpagina en klik op een koppeling.
3. Open foutopsporing wanneer de volgende pagina wordt geladen. Valideer dat u de variabelen ziet van de Activity Map contextgegevens tussen `activitymap.` en `.activitymap`:

![Foutopsporingsgegevens](assets/debugger.png)

## Mogelijke redenen waarom er geen Activity Map-gegevens aanwezig zijn

Controleer elk van de volgende opties om te controleren of er Activity Map-componenten aanwezig zijn:

* **AppMeasurement-versie**: Activity Map wordt ondersteund op versie 1.6 en hoger. Veel problemen met randhoofdletters en kleine letters worden opgelost wanneer u een upgrade uitvoert naar de nieuwste stabiele versie van AppMeasurement.
* **Activity Map module**: Controleer of de  `AppMeasurement_Module_Activity_Map` module aanwezig is in het  `AppMeasurement.js` bestand. Als uw implementatie Adobe Experience Platform gebruikt om gegevens te verzamelen, moet **[!UICONTROL Enable ClickMap]** worden gecontroleerd bij het configureren van de extensie Analytics onder **[!UICONTROL Link tracking]**.
* **Het  `s_sq` cookie**: Activity Map hangt af van het  `s_sq` cookie voor gegevensverzameling.
   * Zorg ervoor dat de `cookieDomainPeriods` variabele correct wordt geplaatst, vooral voor regionale domeinen zoals `*.co.uk` of `*.co.jp`.
   * Zorg ervoor dat de `linkInternalFilters` variabele aan gewenste waarden wordt geplaatst. Als een aangeklikte koppeling niet overeenkomt met interne filters, beschouwt de Activity Map deze als een exit-koppeling en worden er geen gegevens verzameld.
* **Bedekking Activity Map wordt uitgevoerd**: AppMeasurement houdt geen klikgegevens voor uw Web-pagina bij wanneer de Activity Map bekleding wordt toegelaten.
