---
title: Redenen voor opt-out bijhouden
description: Hiermee wordt een voorvertoning weergegeven van de gegevens die worden uitgesloten als u Privacy-instellingen hebt ingeschakeld.
feature: Dimensions
exl-id: f0521f4f-b11e-4ce3-b0fe-60788be6b120
source-git-commit: 4c896fe930b52e440f8b91725fa6451faaa76fc8
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Redenen voor opt-out bijhouden

De dimensie &#39;Optie om te weigeren volgen&#39; fungeert als voorvertoning van gegevens die worden uitgesloten als u Privacy-instellingen hebt ingeschakeld. Deze dimensie wordt vooral gebruikt om te bepalen of uw implementatie negatief zou beïnvloeden als u toeliet [Privacy-instellingen](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html) onder Instellingen van rapportsuite.

De typische implementaties zien 1% of minder van hun algemene verkeer van de rapportreeks onder deze dimensie als de Montages van de Privacy nog niet zijn toegelaten. De percentages hoger dan 1% van al verkeer wijzen op een potentieel implementatieprobleem dat AppMeasurement verhindert eerste-partijkoekjes te plaatsen.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties die nog niet hebben toegelaten [Privacy-instellingen](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html). Als uw organisatie al het **[!UICONTROL Remove users who have blocked all cookies]** Deze dimensie bevat geen gegevens en stelt deze in voor zowel desktopbrowsers als mobiele browsers.

## Dimension-items

Dimension-items bevatten `"Cookies disabled by Desktop Browser"` en `"Cookies disabled by Mobile Browser"`.

* **Cookies uitgeschakeld door de desktopbrowser**: De bezoeker heeft cookies geblokkeerd via een desktopbrowser en **[!UICONTROL Remove users who have blocked all cookies on desktop browsers]** is uitgeschakeld.
* **Cookies uitgeschakeld door mobiele browser**: De bezoeker heeft cookies geblokkeerd via een mobiele browser en **[!UICONTROL Remove users who have blocked all cookies on mobile browsers]** is uitgeschakeld.
