---
title: Bezoekersidentificatie met de Adobe Analytics-taguitbreiding
description: Identificeer bezoekers correct wanneer het uitvoeren van de de markeringsuitbreiding van Adobe Analytics.
source-git-commit: 98e9dc4932bd23d3e0b632705945f56c243750c5
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Bezoekersidentificatie met de Adobe Analytics-taguitbreiding

Met de Adobe Analytics-tagextensie kunt u AppMeasurement implementeren via een tagbeheerinterface. Aangezien deze tagextensie in wezen AppMeasurement onder de kap is, biedt deze vergelijkbare methoden om bezoekers te identificeren en een aparte tagextensie voor de Bezoeker-id-service vereist.

## Bezoekers identificeren aan de hand van de Bezoekersidentiteitsservice (aanbevolen)

Als u de Bezoeker-id-service wilt gebruiken met de Adobe Analytics-tagextensie, neemt u de extensie van de Experience Cloud ID-service op in de eigenschap Tag.

1. Login aan [&#x200B; experience.adobe.com &#x200B;](https://experience.adobe.com) gebruikend uw geloofsbrieven van Adobe ID.
1. Ga naar **[!UICONTROL Data Collection]** > **[!UICONTROL Tags]**.
1. Zoek de gewenste tageigenschap.
1. Navigeer naar **[!UICONTROL Extensions]** en selecteer vervolgens de tab **[!UICONTROL Catalog]** .
1. Zoek de extensie **[!UICONTROL Experience Cloud ID Service]** en selecteer vervolgens **[!UICONTROL Install]** .

De markeringsuitbreiding verkrijgt automatisch uw IMS org ID, zodat is geen extra configuratie noodzakelijk.

## Bezoekers identificeren aan de hand van het cookie `s_vi` (niet aanbevolen)

>[!IMPORTANT]
>
>Adobe raadt u af deze methode te gebruiken om bezoekers te identificeren.

Als uw organisatie de tagextensie Bezoeker-id-service niet gebruikt, gebruikt de extensie Adobe Analytics de eigen vorm van bezoekersidentificatie. Wanneer een bezoeker voor het eerst bij uw plaats aankomt, controleert de uitbreiding een [`s_vi` &#x200B;](https://experienceleague.adobe.com/nl/docs/core-services/interface/data-collection/cookies/analytics) koekje. Dit koekje wordt geplaatst bij het domein aanpassing **[!UICONTROL SSL Tracking Server]** (voor HTTPS) of **[!UICONTROL Tracking Server]** (voor HTTP) wanneer [&#x200B; vormend de markeringsuitbreiding &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/tags/extensions/client/analytics/overview).

* Als u aan het [&#x200B; Beheerde certificaatprogramma &#x200B;](https://experienceleague.adobe.com/nl/docs/core-services/interface/data-collection/adobe-managed-cert) deelneemt, zou uw het volgen server typisch een eerste-partijdomein zijn, makend `s_vi` koekjes eerste-partij.
* Als u niet deelneemt aan het Beheerde certificaatprogramma, is de trackingserver doorgaans een subdomein van `adobedc.net` , `omtrdc.net` of `2o7.net` , waardoor de `s_vi` -cookie een cookie van een andere fabrikant wordt. Vanwege de moderne privacystandaarden van browsers worden cookies van derden door de meeste browsers geweigerd. Als AppMeasurement eenmaal is geweigerd, probeert het een fallback-cookie van de eerste partij (`fid`) in te stellen.

Als u [!UICONTROL SSL Tracking Server] op de juiste wijze instelt, zijn geen verdere identificatiemaatregelen voor de bezoeker vereist.

## Bezoekers identificeren met `visitorID` (niet aanbevolen)

>[!IMPORTANT]
>
>Adobe raadt u af deze methode te gebruiken om bezoekers te identificeren.

Met de variabele **[!UICONTROL Visitor ID]** kan uw organisatie volledig onafhankelijke controle gebruiken om bezoekers te identificeren. Als u [!UICONTROL Visitor ID] instelt met behulp van een gegevenselement, moet u rekening houden met de volgende beperkingen:

* Elke treffer moet dezelfde [!UICONTROL Visitor ID] -waarde bevatten die als één bezoeker moet worden geteld.
   * Bij alle treffers waarmee het gegevenselement [!UICONTROL Visitor ID] wordt weggelaten, wordt automatisch geprobeerd een andere methode voor bezoekersidentificatie te gebruiken, waarbij deze als een afzonderlijke bezoeker worden behandeld.
   * Alle treffers die een andere [!UICONTROL Visitor ID] -waarde dan een vorige treffer bevatten, worden beschouwd als een aparte bezoeker.
   * Adobe biedt geen manier om treffers met verschillende bezoekers-id&#39;s samen te koppelen in Adobe Analytics.
* Gedeeld publiek, Analytics for Target en klantkenmerken worden niet ondersteund voor bezoekers die zijn geïdentificeerd met [!UICONTROL Visitor ID] .

Zie [`visitorID`](/help/implement/vars/config-vars/visitorid.md) voor implementatieinstructies die deze variabele gebruiken.
