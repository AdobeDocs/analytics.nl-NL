---
description: 'null'
title: Privacyworkflow
uuid: f24e8be3-8b5c-409b-ad6b-770198ae2549
translation-type: ht
source-git-commit: dcb07f8717337da904b252864eb7f800f1728231

---


# Privacyworkflow

In deze workflow worden de stappen beschreven die u moet uitvoeren om uw Adobe Analytics-implementatie gereed te maken om Data Privacy-toegangs- en verwijderingsrechten van geregistreerde personen te ondersteunen.

| Taakbeschrijving | Koppelingen naar instructies en meer informatie |
|--- |--- |
| **Stap 1**: Zorg ervoor dat al uw rapportsuites die data kunnen bevatten die relevant zijn voor Data Privacy, zijn toegewezen aan uw Experience Cloud-organisatie (of IMS).  Data Privacy-aanvragen worden verzonden via een Experience Cloud-organisatie en worden toegepast op alle rapportsuites die door deze organisatie worden geclaimd. Aanvragen zullen niet gelden voor rapportsuites die niet aan deze organisatie zijn toegewezen, ook niet als ze deel uitmaken van uw aanmeldingsbedrijf. | Raadpleeg [Rapportsuites aan een organisatie toewijzen](https://docs.adobe.com/content/help/nl-NL/core-services/interface/about-core-services/report-suite-mapping.html). |
| **Stap 2**: Stel uw dataretentiebeleid in. | Er moet een dataretentiebeleid aanwezig zijn, anders kan Adobe geen toegangs-/verwijderingsaanvragen voor Data Privacy-data behandelen.  Zie deze [Veelgestelde vragen over Analytics-dataretentie](/help/technotes/data-retention.md) voor meer informatie. |
| **Stap 3**: Maak u vertrouwd met DULE/Data Privacy-labels, Adobe Analytics-id&#39;s, naamruimten en id-uitbreiding. | Lees de volgende onderwerpen in deze documentatieset:<ul><li>[Data Privacy-labels voor Analytics-variabelen](/help/admin/c-data-governance/gdpr-labels.md)</li><li>[Best practices voor labelen](/help/admin/c-data-governance/gdpr-analytics-ids.md)</li></ul> |
| **Stap 4**: Wijs identiteit, gevoeligheid en Data Governance-labels toe aan elke variabele in een rapportsuite.  Opmerking: Bedenk dat de labels steeds moeten worden gecontroleerd wanneer een nieuwe rapportsuite wordt gemaakt of wanneer een nieuwe variabele in een bestaande rapportsuite wordt ingeschakeld. U dient de labeling mogelijk ook te herzien wanneer integraties van nieuwe oplossingen worden ingeschakeld, omdat deze nieuwe variabelen kunnen laten zien waarvoor een label nodig is. Een herimplementatie van uw mobiele apps of websites kan de manier veranderen waarop bestaande variabelen worden gebruikt, waardoor eveneens updates van labels nodig kunnen zijn. | Volg de instructies in [Rapportsuitedata labelen](/help/admin/c-data-governance/gdpr-setup-reportsuite.md). |
| **Stap 5**: Maak verbinding met de Adobe Data Privacy-API en verzend toegangs- en verwijderingsaanvragen. | Als klant van Adobe Analytics kunt u afzonderlijke Data Privacy-aanvragen verzenden voor toegang tot en verwijdering van klantdata door de [Adobe Experience Cloud Data Privacy-API](https://www.adobe.io/apis/experienceplatform/gdpr.html) op te roepen. U kunt Analytics-id&#39;s (zoals beschreven in de sectie [Best practices voor labelen](/help/admin/c-data-governance/gdpr-analytics-ids.md)) in de aanvragen verzenden met hun respectieve naamruimte-id&#39;s (databron-id&#39;s). |
| **Stap 6**: Bekijk en beheer de Data Privacy-instellingen van uw rapportsuite. | Volg de instructies in [Data Governance-instellingen van rapportsuite weergeven](/help/admin/c-data-governance/gdpr-view-settings.md). |
