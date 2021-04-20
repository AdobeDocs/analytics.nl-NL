---
description: Krijg alarm wanneer de projectcomponenten bepaalde drempels bereiken.
title: Alert Builder
uuid: ebc2d457-4abd-4b1a-9357-489b5aeb3f64
feature: AI Tools
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---


# Alert Builder

>[!IMPORTANT]
>
>Intelligente waarschuwingen zijn alleen beschikbaar voor klanten van Adobe Analytics Prime en Adobe Analytics Ultimate.

## Action Alert Builder

U kunt de waarschuwingsfunctie op vier manieren openen:

* Met de volgende sneltoets in Analysis Workspace:

   `ctrl (or cmd) + shift + a`
* Door naar **[!UICONTROL Workspace]** > **[!UICONTROL Components]** > **[!UICONTROL New Alert]** te gaan.
* Door één of meerdere punten van de vrije lijstlijn van de vrije vorm te selecteren, klik met de rechtermuisknop aan en selecterend **[!UICONTROL Create Alert from Selection]**.
* Vanuit een rapport Rapporten &amp; Analytics door naar **[!UICONTROL More]** > **[!UICONTROL Add Alert]** te gaan.

## Waarschuwingen samenstellen

De interface van de Bouwer van de Alarm is vertrouwd aan degenen die segmenten of berekende metriek in Analytics hebben gebouwd:

![](assets/alert_builder.png)

<!--Meike, I edited this table for validation -->

**Waarschuwingsnaam**

Geef een naam op voor de waarschuwing. De waakzame naam zou de naam van het rapport of de metriedrempel kunnen bevatten.

**Tijdgranulatie**

Geef op wanneer u de metrische waarde wilt controleren: Uur, Dagelijks, Wekelijks, of Maandelijks.

>[!NOTE]
>
>Voor rapportsuites met een aangepaste kalender ondersteunen we geen maandelijkse granulariteit in de Waarschuwingsbouwer.

**Ontvangers**

Geef op waar de waarschuwing kan worden verzonden. Een waarschuwing kan naar een gebruiker van de Analyse, een groep van Analytics, een onbewerkt e-mailadres, of naar een telefoonaantal worden verzonden.

>[!IMPORTANT]
>
>Het telefoonnummer moet worden voorafgegaan door een &quot;+&quot; en een [landcode](https://countrycode.org/).

De e-mail die een gebruiker zou ontvangen zodra een alarm is teweeggebracht kijkt gelijkaardig aan dit:

![](assets/alerts-email.PNG)

**Vervaldatum**

Stel de vervaldatum van de waarschuwing in.

**Een waarschuwing verzenden wanneer...**

*... Een van deze metrische trigger*

* Sleep metriek naar het canvas waar triggers worden toegevoegd.

   Een **&quot;incompatibele componenten&quot;** bericht zal verschijnen als niet alle componenten (metriek/afmetingen/segmenten) in het alarm compatibel met de momenteel geselecteerde rapportreeks zijn.
* Bepaal de drempel die metrisch moet overschrijden alvorens een alarm wordt geplaatst. U kunt deze waarde instellen op een drempel en vervolgens op een van de volgende voorwaarden:

   * abnormaal
   * anomalie is groter dan verwacht
   * anomalie is minder dan verwacht
   * boven of gelijk aan
   * lager is dan of gelijk is
   * wijzigingen door
   * U kunt een drempel instellen van 90%, 95%, 99%, 99,75% en 99,9%.

   U kunt ook berekende metriek gebruiken.

*... Met deze filters*

* Sleep segmenten of dimensies om filters toe te voegen. Als u bijvoorbeeld een segment &quot;Alleen mobiele apparaten&quot; toevoegt, betekent dit dat de regel alleen voor mobiele apparaten wordt geactiveerd.
* Aanvullende filters worden toegevoegd met behulp van de instructie AND.

**Een regel toevoegen**

U kunt EN of OF regels toevoegen door het tandwielpictogram te klikken.

## Waarschuwingen voorvertonen {#section_10D75BA7B77E4C5FAF58A719C082E070}

De interactieve waarschuwingsvoorvertoning laat zien hoe vaak, ongeveer, een waarschuwing wordt geactiveerd op basis van eerdere ervaringen.

Als u bijvoorbeeld de tijdsgranulariteit instelt op dagelijks, kan de voorvertoning u vertellen dat de waarschuwing gedurende een bepaalde metrische x-maal in de afgelopen 30 of 31 dagen zou zijn geactiveerd.

Als u vindt dat teveel alarm zou teweeggebracht zijn, kunt u de drempel in [Alert Manager](/help/components/c-alerts/alert-manager.md) aanpassen.

![](assets/alert_preview.png)
