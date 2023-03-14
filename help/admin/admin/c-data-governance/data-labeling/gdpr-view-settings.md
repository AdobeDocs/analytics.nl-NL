---
description: Het dialoogvenster Privacy Labeling for Data Governance biedt een overzicht van de privacylabels en naamruimten van een rapportsuite. U kunt de instellingen vanaf hier ook exporteren naar een CSV-bestand.
title: Privacy-labels voor gegevensbeheer weergeven/beheren
feature: Data Governance
exl-id: 87b0be42-1098-4e72-8eb8-0c1bb56791f8
source-git-commit: 0f5a1e7264b194b368731f612a04bb805740a932
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 38%

---

# Privacy-labels voor gegevensbeheer weergeven/beheren

De **[!UICONTROL Privacy Labeling for Data Governance]** biedt een overzicht van de privacylabels en naamruimten van een rapportsuite. U kunt de instellingen vanaf hier ook exporteren naar een CSV-bestand.

## Privacy-labels weergeven {#view-privacy}

1. Meld u aan bij Adobe Experience Cloud.
2. Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Data configuration & collection]** > **[!UICONTROL Data Governance]**.

   >[!NOTE]
   >
   >Als dit menu-item niet zichtbaar is, moet u deze toevoegen aan een [productprofiel in Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/product-profile.html) met machtigingen voor deze functionaliteit.

3. Selecteer rechtsboven een rapportsuite waarvan u de privacylabels wilt weergeven of beheren.

![](assets/privacy_labeling.png)

| Instelling | Beschrijving |
| --- | --- |
| **[!UICONTROL Component Name]** | Deze kolom maakt een lijst van alle componenten (afmetingen, metriek) die deel van deze rapportreeks uitmaken. |
| **[!UICONTROL Identity]** | “I”-labels voor identiteitsdata worden gebruikt om data te categoriseren waarmee een specifieke persoon kan worden geïdentificeerd of gecontacteerd. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#data-privacy-identity-labels) |
| **[!UICONTROL Sensitivity]** | “S”-labels voor gevoelige data worden gebruikt om gevoelige data zoals geografische data te categoriseren. In de toekomst zullen extra labels voor gevoelige data worden geïntroduceerd om andere soorten gevoelige informatie te identificeren. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#sensitive-data-labels) |
| **[!UICONTROL GDPR Access]** | Met Data Governance-labels kunnen gebruikers data classificeren die privacygerelateerde overwegingen en contractuele voorwaarden vertegenwoordigen waardoor deze voldoen aan regelgeving en bedrijfsbeleid. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#data-privacy-access-labels) |
| **[!UICONTROL GDPR Delete]** | Een label Verwijderen is alleen vereist voor velden die een waarde bevatten waarmee een treffer aan het gegevensonderwerp kan worden gekoppeld (zodat het gegevensonderwerp kan worden geïdentificeerd). [Meer informatie](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#data-privacy-delete-labels) |
| **[!UICONTROL Namespace]** | Wanneer u een variabele als ID-DEVICE of ID-PERSON labelt, wordt u gevraagd om een naamruimte op te geven. U kunt een eerder gedefinieerde naamruimte gebruiken of een nieuwe naamruimte definiëren. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#provide-namespace) |
| **[!UICONTROL Category]** | Verwijst naar type component, zoals standaardcomponent, conversievariabele, enz. |

{style="table-layout:auto"}

## Privacy-labels kopiëren naar een rapportsuite  {#copy-to-rs}

Voer de volgende stappen uit als u dezelfde privacyinstellingen voor gegevens wilt toepassen op meerdere rapportsuite:

1. Selecteer de variabele die u wilt kopiëren. Let erop dat u de labels voor één variabele tegelijk kunt kopiëren.
1. Klikken **[!UICONTROL Copy to Report Suite(s)]** onder aan de dialoog over gegevensbeheer.

   ![Kopiëren naar rapportsuite](assets/copy_to_reportsuite.png)

1. Het resulterende scherm toont de variabelenaam, de momenteel toegepaste labels die u wilt kopiëren, de rapportsuites en hun id&#39;s en of de instellingen in de doelrapportsuites overeenkomen.

   ![Label kopiëren naar rapportsuite](assets/copy_to_rs.png)

   >[!IMPORTANT]
   >
   >Houd in mening dat alle rapportsuites u selecteert aan uw organisatie van de Experience Cloud moet worden in kaart gebracht.

   Wanneer u de labels voor een variabele of een reeks variabelen naar een andere rapportsuite kopieert, gaat de kopie naar de variabele in de overeenkomstige positie doelrapportsuite. Voor Standaardcomponenten, de Variabelen van de Lijst, en de Gebeurtenissen van het Succes, zullen de etiketten aan de variabele met worden gekopieerd **dezelfde naam** in de reeks van het bestemmingsrapport.

   Voor Conversievariabelen (eVars) en Dimension verkeer (props) gaat de kopie echter naar de variabele met de component **zelfde nummer** in de reeks van het bestemmingsrapport. eVar12 wordt bijvoorbeeld gekopieerd naar eVar12 in alle doelrapportsuites. De namen van deze variabelen worden genegeerd bij het bepalen van het doel van de kopie. Als de overeenkomstige variabele niet is ingeschakeld in de doelrapportsuite, zal het kopiëren van die variabele mislukken.

   Bij het kopiëren van de labels voor classificaties die zijn gedefinieerd voor een variabele, worden de labels gekopieerd naar een classificatie op de corresponderende variabele in de doelrapportsuite (zoals eVar7 naar eVar7) die dezelfde naam heeft als de gekopieerde classificatie. Anders zal het kopiëren voor de labels van die classificatie mislukken.

1. Schakel het vakje naast een of meer rapportsuites in waar de instellingen overeenkomen.
1. Klik op **[!UICONTROL Apply]**.

   Er wordt een statusbericht weergegeven nadat een label is toegepast. Het statusbericht bevat de namen van bestemmingsvariabelen of classificaties en hun rapportsuites waarvoor het kopiëren is mislukt.

   >[!IMPORTANT]
   >
   >Controleer altijd de suites van het doelrapport om ervoor te zorgen dat de etiketten correct hebben gekopieerd. Dit is vooral belangrijk voor variabelen met ID- of DEL-labels.

## Exporteren naar een CSV-bestand {#export-csv}

U kunt een CSV-bestand downloaden met alle huidige labeldefinities voor alle variabelen voor de geselecteerde rapportsuite(s). We adviseren dat uw juridische team uw labelkeuzes controleert, en deze optie maakt die controle mogelijk. U kunt het CSV-bestand met het team delen, zodat ze de controle niet hoeven uit te voeren terwijl ze zijn aangemeld bij de Data Governance-gebruikersinterface.

1. Klikken **[!UICONTROL Export CSV]** rechtsboven in het dialoogvenster wordt het volgende weergegeven:

   ![](assets/export_csv.png)

1. Selecteer één of meerdere rapportreeksen waarvoor u alle montages van het gegevensbeheer wilt uitvoeren.

## Privacy-labels bewerken {#edit}

Zie [Privacylabels voor rapportsuite toewijzen of bewerken](/help/admin/admin/c-data-governance/data-labeling/gdpr-setup-reportsuite.md).
