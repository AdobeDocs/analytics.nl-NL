---
description: Adobe Report Builder beschikt nu over machtigingsinstellingen die overeenkomen met de instellingen in Admin Tools voor Analytics.
title: Toegangsrechten van gebruikers voor afmetingen en metriek
uuid: b561407d-c4fa-4f1e-8b16-5ca46fcbf36f
feature: Report Builder
role: User, Admin
exl-id: 53cfdcf4-31c3-40ab-aca4-8f0f9be6fe13
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Toegangsrechten van gebruikers voor afmetingen en metriek

{{legacy-arb}}

Adobe Report Builder heeft machtigingsinstellingen die vergelijkbaar zijn met de instellingen in de hulpprogramma&#39;s voor Analysebeheer.

Als gebruiker niet-Admin, kunt u eerder werkboeken met verzoeken hebben gecreeerd die aan dimensies en metriek richten die u geen toegang tot hebt. Deze machtigingen worden nu afgedwongen.

Als u bijvoorbeeld een aanvraag vernieuwt die afmetingen of metriek bevat waartoe u geen toegang hebt, krijgt u een beperkte machtigingsfout. In het foutbericht staat dat een aanvraag niet beschikbaar is voor uw gebruikersaccount vanwege beheerdersrechten.

![ Scherenshot die het Beperkte bericht van de Fout van de Toestemming toont.](assets/arb_restrc_perm.png)

Volg deze instructies voor **elk** werkboek van de Report Builder dat u handhaaft:

1. Open het werkboek.
1. Alle aanvragen vernieuwen.
1. Als u wordt veroorzaakt met een fout van de Toestemming van de Toegang van de Gebruiker, klik **[!UICONTROL Open CSV File]** om toegang tot de lijst van beperkte toestemmingsfouten te krijgen.
1. Maak een bestand met de naam AllRestrictedPermissionErrors.xlsx en kopieer/plak de lijst met beperkte machtigingsfouten uit het CSV-bestand in dit bestand.
1. Sluit het werkboek van de Report Builder.

Zodra u alle werkboeken hebt verwerkt, zou u een uitvoerige lijst van beperkte toestemmingsfouten in &quot;AllRestrictedPermissionErrors.xlsx&quot;moeten hebben. Verzend deze lijst naar de beheerder van de de gebruikerstoegang van Adobe Analytics, vragend hem om u toegang tot de metriek en de afmetingen te verlenen.
