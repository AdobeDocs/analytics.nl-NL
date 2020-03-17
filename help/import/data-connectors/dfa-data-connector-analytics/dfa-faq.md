---
description: 'null'
keywords: DFA
title: Veelgestelde vragen
topic: Data connectors
uuid: 59d187e9-1ec1-4cf3-8831-b981f87c9372
translation-type: tm+mt
source-git-commit: ''

---


# Veelgestelde vragen{#frequently-asked-questions}

## Waarom accepteert de wizard Gegevensverbindingen mijn aanmeldingsgegevens niet? {#section-f019b3de18774df3954af7881aa564fa}

Als u hebt geverifieerd dat de aanmeldingsgegevens geldig zijn, controleert u vervolgens of de gebruikersnaam die aan de integratie is verstrekt, is ingeschakeld voor API-toegang. De wizard Gegevensverbindingen gebruikt de DFA API om aanmeldingsgegevens te valideren en schakelt Adobe-specifieke instellingen in de DFA API uit en in. API de Toegang is het plaatsen die van binnen de interface DFA door een beheerder moet worden aangezet. Controleer vervolgens of u toestemming hebt om toegang te krijgen tot de Advertiser-id of de Floodlight Configuration-id die in de wizard is geselecteerd.

## Waarom zie ik geen gegevens van de nielsgeüploade metriek (DFA Impressions, DFA Clicks, enz.)? {#section-465fd22ae6b447ffb6baf20b57daa433}

Als u versie 1.5 van de integratie gebruikt, zou dit kunnen zijn omdat uw integratie nog geen identiteitskaart van de Plaats van de Cliënt is toegewezen. Een identiteitskaart van de Plaats van de Cliënt (CSID) wordt vereist voor de nachtelijke uitwisseling om voor te komen, en om gegevens van DFA en server te verzoeken. CSID&#39;s kunnen maximaal drie dagen duren vanaf de datum van integratie die met Google moet worden uitgewisseld. Zodra CSID van Google is ontvangen, zult u via het e-mailadres van de integratie van nieuwe CSID, samen met de recentste code worden op de hoogte gebracht JavaScript.

Als het meer dan 3 dagen is geweest en u niet opstellings-e-mail hebt ontvangen en de metriek stromen niet, dan is het meest waarschijnlijke probleem dat CSID reeds aan een andere integratie is toegewezen. Google onderhoudt een 1 tot 1 afbeelding tussen CSID en Report Suite. Dit houdt in dat als een integratie in één rapportsuite dezelfde Advertiser-id gebruikt als een andere integratie in een andere rapportsuite, alleen de eerste aan een CS-id zal worden toegewezen. Als u wilt wijzigen aan welke rapportsuite of Advertiser-id een CSID is toegewezen, moet u een ticket openen met Google Support.

Bijvoorbeeld, zeg er een integratie in Reeks A van het Rapport met Advertiser identiteitskaart Z is die toegewezen CSID krijgt. Als een andere integratie later opstelling in Reeks B van het Rapport met Advertiser Z is, zal deze nieuwere integratie NIET opnieuw toegewezen CSID worden. Hiervoor is een Google-ticket nodig. Anderzijds, neem het voorbeeld van een integratie in Report Suite A, met Advertiser ID Z, en later een andere integratie in Report Suite A, wordt Advertiser Z opstelling. Alleen de eerste integratie zal gegevens voor de integratie ontvangen; in dit geval kan de eerste integratie echter worden gedeactiveerd en zullen de gegevens naar de tweede integratie gaan .

> [!NOTE] CSIDs wordt niet gebruikt in versie 2.0 van de integratie en zo is het onderhandelingsproces van CSID niet van toepassing.

## Ik gebruik versie 2.0 van de integratie en de kostenmetriek verschijnen niet voor mijn DFA advertenties. Waarom zou dat zo zijn? {#section-805748111bbe4bbf918d6dbbb2641fff}

Kostenmaatstaven moeten zowel vanuit de Google DFA-zijde worden ingeschakeld als in de DFA-interface worden geleverd en ingeschakeld in de wizard Gegevensconnectors. De eerste plaats om te verifiëren is dat u een gebeurtenis Analytics voor DFA Media Kosten in kaart hebt gebracht, en een muntcode verstrekt. Als u de Media Cost-gebeurtenis hebt toegewezen en de wizard hebt voltooid en opgeslagen, wordt de DFA omnitureCostData-vlag ingeschakeld in de DFA API. Dit zal aan Google duidelijk maken dat de metriek in het nachtelijke dossier zou moeten worden verzonden. U kunt via de DFA-interface controleren of omnitureCostData is ingeschakeld door eigenschappen op de geïntegreerde Floodlight te bekijken. Nadat u deze twee plaatsen hebt gecontroleerd, zorgt u er ten slotte voor dat de advertenties die deel uitmaken van de geïntegreerde functie Vullicht, kostengegevens en kostenstructuren opgeven. Als de kostengegevens niet in de interface DFA worden verstrekt, zal het niet in Analytics verschijnen.

## Waarom geven bepaalde advertenties geen DFA-indrukkingen of doorkijkcijfers weer, maar ze tonen wel kliks en doorklikken? {#section-39b2eeeefd7f43d1a373df0b987bacef}

Er zijn enkele advertenties die alleen klikgegevens opnemen, ook wel kliktrackers genoemd. Dit type advertenties retourneert geen laatste imitatiegegevens vanaf het moment dat de Floodlight-server wordt opgevraagd. Als u wilt controleren of een bepaalde advertentie een kliktracker of alleen-klikadvertentie is, neemt u contact op met uw DFA-bureau of uw Google Support-vertegenwoordiger.

## Waarom zijn er geen doorklikpogingen voor advertenties die DFA Kliks tonen? {#section-758c1f1fc5b54bfc9294dcdc71bbd96a}

Daar kan een van de vele antwoorden op zijn.

Controleer eerst of de desbetreffende advertentie een bestemmingspagina-URL heeft die (a) gelabeld is met Adobe-code voor dezelfde rapportsuite die u bekijkt en (b) de parameter voor de *`clickThroughParam`* queryreeks bevat.

Ten tweede, verifieer dat u een werkende integratie hebt door de stappen te volgen in het [Bevestigen van een Succesvolle Integratie](../dfa-data-connector-analytics/dfa-integration.md)DFA. Als er een DFA-trackingcode wordt weergegeven bij de Adobe-hit op de bestemmingspagina, ziet u dat Click-through wordt weergegeven in het rapport DFA-campagnes. Als u het niet ziet door komen, verifieer dat de rapportreeksen tussen de *`s.account`* variabele van de landingspagina aanpassen, en de rapportreeks die in Rapporten &amp; Analytics wordt bekeken. Als deze overeenkomen, controleert u de volgcodes in het rapport Weergeven via eVar die eruitzien als DFA:XXX:XXX:XXX:llXXX:XXX:XXX:XXX:XXX:XXX.

Deze tonen aan mislukkingen van de DFA VISTA-regel om de ruwe gegevens van DFA samen te vatten. Dit probleem kan worden verholpen door een ondersteuningsticket te openen via uw Adobe-accountvertegenwoordiger.

Als geen van de bovenstaande oplossingen het probleem verklaart, zie het [Reconciling van Metrische discrepanties](../dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies.md) om andere mogelijkheden te onderzoeken.
