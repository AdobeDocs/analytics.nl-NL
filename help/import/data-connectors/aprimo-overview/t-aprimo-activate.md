---
description: Gebruik de configuratiewizard van Adobe Data Connectors om de integratie in te stellen.
title: De integratie activeren
uuid: 0a5d2d45-5133-4259-96ce-c992a1e314ee
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# De integratie activeren {#activate-the-integration}

Gebruik de configuratiewizard van Adobe Data Connectors om de integratie in te stellen.

1. Start [Gegevensconnectors](https://marketing.adobe.com/resources/help/en_US/genesis/c_overview.html) en klik **[!UICONTROL + Add New]** om een nieuwe integratie [toe te](https://marketing.adobe.com/resources/help/en_US/genesis/t_add_integration.html)voegen.
1. Selecteer in de **[!UICONTROL Show]** lijst de integratie van de **[!UICONTROL By Name]** Partner [!DNL ~~] en sleep deze naar een lege plug-in.
1. Voltooi de Tovenaar van de Integratie gebruikend de informatie in de volgende lijst:

| Veld | Beschrijving |
|--- |--- |
| Rapportsuite | De rapportsuite die de gegevens van deze integratie ontvangt. |
| Integratienaam | Specificeer de integratienaam die de Verbindingen van Gegevens in de Actieve Lijst van de Integratie van de rapportreeks tonen. |
| Account-id | Geef uw accountid voor de maand april op. |
| Ontvanger-id | Deze id is een gecodeerde of numerieke weergave van een e-mailadres uit het systeem van april. Deze &quot;Ontvanger-id&quot; is gekoppeld aan het gedrag van een downstreambezoeker op de site Ontvanger-id (winkels, aankopen, enz.) die in het systeem van april wordt opgenomen en voor hermarketingdoeleinden kan worden gebruikt. |
| Geklikt | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de gegevens waarop u hebt geklikt, worden opgeslagen die uit het e-mailsysteem zijn geïmporteerd. Met de gebeurtenis Klikken kunt u het aantal bezoekers zien dat op het e-mailbericht heeft geklikt. |
| Bericht-id | (Vereist) Hiermee slaat u de unieke e-mailings-id op. |
| Geopend | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de gegevens worden opgeslagen die via e-mail zijn geopend en die zijn geïmporteerd uit het e-mailsysteem. Met de gebeurtenis Geopend kunt u het aantal bezoekers zien dat het e-mailbericht heeft geopend. |
| Ontvanger-id | (Vereist) Hiermee slaat u de unieke bezoeker-id op. |
| Verzonden | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de gegevens worden opgeslagen die vanuit het e-mailsysteem zijn geïmporteerd. Met de gebeurtenis Verzonden kunt u het aantal e-mailberichten zien dat is verzonden. |
| Bounces | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de gegevens van Total Bounces in het e-mailsysteem worden opgeslagen. Met de gebeurtenis Total-Bounces kunt u het aantal e-mailberichten zien dat niet aan ontvangers is bezorgd vanwege een leveringsprobleem. |
| Abonnement opgezegd | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de e-mailgegevens worden opgeslagen die uit het e-mailsysteem zijn geïmporteerd. Met de gebeurtenis Unsubscribed kunt u het aantal bezoekers zien dat het e-mailbericht heeft geopend, maar vervolgens op de koppeling Unsubscribe klikken om toekomstige e-mailberichten van uw organisatie af te melden. |
| Segmenten | Deze integratie leidt tot de partner-bepaalde segmenten die in de sectie van de Segmenten van de Partner worden getoond. Bovendien, kunt u bestaande Reeks-Vlakke segmenten van het Rapport selecteren om in de integratie te omvatten. |
| Toegangsverzoeken | Schakel de aanbevolen toegangsrechten in. |
| Gegevensverzameling | Selecteer **Insteekmodule** JavaScript als u de insteekmodule s_code.js als verzamelingsmodel voor deze integratie wilt gebruiken. |
Selecteer **Geautomatiseerde Oplossing** als u een geautomatiseerd inzamelingsmodel voor deze integratie wilt gebruiken, dan specificeer de unieke herkenningstekens die voor deze integratie worden gebruikt. Als u deze optie selecteert, geeft u de unieke id&#39;s op die voor deze integratie worden gebruikt:
<ul><li>Parameter tekenreeks voor query-id van bericht: Deze waarde vertegenwoordigt de bericht-id die door uw e-mailpartner aan de URL van de bestemmingspagina is toegevoegd.</li>
<li>Parameter voor tekenreeks ontvangerid-query: Deze waarde vertegenwoordigt de ontvanger-id die door uw e-mailpartner is toegevoegd aan de URL van de bestemmingspagina.</li></ul>||Het dashboard en de Generatie van de Bladwijzer|produceren automatisch een dashboard en referenties voor de integratie.|
