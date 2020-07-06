---
description: Laat gebruikerstoestemmingen voor Algemene punten (het factureren, logboeken, enz.), het Beheer van het Bedrijf, Hulpmiddelen, de Toegang van de Dienst van het Web, de Bouwer van het Rapport, en de integratie van de Verbindingen van Gegevens toe.
keywords: groups;permissions
subtopic: Users and groups
title: Toestemmingen voor Analytics-tools
topic: Admin tools
uuid: 8e86bc17-46d3-4c5e-ac25-9f3bfc29b8fa
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 10%

---


# Toestemmingen voor Analytics-tools

>[!IMPORTANT]
>
>Gebruiker- en productbeheer is verplaatst naar de [Admin Console](https://helpx.adobe.com/nl/enterprise/using/admin-console.html). Adobe geeft een melding wanneer het uw tijd is om gebruikers te migreren. Nadat alle klanten zijn gemigreerd, wordt de Help-inhoud voor **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]** ingetrokken.

Laat gebruikerstoestemmingen voor Algemene punten (het factureren, logboeken, enz.), het Beheer van het Bedrijf, Hulpmiddelen, de Toegang van de Dienst van het Web, de Bouwer van het Rapport, en de integratie van de Verbindingen van Gegevens toe.

**[!UICONTROL User Management]** > **[!UICONTROL Groups]** > **[!UICONTROL All Report Access]** > **[!UICONTROL Analytics Tools]** > **[!UICONTROL Customize]**

>[!NOTE]
>
>De release van 2016 (20 oktober) bracht wijzigingen in groepsbeheer. Zie [Administratieve Veranderingen - Herfst 2016](/help/admin/user-management2/c-user-management/permissions-changes.md) voor een samenvatting van veranderingen.

## Rapporttoegang - Analytics-gereedschappen

![](assets/report-access-analytics-tools.png)

Klik **[!UICONTROL Customize]** om items te selecteren waartoe deze groep toegang heeft.

## Veldbeschrijvingen

De instellingen op deze pagina hebben betrekking op de rapportsuites die op de [!UICONTROL Define User Groups] pagina zijn geselecteerd.

| Element | Beschrijving |
|--- |--- |
| **Algemeen** |  |
| [Code Manager](/help/admin/admin/code-manager-admin.md) | Hiermee wordt machtiging ingeschakeld om code voor gegevensverzameling te downloaden voor web en mobiele platforms. |
| Codebeheer - Webservices | Staat een niet administratieve gebruiker toe om tot de Manager van de Code door de Diensten van het Web toegang te hebben. |
| [Logboeken](/help/admin/admin/logs.md) | Hiermee schakelt u machtigingen in voor het aanmelden van bestanden, zodat u kunt zien wanneer gebruikers zich aanmelden, hoe hun gebruik, toegang, rapportsuites en Admin-wijzigingen zijn. |
| Logboeken - Webservices | Staat een niet-administratieve gebruiker toe om tot de logboeken van Hulpmiddelen Admin door de Diensten van het Web toegang te hebben. |
| [Traffic-beheer](/help/admin/c-traffic-management/traffic-management.md) | De pagina van het Beheer van het verkeer laat u verwachte veranderingen van het verkeersvolume specificeren. |
| Machtigingsbeheer | Hiermee geeft u gebruikers die geen beheerder zijn toegang tot de pagina&#39;s voor gebruikersbeheer in de beheerprogramma&#39;s. Deze gebruikers beschikken over Leesmachtigingen, maar hebben geen schrijfmachtigingen. |
| Machtigingen (schrijven) - Webservices | Verleent niet-administratieve gebruikers lees en schrijf toestemmingsmontages onder het Beheer van de Gebruiker in de Diensten van het Web.<br>Deze instelling verwijst specifiek naar de aangegeven handelingen voor machtigingen in de Admin API. |
| Machtigingen (lezen) - Webservices | Staat een niet-administratieve gebruiker toe om toestemmingsmontages onder Beheer van de Gebruiker in de Diensten van het Web te bekijken.<br>Deze instelling verwijst specifiek naar de aangegeven handelingen voor machtigingen in de Admin API. |
| **Bedrijfsbeheer** |  |
| [Beveiliging](/help/admin/company/security-manager.md) | Verleent toestemming aan de pagina van de Manager van de Veiligheid om toegang tot het melden van gegevens te controleren. De opties omvatten sterke wachtwoorden, wachtwoordafloop, IP login beperkingen, en e-maildomeinbeperkingen. |
| Ondersteuningsinformatie | Verleent toestemming aan de Informatie van de Steun in de Montages van het Bedrijf. |
| [Webservices](/help/admin/company/web-services-admin.md) | Hiermee krijgt u toegang tot de pagina Webservices in de interface Admin Tools ([!UICONTROL Company Settings] > [!UICONTROL Web Services]).<br>De webservices-API biedt programmatische toegang tot Adobe Analytics-services waarmee u functionaliteit kunt dupliceren en uitbreiden die beschikbaar is via de gebruikersinterface. |
| Single Sign-On (verouderd) | Hiermee krijgt u toegang tot de eenmalige aanmeldingspagina in Admin Tools.<br>**Opmerking:**Single Sign-On in de Adobe Experience Cloud wordt geïmplementeerd via een[account dat een koppeling](https://docs.adobe.com/content/help/nl-NL/core-services/interface/manage-users-and-products/organizations.html)maakt tussen de Experience Cloud en de oplossingen. |
| [Handelingen in behandeling](/help/admin/company/pending-actions-admin.md) | Hiermee geeft u toestemming voor het beheren van lopende handelingen in [!UICONTROL Company Settings]. |
| [Co-branding](/help/admin/company/co-branding-admin.md) | Hiermee geeft u toestemming voor het cobrand van Analytics. |
| [Voorkeuren](/help/admin/admin/preferences-manager.md) | Hiermee geeft u de gebruiker toestemming [!UICONTROL Preference Manager]. |
| [Rapportageopties verbergen](/help/admin/company/c-hide-report-suites.md) | Hiermee geeft u toestemming om rapportsuites te verbergen in de gebruikersinterface van Adobe Analytics. |
| **Gereedschappen** | Met deze instellingen hebt u toegang tot Analytics-gereedschappen (interfaces en toepassingen) en geavanceerde mogelijkheden, zoals segmentatie en berekende meetgegevens. |
| [Huidige data](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/current-data.html) | Hiermee geeft u toestemming om de functie Huidige gegevens te gebruiken bij rapportage. |
| [Ad hoc analysis](https://docs.adobe.com/content/help/en/analytics/analyze/ad-hoc-analysis/adhoc-home.html) licentiegebruikers | Hiermee krijgt u toegang [!UICONTROL Ad Hoc Analysis]. |
| Webservicetoegang | Laat de toegang van de Diensten van het Web voor niet-beheerders toe. Genereert de geloofsbrieven van de Dienst van het Web. |
| [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/t-install-arb.html) | Leden van deze groep krijgen toegang tot [!UICONTROL Report Builder] licenties. |
| [Analysis Workspace](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html) Access | Biedt gebruikers toegang tot Analysis Workspace, de aanbevolen rapportinterface voor [!DNL Adobe Analytics]. |
| [Rapporten en Analytics](https://docs.adobe.com/content/help/en/analytics/landing/an-key-concepts.html) | Biedt gebruikers toegang tot Rapporten &amp; Analytics. |
| [Berekend metrisch ontwerp](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/cm-overview.html) | Hiermee geeft u gebruikers toestemming om berekende metriek te maken. |
| [Segment maken](https://docs.adobe.com/content/help/en/analytics/components/segmentation/seg-home.html) | Hiermee geeft u gebruikers toestemming om segmenten te maken. |
| **Data Connectors** |  |
| Integraties (maken, bijwerken of verwijderen) | Verleent toestemming om, de integratie van de Verbinding van Gegevens tot stand te brengen bij te werken en te schrappen. |
