---
description: Het sjabloonbestand voor importeren is ontworpen om het importeren te starten.
subtopic: Data sources
title: Een sjabloon voor een importbestand genereren
topic-fix: Developer and implementation
uuid: bcd90e34-42e6-4cd1-b67e-87586dea25d8
exl-id: c2717936-a011-4224-8a9e-94753abbcb33
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 3%

---

# Een sjabloon voor een importbestand genereren

Het sjabloonbestand voor importeren is ontworpen om het importeren te starten.

U bent niet beperkt tot de kolommen die in de sjabloon zijn gedefinieerd. U kunt zo nodig extra kolommen toevoegen, zolang de metrische waarde of de definitie voor het geselecteerde gegevenstype voor gegevensverwerking wordt ondersteund. U kunt de ondersteunde metriek en afmetingen voor elk type in de volgende secties bekijken: [Weblog](/help/import/c-data-sources/c-datasrc-types/datasrc-web-log.md), [Verkeer](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md), [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md), [Transactie ID](/help/import/c-data-sources/c-datasrc-types/datasrc-transactionid.md), [Visitor ID](/help/import/c-data-sources/c-datasrc-types/datasrc-visitorid.md), [Volledige verwerking](/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md)). Bijvoorbeeld, voor een type van verkeersgegevens, kunt u een kolom voor om het even welke metrisch of dimensies toevoegen die in [Verkeer](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md) worden vermeld.

Nadat u de sjabloon hebt gemaakt, kunt u de sjabloon downloaden, uw gegevens in de sjabloon invoeren en de gegevens vervolgens uploaden naar de FTP-site Gegevensbronnen. Zodra verwerkt door de Gegevensbronserver, zijn de ingevoerde gegevens beschikbaar voor gebruik in uw rapporten van Analytics.

De gegevensbronsjabloon is een .txt-bestand dat u met elke teksteditor kunt openen. Het is echter het eenvoudigst om met de sjabloon te werken met Microsoft Excel of een andere spreadsheettoepassing. De sjablooninhoud varieert op basis van uw selecties in de wizard Activering gegevensbron.

Zie [Bestandsreferentie importeren](/help/import/c-data-sources/datasrc-template/datasrc-import-file-reference.md) voor meer informatie.

1. Meld u aan bij Analytics.
1. Selecteer **[!UICONTROL Admin]** > **[!UICONTROL Data Sources]** in de koptekst van de Intel Health Care Management Suite.
1. Selecteer op het tabblad **[!UICONTROL Data Sources Create]** een sjablooncategorie en typ deze.
1. Controleer de activeringsinstructies/informatie en klik op **[!UICONTROL Activate]**.

   Stap Resultaat 1. Selecteer opties voor het genereren van sjablonen in de wizard Activering gegevensbron.

   | Wizard Pagina | Veld | Beschrijving |
   |--- |--- |--- |
   | 1 | Naam | De malplaatjenaam die de Analyses in de Manager van Gegevensbronnen toont. |
   | 1 | E-mail | Het e-mailadres dat alle meldingen ontvangt die betrekking hebben op het gebruik van deze gegevensbronsjabloon. |
   | 3 | Selectievakje voor bijbehorende kosten | Schakel het selectievakje in om aan te geven dat u de aan het gebruik van deze gegevensbronsjabloon gekoppelde kosten accepteert. |
   | 2 | Metrisch kiezen | Selecteer de metriek die u wilt importeren met deze gegevensbron. Analytics raadt bepaalde metriek aan die op de Categorie en het Type van Gegevensbron wordt gebaseerd die in Stap 3 wordt geselecteerd.  Als u een andere metrische waarde wilt opgeven, typt u de naam in een leeg veld en schakelt u het selectievakje in om de metrische waarde in te schakelen. |
   | 1 | Metrische gegevens toewijzen | Selecteer een gebeurtenis Analytics om elke geïmporteerde metrische waarde te ontvangen die is geselecteerd in Wizard pagina 2.  Deze zouden nieuwe, niet toegewezen Gebeurtenissen moeten zijn die u eerder namen hebt toegewezen die aan de ingevoerde metrische gegevens beantwoorden die zij door Gegevensbronnen zullen ontvangen.  Als een eVar-, product- of trackingcode-variabele een doelvariabele is en de geüploade waarden overeenkomen met bestaande vastgelegde waarden, voegen de geüploade gebeurtenissen in feite metriek toe aan bestaande waarden. Bijvoorbeeld, zou u metrisch van &quot;Offline Orden&quot;met een de gegevensdimensie van Producten kunnen tot stand brengen die reeds de Weergaven van het Product, Controles, en Orden als bestaande metriek heeft. |
   | 4 | Dimension voor gegevens kiezen | Selecteer de gegevensafmetingen om de geïmporteerde metriek van deze gegevensbron uit te splitsen. Analytics raadt bepaalde gegevensafmetingen aan op basis van het gegevenstype Gegevensbron dat in stap 3 is geselecteerd.  Als u een andere gegevensdimensie wilt opgeven, typt u de naam in een leeg veld en schakelt u het selectievakje in om de gegevensdimensie in te schakelen. |
   | 5 | Dimension kaartgegevens | Selecteer een standaardrapport of eVar om elke ingevoerde gegevensdimensie te ontvangen die in pagina 4 van de Tovenaar wordt geselecteerd. |

1. Nadat het malplaatje wordt geproduceerd, kopieer gegevens in de aangewezen kolommen van het malplaatje van de Gegevensbron, ervoor zorgend om aan het gegevensformaat te houden dat voor die gegevenskolom wordt vereist.

   Stap Resultaat 1. Sla het gegevensbronbestand op met een naamgevingsconventie van uw keuze. Adobe raadt u aan een consistente naamgevingsconventie te gebruiken voor alle gegevensbronbestanden. Gebruik een algemene bestandsextensie, zoals .txt of .tsv (of gebruik geen extensie).
