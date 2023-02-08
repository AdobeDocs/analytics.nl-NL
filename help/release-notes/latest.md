---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: e7140b78b7b2c6c63cb93f1341581cc83af7b33b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Opmerkingen bij de huidige Adobe Analytics-release (februari 2023)

**Laatste update**: 2 februari 2023

Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies in Adobe Analytics

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Bijgewerkte gebruikersinterface voor de etiketten van de Privacy van Gegevens** | De bijgewerkte interface stroomlijnt het proces van het creëren van, het beheren van, en het uitgeven van de etiketten van de gegevensprivacy voor de componenten van de rapportreeks. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-setup-reportsuite.html?lang=en) | N.v.t. | 8 februari 2023 |
| **Vergelijkingsdatumbereiken in Mobile Scorecards** | Met de mobiele Scorecards kunt u **[!UICONTROL Include comparison dates]** instellen om vergelijkingsdatums weer te geven of te verbergen. | N.v.t. | 8 februari 2023 |
| **Agenda-updates in werkruimte** | <ul><li>Datums deelvenster Anker: U kunt de componenten van het datumbereik relatief maken ten opzichte van de deelvensterkalender. [Meer informatie](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#relative-panel-dates)</li><li>Updates voor kalenderstijlen: De kalenderstijlen door UI zijn bevorderd om een consistentere en gebruiksvriendelijker werkschema voor te stellen.</li><li>Updates van de kalenderformule: Als u relatieve datums gebruikt, wordt in alle kalenderformules het begin van het datumbereik van het deelvenster weergegeven. [Meer informatie](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#formula-relative-dates)</li></ul> | N.v.t. | 8 februari 2023 |
| **Rij-/kolomfiltering voor streaming Adobe Analytics Source Connector** | Met de Bronverbinding Analytics in Adobe Experience Platform kunt u nu analysegegevens filteren die worden gebruikt om profielen te vullen in [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en). Filteren op rijniveau helpt het aantal gebeurtenissen dat aan profielen is gekoppeld, te verminderen. Door het filteren van kolomniveaus kunt u de rijkdom van de gebeurtenissen zelf verminderen, zodat u het gebruik van profielrechten kunt optimaliseren. Deze filtering is alleen van toepassing op gegevens die naar het realtime-klantprofiel worden verzonden en [Identiteitsservice](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=en). **Filteren heeft geen invloed op de gegevens die naar het Data Lake worden verzonden voor gebruik in toepassingen zoals Customer Journey Analytics**. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en#filtering-for-profile) | N.v.t. | 22 februari 2023 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Adobe Analytics

AN-302282; AN-303127; AN-303541; AN-303550; AN-305282; AN-306504; AN-307351; AN-307496; AN-307530; AN-307947; AN-308497; AN-308610; AN-308777; AN-308994; AN-309143; AN-309404; AN-309414; AN-309445; AN-309575; AN-309630; AN-309658; AN-309690; AN-309742; AN-309861; AN-309967; AN-309973; AN-310059; AN-310132; AN-310168; AN-310238; AN-310241; AN-310301; AN-310318; AN-310324; AN-310335; AN-310338; AN-310460; AN-310500; AN-310684; AN-310690; AN-311010; AN-311022; AN-311043; AN-311125; AN-311250; AN-311370; AN-311458;

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Bijwerken naar apparaatraadplegingen als gevolg van Google Client Hints** | 25 januari 2023 | Het gebruik van client-hints in apparaatzoekopdracht begint bij **16 februari 2023**. <p> <p>Vanaf oktober 2022 is het mogelijk om clienttips te verzamelen met de Web SDK- of AppMeasurement JavaScript-bibliotheken. Maar de cliëntwenken zullen niet in apparatenraadpleging tot Februari 2023 worden opgenomen. Op dat ogenblik, zal Adobe beginnen gebruikend cliëntwenken naast gebruiker-Agent wanneer het afleiden van bepaalde apparateninformatie voor klappen die uit Chromium browsers, zoals Google Chrome en Microsoft Edge komen. Dit is in antwoord op het plan van Google om de informatie geleidelijk te verminderen die van het user-Agent koord in plaats van gegevens wordt voorgesteld die via cliëntwenken worden overgegaan. <p> <p>Als deel van deze verandering, zal Adobe de Atlas van het Apparaat voor alle apparatenraadplegingen met betrekking tot gebruiker-Agent gebruiken. [Meer informatie](/help/technotes/client-hints.md) |
| **Geplande rapporten onderbreken in rapporten en analyses** | 6 januari 2023 | Adobe heeft deze functies vervangen op **31 jan. 2023**. Houd er rekening mee dat de vervaltijden voor zowel rapporten als gegevensextracten beperkt blijven tot negen maanden. aan het einde van deze periode wordt de levering van rapporten en gegevensuittreksels gepauzeerd , tenzij het schema opnieuw wordt geactiveerd .<p>Voor 31 januari 2023 moest u de geplande rapportage migreren naar een van de andere mechanismen waarover u in Adobe Analytics beschikt. Neem voor aanvullende vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Geplande taken pauzeren in Report Builder** | 6 januari 2023 | Aan **31 januari 2023** Adobe heeft wijzigingen doorgevoerd in geplande taken in Report Builder als onderdeel van onze optimalisatie van prestaties en levering. Deze wijzigingen omvatten het verwijderen van de mogelijkheid om geplande leveringen &#39;end na x occurrences&#39; te laten beëindigen.<p>U kunt Report Builder-taken per uur blijven plannen en deze na maximaal 99 exemplaren laten beëindigen. De terugdraaiing geldt alleen voor uurwerk. het &quot; einde na x &quot; komt niet voor alle andere leveringsintervallen ( dagelijks , wekelijks , maandelijks en jaarlijks ) . Neem voor meer vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](/help/analyze/report-builder/r-arb-scheduled-reports.md) |

{style=&quot;table-layout:auto&quot;}

## Aankondigingen aan het einde van de levensduur

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **EOL voor Data Workbench** | 14 september 2022 | Adobe is voornemens de Data Workbench aan het einde van de levensduur doeltreffend te maken **31 december 2023**. Zie [Aankondiging einde levensduur Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html) voor meer informatie. Neem contact op met de Adobe-accountmanager van uw organisatie voor vragen. |
| **EOL voor[!DNL Reports & Analytics]** | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de normen voor Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |
| **EOL van [!UICONTROL Publishing Lists] functie** | 29 september 2022 | Als onderdeel van het EOL van Rapporten &amp; Analytics, worden de het publiceren lijsten vermeld om eind van het leven in te bereiken **december 2023**. U kunt geen nieuwe of bestaande Publishing Lists maken om Analysis Workspace-projecten te verzenden of te plannen. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.23.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
