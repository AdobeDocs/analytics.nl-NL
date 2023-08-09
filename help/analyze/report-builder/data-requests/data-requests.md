---
description: De eerste stap bij het maken van een aanvraag in Report Builder.
title: Data-aanvragen - stap 1 van de wizard Aanvragen
feature: Report Builder
role: User, Admin
exl-id: 698662a8-8b6b-4338-a315-b41cf6a9424e
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 3%

---

# Data-aanvragen - stap 1 van de wizard Aanvragen

Voor de Tovenaar van het Verzoek: Stap 1 vorm, selecteert u de rapportreeks, rapporttype, segmenten, en vormt data.

![Schermafbeelding met de wizard Verzoek: formulier Stap 1.](assets/rw1_overview.png)

1. **[!UICONTROL Report Suite]**: De lijst van rapportsuites beschikbaar aan u die op uw login geloofsbrieven wordt gebaseerd. Zie [Rapportsets selecteren](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).

1. **Bereik selecteren**: Hiermee kunt u een rapportsuite-id selecteren in een cel in Excel. Zie [Rapportsets selecteren](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).

1. **Segment**: Segmenten zijn aangepaste subsets van gegevens of gegevens die zijn gefilterd door regels die u maakt. Segmenten zijn gebaseerd op hits, bezoeken en bezoekers. Zie de [Handleiding voor analysegmentatie](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html) voor meer informatie over segmenten.

   U kunt bijvoorbeeld een [!UICONTROL Pages Report]en past u vervolgens een segment voor eerste bezoeken toe.

1. **Rapporttype**: Geeft het basisrapport op dat u in de gegevensaanvraag wilt uitvoeren. U stelt één rapport per verzoek in werking, en dat rapport kan één-aan-vele dimensies en één-aan-vele metriek hebben. De metriek en de afmetingen voor een rapporttype worden getoond op [!UICONTROL Request Wizard; Step 2] interface. Zie [Rapporttypen selecteren](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md).

1. **Datumbereik**: Definieert de tijdsperiode die door de aanvraag wordt bestreken. Er zijn verschillende soorten aanvraagtijdsperiodes beschikbaar, zoals vooraf ingesteld, vast en rollen. Het maximumaantal termijnen is 366. U kunt ook een datumbereik kiezen dat door een cel is opgegeven en datumbereiken opslaan als sjablonen voor later gebruik.  Zie [Rapportdatums configureren](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md)

1. **Korreligheid toepassen**: Geeft het niveau van op tijd gebaseerde details aan dat in het rapport wordt opgenomen. Zie [Korreligheid](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md).

## Problemen oplossen

Soms verschijnt de aanvraagwizard buiten het scherm, vooral voor gebruikers die tussen monitorinstellingen schakelen. U gebruikt bijvoorbeeld een dockingstation op het werk en uw laptop thuis. Als u nogmaals op Maken klikt terwijl er al een wizard voor aanvragen is geopend, wordt de volgende fout gegenereerd:

&quot;U moet eerst het proces van de verzoektovenaar voltooien alvorens nieuwe te beginnen.&quot;

Als u de wizard Aanvragen weer op het scherm plaatst, wordt dit probleem opgelost.

1. Open Microsoft Excel en meld u aan bij Report Builder.
2. Klikken [!UICONTROL Create], die de aanvraagwizard buiten het scherm opent.
3. Druk `[Alt]` + `[Space]`.
4. Druk `[M]`.
5. Druk op een van de pijltoetsen.
6. Verplaats de muis, die de aanvraagwizard aan de cursor koppelt
7. Klik met de muis om de wizard voor aanvragen op het scherm weer te geven.
