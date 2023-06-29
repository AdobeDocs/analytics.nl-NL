---
title: Productprofielen voor Adobe Analytics
description: Leer hoe productprofielen kunnen worden gebruikt als voorinstellingen voor machtigingen die productbeheerders kunnen toewijzen aan gebruikers binnen een organisatie.
exl-id: 834e4cf1-20b0-4c9d-939a-19e00494c8dd
feature: Admin Tools
source-git-commit: 1a7b853d6f5fc627223ea69e64b4a240c61aef2a
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 1%

---

# Productprofielen voor Adobe Analytics

Productprofielen zijn voorinstellingen voor machtigingen die productbeheerders kunnen toewijzen aan gebruikers binnen een organisatie. Als u een productprofiel maakt en een Experience Cloud-gebruiker aan dat productprofiel toewijst, nemen deze de machtigingsitems in het productprofiel over.

Voor algemene informatie over productprofielen, zoals het maken van productprofielen en het toewijzen van gebruikers, raadpleegt u [Productprofielen beheren voor zakelijke gebruikers](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) in de gebruikershandleiding voor de onderneming.

## Beheerders van productprofielen

Beheerders van productprofielen zijn een optionele groep die gebruikers aan dat productprofiel kan toevoegen of eruit kunnen verwijderen. Een productprofielbeheerder is niet hetzelfde als een productbeheerder:

* Beheerders van productprofielen hebben geen volledige toegang tot Adobe Analytics. Volledige toegang tot Adobe Analytics is voorbehouden aan productbeheerders.
* Beheerders van productprofielen kunnen de machtigingsitems in hun productprofiel niet aanpassen.
* Beheerders van productprofielen kunnen productprofielen toewijzen aan of verwijderen uit gebruikersgroepen.
* Beheerders met productprofielen zijn ideaal voor teamleiders of managers die toegang tot Adobe Analytics voor hun team moeten verlenen en beheren. Individuen hoeven geen systeembeheerders of productbeheerders te storen om toegang te verlenen tot Adobe Analytics.

Zie de sectie ‘Beheer van productprofielbeheerders’ in het artikel voor informatie over het toewijzen van productprofielbeheerders. [Productprofielen beheren voor zakelijke gebruikers](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) in de gebruikershandleiding voor de onderneming.

## Adobe Analytics-machtigingsitems

De minimaal vereiste rechten in een productprofiel voor toegang tot Adobe Analytics zijn:

* Het productprofiel moet toegang hebben tot ten minste één rapportsuite
* Het productprofiel moet behoren tot het machtigingsitem Analytics Tools **Analysis Workspace Access** (of **Toegang tot rapporten en analyses**)

### Rapportsuites

Hiermee krijgt u toegang tot rapportreeksen die bij uw analyseorganisatie horen. Een gebruiker moet tot minstens één rapportenreeks behoren om toegang te hebben om Adobe Analytics te gebruiken.

### Metrics

Biedt toegang tot metriek in uw rapportenreeks. Metriek worden vermeld als hun respectieve component in Analysis Workspace, of als metrisch beschikbaar in Rapporten &amp; Analytics is, beschikbaar als menupunt onder de Metriek van de Plaats.

Aangepaste metriek krijgen het label &#39;Aangepaste gebeurtenis 1-1000&#39; om ze onafhankelijk te houden van rapportsuites. Als &#39;Aangepaste gebeurtenis 1&#39; een toegelaten toestemmingspunt is, heeft die gebruiker toegang tot event1 in alle rapportreeksen in het productprofiel.

### Dimensies

Biedt toegang tot dimensies in uw rapportsuite. Dimension worden vermeld als hun respectieve component in Analysis Workspace, of als de afmeting in Rapporten &amp; Analytics beschikbaar is, beschikbaar als menupunt.

Aangepaste variabelen, zoals eVars, krijgen het label &#39;Aangepaste omzetting 1-250&#39; om ze onafhankelijk te houden van rapportsuites. Als &#39;Aangepaste omzetting 1&#39; een toegelaten toestemmingspunt is, heeft die gebruiker toegang tot eVar1 in alle rapportreeksen in het productprofiel.

### Rapportsuite-gereedschappen

De punten van de de reekshulpmiddelen van het rapport verlenen toegang tot eigenschappen die voor de rapportsuites specifiek zijn de gebruiker heeft toegang tot. Zie [Rapportsuite-gereedschappen](report-suite-tools.md) voor een volledige lijst van toestemmingspunten en beschrijvingen.

### Analysegereedschappen

De hulpmiddelen van de analysehulpmiddelen verlenen toegang tot eigenschappen die van de montages van de rapportreeks onafhankelijk zijn. Zie [Machtigingen voor productprofielen voor Analytics Tools](analytics-tools.md) voor een volledige lijst van toestemmingspunten en beschrijvingen.

## Ontwikkelaars van productprofielen

Ontwikkelaars zijn vergelijkbaar met gebruikers, behalve dat ze de Experience Cloud API voor Adobe-ontwikkelaars kunnen gebruiken. Zie [Ontwikkelaars beheren](https://helpx.adobe.com/nl/enterprise/using/manage-developers.html) in de gebruikershandleiding voor bedrijven voor meer informatie. Als aan een gebruiker voor een profiel toegang tot de ontwikkelaar wordt verleend, hebben deze toegang tot de Dev Console (console.adobe.io) en kunnen de Adobe Analytics-integraties worden bewerkt. De API-aanroepen en antwoorden van Analytics die voor de gebruiker zijn geautoriseerd, zijn afhankelijk van de netmachtigingen van alle profielen waarin die gebruiker Developer Access heeft.

Met profielmachtigingen, inclusief alle metriek, alle dimensies en één rapportsuite, kan een Developer Access-lid van het profiel API-aanroepen relevant maken voor elke component in de relevante suite. Als Anomaly Detection is toegevoegd, kunnen de rapporten uitgebreidere reacties bevatten, waarbij de afwijkende gegevens worden toegevoegd. Als vuistregel geldt dat als een profiel toegang verleent tot een scenario binnen de Adobe Analytics-interface, ontwikkelaarstoegang voor een profiel dat op dezelfde manier is gedefinieerd, overeenkomstige API-aanroepen en -antwoorden mogelijk maakt.
