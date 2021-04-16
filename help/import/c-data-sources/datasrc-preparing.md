---
description: Stappen die u kunt nemen om gegevensbronnen voor te bereiden
subtopic: Data sources
title: Voorbereiden op het gebruik van gegevensbronnen
topic-fix: Developer and implementation
uuid: 876ea069-574b-4e23-93b7-e3828bfd90f5
exl-id: 3cad7c33-f31c-41a2-9dd2-9535713c7620
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 5%

---

# Voorbereiden op het gebruik van gegevensbronnen

Stappen die u kunt nemen om gegevensbronnen voor te bereiden

* [De metriek identificeren en een naam geven](/help/import/c-data-sources/datasrc-preparing.md#section_0D1DA6D7768E4C4CB6E9A2F4639C0135)
* [Identificeer de Dimension van Gegevens](/help/import/c-data-sources/datasrc-preparing.md#section_8EC6BDC4AA314D9EB85F6FCD8E6ABC0A)
* [Code bijhouden campagne](/help/import/c-data-sources/datasrc-preparing.md#section_468222796FF449ABAA90D88EB3264CB1)
* [Transactie-id](/help/import/c-data-sources/datasrc-preparing.md#section_D9513C1204B7496C9B738C5B12CCCFC7)
* [Een geldig datumbereik voor gegevensbrongegevens identificeren](/help/import/c-data-sources/datasrc-preparing.md#section_03AAB1291BDC4403BDC50905A78FDB71)

## De metriek {#section_0D1DA6D7768E4C4CB6E9A2F4639C0135} identificeren en een naam geven

Het is belangrijk om de metriek of de metingen te begrijpen die in uw gegevensbronnen, zoals *`Off-line Sales Revenue by Product`*, *`Returns by Product`*, of *`Ad Impressions by Campaign`* zijn. Dit zijn de namen die u met rapportmetriek (gebeurtenissen, steunen, en steunen) kunt associëren.

Nadat u aangewezen metrisch-aan-gebeurtenis afbeeldingen voor de gegevens van Gegevensbronnen bepaalt, noem de gebeurtenissen met beschrijvende namen aangewezen voor de bijbehorende Metrische Gegevensbronnen anders.

Zie [Gebeurtenissen met succes](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/success-events/success-event.html) in de Help voor beheerprogramma&#39;s.

>[!NOTE]
>
>Adobe adviseert sterk het gebruiken van nieuwe, lege gebeurtenissen met de gegevens van Gegevensbronnen, maar in zeldzame gevallen zou het zinvol kunnen zijn om een reeds bestaande gebeurtenis te gebruiken.

## De Dimension van Gegevens {#section_8EC6BDC4AA314D9EB85F6FCD8E6ABC0A} identificeren

Identificeer en verzamel de gegevens (rapporten) die u wilt gebruiken om de metriek te verdelen die door Gegevensbronnen wordt ingevoerd. Deze gegevens worden *`data dimensions`* genoemd.

Bijvoorbeeld, als een Gegevensbronnen metrische maatregelen en indrukkingen, is uw gegevensdimensie waarschijnlijk de campagne volgende code. Als u off-line verkoop meet, zou u productcode (of SKU) als uw gegevensdimensie kunnen willen gebruiken.

U kunt veelvoudige gegevensafmetingen aan metrisch bepalen, maar elke metrisch moet een relevante waarde, of een combinatie waarden, voor elke bijbehorende gegevensdimensie verstrekken. Als u bijvoorbeeld een Offlineverkoop importeert en koppelt aan de gegevensafmetingen *`Product`* en *`Partner`*, moet de Offlineverkoop relevant zijn voor elke combinatie van product en partner (bijvoorbeeld Totale inkomsten).

>[!NOTE]
>
>Het is mogelijk om Totale metriek in te voeren die niet door om het even welke gegevensdimensie kan worden verdeeld.

Nadat u de gegevensafmetingen bepaalt om met een gegevensbron te gebruiken, integreer de dimensiegegevens in marketing rapporten door het aan een variabele in kaart te brengen. Gebruik standaardrapporten (bijvoorbeeld Product, Trackingcode, Trefwoord zoeken) of Conversieverkeer (eVars).

Wanneer u Vars gebruikt, kunt u bestaande of nieuwe Vars gebruiken als gegevensafmetingen. Na het selecteren van een eVar om een gegevensdimensie van Gegevensbronnen te ontvangen, zorg ervoor u hen geschikt noemt.

Zie [Gebeurtenissen met succes](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/success-events/success-event.html) in de Help bij Analytics.

## Code voor bijhouden campagne {#section_468222796FF449ABAA90D88EB3264CB1}

Naast het importeren van succesgebeurtenissen kunt u desgewenst gekoppelde eVar importeren. Als u bijvoorbeeld online activiteiten bijhoudt met een code voor bijhouden van campagne en over code voor het bijhouden van campagnes voor de offline metriek beschikt, kunt u de metriek importeren met de codes voor bijhouden van campagnes. Op deze manier kunt u zowel online als offline metriek weergeven in campagnerapporten.

Als u geen Metriek van Gegevensbronnen met een bijbehorende waarde van de eVar invoert, kunt u geen Metriek bekijken van de Gegevensbron die door eVars wordt verdeeld. In plaats daarvan, kunt u slechts Totale metriek zien.

## Transactie-id {#section_D9513C1204B7496C9B738C5B12CCCFC7}

De transactie-id wordt gebruikt om een online gebeurtenis te verbinden met een offline gebeurtenis.

## Een geldig datumbereik voor gegevensbrongegevens identificeren {#section_03AAB1291BDC4403BDC50905A78FDB71}

Nadat u de metriek van Gegevensbronnen (de Gebeurtenissen van de Douane) en gegevensafmetingen (eVars) bepaalt, herzie de datumwaaier van de gegevens van de Gegevensbron die u wilt invoeren. U kunt geen Gegevensbronnen invoeren die buiten de waaier van uw bestaande rapporteringsgegevens vallen.

U kunt bijvoorbeeld geen gegevensbrongegevens importeren van voordat u online gegevenstracking hebt geïmplementeerd. Gegevensbrongegevens moeten per dag worden uitgesplitst.
