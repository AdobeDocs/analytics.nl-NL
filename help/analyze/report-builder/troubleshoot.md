---
description: Manieren u de levering van de rapportbouwer, en een lijst van foutenmeldingen optimaliseren die af en toe konden voorkomen.
title: Het oplossen van problemen en beste praktijken voor de Bouwer van het Rapport
topic: Report builder
uuid: 36a08143-dc78-40f5-9ce9-7d16980aa27b
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Het oplossen van problemen en beste praktijken voor de Bouwer van het Rapport

Manieren u de levering van de rapportbouwer, en een lijst van foutenmeldingen optimaliseren die af en toe konden voorkomen.

## De gebruikers van de Bouwer van het rapport 5.0 en het openen van 5.1 werkboeken {#section_C29898775999453FABB5FB0E098415C8}

Adobe heeft het scheidingsteken tussen afmetingen en classificaties gewijzigd van een onderstrepingsteken (_) in||. Deze verandering heeft verenigbaarheidsimplicaties voor een gebruiker van de Bouwer van het Rapport 5.0 die een werkboek van de Bouwer van het Rapport v5.1 met classificatieverzoeken opent. Telkens wanneer een werkboek van een versie ouder dan v5.1 wordt geopend, zullen al zijn geserialiseerde classificatieverzoeken in dit formaat worden omgezet.

Dit introduceert een voorwaarts compatibiliteitsprobleem: Zodra omgezet in v5.1, als een werkboek met een gebruiker op de Bouwer van het Rapport v5.0 wordt gedeeld, zal die gebruiker niet het classificatieverzoek kunnen erkennen (inderdaad, zoekt het &quot;_&quot;maar v5.1 geserialiseerde &quot;||&quot;).

U zult het volgende neveneffect ervaren wanneer het openen van een werkboek ARB v5.1 met classificatieverzoek:

* Wanneer het openen van het werkboek, zult u de volgende waarschuwing krijgen: &quot;Dit werkboek werd het laatst bewaard gebruikend de Bouwer van het Rapport v5.1. Deze versie heeft sommige eigenschappen geïntroduceerd die met de versie van de Bouwer van het Rapport onverenigbaar zijn die op deze computer wordt geïnstalleerd. Het wordt hoogst geadviseerd dat u aan de recentste versie van de Bouwer van het Rapport alvorens dit werkboek bij te werken bevordert.&quot;
* Als u een ARB- verzoek met classificatie met de rechtermuisknop aanklikt, zullen de de contextmenu&#39;s van de Bouwer van het Rapport (geef verzoek uit, voeg afhankelijk verzoek toe...) niet verschijnen.
* Als u Vernieuwen allen uitvoert, door de derde knoop te klikken, of door een reeks verzoeken van de vorm van de Manager van het Verzoek te verfrissen, zal het classificatieverzoek zonder fout uitvoeren. De classificatiewaarden worden echter niet opgemaakt.
* U kunt het verzoek nog uitgeven door de Manager van het Verzoek te openen, dan die van rij aan rij gaat, tot het de juiste verzoek bereikt.
* Als u de aanvraag bewerkt en alle parameters ongewijzigd laat en vervolgens op Voltooien klikt, wordt de reactie op de juiste wijze weggeschreven. Als u het verzoek bewerkt, wordt het probleem opgelost wanneer de parameters voor de indeling van de respons opnieuw worden geserialiseerd. Er is dus een tijdelijke oplossing, hoewel het tijdrovend is.

## Verificatiekwesties in Report Builder {#section_FD79104DF1414FE2B36591606C963DE6}

De Bouwer van het rapport vereist authentificatie om gegevensverzoeken van uw rapportsuites tot stand te brengen. Soms zijn er kwesties het aanmelden aan rapportbuilder afhankelijk van uw montages binnen [!DNL Analytics] of uw netwerk.

**Ongeldige aanmeldmaatschappij**

Deze fout komt het meest meestal voor wanneer of het login bedrijf incorrect is ingegaan, of als er de kwesties van de netwerkactiviteit zijn. Ga als volgt te werk:

* Controleer de spelling van het aanmeldingsbedrijf om te controleren of er geen typefout of foutruimte is.
* Meld u bij Analytics aan bij hetzelfde aanmeldingsbedrijf om te controleren of de gegevens juist zijn. Als u zich niet met die geloofsbrieven kunt aanmelden, contacteer één van de beheerders van uw organisatie om het correcte login bedrijf te verkrijgen.

**Firewall**

De Bouwer van het rapport gebruikt havens 80 en 443. Zorg ervoor dat deze poorten zijn toegestaan via de firewall van uw organisatie. Zie ook de Interne IP van Adobe Adressen voor extra firewalluitsluitingen.

## Aanbevelingen voor het optimaliseren van aanvragen {#section_33EF919255BF46CD97105D8ACB43573F}

De volgende factoren kunnen de complexiteit van aanvragen verhogen en tot een langzamere verwerking leiden:

**Factoren die leveringen kunnen vertragen**

* Te veel bladwijzers, dashboards en de werkboeken van de Bouwer van het Rapport werden gepland binnen een paar uur
* Te veel werkboeken van de Bouwer van het Rapport werden gepland rond de zelfde tijd. Wanneer dit voorkomt, wordt de rapport API rij achtergeregistreerd.

**Factoren die werkboekruntime kunnen vertragen**

* Aanzienlijke toename van classificaties.
* Het bereik van de aanvraagdatum in de loop van de tijd vergroten.

   **Voorbeeld**: Stel dat u een trendverzoek maakt met de instelling Huidig jaar, uitgesplitst op daggranulariteit. Aan het einde van het jaar zal het verzoek meer periodes retourneren dan aan het begin van het jaar.

   `(January 1 - January 30 versus January 1 - December 31.)`

**Veroorzaakt dat in de mislukking van de werkboeklevering resulteert**

De complexe formules van Excel in een werkboek, in het bijzonder degenen die datum en tijd impliceren.

**Cellen die 0s (geen waarden) terugkeren**

Een apostrof of één enkel citaat in de het bladnaam van Excel zal rapportaannemer veroorzaken om geen waarden terug te keren. (Dit is een Microsoft Excel-beperking.)

**Afzonderlijke verzoekprestaties**

De verwerkingssnelheid kan worden beïnvloed door de volgende instellingen:

| Instelling | Snellere prestaties | Lagere prestaties |
|--- |--- |--- |
| Uitsplitsingen en uitsplitsingsvolgorde | Weinig | Veel |
|  | Voorbeeld: Als u A indeelt door Z, zou het aantal punten voor A altijd minder moeten zijn dan het aantal punten voor Z. Als dit andersom is, kan de aanvraagtijd aanzienlijk toenemen. |
| Datumbereik | Klein bereik | Breed bereik |
| Filteren | Specifieke filtering | Populairste filtering |
| Korreligheid | Geaggregeerd | Uur<ul><li>Dagelijks</li><li>Wekelijks</li><li>Maandelijks</li><li>Driemaandelijks</li><li>Jaarlijks</li></ul> |
| Aantal vermeldingen | Kleine gegevensset | Grote gegevensset |


**Planningstijd**

Stapelplanning over een periode van 24 uur (zie onderstaande tabel). Bestaande bladwijzers, dashboards, en de werkboeken van de Bouwer van het Rapport die samen worden gepland kunnen vertragingen veroorzaken.

Plan grotere, complexere verzoeken in de vroege ochtend om voor handimpulsen en verfrissing toe te staan om tijdens de bedrijfsdag voor te komen.

| Planningstijd | 01:00 - 2.00 uur | 02:00 - 07.00 uur | 07:00 - 18:00 | 18:00 - Middernacht |
|--- |--- |--- |--- |--- |
| Gebruik van Report Builder | Quiet | Heel druk | Gebruik op de client.<br>Hogere volumes van gebruikers die lokaal vernieuwen en vragen om &quot;direct verzenden&quot;.<br>Bovendien, verifieer of de API rij wanneer geplande werkboeken uit tijd wordt ontruimd. | Niet bezig |

**Tijdstippen**

Alle geplande rapporttijden na vier uur. Het systeem probeert nog drie keer te plannen, wat mogelijk resulteert in een fout. (Over het algemeen duurt het langer om de gegevensset te kunnen uitvoeren naarmate de gegevensset groter wordt.) Deze kunnen in rapportering en de Bouwer van het Rapport worden gezien: [!DNL Analytics]

* [!DNL Analytics]: **[!UICONTROL Favorites]** > **[!UICONTROL Scheduled Reports]**

* Report Builder: Klik **[!UICONTROL Management]** op het [!UICONTROL Add-ins] tabblad in Excel.

## Foutberichten {#section_3DF3A1EEDAD149CB941BEABEF948A4A5}

Een lijst met foutberichten die soms kunnen optreden terwijl u Report Builder gebruikt.

>[!NOTE] Dit is slechts een selectie van foutberichten en geen uitputtende lijst. Neem contact op met de beheerder voor meer informatie over het oplossen van fouten.

**Deze eigenschap kan slechts op een open werkboek worden toegepast.**

Als geen werkboeken (spreadsheetdocumenten) in Excel open zijn, en u één van de pictogrammen in de toolbar van de rapportbouwer klikt, wordt dit bericht getoond. Bovendien wordt de werkbalk uitgeschakeld totdat u een spreadsheet opent. U kunt echter op het online Help-pictogram klikken terwijl de werkbalk nog steeds is ingeschakeld zonder dat deze fout optreedt.

**U moet eerst het programma afsluiten[!UICONTROL Request Wizard]voordat u het[!UICONTROL Request Manager]activeert.**

Terwijl de [!UICONTROL Request Manager] en de [!UICONTROL Request Wizard] zijn functioneel verbonden, is het niet mogelijk om met het te werken [!UICONTROL Request Manager] alvorens acties te voltooien of te annuleren die in de [!UICONTROL Request Wizard].

**Er is geen verzoek aan dit bereik gekoppeld.**

Dit foutbericht treedt op als u op de [!UICONTROL From Sheet] knop in de werkbalk klikt [!UICONTROL Request Manager] wanneer een cel van het werkblad geen aanvragen bevat.

Om te identificeren welke cellen in het spreadsheet verzoeken bevatten, klik individuele verzoeken die in de lijst in de [!UICONTROL Request Manager]lijst worden vermeld. Als een aanvraag is gekoppeld aan cellen, worden de cellen gemarkeerd weergegeven wanneer de aanvraag in de tabel wordt geselecteerd.

**Het geselecteerde bereik is ongeldig. Selecteer een ander bereik.**

Als een cel van het werkblad is geselecteerd en er al een aanvraag aan is toegewezen, treedt deze fout op. Verwijder de aanvraag die aan de cellen is toegewezen of kies een andere reeks cellen die u wilt toewijzen.

Wanneer u cellen wilt verwijderen, is het belangrijk dat u cellen zoekt die aanvragen bevatten en de aanvraag verwijdert voordat u de cellen verwijdert (rijen of kolommen verwijdert).

**Sluit de Excel-cel met focus af voordat u deze functie gebruikt.**

Als u op *uitgeeft wijze* in een cel van Excel bent en één van de pictogrammen van de Bouwer van het Rapport klikt, verschijnt dit foutenbericht. De bewerkingsmodus in een Excel-cel betekent dat de cel is geselecteerd en de cursor in de cel wordt weergegeven. U bent ook in uitgeeft wijze in een cel van Excel wanneer u direct in de [!UICONTROL Formula] bar of in de [!UICONTROL Name Box] bovenkant van Excel typt.

**Het geselecteerde bereik snijdt het bereik van een andere aanvraag door. Wijzig de selectie.**

Als u al een set cellen aan het werkblad hebt toegewezen, wordt deze fout weergegeven.

Een manier om te bepalen welke cellen worden toegewezen voordat u nieuwe aanvragen toevoegt, is het sluiten [!UICONTROL Request Wizard] en het openen van het [!UICONTROL Request Manager]bestand. Selecteer vervolgens de items die een voor een in de overzichtstabel voor aanvragen worden vermeld. Wanneer u een verzoek in de lijst selecteert, worden de corresponderende cellen met aanvraagtoewijzingen in het werkblad gemarkeerd.

Dit is een van de redenen waarom u cellen moet markeren met markering, rij- of kolominformatie of een opmaakstijl voordat u meerdere cellen aan meerdere gebieden toewijst.
