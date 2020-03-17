---
source-git-commit: d8f2458e7bae596dbabc8dab33ea5d2881047566
translation-type: tm+mt

---
# Productprofielen in Adobe Analytics

Productprofielen zijn een voorinstelling voor machtigingen die productbeheerders kunnen toewijzen aan gebruikers binnen een organisatie. Als u een productprofiel maakt en een Experience Cloud-gebruiker aan dat productprofiel toewijst, nemen deze de machtigingsitems in het productprofiel over.

Zie [Producten en profielen](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) beheren in de gebruikershandleiding voor bedrijven voor algemene informatie over productprofielen.

## Beheerders van productprofielen

Beheerders van productprofielen zijn een optionele groep die gebruikers aan dat productprofiel kan toevoegen of eruit kunnen verwijderen. Een productprofielbeheerder is niet hetzelfde als een productbeheerder:

* Beheerders van productprofielen zijn alleen verantwoordelijk voor de gebruikerslijst van een productprofiel.
* Beheerders van productprofielen hebben niet volledige toegang tot Adobe Analytics. Volledige toegang tot Adobe Analytics is gereserveerd voor productbeheerders.
* Beheerders van productprofielen kunnen de machtigingsitems in hun productprofiel niet aanpassen. a product admin moet toestemmings puntaanpassingen maken.
* Beheer van productprofielen is ideaal voor teamleiders of managers die eenvoudig toegang tot Adobe Analytics voor hun team moeten verlenen en beheren. Individuen hoeven geen systeembeheerders of productbeheerders in te schakelen om toegang te verlenen tot Adobe Analytics.

## Adobe Analytics-machtigingsitems

De minimaal vereiste rechten in een productprofiel voor toegang tot Adobe Analytics zijn:

* Het productprofiel moet toegang hebben tot ten minste één rapportsuite
* Het productprofiel moet behoren tot het machtigingspunt **Analyse van de Werkruimte** van de Analyse van de Hulpmiddelen (of **Rapporten &amp; Toegang** van de Analyse)

### Rapportageopties

Hiermee krijgt u toegang tot rapportreeksen die bij uw analyseorganisatie horen. Een gebruiker moet tot minstens één rapportsuite behoren om toegang te krijgen tot Adobe Analytics.

### Metrisch

Biedt toegang tot metriek in uw rapportenreeks. Metriek worden vermeld als hun respectieve component in de Werkruimte van de Analyse, of als metrisch in Rapporten &amp; Analytics beschikbaar is, beschikbaar als menupunt onder de Metriek van de Plaats.

Aangepaste metriek krijgen het label &#39;Aangepaste gebeurtenis 1-1000&#39; om ze onafhankelijk te houden van rapportsuites. Als &#39;Aangepaste gebeurtenis 1&#39; een toegelaten toestemmingspunt is, heeft die gebruiker toegang tot event1 in alle rapportreeksen in het productprofiel.

### Afmetingen

Biedt toegang tot dimensies in uw rapportsuite. De afmetingen worden vermeld als hun respectieve component in de Werkruimte van de Analyse, of als de afmeting in Rapporten &amp; Analytics beschikbaar is, beschikbaar als menupunt.

Aangepaste variabelen, zoals eVars, krijgen het label &#39;Aangepaste omzetting 1-250&#39; om ze onafhankelijk te houden van rapportsuites. Als &#39;Aangepaste omzetting 1&#39; een toegelaten toestemmingspunt is, heeft die gebruiker toegang tot eVar1 in alle rapportreeksen in het productprofiel.

### Rapportsuite-gereedschappen

De punten van de de reekshulpmiddelen van het rapport verlenen toegang tot eigenschappen die voor de rapportsuites specifiek zijn de gebruiker heeft toegang tot. Zie [Report Suite Tools](report-suite-tools.md) voor een volledige lijst met machtigingsitems en beschrijvingen.

### Analysegereedschappen

De hulpmiddelen van de analysehulpmiddelen verlenen toegang tot eigenschappen die van de montages van de rapportreeks onafhankelijk zijn. Zie [Analysehulpmiddelen](analytics-tools.md) voor een volledige lijst van toestemmingspunten en beschrijvingen.

## Ontwikkelaars van productprofielen

Ontwikkelaars zijn vergelijkbaar met gebruikers, maar hebben de mogelijkheid om de Experience Cloud-API te gebruiken voor Adobe I/O. Zie [Ontwikkelaars](https://helpx.adobe.com/enterprise/using/manage-developers.html) beheren in de gebruikershandleiding voor bedrijven voor meer informatie.
