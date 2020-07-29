---
description: 'null'
title: Data-aanvragen - stap 1 van de wizard Aanvragen
uuid: 717542c3-e4aa-4e00-b0ca-cadecd219d13
translation-type: tm+mt
source-git-commit: 178e372e63c436268a1f7028d986504983430b2f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 5%

---


# Data-aanvragen - stap 1 van de wizard Aanvragen

Op de wizard Verzoek: Stap 1 vorm, selecteert u de rapportreeks, rapporttype, segmenten, en vormt data.

![](assets/rw1_overview.png)

1. **[!UICONTROL Report Suite]**: De lijst van rapportreeksen beschikbaar aan u op uw login geloofsbrieven wordt gebaseerd die. Zie [Rapportsets](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md)selecteren.

1. **Bereik selecteren**: Hiermee kunt u een rapportsuite-id selecteren in een cel in Excel. Zie [Rapportsets](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md)selecteren.

1. **Segment**: De segmenten zijn douanesubsets van gegevens, of gegevens die door regels worden gefilterd die u creeert. Segmenten zijn gebaseerd op hits, bezoeken en bezoekers. Zie de [Analytics Segmentation Guide](https://docs.adobe.com/content/help/en/analytics/components/segmentation/seg-home.html) voor meer informatie over segmenten.

   U kunt bijvoorbeeld een segment uitvoeren [!UICONTROL Pages Report]en vervolgens een segment voor het eerst bezoeken toepassen.

1. **Overschrijven** van publicatielijst toestaan: Wanneer u een rapport plant, kunt u een het publiceren lijst kiezen voor distributie te gebruiken. Publicatielijsten worden ingesteld in **[!UICONTROL Analytics]** > **[!UICONTROL Admin tools]**. De rapportsuite voor deze aanvraag wordt vervangen door de id van de rapportsuite die aan elke ontvanger in de publicatielijst is toegewezen. See [Allow Publishing List Overrides](/help/analyze/report-builder/data-requests/allow-publishing-list-overrides.md).

1. **Rapporttype**: Specificeert het basisrapport u in uw gegevensverzoek wilt lopen. U stelt één rapport per verzoek in werking, en dat rapport kan één-aan-vele dimensies en één-aan-vele metriek hebben. De metriek en de afmetingen voor een rapporttype worden getoond op de [!UICONTROL Request Wizard; Step 2] interface. Zie Rapporttypen [](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md)selecteren.

1. **Datumbereik**: Definieert de tijdsperiode die door de aanvraag wordt bestreken. Er zijn verschillende soorten aanvraagtijdsperiodes beschikbaar, zoals vooraf ingesteld, vast en rollen. Het maximumaantal termijnen is 366. U kunt ook een datumbereik kiezen dat door een cel is opgegeven en datumbereiken opslaan als sjablonen voor later gebruik.  Zie Rapportdatums [configureren](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md)

1. **Korreligheid** toepassen: Specificeert het niveau van op tijd-gebaseerd detail dat in het rapport wordt omvat. Zie [Korreligheid](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md).

## Problemen oplossen

Soms verschijnt de aanvraagwizard buiten het scherm, vooral voor gebruikers die tussen monitorinstellingen schakelen. U gebruikt bijvoorbeeld een dockingstation op het werk en uw laptop thuis. Als u nogmaals op Maken klikt terwijl er al een wizard voor aanvragen is geopend, wordt de volgende fout gegenereerd:

&quot;U moet eerst het proces van de verzoektovenaar voltooien alvorens nieuwe te beginnen.&quot;

Als u de wizard Aanvragen weer op het scherm plaatst, wordt dit probleem opgelost.

1. Open Microsoft Excel en meld u aan bij Report Builder.
2. Klik [!UICONTROL Create], die de verzoektovenaar buiten scherm opent.
3. Druk op `[Alt]` + `[Space]`.
4. Druk op `[M]`.
5. Druk op een van de pijltoetsen.
6. Verplaats de muis, die de aanvraagwizard aan de cursor koppelt
7. Klik met de muis om de wizard voor aanvragen op het scherm weer te geven.
