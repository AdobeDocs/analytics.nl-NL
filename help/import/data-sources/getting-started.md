---
title: Aan de slag met gegevensbronnen
description: Upload voorbeeldgegevens naar een ontwikkelrapport-suite.
exl-id: d9f74f55-abbb-4ceb-b4db-8d3c32aacd4a
feature: Data Sources
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

---

# Aan de slag met gegevensbronnen

U kunt deze stappen volgen om steekproefgegevens in een reeks van het ontwikkelingsrapport gemakkelijk te uploaden om het werkschema in actie te zien. Zodra u het proces begrijpt, kunt u het uitbreiden en aanpassen specifiek aan de implementatie van uw organisatie.

>[!IMPORTANT]
>
>Voer de volgende stappen uit met behulp van een ontwikkelings- of testrapportsuite. Gegevens die via gegevensbronnen zijn geüpload, zijn **permanent**. Het beïnvloedt de gegevens van het productierapport als geupload daar.

1. Aanmelden bij Adobe Analytics via [https://experience.adobe.com](https://experience.adobe.com).
1. Ga naar **[!UICONTROL Admin]** > **[!UICONTROL All Admin]** > **[!UICONTROL Data sources]**.
1. Selecteer een reeks van het ontwikkelingsrapport gebruikend de drop-down lijst in het hoogste recht.
1. Klik op de knop **[!UICONTROL Create]** linksboven.
1. Onder [!UICONTROL Select Category]kiest u &quot;[!UICONTROL Generic]&quot;, en onder [!UICONTROL Select Type]kiest u &quot;[!UICONTROL Generic Data Source (Summary Data Only)]&quot;.
1. Klik op **[!UICONTROL Activate]**. Er wordt een pop-upvenster geopend waarin de [!UICONTROL Data Source Activation Wizard].
   1. Stap 1: Geef de gegevensbron een naam en klik op het selectievakje voor disclaimer.
   1. Stap 2: Deze stap werd meer gebruikt in eerdere versies van Adobe Analytics. Klik op een selectievakje en typ vervolgens een waarde in het tekstveld ernaast.
   1. Stap 3: Kies metrisch om in uw dossier van het gegevensbronmalplaatje te omvatten. Selecteer &quot;Gebeurtenis 1&quot; in de vervolgkeuzelijst.
   1. Stap 4: Deze stap werd meer gebruikt in eerdere versies van Adobe Analytics. Klik op een selectievakje en typ vervolgens een waarde in het tekstveld ernaast.
   1. Stap 5: Kies de dimensie die u in het sjabloonbestand voor de gegevensbron wilt opnemen. Selecteer &quot;eVar1&quot;van de drop-down lijst.
   1. Stap 6: Bekijk het overzicht en geef de afmetingen en maatstaven weer die in het sjabloonbestand zijn opgenomen.
   1. Stap 7: Klik op de knop **[!UICONTROL Download]** om het sjabloonbestand met gegevensbronnen te downloaden. Noteer ook de aanmeldingsgegevens voor de FTP-site, aangezien deze binnenkort worden gebruikt.
1. De gegevensbron wordt nu gemaakt; de volgende stap is om het gegevens te verstrekken aan proces. Open het gedownloade bestand in de gewenste teksteditor.
1. Het sjabloonbestand bevat drie regels. twee regels voor opmerkingen (beginnend met &quot;`#`&quot;) en een koptekstrij:

   ```text
   # Generic Data Source (Summary Data Only) template file (user: 123456789 ds_id: 2)
   #    eVar1    event1
   Date    Evar 1    Event 1
   ```

1. Voer de gegevens in verschillende rijen in, waarbij elk item door een tab wordt gescheiden. Gebruik geen spaties of komma&#39;s om waarden van elkaar te scheiden.
   * De eerste kolom is de datum in de volgende notatie: `MM/DD/YYYY/HH/mm/SS`.
   * De tweede kolom is de tekstwaarde die u in eVar1 wilt opnemen.
   * De derde kolom is het bedrag dat u gebeurtenis 1 wilt verhogen.

   ```text
   # Generic Data Source (Summary Data Only) template file (user: 123456789 ds_id: 5)
   #    eVar1    event1
   Date    Evar 1    Event 1
   09/07/YYYY/11/23/00    Data source example value    3
   09/07/YYYY/15/59/00    Another data source value    18
   ```

1. Sla het bestand op. U kunt desgewenst een andere bestandsnaam opgeven. Nadat het bestand is opgeslagen, kunt u de teksteditor sluiten.
1. Navigeer in Windows Verkenner, de Finder of de FTP-client van uw keuze naar [ftp://ftp.omniture.com](ftp://ftp.omniture.com).
1. Wanneer ertoe aangezet voor login geloofsbrieven, gebruik de gebruikersbenaming en het wachtwoord in de laatste stap van de tovenaar van de gegevensbronverwezenlijking wordt verstrekt. U kunt er nogmaals naar verwijzen door naar [!UICONTROL Data sources] en klikken **[!UICONTROL FTP Info]** naast de gegevensbron die u hebt gemaakt.
1. Als u de verificatie hebt voltooid, sleept u het bewerkte bestand naar het geverifieerde FTP-venster.
1. Maak een leeg tekstbestand op een willekeurige locatie buiten het FTP-venster. Geef deze dezelfde bestandsnaam als het gegevensbronbestand dat u naar de FTP-site hebt geüpload, met één uitzondering. In plaats van een `.txt` bestandstype, geef deze een `.fin` bestandstype. Controleer of u de bestandstypen kunt zien en wijzigen met de instellingen van het besturingssysteem.
1. Sleep de lege `.fin` naar dezelfde FTP-locatie als het gegevensbronbestand. De aanwezigheid van de `.fin` Het bestand vertelt Adobe dat het gegevensbronbestand volledig is geüpload en klaar is om te worden opgenomen.
1. Na enkele minuten verdwijnt het bestand van de FTP-locatie en is het zichtbaar in de rapportage.
1. Vernieuw de pagina Gegevensbronnen en bevestig dat het dossier met succes werd opgenomen.
1. Navigeer naar Analysis Workspace en maak een project.
1. Sleep eVar1 als een afmeting aan het werkruimtekanvas, en gebeurtenis 1 als metrisch. Zorg ervoor dat het datumbereik van de werkruimte de datums bevat die u in de gegevensbron hebt opgegeven.

   ![Voorbeeldrapport](assets/success-report.png)

## Volgende stappen

[Bestandsindeling](file-format.md): Leer de details rond het creëren van een dossier van gegevensbronnen dat aan uw organisatie wordt aangepast.
