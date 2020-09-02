---
source-git-commit: f20e0547c00f185659a2eabe0110f43c56c30114
workflow-type: tm+mt
translation-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---
# Productprofielen in Adobe Analytics

Productprofielen zijn een voorinstelling voor machtigingen die productbeheerders kunnen toewijzen aan gebruikers binnen een organisatie. Als u een productprofiel maakt en een Experience Cloud-gebruiker aan dat productprofiel toewijst, nemen deze de machtigingsitems in het productprofiel over.

Zie [Producten en profielen](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) beheren in de gebruikershandleiding voor bedrijven voor algemene informatie over productprofielen.

## Beheerders van productprofielen

Beheerders van productprofielen zijn een optionele groep die gebruikers aan dat productprofiel kan toevoegen of eruit kunnen verwijderen. Een productprofielbeheerder is niet hetzelfde als een productbeheerder:

* Beheerders van productprofielen hebben geen volledige toegang tot Adobe Analytics. Volledige toegang tot Adobe Analytics is voorbehouden aan productbeheerders.
* Beheerders van productprofielen kunnen machtigingsitems in hun productprofiel aanpassen.
* Beheerders van productprofielen kunnen productprofielen toewijzen aan of verwijderen uit gebruikersgroepen.
* Beheerders met productprofielen zijn ideaal voor teamleiders of managers die toegang tot Adobe Analytics voor hun team moeten verlenen en beheren. Individuen hoeven geen systeembeheerders of productbeheerders te storen om toegang te verlenen tot Adobe Analytics.

## Adobe Analytics-machtigingsitems

De minimaal vereiste rechten in een productprofiel voor toegang tot Adobe Analytics zijn:

* Het productprofiel moet toegang hebben tot ten minste één rapportsuite
* Het productprofiel moet behoren tot het machtigingsitem Analytics Tools **Analysis Workspace Access** (of **Reports &amp; Analytics Access**)

### Rapportsuites

Hiermee krijgt u toegang tot rapportreeksen die bij uw analyseorganisatie horen. Een gebruiker moet tot minstens één rapportenreeks behoren om toegang te hebben om Adobe Analytics te gebruiken.

### Metrics

Biedt toegang tot metriek in uw rapportenreeks. Metriek worden vermeld als hun respectieve component in Analysis Workspace, of als metrisch beschikbaar in Rapporten &amp; Analytics is, beschikbaar als menupunt onder de Metriek van de Plaats.

Aangepaste metriek krijgen het label &#39;Aangepaste gebeurtenis 1-1000&#39; om ze onafhankelijk te houden van rapportsuites. Als &#39;Aangepaste gebeurtenis 1&#39; een toegelaten toestemmingspunt is, heeft die gebruiker toegang tot event1 in alle rapportreeksen in het productprofiel.

### Dimensies

Biedt toegang tot dimensies in uw rapportsuite. Dimension worden vermeld als hun respectieve component in Analysis Workspace, of als de afmeting in Rapporten &amp; Analytics beschikbaar is, beschikbaar als menupunt.

Aangepaste variabelen, zoals eVars, krijgen het label &#39;Aangepaste omzetting 1-250&#39; om ze onafhankelijk te houden van rapportsuites. Als &#39;Aangepaste omzetting 1&#39; een toegelaten toestemmingspunt is, heeft die gebruiker toegang tot eVar1 in alle rapportreeksen in het productprofiel.

### Rapportsuite-gereedschappen

De punten van de de reekshulpmiddelen van het rapport verlenen toegang tot eigenschappen die voor de rapportsuites specifiek zijn de gebruiker heeft toegang tot. Zie [Report Suite Tools](report-suite-tools.md) voor een volledige lijst met machtigingsitems en beschrijvingen.

### Analysegereedschappen

De hulpmiddelen van de analysehulpmiddelen verlenen toegang tot eigenschappen die van de montages van de rapportreeks onafhankelijk zijn. Zie [Analysehulpmiddelen](analytics-tools.md) voor een volledige lijst van toestemmingspunten en beschrijvingen.

## Ontwikkelaars van productprofielen

Ontwikkelaars zijn vergelijkbaar met gebruikers, behalve dat ze de Experience Cloud API op Adobe I/O kunnen gebruiken. Zie [Ontwikkelaars](https://helpx.adobe.com/enterprise/using/manage-developers.html) beheren in de gebruikershandleiding voor bedrijven voor meer informatie.
