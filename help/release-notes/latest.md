---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 3%

---

# Opmerkingen bij de huidige Adobe Analytics-release (februari 2023)

**Laatste update**: 27 februari 2023

Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies in Adobe Analytics

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Bijgewerkte gebruikersinterface voor de etiketten van de Privacy van Gegevens** | De bijgewerkte interface stroomlijnt het proces van het creëren van, het beheren van, en het uitgeven van de etiketten van de gegevensprivacy voor de componenten van de rapportreeks. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-setup-reportsuite.html?lang=en) | N.v.t. | 8 februari 2023 |
| **Vergelijk datumbereiken in Mobile Scorecards verbergen** | Met de mobiele Scorecards kunt u **[!UICONTROL Include comparison dates]** instellen om vergelijkingsdatums weer te geven of te verbergen. | N.v.t. | 8 februari 2023 |
| **Agenda-updates in werkruimte** | <ul><li>Datums deelvenster Anker: U kunt de componenten van het datumbereik relatief maken ten opzichte van de deelvensterkalender. [Meer informatie](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#relative-panel-dates)</li><li>Updates voor kalenderstijlen: De kalenderstijlen door UI zijn bevorderd om een consistentere en gebruiksvriendelijker werkschema voor te stellen.</li><li>Updates van de kalenderformule: Als u relatieve datums gebruikt, wordt in alle kalenderformules het begin van het datumbereik van het deelvenster weergegeven. [Meer informatie](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#formula-relative-dates)</li></ul> | N.v.t. | 8 februari 2023 |
| **Updates voor het datumbereik van deelvensters** | In Workspace zijn de volgende verbeteringen aangebracht:<ul><li>Vanaf de release van februari worden voorvertoningen van componenten en gegevens gebaseerd op het datumbereik van het deelvenster en niet op de laatste 90 dagen. </li><li>Alle weergegeven dimensie-items zijn beschikbaar op basis van het datumbereik van het deelvenster.</li><li>Alle datumvoorvertoningen in het segment en de berekende metrische builders worden gebaseerd op het bereik van de deelvensterdatum (tenzij ze worden benaderd door de componentmanagers, die geen bijbehorend deelvenster hebben, zijn ze nog steeds gebaseerd op de laatste 90 dagen).</li><li>In alle voorvertoningen van gegevens worden gegevens of componenten weergegeven op basis van het datumbereik van het deelvenster.</li></ul> | N.v.t. | 8 februari 2023 |
| **Rij-/kolomfiltering voor streaming Adobe Analytics Source Connector** | Met de Bronverbinding Analytics in Adobe Experience Platform kunt u nu analysegegevens filteren die worden gebruikt om profielen te vullen in [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en). Filteren op rijniveau helpt het aantal gebeurtenissen dat aan profielen is gekoppeld, te verminderen. Filteren op kolomniveau helpt de rijkheid van de gebeurtenissen zelf te verminderen, zodat u het gebruik van profielrechten kunt optimaliseren. Deze filtering is alleen van toepassing op gegevens die naar het realtime-klantprofiel worden verzonden en [Identiteitsservice](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=en). **Filteren heeft geen invloed op de gegevens die naar het Data Lake worden verzonden voor gebruik in toepassingen zoals Customer Journey Analytics**. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en#filtering-for-profile) | N.v.t. | Gewijzigd tot 29 maart 2023 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Adobe Analytics

AN-302282; AN-303127; AN-303541; AN-303550; AN-305282; AN-306504; AN-307351; AN-307496; AN-307530; AN-307947; AN-308497; AN-308610; AN-308777; AN-308994; AN-309143; AN-309404; AN-309414; AN-309445; AN-309575; AN-309630; AN-309658; AN-309690; AN-309742; AN-309861; AN-309967; AN-309973; AN-310059; AN-310132; AN-310168; AN-310238; AN-310241; AN-310301; AN-310318; AN-310324; AN-310335; AN-310338; AN-310460; AN-310500; AN-310684; AN-310690; AN-311010; AN-311022; AN-311043; AN-311125; AN-311250; AN-311370; AN-311458;

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Bijwerken naar apparaatraadplegingen als gevolg van Google Client Hints** | 27 februari 2023 | Het voor 16 februari 2023 geplande gebruik van de tips voor de klant is uitgesteld om de kwaliteit van de raadplegingen van het apparaat met behulp van de tips beter te waarborgen. We hebben de eerste fase van de release for support of Client Hints afgerond op 27 februari 2023 en de tweede en laatste fase op donderdag 2 maart 2023. [Meer informatie](/help/technotes/client-hints.md) |
| **Beschikbaarheid van analytische bronconnector** | 15 februari 2023 | Op 28 februari 2023 werd de Analytics Source Connector beschikbaar gesteld in het nieuwe Adobe Experience Platform-datacenter in Canada. |
| **Automatische migratie naar architectuur met classificatieset** | 8 februari 2023 | In de komende maanden is Adobe van plan om alle classificaties in alle organisaties te migreren naar de nieuwste classificatiearchitectuur. Naar schatting zullen de laatste klanten die naar migratie gaan, in mei 2023 plaatsvinden. Geen actie van de klant wordt vereist, en geen onderbreking wordt verwacht. Deze nieuwe architectuur heeft veel voordelen, zoals:<ul><li>Aanzienlijk kortere verwerkingstijd (72 uur → 24 uur)</li><li>De mogelijkheid om de [Classificatiesets](/help/components/classifications/sets/overview.md) UI</li><li>De optie om classificatiegegevens in Adobe Experience Platform in de toekomst via de [Adobe Analytics-bronconnector voor classificatiegegevens](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html)</li></ul>Houd rekening met de volgende wijzigingen die mogelijk van invloed zijn op de workflow van uw organisatie:<ul><li>Wanneer u de browser of FTP-import gebruikt, &#39;[!UICONTROL Overwrite on conflict]&#39; is altijd ingeschakeld.</li><li>Wanneer u de browser of FTP-importmodule gebruikt, wordt de optie om direct na het importeren te exporteren niet meer ondersteund.</li><li>De API Analytics 2.0 `GetDimensions` het eindpunt keert nu koordherkenningstekens voor classificaties in plaats van numerieke herkenningstekens terug. Numerieke id&#39;s kunnen nog steeds worden gebruikt, maar Adobe raadt u aan waar mogelijk de nieuwe tekenreeks-id&#39;s te gebruiken. Numerieke id&#39;s kunnen worden opgehaald met de `?expansion=hidden` querytekenreeksparameter.</li></ul>Neem contact op met de klantenservice van Adobe als u een specifieker migratieplan voor uw organisatie wilt of vragen of zorgen hebt over deze migratie. [Meer informatie](/help/components/classifications/sets/overview.md) |

{style=&quot;table-layout:auto&quot;}

## Aankondigingen einde levensduur (EOL)

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **EOL van bepaalde functies voor rapporten en analyse en Report Builder-planning** | 9 februari 2023 | De volgende planningsfuncties zijn op 31 januari 2023 opgeheven:<ul><li>De optie &quot;end after x occurrences&quot; voor taken per uur in Report Builder</li><li>De mogelijkheid om nieuwe rapporten te plannen en gegevensfragmenten te downloaden in Reports and Analytics</li></ul><p>**Opmerking**: Deze functies zijn oorspronkelijk in april 2022 beëindigd, maar de wijziging is teruggedraaid. We hebben ook een bericht verzonden dat deze functies tijdelijk werden hersteld en dat ze op 31 januari 2023 opnieuw zouden worden beëindigd. |
| **EOL van [!UICONTROL Publishing Lists] functie** | 29 september 2022 | Als onderdeel van het EOL van Rapporten &amp; Analytics, worden de het publiceren lijsten vermeld om eind van het leven in te bereiken **december 2023**. U kunt geen nieuwe of bestaande Publishing Lists maken om Analysis Workspace-projecten te verzenden of te plannen. |
| **EOL voor Data Workbench** | 14 september 2022 | Adobe is voornemens de Data Workbench aan het einde van de levensduur doeltreffend te maken **31 december 2023**. Zie [Aankondiging einde levensduur Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html) voor meer informatie. Neem contact op met het accountteam van uw Adobe. |
| **EOL voor[!DNL Reports & Analytics]** | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de normen voor Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.23.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
