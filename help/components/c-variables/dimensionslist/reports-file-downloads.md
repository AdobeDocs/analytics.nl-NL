---
description: Met Bestandsdownloads krijgt u inzicht hoe vaak uw bezoekers bestanden downloaden van uw site. Voorbeelden van bestandsdownloads zijn bijvoorbeeld tekstverwerkingsdocumenten, spreadsheets, audiobestanden, filmbestanden, gebruikershandleidingen, enzovoort. Dit geldt zowel voor bestanden die rechtstreeks vanuit de browser worden opgeslagen en geopend, als voor bestanden die op de computer van de gebruiker zijn opgeslagen. Het rapport bevat de naam van het bestand dat wordt gedownload, inclusief de volledige URL die nodig is voor toegang tot het bestand.
title: Bestanden downloaden
topic: Reports
uuid: 897fc221-aa30-4eac-aca6-bccb76adaf71
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Bestanden downloaden

Met Bestandsdownloads krijgt u inzicht hoe vaak uw bezoekers bestanden downloaden van uw site. Voorbeelden van bestandsdownloads zijn bijvoorbeeld tekstverwerkingsdocumenten, spreadsheets, audiobestanden, filmbestanden, gebruikershandleidingen, enzovoort. Dit geldt zowel voor bestanden die rechtstreeks vanuit de browser worden opgeslagen en geopend, als voor bestanden die op de computer van de gebruiker zijn opgeslagen. Het rapport bevat de naam van het bestand dat wordt gedownload, inclusief de volledige URL die nodig is voor toegang tot het bestand.

**Navigatie**

**[!UICONTROL Reports]** > **[!UICONTROL Site Content]** > **[!UICONTROL Links]** > **[!UICONTROL File Downloads]**

Als dit rapport niet beschikbaar is op de standaardlocatie, vraagt u dit na bij uw beheerders, die de standaardmenustructuur hebben gewijzigd om beter te voldoen aan de unieke behoeften van uw organisatie.

Gebruik dit rapport om:

* Bepaal de bestanden die het vaakst van uw site worden gedownload.
* Begrijp als bepaalde dossiers vaker tijdens specifieke tijdsperioden worden gedownload.
* Controleer of alle indelingen voor een bepaald document vereist zijn.

   U vertaalt momenteel bijvoorbeeld uw gebruikershandleidingen in twaalf talen en maakt deze beschikbaar via uw website. Met het rapporteren van bestandsdownloads kunt u weten hoe vaak elke handmatige versie wordt gedownload en kunt u de waarde beoordelen van het blijven vertalen van de gebruikershandleiding in alle twaalf talen.

**Problemen oplossen**

Marketingsrapporten bevatten informatie over bestanden die zijn gedownload van een pagina van uw site die JavaScript-code bevat. Bepaalde variabelen moeten echter wel aanwezig zijn en correct zijn ingesteld, zodat gegevens over het downloaden van bestanden kunnen worden gerapporteerd. Als in dit rapport geen gegevens worden weergegeven of als de verwachte waarden niet worden weergegeven, volgt u de onderstaande stappen om uw implementatie te valideren.

1. Zoek op uw site het algemene JavaScript-bestand. Dit wordt vaak genoemd [!DNL s_code.js], maar kan anders genoemd zijn. Als de naam van de JavaScript-code is gewijzigd, kunt u de JavaScript-bestanden op uw site zoeken naar de waarde *`s.account`*, die deel uitmaakt van de JavaScript-code.

1. Zoek in het bestand de variabele [s.trackDownloadLinks](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_trackdownllinks.html) . Zorg ervoor dat deze is ingesteld op *true*

1. Zoek de variabele [s.linkDownloadFileTypes](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_linkdownfiletypes.html) . Controleer of alle gewenste bestandsextensies in deze lijst voorkomen. Voeg zo nodig ontbrekende extensies toe, zoals [!DNL .zip], [!DNL .pdf]enzovoort.)

Als deze variabelen correct lijken te zijn geconfigureerd, maar de gegevens [!UICONTROL File Downloads Report] nog steeds niet worden ontvangen, moeten de ondersteunde gebruikers van uw organisatie contact opnemen met de klantenservice.
