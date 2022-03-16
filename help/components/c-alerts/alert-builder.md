---
description: Gebruik waarschuwingen in Analysis Workspace.
title: Overzicht van Alert Builder
feature: Alerts
exl-id: 82e51357-4a32-4db1-bc56-95a72dbaa1be
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Alert Builder

>[!IMPORTANT]
>
>Intelligente waarschuwingen zijn beschikbaar voor Adobe [!DNL Analytics] Primair en Adobe [!DNL Analytics] Alleen ultieme klanten.

U kunt de waarschuwingsfunctie op vier manieren openen:

* Met de volgende sneltoets in Analysis Workspace:

   `ctrl (or cmd) + shift + a`
* Ga naar **[!UICONTROL Workspace]** > **[!UICONTROL Components]** > **[!UICONTROL New Alert]**.
* Door een of meer vrije regelitems voor tabellen te selecteren, klikt u met de rechtermuisknop en selecteert u **[!UICONTROL Create Alert from Selection]**.
* Van binnen een [!UICONTROL Reports & Analytics] rapport, door **[!UICONTROL More]** > **[!UICONTROL Add Alert]**.

De interface van de Bouwer van de Alarm is vertrouwd aan degenen die ingebouwde segmenten of berekende metriek in hebben [!DNL Analytics]:

![](assets/alert_builder.png)

**Waarschuwingsnaam**

Geef een naam op voor de waarschuwing. De waakzame naam zou de naam van het rapport of de metriedrempel kunnen bevatten.

**Tijdgranulatie**

Geef op wanneer u de metrische waarde wilt controleren: Uur, Dagelijks, Wekelijks, of Maandelijks.

>[!NOTE]
>
>Voor rapportsuites met een aangepaste kalender ondersteunen we geen maandelijkse granulariteit in de Waarschuwingsbouwer.

**Ontvangers**

Geef op waar de waarschuwing kan worden verzonden. Een waarschuwing kan naar een [!DNL Analytics] gebruiker, en [!DNL Analytics] groep, een onbewerkt e-mailadres of een telefoonnummer.

>[!IMPORTANT]
>
>Het telefoonnummer moet worden voorafgegaan door een plusteken (+) en een [landcode](https://countrycode.org/).

**Vervaldatum**

Stel de vervaldatum van de waarschuwing in.

**Een waarschuwing verzenden wanneer...**

*... Een van deze metrische trigger*

* Sleep metriek naar het canvas waar triggers worden toegevoegd.

   Let erop dat een **&quot;incompatibele componenten&quot;** Het bericht verschijnt als niet alle componenten (metriek/afmetingen/segmenten) in het alarm compatibel zijn met de momenteel geselecteerde rapportreeks.

* Bepaal de drempel die metrisch moet overschrijden alvorens een alarm wordt geplaatst. U kunt deze waarde instellen op een drempel en vervolgens op een van de volgende voorwaarden:

   * abnormaal
   * anomalie is groter dan verwacht
   * anomalie is minder dan verwacht
   * anomalie overschrijdt
   * boven of gelijk aan
   * lager is dan of gelijk is
   * wijzigingen door

* &quot;Anomaly overschrijdt&quot; is een nieuwe voorwaarde die de bestaande (statische) drempels overschrijdt. Het trekt in Anomaly Detection algoritmen die dynamisch de trekker bepalen. U kunt een drempel instellen van 90%, 95%, 99%, 99,75% en 99,9%.
* Uurgranulariteiten worden vastgesteld op een drempel van 99,75% en dagelijkse granulariteiten op 99%.
* U kunt ook berekende metriek gebruiken.

*... Met deze filters*

Sleep segmenten of dimensies om filters toe te voegen. Als u bijvoorbeeld een segment &quot;Alleen mobiele apparaten&quot; toevoegt, betekent dit dat de regel alleen voor mobiele apparaten wordt geactiveerd.

Aanvullende filters worden toegevoegd met behulp van de instructie AND.

**Een regel toevoegen**

U kunt EN of OF regels toevoegen door het tandwielpictogram te klikken.

## Waarschuwingsvoorvertoning {#section_10D75BA7B77E4C5FAF58A719C082E070}

De interactieve waarschuwingsvoorvertoning laat zien hoe vaak, ongeveer, een waarschuwing wordt geactiveerd op basis van eerdere ervaringen.

Als u bijvoorbeeld de tijdsgranulariteit instelt op dagelijks, kan de voorvertoning u vertellen dat de waarschuwing gedurende een bepaalde metrische x-maal in de afgelopen 30 of 31 dagen zou zijn geactiveerd.

Als u vindt dat te veel waarschuwingen zijn geactiveerd, kunt u de drempel in het dialoogvenster [Waarschuwingsbeheer](/help/components/c-alerts/alert-manager.md).

![](assets/alert_preview.png)
