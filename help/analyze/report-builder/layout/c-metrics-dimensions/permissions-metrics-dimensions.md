---
description: Adobe Report Builder beschikt nu over machtigingsinstellingen die overeenkomen met de instellingen in Admin Tools voor Analytics.
title: Toegangsrechten van gebruikers voor dimensies en cijfers
uuid: b561407d-c4fa-4f1e-8b16-5ca46fcbf36f
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---


# Toegangsrechten van gebruikers voor dimensies en cijfers

Adobe Report Builder beschikt nu over machtigingsinstellingen die overeenkomen met de instellingen in Admin Tools voor Analytics.

Als gebruiker niet-Admin, kunt u eerder werkboeken met verzoeken hebben gecreeerd die aan dimensies en metriek richten die u geen toegang tot hebt. Deze machtigingen worden nu afgedwongen.

Als u bijvoorbeeld een aanvraag vernieuwt die afmetingen of metriek bevat waartoe u geen toegang hebt, krijgt u een beperkte machtigingsfout:

![](assets/arb_restrc_perm.png)

Volg deze instructies voor **each** werkboek van Report Builder dat u handhaaft:

1. Open het werkboek.
1. Alle aanvragen vernieuwen.
1. Als u wordt ertoe aangezet met een fout van de Toestemming van de Toegang van de Gebruiker, klik **[!UICONTROL Open CSV File]** om toegang tot de lijst van beperkte toestemmingsfouten te krijgen.
1. Maak een bestand met de naam AllRestrictedPermissionErrors.xlsx en kopieer/plak de lijst met beperkte machtigingsfouten uit het CSV-bestand in dit bestand.
1. Sluit het werkboek van de Report Builder.

Zodra u alle werkboeken hebt verwerkt, zou u een uitvoerige lijst van beperkte toestemmingsfouten in &quot;AllRestrictedPermissionErrors.xlsx&quot;moeten hebben. Verzend deze lijst naar de beheerder van de de gebruikerstoegang van Adobe Analytics, vragend hem om u toegang tot de metriek en de afmetingen te verlenen.
