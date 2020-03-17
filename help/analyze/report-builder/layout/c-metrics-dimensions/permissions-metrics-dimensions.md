---
description: Adobe Report Builder beschikt nu over machtigingsinstellingen die overeenkomen met de instellingen in de beheerprogramma's voor analysemogelijkheden.
title: Toegangsrechten van gebruikers voor afmetingen en metriek
topic: Report builder
uuid: b561407d-c4fa-4f1e-8b16-5ca46fcbf36f
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Toegangsrechten van gebruikers voor afmetingen en metriek

Adobe Report Builder beschikt nu over machtigingsinstellingen die overeenkomen met de instellingen in de beheerprogramma&#39;s voor analysemogelijkheden.

Als gebruiker niet-Admin, kunt u eerder werkboeken met verzoeken hebben gecreeerd die aan dimensies en metriek richten die u geen toegang tot hebt. Deze machtigingen worden nu afgedwongen.

Als u bijvoorbeeld een aanvraag vernieuwt die afmetingen of metriek bevat waartoe u geen toegang hebt, krijgt u een beperkte machtigingsfout:

![](assets/arb_restrc_perm.png)

Volg deze instructies voor **elk** werkboek van de Bouwer van het Rapport dat u handhaaft:

1. Open het werkboek.
1. Alle aanvragen vernieuwen.
1. Als u wordt ertoe aangezet met een fout van de Toestemming van de Toegang van de Gebruiker, klik **[!UICONTROL Open CSV File]** om toegang tot de lijst van beperkte toestemmingsfouten te krijgen.
1. Maak een bestand met de naam AllRestrictedPermissionErrors.xlsx en kopieer/plak de lijst met beperkte machtigingsfouten uit het CSV-bestand in dit bestand.
1. Sluit het werkboek van de Bouwer van het Rapport.

Zodra u alle werkboeken hebt verwerkt, zou u een uitvoerige lijst van beperkte toestemmingsfouten in &quot;AllRestrictedPermissionErrors.xlsx&quot;moeten hebben. Verzend deze lijst naar de beheerder van de de gebruikerstoegang van de Analyse van Adobe, vragend hem om u toegang tot de metriek en de afmetingen te verlenen.
