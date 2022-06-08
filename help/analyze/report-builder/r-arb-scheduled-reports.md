---
description: De beschrijvingen van het gebied voor de Geplande Manager van de Taak.
title: Gepland Taakbeheer
feature: Report Builder
role: User, Admin
exl-id: 8bacd7e4-ab50-4b36-842c-a8b6130a58d9
source-git-commit: 9a16f3942505028624e5c07568342a9acac898d7
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Gepland Taakbeheer

De [!UICONTROL Scheduled Task Manager] laat u een lijst van bestaande geplande rapporten, samen met hun ontvangers, planningsdetails, en dossierformaten zien. Ook kunt u geplande werkboeken die niet zijn uitgevoerd opnieuw activeren.

## Oudere geplande taken pauzeren

Op 21 april 2022 hebben we wijzigingen doorgevoerd in de geplande taken in Report Builder als onderdeel van onze inspanningen om de prestaties en prestaties te optimaliseren. Deze wijzigingen omvatten het verwijderen van de mogelijkheid om geplande leveringen &#39;end na x occurrences&#39; te laten beëindigen. In antwoord op verschillende verzoeken van klanten die meer tijd zoeken om alternatieven te onderzoeken en te implementeren, hebben we besloten deze optie op beperkte wijze te herstellen tot **31 jan. 2023**.

U kunt Report Builder-taken per uur blijven plannen en deze na maximaal 99 exemplaren laten beëindigen. De terugdraaiing geldt alleen voor uurwerk. het &quot; einde na x &quot; komt niet voor alle andere leveringsintervallen ( dagelijks , wekelijks , maandelijks en jaarlijks ) .

Deze optie wordt afgekeurd op 31 januari 2023.
Neem voor meer vragen of ondersteuning contact op met de klantenservice van Adobe.

Deze pauze is specifiek van toepassing op **alle taken die vóór 31 januari 2020 zijn gemaakt**. Er worden geen taken, werkboeken of gegevens verwijderd. Taken die ouder zijn dan twee jaar, worden onderbroken en er worden geen extra geplande taken verzonden.

Om het even welke taken die u wenst om het verzenden te hervatten kunnen worden opnieuw geactiveerd. Meld u aan bij Report Builder en start de [!UICONTROL Scheduled Task Manager]. Klikken **[!UICONTROL Reactivate]** voor de geplande taak wilt u het verzenden hervatten. Voor elke opnieuw geactiveerde taak geldt een standaardvervaldatum van 18 maanden, tenzij een kortere vervaldatum wordt gekozen.

Bovendien geldt voor elke taak waarvoor de aanmaakdatum minder dan twee jaar bedraagt en waarvoor geen huidige vervaldatum (of met een vervaldatum van meer dan twee jaar) geldt, een standaardvervaldatum van 18 maanden. De nieuwe vervaldatum is 15 oktober 2023. U kunt deze vervaldatum wijzigen in minder dan 18 maanden, maar niet langer. Op het moment van aflopen wordt de taak gepauzeerd. U kunt de taak echter opnieuw activeren met een nieuwe vervaldatum van 18 maanden. Er worden geen taken, werkboeken of gegevens verwijderd.

Het doel van deze pauze is onze geplande takengegevensbestand effectief te beheren en te handhaven om optimale prestaties en levering voor vereiste taken en werkboeken te verzekeren. Dit zal dienen als ons nieuwe governancebeleid. Na 31 januari 2023 hebben alle taken een maximale vervaldatum van 18 maanden. Na 18 maanden worden de verlopen taken gepauzeerd en kunnen deze zo nodig opnieuw worden geactiveerd.

## Geplande taken configureren

| Veld | Beschrijving |
| --- | --- |
| **[!UICONTROL Scheduled Reports tab]** |  |
| [!UICONTROL Report Name] | Geeft de naam van de geplande taak aan. |
| [!UICONTROL Email/FTP] | Het e-mailadres of FTP-adres van de ontvanger. **Opmerking:** Als e-mail is geselecteerd, worden rapporten die groter zijn dan 1 MB automatisch als .zip-bestand aan de e-mail toegevoegd. Deze functie helpt de grootte van het bijlagebestand klein te houden en kan niet worden uitgeschakeld. |
| [!UICONTROL Publishing Options] | In deze kolom wordt Power BI weergegeven als een van de [Publicatieopties voor Power BI](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/publish-powerbi/power-bi.html) is geselecteerd. |
| [!UICONTROL Schedule] | Het geplande type levering. |
| [!UICONTROL File Format] | Het leveringsformaat van het rapport, zoals Excel, PDF, HTML, etc. |
| [!UICONTROL Reactivate] | Wanneer een gepland werkboek niet in werking stelt, probeert Report Builder om het werkboek tweemaal om de vijftien minuten in werking te stellen. Na drie mislukte pogingen deactiveert Report Builder het programma en toont de Reactivate knoop. Wanneer u een werkboek opnieuw activeert, begint de geplande levering opnieuw van de tijd het werd gedeactiveerd.<p>Bijvoorbeeld, als een gepland werkboek 14 dagen geleden werd gedeactiveerd, en u het vandaag opnieuw activeert, loopt het voor elke ontbrekende dag en zal 14 keer worden geleverd. Als u niet het werkboek voor de ontbrekende dagen wordt geleverd, kunt u het geplande werkboek schrappen en dan een nieuw gepland werkboek creëren gebruikend de zelfde het plannen parameters.<p>**Opmerking:** Activeer een werkboek niet tenzij u de reden kent het systeem het onbruikbaar maakte. Om problemen op te lossen, download een gedeactiveerd werkboek en vernieuw het op de cliëntkant. Als u geen fouten ziet, moet u het opnieuw kunnen activeren. |
| [!UICONTROL Last sent] | De datum en het tijdstip waarop het rapport voor het laatst is verzonden. |
| **Het tabblad Ontvanger** |  |
| [!UICONTROL Recipient email] | De e-mailontvanger van het rapport. |
| [!UICONTROL Reports] | De rapporten die naar elke ontvanger werden verzonden. |
| **Tabblad Rapportgeschiedenis** |  |
| [!UICONTROL File Name] | Geeft de naam van de geplande taak aan. |
| [!UICONTROL Date] | De datum en het tijdstip waarop het rapport voor het laatst is verzonden. |
| [!UICONTROL Status] | De status geeft aan of het rapport is verzonden of niet is verzonden. |
| [!UICONTROL Email/FTP] | Het e-mailadres of FTP-adres van de ontvanger van het rapport. |
| [!UICONTROL File Format] | Het leveringsformaat van het rapport, zoals Excel, PDF, HTML, etc. |
