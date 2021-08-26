---
description: Geeft een overzicht van de stappen waarmee uw Adobe Analytics-implementatie de toegang tot Data Privacy en verwijderingsrechten van de betrokkenen ondersteunt.
title: Privacyworkflow
uuid: f24e8be3-8b5c-409b-ad6b-770198ae2549
exl-id: c364b364-6d77-4b2c-88ab-65daf812f242
source-git-commit: 7cb2489c2deaf8e75c71589895314067a010caf8
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 31%

---

# Privacyworkflow

In deze workflow worden de stappen beschreven die u moet uitvoeren om uw Adobe Analytics-implementatie gereed te maken om Data Privacy-toegangs- en verwijderingsrechten van geregistreerde personen te ondersteunen.

1. **Stel uw beleid voor gegevensbewaring in.** Een beleid van het gegevensbehoud wordt vereist voor Adobe aan de gegevenstoegang van de Privacy van de dienst of schrapt verzoeken.  Zie [Veelgestelde vragen over gegevensbewaring](/help/technotes/data-retention.md) voor meer informatie.
1. **U kunt uzelf vertrouwd maken met de labels DULE/Data Privacy, Adobe Analytics-id&#39;s, naamruimten en ID-uitbreiding.** Zie de Etiketten van de Privacy van  [Gegevens voor de ](/help/admin/c-data-governance/gdpr-labels.md) Variabelen van de Analyse en  [Etikettering Beste praktijken](/help/admin/c-data-governance/gdpr-analytics-ids.md).
1. **Wijs identiteit, gevoeligheid, en de etiketten van het gegevensbeheer aan elke variabele in een rapportreeks toe.** De etikettering moet worden herzien telkens als een nieuwe rapportreeks wordt gecreeerd of wanneer de nieuwe variabele binnen een bestaande rapportreeks wordt toegelaten. Controleer ook de etikettering wanneer de nieuwe oplossingsintegratie wordt toegelaten, aangezien zij nieuwe variabelen kunnen blootstellen die etikettering kunnen vereisen. Een nieuwe implementatie van uw mobiele apps of websites kan de manier veranderen waarop bestaande variabelen worden gebruikt, wat ook updates van labels kan vereisen. Zie [Gegevens van de Reeks van het Rapport van het Etiket](/help/admin/c-data-governance/gdpr-setup-reportsuite.md).
1. **Maak verbinding met de Adobe Data Privacy API en verzend Toegang en schrap Verzoeken.** Als klant van Adobe Analytics kunt u afzonderlijke Data Privacy-aanvragen verzenden voor toegang tot en verwijdering van klantdata door de [Adobe Experience Cloud Data Privacy-API](https://www.adobe.io/apis/experienceplatform/gdpr.html) op te roepen. U kunt Analytics-id&#39;s (zoals beschreven in de sectie [Best practices voor labelen](/help/admin/c-data-governance/gdpr-analytics-ids.md)) in de aanvragen verzenden met hun respectieve naamruimte-id&#39;s (databron-id&#39;s).
1. **Bekijk en beheer de privacyinstellingen van uw rapportsuite.** Zie De instellingen voor [ gegevensbeheer van de rapportsuite ](/help/admin/c-data-governance/gdpr-view-settings.md)weergeven.
