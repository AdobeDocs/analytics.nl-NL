---
title: Een gegevensfeed maken
description: Leer hoe u een gegevensfeed maakt en informatie over de bestandsgegevens die aan Adobe moeten worden verstrekt.
feature: Data Feeds
exl-id: 36c8a40e-6137-4836-9d4b-bebf17b932bc
source-git-commit: d0e3a81a9b38468602b7c2b0f573425013ef78c7
workflow-type: tm+mt
source-wordcount: '2032'
ht-degree: 0%

---

# Een gegevensfeed maken

Wanneer u een gegevensfeed maakt, biedt u Adobe het volgende:

* De informatie over de bestemming waarnaar u Raw-gegevensbestanden wilt verzenden
* De gegevens die u in elk bestand wilt opnemen

Alvorens u een gegevensvoer creeert, is het belangrijk om een basisbegrip van gegevensvoer te hebben en ervoor te zorgen dat u aan alle voorwaarden voldoet. Voor meer informatie, zie [&#x200B; Overzicht van de voer van Gegevens &#x200B;](data-feed-overview.md).

## Een gegevensfeed maken en configureren {#create-and-configure-data-feed}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_os_strings"
>title="Tekenreeksen van het besturingssysteem vervangen"
>abstract="Deze optie ontruimt omhoog de gegevensoutput door de volgende koordopeenvolgingen te ontdekken ingebed in klantengegevens en hen te vervangen met een ruimte: <br/> Vensters: CRLF, CR, of TAB <br/> Mac en Linux: \ n, \ r, of \ t"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_export_file"
>title="Manifest"
>abstract="Kies of u een manifestbestand wilt opnemen bij elke gegevensdoorvoerlevering. Manifest-bestanden bevatten informatie voor elk bestand dat in de gegevensfeed is opgenomen. Bij het verzenden van gegevens uit de gegevensfeed in één pakket kunt u er ook voor kiezen een eindbestand op te nemen, maar manifestbestanden worden aanbevolen. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_notify"
>title="Melding verzenden wanneer voltooid"
>abstract="Geef een of meer e-mailadressen op waar een melding moet worden verzonden nadat de gegevensinvoer is verzonden. Meerdere e-mailadressen moeten met een komma worden gescheiden."

<!-- markdownlint-enable MD034 -->

<!-- added help for Dynamic lookups to this page: help/export/analytics-data-feed/c-df-contents/dynamic-lookups.md -->

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

1. Selecteer het 9-vierkante pictogram in hoger-recht, dan uitgezochte [!UICONTROL **Analytics**].

1. In de hoogste navigatiebar, ga [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Selecteer [!UICONTROL **leiden gegevensvoer**] tot.

   Een paginavertoningen met de volgende categorieën: [!UICONTROL **Details**], [!UICONTROL **Gegevens die**] formatteren, [!UICONTROL **structuur van Gegevens**], [!UICONTROL **Programma**], en [!UICONTROL **Bestemming**] formatteren.

   ![&#x200B; Nieuwe pagina van de gegevensvoer &#x200B;](assets/data-feed-new.png)

1. In de [!UICONTROL **sectie van Details**], voltooi de volgende gebieden:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Naam**] | De naam van de gegevensinvoer. De namen moeten binnen de geselecteerde rapportreeks uniek zijn, en kunnen tot 255 karakters in lengte zijn. [Meer informatie](/help/export/analytics-data-feed/df-faq.md#must-feed-names-be-unique) |
   | [!UICONTROL **Markeringen**] | Pas om het even welke markeringen op de gegevensvoer voor gemakkelijkere categorisering toe. U kunt op markeringen filtreren zoals die in [&#x200B; worden beschreven Filter en de lijst van gegevensvoer &#x200B;](/help/export/analytics-data-feed/df-manage-feeds.md#filter-and-search-the-list-of-data-feeds) in [&#x200B; zoeken beheert gegevensvoer &#x200B;](/help/export/analytics-data-feed/df-manage-feeds.md). |
   | [!UICONTROL **Beschrijving**] | Geef een beschrijving op voor de gegevensinvoer. De beschrijving die u toevoegt, wordt weergegeven wanneer u de gegevensfeed bewerkt. |

1. In de [!UICONTROL **het formatteren van Gegevens**] sectie, specificeer de volgende informatie:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **formaat van de Compressie**] | Het type compressie dat wordt gebruikt. **Gzip** outputs dossiers in `.tar.gz` formaat. **Zip** outputs dossiers in `.zip` formaat. |
   | [!UICONTROL **Verpakkingstype**] | Selecteer [!UICONTROL **Veelvoudige dossiers**] voor de meeste gegevensvoer. Met deze optie worden uw gegevens gepagineerd in ongecomprimeerde 2GB-blokken. (Als de [!UICONTROL **Veelvoudige dossiers**] optie wordt geselecteerd en uncompressed gegevens voor het rapporteringsvenster minder dan 2GB is, wordt één dossier verzonden.) Het selecteren van **Enig dossier** output het `hit_data.tsv` dossier in één enkel, potentieel massief dossier. |
   | [!UICONTROL **Manifest**] | Kies of u een manifestbestand wilt opnemen bij elke gegevensdoorvoerlevering. <p>U kunt uit de volgende opties kiezen:</p><ul><li>**[!UICONTROL Manifest file]**: bevat informatie voor elk bestand dat is opgenomen in de gegevensinvoer.</li><li>**[!UICONTROL Finish file (Legacy)]**: geeft aan dat de gegevensinvoer is voltooid. Er wordt geen andere informatie opgenomen. Deze optie is geschikt voor bestaande feeds die deze optie oorspronkelijk hebben gebruikt en die opnieuw moeten worden verwerkt. Deze functie is alleen beschikbaar wanneer gegevens uit de gegevensinvoer in één pakket worden verzonden. </li><li>**[!UICONTROL None]**: Er is geen bestand opgenomen</li></ul> |
   | [!UICONTROL **verzendt manifest zelfs wanneer geen gegevens**] | Bepaalt of Adobe a [&#x200B; duidelijk dossier &#x200B;](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md#feed-manifest) aan de bestemming zou moeten leveren wanneer geen gegevens voor een voederinterval worden verzameld. Als u **Manifest dossier** selecteert, ontvangt u een duidelijk dossier gelijkend op het volgende wanneer geen gegevens worden verzameld:<p>`text`</p><p>`Datafeed-Manifest-Version: 1.0`</p><p>`Lookup-Files: 0`</p><p>`Data-Files: 0`</p><p> `Total-Records: 0`</p> |
   | [!UICONTROL **vervangt werkend systeemkoorden**] | Bij het verzamelen van gegevens kunnen sommige tekens (zoals nieuwe regels) problemen veroorzaken. Selecteer deze optie als u deze tekens uit de voederbestanden wilt verwijderen.<p>Deze optie ontdekt de volgende koordopeenvolgingen ingebed in klantengegevens en vervangt hen met een ruimte:</p> <ul><li>**Vensters:** CRLF, CR, of TAB</li><li>**Mac en Linux:** \ n, \ r, of \ t</li></ul> |
   | [!UICONTROL **laat dynamische raadplegingen**] toe | Met dynamische zoekopdrachten kunt u extra opzoekbestanden in uw gegevensfeed ontvangen die anders niet beschikbaar zijn. Met deze instelling kunnen de volgende opzoektabellen worden verzonden met elk gegevensbestand met gegevensinvoer:<ul><li> **naam van de Drager**</li><li>**Mobiele attributen**</li><li>**Werkend systeemtype**</li></ul><p>Voor meer informatie, zie [&#x200B; Dynamische raadplegingen &#x200B;](/help/export/analytics-data-feed/c-df-contents/dynamic-lookups.md).</p> |
   | **laat-aankomende treffers** toestaan | Historische gegevens kunnen worden aangeleverd nadat een gegevenfeed-taak een bepaald uur of een bepaalde dag is verwerkt, bijvoorbeeld door middel van treffers met een tijdstempel of gegevensbronnen.<p>Selecteer deze optie om gegevens op te nemen die zijn ontvangen nadat de gegevensinvoertaak de gegevens heeft verwerkt binnen de ingestelde rapportagefrequentie (gewoonlijk dagelijks of per uur). Als deze optie is ingeschakeld, controleert elke keer dat een gegevensfeed gegevens verwerkt, de late resultaten die zijn binnengekomen en worden deze in batches opgeslagen met het volgende gegevensdoorvoerbestand dat wordt verzonden.</p><p>Voor meer informatie, zie [&#x200B; laat-aankomende treffers &#x200B;](/help/export/analytics-data-feed/c-df-contents/late-arriving-hits.md).</p> |
   | **venster van de Lookback** (voor laat-aankomende treffers) | Deze optie wordt weergegeven wanneer de optie **[!UICONTROL Allow late-arring hits]** is ingeschakeld. Selecteer het terugkijkvenster om het tijdkader van late klappen te beperken die inbegrepen zijn. Selecteer **[!UICONTROL Unlimited]** als u alle laat aankomende klappen wilt toestaan, ongeacht hoe laat. U kunt een vooraf ingesteld interval kiezen, zoals **[!UICONTROL 1 hour]** , **[!UICONTROL 2 hours]** , **[!UICONTROL 1 week]** , **[!UICONTROL 2 weeks]** enzovoort. Of selecteer **[!UICONTROL Custom lookback window]** en geef vervolgens in het veld **[!UICONTROL Custom Lookback]** een opzoekvenster op van maximaal 26.280 uur. |

1. In de [!UICONTROL **sectie van de Gegevensstructuur**], op het **[!UICONTROL Report suite]** gebied, selecteer de bronrapportreeks die de gegevens bevat die u wilt uitvoeren. <p>Houd rekening met het volgende wanneer u een rapportsuite selecteert:</p> <ul><li>Als de veelvoudige gegevensvoer voor de zelfde rapportreeks wordt gecreeerd, moet elke gegevensvoer verschillende kolomdefinities hebben.</li><li>Alleen bronrapportsuites ondersteunen gegevensfeeds; virtuele rapportsuites worden niet ondersteund.</li><li>De lijst van beschikbare kolommen hangt van het login bedrijf af dat de geselecteerde rapportreeks tot behoort. Als u de rapportsuite wijzigt, kan de lijst met beschikbare kolommen worden gewijzigd. </li></ul>

1. Gebruik een van de volgende methoden of beide methoden om te bepalen welke gegevenskolommen in de feed moeten worden opgenomen:

   * **voeg individueel kolommen toe:** in de **[!UICONTROL Available]** sectie op de linkerzijde, selecteer om het even welke kolommen die u wilt omvatten, dan selecteren **[!UICONTROL Include]**. Alle gegevenskolommen in Adobe Analytics zijn beschikbaar. U kunt meerdere kolommen selecteren door **[!UICONTROL Shift]** ingedrukt te houden of door **[!UICONTROL Command]** (in macOS) of **[!UICONTROL Ctrl]** (in Windows) ingedrukt te houden. Klik op **[!UICONTROL Add all]** om alle kolommen in een gegevensfeed op te nemen.

     Kolommen die u toevoegt, worden weergegeven in de sectie **[!UICONTROL Included]** aan de rechterkant.

   * **voeg een kolommalplaatje toe:** op het **[!UICONTROL Column templates]** gebied, selecteer een kolommalplaatje toe te voegen. Een kolomsjabloon is een vooraf gedefinieerde groep kolommen en Adobe biedt standaard diverse sjablonen.

     Alle kolommen in de sjabloon worden weergegeven in de sectie **[!UICONTROL Included]** aan de rechterkant.

1. (Optioneel) Als u een kolomsjabloon wilt maken die is gebaseerd op de gegevensfeed die u momenteel maakt, selecteert u **[!UICONTROL Save as template]** , geeft u een naam voor de sjabloon op en selecteert u **[!UICONTROL Save]** . Deze optie is handig als u extra gegevensfeeds wilt maken die dezelfde kolommen bevatten.

   ![&#x200B; creeer kolommalplaatje terwijl het creëren van een gegevensvoer &#x200B;](assets/data-feed-template-create2.png)

1. (Optioneel) Selecteer **[!UICONTROL Download columns]** als u een lijst met opgenomen kolommen in de CSV-indeling wilt downloaden. Deze optie kan handig zijn voor gegevensfeeds met een groot aantal kolommen.

1. In de [!UICONTROL **sectie van het Programma**], specificeer de volgende informatie:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Frequentie**] | Selecteer hoe vaak de gegevensinvoer moet worden verzonden. De beschikbare opties worden dynamisch ingevuld op basis van de configuratie van de rapportsuite. <p>De volgende opties zijn algemeen beschikbaar:</p><ul><li>**Dagelijkse**: De voer bevat de waarde van een volledige dag van gegevens, van middernacht aan middernacht in de tijdzone van de rapportreeks. Gebruik deze optie voor back-up of historische gegevens of voor doorlopende feeds.</li><li>**Uur**: De voer bevat de waarde van één uur van gegevens. Gebruik deze optie als u doorgaat met feeds.</li></ul><p>Een exportfrequentie van 15 minuten is mogelijk, maar is standaard niet beschikbaar. Om deze optie beschikbaar te maken in uw omgeving, dient u eerst contact op te nemen met de klantenservice van Adobe en te verzoeken dat uw rapportenpakket is geconfigureerd voor ondersteuning van 15-minuten export.</p> |
   | [!UICONTROL **Verwerkingsvertraging**] | Geef op of u een bepaalde hoeveelheid tijd wilt wachten voordat u een bestand met gegevensinvoer verwerkt. Een vertraging kan handig zijn om mobiele implementaties de mogelijkheid te geven om offlineapparaten online te komen en gegevens te verzenden. Het kan ook worden gebruikt om de server-zijprocessen van uw organisatie in het beheren van eerder verwerkte dossiers aan te passen. In de meeste gevallen is geen uitstel nodig. U kunt een feed maximaal 8 uur (480 minuten) of zelfs langer uitstellen als u een aangepaste hoeveelheid tijd selecteert (9.999 minuten vertraging of ongeveer 1 week). |
   | [!UICONTROL **Ononderbroken voer**] | Als u deze optie selecteert, wordt de einddatum verwijderd, zodat een feed voor onbepaalde tijd kan worden uitgevoerd. Als een feed de verwerking van historische gegevens heeft voltooid, wacht een feed tot de gegevens een bepaald uur of een bepaalde dag zijn verzameld. Wanneer het huidige uur of de huidige dag eindigt, begint de verwerking na de opgegeven vertraging. |
   | [!UICONTROL **de datum van het Begin**] | Geef de datum op waarop de gegevensinvoer moet beginnen. Als u onmiddellijk wilt beginnen met het verwerken van gegevensfeeds voor historische gegevens, stelt u deze datum in op een datum in het verleden waarop gegevens worden verzameld. De begindatum is gebaseerd op de tijdzone van de rapportreeks. |
   | [!UICONTROL **einddatum**] | Geef de datum op waarop de gegevensinvoer moet worden beëindigd. De einddatum is gebaseerd op de tijdzone van de rapportreeks. |

1. In de [!UICONTROL **sectie van de Bestemming**], vorm de bestemming waar u de gegevens wilt worden verzonden.

   >[!NOTE]
   >
   >Overweeg het volgende wanneer het vormen van een rapportbestemming:
   >
   >* Adobe raadt u aan een cloudaccount te gebruiken voor uw rapportbestemming. [&#x200B; Verouderde FTP en de rekeningen van SFTP &#x200B;](#legacy-destinations) zijn beschikbaar, maar niet geadviseerd.
   >* Alle cloudaccounts die u eerder hebt geconfigureerd, kunnen worden gebruikt voor gegevensfeeds. U kunt cloudaccounts op de volgende manieren configureren:
   >
   >   * Wanneer het vormen van wolkenrekeningen voor [&#x200B; Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
   >   
   >   * Wanneer [&#x200B; het invoeren van de classificatiegegevens van Adobe Analytics &#x200B;](/help/components/locations/locations-manager.md) (Om het even welke plaatsen die voor het invoeren van classificatiegegevens worden gevormd kunnen niet worden gebruikt.)
   >   
   >   * Van de manager van Plaatsen, in [&#x200B; Componenten > Plaatsen &#x200B;](/help/components/locations/configure-import-accounts.md)
   >
   >* Cloud-accounts zijn gekoppeld aan uw Adobe Analytics-gebruikersaccount. Andere gebruikers kunnen geen wolkenrekeningen gebruiken of bekijken die u vormt tenzij u hen ter beschikking stelt aan alle gebruikers in uw organisatie.
   >
   >* U kunt om het even welke plaatsen uitgeven die u van de manager van Plaatsen in [&#x200B; Componenten > Plaatsen &#x200B;](/help/components/locations/configure-import-accounts.md) creeert

   Vul de volgende velden in:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Rekening**] | Voer een van de volgende handelingen uit:<ul><li>**Gebruik een bestaande rekening:** selecteer het drop-down menu naast het **[!UICONTROL Account]** gebied. U kunt ook beginnen met het typen van de accountnaam en deze selecteren in het keuzemenu. <p>De rekeningen zijn beschikbaar aan u slechts als u hen vormde of als zij met een organisatie worden gedeeld u een deel van bent.</p></li><li>**creeer een nieuwe rekening:** Uitgezocht **[!UICONTROL Add new]** onder het **[!UICONTROL Account]** gebied. Voor informatie over hoe te om de rekening te vormen, zie [&#x200B; een plaatsrekening &#x200B;](/help/components/locations/configure-import-accounts.md#configure-a-location-account) in [&#x200B; vormen wolkeninvoer en uitvoerrekeningen &#x200B;](/help/components/locations/configure-import-accounts.md).</li></ul> |
   | [!UICONTROL **Plaats**] | Voer een van de volgende handelingen uit:<ul><li>**Gebruik een bestaande plaats:** selecteer het drop-down menu naast het **[!UICONTROL Location]** gebied. Of typ de naam van de locatie en selecteer deze in het keuzemenu.</li><li>**creeer een nieuwe plaats:** Uitgezocht **[!UICONTROL Add new]** onder het **[!UICONTROL Location]** gebied. Voor informatie over hoe te om de plaats te vormen, zie [&#x200B; een plaats &#x200B;](/help/components/locations/configure-import-locations.md#configure-a-location) in [&#x200B; vormen wolkeninvoer en uitvoerplaatsen &#x200B;](/help/components/locations/configure-import-locations.md). |
   | [!UICONTROL **Melden wanneer volledig**] | Geef een of meer e-mailadressen op waar een melding moet worden verzonden nadat de gegevensinvoer is verzonden of niet is verzonden. Meerdere e-mailadressen moeten met een komma worden gescheiden. |

1. Selecteer **[!UICONTROL Save]**.

## Kolomsjablonen beheren

Met sjablonen kunt u dezelfde kolommen opnieuw gebruiken voor toekomstige gegevensfeeds die u maakt.

Bij het beheren van sjablonen kunt u nieuwe sjablonen maken, reeds gemaakte sjablonen gebruiken, sjablonen kopiëren, sjablonen bewerken en sjablonen verwijderen.

[!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**] > **[!UICONTROL Manage templates]**

![&#x200B; beheert kolommalplaatjes &#x200B;](assets/data-feed-template-manage.png)

### Een kolomsjabloon maken

Als u meerdere gegevensfeeds maakt die dezelfde kolommen gebruiken, wordt u aangeraden kolomsjablonen te maken. Alle kolomsjablonen die u maakt, kunnen door iedereen in uw organisatie worden gebruikt.

Een kolomsjabloon maken:

1. In Adobe Analytics, ga [!UICONTROL **Admin**] > [!UICONTROL **de voer van Gegevens**] > **[!UICONTROL Manage templates]**.

1. Selecteer **[!UICONTROL Create new template]** om een nieuwe kolomsjabloon te maken.

   ![&#x200B; creeer kolommalplaatje &#x200B;](assets/data-feed-template-create.png)

1. Geef in het veld **[!UICONTROL Template name]** een naam voor de sjabloon op.

1. Selecteer in de sectie **[!UICONTROL Available]** aan de linkerkant de kolommen die u wilt opnemen en selecteer vervolgens **[!UICONTROL Include]** . Alle beschikbare gegevenskolommen in Adobe Analytics zijn beschikbaar. U kunt meerdere kolommen selecteren door **[!UICONTROL Shift]** ingedrukt te houden of door **[!UICONTROL Command]** (in macOS) of **[!UICONTROL Ctrl]** (in Windows) ingedrukt te houden. Klik op **[!UICONTROL Add all]** om alle kolommen in een gegevensfeed op te nemen.

   Kolommen die u toevoegt, worden weergegeven in de sectie **[!UICONTROL Included]** aan de rechterkant.

1. Selecteer **[!UICONTROL Save]**.

### Een kolomsjabloon bewerken

1. In Adobe Analytics, ga [!UICONTROL **Admin**] > [!UICONTROL **de voer van Gegevens**] > **[!UICONTROL Manage templates]**.

1. Selecteer de sjabloon die u wilt bewerken en selecteer vervolgens **[!UICONTROL Edit]** .

1. Breng desgewenst wijzigingen aan en selecteer vervolgens **[!UICONTROL Save]** .

### Een kolomsjabloon kopiëren

1. In Adobe Analytics, ga [!UICONTROL **Admin**] > [!UICONTROL **de voer van Gegevens**] > **[!UICONTROL Manage templates]**.

1. Selecteer de sjabloon die u wilt kopiëren en selecteer vervolgens **[!UICONTROL Copy]** .

1. Geef in het veld **[!UICONTROL Template name]** een naam voor de sjabloon op.

1. Breng eventuele aanvullende wijzigingen aan en selecteer vervolgens **[!UICONTROL Save]** .

### Kolomsjablonen verwijderen

1. In Adobe Analytics, ga [!UICONTROL **Admin**] > [!UICONTROL **de voer van Gegevens**] > **[!UICONTROL Manage templates]**.

1. Selecteer een of meer sjablonen die u wilt verwijderen en selecteer vervolgens **[!UICONTROL Delete]** .


<!-- why would you want to do this? -->


<!-- I don't think we need anything after this, but saving here just in case:

1. In the [!UICONTROL **Feed Information**] section, complete the following fields:
   
   | Field | Function |
   |---------|----------|
   | [!UICONTROL **Name**] | The name of the data feed. Must be unique within the selected report suite, and can be up to 255 characters in length. [Learn more](/help/export/analytics-data-feed/df-faq.md#must-feed-names-be-unique) |
   | [!UICONTROL **Report suite**] | The report suite that the data feed is based on. If multiple data feeds are created for the same report suite, they must have different column definitions. Only source report suites support data feeds; virtual report suites are not supported. |
   | [!UICONTROL **Email when complete**] | The email address to be notified when a feed finishes processing. The email address must be properly formatted. |
   | [!UICONTROL **Feed interval**] | Select **Daily** for backfill or historical data. Daily feeds contain a full day's worth of data, from midnight to midnight in the report suite's time zone. Select **Hourly** for continuing data (Daily is also available for continuing feeds if you prefer). Hourly feeds contain a single hour's worth of data. |
   | [!UICONTROL **Delay processing**] | Wait a given amount of time before processing a data feed file. A delay can be useful to give mobile implementations an opportunity for offline devices to come online and send data. It can also be used to accommodate your organization's server-side processes in managing previously processed files. In most cases, no delay is needed. A feed can be delayed by up to 120 minutes. |
   | [!UICONTROL **Start & end dates**] | The start date indicates the date when you want the data feed to begin. To immediately begin processing data feeds for historical data, set this date to any date in the past when data is being collected. The start and end dates are based on the report suite's time zone. |
   | [!UICONTROL **Continuous feed**] | This checkbox removes the end date, allowing a feed to run indefinitely. When a feed finishes processing historical data, a feed waits for data to finish collecting for a given hour or day. Once the current hour or day concludes, processing begins after the specified delay. |
   
1. In the [!UICONTROL **Destination**] section, in the [!UICONTROL **Type**] drop-down menu, select the destination where you want the data to be sent. 

   >[!NOTE]
   >
   >Consider the following when configuring a report destination:
   >
   >* We recommend using a cloud account for your report destination. [Legacy FTP and SFTP accounts](#legacy-destinations) are available, but are not recommended.
   >* Any cloud accounts that you previously configured are available to use for Data Feeds. You can configure cloud accounts in any of the following ways:
   >
   >   * When configuring cloud accounts for [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) 
   >   
   >   * When [importing Adobe Analytics classification data](/help/components/locations/locations-manager.md) (Any locations that are configured for importing classification data cannot be used.)
   >   
   >   * From the Locations manager, in [Components > Locations](/help/components/locations/configure-import-accounts.md) 
   >
   >* Cloud accounts are associated with your Adobe Analytics user account. Other users cannot use or view cloud accounts that you configure.
   >
   >* You can edit any locations that you create from the Locations manager in [Components > Locations](/help/components/locations/configure-import-accounts.md)

   ![Data feed destination drop-down menu](assets/datafeed-destinations-dropdown.png)

   Use any of the following destination types when creating a data feed. For configuration instructions, expand the destination type. (Additional [legacy destinations](#legacy-destinations) are also available, but are not recommended.)

   +++Amazon S3

   You can send feeds directly to Amazon S3 buckets. This destination type requires only your Amazon S3 account and the location (bucket). 

   Adobe Analytics uses cross-account authentication to upload files from Adobe Analytics to the specified location in your Amazon S3 instance.

   When using Amazon S3 with Data Feeds, only SSE-S3 encryption is supported.

   To configure an Amazon S3 bucket as the destination for a data feed:

   1. Begin creating a data feed as described in [Create and configure a data feed](#create-and-configure-a-data-feed).
   
   1. In the [!UICONTROL **Destination**] section, in the [!UICONTROL **Type**] drop-down menu, select [!UICONTROL **Amazon S3**].

      ![Amazon S3 destination](assets/datafeed-destination-amazons3.png)

   1. Select [!UICONTROL **Select location**].

      The Amazon S3 Export Locations page is displayed.

   1. (Conditional) If an Amazon S3 account (and a location on that account) has already been configured in Adobe Analytics, you can use it as your data feed destination: 

      >[!NOTE]
      >
      >Accounts are available to you only if you configured them or if they were shared with an organization you are a part of.
   
      1. Select the account from the [!UICONTROL **Select account**] drop-down menu.

         Any cloud accounts that were configured in any of the following areas of Adobe Analytics are available to use:
      
         * When importing Adobe Analytics classification data, as described in [Schema](/help/components/classifications/sets/manage/schema.md).
      
           However, any locations that are configured for importing classification data cannot be used. Instead, add a new destination as described below.

         * When configuring accounts and locations in the Locations area, as described in [Configure cloud import and export accounts](/help/components/locations/configure-import-accounts.md) and [Configure cloud import and export locations](/help/components/locations/configure-import-locations.md).
   
      1. Select the location from the [!UICONTROL **Select location**] drop-down menu.

      1. Select [!UICONTROL **Save**] > [!UICONTROL **Save**].

      The destination is now configured to send data to the Amazon S3 location that you specified.
   
   1. (Conditional) If you have not previously added an Amazon S3 account:

      1. Select [!UICONTROL **Add account**], then specify the following information:
   
         |Field | Function |
         |---------|----------|
         | [!UICONTROL **Account name**] | A name for the account. This can be any name you choose. |
         | [!UICONTROL **Account description**] | A description for the account. |
         | [!UICONTROL **Role ARN**] | You must provide a Role ARN (Amazon Resource Name) that Adobe can use to gain access to the Amazon S3 account. To do this, you create an IAM permission policy for the source account, attach the policy to a user, and then create a role for the destination account. For specific information, see [this AWS documentation](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |
         | [!UICONTROL **User ARN**] | The User ARN (Amazon Resource Name) is provided by Adobe. You must attach this user to the policy you created. |

         {style="table-layout:auto"}

      1. Select [!UICONTROL **Add location**], then specify the following information:
   
         |Field | Function |
         |---------|----------|
         | [!UICONTROL **Name**] | A name for the account.  |
         | [!UICONTROL **Description**] | A description for the account. |
         | [!UICONTROL **Bucket**] | The bucket within your Amazon S3 account where you want Adobe Analytics data to be sent. <p>Ensure that the User ARN that was provided by Adobe has the `S3:PutObject` permission in order to upload files to this bucket. This permission allows the User ARN to upload initial files and overwrite files for subsequent uploads.</p><p>Bucket names must meet specific naming rules. For example, they must be between 3 to 63 characters long, can consist only of lowercase letters, numbers, dots (.), and hyphens (-), and must begin and end with a letter or number. [A complete list of naming rules are available in the AWS documentation](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
         | [!UICONTROL **Prefix**] | The folder within the bucket where you want to put the data. Specify a folder name, then add a backslash after the name to create the folder. For example, `folder_name/` |

         {style="table-layout:auto"}

      1. Select [!UICONTROL **Create**] > [!UICONTROL **Save**].

         The destination is now configured to send data to the Amazon S3 location that you specified.

      1. (Conditional) If you need to manage the destination (account and location) that you just created, it is available in the [Locations manager](/help/components/locations/locations-manager.md).
   
   +++

   +++Azure RBAC

   You can send feeds directly to an Azure container by using RBAC authentication. This destination type requires an Application ID, Tenant ID, and Secret. 

   To configure an Azure RBAC account as the destination for a data feed:

   1. If you haven't already, create an Azure application that Adobe Analytics can use for authentication, then grant access permissions in access control (IAM). 
   
      For information, refer to the [Microsoft Azure documentation about how to create an Azure Active Directory application](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal). 
   
   1. In the Adobe Analytics admin console, in the [!UICONTROL **Destination**] section, in the [!UICONTROL **Type**] drop-down menu, select [!UICONTROL **Azure RBAC**].

      ![Azure RBAC destination](assets/datafeed-destination-azurerbac.png)

   1. Select [!UICONTROL **Select location**].

      The Azure RBAC Export Locations page is displayed.

   1. (Conditional) If an Azure RBAC account (and a location on that account) has already been configured in Adobe Analytics, you can use it as your data feed destination: 

      >[!NOTE]
      >
      >Accounts are available to you only if you configured them or if they were shared with an organization you are a part of.
   
      1. Select the account from the [!UICONTROL **Select account**] drop-down menu.

      Any cloud accounts that you configured in any of the following areas of Adobe Analytics are available to use:
      
         * When importing Adobe Analytics classification data, as described in [Schema](/help/components/classifications/sets/manage/schema.md).
      
           However, any locations that are configured for importing classification data cannot be used. Instead, add a new destination as described below.

         * When configuring accounts and locations in the Locations area, as described in [Configure cloud import and export accounts](/help/components/locations/configure-import-accounts.md) and [Configure cloud import and export locations](/help/components/locations/configure-import-locations.md).

      1. Select the location from the [!UICONTROL **Select location**] drop-down menu.

      1. Select [!UICONTROL **Save**] > [!UICONTROL **Save**].

         The destination is now configured to send data to the Azure RBAC location that you specified.

   1. (Conditional) If you have not previously added an Azure RBAC account:

      1. Select [!UICONTROL **Add account**], then specify the following information:
   
         |Field | Function |
         |---------|----------|
         | [!UICONTROL **Account name**] | A name for the Azure RBAC account. This name displays in the [!UICONTROL **Select account**] drop-down field and can be any name you choose. |
         | [!UICONTROL **Account description**] | A description for the Azure RBAC account. This description displays in the [!UICONTROL **Select account**] drop-down field and can be any name you choose.  |
         | [!UICONTROL **Application ID**] | Copy this ID from the Azure application that you created. In Microsoft Azure, this information is located on the **Overview** tab within your application. For more information, see the [Microsoft Azure documentation about how to register an application with the Microsoft identity platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Tenant ID**] | Copy this ID from the Azure application that you created. In Microsoft Azure, this information is located on the **Overview** tab within your application. For more information, see the [Microsoft Azure documentation about how to register an application with the Microsoft identity platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Secret**] | Copy the secret from the Azure application that you created. In Microsoft Azure, this information is located on the **Certificates & secrets** tab within your application. For more information, see the [Microsoft Azure documentation about how to register an application with the Microsoft identity platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

         {style="table-layout:auto"}

      1. Select [!UICONTROL **Add location**], then specify the following information: 
   
         |Field | Function |
         |---------|----------|
         | [!UICONTROL **Name**] | A name for the location. This name displays in the [!UICONTROL **Select location**] drop-down field and can be any name you choose. |
         | [!UICONTROL **Description**] | A description for the location. This description displays in the [!UICONTROL **Select location**] drop-down field and can be any name you choose. |
         | [!UICONTROL **Account**] | The Azure storage account. |
         | [!UICONTROL **Container**] | The container within the account you specified where you want Adobe Analytics data to be sent. Ensure that you grant permissions to upload files to the Azure application that you created earlier. |
         | [!UICONTROL **Prefix**] | The folder within the container where you want to put the data. Specify a folder name, then add a backslash after the name to create the folder. For example, `folder_name/`<p>Make sure the Application ID that you specified when configuring the Azure RBAC account has been granted the `Storage Blob Data Contributor` role in order to access the container (folder).</p> <p>For more information, see [Azure built-in roles](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).</p> |

         {style="table-layout:auto"}

      1. Select [!UICONTROL **Create**] > [!UICONTROL **Save**].

         The destination is now configured to send data to the Azure RBAC location that you specified.

      1. (Conditional) If you need to manage the destination (account and location) that you just created, it is available in the [Locations manager](/help/components/locations/locations-manager.md).
   
   +++

   +++Azure SAS

   You can send feeds directly to an Azure container by using SAS authentication. This destination type requires an Application ID, Tenant ID, Key vault URI, Key vault secret name, and secret. 

   To configure Azure SAS as the destination for a data feed:

   1. If you haven't already, create an Azure application that Adobe Analytics can use for authentication. 
   
      For information, refer to the [Microsoft Azure documentation about how to create an Azure Active Directory application](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal). 
   
   1. In the Adobe Analytics admin console, in the [!UICONTROL **Destination**] section, select [!UICONTROL **Azure SAS**].

      ![Azure SAS destination](assets/datafeed-destination-azuresas.png)

   1. Select [!UICONTROL **Select location**].

      The Azure SAS Export Locations page is displayed.

   1. (Conditional) If an Azure SAS account (and a location on that account) has already been configured in Adobe Analytics, you can use it as your data feed destination: 

      >[!NOTE]
      >
      >Accounts are available to you only if you configured them or if they were shared with an organization you are a part of.
   
      1. Select the account from the [!UICONTROL **Select account**] drop-down menu.

         Any cloud accounts that you configured in any of the following areas of Adobe Analytics are available to use:
      
         * When importing Adobe Analytics classification data, as described in [Schema](/help/components/classifications/sets/manage/schema.md).
      
           However, any locations that are configured for importing classification data cannot be used. Instead, add a new destination as described below.

         * When configuring accounts and locations in the Locations area, as described in [Configure cloud import and export accounts](/help/components/locations/configure-import-accounts.md) and [Configure cloud import and export locations](/help/components/locations/configure-import-locations.md).

      1. Select the location from the [!UICONTROL **Select location**] drop-down menu.

      1. Select [!UICONTROL **Save**] > [!UICONTROL **Save**].

         The destination is now configured to send data to the Azure SAS location that you specified.
   
   1. (Conditional) If you have not previously added an Azure SAS account:

      1. Select [!UICONTROL **Add account**], then specify the following information:
   
         |Field | Function |
         |---------|----------|
         | [!UICONTROL **Account name**] | A name for the Azure SAS account. This name displays in the [!UICONTROL **Select account**] drop-down field and can be any name you choose. |
         | [!UICONTROL **Account description**] | A description for the Azure SAS account. This description displays in the [!UICONTROL **Select account**] drop-down field and can be any name you choose. |
         | [!UICONTROL **Application ID**] | Copy this ID from the Azure application that you created. In Microsoft Azure, this information is located on the **Overview** tab within your application. For more information, see the [Microsoft Azure documentation about how to register an application with the Microsoft identity platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Tenant ID**] | Copy this ID from the Azure application that you created. In Microsoft Azure, this information is located on the **Overview** tab within your application. For more information, see the [Microsoft Azure documentation about how to register an application with the Microsoft identity platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Key vault URI**] | <p>The path to the SAS URI in Azure Key Vault. To configure Azure SAS, you need to store an SAS URI as a secret using Azure Key Vault. For information, see the [Microsoft Azure documentation about how to set and retrieve a secret from Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>After the key vault URI is created:<ul><li>Add an access policy on the Key Vault in order to grant permission to the Azure application that you created.<p>For information, see the [Microsoft Azure documentation about how to assign a Key Vault access policy](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p><p>Or</p><p>If you want to grant an access role directly without creating an access policy, see the [Microsoft Azure documentation about how to assign Azure roles using Azure portal](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal). This adds the role assignment for the application ID to access the key vault URI. </p></li><li>Make sure the Application ID has been granted the `Key Vault Certificate User` built-in role in order to access the key vault URI.</br><p>For more information, see [Azure built-in roles](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).</p></li></ul> |
         | [!UICONTROL **Key vault secret name**] | The secret name you created when adding the secret to Azure Key Vault. In Microsoft Azure, this information is located in the Key Vault you created, on the **Key Vault** settings pages. For information, see the [Microsoft Azure documentation about how to set and retrieve a secret from Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
         | [!UICONTROL **Secret**] | Copy the secret from the Azure application that you created. In Microsoft Azure, this information is located on the **Certificates & secrets** tab within your application. For more information, see the [Microsoft Azure documentation about how to register an application with the Microsoft identity platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

         {style="table-layout:auto"}

      1. Select [!UICONTROL **Add location**], then specify the following information: 
   
         |Field | Function |
         |---------|----------|
         | [!UICONTROL **Name**] | A name for the location. This name displays in the [!UICONTROL **Select location**] drop-down field and can be any name you choose. |
         | [!UICONTROL **Description**] | A description for the location. This description displays in the [!UICONTROL **Select location**] drop-down field and can be any name you choose. |
         | [!UICONTROL **Container**] | The container within the account you specified where you want Adobe Analytics data to be sent. |
         | [!UICONTROL **Prefix**] | The folder within the container where you want to put the data. Specify a folder name, then add a backslash after the name to create the folder. For example, `folder_name/`<p>Make sure that the SAS URI store that you specified in the Key Vault secret name field when configuring the Azure SAS account has the `Write` permission. This allows the SAS URI to create files in your Azure container. <p>If you want the SAS URI to also overwrite files, make sure that the SAS URI store has the `Delete` permission.</p><p>For more information, see [Blob storage resources](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction#blob-storage-resources) in the Azure Blob Storage documentation.</p> |

         {style="table-layout:auto"}

      1. Select [!UICONTROL **Create**] > [!UICONTROL **Save**].

         The destination is now configured to send data to the Azure SAS location that you specified.

      1. (Conditional) If you need to manage the destination (account and location) that you just created, it is available in the [Locations manager](/help/components/locations/locations-manager.md).
   
   +++

   +++Google Cloud Platform

   You can send feeds directly to Google Cloud Platform (GCP) buckets. This destination type requires only your GCP account name and the location (bucket) name. 
   
   Adobe Analytics uses cross-account authentication to upload files from Adobe Analytics to the specified location in your GCP instance.

   To configure a GCP bucket as the destination for a data feed:

   1. In the Adobe Analytics admin console, in the [!UICONTROL **Destination**] section, select [!UICONTROL **Google Cloud Platform**].

      ![Google Cloud Platform destination](assets/datafeed-destination-gcp.png)

   1. Select [!UICONTROL **Select location**].

      The GCP Export Locations page is displayed.

   1. (Conditional) If a Google Cloud Platform account (and a location on that account) has already been configured in Adobe Analytics, you can use it as your data feed destination: 

      >[!NOTE]
      >
      >Accounts are available to you only if you configured them or if they were shared with an organization you are a part of.
   
      1. Select the account from the [!UICONTROL **Select account**] drop-down menu.

         Any cloud accounts that you configured in any of the following areas of Adobe Analytics are available to use:
      
         * When importing Adobe Analytics classification data, as described in [Schema](/help/components/classifications/sets/manage/schema.md).
      
           However, any locations that are configured for importing classification data cannot be used. Instead, add a new destination as described below.

         * When configuring accounts and locations in the Locations area, as described in [Configure cloud import and export accounts](/help/components/locations/configure-import-accounts.md) and [Configure cloud import and export locations](/help/components/locations/configure-import-locations.md).

      1. Select the location from the [!UICONTROL **Select location**] drop-down menu.

      1. Select [!UICONTROL **Save**] > [!UICONTROL **Save**].

         The destination is now configured to send data to the Google Cloud Platform location that you specified.
   
   1. (Conditional) If you have not previously added a GCP account:

      1. Select [!UICONTROL **Add account**], then specify the following information:
   
         |Field | Function |
         |---------|----------|
         | [!UICONTROL **Account name**] | A name for the account. This can be any name you choose. |
         | [!UICONTROL **Account description**] | A description for the account. |
         | [!UICONTROL **Project ID**] | Your Google Cloud project ID. See the [Google Cloud documentation about getting a project ID](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |

         {style="table-layout:auto"}

      1. Select [!UICONTROL **Add location**], then specify the following information:
   
         |Field | Function |
         |---------|----------|
         | [!UICONTROL **Principal**] | The Principal is provided by Adobe. You must grant permission to receive feeds to this principal. |
         | [!UICONTROL **Name**] | A name for the account.  |
         | [!UICONTROL **Description**] | A description for the account. |
         | [!UICONTROL **Bucket**] | The bucket within your GCP account where you want Adobe Analytics data to be sent. <p>Ensure that you have granted either of the following permissions to the Principal provided by Adobe: (For information about granting permissions, see [Add a principal to a bucket-level policy](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add) in the Google Cloud documentation.)<ul><li>`roles/storage.objectCreator`: Use this permission if you  want to limit the Principal to only create files in your GCP account. </br>**Important:** If you use this permission with scheduled reporting, you must use a unique file name for each new scheduled export. Otherwise, the report generation will fail because the Principal does not have access to overwrite existing files.</li><li>(Recommended) `roles/storage.objectUser`: Use this permission if you want the Principal to have access to view, list, update, and delete files in your GCP account.</br>This permission allows the Principal to overwrite existing files for subsequent uploads, without the need to auto-generate unique file names for each new scheduled export.</li></ul><p>If your organization is using [Organization policy constraints](https://cloud.google.com/storage/docs/org-policy-constraints) to allow only the Google Cloud Platform account in your allow list, you need the following Adobe-owned Google Cloud Platform organization ID: <ul><li>`DISPLAY_NAME`: `adobe.com`</li><li>`ID`: `178012854243`</li><li>`DIRECTORY_CUSTOMER_ID`: `C02jo8puj`</li></ul> </p> |
         | [!UICONTROL **Prefix**] | The folder within the bucket where you want to put the data. Specify a folder name, then add a backslash after the name to create the folder. For example, `folder_name/` |

         {style="table-layout:auto"}

      1. Select [!UICONTROL **Create**] > [!UICONTROL **Save**].

         The destination is now configured to send data to the GCP location that you specified.

      1. (Conditional) If you need to manage the destination (account and location) that you just created, it is available in the [Locations manager](/help/components/locations/locations-manager.md).
   
   +++

1. In the  [!UICONTROL **Data Column Definitions**] section, select the latest [!UICONTROL **All Adobe Columns**] template in the drop-down menu, then complete the following fields:
   
   |Field | Function |
   |---------|----------|
   | [!UICONTROL **Remove escaped characters**] | When collecting data, some characters (such as newlines) can cause issues. Check this box if you would like these characters removed from feed files. |
   | [!UICONTROL **Compression format**] | The type of compression used. **Gzip** outputs files in `.tar.gz` format. **Zip** outputs files in `.zip` format. |
   | [!UICONTROL **Packaging type**] | Select [!UICONTROL **Multiple files**] for most data feeds. This option paginates your data into uncompressed 2GB chunks. (If the [!UICONTROL **Multiple files**] option is selected and uncompressed data for the reporting window is less than 2GB, one file is sent.) Selecting **Single file** outputs the `hit_data.tsv` file in a single, potentially massive file. |
   | [!UICONTROL **Manifest**] | Determines whether Adobe should deliver a [manifest file](c-df-contents/datafeeds-contents.md#feed-manifest) to the destination when no data is collected for a feed interval. If you select **Manifest File**, you receive a manifest file similar to the following when no data is collected:<p>`text`</p><p>`Datafeed-Manifest-Version: 1.0`</p><p>`Lookup-Files: 0`</p><p>`Data-Files: 0`</p><p> `Total-Records: 0`</p> |
   | [!UICONTROL **Column templates**] | When creating many data feeds, Adobe recommends creating a column template. Selecting a column template automatically includes the specified columns in the template. Adobe also provides several templates by default. |
   | [!UICONTROL **Available columns**] | All available data columns in Adobe Analytics. Click [!UICONTROL Add all] to include all columns in a data feed. |
   | [!UICONTROL **Included columns**] | The columns to include in a data feed. Click [!UICONTROL Remove all] to remove all columns from a data feed. |
   | [!UICONTROL **Download CSV**] | Downloads a CSV file containing all included columns. |

1. Select [!UICONTROL **Save**] in the top-right.

    Historical data processing begins immediately. When data finishes processing for a day, the file is sent to the destination that you configured.

    For information about how to access the data feed and to get a better understanding of its contents, see [Data feed contents - overview](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md).

## Legacy destinations

>[!IMPORTANT]
>
>The destinations described in this section are legacy, and are not recommended. Instead, use one of the following destinations when creating a data feed: Amazon S3, Google Cloud Platform, Azure RBAC, or Azure SAS. See [Create and configure a data feed](#create-and-configure-a-data-feed) for detailed information about each of these recommended destinations. 


The following information provides configuration information for each of the legacy destinations:

### FTP

Data feed data can be delivered to an Adobe or customer-hosted FTP location. Requires an FTP host, username, and password. Use the path field to place feed files in a folder. Folders must already exist; feeds throw an error if the specified path does not exist.

Use the following information when completing the available fields:

* [!UICONTROL **Host**]: Enter the desired FTP destination URL. For example, `ftp://ftp.omniture.com`.
* [!UICONTROL **Path**]: Can be left blank
* [!UICONTROL **Username**]: Enter the username to log in to the FTP site.
* [!UICONTROL **Password and confirm password**]: Enter the password to log in to the FTP site.

### SFTP

SFTP support for data feeds is available. Requires an SFTP host, username, and the destination site to contain a valid RSA or DSA public key. You can download the appropriate public key when creating the feed.

### S3

You can send feeds directly to Amazon S3 buckets. This destination type requires a Bucket name, an Access Key ID, and a Secret Key. See [Amazon S3 bucket naming requirements](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) within the Amazon S3 docs for more information.

The user you provide for uploading data feeds must have the following [permissions](https://docs.aws.amazon.com/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html):

* s3:GetObject
* s3:PutObject
* s3:PutObjectAcl

  >[!NOTE]
  >
  >For each upload to an Amazon S3 bucket, [!DNL Analytics] adds the bucket owner to the BucketOwnerFullControl ACL, regardless of whether the bucket has a policy that requires it. For more information, see "[What is the BucketOwnerFullControl setting for Amazon S3 data feeds?](df-faq.md#BucketOwnerFullControl)"

The following 16 standard AWS regions are supported (using the appropriate signature algorithm where necessary):

* us-east-2
* us-east-1
* us-west-1
* us-west-2
* ap-south-1
* ap-northeast-2
* ap-southeast-1
* ap-southeast-2
* ap-northeast-1
* ca-central-1
* eu-central-1
* eu-west-1
* eu-west-2
* eu-west-3
* eu-north-1
* sa-east-1

>[!NOTE]
>
>The cn-north-1 region is not supported.

### Azure Blob

Data feeds support Azure Blob destinations. Requires a container, account, and a key. Amazon automatically encrypts the data at rest. When you download the data, it gets decrypted automatically. See [Create a storage account](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) within the Microsoft Azure docs for more information.

>[!NOTE]
>
>You must implement your own process to manage disk space on the feed destination. Adobe does not delete any data from the server.

-->
