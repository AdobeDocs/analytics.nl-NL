---
description: Leer over de gebiedsbeschrijvingen voor de Geplande Manager van de Taak.
title: Ongeveer de Geplande Manager van de Taak
feature: Report Builder
role: User, Admin
exl-id: 8bacd7e4-ab50-4b36-842c-a8b6130a58d9
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# Geplande Taakmanager

{{legacy-arb}}

Met [!UICONTROL Scheduled Task Manager] kunt u een lijst met bestaande geplande rapporten weergeven, samen met de ontvangers, planningsdetails en bestandsindelingen. Ook kunt u geplande werkboeken die niet zijn uitgevoerd opnieuw activeren.

## Oudere geplande taken pauzeren

Op 21 april 2022 hebben we wijzigingen doorgevoerd in de geplande taken in Report Builder als onderdeel van onze inspanningen voor het optimaliseren van prestaties en levering. Deze wijzigingen omvatten het verwijderen van de mogelijkheid om geplande leveringen &#39;end na x occurrences&#39; te laten beëindigen. In antwoord op verscheidene klantenverzoeken die meer tijd zoeken om alternatieven te onderzoeken en uit te voeren, hebben wij besloten om deze optie op een beperkte manier tot **Jan 31, 2023** te herstellen.

U kunt Report Builder-taken per uur blijven plannen en deze na maximaal 99 exemplaren laten beëindigen. De rollback is alleen van toepassing op taken per uur. De &quot;end after x occurrences&quot; blijft niet beschikbaar voor alle andere leveringsintervallen (dagelijks, wekelijks, maandelijks en jaarlijks).

Deze optie wordt per 31 januari 2023 ingetrokken.
Neem voor meer vragen of ondersteuning contact op met de klantenservice van Adobe.

Specifiek, is deze pauze op **van toepassing om het even welke die taken vóór 31 Januari, 2020** worden gecreeerd. Er worden geen taken, werkboeken of gegevens verwijderd. Taken die ouder zijn dan twee jaar, worden onderbroken en er worden geen extra geplande taken verzonden.

Om het even welke taken die u wenst om het verzenden te hervatten kunnen worden opnieuw geactiveerd. Meld u aan bij Report Builder en start de [!UICONTROL Scheduled Task Manager] . Klik op **[!UICONTROL Reactivate]** voor de geplande taak die u opnieuw wilt verzenden. Voor elke opnieuw geactiveerde taak geldt een standaardvervaldatum van 18 maanden, tenzij een kortere vervaldatum wordt gekozen.

Bovendien geldt voor elke taak waarvoor de aanmaakdatum minder dan twee jaar bedraagt en waarvoor geen huidige vervaldatum (of met een vervaldatum van meer dan twee jaar) geldt, een standaardvervaldatum van 18 maanden. De nieuwe vervaldatum is 15 oktober 2023. U kunt deze vervaldatum wijzigen in minder dan 18 maanden, maar niet langer. Op het moment van aflopen wordt de taak gepauzeerd. U kunt de taak echter opnieuw activeren met een nieuwe vervaldatum van 18 maanden. Er worden geen taken, werkboeken of gegevens verwijderd.

Het doel van deze pauze is onze geplande takengegevensbestand effectief te beheren en te handhaven om optimale prestaties en levering voor vereiste taken en werkboeken te verzekeren. Dit zal dienen als ons nieuwe governancebeleid. Na 31 januari 2023 hebben alle taken een maximale vervaldatum van 18 maanden. Na 18 maanden worden de verlopen taken gepauzeerd en kunnen deze zo nodig opnieuw worden geactiveerd.

## Geplande taken configureren

| Veld | Beschrijving |
| --- | --- |
| **[!UICONTROL Scheduled Reports tab]** | |
| [!UICONTROL Report Name] | Geeft de naam van de geplande taak aan. |
| [!UICONTROL Email/FTP] | Het e-mailadres of FTP-adres van de ontvanger. **Nota:** als e-mail wordt geselecteerd, worden de rapporten groter dan 1 MB automatisch in bijlage aan e-mail als .zip dossier. Deze functie helpt de grootte van het bijlagebestand klein te houden en kan niet worden uitgeschakeld. |
| [!UICONTROL Publishing Options] | Deze kolom zal van Power BI een lijst maken als één van [ Power BI het publiceren opties ](/help/analyze/legacy-report-builder/c-publish-power-bi/power-bi.md) wordt geselecteerd. |
| [!UICONTROL Schedule] | Het geplande type levering. |
| [!UICONTROL File Format] | De leveringsformaat van het rapport, zoals Excel, PDF, HTML, etc. |
| [!UICONTROL Reactivate] | Wanneer een gepland werkboek niet in werking stelt, probeert Report Builder om het werkboek twee keer om de vijftien minuten in werking te stellen. Na drie mislukte pogingen deactiveert Report Builder het programma en geeft de knop Opnieuw activeren weer. Wanneer u een werkboek opnieuw activeert, begint de geplande levering opnieuw van de tijd het werd gedeactiveerd.<p>Bijvoorbeeld, als een gepland werkboek 14 dagen geleden werd gedeactiveerd, en u het vandaag opnieuw activeert, loopt het voor elke ontbrekende dag en zal 14 keer worden geleverd. Als u niet het werkboek voor de ontbrekende dagen wordt geleverd, kunt u het geplande werkboek schrappen en dan een nieuw gepland werkboek creëren gebruikend de zelfde het plannen parameters.<p>**Nota:** activeer geen werkboek tenzij u de reden kent het systeem het onbruikbaar maakte. Om problemen op te lossen, download een gedeactiveerd werkboek en vernieuw het op de cliëntkant. Als u geen fouten ziet, moet u het opnieuw kunnen activeren. |
| [!UICONTROL Last sent] | De datum en het tijdstip waarop het rapport voor het laatst is verzonden. |
| **Ontvanger lusje** | |
| [!UICONTROL Recipient email] | De e-mailontvanger van het rapport. |
| [!UICONTROL Reports] | De rapporten die naar elke ontvanger werden verzonden. |
| **het lusje van de Geschiedenis van Rapporten** | |
| [!UICONTROL File Name] | Geeft de naam van de geplande taak aan. |
| [!UICONTROL Date] | De datum en het tijdstip waarop het rapport voor het laatst is verzonden. |
| [!UICONTROL Status] | De status geeft aan of het rapport is verzonden of niet is verzonden. |
| [!UICONTROL Email/FTP] | Het e-mailadres of FTP-adres van de ontvanger van het rapport. |
| [!UICONTROL File Format] | De leveringsformaat van het rapport, zoals Excel, PDF, HTML, etc. |
