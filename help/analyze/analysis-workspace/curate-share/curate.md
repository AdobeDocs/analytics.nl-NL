---
description: Met Curatie kunt u componenten beperken voordat u een project deelt.
keywords: Analysis Workspace curation
title: Cursieve projecten
feature: Curate and Share
role: User, Admin
exl-id: 5e23be83-586a-4543-9be9-65c631b8b0b7
source-git-commit: 8f7c6a0d1477b599b05aeb7b74c4ee96531d294d
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# Cursieve projecten

Met Curatie kunt u de componenten (afmetingen, metriek, segmenten, datumbereiken) beperken voordat u een project deelt. Wanneer een ontvanger het project opent, zien zij een beperkte reeks componenten die u voor hen hebt gebogen. Curation is een optionele maar aanbevolen stap voordat een project wordt gedeeld.

>[!NOTE]
> Productprofielen zijn het belangrijkste mechanisme dat bepaalt welke componenten een gebruiker kan zien. Ze worden beheerd via de Adobe Experience Cloud Admin Console. Curatie is een secundair filter.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ projecten van de Kromme ](https://video.tv.adobe.com/v/24711?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Projectcursus toepassen

1. Selecteer **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]** .
De componenten die in het project worden gebruikt worden automatisch toegevoegd.
Als een project veelvoudige rapportreeksen heeft, ziet u een curate dalingsdoel voor elke rapportreeks in het project.
1. (Optioneel) Als u meer componenten wilt toevoegen, sleept u componenten die u wilt delen van het linkerdeelvenster naar de neerzetzone **[!UICONTROL Curate components]** voor de gegevensweergave.
1. Selecteer **[!UICONTROL Done]** .

U kunt de curve ook toepassen vanuit het menu [!UICONTROL Share] door **[!UICONTROL Curate and Share]** te selecteren. Deze optie leidt automatisch het project tot de componenten in gebruik in het project. U kunt aanvullende componenten toevoegen na de bovenstaande stappen.

![](assets/curation-field.png)

Wanneer een ontvanger een gebogen project opent, zien zij slechts de gebogen reeks componenten u hebt bepaald:


## Projectcursus verwijderen

U kunt als volgt de projectcuratie verwijderen en de volledige set componenten in de linkerspoorstaaf herstellen:

1. Selecteer **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]** .
1. Selecteer **[!UICONTROL Remove Curation]** .
1. Selecteer **[!UICONTROL Done]** .

## Curve virtuele rapportsuite

Om curatie op een rapport-reeks niveau toe te passen, zodat het op vele projecten in één keer van toepassing is, kunt u componenten in een Virtuele Reeks van het Rapport [ tot stand brengen ](https://experienceleague.adobe.com/nl/docs/analytics/components/virtual-report-suites/vrs-components).

>[!NOTE]
>
> De virtuele kromming van de rapportreeks wordt altijd toegepast vóór projectkromming. Zelfs als uw gebogen project bepaalde componenten omvat, worden zij gefilterd uit als de gebogen Virtuele rapportreeks deze componenten niet omvat.
> 

## Opties voor componentcurving

In een beheerd project of een virtuele-rapportsuite wordt de ontvanger de optie **[!UICONTROL Show All]** -componenten in de linkertrack aangeboden. [!UICONTROL Show All] onthult verschillende reeksen componenten, afhankelijk van:

* Het machtigingsniveau van de gebruiker (beheerder of niet-beheerder)
* Projectrol (eigenaar/editor of niet)
* Type toegepaste curatie (Virtual Report suiteS of project)
* Componenten die eigendom zijn van of worden gedeeld met de gebruiker. De eigendom/gedeelde componenten omvatten segmenten, berekende metriek, en datumwaaiers. Ze omvatten geen geïmplementeerde componenten, zoals eVars, props en aangepaste gebeurtenissen.

Opmerking: niet-beheerfuncties hebben geen toegang tot de linkerspoorstaaf in een project, zodat ze zijn weggelaten uit de onderstaande tabel.

| Curvetype | Admins | Niet-Admin-projecteigenaar of -bewerkingsrol | Niet-beheerder dubbele rol |
|---|---|---|---|
| Cursief virtueel rapportenpakket | Alle niet-beheerde componenten van de Virtuele rapportreeks | Niet-beheerde componenten van de Virtuele rapportreeks die deze rol bezit of die met hen zijn gedeeld | Niet-beheerde componenten van de Virtuele rapportreeks die deze rol bezit of die met hen zijn gedeeld |
| Gekromd project | Alle niet-gekrulde projectcomponenten | Alle niet-gekrulde projectcomponenten | Niet-gekrulde projectcomponenten die deze rol bezit of die met hen zijn gedeeld |
| Gekromd project in een gekrulde virtuele rapportsuite | Alle niet-gekromde componenten, weergegeven onder **[!UICONTROL Non-Curated Project Components]** en **[!UICONTROL Non-Curated Virtual report suite components]** | Alle niet-gebogen projectcomponenten EN niet-gebogen Virtuele componenten van de rapportreeks die deze rol bezit of die met hen zijn gedeeld | Niet-beheerde virtuele rapportsuite en projectcomponenten waarvan deze rol eigenaar is of die met hen zijn gedeeld |
