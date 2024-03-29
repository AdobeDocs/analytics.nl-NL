---
title: Verwerkingsvolgorde voor gegevens in Adobe Analytics
description: Leer de volgorde van componenten en services die gegevens verwerken in Adobe Analytics.
exl-id: a8dc9c12-07d3-4dc8-b2df-136f7a7a1e77
feature: Data Configuration and Collection
source-git-commit: 914b822aae659d1d0f0b8a98480090ead99e102a
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---

# Verwerkingsvolgorde voor gegevens in Adobe Analytics

Adobe biedt verschillende manieren om gegevens te wijzigen of te bewerken voordat deze in de rapportage worden weergegeven. Op deze pagina ziet u de volgorde waarin verschillende Adobe Analytics-functies gegevens verwerken. U kunt deze lijst gebruiken om gegevensinconsistenties problemen op te lossen, of de beste eigenschap bepalen om te gebruiken wanneer de gegevensaanpassingen noodzakelijk zijn.

![Verwerkingsopdracht](assets/processing-order.png)

## Gegevens voordat deze naar de Adobe worden verzonden

Voordat gegevens naar de Adobe worden verzonden, worden doorgaans clientgegevens gecompileerd met een van de volgende methoden:

* **AppMeasurement**: Een JavaScript-bestand dat op uw site wordt gehost en waarnaar op elke pagina wordt verwezen. Gegevens worden rechtstreeks naar Adobe Analytics verzonden.
* **Adobe Experience Platform Web SDK**: Een JavaScript-bestand dat op uw site wordt gehost en waarnaar op elke pagina wordt verwezen. Gegevens worden naar het Adobe Experience Platform Edge-netwerk verzonden.
* **Tags in Adobe Experience Cloud-gegevensverzameling**: Een JavaScript-bestand waarnaar op elke pagina wordt verwezen, met regels die zijn gemaakt in de gebruikersinterface voor gegevensverzameling. De extensie Adobe Analytics biedt een eenvoudigere manier om AppMeasurement te implementeren. De uitbreiding van SDK van het Web biedt een gemakkelijkere manier aan om het Web SDK uit te voeren.

Als u gegevens naar het Edge-netwerk verzendt, kunt u deze zo configureren dat gegevens naar Adobe Analytics (en vele andere Adobe Experience Cloud-oplossingen) worden doorgestuurd. Ongeacht de implementatiemethode wordt uiteindelijk een afbeeldingsverzoek met de gewenste variabelen verzonden naar de servers voor gegevensverzameling van de Adobe.

## Gegevens op het moment dat ze worden geleverd op Adobe Analytics-servers voor gegevensverzameling

Zodra de gegevens naar Adobe Analytics zijn verzonden, worden de gegevens door de volgende functies naar wens aangepast:

1. **Tabellen opzoeken**: Dimensionen die zich op Adobe-interne raadplegingslijsten baseren (bijvoorbeeld [Browser](/help/components/dimensions/browser.md) dimensie) wordt aangepast aan de corresponderende waarde.
2. [**Dynamische variabelen**](/help/implement/vars/page-vars/dynamic-variables.md): Als een dynamische variabele in een willekeurig deel van een afbeeldingsaanvraag wordt weergegeven, wordt de waarde gekopieerd en behandeld als een onafhankelijke waarde die voorwaarts wordt verplaatst.
3. [**Bot-regels**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md): Pas standaard- of aangepaste bot-filters toe om die gegevens uit te sluiten van rapportage.
4. [**Verwerkingsregels**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md): Aangepaste regels toegepast op uw gegevens door uw organisatie. Omvat de toewijzing van [Contextgegevensvariabelen](/help/implement/vars/page-vars/contextdata.md) aan haar respectieve variabele.
5. **VISTA-regels**: Aangepaste flexibele regels toegepast op uw gegevens door een consultant van de Adobe. De regels van VISTA kunnen potentieel lopen vóór of na de regels van de Verwerking, afhankelijk van de behoeften van uw organisatie. De meeste regels VISTA lopen over het algemeen na de regels van de Verwerking, maar elke organisatie is opstelling verschillend. Neem contact op met het accountteam van uw Adobe voor meer informatie over bestaande VISTA-regels.
6. [**Verwerkingsregels voor distributiekanalen**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md): U kunt [Verwerkingsregels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) gegevens voorbereiden voor gebruik in de verwerkingsregels voor marketingkanalen.
7. **Geolocatiegegevens**: Dimensionen die zich op IP adresraadpleging baseren (bijvoorbeeld [Landen](/help/components/dimensions/countries.md) -dimensie) worden gevuld.
8. [**IP obfuscatie**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md): Als uw organisatie ervoor heeft gekozen IP adressen in ruwe gegevens te verduisteren, wordt het gedaan nadat alle andere verwerkingsfuncties hebben voltooid.

Op dit punt, wordt de individuele klap geregistreerd in de lijsten van de rapportreeksgegevens. Na de standaard [latentie](latency.md) interval, is het beschikbaar in rapportering.

## Gegevens wijzigen nadat deze zijn verwerkt

De gegevens in Adobe Analytics zijn meestal permanent, maar er zijn enkele functies die selectieve gegevensaanpassingen of -verwijdering mogelijk maken:

* [**API voor gegevensherstel**](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/): Bewerk bepaalde kolommen of verwijder de gewenste rijen met gegevens.
* [**Gegevensbeheer**](/help/admin/admin/c-data-governance/an-gdpr-workflow.md): Pas privacyverzoeken aan om gegevens permanent te verwijderen.
* [**Classificaties**](/help/components/classifications/c-classifications.md): Maak dimensies op basis van regels of geüploade gegevens waarmee u gegevens anders kunt ordenen. De onderliggende gegevens van de rapportreeks worden niet gewijzigd, zodat kunt u classificatiegegevens vrij uitgeven of beschrijven.
* [**Virtuele rapportsuites**](/help/components/vrs/vrs-about.md): Maak een alternatieve rapportsuite-weergave die de time-out van het bezoek kan wijzigen of die toestaat [Apparaatanalyse](/help/components/cda/overview.md).
