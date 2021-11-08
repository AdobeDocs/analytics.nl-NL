---
description: Gegevens die worden verzameld op websites, mobiele apps of die worden geüpload met behulp van webservice-API's of gegevensbronnen, worden verwerkt en opgeslagen in Adobe Data Warehouse. Deze onbewerkte klikstreamgegevens vormen de gegevensset die door Adobe Analytics wordt gebruikt.
keywords: clickStream;data feed;datafeed;Data Feed
title: Overzicht van gegevensinvoer voor analyse
uuid: 6bdbe90c-e6ed-4bb0-b5be-24fd795adde4
exl-id: 2cfff9ad-cdb5-4ae9-a266-4f3d3d046f0c
source-git-commit: 505995973beb2dab1ac2aa4521210b650e3a6988
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 5%

---

# Overzicht van gegevensinvoer voor analyse

Gegevensfeeds zijn een krachtige manier om onbewerkte gegevens uit Adobe Analytics te halen. Deze onbewerkte gegevens kunnen worden gebruikt op andere platformen buiten de Adobe om naar eigen goeddunken van uw organisatie te worden gebruikt. De gegevens worden aan het einde van elk uur in partijen per uur of aan het einde van elke dag in partijen per uur verstrekt.

## Vereisten

Zorg ervoor dat u aan alle volgende vereisten voldoet voordat u gegevensfeeds gebruikt.

* Houd een FTP-site en aanmeldingsgegevens bij de hand. Gegevensfeeds kunnen alleen naar een serverdoel worden verzonden. Uw organisatie biedt doorgaans FTP-referenties. Adobe kan een FTP-locatie op uw verzoek een bescheiden hoeveelheid opslagruimte bieden. Neem contact op met de klantenservice om een FTP-bestemming aan te vragen voor gegevensfeeds.
* Een werkende implementatie die gegevens naar de servers van de Adobe- gegevensinzameling verzendt. Zie [Een implementatie valideren en publiceren](/help/implement/launch/validate-publish-prod.md) in de gebruikershandleiding Implementeren.
* Uw account is een productbeheerder voor Analytics of uw account behoort tot een productprofiel met toegang tot gegevensfeeds.

## Aan de slag

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
2. Klik op het pictogram met 9 vierkantjes rechtsboven in het venster en klik vervolgens op het gekleurde Analytics-logo.
3. Navigeer in de bovenste navigatiebalk naar Beheer > Gegevensfeeds.
4. Klik op [!UICONTROL Add]. Er wordt een nieuwe pagina weergegeven met drie hoofdcategorieën: [!UICONTROL Feed information], [!UICONTROL Destination], en [!UICONTROL Data Column Definitions].
5. Uitvullen [!UICONTROL Feed Information] velden.
   * Naam: Elke gewenste naam, zoals &quot;Gegevensinvoer testen&quot;.
   * Rapportsuite: Selecteer de gewenste rapportsuite.
   * E-mail indien voltooid: Voer uw e-mail in.
   * Diervoederinterval: Selecteer het gewenste interval (per uur of per dag).
   * Vertraging bij verwerking: Kan worden gelaten zoals [!UICONTROL No Delay].
   * Begin- en einddatum: Selecteer een begindatum van enkele dagen geleden en vandaag als einddatum.
6. Uitvullen [!UICONTROL Destination] velden.
   * Type: FTP
   * Host: Voer de gewenste FTP-doel-URL in. Bijvoorbeeld, `ftp://ftp.omniture.com`.
   * Pad: Kan leeg blijven
   * Gebruikersnaam: Voer de gebruikersnaam in die u wilt aanmelden bij de FTP-site.
   * Wachtwoord en wachtwoord bevestigen: Voer het wachtwoord in om u aan te melden bij de FTP-site.
7. Uitvullen [!UICONTROL Data Column Definitions].
   * Selecteer de meest recente sjabloon &#39;All Adobe Columns&#39; in de vervolgkeuzelijst.
   * Compressie-indeling: Gzip
   * Type verpakking: Meerdere bestanden
   * Manifest: Geen bestand
8. Klikken [!UICONTROL Save] in de rechterbovenhoek.
9. Als de gegevens eenmaal zijn opgeslagen, worden historische gegevens verwerkt. Wanneer de gegevens een dag lang zijn verwerkt, wordt het bestand op de FTP-site geplaatst.
10. Meld u aan bij de FTP-site met Windows Verkenner of een toegewezen FTP-client.
11. Download het gecomprimeerde gegevensbestand naar uw lokale computer.
12. Het gecomprimeerde bestand decomprimeren met een programma dat ondersteuning biedt `.tar.gz` bestandsextensies.
13. Open de `hit_data.tsv` in uw spreadsheet of databasetoepassing van keuze om onbewerkte gegevens voor die dag weer te geven.

## Volgende stappen

Zodra u het basiswerkschema begrijpt van het verkrijgen van gegevensvoer, kunt u met teams binnen uw organisatie werken om ruwe gegevens in een gegevensbestand op te slaan of in te voeren.

* [Een gegevensfeed maken](create-feed.md): Technische details voor het maken van een gegevensfeed, waarbij afzonderlijke velden gedetailleerder worden uitgelegd
* [Gegevensfeeds beheren](df-manage-feeds.md): Meer informatie over navigeren in de interface voor gegevensinvoer
* [Inhoud gegevensfeed](c-df-contents/datafeeds-contents.md): Begrijp wat binnen het samengeperste dossier is
* [Definities gegevenskolom](c-df-contents/datafeeds-reference.md): Een uitgebreide lijst van alle beschikbare kolommen

## Aanvullende bronnen

Video navigating the data feed interface:

>[!VIDEO](https://video.tv.adobe.com/v/25452/?quality=12)

Video over het zoeken naar de id van uw gegevensfeed:

>[!VIDEO](https://video.tv.adobe.com/v/335747/?quality=12)
