---
title: Opmerkingen bij de release van Adobe Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 2232778be91502eca2ecdc2c9598b8a3375abb8b
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 2%

---

# Huidige Adobe Analytics-releaseopmerkingen (augustus 2023)

**Laatste update**: 24 augustus 2023

Deze releaseopmerkingen hebben betrekking op de releaseperiode van 9 augustus tot 13 september 2023. Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Classificatiesets in API 2.0** | Biedt Adobe Analytics API 2.0-methoden voor het opslaan, verwijderen, ophalen, importeren en exporteren van indelingssetgegevens. | N.v.t. | 30 augustus 2023 |
| **Activity Manager rapporteren** | De manager van de Activiteit van de Rapportering verstrekt beheerders met gedetailleerde zicht in het melden van consumptie voor elke rapportreeks, die beheerders toestaat om capaciteitskwesties tijdens piekrapporteringstijden gemakkelijk te diagnostiseren en dan te bevestigen. [Meer informatie](/help/admin/admin/reporting-activity.md) | N.v.t. | 12 september 2023 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Probleem opgelost waarbij aangepaste gebeurtenissen niet werden geladen. (AN-324163)
* Probleem verholpen waarbij labels voor legenda&#39;s in een visualisatie niet konden worden bewerkt. (AN-323246)

AN-315605; AN-316306; AN-317494; AN-317844; AN-320424; AN-320597; AN-320680; AN-3 320869; AN-321624; AN-321693; AN-322009; AN-322244; AN-322380; AN-322432; AN-3 22466; AN-322556; AN-322669; AN-322735; AN-323151; AN-323220; AN-323380; AN-32 3492; AN-323595; AN-323755; AN-323854; AN-323916; AN-324044; AN-324200; AN-324 213; AN-324238; AN-324347; AN-323598; AN-323625; AN-323631; AN-323638; AN-3236 41; AN-323755; AN-323767; AN-323777; AN-323825; AN-323846; AN-323972; AN-3241 3; AN-324170; AN-324197; AN-324273; AN-324275; AN-324345; AN-324384; AN-32443; AN-324511; AN-324513; AN-324521; AN-324524; AN-324531; AN-324532; AN-324534; AN 324537; AN-324569; AN-324618; AN-324635; AN-324688; AN-324704; AN-324712; AN-3 24721; AN-324745; AN-324792; AN-324793; AN-324794; AN-324795; AN-324824 324947; AN-325003; AN-325073; AN-324947; AN-325003; AN-325073; AN-325 143; AN-325148; AN-325153; AN-325177; AN-325187; AN-325252; AN-325305; AN-3253 325491; AN-325495; AN-325508; AN-325491; AN-325495; AN-325508; AN-32559 4; AN-325601; AN-325660; AN-325779; AN-325857; AN-32583; AN-325885; AN-32586


## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Vervaldatum van 37 maanden voor aankoop-id&#39;s en gebeurtenis-id&#39;s (gebeurtenisserialisatie)** | Juli 10,2023 | Een aanstaande versie van de Analytics Hit-verwerkingsengine, die is bedoeld voor release bij **13 juli 2023**, wordt begonnen met het afdwingen van een vervaldatum van 37 maanden voor aankoop-id&#39;s en gebeurtenis-id&#39;s (gebeurtenisserialisatie). Aankoop-id&#39;s en gebeurtenis-id&#39;s verlopen momenteel nooit in Adobe Analytics. Zodra een aankoop-id of een gebeurtenis-id wordt gezien/gebruikt, wordt bij elke toekomstige hit, ongeacht wanneer, die aankoop of gebeurtenis gemarkeerd als een duplicaat. Met de nieuwe verwerkingsmotor:<ul><li>Aankoop-id&#39;s en gebeurtenis-id&#39;s verlopen altijd na 37 maanden.</li><li>Als de aankoop-id of de gebeurtenis-id 37 maanden is geleden, wordt deze niet langer beschouwd als een dubbele aankoop of gebeurtenis.</li><li> Als u aankoop-id&#39;s of gebeurtenis-id&#39;s van meer dan 37 maanden geleden &quot;opnieuw gebruikt&quot;, worden ze niet langer beschouwd als duplicaten.</li></ul> |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar Adobe I/O OAuth Server-to-Server-gebruikersgegevens migreren door **1 januari 2025**. Zie de kennisgeving aan het einde van de levensduur in de onderstaande tabel voor meer informatie en tijdlijnen. |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar Adobe I/O OAuth Server-to-Server-gebruikersgegevens migreren door **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementatiehandleiding voor nieuwe en oude toepassingen met OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[De nieuwe OAuth Server-to-Server-referenties gebruiken](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL voor[!DNL Reports & Analytics]** | 7 maart 2023 | Effectief **31 december 2023**, is de Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] niet langer aan de technologienormen van de Adobe voldoen. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit.<p>Op 31 december 2023 zullen we veel van de bijbehorende functies Rapporten en Analytics beëindigen, waaronder, maar niet beperkt tot: Geplande rapporten, Gegevensextracten en DL-rapporten. Na 31 december 2023 worden alle geplande rapporten niet meer verzonden. In **April 2023**, worden alle rapporten die volgens de planning na 31 december 2023 zouden verlopen, automatisch bijgewerkt en op 31 december 2023 weer afgehandeld. Bovendien kun je toekomstige rapporten niet langer plannen na 31 december 2023. |
| **EOL van [!UICONTROL Publishing Lists] functie** | 29 september 2022 | In het kader van de regeling exportgerichte bedrijven voor rapporten en analyses: [!UICONTROL Publishing Lists] zijn bedoeld om het einde van de levensduur van **december 2023**. U kunt geen nieuwe of bestaande [!UICONTROL Publishing Lists] naar verzenden of plannen [!UICONTROL Analysis Workspace] projecten. |
| **EOL voor Data Workbench** | 14 september 2022 | Adobe wil Data Workbench aan het einde van de levensduur effectief maken **31 december 2023**. Zie [Aankondiging einde levensduur Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html) voor meer informatie. Neem contact op met de accountmanager van de Adobe van uw organisatie voor vragen. |

{style="table-layout:auto"}

## AppMeasurement

Voor de meest recente updates over releases van AppMeasurementen (versie 2.24.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
