---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: f258a1150a4bee11f5922d058930dc38b1ddfa14
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 1%

---

# Huidige Adobe Analytics-releaseopmerkingen (release van juni 2025)

**Laatste update**: 24 juni 2025

Deze releaseopmerkingen hebben betrekking op de periode van 18 juni tot en met 15 juli 2025. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Steun voor veilige wolkenbestemmingen in nieuwe Report Builder** | De Javascript Report Builder-invoegtoepassing ondersteunt nu het exporteren van rapporten naar de volgende opslaglocaties in de cloud:<ul><li>Amazon S3 Role ARN</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li></ul><p>Eerder waren alleen FTP- en e-maildoelen beschikbaar. FTP wordt niet meer ondersteund vanwege beveiligingsproblemen.</p><p>Voor meer informatie, zie [ werkboeken van het Programma door naar wolkenbestemmingen ](/help/analyze/report-builder/report-builder-export.md) uit te voeren.</p><p>Naast deze veranderingen, wanneer het creëren van een plaats in Adobe Analytics, verstrekt het Gebruik met gebied nu de optie om de plaats met Report Builder te gebruiken, zoals die in [ wordt beschreven vormt wolkeninvoer en de uitvoerplaatsen ](/help/components/locations/configure-import-locations.md).</p> |  | 19 juni 2025 (oorspronkelijk 18 juni) |
| **Nieuwe voorproefervaring** | In het voorvertoningsvenster, dat wordt gebruikt wanneer u een segment maakt of de instellingen van een gegevensweergave configureert, wordt nu een horizontale streekvisualisatie gebruikt in plaats van een donutvisualisatie. |  | donderdag 18 juni 2025 |
| **Gewijzigde dialoog van het attributiemodel** | U kunt de container en de tijdsperiode nu afzonderlijk definiëren in het dialoogvenster voor het toewijzingsmodel. |  | Juni 18,2025 |
| **bijgewerkte navigatie aan de Attributen UI van de Klant** | De gebruikersinterface Klantkenmerken is nu rechtstreeks toegankelijk vanuit de toepassingskiezer in Adobe Experience Cloud. |  | TBD |
| **Streaming Media: De planningsgegevens van de steun** | U kunt nu geplande gegevens van eerder live streaming media-inhoud uploaden om de viewer eenvoudiger en nauwkeuriger bij te houden. Hieronder volgen voorbeelden van live-inhoud die wordt ondersteund met het uploaden van planningsgegevens:<ul><li>SNELLE (Free Ad Supported TV) platforms</li><li>Lokale streams</li><li>Levende sport</li></ul>Door planningsgegevens te uploaden, kunt u de viewergegevens bijhouden voor afzonderlijke programma&#39;s die worden uitgevoerd tijdens de tijd die u aangeeft in het uploadbestand. U kunt zelfs kijkersgegevens voor specifieke onderwerpen of programmasegmenten verzamelen. Deze mogelijkheden zijn beschikbaar ongeacht de manier waarop u de Verzameling van de Media van de Streaming uitvoerde.<p>Eerder, was het moeilijk om een bepaalde zitting aan specifieke programma&#39;s nauwkeurig te verbinden wanneer het analyseren van levende inhoud, en het was niet mogelijk om een bepaalde zitting aan individuele onderwerpen of programmasegmenten te binden. Meer informatie |  | 15 augustus 2025 (oorspronkelijk 25 juni 2025) |

## Oplossingen in Adobe Analytics

**A4T**: AN-379045
**Advertising Analytics**: AN-377338
**Alarm**: AN-377229
**Analysis Workspace**: AN-378891; AN-379589; AN-379604; AN-381270; AN-382264; AN-382414;
**API 1.4**: AN-380188
**API 2.0**: AN-373078; AN-379006; AN-381248
**Classificaties**: AN-379209; AN-379315; AN-379567; AN-379573; AN-379749; AN-379764; 79818; AN-380433; AN-381670; AN-381751; AN-381994; AN-382055; AN-382682; AN-38 3059; AN-383409
**Analyse van de Bijdrage**: AN-369822
**het voer van Gegevens**: AN-36552; AN-367158; AN-378288; AN-379754; AN-380433; AN-380855; 380959; AN-381115; AN-381657; AN-381931
**Data Warehouse**: AN-379244
**Platform**: AN-375847
**Verwerkingsregels**: AN-375157
**Report Builder**: AN-371395; AN-372174; AN-373815; AN-383194
**Vraag van de Server**: AN-380930
**Logboeken van het Gebruik &amp; van de Toegang**: AN-372130; AN-382123
**Virtuele Suites van het Rapport**: AN-382010


## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Verouderde Report Builder** | donderdag 18 juni 2025 | De oude Report Builder-add-in wordt in juni 2026 opgeheven. Alle gebruikers zouden moeten beginnen hun erfeniswerkboeken aan [ nieuwe Report Builder ](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/rb-overview) te bevorderen. De nieuwe Report Builder is beschikbaar voor zowel Adobe Analytics- als Customer Journey Analytics-klanten. Het heeft [ dichtbij eigenschappariteit ](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/convert-workbooks#unsupported) plus vele nieuwe geschikte eigenschappen en verbeteringen UI. Om het verbeteringsproces te vergemakkelijken, omvat de nieuwe Report Builder een gemakkelijke werkboekomzettingseigenschap. De nieuwe Report Builder is alleen beschikbaar als add-in via de Microsoft Store. Vele organisaties vereisen een intern goedkeuringsproces alvorens toe:voegen-binnen ter beschikking kan worden gesteld aan gebruikers. Wacht tijd en werk nu met uw organisatie om ervoor te zorgen dat u voldoende tijd hebt om uw werkboeken te upgraden vóór de EOL-datum. |
| **Toegang via erfenisdomeinen of via erfenisSSO** | vrijdag 10 april 2025 | Adobe is van plan om bij te werken hoe gebruikers Adobe Analytics openen om de beveiliging te verbeteren en uw aanmeldingservaring te stroomlijnen. Als deel van deze inspanning, zal de toegang via erfenisdomeinen of via erfenisSSO, met inbegrip van `my.omniture.com`, permanent worden beëindigd op **2 Januari, 2026**. Na deze datum werken de oude aanmeldingsgegevens en de oudere SSO niet meer. Alle gebruikers moeten zich via `experience.adobe.com` aanmelden met hun Adobe Experience Cloud-id&#39;s. Als u hulp met uw identiteitskaart van Experience Cloud nodig hebt, gelieve de beheerder van Adobe Analytics van uw organisatie of [ de Zorg van de Klant van Adobe ](https://helpx.adobe.com/contact.html) te contacteren. |
| **Migratie aan de geloofsbrieven van Server-aan-Server van Adobe I/O OAuth** | zaterdag 17 januari 2025 | Adobe Analytics API en Livestream klanten die de geloofsbrieven van Adobe I/O JWT gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door **30 Juni, 2025** migreren. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[ migrerend van de Rekening van de Dienst (JWT) geloofsbrieven ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration)</li><li>[ gids van de Implementatie voor nieuwe en oude toepassingen met OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)<li>[ Gebruikend de nieuwe Server-aan-Server geloofsbrieven OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)</li><li>[ FAQs ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs)</li></ul> |
| **Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |



## AppMeasurement

Voor de recentste updates op de versies van AppMeasurement, gelieve te verwijzen naar [ de versienota&#39;s van AppMeasurement ](https://github.com/adobe/appmeasurement/releases).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2025](/help/release-notes/2025.md)
* [ de versienota&#39;s van Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [ het stromen de versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
