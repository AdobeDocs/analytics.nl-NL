---
title: Mobiele afmetingen
description: Dimension die op het IP adres van het apparaat worden gebaseerd.
feature: Dimensions
exl-id: fa460888-513d-4d14-93b1-33d308e0758a
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 0%

---

# Mobiele afmetingen

*Deze pagina verwijst naar eigenschappen van mobiele apparaten die uw website openen. Als u apparaten op een mobiele app wilt bijhouden, raadpleegt u [Analyses implementeren voor mobiele apparaten](/help/implement/mobile-device-sdk.md) in de gebruikershandleiding Implementeren.*

De mobiele afmetingen bieden inzicht in de eigenschappen van mobiele apparaten die uw site bezoeken. U kunt deze afmetingen gebruiken om te begrijpen welke functies een mobiel apparaat ondersteunt.

## Deze afmetingen vullen met gegevens

Deze dimensies verwijzen naar opzoekregels die intern zijn aan Adobe. [!UICONTROL Mobile Carrier] raadplegingen worden bepaald door IP adres, gebruikend gegevens wij van NetAcuity (een Digitaal product van Elementen) krijgen.
Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werken alle mobiele afmetingen buiten het vak.

## Beschrijvingen van mobiele afmetingen

>[!NOTE]
>
>Dimension-items met label `"None"` zijn niet-mobiele apparaten. Als u een rapport wilt maken dat alleen mobiele apparaten bevat, sleept u de dimensie Mobiel apparaat naar het segmentgebied van het canvas Workspace.

* **Ondersteuning voor mobiele audio**: Bepaalt de bestandsindelingen die het apparaat kan afspelen. Voorbeelden van waarden zijn `"MP3"`, `"AAC"`, en `"MIDI Monophonic"`. Waarden in deze dimensie sluiten elkaar niet uit; één enkele slag kan aan veelvoudige afmetingspunten toeschrijven.
* **Mobiele drager**: Waarden voor deze dimensie worden gevuld door gegevens van derden (Digital Elements) op te zoeken op basis van de IP-adressen die door Analytics zijn vastgelegd. Voorbeelden van waarden zijn `"Reliance Jio"`, `"Airtel"`, `"Vodafone"`, en `"Verizon"`.
* **Mobiele kleurdiepte**: De kleurdiepte van het mobiele apparaat, in bits.
* **Ondersteuning voor mobiele cookies**: Hiermee wordt bepaald of het mobiele apparaat cookies ondersteunt. In dit rapport wordt niet aangegeven of de browser cookies accepteert. Dimension-items bevatten `"Supported"`, `"Not supported"`, en `"Unknown"`.
* **Mobiel apparaat**: Het mobiele apparaat dat de bezoeker gebruikt.
* **Mobiel apparaatnummer**: Hiermee wordt bepaald of het mobiele apparaat het nummer verzendt. Dimension-items bevatten `"Supported"`, `"Not supported"`, en `"Unknown"`.
* **Mobiel apparaattype**: Het type mobiel apparaat. Voorbeelden van waarden zijn `"Mobile phone"`, `"Tablet"`, `"Media player"`, en `"Gaming console"`.
* **Mobiele DRM**: Het type DRM dat door het mobiele apparaat wordt ondersteund. Voorbeelden van waarden zijn `"DRM OMA forward"`, `"DRM OMA combined delivery"`, en `"DRM OMA separate delivery"`.
* **Ondersteuning voor mobiele images**: De typen afbeeldingen die door een mobiel apparaat worden ondersteund. Voorbeelden van waarden zijn `"PNG"`, `"JPEG"`, en `"GIF 87"`. Waarden in deze dimensie sluiten elkaar niet uit; één enkele slag kan aan veelvoudige afmetingspunten toeschrijven.
* **Mobiele informatiediensten**: De soorten nieuwsdiensten die door het apparaat worden gesteund. Recente apparaten rapporteren deze informatie doorgaans niet.
* **Mobile Java VM**: De versies van Java die het apparaat ondersteunt.
* **Decoratie van mobiele post**: Hiermee wordt bepaald of het apparaat Decomail ondersteunt, een functie die ooit populair is op Japanse apparaten.
* **Mobiele fabrikant**: Groepeert mobiele apparaten op fabrikant. Voorbeelden van waarden zijn `"Apple"`, `"Samsung"`, `"Huawei"`, en `"Motorola"`.
* **Maximale bladwijzerlengte voor mobiel**: Het maximumaantal bytes dat het mobiele apparaat ondersteunt in URL&#39;s met bladwijzer. Recente apparaten hebben doorgaans geen limiet.
* **Maximale URL-lengte browser**: Het maximumaantal bytes dat het mobiele apparaat ondersteunt in URL&#39;s. Recente apparaten hebben doorgaans geen limiet.
* **Maximale e-maillengte voor mobiel**: Het maximumaantal bytes dat het mobiele apparaat in een e-mail ondersteunt. Recente apparaten hebben doorgaans geen limiet.
* **Mobiele netprotocollen**: De typen protocollen die het apparaat ondersteunt bij internettoegang. Voorbeelden van waarden zijn `"EDGE"`, `"GPRS"`, `"UMTS"`, en `"LTE"`.
* **Mobiel besturingssysteem (afgekeurd)**: Gebruik de [Besturingssysteem](operating-systems.md) dimensie in plaats daarvan.
* **Mobiele druk om te praten**: Hiermee wordt bepaald of het apparaat PTT (Push to Talk) ondersteunt, waardoor het mobiele apparaat zich kan gedragen zoals een 2-wegsradio. Deze functie wordt gewoonlijk niet gerapporteerd door recente apparaten.
* **Hoogte van mobiel scherm**: De hoogte van het scherm, in pixels. Let op: iPhones rapporteren altijd `"480"` omdat iPhone-apparaatversie niet kan worden bepaald. Zie de onderstaande sectie over het bepalen van de versie van iPhone-apparaten.
* **Grootte van mobiel scherm**: De volledige afmetingen van het mobiele apparaat in pixels. De gerapporteerde schermgrootte geeft de oriëntatie van het apparaat niet aan. Ongeacht de schermoriëntatie heeft elk apparaat een vaste schermresolutie in het rapport. Deze grootte is gebaseerd op onderzoek dat bepaalt welke oriëntatie waarschijnlijker is. U kunt formaten zien zoals `"768x1024"` en `"1024x768"` in hetzelfde rapport waarbij elke grootte een of meer verschillende apparaten vertegenwoordigt.
* **Breedte van mobiel scherm**: De breedte van het scherm, in pixels.
* **Ondersteuning voor mobiele video**: De videobestandsindelingen en codecs die het mobiele apparaat ondersteunt. Er bestaan verschillende dimensieitems voor verschillende codecs van MP4- en 3GPP-bestanden. Waarden in deze dimensie sluiten elkaar niet uit; één enkele slag kan aan veelvoudige afmetingspunten toeschrijven.

## iPhone scheiden op model of versie

De mobiele apparaten melden hun ingebouwde programmatuurversie in het koord van de gebruikersagent, niet de apparatenversie. Een iPhone van het huidige type bevat bijvoorbeeld dezelfde gebruikersagent als iPhone van de laatste generatie als deze dezelfde firmware-versie heeft. Aangezien er geen manier is om een iPhone-apparaatversie te bepalen met JavaScript, horen alle iPhones in hetzelfde emmertje. De mobiele afmetingen zijn strikt gebaseerd op raadplegingen die gebruikersagent van verwijzingen voorzien, zodat zult u zien dat alle iPhones een mobiele het schermgrootte van melden `320 x 480`.

Als u iPhone-apparaatversie wilt verzamelen, kunt u deze beperking op twee manieren omzeilen.

* **De SDK van iOS gebruiken**: De mobiele SDK bevat afmetingen die de apparaatversie beschikbaar maken voor gebruik in de rapportage. Deze methode is ideaal voor mobiele apps dan voor websites.
* **Andere variabelen gebruiken die beschikbaar zijn via JavaScript**: Sommige variabelen, zoals `screen.height` en `screen.width`, kan worden gebruikt om apparaatversie af te leiden. U kunt bijvoorbeeld het volgende codefragment op uw site gebruiken:

   ```js
   if (navigator.userAgent.indexOf('iPhone') > -1) {
     s.eVarXX = screen.width + "x" + screen.height;
     }
   ```

   Dit codeblok detecteert eerst of het apparaat een iPhone is. Als dit het geval is, gebruikt de code JavaScript om de schermresolutie in een eVar te trekken. Met deze methode kunt u de apparaatversie detecteren als schermresoluties uniek zijn.
