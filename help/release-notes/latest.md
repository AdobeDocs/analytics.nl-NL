---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: ccb40e45ea559db815f4252d85baa61b9e109024
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 2%

---

# Opmerkingen bij de huidige Adobe Analytics-release (maart 2023)

**Laatste update**: 7 maart 2023

Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies in Adobe Analytics {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Gegevenswoordenboek in Analysis Workspace** | Met het gegevenswoordenboek kunnen gebruikers en beheerders de componenten (afmetingen, metriek) in hun analyseomgeving bijhouden, beheren en beter begrijpen. [Meer informatie](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) | 15 maart 2023 | 22 maart 2023 |
| **Gegevensartikelen in mobiele dashboards** | Met gegevensartikelen kunt u meerdere aanpasbare detailweergaven toevoegen aan tegels in Mobile Scorecard-projecten. Gebruik gegevensverhalen om dieper in belangrijke bestuurders, verwante metriek, en verschillende stappen tijdens de klantenreis te duiken. U kunt eenvoudig door deze weergaven heen vegen om het hele verhaal achter uw belangrijkste meetgegevens te begrijpen. Meer informatie (volgen) | N.v.t. | 8 maart 2023 |
| **Vervaldatums voor het geplande project** | U kunt maximale vervaldatums voor geplande projecten instellen op maximaal één jaar, ongeacht de planningsfrequentie. | N.v.t. | 8 maart 2023 |
| **Het delen van verbindingen voor projecten (geen vereiste login)** - Alleen persoonlijke bètatoegang | <p>U kunt nu alleen-lezen koppelingen naar Analysis Workspace-projecten delen met mensen die geen toegang hebben tot Adobe Analytics. U kunt projectverbindingen met mensen buiten uw organisatie, of die binnen uw organisatie delen die niet provisioned voor Adobe Analytics zijn. [Meer informatie](/help/analyze/analysis-workspace/curate-share/share-projects.md)</p> <p>Neem contact op met het accountteam van Adobe om deel te nemen aan de persoonlijke bètaversie.</p> | 15 maart 2023 (particuliere bèta) | April 2023 |

## Oplossingen in Adobe Analytics

AN-308177; AN-308727; AN-308846; AN-309591; AN-310614; AN-311544; AN-311570; AN-311665; AN-311948; AN-312108; AN-312114; AN-312142; AN-312143; AN-312389; AN-312391; AN-312431; AN-312453; AN-312454; AN-312458; AN-312503; AN-312533; AN-312682; AN-312698; AN-312714; AN-312738; AN-312807; AN-312829; AN-312849; AN-312875; AN-312980; AN-312997; AN-313059; AN-313077; AN-313110; AN-313195; AN-313196; AN-313258; AN-313554; AN-313580; AN-313702; AN-313820; AN-313844; AN-313859; AN-313879; AN-314273

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Bijwerken naar apparaatraadplegingen als gevolg van Google Client Hints** | 27 februari 2023 | Het voor 16 februari 2023 geplande gebruik van de tips voor de klant is uitgesteld om de kwaliteit van de raadplegingen van het apparaat met behulp van de tips beter te waarborgen. We zijn op 27 februari 2023 verder gegaan met de eerste fase van de release ter ondersteuning van Client Hints. De tweede en laatste fase van de release werd op donderdag 2 maart 2023 afgerond. [Meer informatie](/help/technotes/client-hints.md) |
| **Beschikbaarheid van analytische bronconnector** | 15 februari 2023 | Op 28 februari 2023 werd de Analytics Source Connector beschikbaar gesteld in het nieuwe Adobe Experience Platform-datacenter in Canada. |
| **Automatische migratie naar architectuur met classificatieset** | 8 februari 2023 | In de komende maanden is Adobe van plan om alle classificaties in alle organisaties te migreren naar de nieuwste classificatiearchitectuur. Naar schatting zullen de laatste klanten die naar migratie gaan, in mei 2023 plaatsvinden. Geen actie van de klant wordt vereist, en geen onderbreking wordt verwacht. Deze nieuwe architectuur heeft veel voordelen, zoals:<ul><li>Aanzienlijk kortere verwerkingstijd (72 uur → 24 uur)</li><li>De mogelijkheid om de [Classificatiesets](/help/components/classifications/sets/overview.md) UI</li><li>De optie om classificatiegegevens in Adobe Experience Platform in de toekomst via de [Adobe Analytics-bronconnector voor classificatiegegevens](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html)</li></ul>Houd rekening met de volgende wijzigingen die mogelijk van invloed zijn op de workflow van uw organisatie:<ul><li>Wanneer u de browser of FTP-import gebruikt, &#39;[!UICONTROL Overwrite on conflict]&#39; is altijd ingeschakeld.</li><li>Wanneer u de browser of FTP-importmodule gebruikt, wordt de optie om direct na het importeren te exporteren niet meer ondersteund.</li><li>De API Analytics 2.0 `GetDimensions` het eindpunt keert nu koordherkenningstekens voor classificaties in plaats van numerieke herkenningstekens terug. Numerieke id&#39;s kunnen nog steeds worden gebruikt, maar Adobe raadt u aan waar mogelijk de nieuwe tekenreeks-id&#39;s te gebruiken. Numerieke id&#39;s kunnen worden opgehaald met de `?expansion=hidden` querytekenreeksparameter.</li></ul>Neem contact op met de klantenservice van Adobe als u een specifieker migratieplan voor uw organisatie wilt of vragen of zorgen hebt over deze migratie. [Meer informatie](/help/components/classifications/sets/overview.md) |

{style="table-layout:auto"}

## Aankondigingen einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **EOL voor[!DNL Reports & Analytics]** | 7 maart 2023 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de normen voor Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit.<p>Op 31 december 2023 zullen we een groot aantal van de bijbehorende functies voor rapporten en analyse beëindigen, waaronder, maar niet beperkt tot: Geplande Rapporten, de Uittreksels van Gegevens, en Rapporten DL. Na 31 december 2023 worden alle geplande rapporten niet meer verzonden. In **April 2023**, worden alle rapporten die volgens de planning na 31 december 2023 zouden verlopen, automatisch bijgewerkt en op 31 december 2023 weer afgehandeld. Bovendien kun je toekomstige rapporten niet langer plannen na 31 december 2023. |
| **EOL van [!UICONTROL People] metrisch** | 28 februari 2023 | Met de afgekeurde [[!DNL Device Co-op]](https://experienceleague.adobe.com/docs/discontinued/using/device-co-op.html), is de Device Co-op-related People-meting niet langer relevant. In de nabije toekomst (datum TBD) verwijderen we deze [!UICONTROL People] metrisch. Op dat moment zullen we de gegevens doorsturen naar de [!UICONTROL Unique Visitor] metrisch om projecten, segmenten en berekende metriek van het breken te verhinderen.<p>**Opmerking**: De [[!UICONTROL People] Metrisch gekoppeld aan apparaatanalyse](/help/components/metrics/people.md) Deze aankondiging heeft geen gevolgen. |
| **EOL van [!UICONTROL Publishing Lists] functie** | 29 september 2022 | In het kader van de regeling exportgerichte bedrijven voor rapporten en analyses [!UICONTROL Publishing Lists] zijn bedoeld om het einde van de levensduur van **december 2023**. U kunt geen nieuwe of bestaande [!UICONTROL Publishing Lists] om te verzenden of te plannen [!UICONTROL Analysis Workspace] projecten. |
| **EOL voor Data Workbench** | 14 september 2022 | Adobe is voornemens de Data Workbench aan het einde van de levensduur doeltreffend te maken **31 december 2023**. Zie [Aankondiging einde levensduur Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html) voor meer informatie. Neem contact op met de Adobe-accountmanager van uw organisatie voor vragen. |
| **EOL voor[!DNL Reports & Analytics]** | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de normen voor Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

{style="table-layout:auto"}

## AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.23.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
