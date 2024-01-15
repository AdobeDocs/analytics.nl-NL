---
description: Geeft een overzicht van de stappen waarmee uw Adobe Analytics-implementatie de toegang tot Data Privacy en verwijderingsrechten van de betrokkenen ondersteunt.
title: Privacyworkflow
feature: Privacy
role: Admin
exl-id: c364b364-6d77-4b2c-88ab-65daf812f242
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 16%

---

# Privacyworkflow

In deze workflow worden de stappen beschreven die u moet uitvoeren om uw Adobe Analytics-implementatie gereed te maken om Data Privacy-toegangs- en verwijderingsrechten van geregistreerde personen te ondersteunen.

1. Beginnen met de [Overzicht van Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html) in Adobe Experience Platform om een idee te krijgen van welke vragen u moet stellen voordat u een label geeft aan uw analysegegevens.
1. **Stel uw beleid voor gegevensbewaring in.** Een beleid van het gegevensbehoud wordt vereist voor Adobe aan de gegevenstoegang van de Privacy van de dienst/schrapt verzoeken.  Zie de klasse [Veelgestelde vragen over gegevensbewaring](/help/technotes/data-retention.md). Als u de Privacys Service-API wilt gebruiken, moet u ervoor zorgen dat de bewaarperiode voor gegevens is ingesteld in Adobe Analytics.
1. **U kunt uzelf vertrouwd maken met de labels Data Privacy, Adobe Analytics-id&#39;s, naamruimten en ID-uitbreiding.** Zie [Data Privacy Labels voor analytische variabelen](/help/admin/admin/c-data-governance/data-labeling/gdpr-labels.md) en [Aanbevolen werkwijzen labelen](/help/admin/admin/c-data-governance/data-labeling/gdpr-analytics-ids.md).
1. **U kunt uzelf vertrouwd maken met de labels DULE/Data Privacy, Adobe Analytics-id&#39;s, naamruimten en ID-uitbreiding.** Zie [Data Privacy Labels voor analytische variabelen](/help/admin/admin/c-data-governance/data-labeling/gdpr-labels.md) en [Aanbevolen werkwijzen labelen](/help/admin/admin/c-data-governance/data-labeling/gdpr-analytics-ids.md).
1. **Wijs identiteit, gevoeligheid, en de etiketten van het gegevensbeheer aan elke variabele in een rapportreeks toe.** De etikettering moet worden herzien telkens als een nieuwe rapportreeks wordt gecreeerd of wanneer de nieuwe variabele binnen een bestaande rapportreeks wordt toegelaten. Controleer ook de etikettering wanneer de nieuwe oplossingsintegratie wordt toegelaten, aangezien zij nieuwe variabelen kunnen blootstellen die etikettering kunnen vereisen. Een nieuwe implementatie van uw mobiele apps of websites kan de manier veranderen waarop bestaande variabelen worden gebruikt, wat ook updates van labels kan vereisen. Zie [Rapportsuite-gegevens labelen](/help/admin/admin/c-data-governance/data-labeling/gdpr-namespaces.md).
1. **Maak verbinding met de Adobe Data Privacy API en verzend Toegang en verwijder verzoeken.** Als Adobe Analytics-klant kunt u individuele verzoeken om privacy van gegevens verzenden om toegang te krijgen tot en gegevens van klanten te verwijderen door de [Adobe Experience Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html). U kunt Analytics-id&#39;s (zoals beschreven in de sectie [Best practices voor labelen](/help/admin/admin/c-data-governance/data-labeling/gdpr-analytics-ids.md)) in de aanvragen verzenden met hun respectieve naamruimte-id&#39;s (databron-id&#39;s).
1. **Bekijk en beheer de privacyinstellingen van uw rapportsuite.** Zie [De instellingen voor gegevensbeheer van de rapportsuite weergeven](/help/admin/admin/c-data-governance/data-labeling/gdpr-view-settings.md).
