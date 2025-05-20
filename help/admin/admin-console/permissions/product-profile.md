---
title: Productprofielen voor Adobe Analytics
description: Leer hoe productprofielen kunnen worden gebruikt als voorinstellingen voor machtigingen die productbeheerders kunnen toewijzen aan gebruikers binnen een organisatie.
exl-id: 834e4cf1-20b0-4c9d-939a-19e00494c8dd
feature: Admin Tools
role: Admin
source-git-commit: 8f1a17d2b07d5b37ef6d3d3f426234b29be61319
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Productprofielen voor Adobe Analytics

Productprofielen zijn voorinstellingen voor machtigingen die productbeheerders kunnen toewijzen aan gebruikers binnen een organisatie. Als u een productprofiel maakt en een Experience Cloud-gebruiker aan dat productprofiel toewijst, nemen deze de machtigingsitems in het productprofiel over.

Voor algemene informatie over productprofielen, met inbegrip van het creëren van productprofielen en het toewijzen van gebruikers, zie [ productprofielen voor ondernemingsgebruikers beheren ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) in de de gebruikersgids van de Onderneming.

## Beheerders van productprofielen

Beheerders van productprofielen zijn een optionele groep die gebruikers aan dat productprofiel kan toevoegen of eruit kunnen verwijderen. Een productprofielbeheerder is niet hetzelfde als een productbeheerder:

* Beheerders van productprofielen hebben geen volledige toegang tot Adobe Analytics. Volledige toegang tot Adobe Analytics is voorbehouden aan productbeheerders.
* Beheerders van productprofielen kunnen de machtigingsitems in hun productprofiel niet aanpassen.
* Beheerders van productprofielen kunnen productprofielen toewijzen aan of verwijderen uit gebruikersgroepen.
* Beheerders met productprofielen zijn ideaal voor teamleiders of managers die toegang tot Adobe Analytics voor hun team moeten verlenen en beheren. Individuen hoeven geen systeembeheerders of productbeheerders te storen om toegang te verlenen tot Adobe Analytics.

Voor informatie over hoe te om de beheerders van het productprofiel toe te wijzen, zie de sectie &quot;beheer van productprofiel&quot;in het artikel, [ beheer productprofielen voor ondernemingsgebruikers ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) in de gebruikersgids van de Onderneming.

## Adobe Analytics-machtigingsitems

De minimaal vereiste rechten in één productprofiel voor toegang tot Adobe Analytics zijn:

* Het productprofiel moet toegang hebben tot ten minste één rapportsuite
* Het productprofiel moet tot het de toestemmingspunt van de Hulpmiddelen van de Analyse **Toegang van het Project van Workspace** behoren.

### Rapportsuites

Hiermee krijgt u toegang tot rapportreeksen die bij uw analyseorganisatie horen. Een gebruiker moet tot minstens één rapportenreeks behoren om toegang te hebben om Adobe Analytics te gebruiken.

### Metrics

Biedt toegang tot metriek in uw rapportenreeks. Metriek worden als hun respectievelijke component weergegeven in Analysis Workspace.

Aangepaste metriek krijgen het label &#39;Aangepaste gebeurtenis 1-1000&#39; om ze onafhankelijk te houden van rapportsuites. Als &#39;Aangepaste gebeurtenis 1&#39; een toegelaten toestemmingspunt is, heeft die gebruiker toegang tot event1 in alle rapportreeksen in het productprofiel.

### Dimensies

Biedt toegang tot dimensies in uw rapportsuite. Dimensies worden vermeld als hun respectievelijke component in Analysis Workspace.

Aangepaste variabelen, zoals eVars, krijgen het label &#39;Aangepaste omzetting 1-250&#39; om ze onafhankelijk te houden van rapportsuites. Als &#39;Aangepaste conversie 1&#39; een toegelaten toestemmingspunt is, heeft die gebruiker toegang tot eVar1 in alle rapportreeksen in het productprofiel.

### Rapportsuite-gereedschappen

De punten van de de reekshulpmiddelen van het rapport verlenen toegang tot eigenschappen die voor de rapportsuites specifiek zijn de gebruiker heeft toegang tot. Zie {de Hulpmiddelen van de Reeks van het 0} Rapport ](report-suite-tools.md) voor een volledige lijst van toestemmingspunten en beschrijvingen.[

### Analysegereedschappen

De hulpmiddelen van de analysehulpmiddelen verlenen toegang tot eigenschappen die van de montages van de rapportreeks onafhankelijk zijn. Zie {de profieltoestemmingen van 0} Product voor Hulpmiddelen van Analytics ](analytics-tools.md) voor een volledige lijst van toestemmingspunten en beschrijvingen.[

## Ontwikkelaars van productprofielen

Ontwikkelaars zijn vergelijkbaar met gebruikers, maar ze krijgen de mogelijkheid om de Experience Cloud API op Adobe Developer te gebruiken. Zie [ Ontwikkelaars ](https://helpx.adobe.com/nl/enterprise/using/manage-developers.html) in de gebruikersgids van de Onderneming voor meer informatie leiden. Als een gebruiker ontwikkelaarstoegang voor om het even welk profiel wordt verleend, kunnen zij tot de Console van Dev (console.adobe.io) toegang hebben en de integraties van Adobe Analytics uitgeven. De API-aanroepen en antwoorden van Analytics die voor de gebruiker zijn geautoriseerd, zijn afhankelijk van de netmachtigingen van alle profielen waartoe de gebruiker toegang heeft als ontwikkelaar.

Met profielmachtigingen die alle metriek, alle dimensies en één rapportsuite bevatten, kan een ontwikkelaar bijvoorbeeld API-aanroepen relevant maken voor elke component in die rapportsuite. Als het machtigingsitem voor afwijkingsdetectie is toegevoegd, kunnen API-reacties afwijkende gegevens bevatten. Als vuistregel geldt dat als een profiel toegang verleent tot een scenario binnen de Adobe Analytics-interface, ontwikkelaarstoegang tot een profiel dat op dezelfde manier is gedefinieerd, overeenkomstige API-aanroepen en -antwoorden mogelijk maakt.
