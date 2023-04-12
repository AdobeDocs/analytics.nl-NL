---
title: Verwerkingsvolgorde voor gegevens in Adobe Analytics
description: Leer de volgorde van componenten en services die gegevens verwerken in Adobe Analytics.
exl-id: a8dc9c12-07d3-4dc8-b2df-136f7a7a1e77
source-git-commit: 34ba0e09cd909951a777b0ad3da080958633f97e
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---

# Verwerkingsvolgorde voor gegevens in Adobe Analytics

Adobe biedt verschillende manieren om gegevens te wijzigen of te bewerken voordat deze in de rapportage worden weergegeven. Op deze pagina ziet u de volgorde waarin verschillende Adobe Analytics-functies gegevens verwerken. U kunt deze lijst gebruiken om gegevensinconsistenties problemen op te lossen, of de beste eigenschap bepalen om te gebruiken wanneer de gegevensaanpassingen noodzakelijk zijn.

![Verwerkingsopdracht](assets/processing-order.png)

## Gegevens voordat deze naar Adobe worden verzonden

Voordat gegevens naar Adobe worden verzonden, worden doorgaans clientgegevens gecompileerd met een van de volgende methoden:

* **AppMeasurement**: Een JavaScript-bestand dat op uw site wordt gehost en waarnaar op elke pagina wordt verwezen. Gegevens worden rechtstreeks naar Adobe Analytics verzonden.
* **Adobe Experience Platform Web SDK**: Een JavaScript-bestand dat op uw site wordt gehost en waarnaar op elke pagina wordt verwezen. Gegevens worden verzonden naar Adobe Experience Edge.
* **Tags in Adobe Experience Cloud-gegevensverzameling**: Een JavaScript-bestand waarnaar op elke pagina wordt verwezen, met regels die zijn gemaakt in de gebruikersinterface voor gegevensverzameling. De Adobe Analytics-extensie biedt een eenvoudigere manier om AppMeasurement te implementeren. De uitbreiding van SDK van het Web biedt een gemakkelijkere manier aan om het Web SDK uit te voeren.

Als u gegevens naar Adobe Experience Edge verzendt, kunt u deze zo configureren dat gegevens worden doorgestuurd naar Adobe Analytics (en vele andere Adobe Experience Cloud-oplossingen). Ongeacht de implementatiemethode wordt uiteindelijk een afbeeldingsverzoek met de gewenste variabelen verzonden naar de Adobe-gegevensverzamelingsservers.

## Gegevens op het moment dat ze worden geleverd op Adobe Analytics-servers voor gegevensverzameling

Zodra de gegevens naar Adobe Analytics zijn verzonden, worden de gegevens door de volgende functies naar wens aangepast:

1. **Tabellen opzoeken**: Dimension die zich op Adobe-interne raadplegingslijsten baseren (bijvoorbeeld [Browser](/help/components/dimensions/browser.md) dimensie) wordt aangepast aan de corresponderende waarde.
2. [**Dynamische variabelen**](/help/implement/vars/page-vars/dynamic-variables.md): Als een dynamische variabele in om het even welk deel van een beeldverzoek wordt gezien, wordt de waarde gekopieerd over en behandeld als een onafhankelijke waarde die zich voorwaarts beweegt.
3. [**Bot-regels**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md): Pas standaard- of aangepaste bot-filters toe om die gegevens uit te sluiten van rapportage.
4. [**Verwerkingsregels**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md): Aangepaste regels die door uw organisatie op uw gegevens zijn toegepast. Omvat het in kaart brengen van [Contextgegevensvariabelen](/help/implement/vars/page-vars/contextdata.md) aan haar respectieve variabele.
5. **VISTA-regels**: Aangepaste flexibele regels toegepast op uw gegevens door een consultant voor Adobe. De regels van VISTA kunnen potentieel lopen vóór of na de regels van de Verwerking, afhankelijk van de behoeften van uw organisatie. De meeste regels VISTA lopen over het algemeen na de regels van de Verwerking, maar elke organisatie is opstelling verschillend. Neem contact op met uw Adobe-accountteam voor meer informatie over bestaande VISTA-regels.
6. [**Verwerkingsregels voor distributiekanalen**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md): U kunt [Verwerkingsregels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) gegevens voorbereiden voor gebruik in de verwerkingsregels voor marketingkanalen.
7. **Geolocatiegegevens**: Dimension die zich op IP adresraadpleging baseren (bijvoorbeeld [Landen](/help/components/dimensions/countries.md) -dimensie) worden gevuld.
8. [**IP obfuscatie**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md): Als uw organisatie ervoor heeft gekozen IP adressen in ruwe gegevens te verduisteren, wordt het gedaan nadat alle andere verwerkingsfuncties hebben voltooid.

Op dit punt, wordt de individuele klap geregistreerd in de lijsten van de rapportreeksgegevens. Na de standaard [latentie](latency.md) interval, is het beschikbaar in rapportering.

## Gegevens wijzigen nadat deze zijn verwerkt

De gegevens in Adobe Analytics zijn meestal permanent; er zijn echter enkele kenmerken die een selectieve aanpassing of verwijdering van gegevens mogelijk maken :

* [**API voor gegevensherstel**](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/): Bewerk bepaalde kolommen of verwijder de gewenste rijen met gegevens.
* [**Gegevensbeheer**](/help/admin/admin/c-data-governance/an-gdpr-workflow.md): Pas privacyverzoeken aan om gegevens permanent te verwijderen.
* [**Classificaties**](/help/components/classifications/c-classifications.md): Maak dimensies op basis van regels of geüploade gegevens waarmee u gegevens anders kunt ordenen. De onderliggende gegevens van de rapportreeks worden niet gewijzigd, zodat kunt u classificatiegegevens vrij uitgeven of beschrijven.
* [**Virtuele rapportsuites**](/help/components/vrs/vrs-about.md): Maak een alternatieve rapportsuite-weergave die de time-out van het bezoek kan wijzigen of die [Apparaatanalyse](/help/components/cda/overview.md).
