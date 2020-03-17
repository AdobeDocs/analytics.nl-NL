---
description: Deze integratie combineert de kracht van een geïntegreerd feedbacksysteem voor het in de handel brengen van e-mail en de gedragsrapportage van Adobe Analytics om krachtige analyses en optimaliseringsmogelijkheden voor uw organisatie te creëren.
title: optivo® broadmail Data Connector voor Adobe Analytics
uuid: bd713080-9d1a-49ee-aad0-86dd5c37c34a
translation-type: tm+mt
source-git-commit: ''

---


# optivo® broadmail Data Connector voor Adobe Analytics{#optivo-broadmail-data-connector-for-adobe-analytics}

Deze integratie combineert de kracht van een geïntegreerd feedbacksysteem voor het in de handel brengen van e-mail en de gedragsrapportage van Adobe Analytics om krachtige analyses en optimaliseringsmogelijkheden voor uw organisatie te creëren.

[!DNL ~Partner~] is een professionele software voor e-mailmarketing. De belangrijkste functie van deze organisatie is het maken, verzenden en evalueren van nieuwsbrieven en e-mailcampagnes. `[~Partner~]` is beschikbaar als cloudservice (software als service).

De `[~Partner~]` integratie biedt geautomatiseerde remarketing en gegevenssynchronisatie, die tot verhoogde omzettingen en opbrengst leiden. Dankzij deze integratie kunnen marketers segmenten voor hun klanten automatisch synchroniseren op basis van hun e-mailinteractie en sitegedrag. De geautomatiseerde gegevensuitwisseling van klantgerichte segmenten helpt u om hoogst gerichte e-mailcampagnes te creëren die verkoop bevorderen, zoals het winkelwagentjes verlaten en post-aankoop hermarketing aan dwars, omhoog en wederverkoopproducten.

Bij deze integratie worden ook gegevens uitgewisseld over geslaagde e-mailcampagnes van `[~Partner~]` naar Adobe Analytics. Essentiële gegevens worden centraal weergegeven in het overzicht van uw e-mailcampagne.

## Data Connectors Laboratory Program {#section-51f9864851b64d96873127b9ac9c9a2b}

Dit programma is een snelle methode voor de partners van het platform van Adobe van derden om integratie te bouwen en hen te leveren aan onze gemeenschappelijke markt. De integraties worden volledig ontwikkeld door onze partners en beschikbaar gesteld op de Adobe Experience Cloud volgens de methoden van de gebruikersgemeenschap. Deze services worden gratis ter beschikking gesteld van Adobe-klanten van Adobe Analytics en andere Solutions en worden, gezien de aard van de integraties door derden, op basis van de actuele situatie geleverd zonder impliciete garanties van Adobe.

Neem contact op met uw accountmanager van Adobe als u vragen hebt over uw huidige service, garantie of licentie.

## Belangrijke voordelen en functies{#key-benefits-and-features}

Deze integratie omvat de volgende belangrijke voordelen:

* Kopers terughalen die bladeren en verlaten
* Verhoog de verkoop met gerichte cross-sell en up-sell hermarketing
* Automatische segmentcampagnes
* Geoptimaliseerde campagnes worden uitgevoerd
* Segmenten in [!DNL ~Partner~] voor gerichte hermarketing
* Constante metrische updates van de campagne
* Geautomatiseerde gesprekstriggers

## Dynamische marketingsegmenten{#dynamic-marketing-segments}

Deze integratie kenmerkt de volgende dynamische marketing segmenten:

* **Aankoopprofielen:** Herhalingsbestellingen en gemiddelde orderwaarde verhogen via campagnes die zijn bedoeld voor aankooppatronen van bezoekers.
* **Gedragsprofiel van product-/inhoudsweergave:** Bereik potentiële klanten door marketing segmenten die op productmeningen en inhoud toegang profiling worden gebaseerd.
* **Profiel voor afschrijving van winkelwagentje:** Help bezoekers om te zetten in klanten via fijnafgestemde campagnes die speciaal zijn ontworpen voor mensen die aarzelen om winkelwagentjes te maken.
* **Effectieve markering:** Klanten kunnen ook aangepaste remarketing-segmenten maken en plannen die specifiek zijn voor de behoeften van hun gebruikers.

## Voordat u activeert{#before-you-activate}

Voordat u de integratie van gegevensconnectors start voor, moet u aan de volgende vereisten voldoen:

## Vereisten voor Adobe Analytics {#section-960e70fd2eae4a1cb88a2e4b53a97313}

* **rapportsuite specifiek:** Wees erop gewezen dat deze integratie specifiek is voor de rapportsuite. Zorg ervoor dat u de gewenste rapportsuite hebt geselecteerd voordat u de integratie activeert.
* **Beschikbare en geconfigureerde Adobe Analytics-variabelen:** Voor deze integratie zijn aangepaste gebeurtenissen en aangepaste eVars vereist.

* **Geautoriseerde vertegenwoordiger:** Houd er rekening mee dat het inschakelen van deze integratie ertoe kan leiden dat uw bedrijf kosten aanrekent in overeenstemming met uw serviceovereenkomst met Adobe, Inc. of uw serviceovereenkomst met een van de vertrouwde partners van Adobe, al naargelang het geval. Door deze integratie te activeren, vertegenwoordigt u hierbij dat u een gemachtigde vertegenwoordiger van uw bedrijf bent; en als zodanig stemt uw bedrijf ermee in de eventuele kosten te betalen die in de hierboven beschreven serviceovereenkomst zijn vermeld.
* **Bericht-id:** Voor de integratie is het nodig dat we een bericht-id vastleggen en opslaan in een Adobe Analytics-variabele (eVar). Deze id&#39;s zijn nodig om de verzendingen te identificeren. Als deel van het opstellingsproces, moet u eVar voor dit doel identificeren wanneer ertoe aangezet door de Tovenaar.
* **Partner:** De integratie vereist dat wij vangen en een [!UICONTROL ~Partner~] binnen een variabele van de Analyse van Adobe opslaan (eVar). Deze identiteitskaart is een gecodeerde of numerieke vertegenwoordiging van een e-mailadres van het systeem van de [!UICONTROL ~Partner~] . Deze [!UICONTROL ~Partner~] is gekoppeld aan het gedrag van downstreambezoekers op de site (winkels, aankopen, enz.) dat in het systeem van de [!UICONTROL ~Partner~] wordt getrokken en voor remarketing doeleinden kan worden leveraged. Als deel van het opstellingsproces, moet u eVar voor dit doel identificeren wanneer ertoe aangezet door de Tovenaar.
* **Tijd na klikken:** Als onderdeel van het installatieproces vereist deze integratie een toewijzing aan een eVar die overeenkomt met de tijd van een postklikactie. Dit is nodig om informatie over een ontvankelijke actie aan [!UICONTROL ~Partner~] over te brengen nadat de ontvanger een verbinding in een post klikte.

* **Klik op Product:** Als onderdeel van het installatieproces vereist deze integratie een toewijzing aan een eVar die aan het aangeboden product beantwoordt dat met een post klikactie wordt geassocieerd. Dit is nodig om informatie over een ontvankelijke actie aan [!UICONTROL ~Partner~] over te brengen nadat de ontvanger een verbinding in een post klikte.

* **Type handeling na klikken:** Als onderdeel van het installatieproces vereist deze integratie een toewijzing aan een eVar die overeenkomt met het type handeling na klikken. Dit is nodig om informatie over een ontvankelijke actie aan [!UICONTROL ~Partner~] over te brengen nadat de ontvanger een verbinding in een post klikte.

* **Privacy-compatibiliteit:** Als u de functie voor het bijhouden van de identiteit van de ontvanger of de bezoeker inschakelt, worden hiermee persoonlijke identificeerbare gegevens van uw sitebezoekers mogelijk bijgehouden. Dit heeft gevolgen voor de persoonlijke levenssfeer en vereist de implementatie van de juiste procedures door uw organisatie, zoals kennisgeving aan en toestemming van uw sitebezoekers.

## Prijzen{#pricing}

Houd er rekening mee dat het inschakelen van deze integratie ertoe kan leiden dat uw bedrijf kosten aanrekent in overeenstemming met uw serviceovereenkomst met Adobe, Inc. of uw serviceovereenkomst met een van de vertrouwde partners van Adobe, al naargelang het geval.

Door deze integratie te activeren, vertegenwoordigt u hierbij dat u een gemachtigde vertegenwoordiger van uw bedrijf bent; en als zodanig stemt uw bedrijf ermee in de eventuele kosten te betalen die in de hierboven beschreven serviceovereenkomst zijn vermeld.

### Prijsoverwegingen van Adobe {#section-1f4f46c0d969435db57d38c1c310a05a}

Huidige klanten van de Adobe Analytics-oplossing hebben geen extra kosten voor het gebruik van deze integratie van gegevensconnectors. Klanten die nog niet naar het nieuwe Adobe Analytics-product zijn gegaan, kunnen voor meer informatie contact opnemen met hun Adobe-accountvertegenwoordiger.

### Prijsoverwegingen voor partners {#section-f8ca71df32224412a5101efb6e356529}

Deze integratie is beschikbaar aan de klanten van de [!DNL ~Partner~] , nochtans zullen de extra integratietarieven van toepassing zijn. Neem contact op met sales@optivo.com voor prijsgegevens. Neem contact op met de [!DNL ~partner~] voor prijsinformatie.

## Adobe Analytics-variabelen{#adobe-analytics-variables}

Voor deze integratie zijn Adobe Analytics-variabelen vereist om de metingen bij te houden.

Nadat u de gebeurtenissen en eVars hebt geïdentificeerd om deze integratie te kunnen gebruiken, moeten deze zijn ingeschakeld in de beheerconsole voor analysemogelijkheden (zie [Rapportsets](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html) voor instructies).
