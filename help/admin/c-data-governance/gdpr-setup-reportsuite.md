---
description: Het labelen van rapportsuitedata betekent dat u labels voor identiteit, gevoeligheid en data-governance toevoegt aan elke variabele in een bepaalde rapportsuite.
title: Rapportsuitedata labelen
feature: Data Governance
exl-id: d1bd833c-3fd4-4572-a5dc-d7bab8a79cb8
source-git-commit: 25eccb2b9fe3827e62b0ae98d9bebf7a97b239f5
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 97%

---

# Rapportsuitedata labelen

Het labelen van rapportsuitedata betekent dat u labels voor identiteit, gevoeligheid en data-governance toevoegt aan elke variabele in een bepaalde rapportsuite. Zorg ervoor dat u zich eerst vertrouwd maakt met de labels en de bijbehorende definities.

>[!NOTE]
>
>Bedenk dat de labels steeds moeten worden gecontroleerd wanneer een nieuwe rapportsuite wordt gemaakt of wanneer een nieuwe variabele in een bestaande rapportsuite wordt ingeschakeld. U dient de labeling mogelijk ook te herzien wanneer integraties van nieuwe oplossingen worden ingeschakeld, omdat deze nieuwe variabelen kunnen laten zien waarvoor een label nodig is. Een herimplementatie van uw mobiele apps of websites kan de manier veranderen waarop bestaande variabelen worden gebruikt, waardoor eveneens updates van labels nodig kunnen zijn.

## Rapportsuitelabels toewijzen of bewerken {#section_39F829F35A274EACA532E2F6FF392996}

**Voorbeeld**: Als datacontroller wilt u e-mailadressen en cookie-id&#39;s verzamelen geregistreerde personen om hun Data Privacy-aanvragen te verwerken. Deze cookie-id&#39;s worden opgeslagen in een rapportsuite in Adobe Analytics. Als u een label voor e-mailadressen en cookie-id&#39;s wilt maken, moet u het DULE-kader (Data Usage Labeling &amp; Enforcement) van Adobe Cloud Platform in Analytics gebruiken.

1. Ga in Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL Data Governance]** > **[!UICONTROL (select report suite)]** ![Privacy-instellingen](assets/privacy_rs_settings.png)

1. Selecteer welke groep variabelen u wilt labelen.

   ![Variabelen](assets/variables.png)

   * **Standaarddimensies** (kant-en-klare Adobe Analytics-dimensies)
   * **Standaardcijfers** (kant-en-klare Adobe Analytics-cijfers)
   * **Conversiegebeurtenissen** (aangepaste succesgebeurtenissen)
   * **Merchandising-conversiedimensies** (Merchandising-eVars)
   * **Conversiedimensies** (non-merchandising-eVars)
   * **Aangepaste traffic-dimensies** (props)
   * **Dimensies en gebeurtenissen van oplossingen** (dimensies/gebeurtenissen in verband met oplossingen zoals Mobile, Video, Activity Map, enz., en integratie met oplossingen zoals Adobe Campaign, Adobe Experience Manager, Advertising Cloud, enz.)
   * **Dataverwerkingsdimensies** (variabelen die niet direct zichtbaar worden in rapportage via de Adobe Analytics-gebruikersinterface, maar beschikbaar voor u is via datafeeds en/of Data Warehouse-aanvragen)

1. (Optioneel) Klik op het informatiepictogram (i) naast elke variabele om de meest voorkomende waarden van de variabele in de afgelopen 90 dagen beter te begrijpen. (Deze functionaliteit is niet beschikbaar voor dataverwerkingsdimensies, omdat deze niet beschikbaar zijn in de Analytics-gebruikersinterface.)

   ![Info](assets/info.png)

1. Selecteer een of meer variabelen door op het selectievakje te klikken en selecteer vervolgens het pictogram **[!UICONTROL Edit]** (rechts) om een of meer variabelen te bewerken.

   ![Bewerken](assets/edit.png)

1. Het dialoogvenster **Labels voor identiteitsdata** wordt automatisch geopend. Deze labels classificeren data die op zichzelf of in combinatie met andere data kunnen worden gebruikt om een individu te identificeren of rechtstreeks contact met een individu op te nemen. Raadpleeg [Labels voor identiteitsdata (DULE)](/help/admin/c-data-governance/gdpr-labels.md#identity-data-labels) voor meer informatie over deze opties.

   >[!NOTE]
   >
   >Het DULE-kader (Data Usage Labeling &amp; Enforcement) is ontworpen als een uniforme manier voor alle oplossingen/services/platforms om metadata over data vast te leggen, te communiceren en te gebruiken in de hele Adobe Experience Cloud. De metadata helpen datacontrollers om aan te geven welke data persoonlijke data zijn, welke data gevoelig zijn, en welke contractbeperkingen aan data zijn gekoppeld.

   ![Identiteitslabels](assets/identity_labels.png)

1. Open de sectie **Gevoelige data** om labels voor gevoelige data in te stellen, dat geolocatiedata categoriseert. Raadpleeg [Labels voor gevoelige data (DULE)](/help/admin/c-data-governance/gdpr-labels.md#sensitive-data-labels) voor meer informatie over deze opties.

   ![Positieve gegevens](assets/sensitive_data.png)

1. Open de Data Privacy-datasectie om **Data Governance**-labels in te stellen. Gebruik deze sectie om Adobe instructies te geven voor de behandeling van elke variabele voor Data Privacy-toegangs- en verwijderingsaanvragen, en tevens om te definiëren welke variabelen moeten worden gescand om id&#39;s van geregistreerde personen voor deze aanvragen te vinden. Raadpleeg [Data Governance-labels (Data Privacy)](/help/admin/c-data-governance/gdpr-labels.md#data-governance-labels) voor meer informatie over deze opties.

   ![Privacy-labels](assets/privacy_labels.png)

1. Klik op **[!UICONTROL Apply]** zodra u alle labeling hebt voltooid.

## Labels kopiëren naar rapportsuite(s) {#section_7C6FDAFF049F4126B84F6261F72668EE}

Als u dezelfde DULE/Data Privacy-instellingen wilt toepassen op meerdere rapportsuites, kunt u de volgende stappen uitvoeren:

1. Selecteer de variabelengroep (Standaarddimensies, Conversiedimensies, enz.) met de variabele die u wilt kopiëren. U kunt de labels slechts voor één groep variabelen tegelijk kopiëren.
1. Selecteer enkele of alle variabelen in deze groep.
1. Klik op **[!UICONTROL Copy Labels to Report Suite(s)]** rechtsboven in het dialoogvenster Data Governance.

   ![Toepassen als sjabloon](assets/apply_as_template.png)

1. Selecteer **[!UICONTROL Select All]** om labels voor de geselecteerde variabelen te kopiëren naar alle rapportsuites, of selecteer de afzonderlijke rapportsuites waar u de labels naartoe wilt kopiëren.

   >[!IMPORTANT]
   >
   >Houd er rekening mee dat alle geselecteerde rapportsuites moeten zijn toegewezen aan uw Experience Cloud-organisatie.

   Wanneer u de labels voor een variabele of een reeks variabelen naar een andere rapportsuite kopieert, gaat de kopie naar de variabele in de overeenkomstige positie doelrapportsuite. Voor standaarddimensies, standaardcijfers, oplossingsdimensies en dimensies van gebeurtenissen en dataverwerking worden de labels gekopieerd naar de variabele met **dezelfde naam** in de doelrapportsuite.

   Voor conversievariabelen (eVars), merchandising-conversievariabelen en aangepaste traffic-dimensies (props) gaat de kopie naar de variabele met **hetzelfde getal** in de doelrapportsuite. eVar12 wordt bijvoorbeeld gekopieerd naar eVar12 in alle doelrapportsuites. De namen van deze variabelen worden genegeerd bij het bepalen van het doel van de kopie. Als de overeenkomstige variabele niet is ingeschakeld in de doelrapportsuite, zal het kopiëren van die variabele mislukken.

   Bij het kopiëren van de labels voor classificaties die zijn gedefinieerd voor een variabele, worden de labels gekopieerd naar een classificatie op de corresponderende variabele in de doelrapportsuite (zoals eVar7 naar eVar7) die dezelfde naam heeft als de gekopieerde classificatie. Anders zal het kopiëren voor de labels van die classificatie mislukken.

   Er wordt een statusbericht weergegeven nadat een set labels is toegepast. Het statusbericht bevat de namen van bestemmingsvariabelen of classificaties en hun rapportsuites waarvoor het kopiëren is mislukt.

   >[!IMPORTANT]
   >
   >Controleer altijd de doelrapportsuites om te zien of de labels goed zijn gekopieerd. Dit is vooral belangrijk voor variabelen met ID- of DEL-labels.

1. Klik op **[!UICONTROL Apply]**.
