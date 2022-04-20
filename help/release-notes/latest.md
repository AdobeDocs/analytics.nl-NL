---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: b93b27fac0a9e3364512bb8a27ad64c7eb379dd1
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 3%

---

# Huidige Adobe Analytics-releaseopmerkingen (april 2022)

**Laatste update**: 19 april 2022

* Voor opmerkingen bij de release van maart 2022 gaat u [hier](/help/release-notes/2022.md).

* Ga voor opmerkingen bij de release Customer Journey Analytics naar [hier](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=en).

* Voor opmerkingen bij de release Media Analytics gaat u naar [hier](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=en).

* Meer informatie over de nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html). De nieuwste zelfhulpdocumentatie, zelfstudies en cursussen over Experience League.

| Functie | Beschrijving | [Doeldatum](releases.md) |
| ----------- | ---------- | ------- |
| Adobe Analytics-bestemmingspagina-updates | Updates van de landingspagina van de gezamenlijke werkruimte/Rapporten &amp; Analytics die de bruikbaarheid en het gemak van navigatie verbetert. [Meer informatie](/help/analyze/landing.md) | 20 april 2022 |
| [!UICONTROL Next item] of [!UICONTROL Previous item] Deelvenster Werkruimte | De [!UICONTROL Next or Previous item] kunt u zoeken naar items die een dimensie-item van uw keuze volgen of er vooraf aan gaan. Gebruik deze optie bijvoorbeeld als u de volgende of vorige pagina&#39;s naar een specifieke productpagina, een marketingkanaal of zelfs naar een apparaattype wilt bekijken. Dit deelvenster gaat verder dan oudere rapporten (verouderde rapporten), omdat u hiermee elke dimensie kunt bekijken en geen nieuwe implementatie nodig hebt om inzichten op te halen. [Meer informatie](/help/analyze/analysis-workspace/c-panels/next-previous.md) | 20 april 2022 |
| [!UICONTROL Page Summary] Deelvenster Werkruimte | De [!UICONTROL Page Summary] biedt een diepgaande analyse van de pagina die u kiest. Het biedt dezelfde details als oudere rapporten en analyses [!UICONTROL Page Summary] verslag, nog veel meer. [Meer informatie](/help/analyze/analysis-workspace/c-panels/page-summary.md) | 20 april 2022 |
| Verwijderde eis van `x-proxy-global-company-id` header voor 2.0 API-aanroepen | Voor de API&#39;s van Adobe Analytics 2.0 is het niet langer nodig `x-proxy-global-company-id` header, aangezien deze informatie deel uitmaakt van het eindpunt URL. U kunt deze koptekst wel invoegen, maar er treedt geen fout meer op als deze ontbreekt. | 20 april 2022 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Adobe Analytics

* Probleem verholpen in Gegevensfeeds waarbij de begin- en einddatum automatisch werden gewijzigd nadat de gegevensfeed was opgeslagen tijdens het maken vanuit de interface Gegevensfeed. De data werden met één dag bijgewerkt. (AN-281262)

* Probleem verholpen waardoor geplande projecten niet konden worden vernieuwd via e-mailkoppeling. (AN-283622)

### Extra correcties in Adobe Analytics

AN-274486; AN-279258; AN-279995; AN-280918; AN-281423; AN-282084; AN-282435; AN-283508; AN-283517; AN-283706; AN-283762; AN-283921; AN-284195; AN-284663; AN-284573; AN-284721; AN-284790; AN-284867; AN-284870; AN-284872; AN-284884; AN-284914; AN-284930; AN-284933; AN-284967; AN-284970; AN-285187; AN-285328; AN-285337; AN-285375; AN-285447; AN-285724; AN-285753; AN-285761;

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **CDA-machtiging (Cross-Device Analytics)** | 13 april 2022 | Effectief **1 mei 2022**, elke nieuwe toepassing van [CDA](/help/components/cda/overview.md) zijn beperkt tot een maximum van drie reeks IDs van het rapport (RSIDs) per klant. |
| **Wijzigen in hoe Adobe Analytics omgaat met A4T-gegevens die via Experience Edge zijn verzameld** | 31 maart 2022 | Op 7 maart 2022 veranderde Analytics hoe het sommige vraag die van de Rand van de Ervaring kwam behandelde die inhoud van het Doel voorgenomen voor Analytics voor het Rapport van het Doel (A4T) omvatten. Vanaf 7 maart worden alle hits met A4T-rapportinhoud gewijzigd, zodat ze niet worden behandeld als gebeurtenissen Paginaweergave of Koppeling. Starten **31 maart 2022** De logica is selectiever, zodat de standaardgebeurtenissen Paginaweergave en Klikken niet worden gewijzigd. Voorwaarts, zijn de enige gebeurtenissen die worden gewijzigd verpersoonlijking-slechts vraag die slechts A4T inhoud heeft. |
| **Bijwerken naar voor bepaalde klanten ondersteunde versleutelingsmethoden voor browsers** | 28 maart 2022 | Adobe biedt twee cipher veiligheidsniveaus aan om aan verschillende klantenbehoeften voor veiligheid op de inzameling van gegevens van eerste partij te voldoen. Aan **23 juni 2022** ondersteuning wordt verwijderd voor bepaalde HTTPS-versleutelingsalgoritmen, ook wel &#39;ciphers&#39; genoemd, voor klanten met hun beveiligingsniveau ingesteld op &#39;High&#39;. Dit betekent dat sommige oudere besturingssystemen geen gegevens meer naar Analytics kunnen verzenden omdat deze geen ondersteuning bieden voor moderne versleutelingsmethoden. Klanten die de standaardinstellingen voor standaardcursorbeveiliging gebruiken, worden niet beïnvloed. Er is al rechtstreeks contact opgenomen met alle klanten die momenteel gebruikmaken van de instelling &quot;Hoog&quot;. Hier vindt u een gedetailleerde lijst van de ciphers die door deze wijziging worden beïnvloed. |
| **Oudere geplande rapporten onderbreken** | 12 april 2022 | Effectief **20 april 2022**, is Adobe voornemens alle geplande rapporten met een aanmaakdatum van meer dan twee jaar (aangemaakt vóór 31 januari 2020) te pauzeren. Er worden geen rapporten of gegevens verwijderd. Alleen rapporten die ouder zijn dan twee jaar worden gepauzeerd en er worden geen aanvullende geplande rapporten verzonden. Meer informatie |
| **2022 ISO-regioupdates** | 11 maart 2021 | Adobe is van plan 2022 ISO-regioupdates uit te voeren op **10 juni 2022**. Verwacht dat er na deze release kleine geo-informatie wordt bijgewerkt. |
| **Oudere geplande Report Builder-taken pauzeren** | 12 april 2022 | Effectief **20 april 2022** Adobe is van plan alle geplande Report Builder-taken die meer dan twee jaar geleden zijn gemaakt, te pauzeren. Deze pauze is met name van toepassing op alle taken die vóór 31 januari 2020 zijn gemaakt. Er worden geen taken, werkboeken of gegevens verwijderd. Taken die ouder zijn dan twee jaar worden echter gepauzeerd en er worden geen extra geplande taken verzonden. Meer informatie |
| **Verlopen van de lijst van gewenste personen EOL-extensie voor verouderde integratie van Analytics OAuth/JWT** | 14 januari 2022 | Aan **25 mei 2022** de [Analytics 1.3 API, 1.4 SOAP API en Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) De extensie lijst van gewenste personen verloopt. Het werd aangeboden klanten te voorzien die erfenis gebruiken [!DNL Adobe Analytics] OAuth/JWT geloofsbrieven extra tijd om hun cliëntintegratie te migreren aan [Adobe IMS-referenties](https://developer.adobe.com/console). Deze vervaldatum beïnvloedt (maar is niet beperkt tot) [!DNL Adobe Analytics Livestream] en [!DNL Adobe Campaign] klanten die hun vereiste IMS-migratie niet hebben voltooid. Klanten die op dit moment verouderde [!DNL Analytics] OAuth/JWT-gebruikersgegevens via de extensie lijst van gewenste personen en die de migratie naar IMS-gegevens op 25 mei 2022 niet hebben voltooid, verliezen de toegang tot Adobe-services. Livestream-klanten kunnen naar deze [instructies](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) over het migreren van hun clienttoepassingen naar IMS-referenties. [!DNL Campaign] klanten kunnen hun Adobe account team bereiken over de upgrade naar de nieuwste versie van [!DNL Campaign]. |
| **EOL voor[!DNL Reports & Analytics]** | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de technologienormen van Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement {#appm}

Voor de meest recente updates over AppMeasurement-releases (versie 2.22.4) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics] releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=en)
