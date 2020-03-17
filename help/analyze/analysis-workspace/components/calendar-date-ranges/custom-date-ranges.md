---
description: Maak aangepaste datumbereiken in de analysewerkruimte en sla deze op als tijdcomponenten.
keywords: Analysis Workspace
title: Aangepaste datumbereiken maken
topic: Reports and analytics
uuid: c8873d41-454d-4f22-ad1f-38cacec5a3bc
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Aangepaste datumbereiken maken

Maak aangepaste datumbereiken in de analysewerkruimte en sla deze op als tijdcomponenten.

**[!UICONTROL Components]** > **[!UICONTROL New Date Range]**

Er wordt een datumbereik toegepast op paneelniveau. Als u een datumbereik aan uw project wilt toevoegen, klikt u op **Deelvensters** > *`<select panel>`* en geeft u een nieuw datumbereik op.

## Datumbereik voor &quot;twee maanden geleden&quot; {#section_C4109C57CB444BB2A79CC8082BD67294}

De volgende waaier van de douanedatum toont een datumwaaier voor &quot;twee maanden geleden,&quot;met een Summiere visualisatie van de Verandering die richtingsverandering toont.

![](assets/date-range-two-months-ago.png)

Het aangepaste datumbereik wordt boven in het deelvenster [!UICONTROL Date Range] Componenten in uw project weergegeven:

![](assets/date-range-panel-two-months-ago.png)

U kunt dit aangepaste datumbereik naar een kolom slepen naast een aangepast maandelijks roldatumbereik met de voorinstelling Laatste maand voor een vergelijking. Voeg een Summiere visualisatie van de Verandering toe en selecteer de totalen van elke kolom om richtingsverandering te tonen:

![](assets/date-range-two-months-table.png)

## Een 7-daags roldatumbereik gebruiken {#section_7EF63B2E9FF54D2E9144C4F76956A8DD}

Een datumbereik is van toepassing op paneelniveau. Als u een datumbereik aan uw project wilt toevoegen, klikt u op **Handelingen** > Deelvenster **** toevoegen en geeft u een nieuw datumbereik op.

In de Bouwer van de Waaier van de Waaier van de Datum, kunt u een waaier van de douanedatum tot stand brengen die in het paneel van Componenten met andere datumwaaiers toont.

U kunt bijvoorbeeld een datumbereik maken dat een rolvenster van 7 dagen opgeeft dat een week geleden eindigt:

![](assets/create_date_range.png)

Gebruik *`rolling daily`*.

* De instellingen voor Start zijn *`current day minus 14 days`*.

* De instellingen voor Einde worden *`current day minus 7 days`* gebruikt.

Dit datumbereik kan een component zijn die u naar elke vrije-vormtabel sleept.
