---
title: Apparaatanalyse instellen
description: Leer hoe u Cross-Device Analytics instelt als u aan de voorwaarden voldoet.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Apparaatanalyse instellen

>[!NOTE] De documentatie van de Analyse van verschillende apparaten kan worden gewijzigd aangezien de eigenschap verder wordt ontwikkeld. Controleer regelmatig of er updates zijn.

Als aan alle voorwaarden is voldaan, voert u de volgende stappen uit om Apparaatanalyse op andere apparaten in te schakelen. U dient deel uit te maken van een groep met productprofielbeheer of over beheerdersrechten in Adobe Analytics te beschikken om deze stappen te kunnen uitvoeren.

>[!IMPORTANT] Aan alle voorwaarden moet worden voldaan voordat u deze stappen uitvoert. Als niet aan alle voorwaarden wordt voldaan, is de functie niet beschikbaar of werkt deze niet. Zie [Apparaatanalyse](cda-home.md) voor vereisten en beperkingen.

## Kies de rapportsuite voor alle apparaten die wordt ingeschakeld voor CDA

Wanneer uw organisatie is ingericht om CDA te gebruiken, kiest u welke rapportsuite moet worden gebruikt. U kunt deze keuze mededelen via uw Adobe-accountmanager. Adobe schakelt vervolgens de gekozen rapportsuite in voor CDA-verwerking.

## Maak een virtuele-rapportsuite voor meerdere apparaten om de apparaatweergave te bekijken

Beheerders die toegang hebben tot het maken van virtuele rapportsuites, kunnen als volgt virtuele CDA-rapportensuites maken:

1. Navigeer naar [Experience.adobe.com](https://experiencecloud.adobe.com) en meld u aan met uw Adobe-id-referenties.
2. Klik op het pictogram met het 9-raster bovenaan en klik vervolgens op Analytics.
3. Houd de muis boven Componenten en klik vervolgens op Virtuele rapportsets.
4. Klik op Toevoegen.
5. Voer een naam in voor uw virtuele-rapportsuite en zorg ervoor dat de CDA-compatibele rapportsuite is geselecteerd.
6. (Optioneel) Pas een segment toe op de virtuele rapportsuite. Bijvoorbeeld, kunt u een segment toepassen dat de virtuele rapportreeks tot data beperkt nadat CDA werd aangezet en het stitching begon. Dit segment staat gebruikers toe om slechts gestikte datumwaaiers binnen VRS te zien.
7. Klik op het selectievakje &#39;Tijdverwerking rapport inschakelen&#39;, waarmee u meer opties kunt inschakelen, waaronder Apparaatanalyse.
8. Klik op het selectievakje &#39;Gebruikersbezoeken op apparaten plaatsen&#39;.
9. Klik op Doorgaan, voltooi de configuratie van de virtuele rapportsuite en klik op Opslaan.

![CDA-selectievakje](assets/cda-checkbox.png)

## Toevoegingen en wijzigingen aan virtuele-rapportsuites voor meerdere apparaten

Houd rekening met de volgende wijzigingen wanneer Apparaatanalyse is ingeschakeld voor een virtuele rapportsuite:

* Er verschijnt een nieuw apparaatpictogram naast de naam van de virtuele rapportsuite. Dit pictogram is exclusief voor virtuele rapportsuites op meerdere apparaten.
* Er is een nieuwe dimensie beschikbaar met de naam &#39;Identified State&#39;. Deze dimensie bepaalt of de Experience Cloud-id op die hit bekend is door de apparaatgrafiek op dat moment.
* Er zijn nieuwe meetgegevens beschikbaar met de labels &#39;Mensen&#39; en &#39;Unieke apparaten&#39;.
* De metrische &#39;Unieke bezoekers&#39; zijn niet beschikbaar, omdat deze worden vervangen door &#39;Mensen&#39; en &#39;Unieke apparaten&#39;.
* Bij het maken van segmenten wordt de segmentcontainer &#39;Visitor&#39; vervangen door een container &#39;Person&#39;.

## CDA Workspace-sjabloon

Adobe biedt een sjabloon om essentiële gegevens over de prestaties van verschillende apparaten te bekijken.

1. Navigeer naar [Experience.adobe.com](https://experiencecloud.adobe.com) en meld u aan met uw Adobe-id-referenties.
1. Klik op het pictogram met het 9-raster bovenaan en klik vervolgens op Analytics.
1. Klik [!UICONTROL Workspace] bij de bovenkant, dan klik [!UICONTROL Create New Project].
1. Zoek de &quot;Reis-IQ: Sjabloon &quot;Cross-Device Analytics&quot; en klik vervolgens op [!UICONTROL Create].
1. Wijzig desgevraagd de rapportsuite in een pakket dat CDA ondersteunt.

Een project van de Werkruimte van de Analyse wordt gecreeerd dat verscheidene panelen bevat. Bovenaan wordt een inhoudsopgave en een inleiding weergegeven, zodat context aan het rapport en navigatie naar afzonderlijke rapporten mogelijk zijn. Klik op een koppeling in de inhoudsopgave of vouw de accordeon van een deelvenster uit om die rapporten weer te geven.

<!-->The content below is mirrored in /help/analyze/analysis-workspace/build-workspace-project/starter-projects.md<-->

* **Bijzondere notitie voor de leden van de coopgrafiek**: Toont welk gedeelte van uw rapportreeks bezoekers in gebieden bevat waar de co-op grafiek wordt gesteund, en gebieden waar het niet wordt gesteund.
* **Identificatie van gebruikers**: Hiermee kunt u zien hoe vaak bezoekers van uw site worden geïdentificeerd met methoden die zijn gebaseerd op Apparaatanalyse.
* **Grootte** publiek meten: Geeft een vergelijking van &#39;Unieke apparaten&#39; in vergelijking met &#39;Mensen&#39;. Het aandeel van deze twee getallen wordt &#39;apparaatcompressie&#39; genoemd, een berekende metrische waarde die zichtbaar is in dit deelvenster. Deze compressiemetrie is afhankelijk van een groot aantal factoren:
   * De grafiek Coop of Privé gebruiken: In het algemeen zien organisaties die het apparaatco-op gebruiken doorgaans betere compressiesnelheden dan organisaties die de persoonlijke grafiek gebruiken.
   * Aanmeldingsfrequentie: Hoe meer gebruikers zich aanmelden op uw site, des te meer Adobe bezoekers kan identificeren en vastzetten op verschillende apparaten. Sites met een lage aanmeldingsfrequentie hebben ook een lage compressiesnelheid.
   * Bedekking van cloud-id: Alleen bezoekers met een ECID kunnen worden aangesloten. Een lager percentage bezoekers van uw site met een ECID correleert met lagere compressiesnelheden.
   * Meerdere apparaatgebruik: Als bezoekers van uw site niet meerdere apparaten gebruiken, ziet u lagere compressiesnelheden.
   * Korreligheid rapporteren: Compressie per dag is doorgaans kleiner dan compressie per maand of jaar. De kansen voor een individu om veelvoudige apparaten te gebruiken worden kleiner binnen één enkele dag dan over een volledige maand. Het segmenteren, het filtreren, of het gebruiken van breekdimensies kunnen een lagere compressiesnelheid ook tonen.
* **Op personen gebaseerde segmenten**: Bevat een segmentvervolgkeuzelijst waarmee u apparaatspecifieke gegevens kunt weergeven. In dit deelvenster kunt u beter experimenteren met segmenten om te zien hoe het opnemen of uitsluiten van apparaattypen van invloed is op rapporten.
* **Analyseren van de reis** tussen apparaten: Verstrekt stroom en reserverapporten die op apparatentype worden gebaseerd.
* **Apparaatattributie**: Combineer de eigenschappen van Reis IQ en Attribution IQ samen.
* **Overige tips en trucs**: Nuttige onderwerpen rond CDA die u meer uit het gebruiken van het laten komen.
