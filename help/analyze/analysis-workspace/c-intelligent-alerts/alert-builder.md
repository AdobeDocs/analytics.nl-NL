---
description: Krijg alarm wanneer de projectcomponenten bepaalde drempels bereiken.
title: Alert Builder
feature: Alerts
role: User, Admin
exl-id: aae28c90-bfdf-49ff-bd38-c9ef63880bf4
source-git-commit: 10ae8213b8745439ab5968853f655a1176b8c38a
workflow-type: tm+mt
source-wordcount: '446'
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
* Ga naar **[!UICONTROL Workspace]** > **[!UICONTROL Components]** > **[!UICONTROL New Alert]**.
* Door een of meer vrije regelitems voor tabellen te selecteren, klikt u met de rechtermuisknop en selecteert u **[!UICONTROL Create Alert from Selection]**.
* Vanuit een rapport Rapporten &amp; Analytics gaat u naar **[!UICONTROL More]** > **[!UICONTROL Add Alert]**.

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
>Het telefoonnummer moet worden voorafgegaan door een plusteken (+) en een [landcode](https://countrycode.org/).

De e-mail die een gebruiker zou ontvangen zodra een alarm is teweeggebracht kijkt gelijkaardig aan dit:

![](assets/alerts-email.PNG)

**Vervaldatum**

Stel de vervaldatum van de waarschuwing in.

**Een waarschuwing verzenden wanneer...**

*... Een van deze metrische trigger*

* Sleep metriek naar het canvas waar triggers worden toegevoegd.

   An **&quot;incompatibele componenten&quot;** Het bericht verschijnt als niet alle componenten (metriek/afmetingen/segmenten) in het alarm compatibel zijn met de momenteel geselecteerde rapportreeks.
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

Als u vindt dat te veel waarschuwingen zijn geactiveerd, kunt u de drempel in het dialoogvenster [Waarschuwingsbeheer](/help/components/c-alerts/alert-manager.md).

![](assets/alert_preview.png)
