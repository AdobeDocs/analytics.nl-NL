---
title: Mobiele afmetingen
description: Dimensies die zijn gebaseerd op de user-agent-tekenreeks van het apparaat.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---


# Mobiele afmetingen

*Deze pagina verwijst naar eigenschappen van mobiele apparaten die uw website openen. Zie Analytics for mobile devices[](/help/implement/mobile-device-sdk.md)implementeren in de gebruikershandleiding voor het implementeren als u apparaten wilt bijhouden op een mobiele app.*

De mobiele afmetingen bieden inzicht in de eigenschappen van mobiele apparaten die uw site bezoeken. U kunt deze afmetingen gebruiken om te begrijpen welke functies een mobiel apparaat ondersteunt.

## Deze afmetingen vullen met gegevens

Deze dimensies verwijzen naar zoekregels die intern zijn voor Adobe. De opzoekwaarde is gebaseerd op de HTTP-header die met de hit is verzonden. `User-Agent` Adobe werkt samen met [DeviceAtlas](https://deviceatlas.com/) om zoekopdrachten tussen gebruikersagent en mobiele afmetingen te onderhouden. Als u een AppMeturement-bibliotheek gebruikt (bijvoorbeeld via Adobe Experience Platform starten), werken alle mobiele afmetingen buiten het vak.

## Beschrijvingen van mobiele afmetingen

>[!NOTE]
>
>Dimensiewaarden met label `"None"` zijn niet-mobiele apparaten. Als u een rapport wilt maken dat alleen mobiele apparaten bevat, sleept u de dimensie Mobiel apparaat naar het segmentgebied van het canvas Workspace.

* **Ondersteuning** voor mobiele audio: Bepaalt de bestandsindelingen die het apparaat kan afspelen. Voorbeelden hiervan zijn `"MP3"`, `"AAC"`en `"MIDI Monophonic"`. Waarden in deze dimensie sluiten elkaar niet uit; een enkele hit kan meerdere waarden van dimensies aangeven.
* **Mobiele drager**: Als de gebruikersagent een drager-specifiek apparaat bevat, is de drager een afmetingswaarde. Voorbeelden van waarden zijn `"Reliance Jio"`, `"Airtel"`, `"Vodafone"`en `"Verizon"`.
* **Mobiele kleurdiepte**: De kleurdiepte van het mobiele apparaat, in bits.
* **Ondersteuning voor** mobiele cookies: Hiermee wordt bepaald of het mobiele apparaat cookies ondersteunt. In dit rapport wordt niet aangegeven of de browser cookies accepteert. De waarden van de afmeting omvatten `"Supported"`, `"Not supported"`, en `"Unknown"`.
* **Mobiel apparaat**: Het mobiele apparaat dat de bezoeker gebruikt.
* **Mobiel apparaatnummer**: Hiermee wordt bepaald of het mobiele apparaat het nummer verzendt. De waarden van de afmeting omvatten `"Supported"`, `"Not supported"`, en `"Unknown"`.
* **Mobiel apparaattype**: Het type mobiel apparaat. Voorbeelden van waarden zijn `"Mobile phone"`, `"Tablet"`, `"Media player"`en `"Gaming console"`.
* **Mobiele DRM**: Het type DRM dat door het mobiele apparaat wordt ondersteund. Voorbeelden hiervan zijn `"DRM OMA forward"`, `"DRM OMA combined delivery"`en `"DRM OMA separate delivery"`.
* **Ondersteuning voor** mobiele afbeeldingen: De typen afbeeldingen die door een mobiel apparaat worden ondersteund. Voorbeelden hiervan zijn `"PNG"`, `"JPEG"`en `"GIF 87"`. Waarden in deze dimensie sluiten elkaar niet uit; een enkele hit kan meerdere waarden van dimensies aangeven.
* **Mobiele informatiediensten**: De soorten nieuwsdiensten die door het apparaat worden gesteund. Recente apparaten rapporteren deze informatie doorgaans niet.
* **Mobiele Java VM**: De versies van Java die het apparaat ondersteunt.
* **Versiering** van mobiele post: Hiermee wordt bepaald of het apparaat Decomail ondersteunt, een functie die ooit populair is op Japanse apparaten.
* **Mobiele fabrikant**: Groepeert mobiele apparaten op fabrikant. Voorbeelden van waarden zijn `"Apple"`, `"Samsung"`, `"Huawei"`en `"Motorola"`.
* **Maximale lengte** van mobiele bladwijzer: Het maximumaantal bytes dat het mobiele apparaat ondersteunt in URL&#39;s met bladwijzer. Recente apparaten hebben doorgaans geen limiet.
* **Maximale lengte** URL browser: Het maximumaantal bytes dat het mobiele apparaat ondersteunt in URL&#39;s. Recente apparaten hebben doorgaans geen limiet.
* **Maximale e-maillengte** voor mobiele apparaten: Het maximumaantal bytes dat het mobiele apparaat in een e-mail ondersteunt. Recente apparaten hebben doorgaans geen limiet.
* **Mobiele netprotocollen**: De typen protocollen die het apparaat ondersteunt bij internettoegang. Voorbeelden van waarden zijn `"EDGE"`, `"GPRS"`, `"UMTS"`en `"LTE"`.
* **Mobiel besturingssysteem (afgekeurd)**: Gebruik in plaats hiervan de dimensie van het [besturingssysteem](operating-systems.md) .
* **Mobiele druk om te spreken**: Hiermee wordt bepaald of het apparaat PTT (Push to Talk) ondersteunt, waardoor het mobiele apparaat zich kan gedragen zoals een 2-wegsradio. Deze functie wordt gewoonlijk niet gerapporteerd door recente apparaten.
* **Hoogte** mobiel scherm: De hoogte van het scherm, in pixels. iPhone rapporteert altijd `"480"` omdat het niet mogelijk is de versie van het iPhone-apparaat te bepalen. Zie de onderstaande sectie over het bepalen van de versie van iPhone-apparaten.
* **Grootte** mobiel scherm: De volledige afmetingen van het mobiele apparaat in pixels. De gerapporteerde schermgrootte geeft de oriëntatie van het apparaat niet aan. Ongeacht de schermoriëntatie heeft elk apparaat een vaste schermresolutie in het rapport. Deze grootte is gebaseerd op onderzoek dat bepaalt welke oriëntatie waarschijnlijker is. U kunt formaten zoals `"768x1024"` en `"1024x768"` in het zelfde rapport zien met elke grootte die één of meerdere verschillende apparaten vertegenwoordigt.
* **Breedte** van mobiel scherm: De breedte van het scherm, in pixels.
* **Ondersteuning voor** mobiele video: De videobestandsindelingen en codecs die het mobiele apparaat ondersteunt. Er bestaan verschillende waarden voor afmetingen voor verschillende codecs van MP4- en 3GPP-bestanden. Waarden in deze dimensie sluiten elkaar niet uit; een enkele hit kan meerdere waarden van dimensies aangeven.

## iPhone scheiden op model of versie

De mobiele apparaten melden hun ingebouwde programmatuurversie in het koord van de gebruikersagent, niet de apparatenversie. Een huidige iPhone bevat bijvoorbeeld een identieke gebruikersagent als de iPhone van de laatste generatie als deze zich in dezelfde firmware-versie bevindt. Aangezien er geen manier is om de apparaatversie van een iPhone te bepalen met behulp van JavaScript, behoren alle iPhones tot hetzelfde emmertje. De mobiele afmetingen zijn strikt gebaseerd op raadplegingen die gebruikersagent van verwijzingen voorzien, zodat zult u zien dat alle iPhones een mobiele het schermgrootte van melden `320 x 480`.

Als u de versie van een iPhone-apparaat wilt verzamelen, kunt u deze beperking op twee manieren omzeilen.

* **De iOS SDK** gebruiken: De mobiele SDK bevat afmetingen die de apparaatversie beschikbaar maken voor gebruik in de rapportage. Deze methode is ideaal voor mobiele apps dan voor websites.
* **Andere variabelen gebruiken die beschikbaar zijn via JavaScript**: Sommige variabelen, zoals `screen.height` en `screen.width`, kunnen worden gebruikt om apparaatversie af te leiden. U kunt bijvoorbeeld het volgende codefragment op uw site gebruiken:

   ```js
   if (navigator.userAgent.indexOf('iPhone') > -1) {
     s.eVarXX = screen.width + "x" + screen.height;
     }
   ```

   Dit codeblok detecteert eerst of het apparaat een iPhone is. Als dit het geval is, gebruikt de code JavaScript om de schermresolutie in een eVar te trekken. Met deze methode kunt u de apparaatversie detecteren als schermresoluties uniek zijn.
