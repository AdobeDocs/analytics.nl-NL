---
description: Interne URL-filters identificeren de referenties die u intern voor uw site beschouwt. Zij helpen verkeersbronnen rapporteren bevolken gegevens en helpen intern verkeer filtreren.
title: Interne URL-filters
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 2%

---


# Interne URL-filters

Interne URL-filters identificeren de referenties die u intern voor uw site beschouwt. Zij helpen verkeersbronnen rapporteren bevolken gegevens en helpen intern verkeer filtreren.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Internal URL Filters]**

Een verwijzing, of verwijzende pagina, is typisch de pagina waarvan een bezoeker uw plaats inging. Als u wilt voorkomen dat gegevens worden schuingetrokken, kunt u interne referenties verwijderen. In rapporten worden gefilterde verwijzingen uitgesloten van de [Referenties](/help/components/dimensions/referrer.md) de [Verwijzen naar domeinen](/help/components/dimensions/referring-domain.md) dimensie, en andere afmetingen van de verkeersbron.

De gemeenschappelijkste rapporten van de redenverkeersbronnen bevolken geen gegevens is dat de Interne Lijst van de Filter URL niet wordt bepaald. Voer de volgende stappen uit om te controleren welke interne URL-filters zijn ingesteld in een rapportsuite. Om dit te voorkomen, verwijdert u de regel met een punt (.) als een filter en voeg uw eigen site toe.

De reden waarom een punt het standaard interne filter URL is om toe te staan dat de gegevens in het rapport van Pagina&#39;s worden verzameld. Als hits niet overeenkomen met interne URL-filters, worden alle pagina&#39;s weergegeven als Overige. De URL bevat altijd een punt dat garandeert dat het rapport Pagina&#39;s wordt ingevuld.
