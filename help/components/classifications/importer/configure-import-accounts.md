---
description: De cloud-importaccount configureren en de locatie waar classificatiegegevens kunnen worden geüpload
keywords: Analysis Workspace
title: Cloudimportlocaties configureren
feature: Classifications
source-git-commit: 8d6ee33e867da274334c8adc557105af4942c894
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 1%

---

# Cloudimportlocaties configureren

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

Voordat u Adobe Analytics-classificatiegegevens kunt importeren vanuit een cloudbestemming, moet u de locatie toevoegen en configureren waar u de classificatiegegevens wilt verzamelen.

Dit proces bestaat uit het toevoegen en configureren van de account (zoals Amazon S3 Role ARN, Google Cloud Platform enzovoort) en de locatie binnen de account (zoals een map binnen de account).

## Een account toevoegen

U moet Adobe Analytics configureren met de benodigde informatie voor toegang tot uw bestemmingsaccount voor de cloud.

1. Selecteer in Adobe Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Locaties**].
1. Op de [!UICONTROL Locations] pagina, selecteert u de [!UICONTROL **Locatiereferenties**] tab.
1. Selecteren [!UICONTROL **Account toevoegen**]. <!-- add screenshot? -->

   Het dialoogvenster Account toevoegen wordt weergegeven.
1. Geef de volgende informatie op: |Veld | Functie | |—|—| | [!UICONTROL **Naam van locatieaccount**] | De naam van de locatieaccount. Deze naam wordt weergegeven wanneer u een locatie maakt | | [!UICONTROL **Beschrijving van locatieaccount**] | Geef een korte beschrijving van de rekening om deze te kunnen onderscheiden van andere rekeningen van hetzelfde type. | | [!UICONTROL **Accounttype**] | Selecteer het type cloudaccount. We raden u aan voor elk accounttype één account te hebben, met meerdere locaties binnen dat account. |
1. In de [!UICONTROL **Accounteigenschappen**] in, geeft u specifieke informatie op over het accounttype dat u hebt geselecteerd.

   Vouw voor configuratieinstructies de sectie hieronder uit die overeenkomt met de [!UICONTROL **Accounttype**] die u hebt geselecteerd.

   +++Amazon S3 Role ARN

   Geef de volgende informatie op om een Amazon S3 Role ARN-account te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Rol ARN**] | U moet een Rol ARN (de Naam van het Middel van Amazon) verstrekken die Adobe kan gebruiken om toegang tot de rekening van Amazon S3 te krijgen. Om dit te doen, creeert u een IAM toestemmingsbeleid voor de bronrekening, maakt het beleid aan een gebruiker vast, en creeert dan een rol voor de bestemmingsrekening. Zie voor specifieke informatie [deze AWS-documentatie](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |
   | [!UICONTROL **ARN gebruiker**] | De Gebruiker ARN (de Naam van het Middel van Amazon) wordt verstrekt door Adobe. U moet deze gebruiker aan het beleid vastmaken u creeerde. |

   {style="table-layout:auto"}

+++

   +++Google Cloud Platform

   Geef de volgende informatie op om een Google Cloud Platform-account te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Project-id**] | Uw Google Cloud-project-id. Zie de [Google Cloud-documentatie over het ophalen van een project-id](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |

   {style="table-layout:auto"}

+++

   +++Azure SAS

   Geef de volgende informatie op om een Azure SAS-account te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **URI sleutelvault**] | <p>Het pad naar het SAS-token in Azure Key Vault.  Om Azure SAS te configureren, moet u een SAS-token opslaan als een geheim met Azure Key Vault. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nadat de sleutelvault-URI is gemaakt, voegt u een toegangsbeleid toe aan de Key Vault om toestemming te verlenen aan de Azure-toepassing die u hebt gemaakt. Zie voor meer informatie de [Microsoft Azure-documentatie over het toewijzen van een beleid voor toegang tot Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
   | [!UICONTROL **geheime naam sleutelvault**] | De geheime naam die u hebt gemaakt toen u het geheim toevoegde aan Azure Key Vault. In Microsoft Azure vindt u deze informatie in de Key Vault die u hebt gemaakt, op de **Key Vault** instellingenpagina&#39;s. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
   | [!UICONTROL **Locatierekeninggeheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

   {style="table-layout:auto"}

+++

   +++Azure RBAC

   Geef de volgende informatie op om een Azure RBAC-account te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **Locatierekeninggeheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie voor meer informatie de [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft-identiteitsplatform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

   {style="table-layout:auto"}

+++

1. Selecteren [!UICONTROL **Opslaan**].

1. Doorgaan met [Een locatie toevoegen](#add-a-location).

## Een locatie toevoegen

1. U moet een account toevoegen voordat u een locatie kunt toevoegen. [Een account toevoegen](#add-an-account) als je dat nog niet hebt gedaan.
1. Selecteer in Adobe Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Locaties**].
1. Op de [!UICONTROL Locations] pagina, selecteert u de [!UICONTROL **Locaties**] tab.
1. Selecteren [!UICONTROL **Locatie toevoegen**]. <!-- add screenshot? -->

   Het dialoogvenster Locatie wordt weergegeven.
1. Geef de volgende informatie op: |Veld | Functie | |—|—| | [!UICONTROL **Naam**] | De naam van de locatie.  | | [!UICONTROL **Beschrijving**] | Geef een korte beschrijving van de rekening om deze te kunnen onderscheiden van andere rekeningen van hetzelfde type. | | [!UICONTROL **Locatieaccount**] | Selecteer de locatie-account waarin u hebt gemaakt [Een account toevoegen](#add-an-account). |

1. In de [!UICONTROL **Locatie-eigenschappen**] in, geeft u specifieke informatie op over het accounttype van uw locatieaccount.

   Vouw voor configuratieinstructies de sectie hieronder uit die overeenkomt met het accounttype dat u in het dialoogvenster [!UICONTROL **Locatieaccounts**] veld.

   +++Amazon S3 Role ARN

   Geef de volgende informatie op om een ARN-locatie voor Amazon S3 Role te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Naam van emmertje**] | Het emmertje in uw Amazon S3-account waarin u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat de gebruiker-ARN die door Adobe is geleverd, toegang heeft om bestanden te uploaden naar dit emmertje. |
   | [!UICONTROL **Voorvoegsel toets**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

+++

   +++Google Cloud Platform

   Geef de volgende informatie op om een locatie voor een Google Cloud-Platform te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Naam van emmertje**] | Het emmertje binnen uw GCP rekening waar u de gegevens van Adobe Analytics wilt worden verzonden. Zorg ervoor dat u aan Opdrachtgever toestemming hebt verleend die door Adobe wordt verstrekt om dossiers aan dit emmertje te uploaden. |
   | [!UICONTROL **Voorvoegsel toets**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

+++

   +++Azure SAS

   Geef de volgende informatie op om een Azure SAS-locatie te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Containernaam**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. |
   | [!UICONTROL **Voorvoegsel toets**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |

   {style="table-layout:auto"}

+++

   +++Azure RBAC

   Geef de volgende informatie op om een Azure RBAC-locatie te configureren:

   | Veld | -functie |
   |---------|----------|
   | [!UICONTROL **Containernaam**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat u machtigingen verleent om bestanden te uploaden naar de Azure-toepassing die u eerder hebt gemaakt. |
   | [!UICONTROL **Voorvoegsel toets**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |
   | [!UICONTROL **Accountnaam**] | De Azure-opslagaccount. |

   {style="table-layout:auto"}

+++

1. Selecteren [!UICONTROL **Opslaan**].

   U kunt nu gegevens importeren naar de account en locatie die u hebt geconfigureerd.