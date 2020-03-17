---
description: 'null'
title: Alert Builder
uuid: 86d00a33-dc99-4dc3-a732-0b895ba487bc
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Alert Builder

>[!IMPORTANT]
>
>Intelligente waarschuwingen zijn alleen beschikbaar voor klanten van Adobe [!DNL Analytics] Premiere en Adobe [!DNL Analytics] Ultimate.

U kunt de waarschuwingsfunctie op vier manieren openen:

* Door de volgende kortere weg in de Werkruimte van de Analyse te gebruiken:

   `ctrl (or cmd) + shift + a`
* Ga naar **[!UICONTROL Workspace]** > **[!UICONTROL Components]** > **[!UICONTROL New Alert]**.
* Door een of meer vrije regelitems voor tabellen te selecteren, klikt u met de rechtermuisknop en selecteert u deze **[!UICONTROL Create Alert from Selection]**.
* Ga vanuit een [!UICONTROL Reports & Analytics] rapport naar **[!UICONTROL More]** > **[!UICONTROL Add Alert]**.

De interface van de Bouwer van de Alarm is vertrouwd aan degenen die binnen gebouwde segmenten of berekende metriek [!DNL Analytics]hebben:

![](assets/alert_builder.png)

**Waarschuwingsnaam**

Geef een naam op voor de waarschuwing. De waakzame naam zou de naam van het rapport of de metriedrempel kunnen bevatten.

**Tijdgranulatie**

Geef op wanneer u de metrische waarde wilt controleren: Uur, Dagelijks, Wekelijks, of Maandelijks.

> [!NOTE] Voor rapportsuites met een aangepaste kalender ondersteunen we geen maandelijkse granulariteit in de Waarschuwingsbouwer.

**Ontvangers**

Geef op waar de waarschuwing kan worden verzonden. Een waarschuwing kan naar een [!DNL Analytics] gebruiker, een [!DNL Analytics] groep, een onbewerkt e-mailadres of een telefoonnummer worden verzonden.

>[!IMPORTANT]
>
>Het telefoonnummer moet worden voorafgegaan door een plusteken (+) en een [landcode](https://countrycode.org/).

**Vervaldatum**

Stel de vervaldatum van de waarschuwing in.

**Een waarschuwing verzenden wanneer...**

*... Een van deze metrische trigger*

* Sleep metriek naar het canvas waar triggers worden toegevoegd.

   Merk op dat een **&quot;incompatibele componenten&quot;** bericht zal verschijnen als niet alle componenten (metriek/afmetingen/segmenten) in het alarm compatibel met de momenteel geselecteerde rapportreeks zijn.

* Bepaal de drempel die metrisch moet overschrijden alvorens een alarm wordt geplaatst. U kunt deze waarde instellen op een drempel en op een van de volgende voorwaarden:

   * abnormaal
   * anomalie is groter dan verwacht
   * anomalie is minder dan verwacht
   * anomalie overschrijdt
   * is boven of gelijk aan
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

Als u vindt dat er te veel waarschuwingen zijn geactiveerd, kunt u de drempel aanpassen in [Waarschuwingsbeheer](/help/components/c-alerts/alert-manager.md).

![](assets/alert_preview.png)
