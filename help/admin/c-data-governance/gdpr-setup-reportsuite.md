---
description: De gegevens van de het rapportreeks van het etiketteren betekent dat u identiteit, gevoeligheid, en de etiketten van het gegevensbeheer aan elke variabele in een bepaalde rapportreeks toewijst. Zorg ervoor dat u zich eerst vertrouwd maakt met de labels en de bijbehorende definities.
title: Gegevens uit de labelrapportsuite
uuid: a694851c-8933-496e-9118-113cc38cba8a
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Gegevens uit de labelrapportsuite

De gegevens van de het rapportreeks van het etiketteren betekent dat u identiteit, gevoeligheid, en de etiketten van het gegevensbeheer aan elke variabele in een bepaalde rapportreeks toewijst. Zorg ervoor dat u zich eerst vertrouwd maakt met de labels en de bijbehorende definities.

>[!NOTE] Herinner dat het Etiketteren moet worden herzien telkens als een nieuwe rapportreeks wordt gecreeerd of wanneer een nieuwe variabele binnen een bestaande rapportreeks wordt toegelaten. Het kan ook nodig zijn om de labeling te herzien wanneer integratie van nieuwe oplossingen is ingeschakeld, omdat deze nieuwe variabelen toegankelijk kunnen maken waarvoor een label nodig kan zijn. Een nieuwe implementatie van uw mobiele apps of websites kan de manier veranderen waarop bestaande variabelen worden gebruikt, wat ook updates van labels kan vereisen.

## Rapportsuite-labels toewijzen of bewerken {#section_39F829F35A274EACA532E2F6FF392996}

**Voorbeeld**: Als gegevenscontroller wilt u e-mailadressen en cookie-id&#39;s verzamelen van betrokkenen om hun privacyverzoeken te verwerken. Deze cookie-id&#39;s worden opgeslagen in een rapportsuite in Adobe Analytics. Als u een label voor e-mailadressen en cookie-id&#39;s wilt maken, moet u het framework Data Usage Labeling &amp; Enforcement (DULE) van het Adobe Cloud Platform in Analytics gebruiken.

1. Navigeer in Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL Data Governance]** > **[!UICONTROL (select report suite)]**![](assets/privacy_rs_settings.png)

1. Selecteer welke groep variabelen u wilt etiketteren.

   ![](assets/variables.png)

   * **Standaardafmetingen** (afmetingen van Adobe Analytics buiten de verpakking)
   * **Standaardmetriek** (cijfers voor Adobe Analytics buiten de verpakking)
   * **Conversiegebeurtenissen** (aangepaste succesgebeurtenissen)
   * **Conversieafmetingen** voor handelsdoeleinden (handelswisselaars)
   * **Omzetafmetingen** (niet-verkoopbare eVars)
   * **Aangepaste verkeersafmetingen** (props)
   * **Afmetingen en gebeurtenissen** van de oplossing (Afmetingen/gebeurtenissen met betrekking tot oplossingen zoals Mobiel, Video, Activiteitenkaart, enz., en integratie met oplossingen zoals de Campagne van Adobe, de Manager van de Ervaring van Adobe, Advertising Cloud, enz.)
   * **Afmetingen** gegevensverwerking (variabelen die niet rechtstreeks beschikbaar zijn in rapportage via de gebruikersinterface van Adobe Analytics, maar die u wel kunt gebruiken via gegevensfeeds en/of verzoeken van het Data Warehouse)

1. (Optioneel) Klik op het informatiepictogram (i) naast elke variabele om de meest voorkomende waarden van de variabele in de afgelopen 90 dagen beter te begrijpen. (Deze functionaliteit is niet beschikbaar voor Afmetingen gegevensverwerking, omdat deze niet beschikbaar zijn in de interface Analytics.)

   ![](assets/info.png)

1. Selecteer een of meer variabelen door op het selectievakje te klikken en selecteer vervolgens het **[!UICONTROL Edit]** pictogram (rechts) om een of meer variabelen te bewerken.

   ![](assets/edit.png)

1. Het dialoogvenster **Naamlabels voor identiteitsgegevens** wordt automatisch geopend. Deze labels classificeren gegevens die op zichzelf of in combinatie met andere gegevens kunnen worden gebruikt om direct contact met een individu te identificeren of in te schakelen. Raadpleeg [Naamlabels (DULE) voor meer informatie over deze opties.](/help/admin/c-data-governance/gdpr-labels.md#identity-data-labels)

   >[!NOTE]
   >
   >Het Data Usage Labeling &amp; Enforcement (DULE) Framework is ontworpen om een uniforme manier te bieden voor oplossingen/services/platforms om metagegevens over gegevens in de Adobe Experience Cloud vast te leggen, te communiceren en te gebruiken. De meta-gegevens helpen gegevenscontrolemechanismen wijzen op welke gegevens persoonlijke informatie is, welke gegevens gevoelige gegevens zijn, en welke contractbeperkingen met gegevens worden geassocieerd.

   ![](assets/identity_labels.png)

1. Open de sectie **Gevoelige gegevens** om Gevoelige gegevenslabels in te stellen, waarin geolocatiegegevens worden gecategoriseerd. Raadpleeg [Gevoelige gegevenslabels (DULE) voor meer informatie over deze opties.](/help/admin/c-data-governance/gdpr-labels.md#sensitive-data-labels)

   ![](assets/sensitive_data.png)

1. Open de sectie Gegevens van de Privacy van Gegevens om de Etiketten van het Beheer van **Gegevens** te plaatsen. In deze sectie leert u Adobe hoe u elke variabele voor toegang tot en verwijdering van gegevensprivacy moet verwerken, en welke variabelen u moet scannen om de id&#39;s van de betrokkene voor deze aanvragen te zoeken. Raadpleeg de labels voor [gegevensbeheer (Data Privacy) voor meer informatie over deze opties.](/help/admin/c-data-governance/gdpr-labels.md#data-governance-labels)

   ![](assets/privacy_labels.png)

1. Klik **[!UICONTROL Apply]** zodra u alle etikettering hebt voltooid.

## Labels kopiëren naar rapportsuite(s) {#section_7C6FDAFF049F4126B84F6261F72668EE}

Als u dezelfde DULE/Data Privacy-instellingen wilt toepassen op meerdere rapportsuite, kunt u de volgende stappen uitvoeren:

1. Selecteer de variabelegroep (Standaardafmetingen, Conversieafmetingen, enz.) met de variabele die u wilt kopiëren. U kunt de labels slechts voor één groep variabelen tegelijk kopiëren.
1. Selecteer enkele of alle variabelen in deze groep.
1. Klik **[!UICONTROL Copy Labels to Report Suite(s)]** bij het hoogste recht van de dialoog van het Beleid van Gegevens.

   ![](assets/apply_as_template.png)

1. Controleer of **[!UICONTROL Select All]** om labels voor de geselecteerde variabelen naar alle rapportsuites te kopiëren of selecteer de afzonderlijke rapportsuites waarnaar u de labels wilt kopiëren.

   >[!IMPORTANT]
   >
   >Houd er rekening mee dat alle gekozen rapportenpakketten moeten worden toegewezen aan uw Experience Cloud-organisatie.

   Wanneer u de etiketten voor een variabele of een reeks variabelen in een verschillende rapportreeks kopieert, gaat het exemplaar naar de variabele in de overeenkomstige positie in de reeks van het bestemmingsrapport. Voor Standaardafmetingen, Standaardmetriek, de Afmetingen van de Oplossing en Gebeurtenissen en de Afmetingen van de Gegevensverwerking, zullen de etiketten aan de variabele met de **zelfde naam** in de reeks van het bestemmingsrapport worden gekopieerd.

   Nochtans, voor de Variabelen van de Omzetting (eVars), de Afmetingen van de Omzetting van de Verkoop en de Dimensies van het Verkeer van de Douane (steunen) zal het exemplaar aan de variabele met het **zelfde aantal** in de reeks van het bestemmingsrapport zijn. eVar12 wordt bijvoorbeeld naar eVar12 gekopieerd in alle suites van het bestemmingsrapport. De namen van deze variabelen worden genegeerd bij het bepalen van het doel van de kopie. Als de overeenkomstige variabele niet in de reeks van het bestemmingsrapport wordt toegelaten, zal het exemplaar voor die variabele ontbreken.

   Wanneer het kopiëren van de etiketten voor classificaties die voor een variabele worden bepaald, zullen de etiketten aan een classificatie op de overeenkomstige variabele in de reeks van het bestemmingsrapport (zoals eVar7 aan eVar7) worden gekopieerd die een naam heeft die aan de classificatie identiek is die wordt gekopieerd. Anders zal de kopie voor de labels van die classificatie mislukken.

   Er wordt een statusbericht weergegeven nadat een set labels is toegepast. Het statusbericht bevat de namen van bestemmingsvariabelen of classificaties en hun rapportsuites waarvoor de kopie is mislukt.

   >[!IMPORTANT]
   >
   >Controleer altijd de suites van het doelrapport om ervoor te zorgen dat de etiketten correct worden gekopieerd. Dit is vooral belangrijk voor variabelen met ID- of DEL-labels.

1. Klik op **[!UICONTROL Apply]**.

