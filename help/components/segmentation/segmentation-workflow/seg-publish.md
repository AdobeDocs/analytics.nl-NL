---
description: Hiermee kunt u het segment gebruiken voor marketingactiviteiten in de Audience Library, Target en Audience Manager.
title: Segmenten publiceren naar Experience Cloud
feature: Segmentation
exl-id: 0215f896-d3f8-42cc-ac8d-8a94b009927b
source-git-commit: 5ef087f1fa4f55b98e9160bc90b8d10c6709a425
workflow-type: tm+mt
source-wordcount: '1241'
ht-degree: 0%

---

# Segmenten publiceren naar Experience Cloud

Als u een Adobe Analytics-segment naar Experience Cloud publiceert, kunt u het segment gebruiken voor marketingactiviteiten in [!DNL Audience Manager] en in andere activeringskanalen, waaronder de Adobe [!DNL Advertising Cloud], [!DNL Target] en [!DNL Campaign]. Recente updates hebben de publicatieworkflow aanzienlijk geoptimaliseerd. U kunt de segmenten Analytics nu binnen 8 uur naar het Experience Cloud publiceren. Gebruik deze segmenten om publiek in Audience Manager aan alle stroomafwaartse bestemmingen te activeren.

We hebben ook het maximumaantal publiceerbare Adobe Analytics-segmenten verhoogd naar 75 (van 20). U kunt gepubliceerde segmenten weergeven in [!UICONTROL Analytics > Components > Segments].

Bekijk deze video voor meer informatie:

>[!VIDEO](https://video.tv.adobe.com/v/32842/?quality=12)

>[!NOTE]
>
>Adobe Campaign (Classic en Standard) gedraagt zich anders in die zin dat er een extra latentie van 24 uur bovenop de 8-uurs latentie ontstaat.

## Vereisten

* Zorg ervoor dat de rapportsuite waarin u dit segment opslaat [ingeschakeld voor Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/t-publish-audience-segment.html). Anders kunt u het niet naar het Experience Cloud publiceren.
* Zorg ervoor dat uw organisatie Experience Cloud-id&#39;s gebruikt.
* Voordat u segmenten kunt publiceren, moet uw beheerder de opdracht [!UICONTROL Segment Publishing] toestemming voor een productprofiel in het dialoogvenster [Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html)en voegt u toe aan het productprofiel.

## Overwegingen

* **Limieten van rapportsuite**: U kunt maximaal 75 segmenten per rapportsuite publiceren. Deze limiet geldt. Als u al 75 gepubliceerde segmenten hebt, kunt u geen extra segmenten publiceren tot u unpublish genoeg segmenten om onder de 75-segmentdrempel te krijgen.
* **Lidmaatschapgrenzen**: publiek gedeeld aan de [!DNL Experience Cloud] uit Adobe Analytics mogen niet meer dan 20 miljoen unieke leden tellen.
* **Gegevensprivacy**: Soorten publiek worden niet gefilterd op basis van de verificatiestatus van een bezoeker. Als een bezoeker in een niet-geverifieerde en geverifieerde status door uw site kan bladeren, kan een bezoeker door handelingen die plaatsvinden wanneer een bezoeker niet-geverifieerd is, toch worden opgenomen in een publiek. Controleren [Adobe Experience Cloud-privacy](https://www.adobe.com/privacy/experience-cloud.html) inzicht te krijgen in de volledige implicaties van het delen van publiek .
* Voor een debat over de **verschillen tussen segmenten [!DNL Adobe Analytics] en[!DNL Audience Manager]**, go [hier](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html).

## Tijdlijn voor segmentpublicatie

| Beschikbaar | Wanneer deze beschikbaar is | Waar beschikbaar |
|---|---|---|
| Metagegevens (segmenttitel en -definitie) | Onmiddellijk na publicatie | [!DNL Audience Manager], [!UICONTROL Experience Cloud Audience Library], [!DNL Target] |
| Nuttig segment met lidmaatschap | ~ 8 uur na publicatie | Bezoekerprofiel Viewer in [!DNL Audience Manager] |
| Treinen en lidmaatschapsbevolking | Binnen 24-48 uur | [!DNL Audience Manager] |

>[!NOTE]
>Eenmaal per week worden alle gegevens volledig gesynchroniseerd om rekening te houden met eventuele delta&#39;s of discrepanties die in de voorgaande week niet zijn vastgelegd.

## Segmenten publiceren in [!UICONTROL Segment Builder]

1. Navigeren naar **[!UICONTROL Analytics > Workspace > Components > Segments]> +**
1. Een segment maken in het dialoogvenster [!UICONTROL Segment Builder].
1. Geef een titel en een beschrijving voor het segment op. U kunt het segment dan niet opslaan.
1. Controleren **[!UICONTROL Publish this segment to the Experience Cloud (for *rapportsuite *)]**.

![Experience Cloud publiceren](assets/publish-ec.png)

>[!IMPORTANT]
>Zorg ervoor dat u &quot;Bezoekers met Experience Cloud-id&quot; gebruikt wanneer u segmentvoorvertoningen bekijkt in Analytics in plaats van de totale segmentvoorvertoning &quot;unieke bezoekers&quot; wanneer u Adobe Analytics-nummers vergelijkt met Audience Manager-nummers:
>
>![Bezoekers segmenteren met ECID](assets/seg-vis-ecid.png)

| Element | Beschrijving |
|---|---|
| **[!UICONTROL Publish this segment to the Experience Cloud (for *`<report suite>`*)]** | Wanneer deze optie wordt toegelaten, worden de segmenttitel en de definitie (d.w.z. het shell publiek zoals vaak gebruikt in advertentieplatforms) onmiddellijk gedeeld met Experience Cloud, terwijl het segmentlidmaatschap wordt geëvalueerd en om de 4 uur gedeeld. <br> Wanneer dat publiek is gekoppeld aan een activiteit in [!DNL Target], bijvoorbeeld [!DNL Analytics] begint met het verzenden van id&#39;s voor bezoekers die voor dat Experience Cloud in aanmerking komen en [!DNL Target] publiek. Op dat punt worden de publieksnaam en de bijbehorende gegevens weergegeven op het tabblad [!DNL Audience Library] pagina in Experience Cloud. </br> |
| **[!UICONTROL Audience Creation Window]** | Het tijdkader dat u selecteert, wordt gebruikt om het publiek te maken op basis van een rolkalender. Bijvoorbeeld, &quot;Laatste 30 dagen&quot;(gebrek) omvat bezoekers die voor het publiek in de laatste 30 dagen van de datum van vandaag (NIET van de originele datum hebben gekwalificeerd toen het segment werd gecreeerd.) |
| **[!UICONTROL Create in Audience Library]** | De segmenten die u maakt en publiceert, kunnen zonder vertraging beschikbaar worden gemaakt op de [!DNL Audience Library] pagina in Experience Cloud. Ze zijn niet afhankelijk van analytische updates. Deze segmenten tellen niet tegen uw grens van 75 gepubliceerde segmenten. |
| **[!UICONTROL x of 75 Published]** | Hiermee geeft u het aantal segmenten weer dat u naar het Experience Cloud hebt gepubliceerd. Klik de verbinding om een lijst van gepubliceerde segmenten en hun bijbehorende rapportreeks en eigenaar te zien. |
| **[!UICONTROL Save]** | Hiermee slaat u dit segment op. |

## Segmenten verwijderen of verwijderen

Als u een segment wilt verwijderen dat naar het Experience Cloud is gepubliceerd, moet u eerst de publicatie ongedaan maken. Als u de publicatie van een segment ongedaan wilt maken, hoeft u alleen **unclick** het selectievakje waarmee u het bestand hebt gepubliceerd.

>[!NOTE]
>
>U **kan** unpublish een segment dat momenteel in gebruik door om het even welke volgende oplossingen van de Adobe is: [!DNL Analytics] (in [!DNL Audience Analytics]), [!DNL Campaign], [!DNL Advertising Cloud] (for [!DNL Core Service] &amp; [!DNL Audience Manager] klanten) en alle andere externe partners (voor [!DNL Audience Manager] klanten). U **kan** Verwijder de publicatie van een segment dat wordt gebruikt door [!DNL Target].

## Publicatiestatus segment weergeven in het dialoogvenster [!UICONTROL Segment Manager]

1. Navigeren naar [!UICONTROL Analytics > Components > Segments].
1. Let op de nieuwe [!UICONTROL Published] kolom. Ja/Nee verwijst naar de vraag of het segment naar Experience Cloud is gepubliceerd.

![Status publiceren](assets/publish-status.png)

## De [!DNL Audience Manager] UUID

Er zijn twee manieren om de Adobe Audience Manager UUID vast te leggen die momenteel aan de browser is gekoppeld:

* Adobe Experience Cloud Debugger
* Native ontwikkelaarsprogramma in browsers (bijv. Chrome Developer Tools)

De volgende schermafbeeldingen tonen u hoe te om Adobe Audience Manager UUID op uw browser terug te winnen en het in de Kijker van het Profiel van de Bezoeker van de Audience Manager te gebruiken om spoor en segmentlidmaatschap te bevestigen.

### Methode 1: Adobe Experience Cloud Debugger gebruiken

1. Downloaden en installeren [Adobe Experience Cloud Debugger](/help/implement/validate/debugger.md) in de Chrome Web Store.
1. Start de foutopsporing wanneer u een pagina laadt.
1. Blader naar de sectie Audience Manager en zoek de Adobe Audience Manager UUID-set op de huidige browserpagina (`50814298273775797762943354787774730612` in het onderstaande voorbeeld)

![Foutopsporing](assets/debugger.jpg)

### Methode 2: Chrome Developer Tools gebruiken (of andere browsergereedschappen)

1. Chrome Developer Tools starten voordat een pagina wordt geladen
1. Laad de pagina en controleer Toepassingen > Cookies. De Adobe Audience Manager UUID moet worden ingesteld in het demdex-cookie van de andere fabrikant ([adobe.demdex.net](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html) in het onderstaande voorbeeld). De veldindex is de Adobe Audience Manager UUID die op de browser is ingesteld (`50814298273775797762943354787774730612` in het onderstaande voorbeeld).

![Chrome Developer Tools](assets/ggogle-uuid.png)

## Audience Manager gebruiken [!UICONTROL Visitor Profile Viewer]

De Adobe Audience Manager UUID in de browser wordt standaard gebruikt wanneer [!UICONTROL Visitor Profile Viewer] is geladen. Als u de resultaten voor andere gebruikers verifieert, voert u een UUID in het veld UUID in en klikt u op [!UICONTROL Refresh]. Zie [Bezoekerprofiel Viewer](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/visitor-profile-viewer.html) voor meer informatie .

![Audience Manager Profile Viewer](assets/aam-vpv.png)

## De segmentkenmerken weergeven in [!DNL Audience Manager]

In Adobe Audience Manager wordt de lijst met bezoekers met ECID&#39;s voor een bepaald segment op streamingwijze geëvalueerd, aangezien Analytics segmenten deelt met Experience Cloud.

1. In [!DNL Audience Manager], ga naar [!UICONTROL Audience Data > Traits > Analytics Traits]. Er wordt een map weergegeven voor elke serie Analytics-rapporten die is toegewezen aan uw organisatie Experience Cloud. Deze mappen (voor Traits, Segmenten en Gegevensbronnen) worden gemaakt wanneer de kernservice Profielen en Soorten publiek/Personen wordt gestart of ingericht.
1. Selecteer de map voor de rapportsuite waarin u eerder het segment hebt gemaakt waarmee u wilt delen [!DNL Audience Manager]. U zult het segment/het publiek zien u creeerde. Wanneer u een segment deelt, gebeuren er 2 dingen in [!DNL Audience Manager]:
   * Er wordt een doel gemaakt, eerst zonder gegevens erin. Ongeveer. 8 uur nadat het segment is gepubliceerd in [!DNL Analytics], wordt de lijst met ECID&#39;s genegeerd en gedeeld met [!DNL Audience Manager] en andere oplossingen voor Experiencen Cloud.

     ![Bevoegdheidsbeheerkenmerken](assets/aam-traits.png)

   * Er wordt een segment met één doel gemaakt. Het gebruikt de gegevensbron die met de rapportreeks wordt geassocieerd waar u het segment publiceerde.
   * De vervaldatum van de reis is nu ingesteld op 16 dagen (voorheen 2 dagen).

## Het segment weergeven in [!DNL Adobe Target]

De [!UICONTROL Publish this segment to the Experience Cloud] Schakel het selectievakje tijdens het maken van segmenten in Adobe Analytics in om het segment beschikbaar te maken in de aangepaste publieksbibliotheek van Adobe Target. Een segment dat in Analytics of Audience Manager wordt gecreeerd kan voor activiteiten in Doel worden gebruikt. U kunt bijvoorbeeld campagneactiviteiten maken op basis van de omzettingscijfers van Analytics en publiekssegmenten die zijn gemaakt in Analytics.

1. Klik op [!UICONTROL Audiences].
1. Op de [!UICONTROL Audiences] pagina, zoekt u het publiek dat afkomstig is van de [!DNL Experience Cloud]. Deze soorten publiek zijn beschikbaar voor gebruik in [!DNL Target] activiteiten.
