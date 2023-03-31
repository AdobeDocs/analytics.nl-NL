---
description: Interne URL-filters identificeren de referenties die u intern voor uw site beschouwt. Zij helpen verkeersbronnen rapporteren bevolken gegevens en helpen intern verkeer filtreren.
title: Interne URL-filters
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: 2beb4cd38fc8b48e2b34468a4570f7168aeacb78
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---


# Interne URL-filters

Met interne URL-filters kunt u de referenties identificeren die u intern voor uw site beschouwt. Zij helpen verkeersbronnen rapporteren bevolken gegevens en helpen intern verkeer filtreren.

Een verwijzing, of verwijzende pagina, is typisch de pagina waarvan een bezoeker uw plaats inging. Als u wilt voorkomen dat gegevens worden schuingetrokken, kunt u interne referenties verwijderen. In rapporten worden gefilterde verwijzingen uitgesloten van de [Referenties](/help/components/dimensions/referrer.md) de [Verwijzen naar domeinen](/help/components/dimensions/referring-domain.md) dimensie, en andere afmetingen van de verkeersbron.

## Bestaande interne URL-filters weergeven

>[!NOTE]
>
>Sommige rapportsuites hebben een intern filter URL van een periode (.) Standaard geconfigureerd. Wanneer dit filter bestaat, wordt al verkeer geclassificeerd als intern. Refererapporten werken pas na de punt (.) wordt verwijderd.

Om te controleren welke interne filters URL voor een rapportreeks worden gevormd: <!-- I don't see the period in my instance? Is the following information valid? "To avoid this, remove the rule listing a period (.) as a filter, and add your own site. The reason why a period is the default internal URL filter is to allow data to be collected in the Pages report. If hits do not match internal URL filters, all pages come up as Other. A period is always somewhere in the URL, which guarantees the Pages report is populated.")-->

1. Selecteren **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** om toegang te krijgen tot Report Suite Manager.

1. Selecteer de rapportsuite waar u wilt controleren welke interne URL-filters zijn geconfigureerd en selecteer **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Internal URL Filters]**.

   Alle bestaande filters worden vermeld in de [!UICONTROL **Huidige filters**] sectie.

## Een intern URL-filter toevoegen aan een rapportsuite

1. Selecteren **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** om toegang te krijgen tot Report Suite Manager.

1. Selecteer de rapportsuite waar u een intern URL-filter wilt toevoegen en selecteer **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Internal URL Filters]**.

1. Typ in het gedeelte Filter toevoegen in het veld dat verschijnt de URL van de pagina die u wilt filteren en selecteer vervolgens [!UICONTROL **Toevoegen**].

   De URL die u hebt toegevoegd, wordt nu weergegeven in het dialoogvenster [!UICONTROL **Huidige filters**] sectie.
