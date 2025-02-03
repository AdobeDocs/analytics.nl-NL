---
description: Hiermee kunt u het segment gebruiken voor marketingactiviteiten in de Audience Library, Target en Audience Manager.
title: Publish Segmenten naar Experience Cloud
feature: Segmentation
exl-id: 0215f896-d3f8-42cc-ac8d-8a94b009927b
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '1240'
ht-degree: 0%

---

# Publish-segmenten naar Experience Cloud

Als u een Adobe Analytics-segment naar Experience Cloud publiceert, kunt u het segment gebruiken voor marketingactiviteiten in [!DNL Audience Manager] en in andere activeringskanalen, zoals de Adoben [!DNL Advertising Cloud] , [!DNL Target] en [!DNL Campaign] .

U kunt de segmenten Analytics binnen 8 uur naar het Experience Cloud publiceren. Gebruik deze segmenten om publiek in Audience Manager aan alle stroomafwaartse bestemmingen te activeren.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ de segmenten van Publish ](https://video.tv.adobe.com/v/32842?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


>[!NOTE]
>
>Adobe Campaign (Classic en Standard) gedraagt zich anders in die zin dat er een extra latentie van 24 uur bovenop de 8-uurs latentie ontstaat.

## Vereisten

* Zorg ervoor dat de rapportreeks die u dit segment aan opslaat [ voor Experience Cloud ](https://experienceleague.adobe.com/docs/core-services/interface/audiences/t-publish-audience-segment.html) wordt toegelaten. Anders kunt u het niet naar het Experience Cloud publiceren.
* Zorg ervoor dat uw organisatie Experience Cloud-id&#39;s gebruikt.
* Alvorens u segmenten kunt publiceren, moet uw Admin de [!UICONTROL Segment Publishing] toestemming aan een productprofiel in de [ Admin Console ](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html) toewijzen, en u toevoegen aan het productprofiel.

## Overwegingen

* **de grenzen van de Reeks van het Rapport**: U kunt tot 75 segmenten per rapportreeks publiceren. Deze limiet geldt. Als u al 75 gepubliceerde segmenten hebt, kunt u geen extra segmenten publiceren tot u unpublish genoeg segmenten om onder de 75-segmentdrempel te krijgen.
* **de grenzen van het Lidmaatschap**: Het publiek dat aan [!DNL Experience Cloud] van Adobe Analytics wordt gedeeld kan 20 miljoen unieke leden niet overschrijden.
* **Privacy van Gegevens**: Het publiek wordt niet gefiltreerd gebaseerd op de authentificatiestatus van een bezoeker. Als een bezoeker in een niet-geverifieerde en geverifieerde status door uw site kan bladeren, kan een bezoeker door handelingen die plaatsvinden wanneer een bezoeker niet-geverifieerd is, toch worden opgenomen in een publiek. Het overzicht [ privacy van Adobe Experience Cloud ](https://www.adobe.com/privacy/experience-cloud.html) om de volledige privacyimplicaties van publiek te begrijpen delend.
* Voor een bespreking over de **verschillen tussen segmenten in [!DNL Adobe Analytics] en[!DNL Audience Manager]**, ga [ hier ](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html).

## Tijdlijn voor segmentpublicatie

| Beschikbaar | Wanneer deze beschikbaar is | Waar beschikbaar |
|---|---|---|
| Metagegevens (segmenttitel en -definitie) | Onmiddellijk na publicatie | [!DNL Audience Manager], [!UICONTROL Experience Cloud Audience Library], [!DNL Target] |
| Nuttig segment met lidmaatschap | ~ 8 uur na publicatie | Bezoekerprofielviewer in [!DNL Audience Manager] |
| Treinen en lidmaatschapsbevolking | Binnen 24-48 uur | [!DNL Audience Manager] |

>[!NOTE]
>Eenmaal per week worden alle gegevens volledig gesynchroniseerd om rekening te houden met eventuele delta&#39;s of discrepanties die in de voorgaande week niet zijn vastgelegd.

## Publish-segmenten in [!UICONTROL Segment Builder]

1. Ga in Adobe Analytics naar **[!UICONTROL Components]** > **[!UICONTROL Segments]**
1. Selecteer **[!UICONTROL Add]** om een nieuw segment te maken.
   ![ Experience Cloud van Publish ](assets/publish-ec.png)
1. Geef een titel en een beschrijving voor het segment op. Deze velden zijn vereist voordat u het bestand opslaat.
1. In de **[!UICONTROL Experience Cloud publishing]** sectie, selecteer de optie, **[!UICONTROL Publish this segment to the Experience Cloud (for *rapportreeks *)]**.

>[!IMPORTANT]
>Zorg ervoor dat u &quot;Bezoekers met Experience Cloud-id&quot; gebruikt wanneer u segmentvoorvertoningen bekijkt in Analytics in plaats van de totale segmentvoorvertoning &quot;unieke bezoekers&quot; wanneer u Adobe Analytics-nummers vergelijkt met Audience Manager-nummers:
>
>![ de bezoekers van het segment met ECID ](assets/seg-vis-ecid.png)

| Element | Beschrijving |
|---|---|
| **[!UICONTROL Publish this segment to the Experience Cloud (for *`<report suite>`*)]** | Wanneer deze optie wordt toegelaten, worden de segmenttitel en de definitie (d.w.z. het shell publiek zoals vaak gebruikt in advertentieplatforms) onmiddellijk gedeeld met Experience Cloud, terwijl het segmentlidmaatschap wordt geëvalueerd en om de 4 uur gedeeld. <br> Wanneer dat publiek is gekoppeld aan een activiteit in [!DNL Target] , begint [!DNL Analytics] bijvoorbeeld met het verzenden van id&#39;s voor bezoekers die in aanmerking komen voor dat Experience Cloud en [!DNL Target] publiek. Op dat punt worden de publieksnaam en de bijbehorende gegevens weergegeven op de pagina [!DNL Audience Library] in het Experience Cloud. </br> |
| **[!UICONTROL Audience Creation Window]** | Het tijdkader dat u selecteert, wordt gebruikt om het publiek te maken op basis van een rolkalender. Bijvoorbeeld, &quot;Laatste 30 dagen&quot;(gebrek) omvat bezoekers die voor het publiek in de laatste 30 dagen van de datum van vandaag (NIET van de originele datum hebben gekwalificeerd toen het segment werd gecreeerd.) |
| **[!UICONTROL Create in Audience Library]** | De segmenten die u maakt en publiceert, kunnen zonder vertraging beschikbaar worden gemaakt op de [!DNL Audience Library] -pagina in het Experience Cloud. Ze zijn niet afhankelijk van analytische updates. Deze segmenten tellen niet tegen uw grens van 75 gepubliceerde segmenten. |
| **[!UICONTROL x of 75 Published]** | Hiermee geeft u het aantal segmenten weer dat u naar het Experience Cloud hebt gepubliceerd. Klik de verbinding om een lijst van gepubliceerde segmenten en hun bijbehorende rapportreeks en eigenaar te zien. |
| **[!UICONTROL Save]** | Hiermee slaat u dit segment op. |

## Segmenten verwijderen of verwijderen

Als u een segment wilt verwijderen dat naar het Experience Cloud is gepubliceerd, moet u eerst de publicatie ongedaan maken. Om een segment ongedaan te maken, enkel **** unclick checkbox die u gebruikte om het te publiceren.

>[!NOTE]
>
>U **kunt niet** unpublish een segment dat momenteel in gebruik door om het even welke volgende Adobe oplossingen is: [!DNL Analytics] (in [!DNL Audience Analytics]), [!DNL Campaign], [!DNL Advertising Cloud] (voor [!DNL Core Service] &amp; [!DNL Audience Manager] klanten) en alle andere externe partners (voor [!DNL Audience Manager] klanten). U **kunt** unpublish een segment dat door [!DNL Target] in gebruik is.

## De publicatiestatus van segmenten weergeven

Het maximumaantal publiceerbare Adobe Analytics-segmenten is 75.

Gepubliceerde segmenten weergeven:

1. Ga in Adobe Analytics naar **[!UICONTROL Components]** > **[!UICONTROL Segments]** .

1. Geef de kolom **[!UICONTROL Published]** weer. **[!UICONTROL Yes]** in deze kolom geeft aan dat het segment is gepubliceerd naar het Experience Cloud. **[!UICONTROL No]** geeft aan dat dit niet het geval is.

   ![ status van Publish ](assets/publish-status.png)

## De UUID [!DNL Audience Manager] ophalen

Er zijn twee manieren om de Adobe Audience Manager UUID vast te leggen die momenteel aan de browser is gekoppeld:

* Adobe Experience Cloud Debugger
* Native ontwikkelaarsprogramma in browsers (bijvoorbeeld Chrome Developer Tools)

De volgende schermafbeeldingen tonen u hoe te om Adobe Audience Manager UUID op uw browser terug te winnen en het in de Kijker van het Profiel van de Bezoeker van de Audience Manager te gebruiken om spoor en segmentlidmaatschap te bevestigen.

### Methode 1: Adobe Experience Cloud Debugger gebruiken

1. De download en installeert [ Debugger van Adobe Experience Cloud ](/help/implement/validate/debugger.md) in de Opslag van het Web van Chrome.
1. Start de foutopsporing wanneer u een pagina laadt.
1. Blader naar de sectie Audience Manager en zoek de Adobe Audience Manager UUID-set op de huidige browserpagina
(`50814298273775797762943354787774730612` in het onderstaande voorbeeld)

![ Debugger ](assets/debugger.jpg)

### Methode 2: Chrome Developer Tools (of andere browsergereedschappen) gebruiken

1. Chrome Developer Tools starten voordat een pagina wordt geladen
1. Laad de pagina en controleer Toepassingen > Cookies. De Adobe Audience Manager UUID moet worden ingesteld in de externe
Het koekje van de index ([ adobe.demdex.net ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html) in het hieronder voorbeeld). De velddemdex is de Adobe Audience Manager UUID-set
in de browser (`50814298273775797762943354787774730612` in het onderstaande voorbeeld).

![ de Hulpmiddelen van de Ontwikkelaar van Chrome ](assets/ggogle-uuid.png)

## Audience Manager gebruiken [!UICONTROL Visitor Profile Viewer]

De Adobe Audience Manager-UUID in de browser wordt standaard gebruikt wanneer [!UICONTROL Visitor Profile Viewer] wordt geladen. Als u de resultaten van andere gebruikers met betrekking tot de eigenschap verifieert, voert u een UUID in het veld UUID in en klikt u op [!UICONTROL Refresh] . Verwijs naar [ de Kijker van het Profiel van de Bezoeker ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/visitor-profile-viewer.html) voor meer informatie.

![ de profielkijker van de Audience Manager ](assets/aam-vpv.png)

## De segmentkenmerken weergeven in [!DNL Audience Manager]

In Adobe Audience Manager wordt de lijst met bezoekers met ECID&#39;s voor een bepaald segment op streamingwijze geëvalueerd, aangezien Analytics segmenten deelt met Experience Cloud.

1. Ga in [!DNL Audience Manager] naar [!UICONTROL Audience Data > Traits > Analytics Traits] . Er wordt een map weergegeven voor elke serie Analytics-rapporten die is toegewezen aan uw organisatie Experience Cloud. Deze mappen (voor Traits, Segmenten en Gegevensbronnen) worden gemaakt wanneer de kernservice Profielen en Soorten publiek/Personen wordt gestart of ingericht.
1. Selecteer de map voor de rapportsuite waarin u eerder het segment hebt gemaakt waarmee u het segment wilt delen [!DNL Audience Manager] . U zult het segment/het publiek zien u creeerde. Wanneer u een segment deelt, gebeuren er twee dingen in [!DNL Audience Manager]:
   * Er wordt een doel gemaakt, eerst zonder gegevens erin. Ongeveer. 8 uur nadat het segment is gepubliceerd in [!DNL Analytics] , wordt de lijst met ECID&#39;s genegeerd en gedeeld met [!DNL Audience Manager] en andere oplossingen voor Experiencen Cloud.

     ![ de managersporen van het Publiek ](assets/aam-traits.png)

   * Er wordt een segment met één doel gemaakt. Het gebruikt de gegevensbron die met de rapportreeks wordt geassocieerd waar u het segment publiceerde.
   * De vervaldatum van de reis is nu ingesteld op 16 dagen (voorheen 2 dagen).

## Het segment weergeven in [!DNL Adobe Target]

Met het selectievakje [!UICONTROL Publish this segment to the Experience Cloud] tijdens het maken van segmenten in Adobe Analytics kan het segment beschikbaar zijn in de aangepaste publieksbibliotheek van Adobe Target. Een segment dat in Analytics of Audience Manager wordt gecreeerd kan voor activiteiten in Doel worden gebruikt. U kunt bijvoorbeeld campagneactiviteiten maken op basis van de omzettingscijfers van Analytics en publiekssegmenten die zijn gemaakt in Analytics.

1. Klik op [!UICONTROL Audiences].
1. Zoek op de pagina [!UICONTROL Audiences] het publiek op dat afkomstig is van [!DNL Experience Cloud] . Deze soorten publiek zijn beschikbaar voor gebruik in [!DNL Target] -activiteiten.
