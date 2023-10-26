---
description: De cloud-importaccount configureren en de locatie waar classificatiegegevens kunnen worden geüpload
keywords: Analysis Workspace
title: Cloudimportlocaties configureren
feature: Classifications
exl-id: 55179868-6228-44ff-835c-f4a7b38e929b
source-git-commit: c43d7bbdad0ad0265e038ee273c74bec136f1c72
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 1%

---

# Cloudimportlocaties configureren

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

Voordat u Adobe Analytics-classificatiegegevens kunt importeren vanuit een cloudbestemming, moet u de account en de locatie binnen die account toevoegen en configureren waar u de classificatiegegevens wilt verzamelen.

Dit proces bestaat uit het toevoegen en configureren van de account (zoals Amazon S3 Role ARN, Google Cloud Platform enzovoort) en de locatie binnen de account (zoals een map binnen de account).

Een locatie voor cloudimport configureren:

1. U moet een account toevoegen voordat u een locatie kunt toevoegen. Voeg een account toe zoals beschreven in [Cloud-importaccounts configureren](/help/components/locations/configure-import-accounts.md).
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
   | [!UICONTROL **Naam van emmertje**] | Het emmertje in uw Amazon S3-account waarin u Adobe Analytics-gegevens wilt verzenden. |
   | [!UICONTROL **Voorvoegsel toets**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

+++

   +++Google Cloud Platform

   Geef de volgende informatie op om een locatie voor een Google Cloud Platform te configureren:

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
