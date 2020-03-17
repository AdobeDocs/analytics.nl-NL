---
description: Gebruik de configuratiewizard van Adobe Data Connectors om de integratie in te stellen.
title: De integratie activeren
uuid: 3b2acdb8-9a1f-4f17-92f2-6a3780a8f626
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# De integratie activeren{#activate-the-integration}

Gebruik de configuratiewizard van Adobe Data Connectors om de integratie in te stellen.

1. Start [Gegevensconnectors](https://marketing.adobe.com/resources/help/en_US/genesis/c_overview.html) en klik **[!UICONTROL + Add New]** om een nieuwe integratie [toe te](https://marketing.adobe.com/resources/help/en_US/genesis/t_add_integration.html)voegen.
1. Selecteer in de **[!UICONTROL Show]** lijst de integratie van de **[!UICONTROL By Name]** Partner [!DNL ~~] en sleep deze naar een lege plug-in.
1. Voltooi de Tovenaar van de Integratie gebruikend de informatie in de volgende lijst:

| Veld | Beschrijving |
|--- |--- |
| Rapportsuite | De rapportsuite die de gegevens van deze integratie ontvangt. |
| Integratienaam | Specificeer de integratienaam die de Verbindingen van Gegevens in de Actieve Lijst van de Integratie van de rapportreeks tonen. |
| E-mailadres | Geef een e-mailadres op voor de ontvangst van informatie over integratie. |
| Account-id | Dit is de unieke id die door uw e-mailserviceprovider aan uw organisatie is toegewezen. Het wordt gebruikt bij het aanvragen van gegevens voor e-mailcampagnes (bijvoorbeeld # Verzonden, # geopend, # geklikt, enz.) van en het verzenden van bezoekerssegmenten naar uw E-mailserviceprovider. |
| Ontvanger-id | Deze id is een gecodeerde of numerieke weergave van een e-mailadres uit het optivo®-omroepsysteem. Deze &quot;Ontvanger-id&quot; is gekoppeld aan het gedrag van een downstreambezoeker op de site (winkels, aankopen, enz.) dat in het optivo® uitzendsysteem wordt geput en voor remarketing doeleinden kan worden gebruikt. |
| Bericht-id | (Vereist) Hiermee slaat u de unieke e-mailings-id op. Deze classificatiedimensies worden gecreeerd door de tovenaar van Verbindingen van Gegevens voor identiteitskaart van het Bericht: <br>a)**Campagnes**: Campagnes verbonden aan het bericht. <br>b)**Kanaal**: Het kanaal van transmissie, dit is constant &quot;optivo uitzending&quot;. <br>c)**Landcode**: Dit veld bevat de landcode van het land van verzending van oorsprong. Het is een constante &quot;DE&quot;. <br>d) **Leveringsgereedschap**: Wijze van verzending, altijd &quot;E-mail&quot;.<br> e) **Berichtnaam**: De naam van het posteren, aangezien het in optivo® broadmail wordt gevormd. <br>f) **Begindatum**: Tijdstempel van het begin van deze mailing. |
| Na klikken tijd | (Vereist) Dit is nodig om informatie over een ontvankelijke actie aan optivo® te overbrengen uitzending nadat de ontvanger een verbinding in een post klikte. |
| Product plaatsen | (Vereist) Dit is nodig om informatie over een ontvankelijke actie aan optivo® te overbrengen uitzending nadat de ontvanger een verbinding in een post klikte. |
| Handeling Na klikken | (Vereist) Dit is nodig om informatie over een ontvankelijke actie aan optivo® te overbrengen uitzending nadat de ontvanger een verbinding in een post klikte. |
| Hard stuiteren | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de gegevens van vaste bronnen die zijn geïmporteerd uit het e-mailsysteem worden opgeslagen. Aantal e-mailberichten die niet aan ontvangers zijn geleverd en als permanent niet-leverbaar worden beschouwd. |
| Zacht stuiteren | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de gegevens van de elektronische basis worden opgeslagen die uit het e-mailsysteem zijn geïmporteerd. Aantal e-mailberichten dat niet aan ontvangers is bezorgd vanwege een leveringsprobleem. |
| Geklikt | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de gegevens worden opgeslagen waarop u hebt geklikt en die u vanuit het e-mailsysteem hebt geïmporteerd. Met de gebeurtenis Klikken kunt u het aantal bezoekers zien dat op het e-mailbericht heeft geklikt. |
| Geopend | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de gegevens worden opgeslagen die met de e-mail zijn geopend en die uit het e-mailsysteem zijn geïmporteerd. Met de gebeurtenis Geopend kunt u het aantal bezoekers zien dat het e-mailbericht heeft geopend. |
| Verzonden | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de via e-mail verzonden gegevens worden opgeslagen die uit het e-mailsysteem zijn geïmporteerd. Met de gebeurtenis Verzonden kunt u het aantal e-mailberichten zien dat is verzonden. |
| Abonnement opgezegd | (Vereist) Geef de Adobe Analytics-gebeurtenis op waarin de uit het e-mailsysteem geïmporteerde gegevens voor het afmelden van e-mailberichten worden opgeslagen. Met de gebeurtenis Unsubscribed kunt u het aantal bezoekers zien dat het e-mailbericht heeft geopend, maar vervolgens op de koppeling Unsubscribe klikken om toekomstige e-mailberichten van uw organisatie af te melden. |
| Segmenten | Laat bestaande segmenten toe om samen met deze integratie worden gebruikt (facultatief). |
| Toegangsverzoeken | Schakel de aanbevolen toegangsrechten in. |
| Gegevensverzameling | Selecteer **Insteekmodule** JavaScript als u de insteekmodule s_code.js als verzamelingsmodel voor deze integratie wilt gebruiken. Selecteer **Geautomatiseerde Oplossing** als u een geautomatiseerd inzamelingsmodel voor deze integratie wilt gebruiken, dan specificeer de unieke herkenningstekens die voor deze integratie worden gebruikt. Als u deze optie selecteert, geeft u de unieke id&#39;s op die voor deze integratie worden gebruikt:<ul><li>Parameter tekenreeks voor query-id van bericht: Deze waarde vertegenwoordigt de bericht-id die door uw e-mailpartner aan de URL van de bestemmingspagina is toegevoegd.</li><li>Parameter voor tekenreeks ontvangerid-query: Deze waarde vertegenwoordigt de ontvanger-id die door uw e-mailpartner is toegevoegd aan de URL van de bestemmingspagina.</li></ul> |
| Dashboard en bladwijzergeneratie | Automatisch een dashboard en bladwijzers voor de integratie genereren. |
