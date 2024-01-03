---
description: Interne URL-filters identificeren de referenties die u intern voor uw site beschouwt. Zij helpen verkeersbronnen rapporteren bevolken gegevens en helpen intern verkeer filtreren.
title: Interne URL-filters
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: 5c2643a143e5c8e17fcf11cfa2da81183bc5c39a
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Interne URL-filters

Met interne URL-filters kunt u de referenties identificeren die u intern voor uw site beschouwt. Zij helpen verkeersbronnen rapporteren bevolken gegevens en helpen intern verkeer filtreren.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Internal URL Filters]**

Een verwijzing, of verwijzende pagina, is typisch de pagina waarvan een bezoeker uw plaats inging. Als u wilt voorkomen dat gegevens worden schuingetrokken, kunt u interne referenties verwijderen. Dimensionen die afhankelijk zijn van interne URL-filters zijn onder andere [Referenter](/help/components/dimensions/referrer.md), [Verwijzen naar domein](/help/components/dimensions/referring-domain.md), [Marketingkanalen](/help/components/dimensions/marketing-channel.md)en andere afmetingen van de verkeersbron.

[Verwerkingsregels voor distributiekanalen](../marketing-channels/c-rules.md) verstrekken &quot;[!UICONTROL Matches internal URL filters]&quot; als mogelijke algemene criteria.

>[!IMPORTANT]
>
>Sommige rapportsuites hebben een intern filter URL van een periode (`.`) standaard geconfigureerd. Wanneer dit filter bestaat, wordt al verkeer geclassificeerd als intern. Refererapporten werken pas nadat dit filter is verwijderd en vervangen door een of meer gewenste interne domeinen.

* Alle bestaande filters weergeven onder de **[!UICONTROL Current Filters]** sectie.
* Een filter toevoegen met behulp van het tekstvak onder het dialoogvenster **[!UICONTROL Add Filter]** en klik vervolgens op **[!UICONTROL Add]**.

Filters werken met **contains** logica voor de volledige URL. Adobe beveelt aan protocol (`https://`) en subdomeinen wanneer het creëren van filters, tenzij het verkeer van afzonderlijke subdomeinen als extern verkeer wordt gewenst.
