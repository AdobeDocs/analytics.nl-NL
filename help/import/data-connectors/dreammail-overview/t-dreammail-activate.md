---
description: Gebruik de wizard Configuratie van Adobe Data Connectors om de integratie in te stellen.
title: De integratie activeren
uuid: 9084b691-291d-49f7-9fa4-abda507e060d
exl-id: b0d6849b-975a-4476-a2d3-36abeee12273
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 2%

---

# De integratie activeren{#activate-the-integration}

Gebruik de wizard Configuratie van Adobe Data Connectors om de integratie in te stellen.

1. Start [Gegevensconnectors](https://experienceleague.adobe.com/docs/analytics/import/dataconnectors/getting-started-data-connectors.html) en klik op **[!UICONTROL + Add New]** om [een nieuwe integratie toe te voegen](https://experienceleague.adobe.com/docs/analytics/import/dataconnectors/getting-started-data-connectors.html).
1. Selecteer **[!UICONTROL Show]** in de lijst **[!UICONTROL By Name]** en sleep de integratie [!DNL ~Partner~] naar een lege plug-in.
1. Voltooi de Tovenaar van de Integratie gebruikend de informatie in de volgende lijst:

| Veld | Beschrijving |
|--- |--- |
| Rapportsuite | De rapportsuite die de gegevens van deze integratie ontvangt. |
| Integratienaam | Specificeer de integratienaam die de Verbindingen van Gegevens in de Actieve Lijst van de Integratie van de rapportreeks tonen. |
| Integratie-UUID | Geef uw UUID voor DreamMail-integratie op. |
| Clientnaam | Geef de naam van uw DreamMail-client op. |
| Sitenaam | Geef de naam van uw DreamMail-site op. |
| Stuitbalken | Aantal e-mailberichten dat niet aan ontvangers is bezorgd vanwege een leveringsprobleem. |
| Afgeleverd | Aantal geslaagde berichtleveringen. |
| Leveringsfouten | Ontbroken berichtleveringen. |
| HTML openen | Aantal bezoekers dat het e-mailbericht heeft geopend. |
| Invaliden | Aantal ongeldige e-mailadressen. |
| Campaign | Marketingcampagne-id. |
| Alongs doorgeven | Met de gebeurtenis Klikken kunt u het aantal bezoekers zien dat op het e-mailbericht heeft geklikt. |
| eVar e-mail | Een e-mailadres uit het DreamMail-systeem. Deze &quot;e-mail-eVar&quot; is gekoppeld aan het gedrag van downstreambezoekers op de site (winkels, aankopen, enz.) dat in het DreamMail-systeem wordt gehaald en voor hermarketingdoeleinden kan worden gebruikt. |
| Spotlight-gebeurtenis | Gebeurtenis die in re-marketing segmenten kan worden uitgevoerd. |
| Spotlightaankopen | Gebeurtenis die in re-marketing segmenten kan worden uitgevoerd. |
| Spotlichtwaarde | Gebeurtenis van de opbrengst die in re-marketing segmenten kan worden uitgevoerd. |
| TotalClicks | Met de gebeurtenis Klikken kunt u het aantal bezoekers zien dat op het e-mailbericht heeft geklikt. |
| Segmenten | Deze integratie leidt tot de partner-bepaalde segmenten die in de sectie van de Segmenten van de Partner worden getoond. Bovendien, kunt u bestaande Reeks-Vlakke segmenten van het Rapport selecteren om in de integratie te omvatten. |
| Toegangsverzoeken | Schakel de aanbevolen toegangsrechten in. |
| Gegevensverzameling | Selecteer **JavaScript-plug-in** als u de s_code.js-plug-in wilt gebruiken als verzamelingsmodel voor deze integratie (zie ). Selecteer **Geautomatiseerde Oplossing** als u een geautomatiseerd inzamelingsmodel voor deze integratie wilt gebruiken, dan specificeer de unieke herkenningstekens die voor deze integratie worden gebruikt. Als u deze optie selecteert, geeft u de unieke id&#39;s op die voor deze integratie worden gebruikt:<ul><li>Parameter tekenreeks voor query-id van bericht: Deze waarde vertegenwoordigt de bericht-id die door uw e-mailpartner aan de URL van de bestemmingspagina is toegevoegd.</li><li>Parameter voor tekenreeks ontvangerid-query: Deze waarde vertegenwoordigt de ontvanger-id die door uw e-mailpartner is toegevoegd aan de URL van de bestemmingspagina.</li></ul> |
| Dashboard en bladwijzergeneratie | Automatisch een dashboard en bladwijzers voor de integratie genereren. |
