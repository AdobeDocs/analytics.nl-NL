---
description: Met Curatie kunt u componenten beperken voordat u een project deelt.
keywords: Analysis Workspace curation
title: Cursieve projecten
feature: Curate and Share
role: User, Admin
exl-id: 5e23be83-586a-4543-9be9-65c631b8b0b7
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# Cursieve projecten

Met Curatie kunt u de componenten (afmetingen, metriek, segmenten, datumbereiken) beperken voordat u een project deelt. Wanneer een ontvanger het project opent, zullen zij een beperkte reeks componenten zien die u voor hen hebt gebogen. Curation is een optionele maar aanbevolen stap voordat een project wordt gedeeld.

>[!NOTE]
> Productprofielen zijn het belangrijkste mechanisme dat bepaalt welke componenten een gebruiker kan zien. Ze worden beheerd via de Admin Console van Adobe Experience Cloud. Curatie is een secundair filter.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ projecten van de Kromme ](https://video.tv.adobe.com/v/24711?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Projectcursus toepassen

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]** .
De componenten die in het project worden gebruikt zullen automatisch worden toegevoegd.
   **Nota**: Als een project veelvoudige rapportreeksen heeft, zult u een curate gebied voor elke rapportreeks in het project zien.
1. (Optioneel) Als u meer componenten wilt toevoegen, sleept u componenten die u wilt delen van de linkerrails naar het veld [!UICONTROL Curate Components] .
1. Klik op **[!UICONTROL Done]**.

U kunt de curve ook toepassen vanuit het menu [!UICONTROL Share] door op **[!UICONTROL Curate and Share]** te klikken. Deze optie leidt automatisch het project tot de componenten in gebruik in het project. U kunt aanvullende componenten toevoegen na de bovenstaande stappen.

![](assets/curation-field.png)

## Samengevoegde projectweergave

Wanneer een ontvanger een gebogen project opent, zullen zij slechts de gebogen reeks componenten zien u hebt bepaald:

![](assets/curate-project.png)

## Projectcursus verwijderen

U kunt als volgt de projectcuratie verwijderen en de volledige set componenten in de linkerspoorstaaf herstellen:

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]** .
1. Klik op **[!UICONTROL Remove Curation]**.
1. Klik op **[!UICONTROL Done]**.

## Curve virtuele rapportsuite

Om curatie op een rapport-reeks niveau toe te passen, zodat het op vele projecten in één keer van toepassing is, kunt u componenten in een Virtuele Reeks van het Rapport [ tot stand brengen ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-components.html?lang=nl-NL).

>[!NOTE]
> De virtuele kromming van de rapportreeks wordt altijd toegepast vóór projectkromming. Dit betekent dat zelfs als uw beheerd project bepaalde componenten omvat, zij uit zullen worden gefiltreerd als de gebogen Virtuele rapportreeks hen niet omvat.

## Alle componenten tonen, optie

In een beheerd project of een virtuele-rapportsuite wordt de ontvanger de optie **[!UICONTROL Show All]** -componenten in de linkertrack aangeboden. [!UICONTROL Show All] onthult verschillende reeksen componenten, afhankelijk van:

* Het machtigingsniveau van de gebruiker (beheerder of niet-beheerder)
* Projectrol (eigenaar/editor of niet)
* Type toegepaste curatie (Virtual Report suiteS of project)
* Componenten die eigendom zijn van of worden gedeeld met de gebruiker. De eigendom/gedeelde componenten omvatten segmenten, berekende metriek, en datumwaaiers. Ze omvatten geen geïmplementeerde componenten zoals eVars, props en aangepaste gebeurtenissen.

Opmerking: niet-beheerfuncties hebben geen toegang tot de linkerspoorstaaf in een project, zodat ze zijn weggelaten uit de onderstaande tabel.

| Curvetype | Admins | Niet-Admin-projecteigenaar of -bewerkingsrol | Niet-beheerder dubbele rol |
|---|---|---|---|
| Cursief virtueel rapportenpakket | Alle niet-beheerde componenten van de Virtuele rapportreeks | Niet-beheerde componenten van de Virtuele rapportreeks die deze rol bezit of die met hen zijn gedeeld | Niet-beheerde componenten van de Virtuele rapportreeks die deze rol bezit of die met hen zijn gedeeld |
| Gekromd project | Alle niet-gekrulde projectcomponenten | Alle niet-gekrulde projectcomponenten | Niet-gekrulde projectcomponenten die deze rol bezit of die met hen zijn gedeeld |
| Gekromd project in een gekrulde virtuele rapportsuite | Alle niet-gekromde componenten, weergegeven onder **[!UICONTROL Non-Curated Project Components]** en **[!UICONTROL Non-Curated Virtual report suite components]** | Alle niet-gebogen projectcomponenten EN niet-gebogen Virtuele componenten van de rapportreeks die deze rol bezit of die met hen zijn gedeeld | Niet-beheerde virtuele rapportsuite en projectcomponenten waarvan deze rol eigenaar is of die met hen zijn gedeeld |
