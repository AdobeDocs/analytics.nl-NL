---
description: 'null'
title: Privacy-workflow
uuid: f24e8be3-8b5c-409b-ad6b-770198ae2549
translation-type: tm+mt
source-git-commit: ''

---


# Privacy-workflow

In deze workflow worden de stappen beschreven die u moet uitvoeren om de implementatie van Adobe Analytics gereed te maken voor ondersteuning van de toegang tot Data Privacy van de betrokkenen en voor het verwijderen van rechten.

| Taakbeschrijving | Koppelingen naar instructies en meer informatie |
|--- |--- |
| **Stap 1**: Zorg ervoor dat al uw rapportensuites die mogelijk gegevens bevatten die relevant zijn voor de gegevensprivacy, zijn toegewezen aan uw organisatie Experience Cloud (of IMS).  Aanvragen voor privacy van gegevens worden ingediend via een Experience Cloud-organisatie en worden toegepast op alle rapportensuites die door die organisatie worden geclaimd. De verzoeken zullen niet van toepassing zijn op rapportsuites die niet aan die Organisatie in kaart worden gebracht, zelfs als zij deel van uw login bedrijf uitmaken. | Raadpleeg de [Kaartweergave voor een organisatie](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/report-suite-mapping.html). |
| **Stap 2**: Stel uw beleid voor gegevensbewaring in. | Adobe kan verzoeken om toegang tot gegevens over privacy van gegevens of om deze te verwijderen alleen uitvoeren als er een beleid voor het bewaren van gegevens is ingesteld.  Zie deze veelgestelde vragen over het bewaren van gegevens van [Analytics voor meer informatie](/help/technotes/data-retention.md). |
| **Stap 3**: U kunt uzelf vertrouwd maken met de labels DULE/Data Privacy, Adobe Analytics ID&#39;s, naamruimten en ID-uitbreiding. | Lees de volgende onderwerpen in deze documentatieset:<ul><li>[Data Privacy Labels voor analytische variabelen](/help/admin/c-data-governance/gdpr-labels.md)</li><li>[Aanbevolen werkwijzen labelen](/help/admin/c-data-governance/gdpr-analytics-ids.md)</li></ul> |
| **Stap 4**: Wijs identiteit, gevoeligheid, en de etiketten van het gegevensbeheer aan elke variabele in een rapportreeks toe.  Opmerking:  Herinner dat het Etiketteren moet worden herzien telkens als een nieuwe rapportreeks wordt gecreeerd of wanneer de nieuwe variabele binnen een bestaande rapportreeks wordt toegelaten. Het kan ook nodig zijn om de labeling te herzien wanneer integratie van nieuwe oplossingen is ingeschakeld, omdat deze nieuwe variabelen toegankelijk kunnen maken waarvoor een label nodig kan zijn. Een nieuwe implementatie van uw mobiele apps of websites kan de manier veranderen waarop bestaande variabelen worden gebruikt, wat ook updates van labels kan vereisen. | Volg de instructies in de Gegevens [van de Reeks van het Rapport van het](/help/admin/c-data-governance/gdpr-setup-reportsuite.md)Etiket. |
| **Stap 5**: Maak verbinding met de Adobe Data Privacy API en verzend toegang- en verwijderverzoeken. | Als klant van Adobe Analytics kunt u individuele verzoeken van de Privacy van Gegevens indienen om tot klantengegevens toegang te hebben en te schrappen, door de [Privacy API](https://www.adobe.io/apis/experienceplatform/gdpr.html)van de Privacy van de Ervaring van de Wolk van Adobe te roepen. U kunt om het even welke die herkenningstekens van Analytics (zoals die in de sectie van het Etiketteren van Beste Praktijken [](/help/admin/c-data-governance/gdpr-analytics-ids.md)worden beschreven) in de verzoeken samen met hun respectieve namespace IDs (gegevensbron IDs) voorleggen. |
| **Stap 6**: Bekijk en beheer de privacyinstellingen van uw rapportsuite. | Volg de instructies in de Instellingen [voor gegevensbeheer van de rapportsuite](/help/admin/c-data-governance/gdpr-view-settings.md)weergeven. |
