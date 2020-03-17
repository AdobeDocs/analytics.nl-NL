---
description: Importeer volggegevens van toepassingen van derden naar Analytics.
title: Aan de slag met de gegevensconnectors van Analytics
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Overzicht van gegevensconnectors

Adobe biedt organisaties informatie in real-time en uitvoerbaar over hun digitale strategieën en marketinginitiatieven. Met gegevensconnectors kunt u trackinggegevens van andere toepassingen importeren in Analytics, zodat u gegevens van één centrale locatie kunt verzamelen en gebruiken. Als u een van de partnerproducten gebruikt, kunt u een integratie tot stand brengen die de toepassingsgegevens in marketing rapporten invoert. Nadat de toepassing is geïntegreerd, kunt u rapporten genereren met gegevens uit de toepassing.

Bijvoorbeeld, zou een e-mailintegratie een e-mailpartner kunnen willen gebruiken om een e-mailcampagne te verspreiden. Wanneer bezoekers naar uw Website komen wilt u weten welke degenen in antwoord op uw e-mailcampagne kwamen. De schakelaars van gegevens integreren gegevens van uw e-mailpartner in marketing rapporten zodat u deze informatie kunt bepalen om de doeltreffendheid van uw e-mailcampagne te meten.

**Systeemvereisten**

Gegevensconnectors moeten op de juiste wijze worden geïntegreerd met de meeste populaire browsers. De rapporten kijken en functioneren het best op systemen die aan de volgende aanbevelingen voldoen:

* Browser: Microsoft Internet Explorer versie 6 en hoger
* Cookies: Vereist
* JavaScript: Ingeschakeld
* Besturingssysteem: Op Windows gebaseerd
* Macromedia Flash Player: versie 6 of hoger
* Monitorresolutie: 1024x768 (800x600 werkt wel)
* Kleurdiepte: 16 bits of hoger

Bovendien wordt de gegevensverzameling verbeterd wanneer in de webbrowsers van gebruikers JavaScript is ingeschakeld.

**Vereisten**

Voer de volgende handelingen uit voordat u de integratie van gegevensconnectors voor uw product configureert:

* Heb de noodzakelijke toegangsgeloofsbrieven voor de rekening van het partnerproduct, met rechten om tot alle gegevens toegang te hebben u met marketing rapporten wilt integreren. U zou een speciale e-mailrekening voor rapportverdelers en voor bericht betreffende de geïntegreerde verrichtingen kunnen willen tot stand brengen.
* Identificeer de douanevariabelen die uw campagneinformatie houden. Dit wordt algemeen bedoeld als campagne het volgen code, maar uw organisatie zou één of andere andere terminologie kunnen gebruiken.
* Bepaal de gebeurtenissen die u impressies wilt ontvangen en klik op gegevens. U kunt de naam van de gebeurtenissen desgewenst wijzigen.
* Plaats de aangewezen code op uw landingspagina zodat de Analytics aangewezen modellering met de gegevens kan doen die uit het partnerproduct komen. De specifieke instructies voor elk partnerproduct worden gevonden in in de Schakelaars van Gegevens Showcase op het lusje van Middelen.

## Integratie toevoegen

U moet een huidige account hebben om toegang te krijgen tot de [!UICONTROL Data Connectors] bestemmingspagina (console). U wordt ook aangeraden bekend te zijn met Adobe Analytics.

1. Meld u aan bij de Adobe Experience Cloud.
1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Data Connectors]**.
1. Klik op **[!UICONTROL Add New]**.
1. Stap door de **[!UICONTROL Add Integration]** interface.

   Afhankelijk van de individuele productintegratie, zou u specifieke configuratieinformatie als deel van het integratieproces kunnen moeten verstrekken.

   Wanneer de integratie voltooit, toont het pictogram van het partnerproduct op de pagina van het Netwerk van Verbindingen van Gegevens en is beschikbaar in menu&#39;s.

## Console gegevensverbindingen

Nadat u een integratie hebt geactiveerd, wordt deze weergegeven op de [!UICONTROL Data Connectors] pagina. U kunt details bekijken en configuratieveranderingen op de console aanbrengen. U kunt actieve integratie en integratie over alle rapportreeksen in uw bedrijf bekijken. U kunt een activiteitenlogboek ook bekijken, een integratie plaatsen als dashboard, een integratie vormen, en hulp vinden.

![Data Connectors-console](assets/data-connectors-console.png)

## Marketingsegmenten in gegevensconnectors

Markeringssegmenten zijn gegevensbestanden die worden gemaakt op basis van de variabelen die worden gebruikt in de integratie van gegevensconnectors.

Adobe Analytics verzendt deze gegevens in afzonderlijke dagelijkse bestanden via gegevensopslagruimte naar een FTP-bestand dat door Adobe voor derden is gemaakt. De derde verspreidt deze bestanden vervolgens naar de client. Bedrijven gebruiken deze doorgaans om producten weer op de markt te brengen voor bedrijven die de site hebben bezocht en een product hebben bekeken, maar die het niet hebben gekocht. (U kunt bijvoorbeeld een klant bereiken die een korting aanbiedt voor een product dat hij heeft bekeken, maar dat niet uiteindelijk heeft aangeschaft.)

**Segmenten**

* [!UICONTROL Cart Abandonment]: Het percentage bezoekers heeft een artikel aan hun winkelwagentje toegevoegd, maar heeft het niet aangeschaft. Het is technisch een berekende metrische samenstelling die van Orders door de Toevoegingen van de Kar wordt gedeeld.
* [!UICONTROL Purchases]: De ontvanger-id&#39;s (of bezoeker-id&#39;s) die aankopen hebben gedaan op basis van de bericht-id in een specifiek product.
* [!UICONTROL Product Views]: Vergelijkbaar met [!UICONTROL Cart Abandonment], is dit ook een berekende metrisch. Het rapporteert [!UICONTROL Product Views] verdeeld door Orders, omdat klanten die het product bekijken enige interesse tonen.

**Voorbeelden van implementatie**

Voor een geslaagde implementatie van hermarketingsegmenten moet aan de volgende voorwaarden worden voldaan:

* Er is een contract voor gegevensverbindingen tot stand gebracht en uw organisatie heeft de implementatiefase met een Adobe-consultant voltooid.
* De overeenkomstige gebeurtenis wordt tezelfdertijd geactiveerd de productvariabele:
   * Afschaffing van winkelwagentje: `scAdd` gebeurtenis
   * Aankopen: `purchase` gebeurtenis
   * Productweergaven: `prodView` gebeurtenis

> [!NOTE] Als het product zonder een bijbehorende gebeurtenis wordt gedefinieerd, wordt de gebeurtenis prodView automatisch geactiveerd.
Indien niet aan de bovenstaande vereisten wordt voldaan, worden de corresponderende hermarketingsegmenten niet correct gerapporteerd.

[!UICONTROL Cart Abandonment]: branden nadat de gebruiker een product aan het winkelwagentje heeft toegevoegd :

```
s.products=";cat";
s.events="scAdd";
```

[!UICONTROL Purchases]: wordt op de pagina met aankoopbevestiging geactiveerd:

```
s.products=";
cat;1;50";
s.events="purchase";
//Note: Though optional, adding the purchaseID variable increases accuracy by preventing duplicate purchases
```

**Vaak voorkomende problemen**

| Probleem | Beschrijving |
| -----------| ---------- |  
| Er worden geen product-id-gegevens weergegeven in het opmerkingensegment-bestand. | Vindt plaats wanneer de juiste gebeurtenis wordt geactiveerd, maar er is geen productvariabele aanwezig op dezelfde aanvraag voor de afbeelding. Om dit te corrigeren, moet u ervoor zorgen dat de productvariabele en de bijbehorende gebeurtenis op dezelfde pagina worden geactiveerd, zoals in de bovenstaande implementatievoorbeelden wordt getoond. |
| De dossiers van het opmerkingssegment worden niet ontvangen. | Als u uw dossiers niet ontvangt, hebben één van de gesteunde gebruikers van uw organisatie contact ClientCare om de oorzaak van rapporten te onderzoeken die niet met succes worden ontvangen. |


> [!IMPORTANT] Het is gebruikelijk voor consultants om ook een verzoek voor een gegevenspaket in te stellen als een dagelijks gepland rapport naast het standaardbestand voor het remarketingsegment van de gegevensconnectors-integratie. Dit verzoek van het gegevenspakhuis zou gegevensconnectorvariabelen evenals niet-gegevens connectorvariabelen omvatten, en het verzoek kan worden gepland gebaseerd slechts op het specifieke verzoek van uw organisatie. Om verwarring te verhinderen wanneer het oplossen van problemen, specificeer of het dossier in kwestie het daadwerkelijke remarketing segmentdossier is, of een verzoek van het gegevenspakhuis dat niet-genese variabelen bevat.
