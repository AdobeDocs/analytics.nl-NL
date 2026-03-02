---
title: Report Builder instellen
description: Leer een complete handleiding voor het installeren en configureren van Adobe Analytics Report Builder for Excel. Stapsgewijze installatie-instructies voor naadloze integratie.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 9d0161a9-ee7b-43a9-92ad-4079cf4b9c6c
source-git-commit: 1e893ce94ee3da46bbf22d7a90573681950d1135
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Report Builder instellen

In dit artikel worden de vereisten beschreven voor het gebruik van Report Builder for Adobe Analytics in [!DNL Microsoft] [!DNL Excel] . En hoe te om toe:voegen-binnen te installeren en te opstelling.

## Vereisten

Report Builder for Adobe Analytics wordt ondersteund door de volgende besturingssystemen en webbrowsers.

### macOS

- macOS versie 10.x of hoger
- Alle [!DNL Microsoft] [!DNL Excel] versies

### Windows

- Windows 10, versie 1904 of hoger
- [!DNL Excel] Versie 2106 of hoger

  Alle gebruikers van Windows Desktop [!DNL Excel] moeten Microsoft Edge Webview2 installeren om toe:voegen-binnen te gebruiken. De controller installeren:

   1. Ga naar <https://aka.ms/webview2installer> .
   1. Selecteer en download het Evergreen standalone-installatieprogramma.
   1. Volg de installatieaanwijzingen.

### Webkantoor

- Ondersteunt alle browsers en versies


## Report Builder Excel Add-in

U moet de [!DNL Excel] Add-in van Report Builder installeren om [!DNL Report Builder] voor Adobe Analytics te kunnen gebruiken. Nadat u de [!DNL Excel] Add-in voor Report Builder hebt geïnstalleerd, hebt u vanuit een open [!DNL Excel] -werkmap toegang tot Report Builder.

### De Report Builder Add-in downloaden en installeren

De Report Builder Add-in downloaden en installeren

1. Start [!DNL Excel] en open een nieuw werkboek.

1. Selecteer **[!UICONTROL Insert]** > **[!UICONTROL Get Add-ins]** .

1. Selecteer het tabblad Opslag in het dialoogvenster Office Add-ins.

1. Zoek naar &quot;Report Builder&quot; en klik op **[!UICONTROL Add]** .

1. Klik in het dialoogvenster Licentievoorwaarden en privacybeleid op **[!UICONTROL Continue]** .

**als het lusje van de Opslag niet wordt getoond**

1. Selecteer Bestand > Account > Instellingen beheren in [!DNL Excel] .

1. Schakel het selectievakje naast &quot;Optionele ervaringen met verbinding inschakelen&quot; in.

1. Start [!DNL Excel] opnieuw.

**als uw organisatie toegang tot de Opslag van Microsoft** blokkeert

- Vraag uw IT- of beveiligingsteam om goedkeuring voor de Report Builder Add-in. Nadat goedkeuring is verleend, selecteert u in het dialoogvenster Office Add-ins de tab **[!UICONTROL Admin Managed]** .

  ![&#x200B; Admin Beheerde lusje in de dialoog van toe:voegen-ins van het Bureau.](./assets/image1.png)

- Alternatief, kunt u het [&#x200B; duidelijke dossier &#x200B;](https://reportbuilder.an.adobe.com/manifest.xml) manueel terugwinnen en het dossier op uw eigen infrastructuur van IT ontvangen. <br/> te volgen gelieve de 1&rbrace; online documentatie van Microsoft Office [&#x200B; voor instructies op hoe te om een Manifest dossier van Excel te installeren niet van de Opslag van Microsoft wordt gediend.](https://learn.microsoft.com/en-us/office/dev/add-ins/publish/publish)

Nadat u de Report Builder Add-in hebt geïnstalleerd, wordt het Report Builder-pictogram weergegeven in het [!DNL Excel] -lint onder het tabblad Start.

![&#x200B; het pictogram van Report Builder in Excel &#x200B;](/help/analyze/report-builder/assets/rb_app_icon.png)

## Aanmelden bij Report Builder

Nadat u de Report Builder for Excel Add-in voor uw werkend platform of browser hebt geïnstalleerd, volg deze stappen om zich aan te melden bij Report Builder.

1. Open een werkboek van Excel.

1. Klik op het Report Builder-pictogram om Report Builder te starten.

1. Klik op de werkbalk Adobe Report Builder op **[!UICONTROL Login]** .

   ![&#x200B; klik de login van Report Builder knoop.](/help/analyze/report-builder/assets/rb_login.png)

1. Voer je Adobe Experience ID-accountgegevens in. Je accountgegevens moeten overeenkomen met je Adobe Analytics-gegevens.

   ![&#x200B; Uw login pictogram en organisatie.](/help/analyze/report-builder/assets/image4.png)

Nadat u zich hebt aangemeld, worden het aanmeldingspictogram en de organisatie boven in het deelvenster weergegeven

## Organisaties wisselen

Wanneer u zich voor het eerst aanmeldt, wordt u aangemeld bij de standaardorganisatie die aan uw profiel is toegewezen.

1. Klik op de naam van de organisatie die wordt weergegeven wanneer u zich aanmeldt.

1. Selecteer een organisatie in de lijst met beschikbare organisaties. Alleen organisaties waartoe u toegang hebt, worden vermeld.

   ![&#x200B; de lijst van organisaties die u kunt toegang hebben.](/help/analyze/report-builder/assets/image5.png)

## Afmelden

U kunt zich vanuit Report Builder afmelden vanuit het gebruikersprofiel.

1. Wijzigingen in geopende werkboeken opslaan.

1. Klik op het pictogram van de avatar om het gebruikersprofiel weer te geven.

   ![&#x200B; Uw avatar van het gebruikersprofiel en de knoop van het Teken uit.](/help/analyze/report-builder/assets/image6.png)

1. Klik **Teken uit**.
