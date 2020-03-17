---
description: Een publicatiewidget is een container waarmee u marketingrapporten (bladwijzers en dashboards) op een webpagina kunt insluiten. De mensen in uw organisatie die geen toegang tot marketing rapporten hebben kunnen relevante gegevens bekijken.
title: Publishing Widget
topic: Admin tools
uuid: 4ecf6a5a-8a4e-4707-b282-39890eba3c5d
translation-type: tm+mt
source-git-commit: ''

---


# Publishing Widget

Een publicatiewidget is een container waarmee u analyserapporten (bladwijzers en dashboards) op een webpagina kunt insluiten. De mensen in uw organisatie die geen toegang tot de rapporten van de Analyse hebben kunnen relevante gegevens bekijken.

U kunt bijvoorbeeld een dashboard opgeven, zodat bedrijfsleiders het aantal bezoekers van de pagina, het aantal unieke bezoekers van de pagina enzovoort kunnen bekijken.

> [!CAUTION] Er is geen verificatie vereist voor het weergeven van gegevens die zijn gepubliceerd via de publicatiewidget. Daarom moet u gepubliceerde gegevens als niet veiliger beschouwen dan gegevens die naar een e-mailgroep of lijstserver worden verzonden. Gebruik de widget alleen in overeenstemming met de beveiligingsnormen van uw organisatie, bestaande contractuele vereisten en het toepasselijke recht. De het Publiceren Widget verstrekt de capaciteit om, door IP adres of domeinweg te beperken, waar u gegevens kunt publiceren. Deze mechanismen zijn echter uitsluitend bedoeld om onbedoelde gegevensverspreiding te voorkomen en zijn geen effectieve manier om de toegang tot gegevens te beveiligen die via de publicatiewidget worden verspreid.
>
> Adobe is niet verantwoordelijk of aansprakelijk voor gegevens die via de publicatiewidget worden weergegeven.

Omdat publicatiewidget grote verkeersvolumes kan aansturen, behoudt Adobe zich het recht voor om naar eigen goeddunken de publicatiewidgets van een bedrijf uit te schakelen voor oneigenlijk gebruik of overmatig verkeer dat de algehele prestaties beïnvloedt.

## Problemen oplossen - Widget-cache publiceren

De eerste keer dat een gebruiker de geïmplementeerde publicatiewidget ziet, voert de widget het rapport uit. Nadat het rapport in werking wordt gesteld, worden de resultaten toegevoegd aan een geheim voorgeheugen en zijn geldig voor 1 uur. Elke volgende gebruiker die de publicatiewidget binnen het volgende uur weergeeft, ziet de versie in de cache (deze wordt onmiddellijk geretourneerd). Nadat een uur is verstreken, zal elke volgende gebruiker die de publicatiewidget weergeeft, het rapport opnieuw uitvoeren, waarna worden deze resultaten in de cache geplaatst, enzovoort. Op die manier wordt gegarandeerd dat de gegevens ten hoogste één uur oud zijn.

Als u gegevensverschillen ziet tussen de Publishing Widget en de rapportinterface, moet u mogelijk de cache van de Publishing Widget wissen.

1. Klik in de publicatiewidget (zodat de widget focus heeft).
1. Klik op **[!UICONTROL Save]** de widget.
1. Voer de widget opnieuw uit. (In de voorvertoningsmodus wordt de cache van de widget niet gebruikt.)

> [!NOTE] Het publiceren Widgets toont slechts de eerste kolom van gegevens in een rapport.

## Widget-beschrijvingen publiceren {#section_D67478AECCA946B19A3E4C7071EB4871}

| Element | Beschrijving |
|--- |--- |
| Naam | De naam voor de widget. |
| Beschrijving | (Optioneel) Geef een beschrijving op voor de widget. |
| Rapport | Selecteer een map of een dashboard in de vervolgkeuzelijst Rapport bovenaan. Selecteer een rapport of bladwijzer in de vervolgkeuzelijst Onderaan rapport.  Voor deze rapporten is geen verificatie van bezoekers vereist. <br>Wanneer een bezoeker een webpagina laadt die een publicatiewidget bevat, geeft de widget automatisch het gekoppelde rapport weer met de huidige rapportgegevens. De veranderingen in een het Publiceren Widget, zoals het veranderen van het bijbehorende rapport, werken automatisch de rapportoutput voor alle Web-pagina&#39;s bij die widget gebruiken, zonder u de Web-pagina&#39;s moet opnieuw opstellen.</br> |
| Doel | Geef de bestemming voor de widget op.   Doelen moeten een geldige URL-indeling hebben, inclusief het voorvoegsel https:// of https://. Het publiceren van widget Doelen zijn inclusief, wat betekent dat de het Publiceren widget functies op alle URLs die de gespecificeerde Doel omvatten. <br>Bijvoorbeeld, staat een Doel van https://www.corp1.com/sales/ het Publiceren widgets op alle Web-pagina&#39;s bij of onder de verkooppagina op www.corp1.com Website toe.</br> |
