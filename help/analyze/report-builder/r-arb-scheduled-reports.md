---
description: De beschrijvingen van het gebied voor de Geplande Manager van de Taak.
title: Gepland Taakbeheer
uuid: dec259f0-2a04-4c94-abbc-5008cf2f1cb8
feature: Report Builder
role: Bedrijfs Praktijk, Beheerder
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 2%

---


# Gepland Taakbeheer

De Geplande Manager van de Taak laat u een lijst van bestaande geplande rapporten, samen met hun ontvangers, planningsdetails, en dossierformaten zien. Ook kunt u geplande werkboeken die niet zijn uitgevoerd opnieuw activeren.

| Veld | Beschrijving |
| --- | --- |
| **Tabblad Geplande rapporten** |  |
| Rapportnaam | Geeft de naam van de geplande taak aan. |
| E-mail/FTP | Het e-mailadres of FTP-adres van de ontvanger. **Opmerking:** Als e-mail is geselecteerd, worden rapporten die groter zijn dan 1 MB automatisch als ZIP-bestand aan de e-mail toegevoegd. Deze functie helpt de grootte van het bijlagebestand klein te houden en kan niet worden uitgeschakeld. |
| Publicatieopties | In deze kolom wordt Power BI weergegeven als een van de [publicatieopties voor Power BI](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/publish-powerbi/power-bi.html) is geselecteerd. |
| Schema | Het geplande type levering. |
| Bestandsindeling | De leveringsindeling van het rapport, zoals Excel, PDF, HTML, enzovoort. |
| Opnieuw activeren | Wanneer een gepland werkboek niet in werking stelt, probeert Report Builder om het werkboek tweemaal om de vijftien minuten in werking te stellen. Na drie mislukte pogingen deactiveert Report Builder het programma en toont de Reactivate knoop. Wanneer u een werkboek opnieuw activeert, begint de geplande levering opnieuw van de tijd het werd gedeactiveerd.  Bijvoorbeeld, als een gepland werkboek 14 dagen geleden werd gedeactiveerd, en u het vandaag opnieuw activeert, loopt het voor elke ontbrekende dag en zal 14 keer worden geleverd. Als u niet het werkboek voor de ontbrekende dagen wordt geleverd, kunt u het geplande werkboek schrappen en dan een nieuw gepland werkboek creëren gebruikend de zelfde het plannen parameters.   Opmerking:  U zou geen werkboek moeten reactiveren tenzij u de reden kent het systeem het onbruikbaar maakte. Één het oplossen van problemenoplossing moet een gedeactiveerd werkboek downloaden, en het op de cliëntkant verfrissen. Als u geen fouten ziet, moet u het opnieuw kunnen activeren. |
| Laatst verzonden | De datum en het tijdstip waarop het rapport voor het laatst is verzonden. |
| **Het tabblad Ontvanger** |  |
| E-mail ontvanger | De e-mailontvanger van het rapport. |
| Rapporten | De rapporten die naar elke ontvanger zijn verzonden. |
| **Tabblad Rapportgeschiedenis** |  |
| Bestandsnaam | Geeft de naam van de geplande taak aan. |
| Datum | De datum en het tijdstip waarop het rapport voor het laatst is verzonden. |
| Status | De status geeft aan of het rapport is verzonden of niet is verzonden. |
| E-mail/FTP | Het e-mailadres of FTP-adres van de ontvanger van het rapport. |
| Bestandsindeling | De leveringsindeling van het rapport, zoals Excel, PDF, HTML, enzovoort. |

