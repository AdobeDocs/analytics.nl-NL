---
title: Schema voor classificatieset
description: Leer om het schema voor een individuele classificatieset te bekijken en uit te geven.
exl-id: 4a7c5bfe-ff2b-4380-af46-435801d73c1e
feature: Classifications
source-git-commit: e89d67d60313867a18b4d2a1e4e7a0e7da5dc31a
workflow-type: tm+mt
source-wordcount: '1385'
ht-degree: 1%

---

# Schema voor classificatieset

Het schema is de lijst met classificaties die u wilt toepassen op de belangrijkste dimensies die u voor de classificatieset hebt gedefinieerd. Als u bijvoorbeeld het product hebt gedefinieerd als de belangrijkste dimensie en dit veld een product-SKU bevat, gebruikt u het schema om classificaties toe te voegen zoals productnaam, productkleur, productgrootte en meer.

Het schema voor een classificatieset bewerken:


1. Selecteer **[!UICONTROL Components]** in de bovenste menubalk van Adobe Analytics en selecteer vervolgens **[!UICONTROL Classification sets]** .
1. Selecteer in **[!UICONTROL Classification Sets]** de tab **[!UICONTROL Classification Sets]** .
1. Selecteer in Beheer **[!UICONTROL Classifications Sets]** de classificatieset waarvoor u het schema wilt bewerken.
1. In de **[!UICONTROL Classification Set: _dialoog van de classificatiereeks naam_]**, selecteer het **[!UICONTROL Schema]** lusje. Dat tabblad bestaat uit de volgende interface-elementen:

   ![&#x200B; de reeksen van de Classificatie - schema &#x200B;](assets/classification-sets-schema.png)

   * [Classificatielijst](#classification-list)
   * [Zoeken](#search)
   * [Acties](#actions)
   * [Actiebalk](#action-bar)

## Classificatielijst

De lijst van classificaties heeft de volgende kolommen:

| Kolom | Beschrijving |
|---|---|
| **[!UICONTROL Classification Name]** | De naam die u hebt opgegeven voor de classificatie. |
| **[!UICONTROL Identity Name]** | De afgeleide naam door het systeem voor de classificatie. Deze naam is een alleen-lezen waarde en u kunt de naam Identiteit gebruiken |
| **[!UICONTROL Classified By]** | Indien gebruikt, een verbinding aan de reeks van raadplegingsclassificatie die wordt gebruikt om deze classificatie te classificeren. |


## Zoeken

U kunt ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg) voor één of meerdere classificaties snel zoeken. Gebruik ![&#x200B; CrossSize100 &#x200B;](/help/assets/icons/CrossSize100.svg) om het onderzoek te ontruimen.

## Acties

De volgende acties zijn beschikbaar als knoppen boven aan de classificatielijst:

| Pictogram | Actie | Beschrijving |
|---|---|---|
| ![&#x200B; voeg toe &#x200B;](/help/assets/icons/Add.svg) | **[!UICONTROL Add]** | [&#x200B; voeg een classificatie &#x200B;](#add) aan de lijst toe. |
| ![&#x200B; UploadToCloud &#x200B;](/help/assets/icons/UploadToCloud.svg) | **[!UICONTROL Upload]** | [&#x200B; upload een JSON, CSV, TSV, of dossier van het LUSJE &#x200B;](#upload). |
| ![Download](/help/assets/icons/Download.svg) | **[!UICONTROL Download]** | [&#x200B; de classificatiegegevens van de Download &#x200B;](#download). |
| ![&#x200B; DocumentFragment &#x200B;](/help/assets/icons/DocumentFragment.svg) | **[!UICONTROL Template]** | [&#x200B; Download een malplaatje &#x200B;](#template) voor classificatiegegevens. |
| ![&#x200B; Geschiedenis &#x200B;](/help/assets/icons/History.svg) | **[!UICONTROL Job History]** | Toon de [&#x200B; manager van de classificatiereeks &#x200B;](/help/components/classifications/sets/job-manager.md), voor de geselecteerde classificatiereeks wordt gefiltreerd. |
| ![&#x200B; Vistuig &#x200B;](/help/assets/icons/Gear.svg) | **[!UICONTROL Automate]** | [&#x200B; automatiseer de opname van classificatiegegevens &#x200B;](#automate) door het gebruik van een wolkenplaats. |


### Toevoegen

Om een nieuwe classificatie toe te voegen, voegt de uitgezochte ![&#x200B; &#x200B;](/help/assets/icons/Add.svg) toe **[!UICONTROL Add]**.

![&#x200B; de reeksen van de Classificatie - voeg classificatie aan schema &#x200B;](assets/classification-sets-schema-add-classification.png) toe

In de **[!UICONTROL Add a new classification for _dialoog van de classificatiereeks naam_]**, ga **[!UICONTROL Classification Name]** in en selecteer **[!UICONTROL Add]**. De classificatie wordt toegevoegd aan de lijst.



### Uploaden

Om classificatiegegevens in het schema voor een classificatie in te voeren, uitgezochte ![&#x200B; UploadToCloud &#x200B;](/help/assets/icons/UploadToCloud.svg) **[!UICONTROL Upload]**.


![&#x200B; de reeksen van de Classificatie - het Schema uploadt een dossier &#x200B;](assets/classification-sets-schema-upload-file.png)

1. In het dialoogvenster **[!UICONTROL Add new classifications]** :

   * Sleep een bestand dat classificatiegegevens bevat en zet het bestand neer op **[!UICONTROL Drag and drop here]** .
   * Selecteer **[!UICONTROL Browse]** en kies een bestand van uw computer of netwerk.

   U ziet een **[!UICONTROL Schema Preview]** van de inhoud van het bestand. In de voorvertoning worden de kolommen met gegevens uit het bestand weergegeven. Om een kolom te resize, selecteer ![&#x200B; ChevronDownSize300 &#x200B;](/help/assets/icons2/ChevronDownSize300.svg) en selecteer **[!UICONTROL Resize column]**. Er wordt een greep weergegeven waarmee u het formaat van de kolom kunt wijzigen.

   Wanneer geen classificatie in de classificatiereeks voor een kolom wordt bepaald, wordt een alarm ![&#x200B; Alarm &#x200B;](/help/assets/icons/Alert.svg) getoond. In de waarschuwing wordt uitgelegd dat een classificatie niet aanwezig is in de bestaande set classificatieschema&#39;s en bij importeren wordt gemaakt.

1. Selecteer **[!UICONTROL Overwrite data on conflict?]** als u de huidige classificatiegegevens wilt overschrijven met het nieuwe geïmporteerde bestand. Bijvoorbeeld:

   | | Sleutel | Huidige productkleur | Bestand importeren | Nieuwe productkleur |
   |---|---|---|---|---|
   | ![&#x200B; SelectBox &#x200B;](/help/assets/icons/SelectBox.svg) **[!UICONTROL Overwrite data on conflict?]** | 1234 | groen | blauw | blauw |
   | ![&#x200B; Vierkant &#x200B;](/help/assets/icons2/Square.svg) **[!UICONTROL Overwrite data on conflict?]** | 1234 | groen | blauw | groen |

1. Selecteer **[!UICONTROL Apply]** . Er wordt een waarschuwing weergegeven als kolommen niet aanwezig zijn als classificaties in de bestaande schemaset. Deze kolommen worden toegevoegd als nieuwe classificaties wanneer u het uploaden bevestigt.

   ![&#x200B; Reeks van de Classificatie - upload classificatiealarm &#x200B;](assets/classification-sets-schema-upload-file-preview-alert.png)

   Selecteer **[!UICONTROL Confirm Upload]** om het uploaden te bevestigen. Selecteer **[!UICONTROL Cancel Upload]** om het uploaden te annuleren.


### Downloaden

Om classificatiegegevens te downloaden, uitgezochte ![&#x200B; Download &#x200B;](/help/assets/icons/Download.svg) **[!UICONTROL Download]**.

![&#x200B; de reeksen van de Classificatie - de gegevens van de de downloadclassificatie van het Schema &#x200B;](assets/classification-sets-schema-download-file.png)

In de **[!UICONTROL Download data for _dialoog van de classificatiereeks naam_]**:

1. Voer het aantal **[!UICONTROL Rows]** in dat u wilt downloaden. Bijvoorbeeld: `10000` .
1. Als u de periode wilt selecteren waarvoor u rijen met classificatiegegevens wilt downloaden, voert u een begin- en eindgegevens in voor **[!UICONTROL Download Rows Received Between]** . Of gebruik ![&#x200B; Kalender &#x200B;](/help/assets/icons/Calendar.svg) om een kalenderpopup te gebruiken om de periode te selecteren.
1. Selecteer een optie in **[!UICONTROL Data Returned]** om te selecteren welke gegevens u wilt retourneren.

   * **[!UICONTROL All values]** retourneert alle waarden voor de huidige classificatiegegevens.
   * **[!UICONTROL Any columns empty]** retourneert een kolom met sleutelwaarden voor de bestaande classificatiegegevens. En kolommen zonder waarde voor classificatiegegevens waarvoor geen waarden bestaan.
   * **[!UICONTROL All columns empty]** retourneert een sleutelkolom met waarden voor de bestaande classificatiegegevens. En kolommen zonder waarde voor classificatiegegevens.
1. Om het [&#x200B; dossierformaat &#x200B;](/help/components/classifications/sets/data-files.md#general-file-requirements) van de gedownloade classificatiegegevens te selecteren, selecteer een optie van het **[!UICONTROL File Format]** drop-down menu. De opties zijn:

   * **[!UICONTROL JSON]**.
   * **[!UICONTROL Comma separated values]** (CSV).
   * **[!UICONTROL Excel tab separated values]** (TSV of TAB).

1. Om het [&#x200B; dossier te selecteren coderend &#x200B;](/help/components/classifications/sets/data-files.md#general-file-requirements) aan wanneer het dossier wordt gedownload, selecteer een optie van het dossier-Coderen drop-down menu. De opties zijn:

   * **[!UICONTROL UTF-8]**.
   * **[!UICONTROL Latin-1]**.


1. Selecteer **[!UICONTROL Download]** om de classificatiegegevens te downloaden. U kunt het gedownloade dossier in de standaarddownloadfolder van uw browser vinden, en het dossier is genoemd <code><i> Reeks van de Classificatie </i>.<i> json </i>|<i> csv </i>|<i> tsv </i></code>. Als het dossier reeds bestaat, een opeenvolgingsaantal <code> (<i> x </i>)</code> wordt toegevoegd aan de bestandsnaam.<br/> als u opties hebt gespecificeerd die geen gegevens terugkeren, ziet u een **[!UICONTROL Notice]** dialoog om u te informeren om de opties voor datumwaaier en teruggekeerde gegevens te veranderen.


### Sjabloon

Om een malplaatje voor classificatiegegevens te downloaden, selecteer ![&#x200B; DocumentFragment &#x200B;](/help/assets/icons/DocumentFragment.svg) **[!UICONTROL Template]**.

![&#x200B; de reeksen van de Classificatie schema - het malplaatje van de Download &#x200B;](assets/classification-sets-schema-download-template.png)

In de **[!UICONTROL Download template for _dialoog van de classificatiereeks naam_]**:

1. Om het [&#x200B; dossierformaat &#x200B;](/help/components/classifications/sets/data-files.md#general-file-requirements) van de gedownloade classificatiegegevens te selecteren, selecteer een optie van het **[!UICONTROL File Format]** drop-down menu. De opties zijn:

   * **[!UICONTROL Comma separated values]**.
   * **[!UICONTROL Excel tab separated values]**.

1. Om het [&#x200B; dossier te selecteren coderend &#x200B;](/help/components/classifications/sets/data-files.md#general-file-requirements) aan wanneer het dossier wordt gedownload, selecteer een optie van het dossier-Coderen drop-down menu. De opties zijn:

   * **[!UICONTROL UTF-8]**.
   * **[!UICONTROL Latin-1]**.

1. Selecteer **[!UICONTROL Download]** om de sjabloon voor classificatiegegevens te downloaden. U kunt het gedownloade dossier in de standaarddownloadfolder van uw browser vinden, en is genoemd <code><i> Vastgestelde Indeling van de Classificatie </i>.<i> csv </i>|<i> tsv </i></code>. Als het dossier reeds bestaat, een opeenvolgingsaantal <code> (<i> x </i>)</code> wordt toegevoegd aan de bestandsnaam.


### Automatisch {#automate}


>[!CONTEXTUALHELP]
>id="classificationsets_schema_automate_locationaccount"
>title="Locatieaccount"
>abstract="Lijst met locatierekeningen van accounttypen die de invoer van classificatiegegevens ondersteunen. Selecteer **[!UICONTROL New account]** om een nieuw locatieaccount te maken."
>additional-url="https://experienceleague.adobe.com/docs/analytics/components/locations/configure-import-accounts.html?lang=nl-NL" text="Cloud-import- en exportaccounts configureren"


>[!CONTEXTUALHELP]
>id="classificationsets_schema_automate_location"
>title="Locatie"
>abstract="Lijst met locaties op een geselecteerde locatie die het importeren van classificatiegegevens ondersteunen. Selecteer **[!UICONTROL New location]** om een nieuwe locatie te maken."
>additional-url="https://experienceleague.adobe.com/docs/analytics/components/locations/configure-import-locations.html?lang=nl-NL" text="Locaties voor het importeren en exporteren van cloud configureren"

U kunt de opname van classificatiegegevens automatiseren via de configuratie en het gebruik van cloudaccount en cloudlocaties.



>[!IMPORTANT]
>De automatisering van classificatieopname van wolkenrekeningen vereist dat u (of uw netwerkbeheerder) IP adreswaaiers specificeert om toe te staan om gegevens in uw netwerk in te voeren. Vorm één of meerdere IP adreswaaiers afhankelijk van de plaats van datacenters van de Analyse die u gebruikt.
>
>| Locatie van datacenter analyseren | Voeg deze IP adreswaaier aan een lijst van gewenste personen in uw netwerk toe |
>|---|---:|
>| Pacific North West | `52.254.104.0/22` |
>| Londen | `51.138.16.0/22` |
>| Singapore | `20.40.0.0/14 ` |
>

Om de opname van classificatie te automatiseren, uitgezochte ![&#x200B; Vistuig &#x200B;](/help/assets/icons/Gear.svg) **[!UICONTROL Automate]**.

![&#x200B; de reeksen van de Classificatie schema - automatiseren &#x200B;](assets/classification-sets-schema-automate.png)

In de **[!UICONTROL Associate / Update Ingest Location for _dialoog van de classificatiereeks naam_]**:

1. Selecteer een optie in **[!UICONTROL Location Account]** om een locatie in de cloud te selecteren. Slechts [&#x200B; plaatsrekeningen van gesteunde rekeningstypes die de invoer van classificatiegegevens &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/components/locations/configure-import-accounts) toestaan worden getoond. Selecteer **[!UICONTROL New account]** als u een nieuwe account wilt maken.
1. Als u een locatie wilt selecteren, selecteert u een optie in **[!UICONTROL Location]** . Alleen de locaties van geselecteerde accounttypen voor het importeren van classificatiegegevens worden weergegeven. Selecteer **[!UICONTROL New location]** als u een nieuwe locatie wilt maken.

   >[!IMPORTANT]
   >
   >De locatie die u maakt of selecteert, moet een **[!UICONTROL Prefix]** (map) in **[!UICONTROL Bucket]** bevatten die als host fungeert voor de bestanden met classificatiegegevens. Bijvoorbeeld een map met de naam `files` . Het hosten van dossiers bij de wortel van een emmertje werkt niet met de meeste wolkenplaatsen.
   >

1. Als u een scheidingsteken wilt selecteren, selecteert u een optie in de vervolgkeuzelijst **[!UICONTROL List delimiter]** . De opties zijn:
   * **[!UICONTROL Comma ,]**
   * **[!UICONTROL Semicolon ;]**
   * **[!UICONTROL Colon :]**
   * **[!UICONTROL Vertical bar |]**
   * **[!UICONTROL Space]**
   * **[!UICONTROL Tab]**
1. Om het [&#x200B; dossier te selecteren die &#x200B;](/help/components/classifications/sets/data-files.md#general-file-requirements) coderen wanneer het dossier wordt gedownload, selecteer een optie van het **[!UICONTROL File Encoding]** drop-down menu. De opties zijn:

   * **[!UICONTROL UTF-8]**.
   * **[!UICONTROL Latin-1]**.

1. Als u gebruikers wilt informeren over het voltooien van taken met inst, voert u voor **[!UICONTROL Email(s) to notify when ingest jobs completes (comma separated)]** een e-mailadres in, gescheiden door komma&#39;s.
1. Selecteer **[!UICONTROL Validate]** . De verbinding met de locatie van de cloud wordt gevalideerd.
1. Als de bevestiging succesvol is, ziet u een pop-upbericht dat ![&#x200B; &#x200B;](/help/assets/icons/CheckmarkCircle.svg) Uitgezocht CheckmarkCircle **[!UICONTROL Location validation successful. Connection to cloud storage verified.]**<br/>toont als u de verbinding aan de wolkenverbinding hebt gecreeerd.**[!UICONTROL Save]**&#x200B;Anders selecteert u **[!UICONTROL Update]**. Of selecteer **[!UICONTROL Cancel]**&#x200B;om de configuratie van de cloudlocatie te annuleren.

Wanneer u bestanden uploadt naar de locatie in de cloud, wordt het bestand binnen 15 minuten gedetecteerd en verzonden als importtaak. Het resultaat van die de invoerbaan wordt gemeld in [&#x200B; de baanmanager van classificaties &#x200B;](/help/components/classifications/sets/job-manager.md). Als u aan de lijst met gebruikers wordt toegevoegd om meldingen te ontvangen over het voltooien van taken die u toevoegt, ontvangt u ook e-mailberichten.

Bijvoorbeeld:

![&#x200B; de reeksen van de Classificatie - de bevestiging e-mail van de Baan &#x200B;](assets/job-failed-validation.png){width="400"}


## Actiebalk

Op de actiebalk staan acties die beschikbaar zijn voor de geselecteerde classificatie. Beschikbare opties zijn:

| Pictogram | Actie | Beschrijving |
|---|---|---|
| ![&#x200B; doorbladeren &#x200B;](/help/assets/icons/Browse.svg) | **[!UICONTROL Add Lookup]** | Voeg een classificatieset toe als een zoekopdracht (subclassificatie).<br/> in de **[!UICONTROL Attach lookup]** lijst: <ol><li>Selecteer een opzoekclassificatie in het vervolgkeuzemenu **[!UICONTROL Classification Name]** .</li><li>Selecteer **[!UICONTROL Add]**.</li></ol>De opzoekclassificatie wordt toegevoegd aan de classificatie en vermeld in de **[!UICONTROL Classified by]** kolom gebruikend interne identiteitskaart. |
| ![&#x200B; RemoveCircle &#x200B;](/help/assets/icons/RemoveCircle.svg) | **[!UICONTROL Remove Lookup]** | Een classificatieset verwijderen als een zoekopdracht. Om de raadpleging van de classificatie permanent te schrappen, in de **[!UICONTROL Remove _classificatiereeks _van_ de dialoog van de classificatiebevestiging_]** uitgezocht **[!UICONTROL Delete]**. |
| ![&#x200B; anders noemen &#x200B;](/help/assets/icons/Rename.svg) | **[!UICONTROL Rename]** | Wijzig de naam van de **[!UICONTROL Classification Name]** van een classificatie. In de **[!UICONTROL Rename: _dialoog van de classificatienaam_]**, ga een nieuwe naam in en selecteer **[!UICONTROL Rename]**. |
| ![&#x200B; Schrapping &#x200B;](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Een classificatie verwijderen. De **[!UICONTROL Delete _dialoog van de classificatienaam_]** verschijnt. Selecteer **[!UICONTROL Delete]** om de classificatie te verwijderen. |
