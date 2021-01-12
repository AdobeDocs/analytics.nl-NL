---
description: Deze integratie combineert de kracht van een geïntegreerd feedbacksysteem voor het in de handel brengen van e-mail en de gedragsrapportage van Adobe Analytics om krachtige analyses en optimaliseringsmogelijkheden voor uw organisatie te creëren.
title: optivo® broadmail Data Connector voor Adobe Analytics
uuid: bd713080-9d1a-49ee-aad0-86dd5c37c34a
translation-type: tm+mt
source-git-commit: 3850dc3503ca57ba4f13f0de63e8420e484db501
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 0%

---


# optivo® broadmail Data Connector voor Adobe Analytics{#optivo-broadmail-data-connector-for-adobe-analytics}

>[!IMPORTANT]
>
>Op 1 augustus 2021 zullen we de Adobe Data Connector-technologie aan het einde van de levensduur hebben. [Meer informatie...](/help/import/data-connectors/data-connectors-eol.md)

Deze integratie combineert de kracht van een geïntegreerd feedbacksysteem voor het in de handel brengen van e-mail en de gedragsrapportage van Adobe Analytics om krachtige analyses en optimaliseringsmogelijkheden voor uw organisatie te creëren.

[!DNL ~~] Partneris een professionele e-mailmarketingsoftware. De belangrijkste functie van deze organisatie is het maken, verzenden en evalueren van nieuwsbrieven en e-mailcampagnes. `[~Partner~]` is beschikbaar als cloudservice (software als service).

De integratie `[~Partner~]` biedt geautomatiseerde remarketing en gegevenssynchronisatie, die tot verhoogde omzettingen en opbrengst leiden. Dankzij deze integratie kunnen marketers segmenten voor hun klanten automatisch synchroniseren op basis van hun e-mailinteractie en sitegedrag. De geautomatiseerde gegevensuitwisseling van klantgerichte segmenten helpt u om hoogst gerichte e-mailcampagnes te creëren die verkoop bevorderen, zoals het winkelwagentjes verlaten en post-aankoop hermarketing aan dwars, omhoog en wederverkoopproducten.

Deze integratie ruilt ook metriek van succesvolle e-mailcampagnes van `[~Partner~]` aan Adobe Analytics. Essentiële gegevens worden centraal weergegeven in het overzicht van uw e-mailcampagne.

## Data Connectors Laboratory Program {#section-51f9864851b64d96873127b9ac9c9a2b}

Dit programma is een snelle methode voor Adobe van partners van derde partijen om integraties op te bouwen en te leveren aan onze gemeenschappelijke markt. De integraties worden volledig ontwikkeld door onze partners en op de Adobe Experience Cloud beschikbaar gesteld volgens de methoden van de gemeenschap. Zij worden zonder extra kosten ter beschikking gesteld aan Adobe-klanten van de Adobe Analytics en andere Oplossingen en worden als zodanig geleverd zonder impliciete garanties van Adobe vanwege de aard van de integratie door derden.

Neem contact op met uw accountmanager van Adobe als u vragen hebt over uw huidige service, garantie of licentie.

## Zeer belangrijke Voordelen en Eigenschappen{#key-benefits-and-features}

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

* **Aankoopprofielen:Herhalingsbestellingen en gemiddelde orderwaarde** verhogen via campagnes die zijn bedoeld voor aanschafpatronen van bezoekers.
* **Gedragsprofiel van product-/inhoudsweergave:** Bereik potentiële klanten via marketingsegmenten op basis van productweergaven en profielen voor toegang tot inhoud.
* **Profiel van afstoting van winkelwagentjes:** Help bezoekers om te zetten in klanten door fijnafgestemde campagnes die speciaal zijn ontworpen voor hen die aarzelen om winkelwagentjes te voltooien.
* **Effectieve marketing:** klanten kunnen ook aangepaste remarketing-segmenten maken en plannen die specifiek zijn voor de behoeften van hun gebruikers.

## Voordat u{#before-you-activate} activeert

Voordat u de integratie van gegevensconnectors start voor, moet u aan de volgende vereisten voldoen:

## Adobe Analytics-vereisten {#section-960e70fd2eae4a1cb88a2e4b53a97313}

* **De Reeks van het rapport specifiek:** gelieve te adviseren deze integratie rapport-reeks specifiek is. Zorg ervoor dat u de gewenste rapportsuite hebt geselecteerd voordat u de integratie activeert.
* **Beschikbare en geconfigureerde Adobe Analytics-variabelen:** deze integratie vereist aangepaste gebeurtenissen en aangepaste eVars.

* **Geautoriseerde vertegenwoordiger:** Houd er rekening mee dat het inschakelen van deze integratie ertoe kan leiden dat uw bedrijf kosten betaalt in overeenstemming met uw serviceovereenkomst met Adobe, Inc. of uw serviceovereenkomst met een van de vertrouwde partners van de Adobe, al naar gelang van toepassing. Door deze integratie te activeren, vertegenwoordigt u hierbij dat u een gemachtigde vertegenwoordiger van uw bedrijf bent; en als zodanig stemt uw bedrijf ermee in de eventuele kosten te betalen die in de hierboven beschreven serviceovereenkomst zijn vermeld.
* **Bericht ID:** De integratie vereist dat wij &quot;identiteitskaart van het Bericht&quot;binnen een variabele van Adobe Analytics (eVar) vangen en opslaan. Deze id&#39;s zijn nodig om de verzendingen te identificeren. Als deel van het opstellingsproces, moet u een eVar voor dit doel identificeren wanneer ertoe aangezet door de Tovenaar.
* **Partner:** De integratie vereist dat wij een  [!UICONTROL ~~] Partnerschap binnen een variabele van Adobe Analytics (eVar) vangen en opslaan. Deze id is een gecodeerde of numerieke weergave van een e-mailadres van het systeem [!UICONTROL ~Partner~]. Deze [!UICONTROL ~Partner~] is gekoppeld aan het gedrag van downstreambezoekers op de site (winkels, aankopen, enz.) dat in het [!UICONTROL ~Partner~] systeem wordt getrokken en voor remarketing doeleinden kan worden gebruikt. Als deel van het opstellingsproces, moet u een eVar voor dit doel identificeren wanneer ertoe aangezet door de Tovenaar.
* **Na klikken Tijd:** Als deel van het opstellingsproces, vereist deze integratie een toewijzing aan een eVar die aan de tijd van een post klikactie beantwoordt. Dit is nodig om informatie over een ontvankelijke actie aan [!UICONTROL ~Partner~] over te brengen nadat de ontvanger een verbinding in een post klikte.

* **Na klikken op product:** Als onderdeel van het installatieproces vereist deze integratie een toewijzing aan een eVar die overeenkomt met het aangeboden product dat is gekoppeld aan een postklikactie. Dit is nodig om informatie over een ontvankelijke actie aan [!UICONTROL ~Partner~] over te brengen nadat de ontvanger een verbinding in een post klikte.

* **Type handeling na klikken:** als onderdeel van het installatieproces vereist deze integratie een toewijzing aan een eVar die overeenkomt met het type handeling na klikken. Dit is nodig om informatie over een ontvankelijke actie aan [!UICONTROL ~Partner~] over te brengen nadat de ontvanger een verbinding in een post klikte.

* **Privacy-naleving:** U moet weten dat deze functie persoonlijke identificeerbare gegevens van uw sitebezoekers kan bijhouden door de functie waarmee de identiteit van de ontvanger of de bezoeker wordt bijgehouden. Dit heeft gevolgen voor de persoonlijke levenssfeer en vereist de implementatie van de juiste procedures door uw organisatie, zoals kennisgeving aan en toestemming van uw sitebezoekers.

## Prijzen{#pricing}

Houd er rekening mee dat het inschakelen van deze integratie ertoe kan leiden dat uw bedrijf kosten aanrekent in overeenstemming met uw serviceovereenkomst met Adobe, Inc. of uw serviceovereenkomst met een van de vertrouwde partners van de Adobe, al naar gelang van toepassing.

Door deze integratie te activeren, vertegenwoordigt u hierbij dat u een gemachtigde vertegenwoordiger van uw bedrijf bent; en als zodanig stemt uw bedrijf ermee in de eventuele kosten te betalen die in de hierboven beschreven serviceovereenkomst zijn vermeld.

### Overwegingen bij prijzen Adobe {#section-1f4f46c0d969435db57d38c1c310a05a}

De huidige klanten van de oplossing van Adobe Analytics hebben geen extra kosten verbonden aan het gebruiken van deze Integratie van Verbindingen van Gegevens. Klanten die nog niet naar het nieuwe Adobe Analytics-product zijn verhuisd, moeten contact opnemen met hun Adobe-accountvertegenwoordiger voor meer informatie.

### Prijsoverwegingen voor partners {#section-f8ca71df32224412a5101efb6e356529}

Deze integratie is beschikbaar voor [!DNL ~Partner~] klanten, nochtans zullen de extra integratiekosten van toepassing zijn. Neem contact op met sales@optivo.com voor prijsgegevens. Neem contact op met [!DNL ~Partner~] voor prijsdetails.

## Adobe Analytics-variabelen{#adobe-analytics-variables}

Voor deze integratie zijn Adobe Analytics-variabelen vereist om de metriek bij te houden.

Na het identificeren van de Gebeurtenis en eVars om met deze integratie te gebruiken, moeten zij in de Admin Console van Analytics worden toegelaten (zie [Suites van het Rapport](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html) voor instructies).
