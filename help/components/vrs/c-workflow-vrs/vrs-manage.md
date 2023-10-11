---
description: Met de Virtual Report suites Manager kunnen beheerders virtuele rapportsuites bewerken, toevoegen, labelen, verwijderen, hernoemen, goedkeuren, kopiëren, exporteren en filteren. Deze is niet zichtbaar voor gebruikers die geen beheerder zijn.
keywords: Virtuele rapportsuite
title: Virtuele rapportsuites beheren
feature: VRS
exl-id: b6d58456-bd07-4d97-aff8-216e8440fdc0
source-git-commit: 266cf18050d60f08f7e170c56453d1e1d805cb7b
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 2%

---

# Virtuele rapportsuites beheren

Met de Virtual Report suites Manager kunnen beheerders virtuele rapportsuites bewerken, toevoegen, labelen, verwijderen, hernoemen, goedkeuren, kopiëren, exporteren en filteren. Deze is niet zichtbaar voor gebruikers die geen beheerder zijn.

**[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Virtual report suites]**

![](assets/vrs-manage.png)

>[!NOTE]
>
>In de Virtual Report Suite Manager kunt u alleen uw eigen virtuele rapportsuites zien. U moet klikken **[!UICONTROL Show All]** om de rest te zien.

| Taak | Beschrijving |
| --- | --- |
| Toevoegen | Neemt u aan de virtuele bouwer van de rapportreeks waar u nieuwe virtuele rapportseries kunt tot stand brengen. |
| Tag | Alle gebruikers kunnen markeringen voor virtuele rapportreeksen tot stand brengen en één of meerdere markeringen op een virtuele rapportreeks toepassen. Nochtans, kunt u markeringen slechts voor die virtuele rapportreeksen zien die u bezit. Welke soorten markeringen moet u creëren? Hier volgen enkele suggesties voor handige tags:<ul><li>Tags die zijn gebaseerd op teamnamen, zoals Sociale marketing, Mobiele marketing</li><li>Projectlabels (analysetags), zoals analyse van de pagina Entry</li><li>Categorielabels: heren; geografie</li><li>Workflowlabels: geCurveerd voor (een specifieke bedrijfseenheid); goedgekeurd</li></ul> |
| Verwijderen | Als u een virtuele rapportreeks schrapt, blijven de geplande rapporten en dashboards die deze virtuele toegepaste rapportreeks hebben normaal werken. Het rapport of dashboard blijft de geschrapte virtuele rapportreeks gebruiken tot u het geplande rapport opnieuw opslaat.  Geplande rapporten worden niet bijgewerkt wanneer u een virtuele rapportsuite met dezelfde naam bewerkt.<br>Bijvoorbeeld: Stel dat u twee virtuele rapportsuites met dezelfde naam en verschillende bovenliggende rapportsuites hebt:<br>U hebt een bladwijzer die verwijzingen de virtuele rapportreeks voor de belangrijkste rapportreeks. Dan schrapt u die virtuele rapportreeks omdat het een duplicaat is. De bladwijzer wordt verder uitgevoerd en verwijst naar de definitie van de verwijderde virtuele rapportsuites. Als u de definitie voor de overige virtuele-rapportsuite wijzigt, verandert de Virtual Report-suite die op de bladwijzer is toegepast, niet. De oude definitie wordt gebruikt. Als u dit wilt corrigeren, werkt u de bladwijzer bij en verwijst u naar de nieuwe definitie. Als u niet zeker bent of een referentie, dashboard of gepland rapport een geschrapte Virtuele rapportreeks gebruikt, kon u de naam van de resterende Virtuele rapportreeksen veranderen zodat is het duidelijker of de referentie de resterende Virtuele rapportreeksen gebruikt. |
| Naam wijzigen | Overal waar de virtuele rapportreeks, zoals in de selecteur van de rapportreeks wordt getoond, toont het de nieuwe naam. |
| Goedkeuren/Niet goedkeuren | Goedkeuren van virtuele rapportsuites om deze &#39;officieel&#39; of &#39;canonicaal&#39; te maken. U kunt het proces omkeren door de goedkeuring ongedaan te maken. |
| Kopiëren | Creeert een verschillend exemplaar met zijn eigen nieuwe identiteitskaart van de rapportreeks, maar met de zelfde naam en definitie. |
| Exporteren naar CSV | Exporteer de definitie van de virtuele rapportsuite naar een CSV-bestand. |
| Filter | Filteren op tags, bovenliggende rapportsuite, eigenaars en andere filters (Alles weergeven, Mijne, Favorieten en Goedgekeurd). |
