---
description: Leer meer over de verschillende opslagopties, zoals automatisch opslaan, opslaan als, opslaan als sjabloon en eerdere versies openen.
title: Projecten opslaan
feature: Workspace Basics
role: User, Admin
exl-id: e8206956-6e24-4a3a-8c3f-8acf1fb9d800
source-git-commit: c368ff6c4ac1636a4d1d910b9f1738ff8208fe0a
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Projecten opslaan {#save-projects}

>[!CONTEXTUALHELP]
>id="workspace_project_addnotes"
>title="Notities toevoegen"
>abstract="Voeg notities toe over de projectversie die wordt opgeslagen. Deze notities worden met de versie opgeslagen en kunnen worden geopend in het menu **[!UICONTROL Project]** > **[!UICONTROL Open previous version]** ."

Projecten in Analysis Workspace worden automatisch elke 2 minuten opgeslagen.

U kunt projecten ook handmatig opslaan. Er zijn aanvullende opties beschikbaar, zoals tags of notities toevoegen, wanneer u een project handmatig opslaat.

## Projecten handmatig opslaan {#Save}

Er zijn verschillende opties beschikbaar wanneer u een project handmatig opslaat in Analysis Workspace.

Een project handmatig opslaan:

1. Open uw project in Analysis Workspace en selecteer **[!UICONTROL Project]**. Kies vervolgens een van de volgende opties:

   | Handeling | Beschrijving |
   |---|---| 
   | **[!UICONTROL Save]** | Wijzigingen in uw project opslaan. Als het project wordt gedeeld, zullen de ontvangers van het project ook de veranderingen zien. Wanneer u uw project voor het eerst opslaat, wordt u gevraagd het project een naam, (optionele) beschrijving en (optionele) tags toe te voegen. |
   | **[!UICONTROL Save with notes]** | Voordat uw project wordt opgeslagen, voegt u notities toe over de wijzigingen in het project. Notities worden opgeslagen met de projectversie en zijn beschikbaar voor alle editors onder [!UICONTROL Project] > [!UICONTROL Open previous version] . |
   | **[!UICONTROL Save as]** | Maak een duplicaat van uw project. Dit heeft geen invloed op het oorspronkelijke project. |
   | **[!UICONTROL Save as template]** | Sparen uw project als a [ malplaatje ](/help/analyze/analysis-workspace/templates/create-templates.md) dat aan uw organisatie onder **[!UICONTROL Project > New]** beschikbaar wordt |

## Automatisch opslaan {#Autosave}

Alle projecten in Analysis Workspace worden automatisch elke 2 minuten opgeslagen op uw lokale computer. Dit geldt ook voor nieuwe projecten die nog niet handmatig zijn opgeslagen.

* **Nieuwe projecten:** alhoewel de nieuwe projecten auto-bewaarde zijn, moet u elk nieuw project manueel bewaren de eerste keer. Analysis Workspace vraagt u om nieuwe projecten handmatig op te slaan wanneer u overschakelt naar een ander project, het browsertabblad sluit enzovoort.

  Als u om het even welke reden onverwachts toegang tot een nieuw gecreeerd project verliest alvorens het manueel op te slaan, wordt een terugwinningsversie van uw project bewaard op de Analysis Workspace landende pagina in een omslag genoemd `Recovered Projects (Last 7 Days)`. U moet het herstelde project herstellen en het handmatig op de gewenste locatie opslaan.

  Een hersteld project herstellen:

   1. Ga naar de [!UICONTROL **Herstelde omslag van Projecten**] op de Analysis Workspace landende pagina.

      ![](assets/recovered-folder.png)

   1. Open het project en sla het op de gewenste locatie op.

* **Bestaande projecten:** Als u om het even welke reden een project met veranderingen verlaat die nog niet auto-bewaarde zijn, veroorzaakt Analysis Workspace of u om uw veranderingen te bewaren of verstrekt een waarschuwingsbericht.

  Hier volgen enkele veelvoorkomende scenario&#39;s:

### Een ander project openen

Als u een extra project opent terwijl het werken aan een project dat veranderingen bevat die nog niet auto-bewaarde zijn, vraagt Analysis Workspace u om het huidige project te bewaren alvorens weg te gaan.

De volgende opties zijn beschikbaar:

* **sparen:** vervangt het meest recente auto-bewaarde lokale exemplaar van uw project met uw recentste veranderingen.
* **sparen als:** slaat uw recentste veranderingen als nieuw project op. Het oorspronkelijke project wordt alleen opgeslagen met de meest recente automatisch opgeslagen wijzigingen.
* **verwerpt Veranderingen:** verwerpt uw recentste veranderingen. In het project blijven de meest recente automatisch opgeslagen wijzigingen behouden.

![](assets/existing-save.png)

### Navigeren weg of een tabblad sluiten

Als u van de pagina weg navigeert of het browser lusje terwijl het bekijken van een project met veranderingen sluit die nog niet auto-bewaard zijn, waarschuwt browser dat uw niet bewaarde veranderingen zullen verloren worden. U kunt kiezen om te vertrekken of te annuleren.

![](assets/browser-image.png)

### Browsercrashes of sessietijden uit

Als uw browser vastloopt of als uw sessietijden uit zijn, dan wordt de volgende keer dat u Analysis Workspace opent, u ertoe aangezet om het even welke veranderingen in uw project terug te krijgen die nog niet auto-bewaard zijn.

Hier volgt het dialoogvenster Projectherstel waarin de eerste keer dat u Analysis Workspace opent na een crash of een time-out, wordt weergegeven.

Selecteer **ja** om het project van het meest recente auto-bewaarde exemplaar te herstellen.

Selecteer **Nr** om het auto-bewaarde exemplaar te schrappen en de laatste gebruiker-bewaarde versie van het project te openen.

![](assets/project-recovery.png)

Voor **nieuwe** projecten die nooit zijn bewaard, zijn niet bewaarde veranderingen niet terugwinbaar.

## Een vorige versie openen {#previous-version}

Een vorige versie van een project openen:

1. Ga naar **[!UICONTROL Project]** > **[!UICONTROL Open previous version]**

   ![](assets/previous-versions.png)

1. Controleer de lijst met eerdere beschikbare versies.
   [!UICONTROL Timestamp] en [!UICONTROL Editor] worden weergegeven, in aanvulling op [!UICONTROL Notes] als ze zijn toegevoegd toen de [!UICONTROL Editor] werd opgeslagen. Versies zonder notities worden gedurende 90 dagen opgeslagen; versies met notities worden gedurende 1 jaar opgeslagen.
1. Selecteer een vorige versie en klik op **[!UICONTROL Load]** .
De vorige versie wordt vervolgens geladen met een melding. De vorige versie wordt pas de huidige opgeslagen versie van het project als u op **[!UICONTROL Save]** klikt. Als u bij de geladen versie vandaan navigeert, ziet u bij het retourneren de laatst opgeslagen versie van het project.
