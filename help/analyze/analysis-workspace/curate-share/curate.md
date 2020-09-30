---
description: Met Curatie kunt u componenten beperken voordat u een project deelt.
keywords: Analysis Workspace curation
title: Cursieve projecten
translation-type: tm+mt
source-git-commit: 232a8376d605fc2345b16fc6579b77dbe2eb7709
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Cursieve projecten

Met Curatie kunt u de componenten (afmetingen, metriek, segmenten, datumbereiken) beperken voordat u een project deelt. Wanneer een ontvanger het project opent, zullen zij een beperkte reeks componenten zien die u voor hen hebt gebogen. Curation is een optionele maar aanbevolen stap voordat een project wordt gedeeld.

>[!NOTE]
> Productprofielen zijn het belangrijkste mechanisme dat bepaalt welke componenten een gebruiker kan zien. Ze worden beheerd via de Adobe Experience Cloud Admin Console. Curatie is een secundair filter.

## Projectcursus toepassen

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]**.
De componenten die in het project worden gebruikt zullen automatisch worden toegevoegd.
   **Opmerking**: Als een project veelvoudige rapportreeksen heeft, zult u een curate gebied voor elke rapportreeks in het project zien.
1. (Optioneel) Als u meer componenten wilt toevoegen, sleept u componenten die u wilt delen van de linkerrails naar het [!UICONTROL Curate Components] veld.
1. Klik op **[!UICONTROL Done]**.

U kunt de curve ook toepassen vanuit het [!UICONTROL Share] menu door te klikken **[!UICONTROL Curate and Share]**. Deze optie leidt automatisch het project tot de componenten in gebruik in het project. U kunt aanvullende componenten toevoegen na de bovenstaande stappen.

![](assets/curation-field.png)

## Samengevoegde projectweergave

Wanneer een ontvanger een gebogen project opent, zullen zij slechts de gebogen reeks componenten zien u hebt bepaald:

![](assets/curate-project.png)

## Projectcursus verwijderen

U kunt als volgt de projectcuratie verwijderen en de volledige set componenten in de linkerspoorstaaf herstellen:

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]**.
1. Klik op **[!UICONTROL Remove Curation]**.
1. Klik op **[!UICONTROL Done]**.

## Cursus Virtual Report Suite (VRS)

Om curatie op een rapport-reeks niveau toe te passen, zodat het op vele projecten in één keer van toepassing is, kunt u componenten in een Virtuele Reeks van het Rapport [leiden (VRS)](https://docs.adobe.com/content/help/en/analytics/components/virtual-report-suites/vrs-components.html).

>[!NOTE]
> De kromming van VRS wordt altijd toegepast vóór projectkromming. Dit betekent dat zelfs als uw gebogen project bepaalde componenten omvat, zij uit zullen worden gefiltreerd als het gebogen VRS hen niet omvat.

## Alle componenten tonen, optie

In een gekromd project of VRS zal de ontvanger de optie aan **[!UICONTROL Show All]** componenten in de linkerspoorstaaf worden voorgesteld. [!UICONTROL Show All] onthult verschillende reeksen componenten, afhankelijk van:

* Het machtigingsniveau van de gebruiker (admin of non-admin)
* Projectrol (eigenaar/editor of niet)
* Type toegepaste kromming (VRS of project)

| Curvetype | Admins | Niet-Admin-projecteigenaar of -bewerkingsrol | Niet-beheerder dubbele rol of weergavefunctie |
|---|---|---|---|
| Gekromde VRS | Alle niet-gebogen VRS-componenten | Niet-beheerde VRS-componenten waarvan deze rol eigenaar is of die met hen zijn gedeeld | Niet-beheerde VRS-componenten waarvan deze rol eigenaar is of die met hen zijn gedeeld |
| Samengevoegd project | Alle niet-gekrulde projectcomponenten | Alle niet-gekrulde projectcomponenten | Niet-gekrulde projectcomponenten die deze rol bezit of die met hen zijn gedeeld |
| Gekromd project in een gekromd VRS | Alle niet-gebogen componenten, vermeld onder **[!UICONTROL Non-Curated Project Components]** en **[!UICONTROL Non-Curated VRS Components]** | Alle niet-gebogen projectcomponenten EN niet-gekrulde componenten VRS die deze rol bezit of die met hen zijn gedeeld | Niet-gekromde VRS en projectcomponenten die deze rol bezit of die met hen zijn gedeeld |
