---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 4c6b05ba46e1e5d7bfca24d8cad57fd4479ed8fa
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 2%

---

# Opmerkingen bij de huidige Adobe Analytics-release (juli 2023)

**Laatste update**: 11 juli 2023

Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Opslaglocaties voor cloudaccounts configureren voor het opnemen van classificatiegegevens** | U kunt opslaglocaties voor cloudaccounts die worden gebruikt voor automatisering van classificatiesets, nu beheren.<p> | N.v.t. | 10 juli 2023 |
| **Verbeteringen in het filter Gegevensreparatie** | Er zijn drie filterverbeteringen toegevoegd aan Data Repair:<ul><li>Filter met één variabele om een tweede variabele te wijzigen. Als `eVar2` bevat &quot;@&quot;, en verwijdert u `eVar3`.</li><li>Filter voor numerieke of niet-numerieke waarden</li><li>Meerdere filters toepassen met een AND. Bijvoorbeeld, waarbij `eVar2="a"` EN `eVar3="b"`</li></ul>[Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/) | 21 juni 2023 | 12 juli 2023 |
| **Beveiligde doelen voor het exporteren van gegevenstoevoer** | Gegevensfeeds kunnen nu naar de volgende opslagdoelen in de cloud worden verzonden:<ul><li>Amazon S3</li><li>Azure RBAC</li><li>Azure SAS</li><li>Google Cloud Platform</li></ul>Doelen die voorheen beschikbaar waren (FTP, SFTP, S3 en Azure Blob) worden niet meer aanbevolen. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/create-feed.html) | 12 juni 2023 | 15 juli 2023 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

AN-307816; AN-318111; AN-318584; AN-318828; AN-320440; AN-320568; AN-320616; AN-321013; AN-321513; AN-321520; AN-321757; AN-321820; AN-321917; AN-322034; AN-322135; AN-322140; AN-322142; AN-322251; AN-322353; AN-322378; AN-322383; AN-322427; AN-322458; AN-322543; AN-322630; AN-322637; AN-322638; AN-322647; AN-322728; AN-322732; AN-322777; AN-322817; AN-322957; AN-322958; AN-323035; AN-323074; AN-323150; AN-323196; AN-323197; AN-323205; AN-323206; AN-323217; AN-323224; AN-323225; AN-323244; AN-323257; AN-323277; AN-323280; AN-323293; AN-323309; AN-323318; AN-323468; AN-323476; AN-323514; AN-323572; AN-323592; AN-323782; AN-323835

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Vervaldatum van 37 maanden voor aankoop-id&#39;s en gebeurtenis-id&#39;s (gebeurtenisserialisatie)** | Juli 10,2023 | Een aanstaande versie van de Analytics Hit-verwerkingsengine, die is bedoeld voor release bij **13 juli 2023**, wordt begonnen met het afdwingen van een vervaldatum van 37 maanden voor aankoop-id&#39;s en gebeurtenis-id&#39;s (gebeurtenisserialisatie). Aankoop-id&#39;s en gebeurtenis-id&#39;s verlopen momenteel nooit in Adobe Analytics. Zodra een aankoop-id of een gebeurtenis-id wordt gezien/gebruikt, wordt bij elke toekomstige hit, ongeacht wanneer, die aankoop of gebeurtenis gemarkeerd als een duplicaat. Met de nieuwe verwerkingsmotor:<ul><li>Aankoop-id&#39;s en gebeurtenis-id&#39;s verlopen altijd na 37 maanden.</li><li>Als de aankoop-id of de gebeurtenis-id 37 maanden is geleden, wordt deze niet langer beschouwd als een dubbele aankoop of gebeurtenis.</li><li> Als u aankoop-id&#39;s of gebeurtenis-id&#39;s van meer dan 37 maanden geleden &quot;opnieuw gebruikt&quot;, worden ze niet langer beschouwd als duplicaten.</li></ul> |
| **Migratie naar AdobeIO OAuth Server-to-Server-referenties** | 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die AdobeIO JWT-gebruikersgegevens gebruiken, moeten door **1 januari 2025**. Zie de kennisgeving aan het einde van de levensduur in de onderstaande tabel voor meer informatie en tijdlijnen. |

{style="table-layout:auto"}

## Aankondigingen einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar Adobe I/O OAuth Server-to-Server-gebruikersgegevens migreren door **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementatiehandleiding voor nieuwe en oude toepassingen met OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Het gebruiken van de nieuwe geloofsbrieven van Server-aan-Server OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL voor[!DNL Reports & Analytics]** | 7 maart 2023 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de normen voor Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit.<p>Op 31 december 2023 zullen we een groot aantal van de bijbehorende functies voor rapporten en analyse beëindigen, waaronder, maar niet beperkt tot: Geplande Rapporten, de Uittreksels van Gegevens, en Rapporten DL. Na 31 december 2023 worden alle geplande rapporten niet meer verzonden. In **April 2023**, worden alle rapporten die volgens de planning na 31 december 2023 zouden verlopen, automatisch bijgewerkt en op 31 december 2023 weer afgehandeld. Bovendien kun je toekomstige rapporten niet langer plannen na 31 december 2023. |
| **EOL van [!UICONTROL Publishing Lists] functie** | 29 september 2022 | In het kader van de regeling exportgerichte bedrijven voor rapporten en analyses [!UICONTROL Publishing Lists] zijn bedoeld om het einde van de levensduur van **december 2023**. U kunt geen nieuwe of bestaande [!UICONTROL Publishing Lists] om te verzenden of te plannen [!UICONTROL Analysis Workspace] projecten. |
| **EOL voor Data Workbench** | 14 september 2022 | Adobe is voornemens de Data Workbench aan het einde van de levensduur doeltreffend te maken **31 december 2023**. Zie [Aankondiging einde levensduur Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html) voor meer informatie. Neem contact op met de Adobe-accountmanager van uw organisatie voor vragen. |

{style="table-layout:auto"}

## AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.23.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
