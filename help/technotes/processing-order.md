---
title: Verwerkingsvolgorde voor gegevens in Adobe Analytics
description: Leer de volgorde van componenten en services die gegevens verwerken in Adobe Analytics.
exl-id: a8dc9c12-07d3-4dc8-b2df-136f7a7a1e77
feature: Data Configuration and Collection
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---

# Verwerkingsvolgorde voor gegevens in Adobe Analytics

Adobe biedt verschillende manieren om gegevens te wijzigen of te bewerken voordat deze in de rapportage worden weergegeven. Op deze pagina ziet u de volgorde waarin verschillende Adobe Analytics-functies gegevens verwerken. U kunt deze lijst gebruiken om gegevensinconsistenties problemen op te lossen, of de beste eigenschap bepalen om te gebruiken wanneer de gegevensaanpassingen noodzakelijk zijn.

![Verwerkingsopdracht](assets/processing-order.png)

## Gegevens voordat deze naar Adobe worden verzonden

Voordat gegevens naar Adobe worden verzonden, worden deze doorgaans op de client gecompileerd met een van de volgende methoden:

* **AppMeasurement**: Een dossier van JavaScript dat op uw plaats wordt ontvangen en op elke pagina van verwijzingen wordt voorzien. Gegevens worden rechtstreeks naar Adobe Analytics verzonden.
* **SDK van het Web van Adobe Experience Platform**: Een dossier van JavaScript dat op uw plaats wordt ontvangen en op elke pagina van verwijzingen voorzien. De gegevens worden naar de Adobe Experience Platform Edge Network verzonden.
* **Markeringen in de Inzameling van Gegevens van Adobe Experience Cloud**: Een dossier van JavaScript dat op elke pagina van verwijzingen wordt voorzien, die regels bevatten die binnen UI van de Inzameling van Gegevens worden gecreeerd. De Adobe Analytics-extensie biedt een eenvoudigere manier om AppMeasurement te implementeren. De extensie Web SDK biedt een eenvoudigere manier om de Web SDK te implementeren.

Als u gegevens naar de Edge Network verzendt, kunt u deze zo configureren dat gegevens naar Adobe Analytics (en vele andere Adobe Experience Cloud-oplossingen) worden doorgestuurd. Ongeacht de implementatiemethode wordt uiteindelijk een afbeeldingsaanvraag met de gewenste variabelen verzonden naar Adobe-servers voor gegevensverzameling.

## Gegevens op het moment dat ze worden geleverd op Adobe Analytics-servers voor gegevensverzameling

Zodra de gegevens naar Adobe Analytics zijn verzonden, worden de gegevens door de volgende functies naar wens aangepast:

1. **Lookup lijsten**: Dimensies die zich op Adobe-interne raadplegingslijsten (bijvoorbeeld, de [ Browser ](/help/components/dimensions/browser.md) dimensie) baseren worden aangepast aan zijn overeenkomstige waarde.
2. [**Dynamische variabelen**](/help/implement/vars/page-vars/dynamic-variables.md): Als een dynamische variabele in om het even welk deel van een beeldverzoek wordt gezien, wordt de waarde gekopieerd over en behandeld als onafhankelijke waarde die zich voorwaarts beweegt.
3. [**Bot regels**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md): Pas standaard of douanebot het filtreren toe om die gegevens van het melden uit te sluiten.
4. [**Regels van de Verwerking**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md): De regels van de Douane die op uw gegevens door uw organisatie worden toegepast. Omvat de afbeelding van [ variabelen van de Contextgegevens ](/help/implement/vars/page-vars/contextdata.md) aan zijn respectieve variabele.
5. **VISTA regels**: De flexibele die regels van de douane op uw gegevens door een consultant van Adobe worden toegepast. De regels van VISTA kunnen potentieel lopen vóór of na de regels van de Verwerking, afhankelijk van de behoeften van uw organisatie. De meeste regels VISTA lopen over het algemeen na de regels van de Verwerking, maar elke organisatie is opstelling verschillend. Neem contact op met uw Adobe-accountteam voor meer informatie over bestaande VISTA-regels.
6. [**de verwerkingsregels van het Kanaal van de Marketing**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md): U kunt [ Regels van de Verwerking gebruiken ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) om gegevens voor gebruik in de verwerkingsregels van het Kanaal van de Marketing voor te bereiden.
7. **Geolocation gegevens**: De afmetingen die op IP adresraadpleging (bijvoorbeeld, de [&#128279;](/help/components/dimensions/countries.md) dimensie van Landen) vertrouwen zijn bevolkt.
8. [**IP verduistering**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md): Als uw organisatie heeft verkiest om IP adressen in ruwe gegevens te verduisteren, wordt het gedaan nadat alle andere verwerkingsfuncties hebben voltooid.

Op dit punt, wordt de individuele klap geregistreerd in de lijsten van de rapportreeksgegevens. Na het standaard [ latentie ](latency.md) interval, is het beschikbaar in het melden.

## Gegevens wijzigen nadat deze zijn verwerkt

De gegevens in Adobe Analytics zijn meestal permanent, maar er zijn enkele functies die selectieve gegevensaanpassingen of -verwijdering mogelijk maken:

* [**de reparatie API van Gegevens** ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/): geef bepaalde kolommen uit of schrap gewenste rijen van gegevens.
* [**het Beleid van Gegevens**](/help/admin/admin/c-data-governance/an-gdpr-workflow.md): Accomodate privacyverzoeken om gegevens permanent te schrappen.
* [**Classificaties**](/help/components/classifications/classifications-overview.md): Creeer dimensies die op regels of geüploade gegevens worden gebaseerd die u toestaan om gegevens verschillend te organiseren. De onderliggende gegevens van de rapportreeks worden niet gewijzigd, zodat kunt u classificatiegegevens vrij uitgeven of beschrijven.
* [**Virtuele rapportreeksen**](/help/components/vrs/vrs-about.md): Creeer een afwisselende mening van de rapportreeks die de bezoekonderbreking kan veranderen, of [ Analytics van het Apparaat ](/help/components/cda/overview.md) toestaan.
