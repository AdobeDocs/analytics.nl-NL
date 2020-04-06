---
description: Gegevens die zijn verzameld op websites, mobiele apps of die zijn geüpload met API's of gegevensbronnen van webservices, worden verwerkt en opgeslagen in het Data Warehouse van Adobe. Deze onbewerkte klikstreamgegevens vormen de gegevensset die wordt gebruikt door Adobe Analytics.
keywords: clickstream;data feed;datafeed;Data Feed
title: Overzicht van gegevensinvoer voor analyse
uuid: 6bdbe90c-e6ed-4bb0-b5be-24fd795adde4
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Overzicht van gegevensinvoer voor analyse

Gegevensfeeds zijn een krachtige manier om onbewerkte gegevens uit Adobe Analytics te halen. Deze onbewerkte gegevens kunnen op andere platforms buiten Adobe worden gebruikt, zodat u ze naar eigen goeddunken van uw organisatie kunt gebruiken. De gegevens worden aan het einde van elk uur in partijen per uur of aan het einde van elke dag in partijen per uur verstrekt.

## Vereisten

Zorg ervoor dat u aan alle volgende vereisten voldoet voordat u gegevensfeeds gebruikt.

* Houd een FTP-site en aanmeldingsgegevens bij de hand. Gegevensfeeds kunnen alleen naar een serverdoel worden verzonden. Uw organisatie biedt doorgaans FTP-referenties. Adobe kan een FTP-locatie op uw verzoek een bescheiden hoeveelheid opslagruimte bieden. Neem contact op met de klantenservice om een FTP-bestemming aan te vragen voor gegevensfeeds.
* Een werkende implementatie die gegevens naar de servers van de gegevensinzameling van Adobe verzendt. Zie Een implementatie [valideren en publiceren in Launch](/help/implement/launch/validate-publish-prod.md) in de gebruikershandleiding Implementeren.
* Uw account is een productbeheerder voor Analytics of uw account behoort tot een productprofiel met toegang tot gegevensfeeds.

## Aan de slag

1. Meld u met uw Adobe-id aan bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com) .
2. Klik op het pictogram van 9 vierkante pixels rechtsboven en klik vervolgens op het gekleurde Analytics-logo.
3. Navigeer in de bovenste navigatiebalk naar Beheer > Gegevensfeeds.
4. Klik op [!UICONTROL Add]. Er wordt een nieuwe pagina weergegeven met drie hoofdcategorieën: [!UICONTROL Feed information], [!UICONTROL Destination], en [!UICONTROL Data Column Definitions].
5. Vul [!UICONTROL Feed Information] velden in.
   * Naam: Elke gewenste naam, zoals &quot;Gegevensinvoer testen&quot;.
   * Rapportsuite: Selecteer de gewenste rapportsuite.
   * E-mail indien voltooid: Voer uw e-mail in.
   * Diervoederinterval: Selecteer het gewenste interval (per uur of per dag).
   * Vertraging bij verwerking: Kan zo blijven [!UICONTROL No Delay].
   * Begin- en einddatum: Selecteer een begindatum van enkele dagen geleden en vandaag als einddatum.
6. Vul [!UICONTROL Destination] velden in.
   * Type: FTP
   * Host: Voer de gewenste FTP-doel-URL in. Bijvoorbeeld, `ftp://ftp.omniture.com`.
   * Pad: Kan leeg blijven
   * Gebruikersnaam: Voer de gebruikersnaam in die u wilt aanmelden bij de FTP-site.
   * Wachtwoord en wachtwoord bevestigen: Voer het wachtwoord in om u aan te melden bij de FTP-site.
7. Vul het veld in [!UICONTROL Data Column Definitions].
   * Selecteer de meest recente sjabloon &#39;Alle Adobe-kolommen&#39; in het vervolgkeuzemenu.
   * Compressie-indeling: Gzip
   * Type verpakking: Meerdere bestanden
   * Manifest: Geen bestand
8. Klik [!UICONTROL Save] in de rechterbovenhoek.
9. Als de gegevens eenmaal zijn opgeslagen, worden historische gegevens verwerkt. Wanneer de gegevens een dag lang zijn verwerkt, wordt het bestand op de FTP-site geplaatst.
10. Meld u aan bij de FTP-site met Windows Verkenner of een toegewezen FTP-client.
11. Download het gecomprimeerde gegevensbestand naar uw lokale computer.
12. Pak het gecomprimeerde bestand uit met een programma dat `.tar.gz` bestandsextensies ondersteunt.
13. Open het `hit_data.tsv` bestand in de spreadsheet of de databasetoepassing van keuze om de onbewerkte gegevens voor die dag weer te geven.

## Volgende stappen

Zodra u het basiswerkschema begrijpt van het verkrijgen van gegevensvoer, kunt u met teams binnen uw organisatie werken om ruwe gegevens in een gegevensbestand op te slaan of in te voeren.

* [Een gegevensfeed](create-feed.md)maken: Technische details voor het maken van een gegevensfeed, waarbij afzonderlijke velden gedetailleerder worden uitgelegd
* [Gegevensfeeds](df-manage-feeds.md)beheren: Meer informatie over navigeren in de interface voor gegevensinvoer
* [Inhoud](c-df-contents/datafeeds-contents.md)van gegevenfeed: Begrijp wat binnen het samengeperste dossier is
* [Definities](c-df-contents/datafeeds-reference.md)gegevenskolom: Een uitgebreide lijst van alle beschikbare kolommen

## Aanvullende bronnen

Video navigating the data feed interface:

>[!VIDEO](https://www.youtube.com/watch?v=m_fb--gNtR4)
