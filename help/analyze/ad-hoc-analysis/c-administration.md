---
description: Configureer gebruikers en leer meer over gegevenssampling.
title: Beheer
uuid: 12f90223-139f-4a8d-bfd3-5cd9af7489d2
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Beheer

Configureer gebruikers en leer meer over gegevenssampling.

Zie de [!DNL Admin Console] Analytics Reference [voor](https://marketing.adobe.com/resources/help/en_US/reference/index.html)hulp.

## Gebruikerslicenties {#concept_C1440741C77C471EB38A243B013EA620}

Voordat een gebruiker zich kan aanmelden, moet aan de gebruiker een gebruikerslicentie worden verleend. Gebruikerslicenties zijn licenties voor gelijktijdig gebruik. Gebruikers kunnen gebruikerslicenties delen, maar het aantal gebruikers op een bepaald tijdstip is beperkt tot het aantal gekochte gebruikerslicenties.

<!-- 

c_user_license.html

 -->

Wanneer het aantal aangemelde gebruikers het aantal beschikbare licenties overschrijdt, wordt de gebruiker in een dialoogvenster gewaarschuwd dat alle beschikbare licenties in gebruik zijn. De positie van de gebruiker in de wachtrij wordt samen met een koppeling weergegeven om de wachtrijpositie opnieuw te controleren. Wanneer een licentie beschikbaar komt, krijgt de gebruiker een e-mail en een pop-updialoogvenster te zien waarin wordt aangegeven dat een ad-hocanalyse beschikbaar is voor toegang. De gebruiker heeft dan 15 minuten om te antwoorden alvorens de positie in de rij te verliezen.

## Gebruikerslicenties verlenen {#task_22AE669703EC48BA9685414538D8B1FA}

Stappen die beschrijven hoe de lokale beheerders van Rapporten en van Analytics gebruikersvergunningen via het toestemmingensysteem kunnen verlenen.

<!-- 

t_user_licenses.xml

 -->

1. Meld u aan bij de [!DNL Experience Cloud].
1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL User Management]**.
1. Klik op **[!UICONTROL Edit Groups]**.

   Als uw bedrijf gebruikersvergunningen heeft gekocht, verschijnt de [!UICONTROL Ad Hoc Analysis License Users] groep in de [!UICONTROL Group Name] kolom. Het aantal beschikbare licenties voor gebruikersaanmeldingen wordt ook weergegeven.

1. Klik op **[!UICONTROL Edit]**.
1. Selecteer onder [!UICONTROL Assign User Logins], de gebruikers die u aan de groep wilt toevoegen, en klik vervolgens op **[!UICONTROL Add.]**
1. Klik op **[!UICONTROL Save Group]**.

   Het licentiesysteem beperkt niet het aantal gebruikers dat aan een groep wordt toegevoegd. Er is slechts een beperkt gebruik tegelijkertijd van het aantal gekochte gebruikerslicenties.

## Gebruikerssessies beheren {#task_868C3DD9CB3F45D19B98EEF60F5E0B32}

Stappen die beschrijven hoe een beheerder de zitting van een gebruiker kan beëindigen. Deze eigenschap verhindert niet een geëindigde gebruiker opnieuw het programma te openen.

<!-- 

t_managing_users.xml

 -->

1. Klik **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]**, dan klik **[!UICONTROL Manage Users]**.
1. Zoek de gebruiker en klik vervolgens op **[!UICONTROL Terminate.]**

   Op de [!UICONTROL Active Ad Hoc Analysis Sessions] pagina wordt de gebruiker die het langst inactief is, boven aan de lijst weergegeven.

## Machtigingen {#concept_A7F2A7600BFF47C38D7C980E08D395B8}

<!-- 

c_permissions.xml

 -->

U stelt toegang in om te rapporteren suites in de [!DNL Administration Console]. U kunt toestemming op het niveau van de rapportreeks vormen. Bijvoorbeeld, als u veelvoudige toegelaten rapportreeksen hebt, maar u niet alle gebruikers toegang tot alle rapportreeksen wilt verlenen, kunt u groepen met specifieke rapportreeksen tot stand brengen, en dan die gebruikers toewijzen aan de toepasselijke groep.

## Voeg een Gebruiker aan de Al Groep van de Toegang van het Rapport toe {#task_E821BF3B4FDB434D844A98AAB15487A9}

Stappen die beschrijven hoe te om gebruikers niet-admin toegang tot alle rapportsuites te verlenen.

<!-- 

t_permissions.xml

 -->

1. Meld u aan bij de **[!UICONTROL Experience Cloud]**.
1. Klik op **[!UICONTROL Adobe Analytics > Admin]** > **[!UICONTROL User Management]** > **[!UICONTROL Edit Groups]**.
1. Klik op **[!UICONTROL All Report Access]**.
1. Selecteer [!UICONTROL Available Users]de gebruiker en klik vervolgens op **[!UICONTROL Add.]**
1. Klik op **[!UICONTROL Save Group]**.

## Machtigingsgroepen maken {#task_65A4C2E58B13475B9B2606CEB93B7CBD}

Creeer toestemmingsgroepen voor niet-admin gebruikers voor specifieke rapportreeksen.

<!-- 

t_permission_groups.xml

 -->

1. Meld u aan bij de **[!UICONTROL Experience Cloud]**.
1. Klik op **[!UICONTROL Adobe Analytics > Admin]** > **[!UICONTROL User Management]** > **[!UICONTROL Edit Groups]**.
1. Maak een machtigingengroep voor gebruikers die geen beheerder zijn en die de door ad-hocanalyse geactiveerde rapportsuites bevat die u toegankelijk wilt maken voor gebruikers.

   De rapportsuites beschikbaar aan de gebruiker worden getoond in het [!UICONTROL Report Cloud] menu wanneer u een nieuw project creeert.

## Proxybeleid instellen in Java {#task_3B03F58519544025B55CF54FACF8F4F5}

Stappen die beschrijven hoe u proxybeleid kunt instellen als u een fout met de serververbinding ontvangt.

<!-- 

t_proxy_policies.xml

 -->

De ad hoc Analyse gebruikt HTTP om met de server te communiceren. Het is onderworpen aan het zelfde volmachtsbeleid zoals ander verkeer van HTTP.

1. Start in de [!DNL Windows Control Panel]app de [!UICONTROL Java Control Panel].
1. On the **[!UICONTROL General]** tab, click **[!UICONTROL Network Settings]**.
1. Selecteer de proxyinstellingen **[!UICONTROL Use browser settings]** of configureer deze handmatig.
1. Klik **[!UICONTROL OK]** en klik vervolgens **[!UICONTROL OK]** op de knop [!UICONTROL Java Control Panel].

## Hoe gegevens worden bemonsterd {#concept_8433CFD38E0243849E92DF4F1E743AC3}

Er worden voorbeelden van bezoekersgegevens genomen om zinvolle, nauwkeurige rapportage te produceren. Het datumbereik wordt gebruikt als het gegevenssegment voor een geladen project. Een segment vertegenwoordigt doorgaans de huidige maand plus de voorafgaande twee maanden.

<!-- 

c_overview_data_sampling.xml

 -->

Voor een optimale verwerking gebruikt ad-hocanalyse ongeveer 750 miljoen als het maximale aantal resultaten per segment. (Hits = paginaweergaven + gebeurtenissen.)

Om tot het verwachte steekproeftarief te komen, worden de geprojecteerde resultaten berekend per gegevensreeks, dan gedeeld door 750 miljoen, zoals hier getoond:

* (Gem. dagelijks aantal hits ( x aantal dagen in het segment ) / 750 miljoen

Als u bijvoorbeeld 10 miljoen hits per dag hebt, met een gegevenssegment van 90 dagen:

* (10,000,000 x 90) / 750,000,000 = 1,2

Om het aantal treffers voor dit segment van 90 dagen onder 750.000.000 te houden, konden de gegevens worden bemonsterd bij 1.2:1, maar omdat steekproeven op hele aantallen worden gebruikt, is het steekproeftarief 2:1.

Een ander voorbeeld: als je 10 miljoen hits per dag hebt, met een gegevenssegment van 365 dagen:

* (10,000,000 x 365) / 750,000,000 = 4,8

Om het aantal treffers voor dit segment van 365 dagen onder 750.000.000 te houden, konden de gegevens worden bemonsterd bij 4.8:1. Met hele getallen is de samplingfrequentie 5:1.
