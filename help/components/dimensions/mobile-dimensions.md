---
title: Afmetingen van mobiele opzoekopdrachten
description: Dimensionen die op het IP adres en gebruikersagent van het apparaat worden gebaseerd.
feature: Dimensions
exl-id: fa460888-513d-4d14-93b1-33d308e0758a
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 0%

---

# Afmetingen van mobiele opzoekopdrachten

*Deze pagina verwijst naar de eigenschappen van mobiele apparaten die uw website openen. Zie [Afmetingen van mobiele levenscyclus](lifecycle-dimensions.md) of [Metingen over mobiele levenscyclus](../metrics/lifecycle-metrics.md) voor tracering in een mobiele app.*

Mobiele zoekopdracht [afmetingen](overview.md) biedt inzicht in de eigenschappen van mobiele apparaten die uw site bezoeken. Deze eigenschappen zijn gebaseerd op de gebruikersagent en IP adres van de slag. U kunt deze afmetingen gebruiken om te begrijpen welke functies door een mobiel apparaat worden ondersteund.

## Deze afmetingen vullen met gegevens

Deze dimensies verwijzen naar opzoekregels die intern zijn voor Adobe.

* Voor de [!UICONTROL Mobile Carrier] dimensie, Adobe partners met [Digitaal element](https://www.digitalelement.com/) het gebruiken van NetAcuity om raadplegingen tussen IP adres en mobiele drager te handhaven.
* Voor alle andere mobiele dimensies werkt de Adobe samen met [DeviceAtlas](https://deviceatlas.com/) om raadplegingen tussen gebruikersagent en elke respectieve mobiele dimensie te handhaven.

De beschikbaarheid van deze afmetingen is afhankelijk van het implementatietype:

* Voor AppMeasurementen-implementaties werken deze afmetingen buiten het vak.
* Voor de implementaties van SDK van het Web, laat toe [!UICONTROL Geo Lookup] (voor mobiele transporteur) of [!UICONTROL Device Lookup] (voor alle andere afmetingen) wanneer [configureren van een gegevensstroom](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=nl-NL).

## Beschrijvingen van mobiele afmetingen

>[!NOTE]
>
>Dimension-items met label `"None"` zijn niet-mobiele apparaten. Als u een rapport wilt maken dat alleen mobiele apparaten bevat, sleept u de dimensie Mobiel apparaat naar het segmentgebied van het canvas Workspace.

* **[!UICONTROL Mobile audio support]**: Hiermee bepaalt u de bestandsindelingen die het apparaat kan afspelen. Voorbeelden van waarden zijn `"MP3"`, `"AAC"`, en `"MIDI Monophonic"`. Waarden in deze dimensie sluiten elkaar niet uit; een enkele hit kan worden toegewezen aan meerdere dimensies-items.
* **[!UICONTROL Mobile carrier]**: De telefoon of gegevensleverancier voor het apparaat. Voorbeelden van waarden zijn `"Reliance Jio"`, `"Airtel"`, `"Vodafone"`, en `"Verizon"`.
* **[!UICONTROL Mobile color depth]**: De kleurdiepte van het mobiele apparaat, in bits.
* **[!UICONTROL Mobile cookie support]**: Hiermee wordt bepaald of cookies worden ondersteund op het mobiele apparaat. Deze dimensie geeft niet aan of de browser cookies accepteert. Tot Dimension-items behoren `"Supported"`, `"Not supported"`, en `"Unknown"`.
* **[!UICONTROL Mobile device]**: Het mobiele apparaat dat de bezoeker gebruikt.
* **[!UICONTROL Mobile device number]**: Hiermee wordt bepaald of het mobiele apparaat het nummer verzendt. Deze dimensie biedt niet het mobiele nummer zelf. Tot Dimension-items behoren `"Supported"`, `"Not supported"`, en `"Unknown"`.
* **[!UICONTROL Mobile device type]**: Het type mobiel apparaat. Voorbeelden van waarden zijn `"Mobile phone"`, `"Tablet"`, `"Media player"`, en `"Gaming console"`.
* **[!UICONTROL Mobile DRM]**: Het type DRM dat door het mobiele apparaat wordt ondersteund. Voorbeelden van waarden zijn `"DRM OMA forward"`, `"DRM OMA combined delivery"`, en `"DRM OMA separate delivery"`.
* **[!UICONTROL Mobile image support]**: De typen afbeeldingen die het mobiele apparaat ondersteunt. Voorbeelden van waarden zijn `"PNG"`, `"JPEG"`, en `"GIF 87"`. Waarden in deze dimensie sluiten elkaar niet uit; een enkele hit kan worden toegewezen aan meerdere dimensies-items.
* **[!UICONTROL Mobile information services]**: De typen nieuwsservices die door het apparaat worden ondersteund. Moderne apparaten rapporteren deze informatie doorgaans niet.
* **[!UICONTROL Mobile Java VM]**: De versies van Java die het apparaat ondersteunt.
* **[!UICONTROL Mobile mail decoration]**: Hiermee wordt bepaald of het apparaat ondersteuning biedt [Decomeren](https://en.wikipedia.org/wiki/Decome), een functie die ooit populair was op Japanse apparaten.
* **[!UICONTROL Mobile manufacturer]**: Hiermee worden mobiele apparaten geclassificeerd op fabrikant. Voorbeelden van waarden zijn `"Apple"`, `"Samsung"`, `"Huawei"`, en `"Motorola"`.
* **[!UICONTROL Mobile max bookmark length]**: Het maximum aantal bytes dat het mobiele apparaat ondersteunt in URL&#39;s met bladwijzer. Moderne apparaten hebben doorgaans geen limiet.
* **[!UICONTROL Mobile max browser URL length]**: Het maximum aantal bytes dat het mobiele apparaat ondersteunt in URL&#39;s. Moderne apparaten hebben doorgaans geen limiet.
* **[!UICONTROL Mobile max email length]**: Het maximum aantal bytes dat het mobiele apparaat in een e-mail ondersteunt. Moderne apparaten hebben doorgaans geen limiet.
* **[!UICONTROL Mobile net protocols]**: De typen protocollen die het apparaat ondersteunt bij internettoegang. Voorbeelden van waarden zijn `"EDGE"`, `"GPRS"`, `"UMTS"`, en `"LTE"`.
* **[!UICONTROL Mobile operating system (deprecated)]**: Gebruik de [Besturingssysteem](operating-systems.md) dimensie in plaats daarvan.
* **[!UICONTROL Mobile push to talk]**: Hiermee wordt bepaald of het apparaat ondersteuning biedt voor PTT (Push to Talk), waardoor het mobiele apparaat zich kan gedragen zoals een 2-wegsradio. Moderne apparaten melden deze functie meestal niet.
* **[!UICONTROL Mobile screen height]**: De hoogte van het scherm, in pixels. Rapport voor iPhones altijd `"480"` omdat iPhone-apparaatversie niet kan worden bepaald. Zie de onderstaande sectie over het bepalen van de iPhone-apparaatversie.
* **[!UICONTROL Mobile screen size]**: De volledige afmetingen van het mobiele apparaat in pixels. De gerapporteerde schermgrootte geeft de oriëntatie van het apparaat niet aan. Ongeacht de schermoriëntatie heeft elk apparaat een vaste schermresolutie in het rapport. Deze grootte is gebaseerd op onderzoek dat bepaalt welke oriëntatie waarschijnlijker is. U kunt formaten zien zoals `"768x1024"` en `"1024x768"` in hetzelfde rapport waarbij elke grootte een of meer verschillende apparaten vertegenwoordigt.
* **[!UICONTROL Mobile screen width]**: De breedte van het scherm, in pixels.
* **[!UICONTROL Mobile video support]**: De videobestandsindelingen en codecs die het mobiele apparaat ondersteunt. Er bestaan verschillende dimensieitems voor verschillende codecs van MP4- en 3GPP-bestanden. Waarden in deze dimensie sluiten elkaar niet uit; een enkele hit kan worden toegewezen aan meerdere dimensies-items.

## IPhone scheiden op model of versie

De mobiele apparaten melden hun ingebouwde programmatuurversie in het koord van de gebruikersagent, niet de apparatenversie. Een iPhone van het huidige type bevat bijvoorbeeld dezelfde gebruikersagent als iPhone van de laatste generatie als deze dezelfde firmware-versie heeft. Aangezien er geen manier is om een iPhone-apparaatversie te bepalen met JavaScript, horen alle iPhones in hetzelfde emmertje. De mobiele afmetingen zijn strikt gebaseerd op raadplegingen die gebruikersagent van verwijzingen voorzien, resulterend in alle iPhones die een mobiele het schermgrootte van tonen `320 x 480`.

Als u de iPhone-apparaatversie wilt verzamelen, kunt u deze beperking op twee manieren omzeilen.

* **De SDK voor mobiele apparaten gebruiken**: De mobiele SDK bevat afmetingen die de apparaatversie beschikbaar maken voor gebruik in rapportage. Deze methode is ideaal voor mobiele apps dan voor websites.
* **Andere variabelen gebruiken die beschikbaar zijn via JavaScript**: Sommige variabelen, zoals `screen.height` en `screen.width`, kan worden gebruikt om apparaatversie af te leiden. U kunt bijvoorbeeld het volgende codefragment op uw site gebruiken:

  ```js
  if (navigator.userAgent.indexOf('iPhone') > -1) {
    s.eVarXX = screen.width + "x" + screen.height;
    }
  ```

  Dit codeblok detecteert eerst of het apparaat een iPhone is. Als dit het geval is, gebruikt de code JavaScript om de schermresolutie in een eVar te trekken. Met deze methode kunt u de apparaatversie detecteren als schermresoluties uniek zijn.
