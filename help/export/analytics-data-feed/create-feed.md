---
title: Een gegevensfeed maken
description: Leer hoe u een gegevensfeed maakt.
feature: Data Feeds
exl-id: 36c8a40e-6137-4836-9d4b-bebf17b932bc
source-git-commit: f66cc6252ecd54c143c08be1e0e7e5bf90cc42e9
workflow-type: tm+mt
source-wordcount: '3156'
ht-degree: 1%

---

# Een gegevensfeed maken

Wanneer u een gegevensfeed maakt, biedt u Adobe de volgende informatie:

* De informatie over de bestemming waarnaar u Raw-gegevensbestanden wilt verzenden

* De gegevens die u in elk bestand wilt opnemen

>[!NOTE]
>
>Alvorens u een gegevensvoer creeert, is het belangrijk om een basisbegrip van gegevensvoer te hebben en dat u aan alle noodzakelijke voorwaarden voldoet. Zie voor meer informatie [Overzicht van gegevensfeeds](data-feed-overview.md).

## Een gegevensfeed maken en configureren

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. Selecteer het pictogram van 9 vierkante pixels rechtsboven en selecteer vervolgens [!UICONTROL **Analyse**].
1. Ga in de bovenste navigatiebalk naar [!UICONTROL **Beheer**] > [!UICONTROL **Gegevensfeeds**].
1. Selecteren [!UICONTROL **Toevoegen**].

   ![Gegevensfeed toevoegen](assets/datafeed-add.png)

   Er wordt een pagina weergegeven met drie hoofdcategorieën: [!UICONTROL **Diervoederinformatie**], [!UICONTROL **Doel**], en [!UICONTROL **Definities gegevenskolom**].
1. In de [!UICONTROL **Diervoederinformatie**] in, vult u de volgende velden in:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Naam**] | De naam van de gegevensinvoer. Moet uniek zijn binnen de geselecteerde rapportreeks, en kan tot 255 karakters in lengte zijn. |
   | [!UICONTROL **Rapportsuite**] | De rapportsuite waarop de gegevensinvoer is gebaseerd. Als de veelvoudige gegevensvoer voor de zelfde rapportreeks wordt gecreeerd, moeten zij verschillende kolomdefinities hebben. Alleen bronrapporten ondersteunen gegevensfeeds; virtuele rapportsuites worden niet ondersteund. |
   | [!UICONTROL **E-mail indien voltooid**] | Het e-mailadres dat moet worden gemeld wanneer een feed de verwerking heeft voltooid. Het e-mailadres moet correct zijn opgemaakt. |
   | [!UICONTROL **Feed-interval**] | Selecteren **Dagelijks** voor back-up of historische gegevens. De dagelijkse voer bevat een volledige waarde van de dag van gegevens, van middernacht aan middernacht in de tijdzone van de rapportreeks.  Selecteren **Uur** voor doorlopende gegevens (Daily is ook beschikbaar voor doorlopende feeds, indien gewenst). Uurfeeds bevatten gegevens van één uur. |
   | [!UICONTROL **Vertraging bij verwerking**] | Wacht een bepaalde hoeveelheid tijd alvorens een dossier van de gegevensvoer te verwerken. Een vertraging kan handig zijn om mobiele implementaties de mogelijkheid te geven om offlineapparaten online te komen en gegevens te verzenden. Het kan ook worden gebruikt om de server-zijprocessen van uw organisatie in het beheren van eerder verwerkte dossiers aan te passen. In de meeste gevallen is geen uitstel nodig. Een diervoeder kan maximaal 120 minuten worden uitgesteld. |
   | [!UICONTROL **Begin- en einddatum**] | De begindatum geeft de eerste datum aan waarop u gegevens wilt invoeren. Stel deze datum in het verleden in om onmiddellijk te beginnen met het verwerken van gegevensfeeds voor historische gegevens. De feeds worden verder verwerkt tot de einddatum. De begin en einddata zijn gebaseerd op de tijdzone van de rapportreeks. |
   | [!UICONTROL **Doorlopende diervoeders**] | Dit selectievakje verwijdert de einddatum, zodat een feed voor onbepaalde tijd kan worden uitgevoerd. Als een feed de verwerking van historische gegevens heeft voltooid, wacht een feed tot de gegevens een bepaald uur of een bepaalde dag zijn verzameld. Zodra het huidige uur of de dag eindigt, begint de verwerking na de gespecificeerde vertraging. |

1. In de [!UICONTROL **Doel**] in de [!UICONTROL **Type**] selecteert u het doel waarnaar u de gegevens wilt verzenden.

   ![Vervolgkeuzemenu bestemming gegevenfeed](assets/datafeed-destinations-dropdown.png)

   Gebruik een van de volgende doeltypen wanneer u een gegevensfeed maakt. Vouw voor configuratieinstructies het doeltype uit. (Extra [verouderde doelen](#legacy-destinations) zijn ook beschikbaar, maar worden niet aanbevolen.)

   +++Amazon S3

   U kunt feeds rechtstreeks naar Amazon S3-emmers verzenden. Voor dit doeltype is alleen uw Amazon S3-account en de locatie (bucket) vereist.

   Adobe Analytics gebruikt verificatie via meerdere accounts om bestanden van Adobe Analytics te uploaden naar de opgegeven locatie in uw Amazon S3-exemplaar.

   Een Amazon S3 emmertje als bestemming voor een gegevensvoer vormen:

   1. In de Adobe Analytics-beheerconsole, in de [!UICONTROL **Doel**] sectie, selecteert u [!UICONTROL **Amazon S3**].

      ![Amazon S3-bestemming](assets/datafeed-destination-amazons3.png)

   1. Selecteren [!UICONTROL **Locatie selecteren**].

      De pagina Amazon S3 Exportlocaties wordt weergegeven.

   1. (Voorwaardelijk) Als u eerder een Amazon S3-account en -locatie hebt toegevoegd:

      1. Selecteer de account in het menu [!UICONTROL **Account selecteren**] vervolgkeuzemenu.

      1. Selecteer de locatie in het menu [!UICONTROL **Locatie selecteren**] vervolgkeuzemenu.

      1. Selecteren [!UICONTROL **Opslaan**] > [!UICONTROL **Opslaan**].

         De bestemming wordt nu gevormd om gegevens naar de Amazon S3 plaats te verzenden die u specificeerde.

   1. (Voorwaardelijk) Als u nog geen Amazon S3-account hebt toegevoegd:

      1. Selecteren [!UICONTROL **Account toevoegen**] en geeft u de volgende informatie op:

         | Veld | -functie |
         |---------|----------|
         | [!UICONTROL **Accountnaam**] | Een naam voor de account. Dit kan elke gewenste naam zijn. |
         | [!UICONTROL **Accountbeschrijving**] | Een beschrijving voor de account. |
         | [!UICONTROL **Rol ARN**] | U moet een Rol ARN (de Naam van het Middel van Amazon) verstrekken die Adobe kan gebruiken om toegang tot de rekening van Amazon S3 te krijgen. Om dit te doen, creeert u een IAM toestemmingsbeleid voor de bronrekening, maakt het beleid aan een gebruiker vast, en creeert dan een rol voor de bestemmingsrekening. Zie voor specifieke informatie [deze AWS-documentatie](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |
         | [!UICONTROL **ARN gebruiker**] | De Gebruiker ARN (de Naam van het Middel van Amazon) wordt verstrekt door Adobe. U moet deze gebruiker aan het beleid vastmaken u creeerde. |

         {style="table-layout:auto"}

         1. Selecteren [!UICONTROL **Locatie toevoegen**] en geeft u de volgende informatie op:

         | Veld | -functie |
         |---------|----------|
         | [!UICONTROL **Naam**] | Een naam voor de account. |
         | [!UICONTROL **Beschrijving**] | Een beschrijving voor de account. |
         | [!UICONTROL **Emmertje**] | Het emmertje in uw Amazon S3-account waarin u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat de gebruiker-ARN die door Adobe is geleverd, toegang heeft om bestanden te uploaden naar dit emmertje. |
         | [!UICONTROL **Voorvoegsel**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |

         {style="table-layout:auto"}

      1. Selecteren [!UICONTROL **Maken**] > [!UICONTROL **Opslaan**].

         De bestemming wordt nu gevormd om gegevens naar de Amazon S3 plaats te verzenden die u specificeerde.

+++

   +++Azure RBAC

   Met RBAC-verificatie kunt u feeds rechtstreeks naar een Azure-container verzenden. Dit bestemmingstype vereist een naam van het Emmertje, een identiteitskaart van de Toepassing, identiteitskaart van de Aannemer, en een Geheime Sleutel.

   Om een Azure RBAC bucket als bestemming voor een gegevensvoer te vormen:

   1. Als u nog geen Azure-toepassing hebt, maakt u een Azure-toepassing die Adobe Analytics voor verificatie kan gebruiken en verleent u vervolgens toegangsmachtigingen in toegangsbeheer (IAM).

      Raadpleeg voor meer informatie de [Microsoft Azure-documentatie over het maken van een Azure Active Directory-toepassing](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal).

   1. In de Adobe Analytics-beheerconsole, in de [!UICONTROL **Doel**] sectie, selecteert u [!UICONTROL **Azure RBAC**].

      ![Azure RBAC-bestemming](assets/datafeed-destination-azurerbac.png)

   1. Selecteren [!UICONTROL **Locatie selecteren**].

      De pagina Azure RBAC Export Locations wordt weergegeven.

   1. (Voorwaardelijk) Als u eerder een Azure RBAC-account en -locatie hebt toegevoegd:

      1. Selecteer de account in het menu [!UICONTROL **Account selecteren**] vervolgkeuzemenu.

      1. Selecteer de locatie in het menu [!UICONTROL **Locatie selecteren**] vervolgkeuzemenu.

      1. Selecteren [!UICONTROL **Opslaan**] > [!UICONTROL **Opslaan**].

         De bestemming wordt nu gevormd om gegevens naar de Azure plaats te verzenden RBAC die u specificeerde.

   1. (Voorwaardelijk) Als u nog geen Azure RBAC-account hebt toegevoegd:

      1. Selecteren [!UICONTROL **Account toevoegen**] en geeft u de volgende informatie op:

         | Veld | -functie |
         |---------|----------|
         | [!UICONTROL **Accountnaam**] | Een naam voor de Azure RBAC-account. Deze naam wordt weergegeven in het dialoogvenster [!UICONTROL **Account selecteren**] en kan elke gewenste naam hebben. |
         | [!UICONTROL **Accountbeschrijving**] | Een beschrijving voor de Azure RBAC-account. Deze beschrijving wordt weergegeven in het dialoogvenster [!UICONTROL **Account selecteren**] en kan elke gewenste naam hebben. |
         | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Geheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

         {style="table-layout:auto"}

      1. Selecteren [!UICONTROL **Locatie toevoegen**] en geeft u de volgende informatie op:

         | Veld | -functie |
         |---------|----------|
         | [!UICONTROL **Naam**] | Een naam voor de locatie. Deze naam wordt weergegeven in het dialoogvenster [!UICONTROL **Locatie selecteren**] en kan elke gewenste naam hebben. |
         | [!UICONTROL **Beschrijving**] | Een beschrijving voor de locatie. Deze beschrijving wordt weergegeven in het dialoogvenster [!UICONTROL **Locatie selecteren**] en kan elke gewenste naam hebben. |
         | [!UICONTROL **Account**] | De Azure-opslagaccount. |
         | [!UICONTROL **Container**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat u machtigingen verleent om bestanden te uploaden naar de Azure-toepassing die u eerder hebt gemaakt. |
         | [!UICONTROL **Voorvoegsel**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |

         {style="table-layout:auto"}

      1. Selecteren [!UICONTROL **Maken**] > [!UICONTROL **Opslaan**].

         De bestemming wordt nu gevormd om gegevens naar de Azure plaats te verzenden RBAC die u specificeerde.

+++

   +++Azure SAS

   Met SAS-verificatie kunt u feeds rechtstreeks naar een Azure-container verzenden. Dit doeltype vereist een naam van het Emmertje, een toepassings-id, een huurnummer-id, de sleutelvault-URI, de geheime naam van de sleutelkluis en een geheime sleutel.

   Om een Azure SAS bucket als bestemming voor een gegevensvoer te vormen:

   1. Als u dat nog niet hebt gedaan, maakt u een Azure-toepassing die Adobe Analytics voor verificatie kan gebruiken.

      Raadpleeg voor meer informatie de [Microsoft Azure-documentatie over het maken van een Azure Active Directory-toepassing](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal).

   1. In de Adobe Analytics-beheerconsole, in de [!UICONTROL **Doel**] sectie, selecteert u [!UICONTROL **Azure SAS**].

      ![Azure SAS-bestemming](assets/datafeed-destination-azuresas.png)

   1. Selecteren [!UICONTROL **Locatie selecteren**].

      De Azure SAS Export Locations-pagina wordt weergegeven.

   1. (Voorwaardelijk) Als u eerder een Azure SAS-account en -locatie hebt toegevoegd:

      1. Selecteer de account in het menu [!UICONTROL **Account selecteren**] vervolgkeuzemenu.

      1. Selecteer de locatie in het menu [!UICONTROL **Locatie selecteren**] vervolgkeuzemenu.

      1. Selecteren [!UICONTROL **Opslaan**] > [!UICONTROL **Opslaan**].

         De bestemming is nu geconfigureerd voor het verzenden van gegevens naar de door u opgegeven Azure SAS-locatie.

   1. (Voorwaardelijk) Als u nog geen Azure SAS-account hebt toegevoegd:

      1. Selecteren [!UICONTROL **Account toevoegen**] en geeft u de volgende informatie op:

         | Veld | -functie |
         |---------|----------|
         | [!UICONTROL **Accountnaam**] | Een naam voor de Azure SAS-account. Deze naam wordt weergegeven in het dialoogvenster [!UICONTROL **Account selecteren**] en kan elke gewenste naam hebben. |
         | [!UICONTROL **Afschrijving van account**] | Een beschrijving voor de Azure SAS-account. Deze beschrijving wordt weergegeven in het dialoogvenster [!UICONTROL **Account selecteren**] en kan elke gewenste naam hebben. |
         | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **URI sleutelvault**] | <p>Het pad naar het SAS-token in Azure Key Vault.  Om Azure SAS te configureren, moet u een SAS-token opslaan als een geheim met Azure Key Vault. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nadat de sleutelvault-URI is gemaakt, voegt u een toegangsbeleid toe aan de Key Vault om toestemming te verlenen aan de Azure-toepassing die u hebt gemaakt. Zie voor meer informatie de [Microsoft Azure-documentatie over het toewijzen van een beleid voor toegang tot Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
         | [!UICONTROL **geheime naam sleutelvault**] | De geheime naam die u hebt gemaakt toen u het geheim toevoegde aan Azure Key Vault. In Microsoft Azure vindt u deze informatie in de Key Vault die u hebt gemaakt, op de **Key Vault** instellingenpagina&#39;s. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
         | [!UICONTROL **Geheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

         {style="table-layout:auto"}

      1. Selecteren [!UICONTROL **Locatie toevoegen**] en geeft u de volgende informatie op:

         | Veld | -functie |
         |---------|----------|
         | [!UICONTROL **Naam**] | Een naam voor de locatie. Deze naam wordt weergegeven in het dialoogvenster [!UICONTROL **Locatie selecteren**] en kan elke gewenste naam hebben. |
         | [!UICONTROL **Beschrijving**] | Een beschrijving voor de locatie. Deze beschrijving wordt weergegeven in het dialoogvenster [!UICONTROL **Locatie selecteren**] en kan elke gewenste naam hebben. |
         | [!UICONTROL **Container**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. |
         | [!UICONTROL **Voorvoegsel**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |

         {style="table-layout:auto"}

      1. Selecteren [!UICONTROL **Maken**] > [!UICONTROL **Opslaan**].

         De bestemming is nu geconfigureerd voor het verzenden van gegevens naar de door u opgegeven Azure SAS-locatie.

+++

   +++Google Cloud Platform

   U kunt feeds rechtstreeks naar de emmers van het Google Cloud Platform (GCP) verzenden. Voor dit doeltype zijn alleen de naam van uw GCP-account en de naam van de locatie (emmertje) vereist.

   Adobe Analytics gebruikt verificatie voor meerdere accounts om bestanden van Adobe Analytics naar de opgegeven locatie in uw GCP-exemplaar te uploaden.

   Om een emmertje GCP als bestemming voor een gegevensvoer te vormen:

   1. In de Adobe Analytics-beheerconsole, in de [!UICONTROL **Doel**] sectie, selecteert u [!UICONTROL **Google Cloud Platform**].

      ![Doel Google Cloud-Platform](assets/datafeed-destination-gcp.png)

   1. Selecteren [!UICONTROL **Locatie selecteren**].

      De pagina GCP-exportlocaties wordt weergegeven.

   1. (Voorwaardelijk) Als u eerder een GCP-account en -locatie hebt toegevoegd:

      1. Selecteer de account in het menu [!UICONTROL **Account selecteren**] vervolgkeuzemenu.

      1. Selecteer de locatie in het menu [!UICONTROL **Locatie selecteren**] vervolgkeuzemenu.

      1. Selecteren [!UICONTROL **Opslaan**] > [!UICONTROL **Opslaan**].

         De bestemming wordt nu gevormd om gegevens naar de plaats te verzenden GCP die u specificeerde.

   1. (Voorwaardelijk) Als u nog geen GCP-account hebt toegevoegd:

      1. Selecteren [!UICONTROL **Account toevoegen**] en geeft u de volgende informatie op:

         | Veld | -functie |
         |---------|----------|
         | [!UICONTROL **Accountnaam**] | Een naam voor de account. Dit kan elke gewenste naam zijn. |
         | [!UICONTROL **Accountbeschrijving**] | Een beschrijving voor de account. |
         | [!UICONTROL **Project-id**] | Uw Google Cloud-project-id. Zie de [Google Cloud-documentatie over het ophalen van een project-id](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |
         | [!UICONTROL **Opdrachtgever**] | De Opdrachtgever wordt geleverd door Adobe. U moet toestemming aan dit hoofd verlenen om voer te ontvangen. Zie de [Google Cloud-documentatie over het toevoegen van een principal aan een beleid](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-iam). |

         {style="table-layout:auto"}

         1. Selecteren [!UICONTROL **Locatie toevoegen**] en geeft u de volgende informatie op:

         | Veld | -functie |
         |---------|----------|
         | [!UICONTROL **Opdrachtgever**] | De Opdrachtgever wordt geleverd door Adobe. U moet toestemming verlenen om voer naar dit hoofd te ontvangen. |
         | [!UICONTROL **Naam**] | Een naam voor de account. |
         | [!UICONTROL **Beschrijving**] | Een beschrijving voor de account. |
         | [!UICONTROL **Emmertje**] | Het emmertje binnen uw GCP rekening waar u de gegevens van Adobe Analytics wilt worden verzonden. Zorg ervoor dat u aan Opdrachtgever toestemming hebt verleend die door Adobe wordt verstrekt om dossiers aan dit emmertje te uploaden. |
         | [!UICONTROL **Voorvoegsel**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |

         {style="table-layout:auto"}

      1. Selecteren [!UICONTROL **Maken**] > [!UICONTROL **Opslaan**].

         De bestemming wordt nu gevormd om gegevens naar de plaats te verzenden GCP die u specificeerde.

+++

1. In de  [!UICONTROL **Definities gegevenskolom**] sectie selecteert u de meest recente [!UICONTROL **Alle Adobe Columns**] in het vervolgkeuzemenu en vul vervolgens de volgende velden in:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Te verwijderen tekens verwijderen**] | Bij het verzamelen van gegevens kunnen sommige tekens (zoals nieuwe regels) problemen veroorzaken. Schakel dit selectievakje in als u deze tekens uit feed-bestanden wilt verwijderen. |
   | [!UICONTROL **Compressie-indeling**] | Het type compressie dat wordt gebruikt. **Gzip** bestanden uitvoeren in `.tar.gz` gebruiken. **Postcode** bestanden uitvoeren in `.zip` gebruiken. |
   | [!UICONTROL **Verpakkingstype**] | Selecteren **Meerdere bestanden** voor de meeste gegevensfeeds. Met deze optie worden uw gegevens gepagineerd in ongecomprimeerde 2GB-blokken. (Als er meerdere bestanden zijn geselecteerd en de niet-gecomprimeerde gegevens voor het rapportagevenster kleiner zijn dan 2 GB, wordt er één bestand verzonden.) Selecteren **Eén bestand** output de `hit_data.tsv` bestand in één, mogelijk enorm bestand. |
   | [!UICONTROL **Manifest**] | Of Adobe een [manifestbestand](c-df-contents/datafeeds-contents.md#feed-manifest) naar de bestemming wanneer geen gegevens voor een voederinterval worden verzameld. Als u **Manifest-bestand** ontvangt u een manifestbestand dat lijkt op het volgende wanneer er geen gegevens worden verzameld:<p>`text`</p><p>`Datafeed-Manifest-Version: 1.0`</p><p>`Lookup-Files: 0`</p><p>`Data-Files: 0`</p><p> `Total-Records: 0`</p> |
   | [!UICONTROL **Kolomsjablonen**] | Adobe raadt u aan een kolomsjabloon te maken wanneer u veel gegevensfeeds maakt. Als u een kolomsjabloon selecteert, worden automatisch de opgegeven kolommen in de sjabloon opgenomen. Adobe biedt standaard ook diverse sjablonen. |
   | [!UICONTROL **Beschikbare kolommen**] | Alle beschikbare gegevenskolommen in Adobe Analytics. Klikken [!UICONTROL Add all] om alle kolommen in een gegevenstoevoer op te nemen. |
   | [!UICONTROL **Opgenomen kolommen**] | De kolommen die in een gegevensfeed moeten worden opgenomen. Klikken [!UICONTROL Remove all] om alle kolommen uit een gegevensvoer te verwijderen. |
   | [!UICONTROL **CSV downloaden**] | Hiermee wordt een CSV-bestand gedownload dat alle kolommen bevat. |

1. Selecteren [!UICONTROL **Opslaan**] in de rechterbovenhoek.

   Historische gegevensverwerking begint onmiddellijk. Wanneer de gegevens verwerking voor een dag beëindigen, wordt het dossier verzonden naar de bestemming die u vormde.

   Voor informatie over hoe te om tot de gegevensvoer toegang te hebben en een beter inzicht in zijn inhoud te krijgen, zie [Inhoud gegevensfeed - overzicht](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md).

## Oudere bestemmingen

>[!IMPORTANT]
>
>De doelen die in deze sectie worden beschreven, zijn verouderd en worden niet aanbevolen. Gebruik in plaats daarvan een van de volgende doelen bij het maken van een gegevensfeed: Amazon S3, Google Cloud Platform, Azure RBAC of Azure SAS. Zie [Een gegevensfeed maken en configureren](#create-and-configure-a-data-feed) voor gedetailleerde informatie over elk van deze aanbevolen bestemmingen.


De volgende informatie verstrekt configuratieinformatie voor elk van de erfenisbestemmingen:

### FTP

Gegevens over gegevenstoevoer kunnen naar een door de Adobe of klant gehoste FTP-locatie worden verzonden. Vereist een FTP-host, gebruikersnaam en wachtwoord. Gebruik het padveld om feed-bestanden in een map te plaatsen. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat.

Gebruik de volgende informatie wanneer u de beschikbare velden invult:
* [!UICONTROL **Host**]: Voer de gewenste FTP-doel-URL in. Bijvoorbeeld, `ftp://ftp.omniture.com`.
* [!UICONTROL **Pad**]: Kan leeg blijven
* [!UICONTROL **Gebruikersnaam**]: Voer de gebruikersnaam in die u wilt aanmelden bij de FTP-site.
* [!UICONTROL **Wachtwoord en wachtwoord bevestigen**]: Voer het wachtwoord in om u aan te melden bij de FTP-site.

### SFTP

SFTP-ondersteuning voor gegevensfeeds is beschikbaar. Vereist een gastheer SFTP, gebruikersbenaming, en de bestemmingsplaats om een geldige RSA of DSA openbare sleutel te bevatten. U kunt de juiste openbare sleutel downloaden wanneer u de feed maakt.

### S3

U kunt feeds rechtstreeks naar Amazon S3-emmers verzenden. Dit bestemmingstype vereist een naam van het Emmertje, een Zeer belangrijke identiteitskaart van de Toegang, en een Geheime Sleutel. Zie [Amazon S3-vereisten voor emmernaamgeving](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) in de Amazon S3-documenten voor meer informatie.

De gebruiker die u opgeeft voor het uploaden van gegevensfeeds, moet het volgende hebben [machtigingen](https://docs.aws.amazon.com/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html):

* s3:GetObject
* s3:PutObject
* s3:PutObjectAcl

  >[!NOTE]
  >
  >Voor elke upload naar een Amazon S3 emmertje, [!DNL Analytics] voegt de emmereigenaar aan BucketOwnerFullControl ACL toe, al dan niet het emmertje een beleid heeft dat het vereist. Zie voor meer informatie &quot;[Wat is de instelling BucketOwnerFullControl voor Amazon S3-gegevensfeeds?](df-faq.md#BucketOwnerFullControl)&quot;

De volgende 16 standaard AWS-gebieden worden ondersteund (waarbij zo nodig het juiste handtekeningalgoritme wordt gebruikt):

* us-East-2
* us-East-1
* us-west-1
* us-west-2
* ap-zuid-1
* ap-northeast-2
* ap-zuidoost-1
* ap-zuidoost-2
* ap-northeast-1
* ca-centraal-1
* EU-centraal-1
* EU-west-1
* EU-west-2
* eu-west-3
* eu-noord-1
* sa-Oost-1

>[!NOTE]
>
>De regio cn-North-1 wordt niet ondersteund.

### Azure Blob

Data feeds ondersteunen Azure Blob-bestemmingen. Hiervoor is een container, account en sleutel vereist. Amazon versleutelt de gegevens automatisch in rust. Wanneer u de gegevens downloadt, worden deze automatisch gedecodeerd. Zie [Een opslagaccount maken](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in de Microsoft Azure-documenten voor meer informatie.

>[!NOTE]
>
>U moet uw eigen proces uitvoeren om schijfruimte op de voederbestemming te beheren. Adobe verwijdert geen gegevens van de server.
