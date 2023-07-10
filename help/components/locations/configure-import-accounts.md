---
description: De cloud-importaccount configureren en de locatie waar classificatiegegevens kunnen worden geüpload
keywords: Analysis Workspace
title: Cloud-importaccounts configureren
feature: Classifications
source-git-commit: 4efb0623d734419c376ca5f2bf2bbd94097ee4e4
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# Cloud-importaccounts configureren

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

Voordat u Adobe Analytics-classificatiegegevens kunt importeren vanuit een cloudbestemming, moet u de account en de locatie binnen die account toevoegen en configureren waar u de classificatiegegevens wilt verzamelen.

Dit proces bestaat uit het toevoegen en configureren van de account (zoals Amazon S3 Role ARN, Google Cloud Platform enzovoort) zoals beschreven in dit artikel, en het toevoegen en configureren van de locatie binnen die account (zoals een map binnen de account) zoals beschreven in [Cloudimportlocaties configureren][/help/components/locations/configure-import-locations.md].

U moet Adobe Analytics configureren met de benodigde informatie voor toegang tot uw bestemmingsaccount voor de cloud.

Een cloud-importaccount configureren:

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

1. Doorgaan met [Cloudimportlocaties configureren](/help/components/locations/configure-import-locations.md).

