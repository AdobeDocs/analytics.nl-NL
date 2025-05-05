---
description: Geeft een overzicht van de stappen waarmee uw Adobe Analytics-implementatie de toegang tot Data Privacy en verwijderingsrechten van de betrokkenen ondersteunt.
title: Privacyworkflow
feature: Privacy
role: Admin
exl-id: c364b364-6d77-4b2c-88ab-65daf812f242
source-git-commit: 3e87d420591405e57e57e18fda4287d5fbd3bf1b
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 17%

---

# Privacyworkflow

In deze workflow worden de stappen beschreven die u moet uitvoeren om uw Adobe Analytics-implementatie gereed te maken om Data Privacy-toegangs- en verwijderingsrechten van geregistreerde personen te ondersteunen.

1. Begin met de [ overzichtspagina van Privacy Service ](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html) in Adobe Experience Platform om een idee van te krijgen welke vragen te vragen alvorens u uw gegevens van Analytics etiketteert.
1. **plaats uw beleid van het gegevensbehoud.** Adobe heeft een beleid voor gegevensbewaring nodig om aanvragen voor toegang tot of verwijdering van gegevensprivacy te kunnen uitvoeren.  Voor meer informatie, zie [ Veelgestelde Veelgestelde vragen van het Behoud van Gegevens ](/help/technotes/data-retention.md). Als u de API voor privacyservices wilt gebruiken, moet u ervoor zorgen dat de bewaarperiode voor gegevens is ingesteld in Adobe Analytics.
1. **vertrouwt me met de etiketten van de Privacy van Gegevens, Adobe Analytics IDs, en namespaces.** zie {de Etiketten van de Privacy van 1} Gegevens voor de Variabelen van Analytics [&#128279;](/help/admin/admin/c-data-governance/data-labeling/gdpr-labels.md) en [ het Etiketteren Beste praktijken ](/help/admin/admin/c-data-governance/data-labeling/gdpr-analytics-ids.md).
1. **wijs identiteit, gevoeligheid, en de etiketten van het gegevensbeheer aan elke variabele in een rapportreeks toe.** De etikettering moet worden herzien telkens als een nieuwe rapportreeks wordt gecreeerd of wanneer de nieuwe variabele binnen een bestaande rapportreeks wordt toegelaten. Controleer ook de etikettering wanneer de nieuwe oplossingsintegratie wordt toegelaten, aangezien zij nieuwe variabelen kunnen blootstellen die etikettering kunnen vereisen. Een nieuwe implementatie van uw mobiele apps of websites kan de manier veranderen waarop bestaande variabelen worden gebruikt, wat ook updates van labels kan vereisen. Zie [ Gegevens van de Reeks van het Rapport van het Etiket ](/help/admin/admin/c-data-governance/data-labeling/gdpr-namespaces.md).
1. **verbind met de API van de Privacy van Gegevens van Adobe en verzend Toegang en schrap Verzoeken.** Als klant van Adobe Analytics, kunt u individuele verzoeken van de Privacy van Gegevens voorleggen om tot klantengegevens toegang te hebben en te schrappen, door de [ de Ervaring Privacy Service API van Adobe te roepen ](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html). U kunt Analytics-id&#39;s (zoals beschreven in de sectie [Best practices voor labelen](/help/admin/admin/c-data-governance/data-labeling/gdpr-analytics-ids.md)) in de aanvragen verzenden met hun respectieve naamruimte-id&#39;s (databron-id&#39;s).
1. **Mening en beheer de montages van de Privacy van de Gegevens van uw rapportreeks.** zie [ de Montages van het Beheer van Gegevens van de Reeks van het Rapport van de Mening ](/help/admin/admin/c-data-governance/data-labeling/gdpr-view-settings.md).
