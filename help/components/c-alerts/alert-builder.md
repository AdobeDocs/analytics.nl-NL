---
description: Gebruik waarschuwingen in Analysis Workspace.
title: Overzicht van Alert Builder
feature: Alerts
exl-id: 82e51357-4a32-4db1-bc56-95a72dbaa1be
source-git-commit: 75d8705170169a0ef9f1ee59b12e4bb2c3afac7a
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---

# Waarschuwingen maken {#create-alerts}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_alerts_timegranularity"
>title="Tijdkorreligheid"
>abstract="De tijdsgranulariteit heeft zowel betrekking op de frequentie waarmee de waarschuwing wordt gecontroleerd als op de frequentie waarmee de waarschuwing wordt opgenomen"

<!-- markdownlint-enable MD034 -->

>[!NOTE]
>
>Het gebruiken van alarm met anomalieopsporing (die ook als _Intelligente Alarm_ wordt bekend) is beschikbaar slechts aan organisaties met een pakket van Adobe Analytics Prime of van Ultimate.

Met waarschuwingen in Adobe Analytics kunt u op basis van gewijzigde percentages of specifieke gegevenspunten op de hoogte worden gesteld. Afhankelijk van het Adobe Analytics-pakket kunt u ook waarschuwingen gebruiken die op basis van afwijkende drempelwaarden moeten worden geactiveerd. Het alarm van het het vraaggebruik van de server is een verschillend soort alarm dat slechts aan de beheerders van Analytics beschikbaar is. Deze waarschuwingen stellen u op de hoogte van het risico of het voorkomen van een overage in de gegevens van het servervraagverbruik en de verplichting. Voor meer informatie, zie {het alarm van het de vraaggebruik van de Server 0} ](/help/admin/admin/c-server-call-usage/scu-alerts.md).[

Voor meer gedetailleerde overzichtsinformatie over alarm, zie [ het overzicht van Alarm ](/help/components/c-alerts/intellligent-alerts.md).

Een waarschuwing maken:

1. Begin met het maken van een waarschuwing door toegang te krijgen tot de waarschuwingsbuilder. U kunt tot de waakzame bouwer op om het even welke volgende manieren toegang hebben:

   * Open een project in Analysis Workspace en selecteer vervolgens **[!UICONTROL Components]** > **[!UICONTROL Create alert]** .
   * Open een project in Analysis Workspace, dan gebruik de volgende kortere weg: ***ctrl (of cmd) + shift + a***.
   * Open een project in Analysis Workspace, selecteer één of meerdere lijnpunten in een vrije vormlijst, dan klik met de rechtermuisknop aan en selecteer **[!UICONTROL Create alert from selection]**. Deze actie vult onmiddellijk de waakzame bouwer vooraf in om een alarm met de correcte metriek en de filters tot stand te brengen.
   * Creeer een alarm [ van waakzame manager ](/help/components/c-alerts/alert-manager.md#create-alerts).

   De waakzame bouwer toont. Deze interface is vertrouwd aan de interface om segmenten of berekende metriek in Analytics te bouwen:

   ![](assets/alert-builder.png)

1. Geef de volgende opties op om de waarschuwing te configureren:

   | Optie | Beschrijving |
   |---------|----------|
   | [!UICONTROL **Titel**] | Geef een naam op voor de waarschuwing. De waakzame naam zou de naam van het rapport of de metriedrempel kunnen bevatten. |
   | [!UICONTROL **Beschrijving (facultatief)**] | Geef een beschrijving voor de waarschuwing op. |
   | [!UICONTROL **granulariteit van de Tijd**] | Selecteer hoe vaak u metrisch wilt controleren: Uur, Dagelijks, Wekelijks, of Maandelijks.<p><b> Nota:</b> voor rapportreeksen met een douanekalender, wordt maandelijkse granulariteit in de Waakzame Bouwer niet gesteund.<!--true?--></p> |
   | [!UICONTROL **Ontvangers**] | Geef op waar de waarschuwing kan worden verzonden. Een waarschuwing kan naar een gebruiker van de Analyse, een groep van Analytics, een onbewerkt e-mailadres, of naar een telefoonaantal worden verzonden.<p><b> Belangrijk:</b> het telefoonaantal moet door `+` en a [ landcode ](https://countrycode.org/) worden voorafgegaan.</p><p>De e-mail die een gebruiker zou ontvangen zodra een alarm is teweeggebracht kijkt gelijkaardig aan:</p><p>![](assets/alerts-email.PNG)</p> |
   | [!UICONTROL **Vervaldatum**] | Stel de datum en tijd in waarop de waarschuwing moet verlopen. |
   | [!UICONTROL **verzend een alarm wanneer**] | [!UICONTROL **om het even welk van deze metrieke trekker**]: Sleep en dalingsmetriek (met inbegrip van berekende metriek) hier om trekkers voor het alarm tot stand te brengen.<p>Een **&quot;incompatibele componenten&quot;** bericht verschijnt als niet alle metriek, dimensies, of segmenten in de alarm compatibel zijn met de momenteel geselecteerde gegevensmening.</p><p>Bepaal de drempel die metrisch moet overschrijden alvorens een alarm wordt geplaatst. U kunt deze waarde instellen op een drempel en vervolgens op een van de volgende voorwaarden:</p><ul><li>anomalie bestaat</li><li>anomalie is groter dan verwacht</li><li>anomalie is minder dan verwacht</li><li>is boven of gelijk aan</li><li>is lager of gelijk aan</li><li>wijzigingen door</li><li>U kunt een drempel instellen van 90%, 95%, 99%, 99,75% en 99,9%.</li></ul><p>[!UICONTROL **met elk van deze filters**]: Sleep en dalingssegmenten of dimensies om filters toe te voegen. Als u bijvoorbeeld een segment &quot;Alleen mobiele apparaten&quot; toevoegt, betekent dit dat de regel alleen voor mobiele apparaten wordt geactiveerd. U kunt extra filters toevoegen door een EN verklaring te gebruiken. U kunt EN of OF regels toevoegen door het tandwielpictogram te klikken.</p><p>Zie [ Alarm - gebruiksgevallen ](/help/components/c-alerts/alerts-use-cases.md) bijvoorbeeld.</p> |
   | [!UICONTROL **Voorproef**] | De interactieve waarschuwingsvoorvertoning laat zien hoe vaak, ongeveer, een waarschuwing wordt geactiveerd op basis van eerdere ervaringen.<p>Als u bijvoorbeeld de tijdsgranulariteit instelt op dagelijks, kan de voorvertoning u vertellen dat de waarschuwing gedurende een bepaalde metrische x-maal in de afgelopen 30 of 31 dagen zou zijn geactiveerd.</p><p>Als u vindt dat teveel alarm zal teweeggebracht worden, kunt u de drempel in de [ Waakzame Manager ](/help/components/c-alerts/alert-manager.md) aanpassen.</p><p>![](assets/alert_preview.png)</p> |

1. Selecteer [!UICONTROL **sparen**].
