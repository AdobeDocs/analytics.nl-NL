---
description: Met de Virtual Report Suite Manager kunnen beheerders virtuele rapportsuites bewerken, toevoegen, labelen, verwijderen, hernoemen, goedkeuren, kopiëren, exporteren en filteren. Deze is niet zichtbaar voor gebruikers die geen beheerder zijn.
keywords: Virtuele rapportsuite
title: Virtuele rapportsuites beheren
feature: Grondbeginselen van rapporten en analyses
uuid: ce683c01-2d7d-4f2a-98db-946f68eda99b
exl-id: b6d58456-bd07-4d97-aff8-216e8440fdc0
translation-type: tm+mt
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 3%

---

# Virtuele rapportsuites beheren

Met de Virtual Report Suite Manager kunnen beheerders virtuele rapportsuites bewerken, toevoegen, labelen, verwijderen, hernoemen, goedkeuren, kopiëren, exporteren en filteren. Deze is niet zichtbaar voor gebruikers die geen beheerder zijn.

**[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Virtual Report Suites]**

![](assets/vrs-manage.png)

>[!NOTE]
>
>In de Virtuele Manager van de Reeks van het Rapport, kunt u slechts uw eigen virtuele rapportreeksen zien. U moet **[!UICONTROL Show All]** klikken om iedereen anders&#39;s te zien.

| Taak | Beschrijving |
|--- |--- |
| Toevoegen | Neemt u aan de virtuele bouwer van de rapportreeks waar u nieuwe virtuele rapportseries kunt tot stand brengen. |
| Tag | Alle gebruikers kunnen labels voor segmenten maken en een of meer tags toepassen op een segment. U kunt echter alleen labels zien voor de segmenten die u bezit. Welke soorten markeringen moet u creëren? Hier volgen enkele suggesties voor handige tags:<ul><li>Tags die zijn gebaseerd op teamnamen, zoals Sociale marketing, Mobiele marketing</li><li>Projectlabels (analysetags), zoals analyse van de pagina Entry</li><li>Categorielabels: Mannen; geografie</li><li>Workflowlabels: Gecurreerd voor (een specifieke bedrijfseenheid); Goedgekeurd</li></ul> |
| Verwijderen | Als u een virtuele rapportreeks schrapt, blijven de geplande rapporten en dashboards die deze virtuele toegepaste rapportreeks hebben normaal werken. Het rapport of dashboard blijft de geschrapte virtuele rapportreeks gebruiken tot u het geplande rapport opnieuw opslaat.  Geplande rapporten worden niet bijgewerkt wanneer u een virtuele rapportsuite met dezelfde naam bewerkt.<br>Bijvoorbeeld: Stel dat u twee virtuele rapportsuites met dezelfde naam en verschillende bovenliggende rapportsuites hebt:<br>U hebt een bladwijzer die verwijst naar de virtuele rapportsuite voor de hoofdrapportsuite. Dan schrapt u die virtuele rapportreeks omdat het een duplicaat is. De bladwijzer wordt verder uitgevoerd en verwijst naar de definitie van de verwijderde vrijwillige VUT-overeenkomst. Als u de definitie voor de resterende vrijwillige VUT-regeling wijzigt, verandert de vrijwillige VUT-regeling die op de bladwijzer is toegepast, niet. De oude definitie wordt gebruikt. Als u dit wilt corrigeren, werkt u de bladwijzer bij en verwijst u naar de nieuwe definitie. Als u niet zeker bent of een referentie, dashboard of gepland rapport schrapte VRS gebruikt, kon u de naam van resterende VRS veranderen zodat is het duidelijker of de referentie resterende VRS gebruikt. |
| Naam wijzigen | Overal waar de virtuele rapportreeks, zoals in de selecteur van de rapportreeks wordt getoond, toont het de nieuwe naam. |
| Goedkeuren/Niet goedkeuren | Goedkeuren van virtuele rapportsuites om deze &#39;officieel&#39; of &#39;canonicaal&#39; te maken. U kunt het proces omkeren door de goedkeuring ongedaan te maken. |
| Kopiëren | Creeert een verschillend exemplaar met zijn eigen nieuwe identiteitskaart van de rapportreeks, maar met de zelfde naam en definitie. |
| Exporteren naar CSV | Exporteer de definitie van de virtuele rapportsuite naar een CSV-bestand. |
| Filter | Filteren op tags, bovenliggende rapportsuite, eigenaars en andere filters (Alles weergeven, Mijne, Favorieten en Goedgekeurd). |
