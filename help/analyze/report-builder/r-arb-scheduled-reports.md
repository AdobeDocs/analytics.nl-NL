---
description: De beschrijvingen van het gebied voor de Geplande Manager van de Taak.
title: Gepland Taakbeheer
feature: Report Builder
role: User, Admin
exl-id: 8bacd7e4-ab50-4b36-842c-a8b6130a58d9
source-git-commit: 91d94ba33328f0ac5fba09cdafb26f58733b4d58
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 1%

---

# Gepland Taakbeheer

De [!UICONTROL Scheduled Task Manager] laat u een lijst van bestaande geplande rapporten, samen met hun ontvangers, planningsdetails, en dossierformaten zien. Ook kunt u geplande werkboeken die niet zijn uitgevoerd opnieuw activeren.

## Oudere geplande taken pauzeren

**15 april 2022** Adobe is van plan alle geplande Report Builder-taken die meer dan twee jaar geleden zijn gemaakt, te pauzeren. Deze pauze is specifiek van toepassing op **alle taken die vóór 31 januari 2020 zijn gemaakt**. Er worden geen taken, werkboeken of gegevens verwijderd. Taken die ouder zijn dan twee jaar, worden onderbroken en er worden geen extra geplande taken verzonden.

Om het even welke taken die u wenst om het verzenden te hervatten kunnen worden opnieuw geactiveerd. Meld u aan bij Report Builder en start de [!UICONTROL Scheduled Task Manager]. Klikken **[!UICONTROL Reactivate]** voor de geplande taak wilt u het verzenden hervatten. Voor elke opnieuw geactiveerde taak geldt een standaardvervaldatum van 18 maanden, tenzij een kortere vervaldatum wordt gekozen.

Bovendien geldt voor elke taak waarvoor de aanmaakdatum minder dan twee jaar bedraagt en waarvoor geen huidige vervaldatum (of met een vervaldatum van meer dan twee jaar) geldt, een standaardvervaldatum van 18 maanden. De nieuwe vervaldatum is 15 oktober 2023. U kunt deze vervaldatum wijzigen in minder dan 18 maanden, maar niet langer. Op het moment van aflopen wordt de taak gepauzeerd. U kunt de taak echter opnieuw activeren met een nieuwe vervaldatum van 18 maanden. Er worden geen taken, werkboeken of gegevens verwijderd.

Het doel van deze pauze is onze geplande takengegevensbestand effectief te beheren en te handhaven om optimale prestaties en levering voor vereiste taken en werkboeken te verzekeren. Dit zal dienen als ons nieuwe governancebeleid. Na 15 april 2022 hebben alle taken een maximale vervaldatum van 18 maanden. Na 18 maanden worden de verlopen taken gepauzeerd en kunnen deze zo nodig opnieuw worden geactiveerd.

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
