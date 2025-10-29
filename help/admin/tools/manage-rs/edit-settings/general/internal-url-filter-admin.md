---
description: Interne URL-filters identificeren de referenties die u intern voor uw site beschouwt. Zij helpen verkeersbronnen rapporteren bevolken gegevens en helpen intern verkeer filtreren.
title: Interne URL-filters
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: e934de3938f013067d6bbd6b516b0444b0c9f782
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Interne URL-filters

Met interne URL-filters kunt u de referenties identificeren die u intern voor uw site beschouwt. Zij helpen verkeersbronnen rapporteren bevolken gegevens en helpen intern verkeer filtreren.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Internal URL Filters]**

Een verwijzing, of verwijzende pagina, is typisch de pagina waarvan een bezoeker uw plaats inging. Als u wilt voorkomen dat gegevens worden schuingetrokken, kunt u interne referenties verwijderen. De afmetingen die zich op interne filters baseren URL omvatten [ Referrer ](/help/components/dimensions/referrer.md), [ Verwijzend domein ](/help/components/dimensions/referring-domain.md), [ de kanalen van de Marketing ](/help/components/dimensions/marketing-channel.md), en andere dimensies van de verkeersbron.

[ de verwerkingsregels van het Kanaal van de Marketing ](../marketing-channels/mc-proc-rules.md) verstrekken &quot;[!UICONTROL Matches internal URL filters]&quot;als mogelijke lijncriteria.

>[!IMPORTANT]
>
>Sommige rapportsuites hebben een intern filter URL van een periode (`.`) die door gebrek wordt gevormd. Wanneer dit filter bestaat, wordt al verkeer geclassificeerd als intern. Refererapporten werken pas nadat dit filter is verwijderd en vervangen door een of meer gewenste interne domeinen.

* Alle bestaande filters weergeven onder de sectie **[!UICONTROL Current Filters]** .
* Voeg een filter toe in het tekstvak onder de sectie **[!UICONTROL Add Filter]** en klik vervolgens op **[!UICONTROL Add]** .

De filters werken gebruikend **bevat** logica tegen volledige URL. Adobe adviseert weglatend protocol (`https://`) en subdomeinen wanneer het creëren van filters, tenzij het verkeer van afzonderlijke subdomeinen als extern verkeer wordt gewenst.
