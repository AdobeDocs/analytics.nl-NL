---
description: De gegevens van de het rapportreeks van het etiketteren betekent dat u identiteit, gevoeligheid, en de etiketten van het gegevensbeheer aan elke variabele in een bepaalde rapportreeks toewijst.
title: Overzicht van privacy-labels
feature: Data Governance
role: Admin
exl-id: d1bd833c-3fd4-4572-a5dc-d7bab8a79cb8
source-git-commit: 325a42c080290509309e90c9127138800d5ac496
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 14%

---

# Overzicht van privacy-labels

Het labelen van rapportsuitedata betekent dat u labels voor identiteit, gevoeligheid en data-governance toevoegt aan elke variabele in een bepaalde rapportsuite. Zorg ervoor dat u eerst met de [ etiketten en hun definities ](/help/admin/tools/privacy-labeling/labels.md) vertrouwd maakt.

>[!NOTE]
>
>Herinner dat het Etiketteren moet worden herzien telkens als een nieuwe rapportreeks wordt gecreeerd of wanneer een nieuwe variabele binnen een bestaande rapportreeks wordt toegelaten. U dient de labeling mogelijk ook te herzien wanneer integraties van nieuwe oplossingen worden ingeschakeld, omdat deze nieuwe variabelen kunnen laten zien waarvoor een label nodig is. Een herimplementatie van uw mobiele apps of websites kan de manier veranderen waarop bestaande variabelen worden gebruikt, waardoor eveneens updates van labels nodig kunnen zijn.

## Privacylabels voor rapportsuite toewijzen of bewerken {#assign-edit}

**Voorbeeld**: U, als Controlemechanisme van Gegevens, van plan bent om e-mailadressen en koekjesidentiteitskaarts van de Onderwerpen van Gegevens te verzamelen om hun verzoeken van de Privacy van Gegevens te verwerken. Deze cookie-id&#39;s worden opgeslagen in een rapportsuite in Adobe Analytics.

1. Navigeer in Adobe Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Data configuration and collection]** > **[!UICONTROL Data governance]** .

   ![ het etiketteren van de Privacy ](assets/privacy_rs_settings.png)

1. Selecteer een rapportsuite in de **[!UICONTROL Report Suites]** -kiezer bovenaan.

1. Selecteer in de filtersectie aan de linkerkant welke groepen variabelen u wilt labelen. U kunt slechts één groep variabelen tegelijk labelen.

   * **StandaardComponenten** - De standaardcomponenten zijn uit-van-de-doos dimensies en metriek van Analytics die door gebrek binnen een implementatie van Analytics worden verzameld.
   * **de Variabelen van de Omzetting** - de Variabele van de Omzetting van Custom Insight (of eVar) wordt geplaatst in de code van Adobe op geselecteerde Web-pagina&#39;s van uw plaats. Zijn belangrijkste doel is omzettingssuccesmetriek in douane marketing rapporten te segmenteren. Een eVar kan op bezoek zijn gebaseerd en net als cookies functioneren. De waarden die in eVar-variabelen worden doorgegeven, volgen de gebruiker gedurende een vooraf bepaalde periode.
   * **de Variabelen van de Lijst** - de variabelen van de Lijst zijn douanevariabelen die u kunt gebruiken nochtans zou willen. Ze werken op dezelfde manier als Vars, maar ze kunnen meerdere waarden in dezelfde hit bevatten. Lijstvariabelen hebben geen tekenlimiet.
   * **Variabelen van het Verkeer** - de Variabelen van het Verkeer van Custom Insight (of steunen) laten u toe om douanegegevens met specifieke op verkeer betrekking hebbende gebeurtenissen te correleren. De propvariabelen worden ingesloten in de implementatiecode op elke pagina van uw website.
   * **Gebeurtenissen van het Succes** - de gebeurtenissen van het Succes (die ook als omzettingsgebeurtenissen of douanegebeurtenissen worden bekend) zijn acties die kunnen worden gevolgd. U bepaalt wat een succesgebeurtenis is. Als een bezoeker bijvoorbeeld een item aanschaft, kan de aankoopgebeurtenis als de succesgebeurtenis worden beschouwd.
   * **Classificaties** - de onderverdelingen van de Classificatie worden gebruikt om Analytics in kaart te brengen die gegevens aan verwante eigenschappen melden. Classificaties kunnen voor verschillende doeleinden worden gebruikt, maar worden meestal gebruikt voor de classificatie van codes voor het bijhouden van campagnes (zowel interne als externe) en product-id&#39;s.

1. Selecteer een variabele door op het selectievakje te klikken en klik vervolgens op **[!UICONTROL Edit Privacy Labels]** op de blauwe balk die onder aan het scherm wordt weergegeven.

   ![ geeft ](assets/edit-label.png) uit

   In dit scherm ziet u de labels die op dat moment zijn toegepast en kunt u aanvullende labels toepassen. Afhankelijk van de component kunt u mogelijk niet alle labels toepassen of wijzigen.

   ![ Toegepaste etiketten ](assets/edit-labels2.png)

1. Klik op **[!UICONTROL Apply]** zodra u alle labeling hebt voltooid.

